import graphviz

def create_german_grammar_mindmap():
    # Create a new directed graph
    mindmap = graphviz.Digraph('German Grammar Mindmap', format='png')

    # Add main topics
    mindmap.node('N', 'Nouns and Pronouns')
    mindmap.node('V', 'Verb Tenses')
    mindmap.node('M', 'Moods and Voices')
    mindmap.node('W', 'Word Order')
    mindmap.node('Mod', 'Modifiers')
    mindmap.node('O', 'Other Features')

    # Add subtopics for Nouns and Pronouns
    mindmap.node('G', 'Genders and Plurals')
    mindmap.node('C', 'Cases: Nominative, Accusative, Dative, Genitive')
    mindmap.node('PN', 'Personal Pronouns')
    mindmap.node('RP', 'Relative Pronouns')
    mindmap.node('AN', 'Adjectival Nouns')
    mindmap.edges([('N', 'G'), ('N', 'C'), ('N', 'PN'), ('N', 'RP'), ('N', 'AN')])

    # Add subtopics for Verb Tenses
    mindmap.node('Pr', 'Present Tense')
    mindmap.node('PP', 'Present Perfect')
    mindmap.node('SP', 'Simple Past')
    mindmap.node('FP', 'Future Perfect')
    mindmap.node('F', 'Future Tense')
    mindmap.node('PaP', 'Past Perfect')
    mindmap.edges([('V', 'Pr'), ('V', 'PP'), ('V', 'SP'), ('V', 'FP'), ('V', 'F'), ('V', 'PaP')])

    # Add subtopics for Moods and Voices
    mindmap.node('Imp', 'Imperative Mood')
    mindmap.node('Pas', 'Passive Voice')
    mindmap.node('Sub1', 'Subjunctive I')
    mindmap.node('Sub2', 'Subjunctive II')
    mindmap.node('Ref', 'Reflexive Verbs')
    mindmap.node('Las', 'Lassen Construction')
    mindmap.edges([('M', 'Imp'), ('M', 'Pas'), ('M', 'Sub1'), ('M', 'Sub2'), ('M', 'Ref'), ('M', 'Las')])

    # Add subtopics for Word Order
    mindmap.node('MC', 'Main Clauses')
    mindmap.node('Q', 'Questions')
    mindmap.node('RC', 'Relative Clauses')
    mindmap.node('DC', 'Dependent Clauses')
    mindmap.node('IC', 'Infinitive Clauses')
    mindmap.node('CS', 'Compound Sentences')
    mindmap.edges([('W', 'MC'), ('W', 'Q'), ('W', 'RC'), ('W', 'DC'), ('W', 'IC'), ('W', 'CS')])

    # Add subtopics for Modifiers
    mindmap.node('AE', 'Adjective Endings')
    mindmap.node('Comp', 'Comparatives and Superlatives')
    mindmap.node('TE', 'Time Expressions')
    mindmap.node('EM', 'Extended Modifiers')
    mindmap.node('PP', 'Prepositions')
    mindmap.node('AP', 'Augmentative Prefixes')
    mindmap.edges([('Mod', 'AE'), ('Mod', 'Comp'), ('Mod', 'TE'), ('Mod', 'EM'), ('Mod', 'PP'), ('Mod', 'AP')])

    # Add subtopics for Other Features
    mindmap.node('MA', 'Modal Auxiliaries')
    mindmap.node('Neg', 'Negations')
    mindmap.node('SP', 'Separable Prefixes')
    mindmap.node('IP', 'Inseparable Prefixes')
    mindmap.node('CW', 'Compound Words')
    mindmap.node('WF', 'Word Formation')
    mindmap.node('Ab', 'Abbreviations')
    mindmap.edges([('O', 'MA'), ('O', 'Neg'), ('O', 'SP'), ('O', 'IP'), ('O', 'CW'), ('O', 'WF'), ('O', 'Ab')])

    # Render the mindmap
    mindmap.render('/mnt/data/German_Grammar_Mindmap', cleanup=True)

# Generate the mindmap
create_german_grammar_mindmap()
