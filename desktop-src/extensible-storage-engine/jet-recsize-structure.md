---
description: 'Altre informazioni su: struttura JET_RECSIZE'
title: Struttura JET_RECSIZE
TOCTitle: JET_RECSIZE Structure
ms:assetid: bb2a63bb-7956-46c2-9791-0d0678a6c366
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294072(v=EXCHG.10)
ms:contentKeyID: 32765687
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
ms.openlocfilehash: e4e6b2f313a5411ba5bfeea73db3b01afe007612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749855"
---
# <a name="jet_recsize-structure"></a><span data-ttu-id="47b37-103">Struttura JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="47b37-103">JET_RECSIZE Structure</span></span>


<span data-ttu-id="47b37-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="47b37-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recsize-structure"></a><span data-ttu-id="47b37-105">Struttura JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="47b37-105">JET_RECSIZE Structure</span></span>

<span data-ttu-id="47b37-106">La struttura **JET_RECSIZE** viene utilizzata da [JetGetRecordSize](./jetgetrecordsize-function.md) per restituire informazioni sui requisiti di utilizzo di un record in spazio dati utente, numero di colonne set, numero di valori e spazio overhead della struttura dei record ESE.</span><span class="sxs-lookup"><span data-stu-id="47b37-106">The **JET_RECSIZE** structure is used by [JetGetRecordSize](./jetgetrecordsize-function.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESE record structure overhead space.</span></span>

<span data-ttu-id="47b37-107">**Windows Vista:** La struttura **JET_RECSIZE** è stata introdotta in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="47b37-107">**Windows Vista:** The **JET_RECSIZE** structure is introduced in Windows Vista.</span></span>

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
    } JET_RECSIZE;
```

### <a name="members"></a><span data-ttu-id="47b37-108">Membri</span><span class="sxs-lookup"><span data-stu-id="47b37-108">Members</span></span>

<span data-ttu-id="47b37-109">**cbData**</span><span class="sxs-lookup"><span data-stu-id="47b37-109">**cbData**</span></span>

<span data-ttu-id="47b37-110">Set di dati utente nel record.</span><span class="sxs-lookup"><span data-stu-id="47b37-110">User data set in the record.</span></span>

<span data-ttu-id="47b37-111">**Nota**  La dimensione della chiave non è inclusa in questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="47b37-111">**Note**  The key size is not included in this.</span></span>

<span data-ttu-id="47b37-112">**cbLongValueData**</span><span class="sxs-lookup"><span data-stu-id="47b37-112">**cbLongValueData**</span></span>

<span data-ttu-id="47b37-113">Dati utente associati al record ma archiviati nella struttura ad albero di valori Long.</span><span class="sxs-lookup"><span data-stu-id="47b37-113">User data associated with the record but stored in the long-value tree.</span></span>

<span data-ttu-id="47b37-114">**Nota**  Non vengono conteggiati valori Long intrinseci.</span><span class="sxs-lookup"><span data-stu-id="47b37-114">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="47b37-115">**cbOverhead**</span><span class="sxs-lookup"><span data-stu-id="47b37-115">**cbOverhead**</span></span>

<span data-ttu-id="47b37-116">Overhead della struttura di record ESE per questo record.</span><span class="sxs-lookup"><span data-stu-id="47b37-116">The overhead of the ESE record structure for this record.</span></span> <span data-ttu-id="47b37-117">Sono incluse le dimensioni della chiave del record.</span><span class="sxs-lookup"><span data-stu-id="47b37-117">This includes the record's key size.</span></span>

<span data-ttu-id="47b37-118">**cbLongValueOverhead**</span><span class="sxs-lookup"><span data-stu-id="47b37-118">**cbLongValueOverhead**</span></span>

<span data-ttu-id="47b37-119">Overhead dei dati con valori Long.</span><span class="sxs-lookup"><span data-stu-id="47b37-119">The overhead of the long-value data.</span></span>

<span data-ttu-id="47b37-120">**Nota**  Non vengono conteggiati valori Long intrinseci.</span><span class="sxs-lookup"><span data-stu-id="47b37-120">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="47b37-121">**cNonTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="47b37-121">**cNonTaggedColumns**</span></span>

<span data-ttu-id="47b37-122">Numero totale di colonne fisse e variabili impostate in questo record.</span><span class="sxs-lookup"><span data-stu-id="47b37-122">Total number of fixed and variable columns set in this record.</span></span>

<span data-ttu-id="47b37-123">**cTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="47b37-123">**cTaggedColumns**</span></span>

<span data-ttu-id="47b37-124">Numero totale di colonne con tag impostati in questo record.</span><span class="sxs-lookup"><span data-stu-id="47b37-124">Total number of tagged columns set in this record.</span></span>

<span data-ttu-id="47b37-125">**cLongValues**</span><span class="sxs-lookup"><span data-stu-id="47b37-125">**cLongValues**</span></span>

<span data-ttu-id="47b37-126">Numero totale di valori Long archiviati nell'albero dei valori Long per questo record.</span><span class="sxs-lookup"><span data-stu-id="47b37-126">Total number of long values stored in the long-value tree for this record.</span></span>

<span data-ttu-id="47b37-127">**Nota**  Non vengono conteggiati valori Long intrinseci.</span><span class="sxs-lookup"><span data-stu-id="47b37-127">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="47b37-128">**cMultiValues**</span><span class="sxs-lookup"><span data-stu-id="47b37-128">**cMultiValues**</span></span>

<span data-ttu-id="47b37-129">Accumulo del numero totale di valori oltre il primo per tutte le colonne del record.</span><span class="sxs-lookup"><span data-stu-id="47b37-129">The accumulation of the total number of values beyond the first for all columns in the record.</span></span>

### <a name="remarks"></a><span data-ttu-id="47b37-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="47b37-130">Remarks</span></span>

<span data-ttu-id="47b37-131">Il numero totale di valori nel record sarà **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.</span><span class="sxs-lookup"><span data-stu-id="47b37-131">The total number of values in the record would be **cMultiValues** + **cNonTaggedColumns** + **cTaggedColumns**.</span></span>

### <a name="requirements"></a><span data-ttu-id="47b37-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47b37-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47b37-133"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="47b37-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="47b37-134">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="47b37-134">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47b37-135"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="47b37-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="47b37-136">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="47b37-136">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47b37-137"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="47b37-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="47b37-138">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="47b37-138">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="47b37-139">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="47b37-139">See Also</span></span>

[<span data-ttu-id="47b37-140">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="47b37-140">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)
