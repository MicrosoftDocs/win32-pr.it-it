---
title: Ricerca di un sottoblocco
description: Ricerca di un sottoblocco
ms.assetid: c494a57f-6395-40a4-a4f2-d200d7ad6223
keywords:
- I/O file multimediale, ricerca di blocchi di RIFF
- I/O di file, ricerca di un blocco di RIFF
- input e output (I/O), ricerca di blocchi di RIFF
- I/O (input e output), ricerca di blocchi RIFF
- ricerca del blocco RIFF
- formato file di interscambio risorse (RIFF)
- RIFF (formato file di interscambio risorse)
- I/O RIFF
- Blocco RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6cfb0ecc3223f4a883998e9f192bfbbb5ff276
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337446"
---
# <a name="searching-for-a-subchunk"></a><span data-ttu-id="7e7fc-112">Ricerca di un sottoblocco</span><span class="sxs-lookup"><span data-stu-id="7e7fc-112">Searching for a Subchunk</span></span>

<span data-ttu-id="7e7fc-113">Nell'esempio seguente viene usata la funzione [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) per cercare il blocco "fmt" nel blocco "riff" dell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="7e7fc-113">The following example uses the [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) function to search for the "FMT" chunk in the "RIFF" chunk of the previous example.</span></span>


```C++
// Find the format chunk (form type "FMT"); it should be 
// a subchunk of the "RIFF" parent chunk. 
mmckinfoSubchunk.ckid = mmioFOURCC('f', 'm', 't', ' '); 
if (mmioDescend(hmmio, &mmckinfoSubchunk, &mmckinfoParent, 
    MMIO_FINDCHUNK)) 
    // Error, cannot find the "FMT" chunk. 
else 
    // "FMT" chunk found. 
```



<span data-ttu-id="7e7fc-114">Per cercare un sottoblocco, ovvero qualsiasi blocco diverso da un blocco "RIFF" o "LIST", identificare il blocco padre nel parametro *lpckParent* della funzione [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) .</span><span class="sxs-lookup"><span data-stu-id="7e7fc-114">To search for a subchunk (that is, any chunk other than a "RIFF" or "LIST" chunk), identify its parent chunk in the *lpckParent* parameter of the [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) function.</span></span>

<span data-ttu-id="7e7fc-115">Se non si specifica un blocco padre, la posizione corrente del file deve trovarsi all'inizio di un blocco prima di chiamare la funzione **mmioDescend** .</span><span class="sxs-lookup"><span data-stu-id="7e7fc-115">If you do not specify a parent chunk, the current file position should be at the beginning of a chunk before you call the **mmioDescend** function.</span></span> <span data-ttu-id="7e7fc-116">Se si specifica un blocco padre, la posizione corrente del file può trovarsi in qualsiasi punto del blocco.</span><span class="sxs-lookup"><span data-stu-id="7e7fc-116">If you do specify a parent chunk, the current file position can be anywhere in that chunk.</span></span>

<span data-ttu-id="7e7fc-117">Se la ricerca di un sottoblocco ha esito negativo, la posizione corrente del file non è definita.</span><span class="sxs-lookup"><span data-stu-id="7e7fc-117">If the search for a subchunk fails, the current file position is undefined.</span></span> <span data-ttu-id="7e7fc-118">È possibile usare la funzione [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) e il membro **DwDataOffset** della struttura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) che descrive il blocco padre da riportare all'inizio del blocco padre, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="7e7fc-118">You can use the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function and the **dwDataOffset** member of the [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) structure describing the parent chunk to seek back to the beginning of the parent chunk, as in the following example:</span></span>


```C++
mmioSeek(hmmio, mmckinfoParent.dwDataOffset + 4, SEEK_SET); 
```



<span data-ttu-id="7e7fc-119">Poiché **dwDataOffset** specifica l'offset all'inizio della parte di dati del blocco, è necessario cercare 4 byte oltre **dwDataOffset** per impostare la posizione del file dopo il tipo di form.</span><span class="sxs-lookup"><span data-stu-id="7e7fc-119">Because **dwDataOffset** specifies the offset to the beginning of the data portion of the chunk, you must seek 4 bytes past **dwDataOffset** to set the file position after the form type.</span></span>

 

 