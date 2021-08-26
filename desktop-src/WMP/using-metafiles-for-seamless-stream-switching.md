---
title: Uso di metafile per il cambio di flusso facile
description: Uso di metafile per il cambio di flusso facile
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
keywords:
- Windows Playlist di metafile multimediali, cambio di flusso di eventi live
- playlist, cambio di flusso di eventi live
- playlist di metafile, cambio di flusso di eventi live
- Windows Playlist di metafile multimediali, passaggio del flusso di eventi
- playlist, passaggio del flusso di eventi
- playlist di metafile, passaggio del flusso di eventi
- Windows playlist metafile multimediali,inserimento di annunci
- playlist, inserimento di annunci
- playlist di metafile, inserimento di annunci
- Windows Media Player,live event stream switching
- Windows Media Player,cambio del flusso di eventi
- Windows Media Player,inserimento di annunci
- cambio di flusso di eventi live
- commutazione del flusso di eventi
- inserimento di annunci
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d4efc4a23f0464446675d9de20d57750bd230d2eef26d31714e2129e380ae9e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001571"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a>Uso di metafile per il cambio di flusso facile

È possibile semplificare il cambio di flusso facile usando playlist di metafile. In genere, quando una parte di contenuto termina, viene eseguita la memorizzazione nel buffer per il clip o il flusso successivo prima dell'apertura (se si tratta di contenuto ricevuto da un server di streaming multimediale). Microsoft Servizi Windows Media consente di eliminare, o almeno ridurre al minimo, questo tempo di memorizzazione nel buffer e fare in modo che un altro frammento di contenuto trasmesso inizi quasi immediatamente. La modalità di funzionamento normale per Windows Media Player è aprire il flusso multimediale successivo a cui fa riferimento la playlist 20 secondi prima della fine del flusso attualmente sottoposto a rendering. Ciò offre in genere una transizione facile tra i flussi multimediali, a seconda di altri fattori, ad esempio i tempi di accesso Web.

Usare **l'elemento EVENT** in una playlist insieme ai comandi OPENEVENT del codificatore per facilitare il passaggio facile tra flussi o file. L'invio di un comando OPENEVENT 20 secondi o più prima del comando EVENT può ridurre al minimo i ritardi nella commutazione del flusso. È Windows Media Player possibile precaricare una parte del contenuto di streaming futuro in un buffer.

Usare Windows Media Encoder per inviare un comando script nel flusso usando il formato seguente:


```XML
OPENEVENT eventname 

```



Il nome dell'evento deve essere quello definito **nell'elemento EVENT** nella playlist. Quando Windows Media Player riceve un comando di script OPENEVENT dal codificatore, cerca l'elemento **EVENT** nella playlist e inizia a memorizzato nel buffer il clip o il flusso definito nell'elemento **EVENT.** Windows Media Player quindi contiene queste informazioni fino all'evento effettivo con lo stesso nome. Quando viene ricevuto l'evento denominato, Windows Media Player passa al contenuto memorizzato nel buffer in precedenza.

> [!Note]  
> Non è possibile usare caratteri Unicode per il comando di script OPENEVENT nel file multimediale o **nell'elemento EVENT** nella playlist.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist metafile**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlist metafile**](metafile-playlists.md)
</dt> <dt>

[**Evento Player.ScriptCommand**](player-player-scriptcommand.md)
</dt> <dt>

[**Uso di playlist metafile**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Informazioni di riferimento su elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guida ai metafile multimediali**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




