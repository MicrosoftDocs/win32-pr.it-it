---
title: Assegnazione di un nome al file di acquisizione
description: Assegnazione di un nome al file di acquisizione
ms.assetid: fae2fd6a-4c2f-432f-a714-9faae6daeafe
keywords:
- capFileSetCaptureFile (macro)
- capFileAlloc (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ea091a36777e176124689ba57be6c0fb75d07d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330687"
---
# <a name="naming-the-capture-file"></a>Assegnazione di un nome al file di acquisizione

Nell'esempio seguente viene utilizzata la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) per specificare un nome file alternativo (MYCAP.AVI) per il file di acquisizione e la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) per preallocare un file di 5 MB.


```C++
char szCaptureFile[] = "MYCAP.AVI";

capFileSetCaptureFile( hWndC, szCaptureFile); 
capFileAlloc( hWndC, (1024L * 1024L * 5)); 
 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




