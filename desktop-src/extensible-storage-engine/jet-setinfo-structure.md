---
description: 'Altre informazioni su: struttura JET_SETINFO'
title: Struttura JET_SETINFO
TOCTitle: JET_SETINFO Structure
ms:assetid: cbc41175-e48f-46b0-aeb1-1120fa2cd981
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294090(v=EXCHG.10)
ms:contentKeyID: 32765705
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
ms.openlocfilehash: 69602aad89142d9f5dc202074ca54cf278767892
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531117"
---
# <a name="jet_setinfo-structure"></a><span data-ttu-id="271e7-103">Struttura JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="271e7-103">JET_SETINFO Structure</span></span>


<span data-ttu-id="271e7-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="271e7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setinfo-structure"></a><span data-ttu-id="271e7-105">Struttura JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="271e7-105">JET_SETINFO Structure</span></span>

<span data-ttu-id="271e7-106">La struttura **JET_SETINFO** contiene parametri di input facoltativi per [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="271e7-106">The **JET_SETINFO** structure contains optional input parameters for [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="271e7-107">Un puntatore **null** può essere passato dove un puntatore a questa struttura verrebbe altrimenti passato.</span><span class="sxs-lookup"><span data-stu-id="271e7-107">A **NULL** pointer can be passed where a pointer to this structure would otherwise be passed.</span></span> <span data-ttu-id="271e7-108">Il significato del passaggio di un **valore null** equivale al passaggio **di JET_SETINFO** con **cbStruct** impostato su sizeof (JET_SETINFO), **ibLongValue** impostato su 0 (zero) e **itagSequence** impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="271e7-108">The meaning of passing a **NULL** is the same as passing **JET_SETINFO** with **cbStruct** set to sizeof(JET_SETINFO), **ibLongValue** set to 0 (zero) and **itagSequence** set to 1.</span></span>

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a><span data-ttu-id="271e7-109">Membri</span><span class="sxs-lookup"><span data-stu-id="271e7-109">Members</span></span>

<span data-ttu-id="271e7-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="271e7-110">**cbStruct**</span></span>

<span data-ttu-id="271e7-111">Dimensione, in byte, del **JET_SETINFO**.</span><span class="sxs-lookup"><span data-stu-id="271e7-111">The size, in bytes, of the **JET_SETINFO**.</span></span> <span data-ttu-id="271e7-112">Questo valore conferma la presenza dei campi seguenti.</span><span class="sxs-lookup"><span data-stu-id="271e7-112">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="271e7-113">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="271e7-113">**ibLongValue**</span></span>

<span data-ttu-id="271e7-114">Offset al primo byte da impostare in una colonna di tipo [JET_coltypLongBinary](./jet-coltyp.md) o [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="271e7-114">The offset to the first byte to be set in a column of type [JET_coltypLongBinary](./jet-coltyp.md) or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="271e7-115">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="271e7-115">**itagSequence**</span></span>

<span data-ttu-id="271e7-116">Descrive il numero di sequenza del valore in una colonna multivalore da impostare.</span><span class="sxs-lookup"><span data-stu-id="271e7-116">Describes the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="271e7-117">La matrice di valori è in base uno.</span><span class="sxs-lookup"><span data-stu-id="271e7-117">The array of values is one-based.</span></span> <span data-ttu-id="271e7-118">Il primo valore è Sequence 1, non 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="271e7-118">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="271e7-119">Se la colonna record ha un solo valore, è necessario passare 1 come **itagSequence** se tale valore viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="271e7-119">If the record column has only one value then 1 should be passed as the **itagSequence** if that value is being replaced.</span></span> <span data-ttu-id="271e7-120">Il valore 0 (zero) indica di aggiungere una nuova istanza di valore di colonna alla fine della sequenza dei valori di colonna.</span><span class="sxs-lookup"><span data-stu-id="271e7-120">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="271e7-121">Con una colonna che può contenere più valori, è possibile usare un numero di sequenza maggiore di 1 in [JetSetColumn](./jetsetcolumn-function.md) e [JetRetrieveColumn](./jetretrievecolumn-function.md) o 0 in [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="271e7-121">With a column that can contain multiple values, it is only possible to use a sequence number larger than 1 in [JetSetColumn](./jetsetcolumn-function.md) and [JetRetrieveColumn](./jetretrievecolumn-function.md) or 0 in [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="271e7-122">Nell'implementazione corrente del motore, qualsiasi colonna creata con JET_bitColumnTagged può contenere più valori.</span><span class="sxs-lookup"><span data-stu-id="271e7-122">In the current implementation of the engine, any column that was created with JET_bitColumnTagged can contain multiple values.</span></span> <span data-ttu-id="271e7-123">Le colonne create con JET_bitColumnMultiValued differiscono dalle colonne con tag multivalore solo nel modo in cui vengono indicizzate.</span><span class="sxs-lookup"><span data-stu-id="271e7-123">Columns created with JET_bitColumnMultiValued differ from multi-valued tagged columns only in the way that they are indexed.</span></span> <span data-ttu-id="271e7-124">Per ulteriori informazioni, vedere [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="271e7-124">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for more information.</span></span>

### <a name="requirements"></a><span data-ttu-id="271e7-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="271e7-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="271e7-126"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="271e7-126"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="271e7-127">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="271e7-127">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="271e7-128"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="271e7-128"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="271e7-129">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="271e7-129">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="271e7-130"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="271e7-130"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="271e7-131">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="271e7-131">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="271e7-132">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="271e7-132">See Also</span></span>

[<span data-ttu-id="271e7-133">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="271e7-133">JetSetColumn</span></span>](./jetsetcolumn-function.md)
