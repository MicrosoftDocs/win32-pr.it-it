---
title: Appendice E Text Attributes for Active Accessibility Text Services Dictionary
description: Questa appendice fornisce informazioni sugli attributi di testo definiti in IAccDictionary.
ms.assetid: 9e405140-c151-4f00-91c5-777c84c41806
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539583f05e5140d96594490b0038b1a629f7760b13e4de223f6a8a3304c3901b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134064"
---
# <a name="appendix-e-text-attributes-for-active-accessibility-text-services-dictionary"></a>Appendice E: Attributi di testo per Active Accessibility dizionario dei servizi di testo

Questa appendice fornisce informazioni sugli attributi di testo definiti in [**IAccDictionary.**](/windows/desktop/api/msaatext/nn-msaatext-iaccdictionary) È organizzato come una serie di tabelle. Ogni tabella include informazioni su una categoria specifica di attributi. Queste categorie sono effettivamente annidate, ma sono separate di seguito per poter visualizzare gli attributi.

> [!Note]  
> Active Accessibility servizi di testo è deprecato. Vedere [Microsoft Windows Framework servizi di testo](../tsf/text-services-framework.md) per altre informazioni sulle tecnologie avanzate di input di testo e linguaggio naturale.

 

Ogni voce in una tabella fornisce un nome di attributo e un nome descrittivo, un tipo, un equivalente di Cascading Style Sheets (CSS), un equivalente tom (Text Object Model) ed eventuali commenti aggiuntivi, se appropriato. La colonna equivalente TOM fornisce informazioni sul metodo TOM usato con l'attributo (parte delle [**interfacce ITextFont,**](/windows/desktop/api/tom/nn-tom-itextfont) [**ITextRange**](/windows/desktop/api/tom/nn-tom-itextrange)o [**ITextPara).**](/windows/desktop/api/tom/nn-tom-itextpara) Le informazioni precedenti a ogni tabella indicano quale interfaccia supporta gli attributi. Le informazioni nella tabella equivalente tom indicano il nome del metodo. Ogni voce nella colonna equivalente di TOM è associata a due metodi. Ad esempio, la voce Name è associata ai **metodi GetName** **e SetName.**

Per altre informazioni su queste interfacce, vedere la documentazione [del](../controls/text-object-model.md) modello a oggetti di testo in Windows Software Development Kit (SDK).

## <a name="font"></a>Carattere

Gli attributi nella tabella seguente sono associati agli attributi generali del tipo di carattere. L'equivalente TOM è [**l'interfaccia ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nome attributo, Nome descrittivo       | Tipo     | Equivalente CSS       | EQUIVALENTE TOM | Commento           |
|-------------------------------------|----------|----------------------|----------------|-------------------|
| Font \_ FaceName, facename<br/> | VT \_ BSTR | Famiglia di caratteri: Verdana | Nome           |                   |
| Dimensioni \_ caratterePts, sizePts<br/>   | VT \_ I4   | Dimensioni carattere: Xpt       | Dimensione           | Le dimensioni sono in punti |



 

## <a name="font_style"></a>Stile \_ carattere

