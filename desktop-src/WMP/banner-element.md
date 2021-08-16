---
title: Elemento BANNER
description: L'elemento BANNER definisce un URL di un file grafico che verrà visualizzato nel pannello di visualizzazione.
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- Elemento BANNER Windows Media Player
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91b3de50c1360337c1344a1af1a0696361614dbc293390470e7c196e53528a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135964"
---
# <a name="banner-element"></a>Elemento BANNER

**L'elemento BANNER** definisce un URL di un file grafico che verrà visualizzato nel pannello di visualizzazione.

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a>Attributi

**HREF** (obbligatorio)

URL di un file grafico visualizzato nel pannello di visualizzazione.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                   |
|-----------------|----------------------------|
| Elementi padre | **ASX**, **ENTRY**         |
| Elementi figlio  | **ABSTRACT**, **MOREINFO** |



 

## <a name="remarks"></a>Commenti

Questo elemento definisce l'URL di un file grafico visualizzato nel pannello Windows Media Player, sotto il contenuto video. Se il contenuto multimediale è solo audio, l'immagine del banner viene visualizzata da sola. Windows Media Player riserva uno spazio di 32 pixel di altezza per 194 pixel (la barra del banner) per l'immagine. Se l'elemento grafico definito nell'URL è inferiore, viene visualizzato con le dimensioni originali. Se l'immagine è più grande dello spazio riservato, Windows Media Player ritaglia l'immagine per adattarla allo spazio.

È possibile usare un elemento **ABSTRACT** nell'ambito dell'elemento **BANNER** per visualizzare il testo come descrizione comando quando l'utente posiziona il puntatore del mouse sull'immagine del banner. Un **elemento MOREINFO** all'interno **di un elemento BANNER** definisce un URL a cui l'utente viene preso quando l'utente fa clic sull'immagine del banner. L'URL può essere qualsiasi percorso o protocollo, ad esempio un collegamento di posta elettronica, un URL Hypertext Transfer Protocol (HTTP) a un sito Web o anche un comando JScript Microsoft. Quando il puntatore viene spostato sull'elemento grafico, l'immagine viene in rilievo e ha l'aspetto di un pulsante.

Un **elemento BANNER** definito per un elemento **ASX** viene visualizzato durante la riproduzione di tutte le clip nella playlist. Un **elemento BANNER** definito in un elemento **ENTRY** viene visualizzato solo durante la riproduzione del clip e durante tale periodo esegue l'override di qualsiasi banner definito all'interno dell'elemento **ASX** padre. È possibile specificare come Windows Media Player spazio per il banner impostando **l'attributo BANNERBAR** dell'elemento **ASX.**

Le immagini banner non sono supportate con i file DRM o quando Windows Media Player è incorporato in una pagina Web.

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio di **elemento BANNER** senza elementi figlio:


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



Di seguito è riportato un esempio di elemento **BANNER** contenente **gli elementi ABSTRACT** e **MOREINFO.**


```XML
<BANNER HREF="https://www.proseware.com/logos/banner1.bmp">
    <ABSTRACT>Click here to go to our website.</ABSTRACT>
    <MOREINFO HREF="https://sample.microsoft.com" />
    <!-- The text in the Abstract element displays as a 
         ToolTip when the mouse hovers over the banner 
         graphic. When a user clicks the banner, the URL 
         given in the MoreInfo element opens in the 
         browser. -->
</BANNER>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Informazioni di riferimento sui metafile multimediali**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





