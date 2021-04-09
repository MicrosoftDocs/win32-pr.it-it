---
description: 'Altre informazioni su: struttura JET_ENUMCOLUMN'
title: Struttura JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN Structure
ms:assetid: f8f512fd-5fcf-47ed-a5db-2fb3bd76c2d7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294138(v=EXCHG.10)
ms:contentKeyID: 32765752
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
ms.openlocfilehash: ca204fef4e67e6883584511b1ac424149a137b79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128223"
---
# <a name="jet_enumcolumn-structure"></a><span data-ttu-id="9153a-103">Struttura JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="9153a-103">JET_ENUMCOLUMN Structure</span></span>


<span data-ttu-id="9153a-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9153a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumn-structure"></a><span data-ttu-id="9153a-105">Struttura JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="9153a-105">JET_ENUMCOLUMN Structure</span></span>

<span data-ttu-id="9153a-106">La struttura **JET_ENUMCOLUMN** enumera i valori di colonna di un record quando viene utilizzata la funzione [JetEnumerateColumns](./jetenumeratecolumns-function.md) .</span><span class="sxs-lookup"><span data-stu-id="9153a-106">The **JET_ENUMCOLUMN** structure enumerates the column values of a record when the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function is used.</span></span> <span data-ttu-id="9153a-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) restituisce una matrice di strutture di **JET_ENUMCOLUMN** .</span><span class="sxs-lookup"><span data-stu-id="9153a-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMN** structures.</span></span> <span data-ttu-id="9153a-108">La matrice viene restituita nella memoria allocata usando il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a tale API.</span><span class="sxs-lookup"><span data-stu-id="9153a-108">The array is returned in memory that is allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to that API.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      JET_ERR err;
      union {
        struct {
          unsigned long cEnumColumnValue;
          JET_ENUMCOLUMNVALUE rgEnumColumnValue;
        };
        struct {
          unsigned long cbData;
          void* pvData;
        };
      };
    } JET_ENUMCOLUMN;
