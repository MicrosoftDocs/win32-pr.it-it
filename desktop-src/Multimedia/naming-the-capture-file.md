---
title: Denominazione del file di acquisizione
description: Denominazione del file di acquisizione
ms.assetid: fae2fd6a-4c2f-432f-a714-9faae6daeafe
keywords:
- Macro capFileSetCaptureFile
- Macro capFileAlloc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c07653b854b4af476c22566aac5e9ecf27cb78b3dac5b317aab4b8f3f23a19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373316"
---
# <a name="naming-the-capture-file"></a>Denominazione del file di acquisizione

L'esempio seguente usa la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) per specificare un nome file alternativo (MYCAP.AVI) per il file di acquisizione e la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) per preallocare un file di 5 MB.


```C++
char szCaptureFile[] = "MYCAP.AVI";

capFileSetCaptureFile( hWndC, szCaptureFile); 
capFileAlloc( hWndC, (1024L * 1024L * 5)); 
 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




