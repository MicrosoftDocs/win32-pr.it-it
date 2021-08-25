---
title: Apertura di un file con mmioOpen
description: Apertura di un file con mmioOpen
ms.assetid: 947d1b1c-ec00-4bd9-948a-4b8e3bfb84f6
keywords:
- I/O file multimediali,apertura di file
- I/O di file, apertura di file
- input e output (I/O),apertura di file
- I/O (input e output),apertura di file
- I/O file multimediale, funzione mmioOpen
- file I/O, funzione mmioOpen
- input e output (I/O),funzione mmioOpen
- I/O (input e output),funzione mmioOpen
- Funzione mmioOpen
- apertura di file di I/O
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbd323e888b181b0166572d11687d3dde66e83f0ce73541555b1f49083564ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893191"
---
# <a name="opening-a-file-with-mmioopen"></a>Apertura di un file con mmioOpen

Per aprire un file per le operazioni di I/O di base, impostare il parametro *lpmmioinfo* della funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) su **NULL.** Nell'esempio seguente viene aperto un file denominato "C: SAMPLESSAMPLE1.TXT" per la lettura e viene verificata la presenza di errori \\ \\ nel valore restituito.


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("C:\\SAMPLES\\SAMPLE1.TXT", NULL, 
    MMIO_READ)) != NULL) 
    // File opened successfully. 
else 
    // File cannot be opened. 
```



Usare il *parametro dwFlags* di **mmioOpen** per specificare i flag per l'apertura di un file.

 

 