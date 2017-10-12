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

Komutunu verdiğimizde var olan branchlar listelenir.

## Localdeki Branchı silme 

```git branch -d <branch_adı>```

Komutunu verdiğimizde adını yazdığımız branch bizim localimizden silinir.Fakat uzaktaki repodan
silinmez.

## Uzaktaki Branchı silme 

```git push <remote> --delete <branch_adı> ```

Komutunu verdiğimizde adını yazdığımız branch uzakdaki depodan silinir.
