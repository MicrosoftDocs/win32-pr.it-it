---
title: Uso di una playlist metafile
description: Uso di una playlist metafile
ms.assetid: e6cbdb76-4405-409e-93c3-38a3baa7c231
keywords:
- Playlist Windows Media Metafile, uso
- playlist di metafile, uso
- playlist, uso
- Playlist Windows Media Metafile, informazioni
- playlist di metafile, informazioni
- playlist, informazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5f1832c0c739874fbbd4db219f2c622fc2debfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709850"
---
# <a name="using-a-metafile-playlist"></a>Uso di una playlist metafile

Dal momento che non è possibile collegarsi direttamente da una pagina Web a un server di flussi multimediali, si usano le playlist del metafile. Le playlist di metafile contengono le informazioni necessarie per Windows Media Player e vengono archiviate in un server Web. È quindi possibile eseguire il collegamento dal documento Web a una playlist del metafile. Quando viene aperta una playlist di metafile, il controllo viene trasferito a Windows Media Player, che elabora il file, si connette al server multimediale di streaming e riproduce il contenuto specificato.

Il browser scarica prima di tutto la playlist metafile nella directory della cache dell'utente. Poiché la playlist del metafile è piccola, si tratta di un passaggio molto rapido. Il computer dell'utente trova quindi nella tabella delle associazioni di file l'associazione della playlist del metafile con Windows Media Player. Windows Media Player apre e interpreta lo scripting nella playlist del metafile, che contiene, tra le altre cose, l'URL del contenuto di streaming. Windows Media Player usa l'URL per individuare il contenuto e avviare il flusso. Lo script di playlist di metafile controlla quindi l'esperienza di streaming.

Poiché le playlist di metafile funzionano tramite un'applicazione helper associata al tipo ASXMIME (Application/Mplayer2 o video/x-ms-asf), sono compatibili con qualsiasi browser che supporta le applicazioni helper. Gli esempi illustrati in questo documento funzioneranno con Microsoft Internet Explorer 4,0 e versioni successive e con Netscape Navigator 4,0 e versioni successive in Microsoft Win32® e le piattaforme Apple Macintosh. In tutti gli esempi, sarà necessario assicurarsi che i file multimediali digitali a cui si fa riferimento abbiano percorsi e nomi file validi per l'ambiente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida ai metafile di Windows Media**](windows-media-metafile-guide.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> <dt>

[**Cenni preliminari sui file di Windows Media**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