Gli attributi nella tabella seguente indirizzano gli attributi di stile del tipo di carattere(ad esempio, se il testo è impostato in grassetto o corsivo). L'equivalente TOM è [**l'interfaccia ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nome attributo, Nome descrittivo                             | Tipo     | Equivalente CSS              | EQUIVALENTE TOM                                            | Commento                   |
|-----------------------------------------------------------|----------|-----------------------------|-----------------------------------------------------------|---------------------------|
| Stile \_ carattere \_ Grassetto, grassetto<br/>                        | VT \_ BOOL | Spessore carattere: grassetto           | Bold                                                      |                           |
| Stile \_ carattere \_ corsivo, corsivo<br/>                    | VT \_ BOOL | Stile carattere: corsivo          | Corsivo                                                    |                           |
| Stile \_ carattere \_ SmallCaps, smallcaps<br/>              | VT \_ BOOL | Font-variant: maiuscoletto    | SmallCaps                                                 |                           |
| Stile \_ carattere \_ maiuscole,maiuscole/minuscole<br/>             | VT \_ BOOL | Trasformazione del testo: maiuscole/minuscole  | Non supportato                                             |                           |
| Stile \_ carattere \_ maiuscolo, maiuscolo<br/>               | VT \_ BOOL | Trasformazione del testo: lettere maiuscole   | AllCaps                                                   |                           |
| Stile \_ carattere \_ minuscolo, minuscolo<br/>               | VT \_ BOOL | Trasformazione del testo: lettere minuscole   | Non supportato                                             |                           |
| Rilievo stile \_ \_ carattere, rilievo<br/>                     | VT \_ BOOL | Non supportato               | Rilievo                                                    |                           |
| Stile \_ carattere \_ Engrave, engrave<br/>                   | VT \_ BOOL | Non supportato               | Incidere                                                   |                           |
| Stile \_ carattere \_ nascosto                                       | VT \_ BOOL | Non supportato               | Nascosto                                                    |                           |
| \_crenatura dello stile del \_ carattere, crenatura<br/>                   | VT \_ R4   | Non supportato               | Crenatura                                                   | Stessi valori di GetKerning |
| Stile \_ carattere \_ con contorno, con contorno<br/>                 | VT \_ BOOL | Non supportato               | Delineato                                                  |                           |
| Posizione \_ stile \_ carattere,posizione<br/>                 | VT \_ R4   | Non supportato               | Posizione                                                  |                           |
| Stile \_ carattere \_ protetto                                    | VT \_ BOOL | Non supportato               | Protetta                                                 |                           |
| Ombreggiatura \_ stile \_ carattere,ombreggiatura<br/>                     | VT \_ BOOL | Altezza riga (meno numeri) | Ombreggiatura                                                    |                           |
| Spaziatura \_ stile \_ carattere,spaziatura<br/>                   | VT \_ R4   | Spaziatura tra lettere              | Spaziatura                                                   | In punti                 |
| Spessore \_ dello stile del \_ carattere, spessore<br/>                     | VT \_ I4   | Spessore del carattere                 | Valori WeightSame come font-weight e GetWeight<br/> |                           |
| Altezza \_ stile \_ carattere,altezza<br/>                     | VT \_ R4   | Line-height                 | Non supportato                                             | In punti                 |
| Stile \_ carattere \_ Lampeggiare, lampeggiare<br/>                       | VT \_ BOOL | Decorazione del testo: lampeggiare      | Non supportato                                             |                           |
| Pedice \_ \_ stile carattere, pedice<br/>               | VT \_ BOOL | Allineamento verticale: sub         | Pedice (anche Posizione)                                 |                           |
| Apice \_ \_ stile carattere, apice<br/>           | VT \_ BOOL | Allineamento verticale: super       | Apice (anche Posizione)                               |                           |
| Colore \_ stile \_ carattere,colore<br/>                       | VT \_ I4   | Color                       | ColorePrimoPiano                                                 | Stile COLORREF RBG        |
| Stile \_ carattere \_ SfondoColore, colore di \_ sfondo<br/> | VT \_ I4   | Colore di sfondo            | ColoreSfondo                                                 | Stile COLORREF RBG        |



 

## <a name="font_style_animation"></a>Animazione \_ stile \_ carattere

