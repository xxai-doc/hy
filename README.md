<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

Առաջարկվում է սկզբում տեղադրել nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) , իսկ հետո [տեղեկատու](https://github.com/xxai-art/doc/blob/main/.envrc) մուտքագրելուց հետո `direnv allow` .

Իմաստն է՝ չինարեն թարգմանություն ճապոներեն, կորեերեն, անգլերեն, անգլերեն թարգմանություն բոլոր մյուս լեզուներով: Եթե ​​ցանկանում եք աջակցել միայն չինարենին և անգլերենին, կարող եք պարզապես գրել `zh: en` .

## ճակատային ծածկագիր

* [ճակատային ծածկագիր](https://github.com/xxai-art/web)
* [Լեզուների փաթեթներ կայքի համար որպես ամբողջություն](https://github.com/xxai-art/web/tree/main/i18n)
* [Լեզուների փաթեթներ մուտքի մոդուլների համար](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Կայքի բազմալեզու փաստաթղթեր](https://github.com/xxai-doc)

Առջևի ծրագրավորման լեզուն [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) է, որն ավելացնում է որոշ առանձնահատկություններ՝ հիմնված coffeescript շարահյուսության վրա, տես [./coffee_plus.md](./coffee_plus.md) :

## Կայքերի և փաստաթղթերի միջազգայնացում

Կառուցեք հետևյալ 3 նախագծերի վրա

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  Վերջածանցը `.mdt` է, դուք կարող եք օգտագործել `<+ ./coffee_plus/import.js>` ի նման շարահյուսությունը՝ արտաքին ֆայլերին անդրադառնալու համար և `.md` վերջածանցով նշագծեր առաջացնել:

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  Markdown թարգմանությունը չի թարգմանի ծածկագրերն ու հղումները, և կքեշի թարգմանված նախադասությունները: Եթե ​​թարգմանությունը փոփոխված է, բայց բնօրինակ տեքստը փոփոխված չէ, այն նորից կատարելը չի ​​վերագրի թարգմանության փոփոխությունը:

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  `yaml` ստեղծած կայքերի թարգմանության լեզվական ֆայլեր:

### Փաստաթղթերի թարգմանության ավտոմատացման հրահանգներ

Տե՛ս կոդերի պահոց [xxai-art/doc](https://github.com/xxai-art/doc)

Առաջարկվում է սկզբում տեղադրել nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) , իսկ հետո [տեղեկատու](https://github.com/xxai-art/doc/blob/main/.envrc) մուտքագրելուց հետո `direnv allow` .

Հարյուրավոր լեզուներով թարգմանված կոդերի մեծ բազայից խուսափելու համար ես յուրաքանչյուր լեզվի համար ստեղծեցի կոդերի առանձին բազա և ստեղծեցի կազմակերպություն՝ կոդերի բազան պահելու համար:

Շրջակա միջավայրի `GITHUB_ACCESS_TOKEN` փոփոխականի կարգավորումը և այնուհետև գործարկելը [create.github.coffee-ն](https://github.com/xxai-art/doc/blob/main/create.github.coffee) ավտոմատ կերպով կստեղծի կոդի պահոցը:

Իհարկե, դուք կարող եք նաև տեղադրել այն կոդի բազայում:

Թարգմանության սցենարի հղում [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Սցենարի կոդը մեկնաբանվում է հետևյալ կերպ.

[bux-ը](https://bun.sh/docs/cli/bunx) փոխարինում է npx-ին, որն ավելի արագ է: Իհարկե, եթե դուք չունեք տեղադրված bun, փոխարենը կարող եք օգտագործել `npx` :

`bunx mdt zh` ը `.mdt` zh գրացուցակում ներկայացնում է որպես `.md` , տես ստորև նշված 2 կապված ֆայլերը:

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` թարգմանության հիմնական կոդը է (եթե դուք ունեք միայն `nodejs` տեղադրված, բայց `bun` և `direnv` տեղադրված չեն, կարող եք նաև գործարկել `npx i18n` ՝ թարգմանելու համար):

Այն կվերլուծի [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) , այս փաստաթղթում `i18n.yml` ի կոնֆիգուրացիան հետևյալն է.

```
en:
zh: ja ko en
```

Իմաստն է՝ չինարեն թարգմանություն ճապոներեն, կորեերեն, անգլերեն, անգլերեն թարգմանություն բոլոր մյուս լեզուներով: Եթե ​​ցանկանում եք աջակցել միայն չինարենին և անգլերենին, կարող եք պարզապես գրել `zh: en` .

Վերջինը [gen.README.coffee-ն](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) է, որը հանում է բովանդակությունը յուրաքանչյուր լեզվի `README.md` ի հիմնական վերնագրի և առաջին ենթավերնագրի միջև՝ `README.md` մուտքագրելու համար: Կոդը շատ պարզ է, կարող եք ինքներդ նայել դրան։

Google API-ն օգտագործվում է անվճար թարգմանության համար: Եթե ​​չեք կարող մուտք գործել Google, խնդրում ենք կարգավորել և սահմանել վստահված անձ, ինչպիսին է՝

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Թարգմանության սկրիպտը կստեղծի թարգմանված քեշ `.i18n` գրացուցակում, խնդրում ենք ստուգել այն `git status` և ավելացնել կոդի պահեստում՝ կրկնվող թարգմանություններից խուսափելու համար:

Խնդրում ենք գործարկել `bunx i18n` ամեն անգամ, երբ փոփոխում եք թարգմանությունը՝ քեշը թարմացնելու համար:

Եթե ​​բնօրինակ տեքստը և թարգմանությունը փոփոխվեն միաժամանակ, քեշը կշփոթվի, այնպես որ, եթե ցանկանում եք փոփոխել, կարող եք փոփոխել միայն մեկը, այնուհետև գործարկել `bunx i18n` ՝ քեշը թարմացնելու համար:
