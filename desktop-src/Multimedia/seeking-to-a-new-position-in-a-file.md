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
# <a name="seeking-to-a-new-position-in-a-file"></a><span data-ttu-id="7bc1c-113">Ricerca in una nuova posizione in un file</span><span class="sxs-lookup"><span data-stu-id="7bc1c-113">Seeking to a New Position in a File</span></span>

<span data-ttu-id="7bc1c-114">Nell'esempio seguente viene spostato all'inizio di un file aperto utilizzando la funzione [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) .</span><span class="sxs-lookup"><span data-stu-id="7bc1c-114">The following example moves to the beginning of an open file using the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function.</span></span>


```C++
mmioSeek(hFile, 0L, SEEK_SET); 
```



<span data-ttu-id="7bc1c-115">Nell'esempio seguente viene spostato alla fine di un file aperto.</span><span class="sxs-lookup"><span data-stu-id="7bc1c-115">The following example moves to the end of an open file.</span></span>


```C++
mmioSeek(hFile, 0L, SEEK_END); 
```



<span data-ttu-id="7bc1c-116">Nell'esempio seguente viene spostata in una posizione di 10 byte dalla fine di un file aperto.</span><span class="sxs-lookup"><span data-stu-id="7bc1c-116">The following example moves to a position 10 bytes from the end of an open file.</span></span>


```C++
mmioSeek(hFile, -10L, SEEK_END); 

```



 

 