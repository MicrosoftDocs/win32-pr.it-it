---
description: 'Altre informazioni su: funzione JetPrereadIndexRanges'
title: JetPrereadIndexRanges (funzione)
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cfdd8d25f7008f5fa854cbee32b54fa01942ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128163"
---
# <a name="jetprereadindexranges-function"></a><span data-ttu-id="a71c5-103">JetPrereadIndexRanges (funzione)</span><span class="sxs-lookup"><span data-stu-id="a71c5-103">JetPrereadIndexRanges Function</span></span>


<span data-ttu-id="a71c5-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a71c5-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="a71c5-105">La funzione **JetPrereadIndexRanges** legge gli indici per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a71c5-105">The **JetPrereadIndexRanges** function prereads indexes to improve the performance.</span></span>

<span data-ttu-id="a71c5-106">La funzione **JetPrereadIndexRanges** è stata introdotta nel sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a71c5-106">The **JetPrereadIndexRanges** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="a71c5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a71c5-107">Parameters</span></span>

<span data-ttu-id="a71c5-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a71c5-108">*sesid*</span></span>

<span data-ttu-id="a71c5-109">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="a71c5-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="a71c5-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="a71c5-110">*tableid*</span></span>

<span data-ttu-id="a71c5-111">Tabella su cui eseguire le preletture.</span><span class="sxs-lookup"><span data-stu-id="a71c5-111">The table to issue the prereads against.</span></span>

<span data-ttu-id="a71c5-112">*rgIndexRanges*</span><span class="sxs-lookup"><span data-stu-id="a71c5-112">*rgIndexRanges*</span></span>

<span data-ttu-id="a71c5-113">Intervalli di chiavi da preleggere.</span><span class="sxs-lookup"><span data-stu-id="a71c5-113">The key ranges to preread.</span></span>

<span data-ttu-id="a71c5-114">*cIndexRanges*</span><span class="sxs-lookup"><span data-stu-id="a71c5-114">*cIndexRanges*</span></span>

<span data-ttu-id="a71c5-115">Numero di intervalli di chiavi da preleggere, determinato dal numero di elementi in *rgIndexRanges*.</span><span class="sxs-lookup"><span data-stu-id="a71c5-115">The number of key ranges to preread, determined by the number of elements in *rgIndexRanges*.</span></span>

<span data-ttu-id="a71c5-116">*pcRangesPreread*</span><span class="sxs-lookup"><span data-stu-id="a71c5-116">*pcRangesPreread*</span></span>

<span data-ttu-id="a71c5-117">Numero di intervalli di chiavi effettivamente preletti.</span><span class="sxs-lookup"><span data-stu-id="a71c5-117">The number of key ranges that were actually preread.</span></span>

<span data-ttu-id="a71c5-118">*rgcolumnidPreread*</span><span class="sxs-lookup"><span data-stu-id="a71c5-118">*rgcolumnidPreread*</span></span>

<span data-ttu-id="a71c5-119">Elenco di ID di colonna per le colonne con valore esteso da preleggere.</span><span class="sxs-lookup"><span data-stu-id="a71c5-119">List of column IDs for long value columns to preread.</span></span> <span data-ttu-id="a71c5-120">Per impostazione predefinita, solo il record di pagina è preletto.</span><span class="sxs-lookup"><span data-stu-id="a71c5-120">By default, only the on-page record is preread.</span></span> <span data-ttu-id="a71c5-121">Se è necessario preleggere le colonne con valore Long all'esterno della pagina, gli ID di colonna devono essere passati tramite questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a71c5-121">If Off-page long value columns need to be preread, their column IDs need to be passed via this parameter.</span></span>

<span data-ttu-id="a71c5-122">*ccolumnidPreread*</span><span class="sxs-lookup"><span data-stu-id="a71c5-122">*ccolumnidPreread*</span></span>

<span data-ttu-id="a71c5-123">Numero di ID di colonna per le colonne con valore lungo da preleggere, determinato dal numero di elementi in *rgcolumnidPreread*.</span><span class="sxs-lookup"><span data-stu-id="a71c5-123">The number of column IDs for long value columns to preread, determined by the number of elements in *rgcolumnidPreread*.</span></span>

<span data-ttu-id="a71c5-124">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a71c5-124">*grbit*</span></span>

<span data-ttu-id="a71c5-125">Gruppo di bit che specifica zero o più valori di direzione di prelettura elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a71c5-125">A group of bits that specifies zero or more of the preread direction values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a71c5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="a71c5-126">Value</span></span></p></th>
<th><p><span data-ttu-id="a71c5-127">Significato</span><span class="sxs-lookup"><span data-stu-id="a71c5-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a71c5-128">Inoltra</span><span class="sxs-lookup"><span data-stu-id="a71c5-128">Forward</span></span></p></td>
<td><p><span data-ttu-id="a71c5-129">Prelettura in futuro.</span><span class="sxs-lookup"><span data-stu-id="a71c5-129">Preread forward.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a71c5-130">Indietro</span><span class="sxs-lookup"><span data-stu-id="a71c5-130">Backwards</span></span></p></td>
<td><p><span data-ttu-id="a71c5-131">Prelettura indietro.</span><span class="sxs-lookup"><span data-stu-id="a71c5-131">Preread backward.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a71c5-132">FirstPageOnly</span><span class="sxs-lookup"><span data-stu-id="a71c5-132">FirstPageOnly</span></span></p></td>
<td><p><span data-ttu-id="a71c5-133">Prelettura solo della prima pagina di qualsiasi colonna lungo.</span><span class="sxs-lookup"><span data-stu-id="a71c5-133">Preread only the first page of any long column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a71c5-134">NormalizedKey</span><span class="sxs-lookup"><span data-stu-id="a71c5-134">NormalizedKey</span></span></p></td>
<td><p><span data-ttu-id="a71c5-135">Chiave/segnalibro normalizzato fornito al posto del valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="a71c5-135">Normalized key/bookmark provided instead of column value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a71c5-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a71c5-136">Return value</span></span>

<span data-ttu-id="a71c5-137">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei codici restituiti elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a71c5-137">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="a71c5-138">Per ulteriori informazioni sui possibili errori di Extensible Storage Engine (ESE), vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="a71c5-138">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a71c5-139">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a71c5-139">Return code</span></span></p></th>
<th><p><span data-ttu-id="a71c5-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a71c5-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a71c5-141">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a71c5-141">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a71c5-142">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="a71c5-142">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="a71c5-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="a71c5-143">Remarks</span></span>

<span data-ttu-id="a71c5-144">Se i record con gli intervalli di chiavi specificati non si trovano nella cache buffer, è consigliabile avviare le letture asincrone per inserire i record nella cache buffer del database.</span><span class="sxs-lookup"><span data-stu-id="a71c5-144">If the records with the specified key ranges are not in the buffer cache, you should start asynchronous reads to bring the records into the database buffer cache.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a71c5-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a71c5-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a71c5-146"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a71c5-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a71c5-147">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a71c5-147">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a71c5-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a71c5-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a71c5-149">Richiede Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="a71c5-149">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a71c5-150"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="a71c5-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a71c5-151">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="a71c5-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a71c5-152"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="a71c5-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a71c5-153">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a71c5-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a71c5-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a71c5-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a71c5-155">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a71c5-155">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a71c5-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a71c5-156">See also</span></span>

[<span data-ttu-id="a71c5-157">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a71c5-157">JET_ERR</span></span>](./jet-err.md)
