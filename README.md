# wordle
bool score_guess(char *secret, char *guess, char *result): Initialize bool match to true. Initialize bool array to {false, false, false, false, false} loop through word, check for exact matches. Loop through work, check for partial matches. Set result[5] to null character. Return match

bool valid_guess(char *guess, char **vocabulary, size_t num_words): Loop through num_words, if guess equals vocabulary[i] return true else false

char **load_vocabulary(char *filename, size_t *num_words): Open file with filename for reading. if file not opened successfully, return null. Initialize capacity to 10. Allocate memory for vocabulary array with size capacity. Set num words to 0. Initialize buffer to hold words. while read a word from file into buffer. Remove newline character from buffer. if num_words is greater than or equal to capacity, then double the capacity, realloc for vocabulary array with new capacity. Duplicate the word in buffer and store it in vocabulary[num_words]. Increment num_words by 1. End while. return vocabulary

void free_vocabulary(char **vocabulary, size_t num_words): Loop through num_words, free memory allocated for vocabulary[i].Finally free memory allocated for vocabulary array.
