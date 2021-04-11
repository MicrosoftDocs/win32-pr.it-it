---
description: 'Altre informazioni su: funzione JetSetCursorFilter'
title: JetSetCursorFilter (funzione)
TOCTitle: JetSetCursorFilter Function
ms:assetid: 3cea5beb-2cf8-4053-8e7f-7b8645580ef0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835040(v=EXCHG.10)
ms:contentKeyID: 49894662
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetCursorFilter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad589fecb190ad0f0676325b78adc7c96028a3fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128634"
---
# <a name="jetsetcursorfilter-function"></a><span data-ttu-id="218ca-103">JetSetCursorFilter (funzione)</span><span class="sxs-lookup"><span data-stu-id="218ca-103">JetSetCursorFilter Function</span></span>


<span data-ttu-id="218ca-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="218ca-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="218ca-105">La funzione **JetSetCursorFilter** imposta una matrice di filtri semplici per la funzione [JetMove](./jetmove-function.md) .</span><span class="sxs-lookup"><span data-stu-id="218ca-105">The **JetSetCursorFilter** function sets an array of simple filters for the [JetMove](./jetmove-function.md) function.</span></span>

<span data-ttu-id="218ca-106">La funzione **JetSetCursorFilter** è stata introdotta nel sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="218ca-106">The **JetSetCursorFilter** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetSetCursorFilter(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in_ecount(cFilters)  JET_INDEX_COLUMN* rgFilters,
  __in          DWORD cFilters,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="218ca-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="218ca-107">Parameters</span></span>

<span data-ttu-id="218ca-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="218ca-108">*sesid*</span></span>

<span data-ttu-id="218ca-109">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="218ca-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="218ca-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="218ca-110">*tableid*</span></span>

<span data-ttu-id="218ca-111">Cursore da posizionare.</span><span class="sxs-lookup"><span data-stu-id="218ca-111">The cursor to position.</span></span>

<span data-ttu-id="218ca-112">*rgFilters*</span><span class="sxs-lookup"><span data-stu-id="218ca-112">*rgFilters*</span></span>

<span data-ttu-id="218ca-113">Filtri dei record semplici.</span><span class="sxs-lookup"><span data-stu-id="218ca-113">The simple record filters.</span></span>

<span data-ttu-id="218ca-114">*cFilters*</span><span class="sxs-lookup"><span data-stu-id="218ca-114">*cFilters*</span></span>

<span data-ttu-id="218ca-115">Numero di filtri.</span><span class="sxs-lookup"><span data-stu-id="218ca-115">The number of filters.</span></span>

<span data-ttu-id="218ca-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="218ca-116">*grbit*</span></span>

<span data-ttu-id="218ca-117">Gruppo di bit che specifica zero o più opzioni di spostamento elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="218ca-117">A group of bits that specifies zero or more of the move options listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="218ca-118">Valore</span><span class="sxs-lookup"><span data-stu-id="218ca-118">Value</span></span></p></th>
<th><p><span data-ttu-id="218ca-119">Significato</span><span class="sxs-lookup"><span data-stu-id="218ca-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="218ca-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="218ca-120">None</span></span></p></td>
<td><p><span data-ttu-id="218ca-121">Opzione predefinita.</span><span class="sxs-lookup"><span data-stu-id="218ca-121">Default option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="218ca-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="218ca-122">Return value</span></span>

<span data-ttu-id="218ca-123">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei codici restituiti elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="218ca-123">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="218ca-124">Per ulteriori informazioni sui possibili errori di Extensible Storage Engine (ESE), vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="218ca-124">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="218ca-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="218ca-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="218ca-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="218ca-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="218ca-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="218ca-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="218ca-128">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="218ca-128">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="218ca-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="218ca-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="218ca-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="218ca-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="218ca-131">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="218ca-131">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="218ca-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="218ca-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="218ca-133">Richiede Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="218ca-133">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="218ca-134"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="218ca-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="218ca-135">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="218ca-135">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="218ca-136"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="218ca-136"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="218ca-137">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="218ca-137">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="218ca-138"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="218ca-138"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="218ca-139">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="218ca-139">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="218ca-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="218ca-140">See also</span></span>

[<span data-ttu-id="218ca-141">JetMove</span><span class="sxs-lookup"><span data-stu-id="218ca-141">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="218ca-142">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="218ca-142">JET_ERR</span></span>](./jet-err.md)
