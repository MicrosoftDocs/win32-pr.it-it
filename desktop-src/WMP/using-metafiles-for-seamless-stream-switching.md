---
title: Uso dei metafile per un cambio di flusso trasparente
description: Uso dei metafile per un cambio di flusso trasparente
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
keywords:
- Playlist Windows Media Metafile, cambio di flusso di eventi Live
- playlist, cambio di flusso di eventi Live
- playlist di metafile, cambio di flusso di eventi Live
- Playlist Windows Media Metafile, cambio di flusso di eventi
- playlist, cambio di flusso di eventi
- playlist di metafile, cambio di flusso di eventi
- Playlist Windows Media Metafile, inserimento ad
- playlist, inserimento di annunci
- playlist di metafile, inserimento di annunci
- Windows Media Player, cambio di flusso di eventi Live
- Windows Media Player, cambio del flusso di eventi
- Windows Media Player, inserimento di annunci
- cambio di flusso di eventi Live
- cambio di flusso di eventi
- inserimento ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29496c71c0c849480bae029f246bfd544667071e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297909"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a>Uso dei metafile per un cambio di flusso trasparente

È possibile semplificare il cambio di flusso senza interruzioni usando le playlist del metafile. In genere, quando viene terminata una parte di contenuto, il buffering viene eseguito per il clip o il flusso successivo prima che venga aperto, se è contenuto ricevuto da un server dei flussi multimediali. Servizi multimediali di Microsoft Windows consente di eliminare o almeno ridurre al minimo il tempo di memorizzazione nel buffer e l'esecuzione di un'altra parte di contenuto trasmesso quasi immediatamente. La modalità di funzionamento normale per Windows Media Player consiste nell'aprire il successivo flusso multimediale a cui fa riferimento la playlist 20 secondi prima della fine del flusso attualmente sottoposto a rendering. In genere fornisce una transizione senza problemi tra flussi multimediali, a seconda di altri fattori, ad esempio i tempi di accesso Web.

Usare l'elemento **Event** in una playlist insieme ai comandi OPENEVENT del codificatore per facilitare il cambio tra i flussi o i file. L'invio di un comando OPENEVENT di 20 secondi o più prima del comando dell'evento può ridurre al minimo i ritardi nel cambio del flusso. Quindi Windows Media Player è in grado di precaricare una parte del contenuto di streaming imminente in un buffer.

Usare Windows Media Encoder per inviare un comando script nel flusso usando il formato seguente:


```XML
OPENEVENT eventname 

```



Il nome dell'evento deve essere quello definito nell'elemento **Event** nella playlist. Quando Windows Media Player riceve un comando di script OPENEVENT dal codificatore, Cerca l'elemento **Event** nella playlist e avvia il buffering della clip o del flusso definito nell'elemento **Event** . Windows Media Player quindi queste informazioni fino all'evento effettivo con lo stesso nome. Quando viene ricevuto l'evento denominato, Windows Media Player passa a tale contenuto precedentemente memorizzato nel buffer.

> [!Note]  
> Non è possibile usare caratteri Unicode per il comando script OPENEVENT nel file multimediale o nell'elemento **Event** nella playlist.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist di metafile**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Evento Player. ScriptCommand**](player-player-scriptcommand.md)
</dt> <dt>

[**Uso delle playlist di metafile**](using-metafile-playlists.md)
</dt> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guida ai metafile di Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




