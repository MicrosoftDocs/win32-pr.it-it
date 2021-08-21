---
title: Ricerca di una nuova posizione in un file
description: Ricerca di una nuova posizione in un file
ms.assetid: 276c3e43-bf9f-4a0a-b33a-7eaa701e92a6
keywords:
- I/O di file multimediali, spostamento all'inizio dei file
- I/O di file, spostamento all'inizio dei file
- input e output (I/O), spostamento all'inizio dei file
- I/O (input e output), spostamento all'inizio dei file
- spostamento all'inizio dei file di I/O
- I/O di file multimediali, ricerca di una nuova posizione nei file
- I/O di file, ricerca di una nuova posizione nei file
- input e output (I/O), ricerca di una nuova posizione nei file
- I/O (input e output), ricerca di una nuova posizione nei file
- ricerca di una nuova posizione nei file di I/O
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e51ab51065bcdf89af84f2fd622558261dd4cf42cac3e50fe54fb116a7ad9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136585"
---
# <a name="seeking-to-a-new-position-in-a-file"></a>Ricerca di una nuova posizione in un file

Nell'esempio seguente si passa all'inizio di un file aperto usando la funzione [**mmioSeek.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)


```C++
mmioSeek(hFile, 0L, SEEK_SET); 
```



L'esempio seguente si sposta alla fine di un file aperto.


```C++
mmioSeek(hFile, 0L, SEEK_END); 
```



Nell'esempio seguente si passa a una posizione di 10 byte dalla fine di un file aperto.


```C++
mmioSeek(hFile, -10L, SEEK_END); 

```



 

 