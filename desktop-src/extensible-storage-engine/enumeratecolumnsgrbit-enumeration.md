---
description: 'Altre informazioni su: Enumerazione EnumerateColumnsGrbit'
title: Enumerazione EnumerateColumnsGrbit
TOCTitle: EnumerateColumnsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.enumeratecolumnsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e27e6810b37b513d550bbafce509b2815ccea2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318805"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a><span data-ttu-id="40a36-103">Enumerazione EnumerateColumnsGrbit</span><span class="sxs-lookup"><span data-stu-id="40a36-103">EnumerateColumnsGrbit enumeration</span></span>

<span data-ttu-id="40a36-104">Opzioni per JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="40a36-104">Options for JetEnumerateColumns.</span></span>

<span data-ttu-id="40a36-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="40a36-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="40a36-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="40a36-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="40a36-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="40a36-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="40a36-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40a36-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EnumerateColumnsGrbit
'Usage
Dim instance As EnumerateColumnsGrbit
```

``` csharp
[FlagsAttribute]
public enum EnumerateColumnsGrbit
```

## <a name="members"></a><span data-ttu-id="40a36-109">Members</span><span class="sxs-lookup"><span data-stu-id="40a36-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="40a36-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="40a36-110">Member name</span></span></th>
<th><span data-ttu-id="40a36-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40a36-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="40a36-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="40a36-112">None</span></span></td>
<td><span data-ttu-id="40a36-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="40a36-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="40a36-114">EnumerateCompressOutput</span><span class="sxs-lookup"><span data-stu-id="40a36-114">EnumerateCompressOutput</span></span></td>
<td><span data-ttu-id="40a36-115">Quando si enumerano i valori di colonna, tutte le colonne per cui si recuperano tutti i valori e con un solo valore di colonna non NULL possono essere restituite in formato compresso.</span><span class="sxs-lookup"><span data-stu-id="40a36-115">When enumerating column values, all columns for which we are retrieving all values and that have only one non-NULL column value may be returned in a compressed format.</span></span> <span data-ttu-id="40a36-116">Lo stato di tali colonne verrà impostato su <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> e le dimensioni del valore della colonna e della memoria che contiene il valore della colonna verranno restituite direttamente nella struttura del <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="40a36-116">The status for such columns will be set to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> and the size of the column value and the memory containing the column value will be returned directly in the <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> structure.</span></span> <span data-ttu-id="40a36-117">Non è garantito che tutte le colonne idonee vengano compresse in questo modo.</span><span class="sxs-lookup"><span data-stu-id="40a36-117">It is not guaranteed that all eligible columns are compressed in this manner.</span></span> <span data-ttu-id="40a36-118">Per ulteriori informazioni, vedere <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="40a36-118">See <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="40a36-119">EnumerateCopy</span><span class="sxs-lookup"><span data-stu-id="40a36-119">EnumerateCopy</span></span></td>
<td><span data-ttu-id="40a36-120">Questa opzione indica che è necessario enumerare i valori di colonna modificati del record anziché i valori di colonna originali.</span><span class="sxs-lookup"><span data-stu-id="40a36-120">This option indicates that the modified column values of the record should be enumerated rather than the original column values.</span></span> <span data-ttu-id="40a36-121">Se il valore di una colonna non è stato modificato, il valore della colonna originale viene enumerato.</span><span class="sxs-lookup"><span data-stu-id="40a36-121">If a column value has not been modified, the original column value is enumerated.</span></span> <span data-ttu-id="40a36-122">In questo modo, è possibile enumerare un valore di colonna che non è ancora stato inserito o aggiornato durante l'inserimento o l'aggiornamento di un record.</span><span class="sxs-lookup"><span data-stu-id="40a36-122">In this way, a column value that has not yet been inserted or updated may be enumerated when inserting or updating a record.</span></span>
<p><span data-ttu-id="40a36-123">Questa opzione è identica a <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>.</span><span class="sxs-lookup"><span data-stu-id="40a36-123">This option is identical to <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="40a36-124">EnumerateIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="40a36-124">EnumerateIgnoreDefault</span></span></td>
<td><span data-ttu-id="40a36-125">Se una colonna specificata non è presente nel record, non verrà restituito alcun valore di colonna.</span><span class="sxs-lookup"><span data-stu-id="40a36-125">If a given column is not present in the record then no column value will be returned.</span></span> <span data-ttu-id="40a36-126">In genere, il valore predefinito per la colonna, se presente, verrebbe restituito in questo caso.</span><span class="sxs-lookup"><span data-stu-id="40a36-126">Ordinarily, the default value for the column, if any, would be returned in this case.</span></span> <span data-ttu-id="40a36-127">Si garantisce che se la colonna è impostata su un valore diverso da quello predefinito, verrà restituito un valore diverso, ovvero se una colonna con un valore predefinito viene impostata in modo esplicito su NULL, verrà restituito un valore NULL come valore per la colonna.</span><span class="sxs-lookup"><span data-stu-id="40a36-127">It is guaranteed that if the column is set to a value different than the default value then that different value will be returned (that is, if a column with a default value is explicitly set to NULL then a NULL will be returned as the value for that column).</span></span> <span data-ttu-id="40a36-128">Anche se questa opzione è richiesta, è comunque possibile visualizzare un valore di colonna che corrisponde al valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="40a36-128">Even if this option is requested, it is still possible to see a column value that happens to be equal to the default value.</span></span> <span data-ttu-id="40a36-129">Non viene effettuato alcun tentativo di rimuovere i valori di colonna che corrispondono ai valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="40a36-129">No effort is made to remove column values that match their default values.</span></span> <span data-ttu-id="40a36-130">È importante ricordare che questa opzione influisca sull'output di <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> se usato con EnumeratePresenceOnly o EnumerateTaggedOnly.</span><span class="sxs-lookup"><span data-stu-id="40a36-130">It is important to remember that this option affects the output of <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> when used with EnumeratePresenceOnly or EnumerateTaggedOnly.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="40a36-131">EnumeratePresenceOnly</span><span class="sxs-lookup"><span data-stu-id="40a36-131">EnumeratePresenceOnly</span></span></td>
<td><span data-ttu-id="40a36-132">Se è presente un valore non NULL per il valore della colonna o della colonna richiesta, i dati associati non vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="40a36-132">If a non-NULL value exists for the requested column or column value then the associated data is not returned.</span></span> <span data-ttu-id="40a36-133">Lo stato associato per quel valore di colonna o colonna verrà invece impostato su <a href="hh557250(v=exchg.10).md">ColumnPresent</a>.</span><span class="sxs-lookup"><span data-stu-id="40a36-133">Instead, the associated status for that column or column value will be set to <a href="hh557250(v=exchg.10).md">ColumnPresent</a>.</span></span> <span data-ttu-id="40a36-134">Se il valore della colonna o della colonna è NULL, <a href="hh557250(v=exchg.10).md">ColumnNull</a> verrà restituito come di consueto.</span><span class="sxs-lookup"><span data-stu-id="40a36-134">If the column or column value is NULL then <a href="hh557250(v=exchg.10).md">ColumnNull</a> will be returned as usual.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="40a36-135">EnumerateTaggedOnly</span><span class="sxs-lookup"><span data-stu-id="40a36-135">EnumerateTaggedOnly</span></span></td>
<td><span data-ttu-id="40a36-136">Quando si enumerano tutti i valori di colonna nel record, ad esempio quando numColumnids è zero, verranno restituiti solo i valori delle colonne con tag.</span><span class="sxs-lookup"><span data-stu-id="40a36-136">When enumerating all column values in the record (for example,that is when numColumnids is zero), only tagged column values will be returned.</span></span> <span data-ttu-id="40a36-137">Questa opzione non è consentita durante l'enumerazione di una matrice di ID di colonna specifica.</span><span class="sxs-lookup"><span data-stu-id="40a36-137">This option is not allowed when enumerating a specific array of column IDs.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="40a36-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40a36-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="40a36-139">Riferimento</span><span class="sxs-lookup"><span data-stu-id="40a36-139">Reference</span></span>

[<span data-ttu-id="40a36-140">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="40a36-140">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="40a36-141">EnumerateIgnoreUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="40a36-141">EnumerateIgnoreUserDefinedDefault</span></span>](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[<span data-ttu-id="40a36-142">EnumerateInRecordOnly</span><span class="sxs-lookup"><span data-stu-id="40a36-142">EnumerateInRecordOnly</span></span>](./windows7grbits.enumerateinrecordonly-field.md)
