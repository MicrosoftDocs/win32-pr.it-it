---
title: Creazione ed eliminazione di un file
description: Creazione ed eliminazione di un file
ms.assetid: a4b4a310-7230-4f1d-b084-c47db39adaac
keywords:
- I/O di file multimediali, creazione di file
- I/O di file, creazione di file
- input e output (I/O),creazione di file
- I/O (input e output),creazione di file
- creazione di file di I/O
- I/O di file multimediali, eliminazione di file
- I/O di file, eliminazione di file
- input e output (I/O),eliminazione di file
- I/O (input e output),eliminazione di file
- eliminazione di file di I/O
- Funzione mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91a2ee8e70508e2c5dc3b24c084cf0b081b6629a519703ef43a15845ef3ec76a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785731"
---
# <a name="creating-and-deleting-a-file"></a>Creazione ed eliminazione di un file

Per creare un file, impostare *il parametro dwOpenFlags* della funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) su MMIO \_ CREATE. L'esempio seguente crea un file e lo apre per la lettura e la scrittura.


```C++
HMMIO hFile; 

hFile = mmioOpen("NEWFILE.TXT", NULL, MMIO_CREATE | MMIO_READWRITE); 
if (hFile != NULL) 
    // File created successfully. 
else 
    // File cannot be created. 
```



Se il file che si sta creando esiste già, verrà troncato a lunghezza zero.

Per eliminare un file, impostare *il parametro dwOpenFlags* della funzione **mmioOpen** su MMIO \_ DELETE. Dopo l'eliminazione, un file non può essere ripristinato in alcun modo standard. Se l'applicazione sta eliminando un file su richiesta di un utente, eseguire una query prima di eliminare il file per assicurarsi che l'utente voglia eliminarlo.

 

 