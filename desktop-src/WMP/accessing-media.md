---
title: Accesso ai supporti
description: Accesso ai supporti
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Windows playlist di metafile multimediali, accesso ai file multimediali
- playlist, accesso ai supporti
- playlist di metafile, accesso ai supporti
- Windows playlist di metafile multimediali, accesso ai file multimediali
- playlist, accesso ai file multimediali
- playlist di metafile, accesso ai file multimediali
- Windows playlist di metafile multimediali, controllo della riproduzione
- playlist, controllo della riproduzione
- playlist di metafile, controllo della riproduzione
- Windows playlist di metafile multimediali,impostazione della durata
- playlist, impostazione della durata
- playlist di metafile, impostazione della durata
- Windows Media Player,accesso ai supporti
- Windows Media Player, accesso ai supporti
- Windows Media Player, controllo della riproduzione
- Windows Media Player,impostazione della durata
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
ms.openlocfilehash: c1a0846be4e8b9b62e424ce24d1b1800bc361c6a28f52a323c6bfa8511ae040b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956401"
---
# <a name="accessing-media"></a>Accesso ai supporti

Usare le playlist per specificare e per controllare i file multimediali di streaming o i file multimediali Windows Media Player riprodotti.

Usare **l'elemento ENTRY** per specificare un singolo elemento multimediale (un file multimediale o un flusso live) ed eventuali elementi figlio (ad esempio immagini, **collegamenti MOREINFO** e **testo ABSTRACT).** Usare un **elemento ENTRYREF** per specificare una playlist. Una playlist può contenere uno o più **elementi ENTRY** **o ENTRYREF.** Windows Media Player esegue una playlist iniziando con la prima voce e quindi riproducendo ogni voce a sua volta fino al termine dell'elenco.

Un **elemento ENTRY** può puntare a qualsiasi tipo di file multimediale Windows Media Player riproduzione. Sono inclusi non solo file con estensione wma, wmv, asf e .avi, per citane alcuni, ma anche flussi live. Usando una serie di elementi **ENTRY** o **ENTRYREF** per fare riferimento al contenuto multimediale, è possibile usare una playlist per inviare un singolo flusso costituito da più origini. I flussi a cui si fa riferimento verranno riprodotti in sequenza e verranno visti come un unico flusso continuo dal visualizzatore. Ad esempio, la playlist può contenere due elementi **ENTRY:** un'introduzione standard da un file multimediale di Windows con estensione wma e un flusso multimediale Windows live.

> [!Note]  
> Una playlist non deve contenere collegamenti a file multimediali con contenuto creato con versioni diverse di Digital Rights Management (DRM). In una playlist di metafile, se sono presenti collegamenti per i file multimediali con contenuto DRM versione 1 e per i file multimediali creati con versioni DRM successive, Windows Media Player riprodurrà solo il contenuto DRM versione 1.

 

## <a name="controlling-playback"></a>Controllo della riproduzione

Usare le playlist per controllare non solo quali clip multimediali vengono riprodotti, ma anche quali parti del clip vengono riprodotte e come. È possibile usare le playlist per definire un set di clip da riprodurre a ciclo continuo o ripetuto, per impostare la durata della riproduzione e per assegnare le ore di inizio e i marcatori di inizio e fine per ogni voce. Gli **elementi STARTTIME,** **STARTMARKER** **ed ENDMARKER** funzionano insieme ai marcatori nel file multimediale.

Ad esempio, la playlist seguente usa un banner pubblicitario e il collegamento **MOREINFO** associato in una **voce** e fa riferimento a **startMARKER** **ed ENDMARKER.**


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

Usare **l'elemento DURATION** per specificare per quanto tempo riprodurre un clip o un set di clip. È anche possibile usare **l'attributo PREVIEWMODE** dell'elemento **ASX** insieme all'elemento **PREVIEWDURATION** per specificare per quanto tempo riprodurre un clip o un set di clip. Impostare **l'attributo PREVIEWMODE** su YES per usare **l'elemento PREVIEWDURATION** per specificare per quanto tempo riprodurre il clip associato. Gli **elementi PREVIEWDURATION** **e DURATION** hanno lo stesso comportamento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Uso di playlist di metafile**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guida ai metafile multimediali**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




