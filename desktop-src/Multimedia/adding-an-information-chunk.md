---
title: Aggiunta di un blocco di informazioni
description: Aggiunta di un blocco di informazioni
ms.assetid: ebba5079-1f67-4236-9260-e36ff72ad51c
keywords:
- Macro capFileSetInfoChunk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 420181fd0da326ebf3ccc6f921e55161c2005d17c3f8713cd104481147b40f1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145134"
---
# <a name="adding-an-information-chunk"></a>Aggiunta di un blocco di informazioni

Se è necessario includere altre informazioni nell'applicazione oltre all'audio e al video, è possibile creare blocchi di informazioni e inserirli in un file di acquisizione. I blocchi di informazioni possono contenere diversi tipi di informazioni, inclusi i dettagli di un'informativa sul copyright, l'identificazione dell'origine video o informazioni temporali esterne. L'esempio seguente archivia le informazioni di temporizzazione esterne di un codice temporale SMPTE (Society of Motion Picture and Engineers) in un blocco di informazioni e aggiunge il blocco a un file di acquisizione usando la macro [**capFileSetInfoChunk.**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk)


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

[Uso dell'acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




