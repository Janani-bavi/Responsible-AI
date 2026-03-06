import math
import numpy as np
from collections import Counter
import  re
import nltk
from nltk.util import ngrams
nltk.download('punkt')

def calculate_perplexity(text, n=2):
    text = re.sub(r'[^\w\s]', '', text.lower())
    tokens = nltk.word_tokenize(text)
    if not tokens:
        return 0.0
    n_grams = list(ngrams(tokens, n))
    freq_dist = nltk.FreqDist(n_grams)
    N = len(n_grams)
    entropy = -sum( (freq_dist[ng] * math.log2(freq_dist[ng]/N)for ng in freq_dist)
    perplexity = 2 ** entropy if N>0 else 0.0
    return perplexity
        def calculate_burstiness(text):
              tokens=nltk.word_tokenize(text)
              word_positions={}
                            for i,word in enumerate(tokens):
                            if word not in word_positions:
              word_positions[word]=[]
    word_positions[word].append(i)
    burstiness_scores=[]
    for word,positions in word_positions.items():
        if(len(positions)>1:
           gaps=np.diff(positions)
            if np.mean(gaps)>0:
                burstiness=np.std(gaps)/np.mean(gaps)
                burstiness_scores.append(burstiness)
                return np.mean(burstiness_scores) if burstiness_scores else 0.0
                sample_text = "AI models can generate human-like text with ease. The quick brown fox jumps over the lazy dog."
print(f"Perplexity: {calculate_perplexity(sample_text)}")
print(f"Burstiness: {calculate_burstiness(sample_text)}")
