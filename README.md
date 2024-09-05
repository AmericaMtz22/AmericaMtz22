def analyze_text(file_path=None, text=None): 
    if text is None and file_path is not None:
        text = read_file(file_path)  

    word_count, words = count_words(text)
    sentence_count = count_sentences(text)
    paragraph_count = count_paragraphs(text)
    avg_word_length = average_word_length(words)
    common_words = most_common_words(words)

    print(f"Total Words: {word_count}")
    print(f"number of sentences: {sentence_count}")
    print(f"number of paragraphs: {paragraph_count}")
    print(f"average word length: {avg_word_length:.2f}")
    print(f"Most common words and their frequencies:")
    for word, freq in common_words:
        print(f"  {word}: {freq}")

text = '''In a faraway kingdom, hidden among the highest mountains in the world, lived a dragon named Kaelar. Unlike others of his kind, Kaelar was not feared by the inhabitants of the kingdom; instead, he was their guardian. Every night, he soared through the skies shining with a golden light, for he had the power to control the stars.

Humans left offerings for him at the top of the mountain, asking for protection. But Kaelar, deep in his heart, longed for more than treasure and prayers. He wanted to know the warmth of true friendship, for his loneliness was immense.

One day, a girl named Lyra climbed the mountain to make a wish to the dragon. She did not ask for riches or power, but for Kaelar to come down from his mountain to see the wonders of the world at her side. Moved by her sincerity, the dragon agreed. Together, Lyra and Kaelar traveled through magical lands, facing challenges and discovering that sometimes the greatest treasure is the company of someone who understands you.

From then on, the nights shone even brighter, as Kaelar no longer looked after the kingdom alone, but with his new friend at his side.'''
analyze_text(text=text)
