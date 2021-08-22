---
title: Modifica delle dimensioni del buffer di I/O
description: Modifica delle dimensioni del buffer di I/O
ms.assetid: eff97399-143e-477b-bb16-7305e83a2317
keywords:
- I/O di file multimediali, modifica delle dimensioni del buffer
- I/O di file, modifica delle dimensioni del buffer
- input e output (I/O), modifica delle dimensioni del buffer
- I/O (input e output), modifica delle dimensioni del buffer
- modifica delle dimensioni del buffer di I/O
- I/O senza buffer
- I/O memorizzato nel buffer
- Funzione mmioSetBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 826fabfb7e51b80bf406721b3d5e7b094f83c1c3fe2061f7edea0810a41dc639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145084"
---
# <a name="changing-the-io-buffer-size"></a>Modifica delle dimensioni del buffer di I/O

L'esempio seguente apre un file denominato SAMPLE.TXT per I/O senza buffer e quindi abilita l'I/O memorizzato nel buffer con un buffer interno di 16.000 usando la funzione [**mmioSetBuffer.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("SAMPLE.TXT", NULL, MMIO_READ)) != NULL) 
{ 
    // File opened successfully; request an I/O buffer. 
    if (mmioSetBuffer(hFile, NULL, 16384L, 0)) 
        // Buffer cannot be allocated. 
    else 
        // Buffer allocated successfully. 
} 
else 
    // File cannot be opened. 
```



 

 