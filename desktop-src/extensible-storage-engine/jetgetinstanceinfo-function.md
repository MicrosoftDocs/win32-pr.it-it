---
description: 'Altre informazioni su: funzione JetGetInstanceInfo'
title: JetGetInstanceInfo (funzione)
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8c8e9a279f536622cfdfccb8bc8882914aeee64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883469"
---
# <a name="jetgetinstanceinfo-function"></a><span data-ttu-id="83981-103">JetGetInstanceInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="83981-103">JetGetInstanceInfo Function</span></span>


<span data-ttu-id="83981-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="83981-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetinstanceinfo-function"></a><span data-ttu-id="83981-105">JetGetInstanceInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="83981-105">JetGetInstanceInfo Function</span></span>

<span data-ttu-id="83981-106">La funzione **JetGetInstanceInfo** recupera le informazioni sulle istanze in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="83981-106">The **JetGetInstanceInfo** function retrieves information about the instances that are running.</span></span>

<span data-ttu-id="83981-107">**Windows XP: JetGetInstanceInfo** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="83981-107">**Windows XP:  JetGetInstanceInfo** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a><span data-ttu-id="83981-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="83981-108">Parameters</span></span>

<span data-ttu-id="83981-109">*pcInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="83981-109">*pcInstanceInfo*</span></span>

<span data-ttu-id="83981-110">Puntatore a un buffer che riceverà il numero di elementi archiviati in *paInstanceInfo*.</span><span class="sxs-lookup"><span data-stu-id="83981-110">A pointer to a buffer which will receive the number of elements stored in *paInstanceInfo*.</span></span>

<span data-ttu-id="83981-111">*paInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="83981-111">*paInstanceInfo*</span></span>

<span data-ttu-id="83981-112">Puntatore a un buffer che riceverà l'indirizzo del primo elemento di una matrice di strutture.</span><span class="sxs-lookup"><span data-stu-id="83981-112">A pointer to a buffer which will receive the address of the first element of an array of structures.</span></span>

### <a name="return-value"></a><span data-ttu-id="83981-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83981-113">Return Value</span></span>

<span data-ttu-id="83981-114">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="83981-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="83981-115">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="83981-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="83981-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="83981-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="83981-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83981-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83981-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="83981-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="83981-119">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="83981-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83981-120">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="83981-120">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="83981-121">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="83981-121">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="83981-122">Questo errore viene restituito da <strong>JetGetInstanceInfo</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="83981-122">This error will be returned by <strong>JetGetInstanceInfo</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="83981-123"><em>pcInstanceInfo</em> o <em>paInstanceInfo</em> sono null.</span><span class="sxs-lookup"><span data-stu-id="83981-123"><em>pcInstanceInfo</em> or <em>paInstanceInfo</em> are NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83981-124">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="83981-124">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="83981-125">Memoria insufficiente per elaborare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="83981-125">There is insufficient memory to process the request.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="83981-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="83981-126">Remarks</span></span>

<span data-ttu-id="83981-127">Tramite il motore di database viene allocata una matrice di strutture di [JET_INSTANCE_INFO](./jet-instance-info-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="83981-127">The database engine will allocate an array of [JET_INSTANCE_INFO](./jet-instance-info-structure.md) structures.</span></span> <span data-ttu-id="83981-128">Il chiamante è responsabile della liberazione della memoria con [JetFreeBuffer](./jetfreebuffer-function.md).</span><span class="sxs-lookup"><span data-stu-id="83981-128">The caller is responsible for freeing this memory with [JetFreeBuffer](./jetfreebuffer-function.md).</span></span>

<span data-ttu-id="83981-129">Se non sono presenti istanze attive, **JetGetInstanceInfo** restituirà JET_errSuccess e *pcInstanceInfo* riceverà un valore pari a 0.</span><span class="sxs-lookup"><span data-stu-id="83981-129">If there are no active instances, **JetGetInstanceInfo** will return JET_errSuccess, and *pcInstanceInfo* will receive a value of 0.</span></span>

#### <a name="requirements"></a><span data-ttu-id="83981-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83981-130">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83981-131"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="83981-131"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="83981-132">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="83981-132">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83981-133"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="83981-133"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="83981-134">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="83981-134">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83981-135"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="83981-135"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="83981-136">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="83981-136">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83981-137"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="83981-137"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="83981-138">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="83981-138">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83981-139"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="83981-139"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="83981-140">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="83981-140">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83981-141"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="83981-141"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="83981-142">Implementato come <strong>JetGetInstanceInfoW</strong> (Unicode) e <strong>JetGetInstanceInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="83981-142">Implemented as <strong>JetGetInstanceInfoW</strong> (Unicode) and <strong>JetGetInstanceInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="83981-143">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="83981-143">See Also</span></span>

[<span data-ttu-id="83981-144">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="83981-144">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="83981-145">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="83981-145">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="83981-146">JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="83981-146">JET_INSTANCE_INFO</span></span>](./jet-instance-info-structure.md)  
[<span data-ttu-id="83981-147">JetFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="83981-147">JetFreeBuffer</span></span>](./jetfreebuffer-function.md)
