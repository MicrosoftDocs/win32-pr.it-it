---
description: 'Altre informazioni su: struttura JET_RETINFO'
title: Struttura JET_RETINFO
TOCTitle: JET_RETINFO Structure
ms:assetid: a47a7902-3ecd-4d42-941f-89d25d78eb4c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294049(v=EXCHG.10)
ms:contentKeyID: 32765648
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
ms.openlocfilehash: 3452c4fab7155ea33b556ac7aa2c777b11a3f954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879610"
---
# <a name="jet_retinfo-structure"></a><span data-ttu-id="e8d9a-103">Struttura JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="e8d9a-103">JET_RETINFO Structure</span></span>


<span data-ttu-id="e8d9a-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e8d9a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_retinfo-structure"></a><span data-ttu-id="e8d9a-105">Struttura JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="e8d9a-105">JET_RETINFO Structure</span></span>

<span data-ttu-id="e8d9a-106">La struttura **JET_RETINFO** contiene parametri di input e output facoltativi per [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="e8d9a-106">The **JET_RETINFO** structure contains optional input and output parameters for [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span> <span data-ttu-id="e8d9a-107">Un puntatore null può essere passato dove un puntatore a questa struttura verrebbe altrimenti passato.</span><span class="sxs-lookup"><span data-stu-id="e8d9a-107">A null pointer can be passed where a pointer to this structure would otherwise be passed.</span></span> <span data-ttu-id="e8d9a-108">Il passaggio di un puntatore null equivale a passare **JET_RETINFO** con **cbStruct** impostato su sizeof (JET_RETINFO), **ibLongValue** impostato su 0 (zero) e **itagSequence** impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="e8d9a-108">Passing a null pointer is the same as passing **JET_RETINFO** with **cbStruct** set to sizeof(JET_RETINFO), **ibLongValue** set to 0 (zero) and **itagSequence** set to 1.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
    } JET_RETINFO;
```

### <a name="members"></a><span data-ttu-id="e8d9a-109">Membri</span><span class="sxs-lookup"><span data-stu-id="e8d9a-109">Members</span></span>

<span data-ttu-id="e8d9a-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="e8d9a-110">**cbStruct**</span></span>

<span data-ttu-id="e8d9a-111">Deve essere impostato sulla dimensione della struttura di **JET_RETINFO** , in byte, e serve per confermare la presenza dei campi seguenti.</span><span class="sxs-lookup"><span data-stu-id="e8d9a-111">Must be set to the size of the **JET_RETINFO** structure, in bytes, and serves to confirm the presence of the following fields.</span></span>

<span data-ttu-id="e8d9a-112">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="e8d9a-112">**ibLongValue**</span></span>

<span data-ttu-id="e8d9a-113">Offset al primo byte da recuperare da una colonna di tipo [JET_coltypLongBinary](./jet-coltyp.md)o [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e8d9a-113">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md), or [JET_coltypLongText](./jet-coltyp.md).</span></span> <span data-ttu-id="e8d9a-114">Si noti che la quantità di dati recuperati da questo offset è inferiore alle dimensioni del buffer di output e alla dimensione dei dati nel valore effettivo dopo questo offset.</span><span class="sxs-lookup"><span data-stu-id="e8d9a-114">Note that the amount of data retrieved from this offset is the lower of the size of the output buffer and the size of data in the actual value after this offset.</span></span>

<span data-ttu-id="e8d9a-115">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="e8d9a-115">**itagSequence**</span></span>

<span data-ttu-id="e8d9a-116">Descrive il numero di sequenza del valore in una colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="e8d9a-116">Describes the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="e8d9a-117">Si noti che la matrice di valori è in base uno.</span><span class="sxs-lookup"><span data-stu-id="e8d9a-117">Note that the array of values is one-based.</span></span> <span data-ttu-id="e8d9a-118">Il primo valore è Sequence 1, not 0.</span><span class="sxs-lookup"><span data-stu-id="e8d9a-118">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="e8d9a-119">Se la colonna record ha un solo valore, è necessario passare 1 come **itagSequence**</span><span class="sxs-lookup"><span data-stu-id="e8d9a-119">If the record column has only one value then 1 should be passed as the **itagSequence**</span></span>

<span data-ttu-id="e8d9a-120">Con una colonna che può contenere più valori, è possibile usare un numero di sequenza maggiore di 1 in [JetSetColumn](./jetsetcolumn-function.md) e [JetRetrieveColumn](./jetretrievecolumn-function.md) o 0 in [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="e8d9a-120">With a column that can contain multiple values, it is only possible to use a sequence number larger than 1 in [JetSetColumn](./jetsetcolumn-function.md) and [JetRetrieveColumn](./jetretrievecolumn-function.md) or 0 in [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="e8d9a-121">Nell'implementazione corrente del motore, qualsiasi colonna creata con JET_bitColumnTagged può contenere più valori.</span><span class="sxs-lookup"><span data-stu-id="e8d9a-121">In the current implementation of the engine, any column that was created with JET_bitColumnTagged can contain multiple values.</span></span> <span data-ttu-id="e8d9a-122">Le colonne create con JET_bitColumnMultiValued differiscono dalle colonne con tag multivalore solo nel modo in cui vengono indicizzate.</span><span class="sxs-lookup"><span data-stu-id="e8d9a-122">Columns created with JET_bitColumnMultiValued differ from multi-valued tagged columns only in the way that they are indexed.</span></span> <span data-ttu-id="e8d9a-123">Per ulteriori informazioni, vedere [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="e8d9a-123">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for more information.</span></span>

<span data-ttu-id="e8d9a-124">**columnidNextTagged**</span><span class="sxs-lookup"><span data-stu-id="e8d9a-124">**columnidNextTagged**</span></span>

<span data-ttu-id="e8d9a-125">Restituisce l'ColumnID della colonna con tag, multivalore o di tipo sparse recuperata quando tutte le colonne con tag vengono recuperate passando 0 come ColumnID a [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="e8d9a-125">Returns the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="e8d9a-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8d9a-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8d9a-127"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e8d9a-127"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e8d9a-128">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e8d9a-128">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8d9a-129"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e8d9a-129"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e8d9a-130">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e8d9a-130">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8d9a-131"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="e8d9a-131"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e8d9a-132">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="e8d9a-132">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e8d9a-133">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e8d9a-133">See Also</span></span>

[<span data-ttu-id="e8d9a-134">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="e8d9a-134">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="e8d9a-135">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="e8d9a-135">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="e8d9a-136">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="e8d9a-136">JET_RETINFO</span></span>]()  
[<span data-ttu-id="e8d9a-137">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="e8d9a-137">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)
