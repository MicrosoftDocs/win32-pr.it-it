---
description: 'Altre informazioni su: struttura JET_RECSIZE2'
title: Struttura JET_RECSIZE2
TOCTitle: JET_RECSIZE2 Structure
ms:assetid: 02a13b5b-d904-49b2-baaa-c60328d70290
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269174(v=EXCHG.10)
ms:contentKeyID: 32765477
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2fd16480f0ec059c977d07f8e445a35094c5f2fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315085"
---
# <a name="jet_recsize2-structure"></a><span data-ttu-id="e7088-103">Struttura JET_RECSIZE2</span><span class="sxs-lookup"><span data-stu-id="e7088-103">JET_RECSIZE2 Structure</span></span>


<span data-ttu-id="e7088-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e7088-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recsize2-structure"></a><span data-ttu-id="e7088-105">Struttura JET_RECSIZE2</span><span class="sxs-lookup"><span data-stu-id="e7088-105">JET_RECSIZE2 Structure</span></span>

<span data-ttu-id="e7088-106">La struttura **JET_RECSIZE2** viene utilizzata da [JetGetRecordSize2](./jetgetrecordsize2-function.md) per restituire informazioni sui requisiti di utilizzo di un record in spazio dati utente, numero di colonne set, numero di valori e spazio overhead della struttura dei record ESE.</span><span class="sxs-lookup"><span data-stu-id="e7088-106">The **JET_RECSIZE2** structure is used by [JetGetRecordSize2](./jetgetrecordsize2-function.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESE record structure overhead space.</span></span>

<span data-ttu-id="e7088-107">**Windows 7:** La struttura **JET_RECSIZE2** viene introdotta nel sistema operativo Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e7088-107">**Windows 7:** The **JET_RECSIZE2** structure is introduced in the Windows 7 operating system.</span></span>

```cpp
    typedef struct {
      unsigned __int64 cbData;
      unsigned __int64 cbLongValueData;
      unsigned __int64 cbOverhead;
      unsigned __int64 cbLongValueOverhead;
      unsigned __int64 cNonTaggedColumns;
      unsigned __int64 cTaggedColumns;
      unsigned __int64 cLongValues;
      unsigned __int64 cMultiValues;
      unsigned __int64 cCompressedColumns;
      unsigned __int64 cbDataCompressed;
      unsigned __int64 cbLongValueDataCompressed;
    } JET_RECSIZE2;
```

### <a name="members"></a><span data-ttu-id="e7088-108">Membri</span><span class="sxs-lookup"><span data-stu-id="e7088-108">Members</span></span>

<span data-ttu-id="e7088-109">**cbData**</span><span class="sxs-lookup"><span data-stu-id="e7088-109">**cbData**</span></span>

<span data-ttu-id="e7088-110">Set di dati utente nel record.</span><span class="sxs-lookup"><span data-stu-id="e7088-110">User data set in the record.</span></span>

<span data-ttu-id="e7088-111">**Nota**  La dimensione della chiave non è inclusa in questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="e7088-111">**Note**  The key size is not included in this.</span></span>

<span data-ttu-id="e7088-112">**cbLongValueData**</span><span class="sxs-lookup"><span data-stu-id="e7088-112">**cbLongValueData**</span></span>

<span data-ttu-id="e7088-113">Dati utente associati al record ma archiviati nella struttura ad albero di valori Long.</span><span class="sxs-lookup"><span data-stu-id="e7088-113">User data associated with the record but stored in the long-value tree.</span></span>

<span data-ttu-id="e7088-114">**Nota**  Non vengono conteggiati valori Long intrinseci.</span><span class="sxs-lookup"><span data-stu-id="e7088-114">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="e7088-115">**cbOverhead**</span><span class="sxs-lookup"><span data-stu-id="e7088-115">**cbOverhead**</span></span>

<span data-ttu-id="e7088-116">Overhead della struttura di record ESE per questo record.</span><span class="sxs-lookup"><span data-stu-id="e7088-116">The overhead of the ESE record structure for this record.</span></span> <span data-ttu-id="e7088-117">Sono incluse le dimensioni della chiave del record.</span><span class="sxs-lookup"><span data-stu-id="e7088-117">This includes the record's key size.</span></span>

<span data-ttu-id="e7088-118">**cbLongValueOverhead**</span><span class="sxs-lookup"><span data-stu-id="e7088-118">**cbLongValueOverhead**</span></span>

<span data-ttu-id="e7088-119">Overhead dei dati con valori Long.</span><span class="sxs-lookup"><span data-stu-id="e7088-119">The overhead of the long-value data.</span></span>

<span data-ttu-id="e7088-120">**Nota**  Non vengono conteggiati valori Long intrinseci.</span><span class="sxs-lookup"><span data-stu-id="e7088-120">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="e7088-121">**cNonTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="e7088-121">**cNonTaggedColumns**</span></span>

<span data-ttu-id="e7088-122">Numero totale di colonne fisse e variabili impostate in questo record.</span><span class="sxs-lookup"><span data-stu-id="e7088-122">Total number of fixed and variable columns set in this record.</span></span>

<span data-ttu-id="e7088-123">**cTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="e7088-123">**cTaggedColumns**</span></span>

<span data-ttu-id="e7088-124">Numero totale di colonne con tag impostati in questo record.</span><span class="sxs-lookup"><span data-stu-id="e7088-124">Total number of tagged columns set in this record.</span></span>

<span data-ttu-id="e7088-125">**cLongValues**</span><span class="sxs-lookup"><span data-stu-id="e7088-125">**cLongValues**</span></span>

<span data-ttu-id="e7088-126">Numero totale di valori Long archiviati nell'albero dei valori Long per questo record.</span><span class="sxs-lookup"><span data-stu-id="e7088-126">Total number of long values stored in the long-value tree for this record.</span></span>

<span data-ttu-id="e7088-127">**Nota**  Non vengono conteggiati valori Long intrinseci.</span><span class="sxs-lookup"><span data-stu-id="e7088-127">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="e7088-128">**cMultiValues**</span><span class="sxs-lookup"><span data-stu-id="e7088-128">**cMultiValues**</span></span>

<span data-ttu-id="e7088-129">Accumulo del numero totale di valori oltre il primo per tutte le colonne del record.</span><span class="sxs-lookup"><span data-stu-id="e7088-129">The accumulation of the total number of values beyond the first for all columns in the record.</span></span>

<span data-ttu-id="e7088-130">**cCompressedColumns**</span><span class="sxs-lookup"><span data-stu-id="e7088-130">**cCompressedColumns**</span></span>

<span data-ttu-id="e7088-131">Numero totale di colonne compresse.</span><span class="sxs-lookup"><span data-stu-id="e7088-131">The total number of compressed columns.</span></span>

<span data-ttu-id="e7088-132">**cbDataCompressed**</span><span class="sxs-lookup"><span data-stu-id="e7088-132">**cbDataCompressed**</span></span>

<span data-ttu-id="e7088-133">Dimensioni compresse dei dati utente in questo record.</span><span class="sxs-lookup"><span data-stu-id="e7088-133">The compressed size of user data in this record.</span></span> <span data-ttu-id="e7088-134">Si tratta dello stesso valore di cbData se non vengono compressi valori Long intrinseci.</span><span class="sxs-lookup"><span data-stu-id="e7088-134">This is the same as cbData if no intrinsic long-values are compressed.</span></span>

<span data-ttu-id="e7088-135">**cbLongValueDataCompressed**</span><span class="sxs-lookup"><span data-stu-id="e7088-135">**cbLongValueDataCompressed**</span></span>

<span data-ttu-id="e7088-136">Dimensioni compresse dei dati utente nell'albero con valori Long.</span><span class="sxs-lookup"><span data-stu-id="e7088-136">The compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="e7088-137">Si tratta dello stesso valore dei dati cbLongValue se non vengono compressi valori Long separati.</span><span class="sxs-lookup"><span data-stu-id="e7088-137">This is the same as cbLongValue data if no separated long values are compressed.</span></span>

### <a name="remarks"></a><span data-ttu-id="e7088-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7088-138">Remarks</span></span>

<span data-ttu-id="e7088-139">Il numero totale di valori nel record sarà **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.</span><span class="sxs-lookup"><span data-stu-id="e7088-139">The total number of values in the record would be **cMultiValues** + **cNonTaggedColumns** + **cTaggedColumns**.</span></span>

<span data-ttu-id="e7088-140">I dati logici nel record sono (cbData + cbLongValueData) e la dimensione fisica dei dati è (cbDataCompressed + cbLongValueDataCompressed).</span><span class="sxs-lookup"><span data-stu-id="e7088-140">The logical data in the record is (cbData+cbLongValueData) and the physical size of the data is (cbDataCompressed+cbLongValueDataCompressed).</span></span> <span data-ttu-id="e7088-141">Questa operazione può essere utilizzata per calcolare il rapporto di compressione dei dati archiviati.</span><span class="sxs-lookup"><span data-stu-id="e7088-141">This can be used to calculate the compression ratio of stored data.</span></span>

### <a name="requirements"></a><span data-ttu-id="e7088-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7088-142">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7088-143"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e7088-143"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e7088-144">Richiede il sistema operativo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e7088-144">Requires Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7088-145"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e7088-145"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e7088-146">Richiede il sistema operativo Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e7088-146">Requires Windows Server 2008 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7088-147"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="e7088-147"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e7088-148">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="e7088-148">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e7088-149">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e7088-149">See Also</span></span>

[<span data-ttu-id="e7088-150">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="e7088-150">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)  
[<span data-ttu-id="e7088-151">JetGetRecordSize2</span><span class="sxs-lookup"><span data-stu-id="e7088-151">JetGetRecordSize2</span></span>](./jetgetrecordsize2-function.md)
