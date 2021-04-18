---
title: Elemento BANNER
description: L'elemento BANNER definisce un URL di un file grafico che verrà visualizzato nel pannello di visualizzazione.
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- Finestra di elemento BANNER Media Player
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e257c14e5908482cdf8de458c259bc64a55c6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331020"
---
# <a name="banner-element"></a>Elemento BANNER

L'elemento **banner** definisce un URL di un file grafico che verrà visualizzato nel pannello di visualizzazione.

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a>Attributi

**Href** (obbligatorio)

URL di un file grafico visualizzato nel pannello di visualizzazione.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                   |
|-----------------|----------------------------|
| Elementi padre | **ASX**, **voce**         |
| Elementi figlio  | **abstract**, **moreinfo** |



 

## <a name="remarks"></a>Commenti

Questo elemento definisce un URL di un file grafico visualizzato nel pannello di visualizzazione di Windows Media Player, sotto il contenuto video. Se il supporto è solo audio, l'icona del banner viene visualizzata da sola. Windows Media Player riserva uno spazio 32 pixel di altezza di 194 pixel di larghezza (barra del banner) per l'immagine. Se il grafico definito nell'URL è più piccolo, viene visualizzato con le dimensioni originali. Se il grafico è più grande dello spazio riservato, Windows Media Player ridurrà l'immagine per adattarla allo spazio.

È possibile usare un elemento **astratto** nell'ambito dell'elemento **banner** per visualizzare il testo come descrizione comando quando l'utente posiziona il puntatore del mouse sull'icona del banner. Un elemento **moreinfo** all'interno di un elemento **banner** definisce un URL a cui l'utente viene utilizzato quando l'utente fa clic sull'icona del banner. L'URL può essere qualsiasi percorso o protocollo, ad esempio un collegamento di posta elettronica, un URL Hypertext Transfer Protocol (HTTP) a un sito Web o anche un comando Microsoft JScript. Quando il puntatore viene spostato sul grafico, il grafico viene visualizzato in rilievo e ha un aspetto simile a un pulsante.

Viene visualizzato un elemento **banner** definito per un elemento **ASX** mentre tutti i clip della playlist sono in riproduzione. Un elemento **banner** definito in un elemento **entry** viene visualizzato solo quando il clip sta eseguendo la riproduzione e durante tale periodo esegue l'override di qualsiasi banner definito all'interno dell'elemento **ASX** padre. È possibile specificare in che modo Windows Media Player riserva spazio per il banner impostando l'attributo **BANNERBAR** dell'elemento **ASX** .

Le immagini banner non sono supportate con i file DRM o quando Windows Media Player è incorporato in una pagina Web.

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio di elemento **banner** senza elementi figlio:


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



Di seguito è riportato un esempio di un elemento **banner** contenente elementi **abstract** e **moreinfo** .


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





