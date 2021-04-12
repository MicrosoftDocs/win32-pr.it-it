---
title: Uso delle playlist nei pacchetti di download di Windows Media (deprecato)
description: Uso delle playlist nei pacchetti di download di Windows Media (deprecato)
ms.assetid: c40efe24-aaed-47fc-8a8a-f412dfc36af7
keywords:
- Metafile di Windows Media, pacchetti di download di Windows Media
- Windows Media Player, pacchetti di download di Windows Media
- Metafile, pacchetti di download di Windows Media
- Windows Media, pacchetti di download di Windows Media
- playlist, pacchetti di download di Windows Media
- playlist di metafile, pacchetti di download di Windows Media
- Playlist Windows Media Metafile, pacchetti di download di Windows Media
- Pacchetti di download di Windows Media, playlist
- Pacchetti di download di Windows Media, playlist di metafile
- Pacchetti di download di Windows Media, playlist metafile di Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00c4daa26d18294c00aad7b4926a017d2f3f6343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396499"
---
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a>Uso delle playlist nei pacchetti di download di Windows Media (deprecato)

Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.

Le playlist sono metafile Windows Media con estensione asx che forniscono informazioni che indicano a Windows Media Player come riprodurre il contenuto in pacchetto. Combinando più file di contenuto in un singolo pacchetto di download di Windows Media, è possibile controllare e personalizzare il pacchetto di download di Windows Media usando la playlist.

> [!Note]  
> In generale, le playlist di metafile vengono usate dai pacchetti di download di Windows Media per fare riferimento al contenuto multimediale nel pacchetto piuttosto che a un flusso da un server in una rete Intranet o Internet. Tuttavia, i riferimenti URL all'interno del file con estensione asx sono supportati.

 

Utilizzando XML, il metafile fornisce le informazioni utilizzate da Windows Media Player per riprodurre e visualizzare il contenuto. Le playlist sono costituite da vari elementi di codice XML con i tag e gli attributi associati. Ogni elemento in una playlist Windows Media Metafile definisce una particolare impostazione o azione in Windows Media Player.

Il computer dell'utente associa un metafile di Windows Media con estensione di file ASX con Windows Media Player. Windows Media Player apre e analizza il codice XML nel metafile, che contiene il percorso per individuare i file audio o video in pacchetto. Lo script di metafile controlla quindi l'esperienza audio, video e grafica. Il metafile contiene anche informazioni elaborate e visualizzate da Windows Media Player nella casella di riepilogo a discesa della playlist. Immediatamente dopo la visualizzazione dell'elenco, viene riprodotto il primo elemento dell'elenco.

Una playlist di metafile è un collegamento ai file che contengono il contenuto incluso nel pacchetto. Il codice seguente è un esempio di un metafile che specifica il bordo da visualizzare usando l'elemento **Skin** , due canzoni da riprodurre e le informazioni della playlist per ogni brano.


```XML
<ASX Version="3.0">
<AUTHOR>Name of content creator goes here</AUTHOR>
<TITLE>Album Title goes here</TITLE>
<PARAM name="Album" value="Album Title "/>
<PARAM name="Artist" value="Artist Name"/>
<PARAM name="Genre" value="Genre"/>
<SKIN HREF="myborder.wmz"/>
    <ENTRY>
        <REF HREF="song1.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #1 title</TITLE>
    </ENTRY>
    <ENTRY>
        <REF HREF="song2.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #2 name</TITLE>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Bordi per Windows Media Player (deprecato)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Pacchetti di download di Windows Media (deprecato)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Metafile di Windows Media**](windows-media-metafiles.md)
</dt> </dl>

 

 




