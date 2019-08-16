```javascript
const bookBy = (author) => {
  return (book) => {
    console.log(`${author} wrote ${book}.`);
  };
};
const booksByRowling = bookBy('J. K. Rowling');

booksByRowling('Harry Potter and the Sorcerer\'s Stone');
// J. K. Rowling wrote Harry Potter and the Sorcerer’s Stone.
booksByRowling('Harry Potter and the Chamber of Secrets');
// J. K. Rowling and the Chamber of Secrets
booksByRowling('Harry Potter and the Prisoner of Azkaban');
// J. K. Rowling wrote Harry Potter and the Prisoner of Azkaban
// Etc.
```
