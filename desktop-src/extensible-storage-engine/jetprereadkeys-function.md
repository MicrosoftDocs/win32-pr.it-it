---
description: 'Altre informazioni su: funzione JetPrereadKeys'
title: JetPrereadKeys (funzione)
TOCTitle: JetPrereadKeys Function
ms:assetid: fc2f46bc-1f81-4af2-aa63-9757e819efc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294143(v=EXCHG.10)
ms:contentKeyID: 32765757
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrereadKeys
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d35407c171bdcd54eb44e9830f382c08a1e6c6c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484876"
---
# <a name="jetprereadkeys-function"></a><span data-ttu-id="1cb57-103">JetPrereadKeys (funzione)</span><span class="sxs-lookup"><span data-stu-id="1cb57-103">JetPrereadKeys Function</span></span>


<span data-ttu-id="1cb57-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1cb57-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetprereadkeys-function"></a><span data-ttu-id="1cb57-105">JetPrereadKeys (funzione)</span><span class="sxs-lookup"><span data-stu-id="1cb57-105">JetPrereadKeys Function</span></span>

<span data-ttu-id="1cb57-106">La funzione **JetPrereadKeys** legge i valori delle chiavi per migliorare le prestazioni della pulizia dell'archivio versioni.</span><span class="sxs-lookup"><span data-stu-id="1cb57-106">The **JetPrereadKeys** function reads key values to improve the performance of version store cleanup.</span></span>

<span data-ttu-id="1cb57-107">**Windows 7:** la funzione PrereadKeys è stata introdotta in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1cb57-107">**Windows 7:  PrereadKeys** function is introduced in Windows 7.</span></span>

```cpp
    JET_ERR JET_API JetPrereadKeys(
      __in JET_SESID sesid,
      __in JET_TABLEID tableid,
      __in_ecount(ckeys) const void ** rgpvKeys,
      __in_ecount(ckeys) const unsigned long * rgcbKeys,
      __in long ckeys,
      __out_opt long * pckeysPreread,
      __in JET_GRBIT grbit
     );
```

### <a name="parameters"></a><span data-ttu-id="1cb57-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cb57-108">Parameters</span></span>

<span data-ttu-id="1cb57-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1cb57-109">*sesid*</span></span>

<span data-ttu-id="1cb57-110">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="1cb57-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="1cb57-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="1cb57-111">*tableid*</span></span>

<span data-ttu-id="1cb57-112">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="1cb57-112">The cursor to use for this call.</span></span>

<span data-ttu-id="1cb57-113">*rgpvKeys*</span><span class="sxs-lookup"><span data-stu-id="1cb57-113">*rgpvKeys*</span></span>

