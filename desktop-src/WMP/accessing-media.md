---
title: Accesso ai supporti
description: Accesso ai supporti
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Playlist Windows Media Metafile, accesso ai file multimediali
- playlist, accesso ai file multimediali
- playlist di metafile, accesso ai file multimediali
- Playlist Windows Media Metafile, accesso multimediale
- playlist, accesso ai supporti
- playlist di metafile, accesso multimediale
- Playlist Windows Media Metafile, controllo della riproduzione
- playlist, controllo della riproduzione
- playlist di metafile, controllo della riproduzione
- Playlist Windows Media Metafile, impostazione durata
- playlist, impostazione della durata
- playlist di metafile, impostazione della durata
- Windows Media Player, accesso ai supporti
- Windows Media Player, accesso ai file multimediali
- Windows Media Player, controllo della riproduzione
- Media Player di Windows, impostazione della durata
- accesso ai supporti
- accesso ai supporti
- controllo della riproduzione
- impostazione della durata
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5a995a6816e3c46a002bd1ea924c9ea9a207000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298577"
---
# <a name="accessing-media"></a>Accesso ai supporti

Usare le playlist per specificare e controllare i supporti di streaming o i file multimediali che Windows Media Player riproduce.

Usare l'elemento **entry** per specificare un singolo elemento multimediale, ovvero un file multimediale o un flusso Live, e tutti gli elementi figlio, ad esempio immagini, collegamenti **moreinfo** e testo **astratto** . Usare un elemento **ENTRYREF** per specificare una playlist. Una playlist può contenere uno o più elementi **entry** o **ENTRYREF** . Windows Media Player esegue una playlist iniziando dalla prima voce e quindi riproducendo ogni voce a sua volta fino al termine dell'elenco.

Un elemento **entry** può puntare a qualsiasi tipo di supporto che Windows Media Player possa riprodurre. Sono inclusi i file WMA, WMV, ASF e AVI, per citarne alcuni, ma anche i flussi live. Usando una serie di elementi **entry** o **ENTRYREF** per fare riferimento al contenuto multimediale, è possibile usare una playlist per inviare un singolo flusso costituito da più origini. I flussi a cui si fa riferimento verranno riprodotti in sequenza e saranno considerati come un flusso continuo dal visualizzatore. La playlist può ad esempio contenere due elementi **entry** : un'introduzione standard da un file Windows Media con estensione WMA e un flusso di Windows Media Live.

> [!Note]  
> Una playlist non deve contenere collegamenti a file multimediali con contenuto creato con diverse versioni di Digital Rights Management (DRM). In una playlist di metafile, se sono presenti collegamenti per i file multimediali con contenuto DRM versione 1 e per i file multimediali creati con versioni successive di DRM, Windows Media Player giocherà solo il contenuto di DRM versione 1.

 

## <a name="controlling-playback"></a>Controllo della riproduzione

Usare le playlist per controllare non solo quale clip multimediale viene riprodotto, ma anche quali parti della clip vengono riprodotte e come. È possibile usare le playlist per definire un set di clip da ciclare o ripetere, per impostare la durata della riproduzione e per assegnare le ore di inizio e i marcatori di inizio e di fine per ogni voce. Gli elementi **StartTime**, **STARTMARKER** e **ENDMARKER** funzionano insieme ai marcatori nel file multimediale.

Ad esempio, la playlist seguente usa un banner ad e il collegamento **moreinfo** associato in una **voce** e fa riferimento a **STARTMARKER** e **ENDMARKER**.


```XML
<ASX version ="3.0">
<Title>Windows Media Example</Title>
<Abstract>Windows Media Technologies</Abstract>
<MoreInfo href = "https://www.proseware.com"/>
    <!--This is the first Entry -->
    <Entry>
        <Title>This is the ad</Title>
        <Author>Ad Department</Author>
        <Copyright>2000</Copyright>
        <Abstract>This is a description of the ad.</Abstract>
        <MoreInfo href = "https://www.proseware.com/"/>
        <Ref href="ad.wma"/>
        <Banner href ="purchase.gif">
           <Abstract>Click here to go to our website.</Abstract>
           <MoreInfo href = "https://www.litwareinc.com/" />
        </Banner>
     </Entry>        
    <!-- This is the second Entry -->
    <!-- The Windows Media file plays from Segment2 to Segment3 -->
    <Entry>
        <Title>Playlist Clip Number Two</Title>
        <Author>Windows Media</Author>
        <Copyright>2000</Copyright>
        <Ref href="show.wma"/>
        <StartMarker Name = "Segment2" />
        <EndMarker Name = "Segment3" />
    </Entry>
</ASX>

```



## <a name="setting-duration"></a>Impostazione della durata

Usare l'elemento **Duration** per specificare per quanto tempo riprodurre un clip o un set di clip. È anche possibile usare l'attributo **PREVIEWMODE** dell'elemento **ASX** insieme all'elemento **PREVIEWDURATION** per specificare per quanto tempo riprodurre un clip o un set di clip. Impostare l'attributo **PREVIEWMODE** su Yes per utilizzare l'elemento **PREVIEWDURATION** per specificare per quanto tempo riprodurre il clip associato. Gli elementi **PREVIEWDURATION** e **Duration** hanno lo stesso comportamento.

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

 

 




