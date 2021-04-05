---
title: Modifica delle dimensioni del buffer di I/O
description: Modifica delle dimensioni del buffer di I/O
ms.assetid: eff97399-143e-477b-bb16-7305e83a2317
keywords:
- I/O dei file multimediali, modifica delle dimensioni del buffer
- I/O di file, modifica delle dimensioni del buffer
- input e output (I/O), modifica delle dimensioni del buffer
- I/O (input e output), modifica delle dimensioni del buffer
- modifica delle dimensioni del buffer di I/O
- I/O senza buffer
- I/O memorizzato nel buffer
- mmioSetBuffer (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2171f4f09b933a3de5ec1e99750261fdda2f80
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046751"
---
# <a name="changing-the-io-buffer-size"></a><span data-ttu-id="4f899-111">Modifica delle dimensioni del buffer di I/O</span><span class="sxs-lookup"><span data-stu-id="4f899-111">Changing the I/O Buffer Size</span></span>

<span data-ttu-id="4f899-112">Nell'esempio seguente viene aperto un file denominato SAMPLE.TXT per l'I/O non memorizzato nel buffer e quindi viene abilitato l'I/O memorizzato nel buffer con un buffer 16K interno mediante la funzione [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) .</span><span class="sxs-lookup"><span data-stu-id="4f899-112">The following example opens a file named SAMPLE.TXT for unbuffered I/O, and then enables buffered I/O with an internal 16K buffer using the [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) function.</span></span>


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



 

 