<span data-ttu-id="1cb57-114">Matrice di puntatori alle chiavi.</span><span class="sxs-lookup"><span data-stu-id="1cb57-114">An array of pointers to keys.</span></span> <span data-ttu-id="1cb57-115">Le chiavi possono essere eseguite con [JetMakeKey](./jetmakekey-function.md) o recuperate con [JetGetBookmark](./jetgetbookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="1cb57-115">Keys can be made with [JetMakeKey](./jetmakekey-function.md) or retrieved with [JetGetBookmark](./jetgetbookmark-function.md).</span></span> <span data-ttu-id="1cb57-116">Le chiavi devono essere ordinate in ordine crescente o decrescente, a seconda del grbit passato.</span><span class="sxs-lookup"><span data-stu-id="1cb57-116">The keys must be sorted in ascending or descending order, depending on the grbit passed.</span></span> <span data-ttu-id="1cb57-117">Le chiavi possono essere ordinate con memcmp.</span><span class="sxs-lookup"><span data-stu-id="1cb57-117">Keys can be sorted with memcmp.</span></span>

<span data-ttu-id="1cb57-118">*rgcbKeys*</span><span class="sxs-lookup"><span data-stu-id="1cb57-118">*rgcbKeys*</span></span>

<span data-ttu-id="1cb57-119">Matrice di lunghezze di chiave.</span><span class="sxs-lookup"><span data-stu-id="1cb57-119">An array of key lengths.</span></span> <span data-ttu-id="1cb57-120">rgpvKeys \[ n \] deve puntare a una chiave di lunghezza rgcbKeys \[ n\]</span><span class="sxs-lookup"><span data-stu-id="1cb57-120">rgpvKeys\[n\] should point to a key of length rgcbKeys\[n\]</span></span>

<span data-ttu-id="1cb57-121">*ckeys*</span><span class="sxs-lookup"><span data-stu-id="1cb57-121">*ckeys*</span></span>

<span data-ttu-id="1cb57-122">Numero di chiavi.</span><span class="sxs-lookup"><span data-stu-id="1cb57-122">The number of keys.</span></span> <span data-ttu-id="1cb57-123">rgpvKeys e rgcbKeys devono puntare a una matrice con almeno elementi ckeys.</span><span class="sxs-lookup"><span data-stu-id="1cb57-123">rgpvKeys and rgcbKeys must each point to an array with at least ckeys elements.</span></span>

<span data-ttu-id="1cb57-124">*pckeysPreread*</span><span class="sxs-lookup"><span data-stu-id="1cb57-124">*pckeysPreread*</span></span>

<span data-ttu-id="1cb57-125">Restituisce il numero di chiavi per le quali sono state effettivamente rilasciate le preletture.</span><span class="sxs-lookup"><span data-stu-id="1cb57-125">Returns the number of keys that prereads were actually issued for.</span></span> <span data-ttu-id="1cb57-126">Questo parametro può essere NULL.</span><span class="sxs-lookup"><span data-stu-id="1cb57-126">This parameter can be NULL.</span></span>

<span data-ttu-id="1cb57-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="1cb57-127">*grbit*</span></span>

<span data-ttu-id="1cb57-128">Deve essere JET_bitPrereadForward o JET_bitPrereadBackward.</span><span class="sxs-lookup"><span data-stu-id="1cb57-128">This must be either JET_bitPrereadForward or JET_bitPrereadBackward.</span></span> <span data-ttu-id="1cb57-129">Se grbit è JET_bitPrereadForward, le chiavi devono essere ordinate in ordine crescente.</span><span class="sxs-lookup"><span data-stu-id="1cb57-129">If grbit is JET_bitPrereadForward, the keys must be sorted in ascending order.</span></span> <span data-ttu-id="1cb57-130">Se grbit è JET_bitPrereadBackward, le chiavi devono essere ordinate in ordine decrescente.</span><span class="sxs-lookup"><span data-stu-id="1cb57-130">If grbit is JET_bitPrereadBackward, the keys must be sorted in descending order.</span></span>

### <a name="return-value"></a><span data-ttu-id="1cb57-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cb57-131">Return Value</span></span>

<span data-ttu-id="1cb57-132">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="1cb57-132">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1cb57-133">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="1cb57-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<span data-ttu-id="1cb57-134">È possibile restituire vari errori di I/O insieme a questi errori di utilizzo dell'API:</span><span class="sxs-lookup"><span data-stu-id="1cb57-134">Various I/O errors can be returned along with these API usage errors:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1cb57-135">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1cb57-135">Return code</span></span></p></th>
<th><p><span data-ttu-id="1cb57-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1cb57-136">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1cb57-137">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="1cb57-137">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="1cb57-138">Grbit non è né JET_bitPrereadForward né JET_bitPrereadBackward.</span><span class="sxs-lookup"><span data-stu-id="1cb57-138">Grbit was neither JET_bitPrereadForward nor JET_bitPrereadBackward.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cb57-139">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="1cb57-139">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="1cb57-140">È stata passata una dimensione della chiave non corretta.</span><span class="sxs-lookup"><span data-stu-id="1cb57-140">An incorrect key size has been passed in.</span></span> <span data-ttu-id="1cb57-141">Le chiavi non possono essere 0 o più lunghe della lunghezza massima della chiave per la tabella.</span><span class="sxs-lookup"><span data-stu-id="1cb57-141">Keys can neither be 0 nor longer than the maximum key length for the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cb57-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1cb57-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1cb57-143">È stato passato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="1cb57-143">An invalid parameter has been passed in.</span></span> <span data-ttu-id="1cb57-144">Questo problema può essere causato da un valore null per un parametro obbligatorio oppure può indicare che la matrice di chiavi non è ordinata correttamente.</span><span class="sxs-lookup"><span data-stu-id="1cb57-144">This can be caused by a null value for a required parameter or can indicate that the key array is not sorted properly.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1cb57-145">**JetPrereadKeys** attraversa le pagine interne dell'albero b per determinare quali pagine foglia contengono le chiavi specificate da RgpvKeys/rgcbKeys.</span><span class="sxs-lookup"><span data-stu-id="1cb57-145">**JetPrereadKeys** traverses the internal pages of the b-tree to determine which leaf pages contain the keys specified by rgpvKeys/rgcbKeys.</span></span> <span data-ttu-id="1cb57-146">L'elenco delle pagine foglia viene ordinato, quindi vengono rilasciate le preletture per gli intervalli di pagine.</span><span class="sxs-lookup"><span data-stu-id="1cb57-146">The list of leaf pages is sorted and then prereads are issued for the ranges of pages.</span></span> <span data-ttu-id="1cb57-147">Il numero di pagine che è possibile preleggere è limitato ed è quindi possibile che non tutte le chiavi vengano prelette.</span><span class="sxs-lookup"><span data-stu-id="1cb57-147">The number of pages that can be preread is limited so it is possible that not all keys may be preread.</span></span> <span data-ttu-id="1cb57-148">In tal caso, il numero di chiavi effettivamente prelette viene restituito in pckeysPreread.</span><span class="sxs-lookup"><span data-stu-id="1cb57-148">In that case, the number of keys actually preread is returned in pckeysPreread.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1cb57-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cb57-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1cb57-150"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="1cb57-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1cb57-151">Richiede Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1cb57-151">Requires Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cb57-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1cb57-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1cb57-153">Richiede Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1cb57-153">Requires Windows Server 2008 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cb57-154"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="1cb57-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1cb57-155">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="1cb57-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cb57-156"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="1cb57-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1cb57-157">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1cb57-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cb57-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1cb57-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1cb57-159">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1cb57-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>
