## Create Operation

**Command**:
```python
from bookshelf.models import Book
Book.objects.create()
book = Book(title="1984", author="George Orwell", publication_year=1949)
book.save()