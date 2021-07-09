## Attention mechanism:
### [Book Link](http://d2l.ai/chapter_attention-mechanisms/index.html)
### [reading link:](https://stats.stackexchange.com/questions/421935/what-exactly-are-keys-queries-and-values-in-attention-mechanisms)
### Background:
 - The optic nerve of a primate’s visual system receives massive sensory input, far exceeding what the brain can fully process. Fortunately, not all stimuli are created equal. Focalization and concentration of consciousness have enabled primates to direct attention to objects of interest, such as preys and predators, in the complex visual environment
 - The ability of paying attention to only a small fraction of the information has evolutionary significance, allowing human beings to live and succeed.
 - Nadaraya-Waston kernel regression in 1964 is a simple demonstration of machine learning with attention mechanisms.
 - other types of attention: --> Multi-head attention, self-attention, Bahdanau attention, 
 
 ### Motivation:
 - Since economics studies the allocation of scarce resources, we are in the era of the attention economy, where human attention is treated as a limited, valuable, and scarce commodity that can be exchanged.
 - Numerous business models have been developed to capitalize on it. On music or video streaming services, we either pay attention to their ads or pay money to hide them
 - All in all, information in our environment is not scarce, attention is. 
 -  When inspecting a visual scene, our optic nerve receives information at the order of  108  bits per second, far exceeding what our brain can fully process
 -   Fortunately, our ancestors had learned from experience (also known as data) that not all sensory inputs are created equal.
 -   Throughout human history, the capability of directing attention to only a fraction of information of interest has enabled our brain to allocate resources more smartly to survive, to grow, and to socialize, such as detecting predators, preys, and mates.
 -   Human attention is a limited, valuable, and scarce resource.


### Attention cues in Biology:
    1. nonvolitional cue :   based on the saliency and conspicuity of objects in the environment (noticeble) --biased towards input 
    2. volitional cue    :    task dependent:
- nonvolitional: --> when noticeble object attracts our attention towards it ('i.e red cup of coffiee)
- volitional --> when we put our attention on some object for some task (tsk dependent)

### Queries, Keys, and Values
 - In the context of attention mechanisms, we refer to volitional cues as queries.
 - Given any query, attention mechanisms bias selection over sensory inputs (e.g., intermediate feature representations) via attention pooling. 
 -  **These sensory inputs are called values in the context of attention mechanisms.**
 -   More generally, every value is paired with a key, which can be thought of the nonvolitional cue of that sensory input
 -   **we can design attention pooling so that the given query (volitional cue) can interact with keys (nonvolitional cues), which guides bias selection over values (sensory inputs).**
 
 
 ### Understanding Query, key , value: Q, K , V
 -  In a seq2seq model, we encode the input sequence to a context vector, and then feed this context vector to the decoder to yield expected good output.
 -  However, if the input sequence is long, relying on only one context vector become less effective. We need all the information from the hidden states in the input sequence (encoder) for better decoding (the attention mechanism).
 -  In other words, in this attention mechanism, the context vector is computed as a weighted sum of the values, where the weight assigned to each value is computed by a compatibility function of the query with the corresponding key 

- Query if from decoder hidden state
- key, value--- encoder hidden state
- The score is the compatibility between the query and key, which can be a dot product between the query and key 
- The scores then go through the softmax function to yield a set of weights whose sum equals 1. Each weight multiplies its corresponding values to yield the context vector which utilizes all the input hidden states
- Note that if we manually set the weight of the last input to 1 and all its precedences to 0s, we reduce the attention mechanism to the original seq2seq context vector mechanism. That is, there is no attention to the earlier input encoder states.
- The difference from the above figure is that the queries, keys, and values are transformations of the corresponding input state vectors.
- The transformation is simply a matrix multiplication like this:
- q = the vector representing a word
- K and V = your memory, thus all the words that have been generated before. Note that K and V can be the same (but don't have to).


### Attention Pooling: Nadaraya-Watson Kernel Regression¶
 - interactions between queries (volitional cues) and keys (nonvolitional cues) result in attention pooling.
 - The attention pooling selectively aggregates values (sensory inputs) to produce the output
 - 
 - 

- 

