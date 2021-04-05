---
title: Appendice E attributi di testo per Active Accessibility dizionario dei servizi di testo
description: In questa appendice vengono fornite informazioni sugli attributi di testo definiti in IAccDictionary.
ms.assetid: 9e405140-c151-4f00-91c5-777c84c41806
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588c827764d17c2576efaa5e3117527e23d1da26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047308"
---
# <a name="appendix-e-text-attributes-for-active-accessibility-text-services-dictionary"></a>Appendice E: attributi di testo per Active Accessibility dizionario dei servizi di testo

In questa appendice vengono fornite informazioni sugli attributi di testo definiti in [**IAccDictionary**](/windows/desktop/api/msaatext/nn-msaatext-iaccdictionary). È organizzata come una serie di tabelle. Ogni tabella include informazioni su una categoria specifica di attributi. Queste categorie sono effettivamente annidate, ma sono separate di seguito in modo che sia possibile visualizzare gli attributi.

> [!Note]  
> Active Accessibility servizi di testo è deprecato. Per ulteriori informazioni sull'input di testo avanzato e sulle tecnologie per il linguaggio naturale, vedere [Microsoft Windows Text Services Framework](../tsf/text-services-framework.md) .

 

Ogni voce di una tabella fornisce un nome di attributo e un nome descrittivo, un tipo, Cascading Style Sheets (CSS) equivalente, un modello a oggetti di testo (TOM) equivalente ed eventuali commenti aggiuntivi laddove appropriato. La colonna equivalente di TOM fornisce informazioni sul metodo TOM usato con l'attributo (parte delle interfacce [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont), [**ITextRange**](/windows/desktop/api/tom/nn-tom-itextrange)o [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) ). Le informazioni precedenti a ogni tabella indicano quale interfaccia supporta gli attributi; le informazioni nella tabella equivalente di TOM indicano il nome del metodo. Ogni voce nella colonna equivalente di TOM è associata a due metodi. La voce Name, ad esempio, è associata ai metodi **GetName** e **Sename** .

Per ulteriori informazioni su queste interfacce, vedere la documentazione del [modello a oggetti di testo](../controls/text-object-model.md) in Windows Software Development Kit (SDK).

## <a name="font"></a>Carattere

