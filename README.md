<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art

Կայքի կոդի մի մասը բաց կոդ է, բարի գալուստ՝ օգնելու թարգմանության օպտիմալացմանը:

## ճակատային ծածկագիր

* [ճակատային ծածկագիր](https://github.com/xxai-art/web)
* [Լեզուների փաթեթներ կայքի համար որպես ամբողջություն](https://github.com/xxai-art/web/tree/main/i18n)
* [Լեզուների փաթեթներ մուտքի մոդուլների համար](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Կայքի բազմալեզու փաստաթղթեր](https://github.com/xxai-doc)

Առջևի ծրագրավորման լեզուն [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) է, որն ավելացնում է որոշ առանձնահատկություններ՝ հիմնված coffeescript շարահյուսության վրա, տես [./coffee_plus.md](./coffee_plus.md) :

## Կայքերի և փաստաթղթերի միջազգայնացում

Կառուցեք հետևյալ 3 նախագծերի վրա

### [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

Նշման ձևանմուշը, `.mdt` վերջածանցով, կարող է վերաբերել արտաքին ֆայլերին շարահյուսությամբ, որը նման է `<+ ./coffee_plus/import.js>` :

[@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

Markdown թարգմանությունը չի թարգմանի կոդերը և հղումները, և կքեշի թարգմանված նախադասությունները: Եթե ​​թարգմանությունը փոփոխված է, բայց բնօրինակ տեքստը փոփոխված չէ, այն նորից կատարելը չի ​​վերագրի թարգմանության փոփոխությունը:

[@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

`yaml` ստեղծած կայքերի թարգմանության լեզվական ֆայլեր:
