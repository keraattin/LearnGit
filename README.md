# Git komutları 

## Config 

```git config --global user.email "<e-mail>" ```


```git config --global user.name "<username>" ```

Commitlerimizde görüncek kimliğimizi belirlemek için bu konfigrasyonları yapmalıyız.
Burada yazacağımız mail adresi ve kullanıcı adımızın github veya bitbucket da kullandıklarımız
olmasına dikkat etmeliyiz.

## Remote

Remote uzun linkleri kısaltmamıza ve onları bir isim ile bağdaştırmamızı sağlar.

### Yeni remote ekleme 

```git remote add <remote_adı> https://github.com/<username>/<repo_adı>.git ```

Komutunu verdiğimizde <remote_adı> kısmına yazdığımız isim ile linki kısaltmış oluruz.

### Remoteları listeleme

```git remote -v ```

### Bir Remote'nin ismini değiştirme

```git remote rename <remote_adı> <yeni_remote_adı> ```

Komutunu verdiğimizde remote ismini değiştirmiş oluruz.

### Remote silme

```git remote rm <remote_adı>```

Komutunu verdiğimizde adını yazdığımız remote'yi sileriz.

### Bir Remote'nin linkini değiştirme

```git remote set-url <remote_adı> https://github.com/<username>/<repo_adı>.git ```

Komutu ile remote ların işaret ettiği linki değiştirebiliriz.

## İnit

### Var olan bir projeyi locale çekme

```git clone https://github.com/<username>/<repo_adı>.git ```

Komutunu verdiğimizde projeyi localimize çekmiş oluyoruz ve otomatik olarak "origin" adında
bir remote eklenmiş oluyor.

### Localde yeni bir depo oluşturma

Projenin bulunduğu dizine geçip 

```git init ```

komutunu verdiğimizde localimizde yeni bir depo oluşturmuş oluruz.

## Diff

### Yapılan değişiklikleri görme

```git diff ```

Komutu ile commitlenmemiş yapılan değişiklikleri görebiliriz.

### Bir dosya üzerinde yapılan değişiklikleri görme

```git diff <dosya_adı> ```

Komutu ile bir dosya üzerinde yapılan değişiklikleri görebiliriz.

### Belirtilen Commit ile deponun şu an ki hali arasındaki değişiklikleri görme 

```git diff <commit_id> ```

Komutu ile yazdığımız commit ile deponun şu an ki hali arasındaki değişiklikleri görebiliriz.

### 2 commit arasındaki değişiklikleri görme 

```git diff <commit_id> <commit_id> ```

Komutu ile 2 commit arasındaki yapılan değişikleri görebiliriz.

### Sadece değişiklik yapılan dosya isimlerini görme

```git diff --name-only ```

Komutu ile sadece değişiklik yapılan dosyaların adını listeyebilirz.

### 2 versiyon arasındaki değişiklikleri görme

```git diff <tag_adı> <tag_adı> ```

Komutunu vererek 2 versiyon arasındaki değişiklikleri görebiliriz.

## Push 

Localdeki commitlenmiş değişikleri uzaktaki depoya göndermemizi sağlar.

```git push <remote_adı> <branch_adı> ```

## Commit 

```git commit -m "<commit_mesajı> ```

Komutunu verdiğimizde stagged olan dosyalara mesaj ile bir commit atmış oluruz.
Her commit bir mesaj içermelidir.

```git commit -a -m "<commit_mesajı> ```

Komutunu verdiğimizde stagged olmayan ama değişiklik yapılan tüm dosyaları 
staged yapar ve bir mesaj ile commit atmış olur.


## Tag - Version

### Tag olusturma 

```git tag <tag> ```

Komutunu verdiğimizde son atılan commit için tag oluşturur ve eğer 
pushlarsak onu realese olarak yayınlar.

### Oluşturduğumuz tag'i uzaktaki depoya gönderme

```git push <remote_adı> <tag>```

Komutunu verdiğimizde oluşturduğumuz tag uzaktaki depoya pushlanır.

### Tagleri listeleme

```git tag ```

veya

```git tag -l ```

Komutu ile oluşturdğumuz tagleri görebiliriz.

### Localdeki tag'i silme 

```git tag -d <tag_adı> ```

Komutu ile localdeki tagı sileriz ama uzak depodaki tag silinmez.

### Uzak depodaki tag'i silme

```git push origin :<tag_adı> ```

veya

```git push --delete <remote_adı> <tag_adı> ```

Komutlarından biri ile uzak depodaki tagleri silmiş oluruz.

### Tag güncelleme 

```git tag --force <tag_adı> <commit_id>```

Komutunu verdiğimizde localimizde tagı güncellemiş oluruz.

```git push --force --tags```

Komutunu verince de uzaktaki depodaki tagı güncellemiş oluruz.
## Branch

### Yeni branch olusturma

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

### Branchlar arası geçiş

```git checkout <branch_adı>```

Komutunu verdiğimizde var olan branchlar arasında geçiş sağlarız.

### Var olan Branchları listeleme

```git branch ```

Localdeki branchları listeler.

```git branch -r```

Uzak depodaki branchları listeler.

```git branch -a```

Hem localdeki hem uzak repodaki branchları listler.

### Localdeki Branchı silme 

```git branch -d <branch_adı>```

Komutunu verdiğimizde adını yazdığımız branch bizim localimizden silinir.Fakat uzaktaki repodan
silinmez.

### Uzaktaki Branchı silme 

```git push <remote> --delete <branch_adı> ```

Komutunu verdiğimizde adını yazdığımız branch uzakdaki depodan silinir.

### Branch birleştirme

```git checkout <birleştirilecek_branch_adı> ```

Birleştireceğimiz brancha geçiş yaptık.

```git merge <birleşecek_branch_adı> ```

Komutunu vererek iki branchı birleştirdik.

```git push -u <remote> <branch_adı> ```

Birleştirdiğimiz branchları uzakdaki repoya pushladık.

### Branch ismi değiştirme 

```git branch -m <branch_adı> <yeni_branch_adı>```

Komutu ile localde branchımızın adını değiştirdik.

```git push <remote> :<eski_branch_adı> <yeni_branch_adı>```

## Reset

### Bir dosyada yapılan değişiklikleri geri almak için

```git checkout <dosya_adı>```


### Commitlenmemiş ama staged area'ya geçmiş değişiklikleri geri almak için

```git reset <dosya_adı>```

### Projede belirli bir commite geri dönme

```git reset --soft <commit_id>```

Komutunu verdiğimizde id sini yazdığımız commite geri döneriz fakat commitler silinmez. 
Sonra bu değişiklikleri uzaktaki depoya pushlamak için:

```git push <remote> <branch_adı> --force```

### Projede belirli bir commite geri dönme ve ondan sonraki commitleri silme

```git reset --hard <commit_id>```

Komutunu verdiğimizde id sini yazdığımız commite geri döneriz ve geri döndüğümüz committen sonraki
bütün commitler silinir.
Sonra bu değişiklikleri uzaktaki depoya pushlamak için:

```git push <remote> <branch_adı> --force```

### Projeyi belirli bir taglenmiş zamana geri döndürme

```git reset --hard <tag_adı>```

Komutunu verdiğimizde projemiz yazdığımız tagdeki haline döner. Verdiğimiz tagden sonraki commitler
silinir. 
Sonra bu değişiklikleri uzaktaki depoya pushlamak için:

```git push <remote> <branch_adı> --force```

