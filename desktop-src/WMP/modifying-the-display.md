---
title: Modifica della visualizzazione
description: Modifica della visualizzazione
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Windows playlist di metafile multimediali, modifica degli schermi
- playlist, modifica di schermi
- playlist di metafile, modifica di schermi
- Windows playlist metafile multimediali,modifica dello schermo
- playlist, modifica della visualizzazione
- playlist di metafile, modifica della visualizzazione
- Windows Media Player,visualizzare la modifica
- Windows Media Player,modifica di schermi
- Windows Media Player,proprietà di testo
- Windows Media Player,proprietà image
- proprietà Windows Media Player,MOREINFO
- Windows Media Player,TESTO ABSTRACT
- Proprietà MOREINFO
- Testo ABSTRACT
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e18ca15f71d9d25d9c99db36683a61b52057580022805c9d5f0f0d250aa738a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054609"
---
# <a name="modifying-the-display"></a>Modifica della visualizzazione

Le playlist possono modificare l'Windows Media Player'interfaccia utente in quattro modi principali:

-   Proprietà del testo
-   Proprietà dell'immagine
-   Proprietà MOREINFO
-   Testo ABSTRACT

## <a name="text-properties"></a>Proprietà del testo

Windows Media Player la visualizzazione del testo dei metadati Titolo, Autore, Copyright e Descrizione. I metadati di clip possono derivare dal flusso o dal file multimediale oppure da una playlist. Mostra metadati proviene dalla playlist. In generale, le playlist sono un metodo migliore per passare le proprietà del testo Windows Media Player, soprattutto se è probabile che gli elementi di testo cambino. È più facile modificare il testo in una playlist piuttosto che ri-creare un file multimediale. Poiché le proprietà lette da una playlist eseguono l'override di quelle contenute nel file multimediale, è possibile aggiornare facilmente il testo visualizzato aggiungendo il nuovo testo alla proprietà corrispondente in una playlist. Nell'esempio seguente il testo dei metadati Title e Author nella playlist esegue l'override del testo Title e Author contenuto nel file multimediale sample.wma.

**Il** testo DESCRIPTION viene recuperato da un Windows file multimediale a cui viene fatto riferimento in un **elemento ENTRY,** a meno che non sia presente un elemento **ABSTRACT** in una playlist metafile. Se è presente **testo ABSTRACT,** verrà visualizzato, eseguendo l'override del **testo DESCRIPTION.**


```XML
<ASX version="3.0" BANNERBAR="AUTO" >
    <ENTRY>
        <BANNER HREF="YourPath\2.gif">
        </BANNER>
        <TITLE>Upgrade</TITLE>
        <AUTHOR>Ad Department</AUTHOR>
        <REF href="YourPath\sample.wma"/>
    </ENTRY>
</ASX>

```



## <a name="image-properties"></a>Proprietà dell'immagine

È possibile aggiungere immagini banner all'interfaccia utente di Windows Media Player. L'immagine può essere usata per la pubblicità, la fornitura di informazioni e l'accesso ai siti Web, per assegnare un nome ad alcune possibilità.

Usare **l'elemento BANNER** per specificare un'immagine grafica (32 pixel di altezza per 194 pixel di larghezza) da visualizzare Windows Media Player. L'immagine viene visualizzata sotto qualsiasi contenuto video. È possibile aggiungere un collegamento ipertestuale al banner usando **l'elemento figlio MOREINFO.**

Una descrizione comando può essere definita da un **elemento ABSTRACT** all'interno dell'ambito **dell'elemento BANNER.** È possibile visualizzare qualsiasi testo della descrizione comando definito sosonendo il puntatore del mouse sull'immagine del banner. Se si seleziona l'immagine del banner con il puntatore del mouse, verrà attivato qualsiasi collegamento ipertestuale definito con **l'elemento MOREINFO.**

Il formato **grafico BANNER** preferito è il formato GIF. Il formato JPG può essere usato se il grafico è ridimensionato correttamente.

L'esempio precedente illustra l'uso **dell'elemento BANNER.**

> [!Note]  
> **Le** immagini BANNER non sono supportate con i file DRM o quando Windows Media Player è incorporato in una pagina Web.

 

Per altre informazioni sui banner, vedere [Grafica personalizzata in Windows Media Player](custom-graphics-in-windows-media-player.md).

## <a name="moreinfo-properties"></a>Proprietà MOREINFO

Le aree di testo e immagine dell'interfaccia utente possono essere associate agli URL. Durante la riproduzione, gli utenti possono selezionare una di queste sezioni per connettersi all'URL associato nel Web browser. Ad esempio, è possibile associare il sito Web di un pubblicitario a un'immagine del banner pubblicitario, come illustrato nel frammento di codice seguente.


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a>Testo ABSTRACT

**Il** testo ABSTRACT viene usato per visualizzare una breve descrizione popup delle aree di testo o immagine dell'interfaccia utente a cui è associato. Durante la riproduzione, se il puntatore del mouse passa su una di queste aree, accanto al puntatore del mouse viene visualizzata una descrizione comando con il testo **ABSTRACT** associato all'area. **Il** testo ABSTRACT viene recuperato da un metafile ed è definito con **l'elemento ABSTRACT.** **L'elemento ABSTRACT** può essere un elemento figlio di un **elemento ENTRY** o **BANNER.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Playlist metafile**](metafile-playlists.md)
</dt> <dt>

[**Uso di playlist metafile**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Informazioni di riferimento su elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guida al metafile multimediale**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