Gli attributi nella tabella seguente sono associati agli attributi del tipo di carattere generale. L'equivalente di TOM è l'interfaccia [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nome attributo, nome descrittivo       | Tipo     | Equivalente CSS       | Equivalente TOM | Commento           |
|-------------------------------------|----------|----------------------|----------------|-------------------|
| Tipo \_ di carattere, facet<br/> | \_BSTR VT | Font-family: Verdana | Nome           |                   |
| Carattere \_ SizePts, SizePts<br/>   | VT \_ I4   | Font-size: XPT       | Dimensione           | Dimensioni in punti |



 

## <a name="font_style"></a>\_Stile carattere

Gli attributi nella tabella seguente specificano gli attributi di stile del tipo di carattere, ad esempio se il testo è impostato in grassetto o in corsivo. L'equivalente di TOM è l'interfaccia [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nome attributo, nome descrittivo                             | Tipo     | Equivalente CSS              | Equivalente TOM                                            | Commento                   |
|-----------------------------------------------------------|----------|-----------------------------|-----------------------------------------------------------|---------------------------|
| Stile del carattere \_ \_ grassetto, grassetto<br/>                        | \_bool VT | Carattere-spessore: grassetto           | Grassetto                                                      |                           |
| Stile del carattere \_ \_ corsivo, corsivo<br/>                    | \_bool VT | Tipo di carattere: corsivo          | Corsivo                                                    |                           |
| Stile del carattere \_ \_ SmallCaps, SmallCaps<br/>              | \_bool VT | Font-variant: Small-Caps    | SmallCaps                                                 |                           |
| \_Stile carattere \_ maiuscolo, maiuscolo<br/>             | \_bool VT | Trasformazione testo: maiuscole  | Non supportato                                             |                           |
| \_Stile carattere \_ maiuscolo, maiuscolo<br/>               | \_bool VT | Trasformazione testo: maiuscolo   | AllCaps                                                   |                           |
| \_Stile carattere \_ minuscolo, minuscolo<br/>               | \_bool VT | Trasformazione testo: minuscolo   | Non supportato                                             |                           |
| \_Rilievo stile carattere \_ , rilievo<br/>                     | \_bool VT | Non supportato               | Rilievo                                                    |                           |
| Stile del tipo \_ \_ di carattere, grave<br/>                   | \_bool VT | Non supportato               | Incidere                                                   |                           |
| \_Stile carattere \_ nascosto                                       | \_bool VT | Non supportato               | Nascosto                                                    |                           |
| \_Crenatura dello stile del tipo \_ di carattere, crenatura<br/>                   | \_R4 VT   | Non supportato               | Crenatura                                                   | Stessi valori di GetKerning |
| \_Stile carattere \_ illustrato, delineato<br/>                 | \_bool VT | Non supportato               | Delineato                                                  |                           |
| \_Posizione stile carattere \_ , posizione<br/>                 | \_R4 VT   | Non supportato               | Posizione                                                  |                           |
| \_Stile carattere \_ protetto                                    | \_bool VT | Non supportato               | Protetta                                                 |                           |
| \_ \_ Ombreggiatura stile carattere, ombreggiatura<br/>                     | \_bool VT | Riga-altezza (meno numeri) | Ombreggiatura                                                    |                           |
| \_ \_ Spaziatura stile carattere, spaziatura<br/>                   | \_R4 VT   | Spaziatura delle lettere              | Spaziatura                                                   | In punti                 |
| Spessore \_ stile carattere \_ , peso<br/>                     | VT \_ I4   | Carattere-spessore                 | WeightSame i valori come carattere-spessore e getWeight<br/> |                           |
| \_Altezza stile carattere \_ , altezza<br/>                     | \_R4 VT   | Line-height                 | Non supportato                                             | In punti                 |
| \_Stile carattere \_ lampeggiante, lampeggiamento<br/>                       | \_bool VT | Decorazione di testo: lampeggiare      | Non supportato                                             |                           |
| \_Pedice dello stile del tipo \_ di carattere, pedice<br/>               | \_bool VT | Allineamento verticale: Sub         | Indice (posizione anche)                                 |                           |
| Apice dello stile del tipo \_ \_ di carattere, apice<br/>           | \_bool VT | Allineamento verticale: Super       | Apice (posizione anche)                               |                           |
| \_Colore stile carattere \_ , colore<br/>                       | VT \_ I4   | Colore                       | ColorePrimoPiano                                                 | Stile RBG COLORREF        |
| \_Stile carattere \_ BackgroundColor, colore di sfondo \_<br/> | VT \_ I4   | Sfondo-colore            | ColoreSfondo                                                 | Stile RBG COLORREF        |



 

## <a name="font_style_animation"></a>\_Animazione stile \_ carattere

Gli attributi nella tabella seguente corrispondono all'animazione del tipo di carattere. L'equivalente di TOM è l'interfaccia [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nome attributo, nome descrittivo                                              | Tipo     | Equivalente CSS | Equivalente TOM |
|----------------------------------------------------------------------------|----------|----------------|----------------|
| \_Animazione stile \_ carattere \_ LasVegasLights, LasVegas \_ luci<br/>         | \_bool VT | Non supportato  | Animazione      |
| \_Animazione dello stile del tipo \_ di carattere \_ BlinkingBackground, sfondo lampeggiante \_<br/> | \_bool VT | Non supportato  | Animazione      |
| \_Animazione dello stile del tipo \_ di carattere \_ SparkleText, \_ testo Spark<br/>               | \_bool VT | Non supportato  | Animazione      |
| \_Animazione dello stile del tipo \_ di carattere \_ MarchingBlackAnts, Marching \_ Black \_ Ants<br/> | \_bool VT | Non supportato  | Animazione      |
| \_Animazione stile \_ carattere \_ MarchingRedAnts, marce \_ rosse \_<br/>     | \_bool VT | Non supportato  | Animazione      |
| \_Animazione stile \_ carattere \_ SHIMMER, SHIMMER<br/>                         | \_bool VT | Non supportato  | Animazione      |
| \_Animazione dello stile del tipo \_ di carattere \_ WipeDown, WipeDown<br/>                       | \_bool VT | Non supportato  | Animazione      |
| \_Animazione dello stile del tipo \_ di carattere \_ WipeRight, WipeRight<br/>                     | \_bool VT | Non supportato  | Animazione      |



 

## <a name="font_style_underline"></a>\_Sottolineato stile carattere \_

Gli attributi nella tabella seguente indirizzano gli stili di sottolineatura per i tipi di carattere. L'equivalente di TOM è l'interfaccia [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nome attributo, nome descrittivo                     | Tipo     | Equivalente CSS                | Equivalente TOM |
|---------------------------------------------------|----------|-------------------------------|----------------|
| \_Tipo \_ di carattere sottolineato \_ singolo, singolo<br/>  | \_bool VT | Decorazione di testo: sottolineatura    | Sottolineato      |
| \_Stile carattere \_ sottolineato \_ doppio, doppio<br/> | \_bool VT | Decorazione di testo: line-through | Barrato  |



 

## <a name="font_style_strikethrough"></a>\_Stile carattere \_ barrato

Gli attributi nella tabella seguente indirizzano gli stili per i tipi di carattere.



| Nome attributo, nome descrittivo                                         | Tipo     | Equivalente CSS | Equivalente TOM |
|-----------------------------------------------------------------------|----------|----------------|----------------|
| \_Stile carattere \_ barrato \_ singolo, \_ attacco \_ singolo<br/> | \_bool VT | Non supportato  | Non supportato  |
| \_Stile carattere \_ barrato \_ doppio, \_ attacco \_ doppio<br/> | \_bool VT | Non supportato  | Non supportato  |



 

## <a name="font_style_overline"></a>\_Allineamento stile \_ carattere

Gli attributi nella tabella seguente indirizzano gli stili di linea per i tipi di carattere.



| Nome attributo, nome descrittivo                             | Tipo     | Equivalente CSS            | Equivalente TOM |
|-----------------------------------------------------------|----------|---------------------------|----------------|
| Carattere \_ \_ \_ di allineamento singolo di tipo carattere, riga \_ singola<br/> | \_bool VT | Decorazione di testo: Overline | Non supportato  |
| Carattere \_ \_ di sovralineatura doppio stile carattere \_ , linea \_ doppia<br/> | \_bool VT | Decorazione di testo: Overline | Non supportato  |



 

## <a name="text"></a>Testo

Gli attributi nella tabella seguente indirizzano gli attributi di formattazione del testo generale.



| Nome attributo, nome descrittivo                     | Tipo        | Equivalente CSS | Equivalente TOM                                       | Commento                                                                               |
|---------------------------------------------------|-------------|----------------|------------------------------------------------------|---------------------------------------------------------------------------------------|
| Testo \_ VerticalWriting, scrittura verticale<br/> | \_bool VT    | Non supportato  | non supportato                                        | Come usato dal cinese/giapponese                                                           |
| RightToLeft del testo \_ , RightToLeft<br/>          | \_bool VT    | Direzione      | Non supportato                                        |                                                                                       |
| Testo \_ ReadOnly, sola lettura<br/>               | \_bool VT    | Non supportato  | ITextFont:: CanChange, ITextRange:: CanEdit            | La proprietà modificabile del documento ha la precedenza                                     |
| Lingua del testo \_ , lingua<br/>                | VT \_ I4      | Non supportato  | ITextFont::GetLanguageID, ITextFont::SetLanguageID   | LANGID                                                                                |
| Orientamento del testo \_ , orientamento<br/>          | VT \_ I4      | Non supportato  | Non supportato                                        | 10??? di un grado                                                                     |
| \_EmbeddedObject di testo, \_ oggetto incorporato<br/>  | \_bool VT    | Non supportato  | Non supportato                                        | Consente la ricerca di oggetti incorporati                                                 |
| \_Collegamento di testo, collegamento<br/>                        | VT \_ sconosciuto | Collegamento           | Non supportato                                        | Puntatore di interfaccia all'oggetto; chiamare QueryInterface per qualsiasi interfaccia di interesse |
| \_Sillabazione del testo, sillabazione<br/>          | \_bool VT    | Non supportato  | ITextPara:: getsillabation, ITextPara:: sesillabazione |                                                                                       |



 

## <a name="text_alignment"></a>Allineamento del testo \_

Gli attributi nella tabella seguente sono indirizzati all'allineamento del testo. L'equivalente di TOM è l'interfaccia [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nome attributo, nome descrittivo               | Tipo     | Equivalente CSS | Equivalente TOM |
|---------------------------------------------|----------|----------------|----------------|
| Allineamento del testo a \_ \_ sinistra, a sinistra<br/>       | \_bool VT | Allineamento testo     | Allineamento      |
| Allineamento del testo a \_ \_ destra, a destra<br/>     | \_bool VT | Allineamento testo     | Allineamento      |
| Allineamento del testo al centro \_ \_<br/>   | \_bool VT | Allineamento testo     | Allineamento      |
| Allineamento del testo \_ \_ giustificato, giustificato<br/> | \_bool VT | Allineamento testo     | Allineamento      |



 

## <a name="text_para"></a>Testo \_ para

Gli attributi nella tabella seguente corrispondono alla formattazione per i paragrafi. L'equivalente di TOM è l'interfaccia [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nome attributo, nome descrittivo                              | Tipo   | Equivalente CSS | Equivalente TOM  | Commento |
|------------------------------------------------------------|--------|----------------|-----------------|---------|
| Testo \_ para \_ FirstLineIndent, primo \_ \_ rientro riga<br/> | \_R4 VT | Non supportato  | FirstLineIndent | In PTS  |
| Testo \_ para \_ LeftIndent, \_ rientro a sinistra<br/>             | \_R4 VT | Non supportato  | LeftIndent      | In PTS  |
| Testo \_ para \_ RightIndent, \_ rientro a destra<br/>           | \_R4 VT | Non supportato  | RightIndent     | In PTS  |
| Testo \_ para \_ SpaceAfter, spazio \_ dopo<br/>             | \_R4 VT | Non supportato  | SpaceAfter      | In PTS  |
| Testo \_ para \_ SpaceBefore, spazio \_ dopo<br/>            | \_R4 VT | Non supportato  | SpaceAfter      | In PTS  |



 

## <a name="text_para_linespacing"></a>Testo \_ para \_ LineSpacing

Gli attributi nella tabella seguente interlineano la spaziatura tra i paragrafi. L'equivalente di TOM è l'interfaccia [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nome attributo, nome descrittivo                               | Tipo     | Equivalente CSS | Equivalente TOM | Commento  |
|-------------------------------------------------------------|----------|----------------|----------------|----------|
| Text \_ para \_ LineSpacing \_ Single, Single<br/>           | \_bool VT | Non supportato  | LineSpacing    |          |
| Text \_ para \_ LineSpacing \_ OnePtFive, One \_ PT \_ cinque<br/> | \_bool VT | Non supportato  | LineSpacing    |          |
| Text \_ para \_ LineSpacing \_ Double, Double<br/>           | \_bool VT | Non supportato  | LineSpacing    |          |
| Testo \_ para \_ LineSpacing almeno \_ , \_ almeno<br/>       | \_R4 VT   | Non supportato  | LineSpacing    | In righe |
| Text \_ para \_ LineSpacing \_ esattamente, esattamente<br/>         | \_R4 VT   | Non supportato  | LineSpacing    | In righe |
| Text \_ para \_ LineSpacing \_ multipli, multiple<br/>        | \_R4 VT   | Non supportato  | LineSpacing    | In righe |



 

## <a name="text_list"></a>Elenco di testo \_

Gli attributi nella tabella seguente elencano gli elenchi e i livelli degli elenchi di testo. L'equivalente di TOM è l'interfaccia [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nome attributo, nome descrittivo | Tipo   | Equivalente CSS | Equivalente TOM | Commento                                                       |
|-------------------------------|--------|----------------|----------------|---------------------------------------------------------------|
| \_Elenco \_ di testo LevelIndex,       | VT \_ I4 | Non supportato  | ListLevelIndex | Dove 1 è l'elenco più esterno, 2 è il livello successivo e così via |



 

## <a name="text_list_type"></a>\_Tipo di elenco di testo \_

Gli attributi nella tabella seguente corrispondono agli stili di elenco per il testo. L'equivalente di TOM è l'interfaccia [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nome attributo, nome descrittivo                          | Tipo     | Equivalente CSS  | Equivalente TOM |
|--------------------------------------------------------|----------|-----------------|----------------|
| \_ \_ Tipo di elenco \_ di testo Bullet, Bullet<br/>             | \_bool VT | Tipo di elenco       | ListType       |
| \_ \_ Tipo di elenco \_ di testo arabo, arabo<br/>             | \_bool VT | Tipo list-style | ListType       |
| \_ \_ Tipo di elenco \_ di testo LowerLetter, \_ lettera inferiore<br/> | \_bool VT | Tipo list-style | ListType       |
| \_ \_ Tipo di elenco \_ di testo UpperLetter, \_ lettera superiore<br/> | \_bool VT | Tipo list-style | ListType       |
| \_ \_ Tipo di elenco \_ di testo LowerRoman, \_ Roman inferiore<br/>   | \_bool VT | Tipo list-style | ListType       |
| \_ \_ Tipo di elenco \_ di testo UpperRoman, superiore \_ romano<br/>   | \_bool VT | Tipo list-style | ListType       |



 

## <a name="app"></a>App



| Nome attributo, nome descrittivo                         | Tipo     | Equivalente CSS | Equivalente TOM |
|-------------------------------------------------------|----------|----------------|----------------|
| App \_ IncorrectSpelling, \_ ortografia non corretta<br/> | \_bool VT |                | Non supportato  |
| \_IncorrectGrammar app, grammatica non corretta \_<br/>   | \_bool VT |                | Non supportato  |



 

 

