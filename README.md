# Git komutları 

# Branch

## Yeni branch olusturma

```git branch <branch_adı>```

Komutunu verdiğimizde localimizde yeni bir branch olusturmuş oluruz.

```git checkout -b <branch_adı>```

Komutunu verdiğimizde localimizde yeni bir branch oluştururuz ve o branch'a geçiş
yapar.

```
git checkout <branch_adı> (Oluşturduğumuz yeni brancha geçmek için)
git push -u <remote> <branch_adı>
```
Komutunu verdiğimizde localimizde yeni oluşturduğumuz branchı uzaktaki repoya göndermiş
oluruz.

## Branchlar arası geçiş

```git checkout <branch_adı>```

Komutunu verdiğimizde var olan branchlar arasında geçiş sağlarız.

## Var olan Branchları listeleme

```git branch ```

Localdeki branchları listeler.

```git branch -r```

Uzak depodaki branchları listeler.

```git branch -a```

Hem localdeki hem uzak repodaki branchları listler.

## Localdeki Branchı silme 

```git branch -d <branch_adı>```

Komutunu verdiğimizde adını yazdığımız branch bizim localimizden silinir.Fakat uzaktaki repodan
silinmez.

## Uzaktaki Branchı silme 

```git push <remote> --delete <branch_adı> ```

Komutunu verdiğimizde adını yazdığımız branch uzakdaki depodan silinir.

## Branch birleştirme

```git checkout <birleştirilecek_branch_adı> ```

Birleştireceğimiz brancha geçiş yaptık.

```git merge <birleşecek_branch_adı> ```

Komutunu vererek iki branchı birleştirdik.

```git push -u <remote> <branch_adı> ```

Birleştirdiğimiz branchları uzakdaki repoya pushladık.
