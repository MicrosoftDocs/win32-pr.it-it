---
description: 'Altre informazioni su: struttura JET_ENUMCOLUMNVALUE'
title: Struttura JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bc95c6b8403a64432451ea29dbb66868fad25264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316487"
---
# <a name="jet_enumcolumnvalue-structure"></a><span data-ttu-id="1f103-103">Struttura JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="1f103-103">JET_ENUMCOLUMNVALUE Structure</span></span>


<span data-ttu-id="1f103-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1f103-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumnvalue-structure"></a><span data-ttu-id="1f103-105">Struttura JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="1f103-105">JET_ENUMCOLUMNVALUE Structure</span></span>

<span data-ttu-id="1f103-106">La struttura **JET_ENUMCOLUMNVALUE** enumera i valori di colonna di un record utilizzando la funzione [JetEnumerateColumns](./jetenumeratecolumns-function.md) .</span><span class="sxs-lookup"><span data-stu-id="1f103-106">The **JET_ENUMCOLUMNVALUE** structure enumerates the column values of a record using the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function.</span></span> <span data-ttu-id="1f103-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) restituisce una matrice di strutture di **JET_ENUMCOLUMNVALUE** .</span><span class="sxs-lookup"><span data-stu-id="1f103-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMNVALUE** structures.</span></span> <span data-ttu-id="1f103-108">La matrice viene restituita nella memoria allocata utilizzando il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a tale funzione.</span><span class="sxs-lookup"><span data-stu-id="1f103-108">The array is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to that function.</span></span>

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a><span data-ttu-id="1f103-109">Membri</span><span class="sxs-lookup"><span data-stu-id="1f103-109">Members</span></span>

<span data-ttu-id="1f103-110">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="1f103-110">**itagSequence**</span></span>

<span data-ttu-id="1f103-111">Valore della colonna (in base a un indice in base 1) enumerato.</span><span class="sxs-lookup"><span data-stu-id="1f103-111">The column value (by one-based index) that was enumerated.</span></span>

<span data-ttu-id="1f103-112">**Err**</span><span class="sxs-lookup"><span data-stu-id="1f103-112">**err**</span></span>

<span data-ttu-id="1f103-113">Codice di stato della colonna risultante dall'enumerazione del valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="1f103-113">The column status code resulting from the enumeration of the column value.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f103-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1f103-114">Value</span></span></p></th>
<th><p><span data-ttu-id="1f103-115">Significato</span><span class="sxs-lookup"><span data-stu-id="1f103-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f103-116">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="1f103-116">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="1f103-117">Il valore della colonna richiesto è NULL.</span><span class="sxs-lookup"><span data-stu-id="1f103-117">The requested column value is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f103-118">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="1f103-118">JET_wrnColumnSkipped</span></span></p></td>
<td><p><span data-ttu-id="1f103-119">Il <em>itagSequence</em> specificato nell'elemento della matrice <em>rgtagSequence</em> nello struct <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> corrispondente a questo struct di <strong>JET_ENUMCOLUMNVALUE</strong> è zero.</span><span class="sxs-lookup"><span data-stu-id="1f103-119">The <em>itagSequence</em> that is specified in the element of the <em>rgtagSequence</em> array in the <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> struct corresponding to this <strong>JET_ENUMCOLUMNVALUE</strong> struct was zero.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f103-120">JET_wrnColumnTruncated</span><span class="sxs-lookup"><span data-stu-id="1f103-120">JET_wrnColumnTruncated</span></span></p></td>
<td><p><span data-ttu-id="1f103-121">Il valore della colonna richiesta è stato troncato alla dimensione specificata prima di essere restituito.</span><span class="sxs-lookup"><span data-stu-id="1f103-121">The requested column value was truncated to the specified size before being returned.</span></span></p>
<p><span data-ttu-id="1f103-122">Questo troncamento si verifica solo per il testo lungo e per le colonne binarie lunghe che contengono grandi quantità di dati.</span><span class="sxs-lookup"><span data-stu-id="1f103-122">This truncation occurs only for long text and long binary columns that contain large amounts of data.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1f103-123">**cbData**</span><span class="sxs-lookup"><span data-stu-id="1f103-123">**cbData**</span></span>

<span data-ttu-id="1f103-124">Valore di colonna enumerato per la colonna.</span><span class="sxs-lookup"><span data-stu-id="1f103-124">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="1f103-125">Il buffer di output viene restituito nella memoria allocata mediante il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="1f103-125">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="1f103-126">**pvData**</span><span class="sxs-lookup"><span data-stu-id="1f103-126">**pvData**</span></span>

<span data-ttu-id="1f103-127">Valore di colonna enumerato per la colonna.</span><span class="sxs-lookup"><span data-stu-id="1f103-127">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="1f103-128">Il buffer di output viene restituito nella memoria allocata mediante il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="1f103-128">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="1f103-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f103-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f103-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1f103-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1f103-131">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1f103-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f103-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1f103-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1f103-133">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1f103-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f103-134"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="1f103-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1f103-135">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="1f103-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="1f103-136">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1f103-136">See Also</span></span>

[<span data-ttu-id="1f103-137">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="1f103-137">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="1f103-138">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="1f103-138">JET_ENUMCOLUMNVALUE</span></span>]()  
[<span data-ttu-id="1f103-139">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1f103-139">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1f103-140">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="1f103-140">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="1f103-141">realloc</span><span class="sxs-lookup"><span data-stu-id="1f103-141">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
