class Solution:
    def ladderLength(self, beginWord: str, endWord: str, wordList: List[str]) -> int:
        

        st = set(wordList)
        
        
        q = []
        q.append([beginWord, 1])
        
        while q:
            word, step = q.pop(0)
            if word == endWord:
                return step
            
            for i in range(len(word)):
                for ch in 'abcdefghijklmnopqrstuvwxyz':
                    new_word = word[:i] + ch + word[i+1:]
                    if new_word in st:
                        st.remove(new_word)
                        q.append((new_word, step+1))
        
        return 0