Gli attributi nella tabella seguente indirizzano l'animazione del tipo di carattere. L'equivalente TOM è [**l'interfaccia ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nome attributo, Nome descrittivo                                              | Tipo     | Css equivalente | EQUIVALENTE TOM |
|----------------------------------------------------------------------------|----------|----------------|----------------|
| Stile \_ carattere \_ Animation \_ LasVegasLights,LasVegas \_ lights<br/>         | VT \_ BOOL | Non supportato  | Animazione      |
| Animazione \_ stile \_ carattere \_ LampeggianteBackground, sfondo \_ lampeggiante<br/> | VT \_ BOOL | Non supportato  | Animazione      |
| Stile \_ carattere \_ \_ Animazione SparkleText, testo \_ sparkle<br/>               | VT \_ BOOL | Non supportato  | Animazione      |
| Animazione \_ \_ stile carattere \_ MarchingBlackAnts, \_ formiche \_ nere in marzo<br/> | VT \_ BOOL | Non supportato  | Animazione      |
| Stile \_ carattere \_ Animation \_ MarchingRedAnts,marching \_ red \_ ants<br/>     | VT \_ BOOL | Non supportato  | Animazione      |
| Stile \_ carattere \_ \_ Animazione Shimmer, Shimmer<br/>                         | VT \_ BOOL | Non supportato  | Animazione      |
| Cancellazione \_ \_ dell'animazione \_ dello stile del carattere,wipeDown<br/>                       | VT \_ BOOL | Non supportato  | Animazione      |
| Stile \_ carattere \_ Animation \_ WipeRight,wipeRight<br/>                     | VT \_ BOOL | Non supportato  | Animazione      |



 

## <a name="font_style_underline"></a>Sottolineatura \_ stile \_ carattere

Gli attributi nella tabella seguente indirizzano gli stili di sottolineatura per i tipi di carattere. L'equivalente TOM è [**l'interfaccia ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nome attributo, Nome descrittivo                     | Tipo     | Css equivalente                | EQUIVALENTE TOM |
|---------------------------------------------------|----------|-------------------------------|----------------|
| Sottolineatura \_ \_ stile carattere \_ singola, singola<br/>  | VT \_ BOOL | Decorazione del testo: sottolineatura    | Sottolineato      |
| Sottolineatura \_ \_ stile carattere \_ Double,double<br/> | VT \_ BOOL | Decorazione del testo: line-through | Barrato  |



 

## <a name="font_style_strikethrough"></a>Barrato \_ stile \_ carattere

Gli attributi nella tabella seguente indirizzano gli stili barrati per i tipi di carattere.



| Nome attributo, Nome descrittivo                                         | Tipo     | Css equivalente | EQUIVALENTE TOM |
|-----------------------------------------------------------------------|----------|----------------|----------------|
| Barrato \_ stile \_ carattere \_ singolo, \_ barrato \_ singolo<br/> | VT \_ BOOL | Non supportato  | Non supportato  |
| Stile \_ carattere \_ Barrato \_ doppio, \_ barrato \_ doppio<br/> | VT \_ BOOL | Non supportato  | Non supportato  |



 

## <a name="font_style_overline"></a>Stile \_ carattere \_ overline

Gli attributi nella tabella seguente indirizzano gli stili overline per i tipi di carattere.



| Nome attributo, Nome descrittivo                             | Tipo     | Equivalente CSS            | EQUIVALENTE TOM |
|-----------------------------------------------------------|----------|---------------------------|----------------|
| Stile \_ carattere \_ overline \_ single,overline \_ single<br/> | VT \_ BOOL | Decorazione di testo: overline | Non supportato  |
| Font \_ Style \_ Overline \_ Double,overline \_ double<br/> | VT \_ BOOL | Decorazione di testo: overline | Non supportato  |



 

## <a name="text"></a>Testo

Gli attributi nella tabella seguente indirizzano gli attributi generali di formattazione del testo.



| Nome attributo, Nome descrittivo                     | Tipo        | Equivalente CSS | EQUIVALENTE TOM                                       | Commento                                                                               |
|---------------------------------------------------|-------------|----------------|------------------------------------------------------|---------------------------------------------------------------------------------------|
| Scrittura \_ verticale del testo, scrittura verticale<br/> | VT \_ BOOL    | Non supportato  | non supportato                                        | Usato da cinese/giapponese                                                           |
| Testo \_ RightToLeft,righttoleft<br/>          | VT \_ BOOL    | Direzione      | Non supportato                                        |                                                                                       |
| Text \_ ReadOnly, sola lettura<br/>               | VT \_ BOOL    | Non supportato  | ITextFont::CanChange, ITextRange::CanEdit            | La proprietà modificabile del documento ha la precedenza                                     |
| Lingua \_ del testo, lingua<br/>                | VT \_ I4      | Non supportato  | ITextFont::GetLanguageID, ITextFont::SetLanguageID   | LANGID                                                                                |
| Orientamento \_ del testo, orientamento<br/>          | VT \_ I4      | Non supportato  | Non supportato                                        | 10??? di un grado                                                                     |
| Text \_ EmbeddedObject, oggetto \_ incorporato<br/>  | VT \_ BOOL    | Non supportato  | Non supportato                                        | Consente la ricerca di oggetti incorporati                                                 |
| Collegamento \_ di testo, collegamento<br/>                        | VT \_ UNKNOWN | Collegamento           | Non supportato                                        | Puntatore a interfaccia all'oggetto . Chiamare QueryInterface per qualsiasi interfaccia di interesse |
| \_Sillabazione del testo, sillabazione<br/>          | VT \_ BOOL    | Non supportato  | ITextPara::GetHyphenation, ITextPara::SetHyphenation |                                                                                       |



 

## <a name="text_alignment"></a>Allineamento \_ del testo

Gli attributi nella tabella seguente indirizzano l'allineamento del testo. L'equivalente TOM è [**l'interfaccia ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nome attributo, Nome descrittivo               | Tipo     | Equivalente CSS | EQUIVALENTE TOM |
|---------------------------------------------|----------|----------------|----------------|
| Allineamento \_ testo \_ a sinistra, a sinistra<br/>       | VT \_ BOOL | Allineamento del testo     | Allineamento      |
| Allineamento \_ del testo a \_ destra,destra<br/>     | VT \_ BOOL | Allineamento del testo     | Allineamento      |
| Allineamento \_ del testo al \_ centro, al centro<br/>   | VT \_ BOOL | Allineamento del testo     | Allineamento      |
| Allineamento \_ del testo \_ Justify,justify<br/> | VT \_ BOOL | Allineamento del testo     | Allineamento      |



 

## <a name="text_para"></a>Parametro di \_ testo

Gli attributi nella tabella seguente indirizzano la formattazione per i paragrafi. L'equivalente TOM è [**l'interfaccia ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nome attributo, Nome descrittivo                              | Tipo   | Equivalente CSS | EQUIVALENTE TOM  | Commento |
|------------------------------------------------------------|--------|----------------|-----------------|---------|
| Text \_ Para \_ FirstLineIndent,first \_ line \_ indent<br/> | VT \_ R4 | Non supportato  | FirstLineIndent | In pts  |
| Text \_ Para \_ LeftIndent,left \_ indent<br/>             | VT \_ R4 | Non supportato  | LeftIndent      | In pts  |
| Rientro \_ \_ a destra del testo, \_ rientro a destra<br/>           | VT \_ R4 | Non supportato  | RightIndent     | In pts  |
| Text \_ Para \_ SpaceAfter,space \_ after<br/>             | VT \_ R4 | Non supportato  | SpaceAfter      | In pts  |
| Text \_ Para \_ SpaceBefore,space \_ after<br/>            | VT \_ R4 | Non supportato  | SpaceAfter      | In pts  |



 

## <a name="text_para_linespacing"></a>Text \_ Para \_ lineSpacing

Gli attributi nella tabella seguente indirizzano l'interlinea in paragrafi. L'equivalente TOM è [**l'interfaccia ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nome attributo, Nome descrittivo                               | Tipo     | Css equivalente | EQUIVALENTE TOM | Commento  |
|-------------------------------------------------------------|----------|----------------|----------------|----------|
| Text \_ Para \_ lineSpacing \_ Single,single<br/>           | VT \_ BOOL | Non supportato  | LineSpacing    |          |
| Text \_ Para \_ lineSpacing \_ OnePtFive,one \_ pt \_ five<br/> | VT \_ BOOL | Non supportato  | LineSpacing    |          |
| Text \_ Para \_ lineSpacing \_ Double,double<br/>           | VT \_ BOOL | Non supportato  | LineSpacing    |          |
| Text \_ Para \_ lineSpacing \_ AtLeast, \_ almeno<br/>       | VT \_ R4   | Non supportato  | LineSpacing    | In righe |
| Text \_ Para \_ lineSpacing \_ Exactly,exactly<br/>         | VT \_ R4   | Non supportato  | LineSpacing    | In righe |
| Text \_ Para \_ lineSpacing \_ Mutiple,multiple<br/>        | VT \_ R4   | Non supportato  | LineSpacing    | In righe |



 

## <a name="text_list"></a>Elenco \_ di testo

Gli attributi nella tabella seguente elencano gli indirizzi e i livelli degli elenchi di testo. L'equivalente TOM è [**l'interfaccia ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nome attributo, Nome descrittivo | Tipo   | Css equivalente | EQUIVALENTE TOM | Commento                                                       |
|-------------------------------|--------|----------------|----------------|---------------------------------------------------------------|
| Text \_ List \_ LevelIndex,       | VT \_ I4 | Non supportato  | ListLevelIndex | Dove 1 è l'elenco più esterno, 2 è il livello successivo e così via |



 

## <a name="text_list_type"></a>Tipo \_ di elenco di \_ testo

Gli attributi nella tabella seguente elencano gli stili per il testo. L'equivalente TOM è [**l'interfaccia ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nome attributo, Nome descrittivo                          | Tipo     | Css equivalente  | EQUIVALENTE TOM |
|--------------------------------------------------------|----------|-----------------|----------------|
| Elenco \_ di testo Tipo punto \_ \_ elenco, punto elenco<br/>             | VT \_ BOOL | Tipo di elenco       | ListType       |
| Tipo \_ di elenco di testo \_ \_ arabo,arabo<br/>             | VT \_ BOOL | List-style-type | ListType       |
| Tipo \_ di elenco di testo \_ \_ LowerLetter, lettera \_ inferiore<br/> | VT \_ BOOL | List-style-type | ListType       |
| Tipo \_ di elenco di testo \_ \_ UpperLetter,upper \_ letter<br/> | VT \_ BOOL | List-style-type | ListType       |
| Tipo \_ di elenco di testo \_ \_ LowerRoman,lower \_ roman<br/>   | VT \_ BOOL | List-style-type | ListType       |
| Tipo \_ di elenco di testo \_ \_ UpperRoman,upper \_ roman<br/>   | VT \_ BOOL | List-style-type | ListType       |



 

## <a name="app"></a>App



| Nome attributo, Nome descrittivo                         | Tipo     | Css equivalente | EQUIVALENTE TOM |
|-------------------------------------------------------|----------|----------------|----------------|
| App \_ non corretta Ortografia, ortografia \_ non corretta<br/> | VT \_ BOOL |                | Non supportato  |
| App \_ incorrectGrammar, grammatica non \_ corretta<br/>   | VT \_ BOOL |                | Non supportato  |



 

 

