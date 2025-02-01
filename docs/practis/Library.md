図書館で本を管理するシステムを作ってください

1. 本のクラス設計
* クラス名: Book
* プロパティ:
    * BookId (int) - 本のID
    * Title (string) - 本のタイトル
    * Author (string) - 著者名
    * IsAvailable (bool) - 貸出可能かどうかの状態
* メソッド:
    * DisplayInfo() - 本の情報を表示する
    * BorrowBook() - 本を借りる（貸出可能ならIsAvailableをfalseにする）
    * ReturnBook() - 本を返却する（IsAvailableをtrueにする）
2. ユーザー情報の管理
* クラス名: User
* プロパティ:
    * UserId (int) - ユーザーID
    * Name (string) - ユーザー名
    * BorrowedBooks (List<Book>) - ユーザーが借りている本のリスト
* メソッド:
    * BorrowBook(Book book) - 本を借りる機能（借りられる本の上限を設定しても良い）
    * ReturnBook(Book book) - 本を返却する機能
    * DisplayBorrowedBooks() - 借りた本の情報を表示する
3. 貸出管理機能
* クラス名: Library
* プロパティ:
    * Books (List<Book>) - 図書館にある本のリスト
    * Users (List<User>) - 図書館の利用者リスト
* メソッド:
    * AddBook(Book book) - 新しい本を追加する
    * RegisterUser(User user) - 新しいユーザーを登録する
    * BorrowBook(int userId, int bookId) - ユーザーが本を借りる
    * ReturnBook(int userId, int bookId) - ユーザーが本を返却する
    * DisplayAvailableBooks() - 図書館にある全ての貸出可能な本を表示する