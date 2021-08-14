---
title: Apertura di un file AVI
description: Apertura di un file AVI
ms.assetid: 322eb45f-7dd3-40f4-b6bf-381021c50397
keywords:
- Funzione AVIFileInit
- Funzione AVIFileOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7e8415e6cb3f54dc4eb6bffa11d7f70879546ff2a434fc75cbb91d283bb65c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373260"
---
# <a name="opening-an-avi-file"></a>Apertura di un file AVI

L'esempio seguente inizializza la libreria AVIFile usando la [**funzione AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) e apre un file AVI usando la [**funzione AVIFileOpen.**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) La funzione usa un gestore di file predefinito.


```C++
// LoadAVIFile - loads AVIFile and opens an AVI file. 
// 
// szfile - filename 
// hwnd - window handle 
// 
VOID LoadAVIFile(LPCSTR szFile, HWND hwnd) 
{ 
    LONG hr; 
    PAVIFILE pfile; 
 
    AVIFileInit();          // opens AVIFile library 
 
    hr = AVIFileOpen(&pfile, szFile, OF_SHARE_DENY_WRITE, 0L); 
    if (hr != 0){ 
        // Handle failure.
        return; 
    } 
 
// 
// Place functions here that interact with the open file. 
// 
 
    AVIFileRelease(pfile);  // closes the file 
    AVIFileExit();          // releases AVIFile library 
} 
 
```



 

 




