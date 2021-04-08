---
title: Creazione ed eliminazione di un file
description: Creazione ed eliminazione di un file
ms.assetid: a4b4a310-7230-4f1d-b084-c47db39adaac
keywords:
- I/O file multimediale, creazione di file
- I/O di file, creazione di file
- input e output (I/O), creazione di file
- I/O (input e output), creazione di file
- creazione di file di I/O
- I/O file multimediale, eliminazione di file
- I/O di file, eliminazione di file
- input e output (I/O), eliminazione di file
- I/O (input e output), eliminazione di file
- eliminazione dei file di I/O
- mmioOpen (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22cd6330874d0b5da74d69193359c025c709c79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725370"
---
# <a name="creating-and-deleting-a-file"></a>Creazione ed eliminazione di un file

Per creare un file, impostare il parametro *dwOpenFlags* della funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) su MMIO \_ create. Nell'esempio seguente viene creato un file che viene aperto per la lettura e la scrittura.


```C++
HMMIO hFile; 

hFile = mmioOpen("NEWFILE.TXT", NULL, MMIO_CREATE | MMIO_READWRITE); 
if (hFile != NULL) 
    // File created successfully. 
else 
    // File cannot be created. 
```



Se il file che si sta creando esiste già, verrà troncato con una lunghezza pari a zero.

Per eliminare un file, impostare il parametro *dwOpenFlags* della funzione **mmioOpen** su MMIO \_ Delete. Dopo aver eliminato un file, non è possibile recuperarlo con alcun mezzo standard. Se l'applicazione sta eliminando un file alla richiesta di un utente, eseguire una query sull'utente prima di eliminare il file per assicurarsi che l'utente voglia eliminarlo.

 

 