---
title: Uso dell'URL e del rollover del server
description: Uso dell'URL e del rollover del server
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Playlist Windows Media Metafile, rollover URL
- playlist, rollover degli URL
- playlist di metafile, rollover degli URL
- Playlist Windows Media Metafile, rollover server
- playlist, rollover del server
- playlist di metafile, rollover del server
- Playlist Windows Media Metafile, rollover di protocollo
- playlist, rollover dei protocolli
- playlist di metafile, rollover di protocollo
- Media Player di Windows, rollover degli URL
- Windows Media Player, rollover del server
- Windows Media Player, rollover dei protocolli
- Rollover degli URL
- rollover del server
- rollover del protocollo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eae38e81f8ae23199628e543f65f2766491f1a2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330255"
---
# <a name="using-url-and-server-rollover"></a>Uso dell'URL e del rollover del server

È possibile usare le playlist di metafile per fornire un mezzo per il rollover automatico a origini di contenuto alternative quando non è possibile accedere o riprodurre un flusso. È possibile utilizzare questo metodo di rollover per specificare le origini dello stesso contenuto in server diversi o in tipi diversi di server. È possibile, ad esempio, specificare una prima alternativa in un server Windows Media diverso. Se il contenuto non viene riprodotto, il client può eseguire il rollback a una seconda alternativa in un server Web. Windows Media Player tenta automaticamente di eseguire il rollback a protocolli diversi in base alle impostazioni delle proprietà di Windows Media prima di provare gli URL di rollover nella playlist.

Impostare il rollover del server e del protocollo inserendo più elementi **ref** in successione all'interno di un elemento **entry** . Ogni elemento **ref** specifica un percorso o un protocollo alternativo per un file multimediale o un flusso.

Codice di esempio


```XML
<!--Server and protocol rollover is set for the file Rollover.wma.-->
<ASX version="3.0">
    <TITLE>MyServer Rollover</TITLE>
   <ENTRY>
      <REF HREF="mms://Server1.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server2.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server3.proseware.com/Path/Rollover.wma"/>
      <REF HREF="https://www.proseware.com/Path/Rollover.wma"/>
   </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist di metafile**](creating-metafile-playlists.md)
</dt> <dt>

[**Uso delle playlist di metafile**](using-metafile-playlists.md)
</dt> </dl>

 

 




