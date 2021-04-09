---
title: Modifica della visualizzazione
description: Modifica della visualizzazione
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Playlist Windows Media Metafile, modifica delle visualizzazioni
- playlist, modifica di visualizzazioni
- playlist di metafile, modifica delle visualizzazioni
- Playlist Windows Media Metafile, visualizzazione modifiche
- playlist, visualizzazione delle modifiche
- playlist di metafile, visualizzazione della modifica
- Media Player di Windows, modifica della visualizzazione
- Media Player di Windows, modifica delle visualizzazioni
- Windows Media Player, proprietà testo
- Windows Media Player, proprietà immagine
- Windows Media Player, proprietà MOREINFO
- Media Player di Windows, testo astratto
- Proprietà di MOREINFO
- Testo astratto
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5c36c55b455b797446cde627449ea705b3bd2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044500"
---
# <a name="modifying-the-display"></a>Modifica della visualizzazione

Le playlist possono modificare l'interfaccia utente di Windows Media Player in quattro modi principali:

-   Proprietà testo
-   Proprietà dell'immagine
-   Proprietà di MOREINFO
-   Testo astratto

## <a name="text-properties"></a>Proprietà testo

Windows Media Player consente la visualizzazione del testo dei metadati title, Author, copyright e Description. I metadati della clip possono provenire dal flusso o dal file multimediale oppure possono provenire da una playlist. Mostra i metadati provengono dalla playlist. In generale, le playlist rappresentano un metodo migliore per passare le proprietà di testo a Windows Media Player, soprattutto se è probabile che gli elementi di testo cambino. È più semplice modificare il testo in una playlist anziché ricreare un file multimediale. Poiché le proprietà lette da una playlist eseguono l'override di quelle contenute nel file multimediale, è possibile aggiornare facilmente il testo visualizzato aggiungendo il nuovo testo alla proprietà corrispondente in una playlist. Nell'esempio seguente, il testo dei metadati title e Author nella playlist sostituisce il titolo e il testo dell'autore contenuti nel file multimediale, Sample. WMA.

Il testo della **Descrizione** viene recuperato da un file Windows Media a cui si fa riferimento in un elemento **entry** a meno che non esista un elemento **astratto** in una playlist di metafile. Se è presente un testo **astratto** , verrà visualizzato, sovrascrivendo il testo della **Descrizione** .


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

Le immagini banner possono essere aggiunte all'interfaccia utente di Windows Media Player. Il grafico può essere usato per la pubblicità, fornire informazioni e fornire l'accesso ai siti Web, per citare alcune possibilità.

Usare l'elemento **banner** per specificare un'immagine grafica (32 pixel di altezza di 194 pixel di larghezza) per la visualizzazione da parte di Windows Media Player. Il grafico viene visualizzato sotto qualsiasi contenuto video. È possibile aggiungere un collegamento ipertestuale al banner usando l'elemento figlio **moreinfo** .

Una descrizione comando può essere definita da un elemento **astratto** all'interno dell'ambito dell'elemento **banner** . Qualsiasi testo della descrizione comando definito può essere visualizzato posizionando il puntatore del mouse sull'icona del banner. Se si seleziona l'icona del banner con il puntatore del mouse, viene attivato qualsiasi collegamento ipertestuale definito con l'elemento **moreinfo** .

Il formato grafico preferito del **banner** è il formato gif. Il formato JPG può essere usato se il grafico è dimensionato correttamente.

Nell'esempio precedente viene illustrato l'utilizzo dell'elemento **banner** .

> [!Note]  
> Le immagini **banner** non sono supportate con i file DRM o quando Windows Media Player è incorporato in una pagina Web.

 

Per ulteriori informazioni sui banner, vedere la pagina relativa [alla grafica personalizzata in Windows Media Player](custom-graphics-in-windows-media-player.md).

## <a name="moreinfo-properties"></a>Proprietà di MOREINFO

Le aree di testo e immagine dell'interfaccia utente possono essere associate agli URL. Durante la riproduzione, gli utenti possono selezionare una di queste sezioni per connettersi all'URL associato nella Web browser. Ad esempio, è possibile associare il sito Web di un inserzionista a un'immagine del banner pubblicitario, come illustrato nel frammento di codice seguente.


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a>Testo astratto

Il testo **astratto** viene usato per visualizzare una breve descrizione popup delle aree di testo o immagine dell'interfaccia utente a cui è associata. Durante la riproduzione, se il puntatore del mouse viene posizionato su una di queste aree, viene visualizzata una descrizione comando accanto al puntatore del mouse che Visualizza il testo **astratto** associato all'area. Il testo **astratto** viene recuperato da un metafile e viene definito con l'elemento **abstract** . L'elemento **astratto** può essere un elemento figlio di una **voce** o di un elemento **banner** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Uso delle playlist di metafile**](using-metafile-playlists.md)
</dt> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guida ai metafile di Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




