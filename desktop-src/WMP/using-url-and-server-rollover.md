---
title: Uso di URL e rollover del server
description: Uso di URL e rollover del server
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Windows playlist di metafile multimediali, rollover degli URL
- playlist, rollover degli URL
- playlist di metafile, rollover degli URL
- Windows Playlist di metafile multimediali, rollover del server
- playlist, rollover del server
- playlist di metafile, rollover del server
- Windows playlist di metafile multimediali, rollover del protocollo
- playlist, rollover del protocollo
- playlist di metafile, rollover del protocollo
- Windows Media Player,rollover url
- Windows Media Player, rollover del server
- Windows Media Player, rollover del protocollo
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
ms.openlocfilehash: 3988ff019fba838e86ea1d0e7b0f6124c367bb8b505a0f2d2e2f639b94d93e52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465676"
---
# <a name="using-url-and-server-rollover"></a>Uso di URL e rollover del server

È possibile usare playlist metafile per fornire un modo per eseguire automaticamente il roll over a origini di contenuto alternative quando non è possibile accedere o riprodurre un flusso. È possibile usare questo metodo di rollover per specificare origini dello stesso contenuto in server diversi o in tipi diversi di server. È possibile, ad esempio, specificare una prima alternativa in un server Windows Media. Se il contenuto non viene riprodotto, il client può eseguire il roll over in una seconda alternativa in un server Web. Windows Media Player tenta automaticamente di eseguire il rollover in protocolli diversi in base alle impostazioni delle proprietà Windows Media prima di provare gli URL di rollover nella playlist.

Impostare il rollover del server e del protocollo inserendo più **elementi REF** in successione all'interno di un **elemento ENTRY.** Ogni **elemento REF** specifica un percorso o un protocollo alternativo per un file multimediale o un flusso.

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

[**Creazione di playlist metafile**](creating-metafile-playlists.md)
</dt> <dt>

[**Uso di playlist metafile**](using-metafile-playlists.md)
</dt> </dl>

 

 




