---
title: Ricerca in una nuova posizione in un file
description: Ricerca in una nuova posizione in un file
ms.assetid: 276c3e43-bf9f-4a0a-b33a-7eaa701e92a6
keywords:
- I/O dei file multimediali, passaggio all'inizio dei file
- I/O di file, passaggio all'inizio dei file
- input e output (I/O), passaggio all'inizio dei file
- I/O (input e output), passaggio all'inizio dei file
- passaggio all'inizio dei file di I/O
- I/O dei file multimediali, ricerca di nuove posizioni nei file
- I/O di file, ricerca di nuove posizioni nei file
- input e output (I/O), ricerca di nuove posizioni nei file
- I/O (input e output), ricerca di nuove posizioni nei file
- ricerca di nuove posizioni nei file di I/O
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 949ca3e9d118fdd83e5b53ae9336ad8ab601c64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336855"
---
# <a name="seeking-to-a-new-position-in-a-file"></a>Ricerca in una nuova posizione in un file

Nell'esempio seguente viene spostato all'inizio di un file aperto utilizzando la funzione [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) .


```C++
mmioSeek(hFile, 0L, SEEK_SET); 
```



Nell'esempio seguente viene spostato alla fine di un file aperto.


```C++
mmioSeek(hFile, 0L, SEEK_END); 
```



Nell'esempio seguente viene spostata in una posizione di 10 byte dalla fine di un file aperto.


```C++
mmioSeek(hFile, -10L, SEEK_END); 

```



 

 