```

### <a name="members"></a><span data-ttu-id="9153a-109">Membri</span><span class="sxs-lookup"><span data-stu-id="9153a-109">Members</span></span>

<span data-ttu-id="9153a-110">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="9153a-110">**columnid**</span></span>

<span data-ttu-id="9153a-111">ID di colonna enumerato.</span><span class="sxs-lookup"><span data-stu-id="9153a-111">The column ID that was enumerated.</span></span>

<span data-ttu-id="9153a-112">**Err**</span><span class="sxs-lookup"><span data-stu-id="9153a-112">**err**</span></span>

<span data-ttu-id="9153a-113">Codice di stato della colonna risultante dall'enumerazione della colonna.</span><span class="sxs-lookup"><span data-stu-id="9153a-113">The column status code that results from the enumeration of the column.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9153a-114">Codici errore</span><span class="sxs-lookup"><span data-stu-id="9153a-114">Error Codes</span></span></p></th>
<th><p><span data-ttu-id="9153a-115">Significato</span><span class="sxs-lookup"><span data-stu-id="9153a-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9153a-116">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="9153a-116">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="9153a-117">L'ID di colonna non rientra nei limiti validi di un ID di colonna.</span><span class="sxs-lookup"><span data-stu-id="9153a-117">The column ID is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9153a-118">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="9153a-118">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="9153a-119">La colonna descritta dall'ID di colonna non esiste nella tabella.</span><span class="sxs-lookup"><span data-stu-id="9153a-119">The column described by the column ID does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9153a-120">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="9153a-120">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="9153a-121">Tutti i valori per questa colonna sono NULL.</span><span class="sxs-lookup"><span data-stu-id="9153a-121">All values for this column are NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9153a-122">JET_wrnColumnPresent</span><span class="sxs-lookup"><span data-stu-id="9153a-122">JET_wrnColumnPresent</span></span></p></td>
<td><p><span data-ttu-id="9153a-123">È stato specificato JET_bitEnumeratePresenceOnly e per questa colonna è stato restituito almeno un valore di colonna non NULL.</span><span class="sxs-lookup"><span data-stu-id="9153a-123">JET_bitEnumeratePresenceOnly was specified and at least one non-NULL column value would have been returned for this column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9153a-124">JET_wrnColumnSingleValue</span><span class="sxs-lookup"><span data-stu-id="9153a-124">JET_wrnColumnSingleValue</span></span></p></td>
<td><p><span data-ttu-id="9153a-125">JET_bitEnumerateCompressOutput è stato specificato ed è stato restituito esattamente un valore di colonna non NULL per questa colonna.</span><span class="sxs-lookup"><span data-stu-id="9153a-125">JET_bitEnumerateCompressOutput was specified and exactly one non-NULL column value has been returned for this column.</span></span> <span data-ttu-id="9153a-126">Di conseguenza, viene restituito il formato compresso di <strong>JET_ENUMCOLUMN</strong> .</span><span class="sxs-lookup"><span data-stu-id="9153a-126">As a result, the compressed form of <strong>JET_ENUMCOLUMN</strong> has been returned.</span></span> <span data-ttu-id="9153a-127">Per ulteriori informazioni, vedere <strong>JET_ENUMCOLUMN</strong> .</span><span class="sxs-lookup"><span data-stu-id="9153a-127">See <strong>JET_ENUMCOLUMN</strong> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9153a-128">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="9153a-128">JET_wrnColumnSkipped</span></span></p></td>
<td><p><span data-ttu-id="9153a-129">L'ID di colonna nello struct <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> corrispondente a questo struct di <strong>JET_ENUMCOLUMN</strong> è zero.</span><span class="sxs-lookup"><span data-stu-id="9153a-129">The column ID in the <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> struct corresponding to this <strong>JET_ENUMCOLUMN</strong> struct was zero.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9153a-130">**cEnumColumnValue**</span><span class="sxs-lookup"><span data-stu-id="9153a-130">**cEnumColumnValue**</span></span>

<span data-ttu-id="9153a-131">Matrice di valori di colonna enumerata per la colonna.</span><span class="sxs-lookup"><span data-stu-id="9153a-131">The array of column values that was enumerated for the column.</span></span> <span data-ttu-id="9153a-132">Il buffer di output viene restituito nella memoria allocata mediante il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="9153a-132">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="9153a-133">Questo buffer di output viene utilizzato quando il codice di stato della colonna non è uguale a JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="9153a-133">This output buffer is used when the column status code is not equal to JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="9153a-134">Per ulteriori informazioni, vedere [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="9153a-134">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="9153a-135">Viene restituito se "ERR \! = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="9153a-135">This is returned if "err \!= JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="9153a-136">**rgEnumColumnValue**</span><span class="sxs-lookup"><span data-stu-id="9153a-136">**rgEnumColumnValue**</span></span>

<span data-ttu-id="9153a-137">Matrice di valori di colonna enumerata per la colonna.</span><span class="sxs-lookup"><span data-stu-id="9153a-137">The array of column values that was enumerated for the column.</span></span> <span data-ttu-id="9153a-138">Il buffer di output viene restituito nella memoria allocata mediante il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="9153a-138">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="9153a-139">Questo buffer di output viene utilizzato quando il codice di stato della colonna non è uguale a JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="9153a-139">This output buffer is used when the column status code is not equal to JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="9153a-140">Per ulteriori informazioni, vedere [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="9153a-140">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="9153a-141">Viene restituito se "ERR \! = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="9153a-141">This is returned if "err \!= JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="9153a-142">**cbData**</span><span class="sxs-lookup"><span data-stu-id="9153a-142">**cbData**</span></span>

<span data-ttu-id="9153a-143">Valore di colonna enumerato per la colonna.</span><span class="sxs-lookup"><span data-stu-id="9153a-143">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="9153a-144">Il buffer di output viene restituito nella memoria allocata mediante il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="9153a-144">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="9153a-145">Questo buffer di output viene utilizzato solo quando il codice di stato della colonna viene JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="9153a-145">This output buffer is only used when the column status code is JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="9153a-146">Per ulteriori informazioni, vedere [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="9153a-146">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="9153a-147">Viene restituito se "Err = = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="9153a-147">This is returned if "err == JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="9153a-148">**pvData**</span><span class="sxs-lookup"><span data-stu-id="9153a-148">**pvData**</span></span>

<span data-ttu-id="9153a-149">Valore di colonna enumerato per la colonna.</span><span class="sxs-lookup"><span data-stu-id="9153a-149">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="9153a-150">Il buffer di output viene restituito nella memoria allocata mediante il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="9153a-150">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="9153a-151">Questo buffer di output viene utilizzato solo quando il codice di stato della colonna viene JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="9153a-151">This output buffer is only used when the column status code is JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="9153a-152">Per ulteriori informazioni, vedere [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="9153a-152">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="9153a-153">Viene restituito se "Err = = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="9153a-153">This is returned if "err == JET_wrnColumnSingleValue".</span></span>

### <a name="requirements"></a><span data-ttu-id="9153a-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9153a-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9153a-155"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9153a-155"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9153a-156">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9153a-156">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9153a-157"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9153a-157"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9153a-158">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9153a-158">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9153a-159"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="9153a-159"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9153a-160">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="9153a-160">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9153a-161">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9153a-161">See Also</span></span>

[<span data-ttu-id="9153a-162">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="9153a-162">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="9153a-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9153a-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9153a-164">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="9153a-164">JET_ENUMCOLUMNID</span></span>](./jet-enumcolumnid-structure.md)  
[<span data-ttu-id="9153a-165">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="9153a-165">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="9153a-166">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="9153a-166">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="9153a-167">realloc</span><span class="sxs-lookup"><span data-stu-id="9153a-167">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
