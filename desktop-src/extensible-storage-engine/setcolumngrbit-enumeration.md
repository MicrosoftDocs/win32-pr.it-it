---
description: 'Altre informazioni su: Enumerazione SetColumnGrbit'
title: Enumerazione SetColumnGrbit
TOCTitle: SetColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39509934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893f8e79b910a305bf6caccacd2d928e947be693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485228"
---
# <a name="setcolumngrbit-enumeration"></a><span data-ttu-id="ebe78-103">Enumerazione SetColumnGrbit</span><span class="sxs-lookup"><span data-stu-id="ebe78-103">SetColumnGrbit enumeration</span></span>

<span data-ttu-id="ebe78-104">Opzioni per JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="ebe78-104">Options for JetSetColumn.</span></span>

<span data-ttu-id="ebe78-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="ebe78-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="ebe78-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ebe78-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ebe78-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ebe78-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe78-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebe78-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetColumnGrbit
'Usage
Dim instance As SetColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum SetColumnGrbit
```

## <a name="members"></a><span data-ttu-id="ebe78-109">Members</span><span class="sxs-lookup"><span data-stu-id="ebe78-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ebe78-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="ebe78-110">Member name</span></span></th>
<th><span data-ttu-id="ebe78-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebe78-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ebe78-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="ebe78-112">None</span></span></td>
<td><span data-ttu-id="ebe78-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="ebe78-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ebe78-114">AppendLV</span><span class="sxs-lookup"><span data-stu-id="ebe78-114">AppendLV</span></span></td>
<td><span data-ttu-id="ebe78-115">Questa opzione consente di accodare i dati a una colonna di tipo JET_coltypLongText o JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="ebe78-115">This option is used to append data to a column of type JET_coltypLongText or JET_coltypLongBinary.</span></span> <span data-ttu-id="ebe78-116">È possibile ottenere lo stesso comportamento determinando la dimensione del valore Long esistente e specificando ibLongValue in psetinfo.</span><span class="sxs-lookup"><span data-stu-id="ebe78-116">The same behavior can be achieved by determining the size of the existing long value and specifying ibLongValue in psetinfo.</span></span> <span data-ttu-id="ebe78-117">Tuttavia, è più semplice utilizzare questo grbit poiché la conoscenza della dimensione del valore della colonna esistente non è necessaria.</span><span class="sxs-lookup"><span data-stu-id="ebe78-117">However, its simpler to use this grbit since knowing the size of the existing column value is not necessary.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ebe78-118">OverwriteLV</span><span class="sxs-lookup"><span data-stu-id="ebe78-118">OverwriteLV</span></span></td>
<td><span data-ttu-id="ebe78-119">Questa opzione consente di sostituire il valore Long esistente con i dati appena forniti.</span><span class="sxs-lookup"><span data-stu-id="ebe78-119">This option is used replace the existing long value with the newly provided data.</span></span> <span data-ttu-id="ebe78-120">Quando si utilizza questa opzione, è come se il valore Long esistente fosse stato impostato su 0 (zero) lunghezza prima dell'impostazione dei nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="ebe78-120">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ebe78-121">RevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="ebe78-121">RevertToDefaultValue</span></span></td>
<td><span data-ttu-id="ebe78-122">Questa opzione è applicabile solo per le colonne con tag, sparse o multivalore.</span><span class="sxs-lookup"><span data-stu-id="ebe78-122">This option is only applicable for tagged, sparse or multi-valued columns.</span></span> <span data-ttu-id="ebe78-123">Causa la restituzione del valore predefinito della colonna nelle successive operazioni di recupero della colonna.</span><span class="sxs-lookup"><span data-stu-id="ebe78-123">It causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="ebe78-124">Tutti i valori di colonna esistenti vengono rimossi.</span><span class="sxs-lookup"><span data-stu-id="ebe78-124">All existing column values are removed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ebe78-125">SeparateLV</span><span class="sxs-lookup"><span data-stu-id="ebe78-125">SeparateLV</span></span></td>
<td><span data-ttu-id="ebe78-126">Questa opzione viene usata per forzare un valore Long, ovvero colonne di tipo JET_coltyp. LongText o JET_coltyp. LongBinary, da archiviare separatamente dal resto dei dati del record.</span><span class="sxs-lookup"><span data-stu-id="ebe78-126">This option is used to force a long value, columns of type JET_coltyp.LongText or JET_coltyp.LongBinary, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="ebe78-127">Questa situazione si verifica in genere quando la dimensione del valore Long impedisce che venga archiviata con i dati dei record rimanenti.</span><span class="sxs-lookup"><span data-stu-id="ebe78-127">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="ebe78-128">Tuttavia, questa opzione può essere usata per forzare l'archiviazione separata del valore Long.</span><span class="sxs-lookup"><span data-stu-id="ebe78-128">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="ebe78-129">Si noti che non è possibile forzare la separazione dei valori long di quattro byte di dimensioni minori.</span><span class="sxs-lookup"><span data-stu-id="ebe78-129">Note that long values four bytes in size of smaller cannot be forced to be separate.</span></span> <span data-ttu-id="ebe78-130">In questi casi, l'opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="ebe78-130">In such cases, the option is ignored.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ebe78-131">SizeLV</span><span class="sxs-lookup"><span data-stu-id="ebe78-131">SizeLV</span></span></td>
<td><span data-ttu-id="ebe78-132">Questa opzione viene usata per interpretare il buffer di input come numero intero di byte da impostare come lunghezza del valore Long descritto dal ColumnID specificato e, se specificato, il numero di sequenza in psetinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="ebe78-132">This option is used to interpret the input buffer as a integer number of bytes to set as the length of the long value described by the given columnid and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="ebe78-133">Se la dimensione specificata è maggiore del valore della colonna esistente, la colonna verrà estesa con 0.</span><span class="sxs-lookup"><span data-stu-id="ebe78-133">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="ebe78-134">Se le dimensioni sono inferiori al valore della colonna esistente, il valore verrà troncato.</span><span class="sxs-lookup"><span data-stu-id="ebe78-134">If the size is smaller than the existing column value then the value will be truncated.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ebe78-135">UniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="ebe78-135">UniqueMultiValues</span></span></td>
<td><span data-ttu-id="ebe78-136">Questa opzione viene utilizzata per applicare che tutti i valori di una colonna multivalore sono distinti.</span><span class="sxs-lookup"><span data-stu-id="ebe78-136">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="ebe78-137">Questa opzione consente di confrontare i dati della colonna di origine, senza alcuna trasformazione, con altri valori di colonna esistenti e viene restituito un errore se viene trovato un duplicato.</span><span class="sxs-lookup"><span data-stu-id="ebe78-137">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="ebe78-138">Se viene specificata questa opzione, non è possibile specificare anche AppendLV, OverwriteLV e SizeLV.</span><span class="sxs-lookup"><span data-stu-id="ebe78-138">If this option is given, then AppendLV, OverwriteLV and SizeLV cannot also be given.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ebe78-139">UniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="ebe78-139">UniqueNormalizedMultiValues</span></span></td>
<td><span data-ttu-id="ebe78-140">Questa opzione viene utilizzata per applicare che tutti i valori di una colonna multivalore sono distinti.</span><span class="sxs-lookup"><span data-stu-id="ebe78-140">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="ebe78-141">Questa opzione Confronta la chiave di trasformazione normalizzata dei dati della colonna, ad altri valori di colonna esistenti trasformati in modo simile e viene restituito un errore se viene trovato un duplicato.</span><span class="sxs-lookup"><span data-stu-id="ebe78-141">This option compares the key normalized transformation of column data, to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="ebe78-142">Se viene specificata questa opzione, non è possibile specificare anche AppendLV, OverwriteLV e SizeLV.</span><span class="sxs-lookup"><span data-stu-id="ebe78-142">If this option is given, then AppendLV, OverwriteLV and SizeLV cannot also be given.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ebe78-143">ZeroLength</span><span class="sxs-lookup"><span data-stu-id="ebe78-143">ZeroLength</span></span></td>
<td><span data-ttu-id="ebe78-144">Questa opzione viene utilizzata per impostare un valore su una lunghezza pari a zero.</span><span class="sxs-lookup"><span data-stu-id="ebe78-144">This option is used to set a value to zero length.</span></span> <span data-ttu-id="ebe78-145">In genere, un valore di colonna è impostato su NULL passando un cbMax di 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="ebe78-145">Normally, a column value is set to NULL by passing a cbMax of 0 (zero).</span></span> <span data-ttu-id="ebe78-146">Tuttavia, per alcuni tipi, ad esempio JET_coltyp. Text, un valore di colonna può essere 0 (zero) Length anziché NULL e questa opzione viene usata per distinguere tra NULL e 0 (zero) Length.</span><span class="sxs-lookup"><span data-stu-id="ebe78-146">However, for some types, like JET_coltyp.Text, a column value can be 0 (zero) length instead of NULL, and this option is used to differentiate between NULL and 0 (zero) length.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ebe78-147">IntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="ebe78-147">IntrinsicLV</span></span></td>
<td><span data-ttu-id="ebe78-148">Provare a archiviare le colonne con valore Long nel record, anche se superano le dimensioni di separazione predefinite.</span><span class="sxs-lookup"><span data-stu-id="ebe78-148">Try to store long-value columns in the record, even if they exceed the default separation size.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ebe78-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebe78-149">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ebe78-150">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ebe78-150">Reference</span></span>

[<span data-ttu-id="ebe78-151">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ebe78-151">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="ebe78-152">Compressed</span><span class="sxs-lookup"><span data-stu-id="ebe78-152">Compressed</span></span>](./windows7grbits.compressed-field.md)

[<span data-ttu-id="ebe78-153">Non compresso</span><span class="sxs-lookup"><span data-stu-id="ebe78-153">Uncompressed</span></span>](./windows7grbits.uncompressed-field.md)
