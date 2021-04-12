---
title: Aggiunta di un blocco di informazioni
description: Aggiunta di un blocco di informazioni
ms.assetid: ebba5079-1f67-4236-9260-e36ff72ad51c
keywords:
- capFileSetInfoChunk (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacb99fb29e4b1882b4f257c428315f42ee3a360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221574"
---
# <a name="adding-an-information-chunk"></a>Aggiunta di un blocco di informazioni

Se è necessario includere altre informazioni nell'applicazione oltre a audio e video, è possibile creare blocchi di informazioni e inserirli in un file di acquisizione. I blocchi di informazioni possono contenere diversi tipi di informazioni, tra cui i dettagli di un avviso di copyright, l'identificazione dell'origine video o informazioni sulla temporizzazione esterna. Nell'esempio seguente vengono archiviate le informazioni sulla temporizzazione esterna di un timecode SMPTE (Society of Motion Picture and Television Engineers) in un blocco di informazioni e il blocco viene aggiunto a un file di acquisizione utilizzando la macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .


```C++
//  This example assumes the application controls 
//  the video source for preroll and postroll. 
CAPINFOCHUNK cic;
// . 
// . 
// . 
cic.fccInfoID = infotypeSMPTE_TIME;
cic.lpData = "00:20:30:12"; 
cic.cbData = strlen (cic.lpData) + 1;
capFileSetInfoChunk (hwndC, &cic); 
 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




