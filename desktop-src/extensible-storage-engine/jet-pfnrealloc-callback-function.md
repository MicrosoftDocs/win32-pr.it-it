---
description: 'Altre informazioni su: JET_PFNREALLOC funzione di callback'
title: Funzione di callback JET_PFNREALLOC
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
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
ms.openlocfilehash: 032c1edcfd18166b79f4c8b2868d53d0b84434d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234098"
---
# <a name="jet_pfnrealloc-callback-function"></a><span data-ttu-id="27594-103">Funzione di callback JET_PFNREALLOC</span><span class="sxs-lookup"><span data-stu-id="27594-103">JET_PFNREALLOC Callback Function</span></span>


<span data-ttu-id="27594-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="27594-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pfnrealloc-callback-function"></a><span data-ttu-id="27594-105">Funzione di callback JET_PFNREALLOC</span><span class="sxs-lookup"><span data-stu-id="27594-105">JET_PFNREALLOC Callback Function</span></span>

<span data-ttu-id="27594-106">La funzione JET_PFNREALLOC è un callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) usato da [JetEnumerateColumns](./jetenumeratecolumns-function.md) per allocare memoria per i buffer di output.</span><span class="sxs-lookup"><span data-stu-id="27594-106">The JET_PFNREALLOC function is a [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback used by [JetEnumerateColumns](./jetenumeratecolumns-function.md) to allocate memory for its output buffers.</span></span>

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a><span data-ttu-id="27594-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="27594-107">Parameters</span></span>

<span data-ttu-id="27594-108">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="27594-108">*pvContext*</span></span>

<span data-ttu-id="27594-109">Puntatore di contesto assegnato a [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="27594-109">The context pointer given to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span> <span data-ttu-id="27594-110">Questo puntatore di contesto può essere usato per trasferire lo stato dal chiamante di [JetEnumerateColumns](./jetenumeratecolumns-function.md) all'implementazione di questo callback.</span><span class="sxs-lookup"><span data-stu-id="27594-110">This context pointer can be used to convey state from the caller of [JetEnumerateColumns](./jetenumeratecolumns-function.md) to the implementation of this callback.</span></span>

<span data-ttu-id="27594-111">*PV*</span><span class="sxs-lookup"><span data-stu-id="27594-111">*pv*</span></span>

<span data-ttu-id="27594-112">Se diverso da NULL, specifica un puntatore a un blocco di memoria allocato in precedenza da questo callback.</span><span class="sxs-lookup"><span data-stu-id="27594-112">If non-NULL, specifies a pointer to a memory block previously allocated by this callback.</span></span> <span data-ttu-id="27594-113">Se NULL, verrà allocato un nuovo blocco di memoria della dimensione richiesta.</span><span class="sxs-lookup"><span data-stu-id="27594-113">If NULL, a new memory block of the requested size will be allocated.</span></span>

<span data-ttu-id="27594-114">*CB*</span><span class="sxs-lookup"><span data-stu-id="27594-114">*cb*</span></span>

<span data-ttu-id="27594-115">Nuova dimensione del blocco di memoria in byte.</span><span class="sxs-lookup"><span data-stu-id="27594-115">The new size of the memory block in bytes.</span></span> <span data-ttu-id="27594-116">Se questo parametro è 0 (zero) e viene specificato un blocco di memoria, il blocco di memoria verrà liberato.</span><span class="sxs-lookup"><span data-stu-id="27594-116">If this parameter is 0 (zero) and a memory block is specified, that memory block will be freed.</span></span>

### <a name="return-value"></a><span data-ttu-id="27594-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27594-117">Return Value</span></span>

<span data-ttu-id="27594-118">Il sistema può generare codici di esito positivo o negativo in seguito a una chiamata a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="27594-118">The system may generate success or failure codes as a result of a call to this function.</span></span> <span data-ttu-id="27594-119">Per informazioni su come restituire questi codici come HRESULT, vedere [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="27594-119">For information about how to return these codes as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27594-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="27594-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="27594-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27594-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27594-122">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="27594-122">Success</span></span></p></td>
<td><p><span data-ttu-id="27594-123">Se è stato specificato un blocco di memoria allocato in precedenza ed è stata specificata una nuova dimensione pari a zero, il blocco viene liberato e verrà restituito NULL.</span><span class="sxs-lookup"><span data-stu-id="27594-123">If a previously allocated memory block was specified and a new size of zero was specified then that block is freed and NULL will be returned.</span></span> <span data-ttu-id="27594-124">Se è stato specificato un blocco di memoria allocato in precedenza ed è stata specificata una nuova dimensione diversa da zero, viene restituito il blocco di memoria riallocato.</span><span class="sxs-lookup"><span data-stu-id="27594-124">If a previously allocated memory block was specified and a non-zero new size was specified then the reallocated memory block is returned.</span></span> <span data-ttu-id="27594-125">Se non è stato specificato alcun blocco di memoria, viene restituito un blocco di memoria appena allocato con le dimensioni specificate.</span><span class="sxs-lookup"><span data-stu-id="27594-125">If no memory block was specified then a newly allocated memory block of the specified size is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27594-126">Errore</span><span class="sxs-lookup"><span data-stu-id="27594-126">Failure</span></span></p></td>
<td><p><span data-ttu-id="27594-127">Viene restituito NULL.</span><span class="sxs-lookup"><span data-stu-id="27594-127">NULL will be returned.</span></span> <span data-ttu-id="27594-128">Se è stato fornito un blocco di memoria precedentemente allocato, il blocco rimarrà allocato.</span><span class="sxs-lookup"><span data-stu-id="27594-128">If a previously allocated memory block was provided then that block will remain allocated.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="27594-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27594-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27594-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="27594-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="27594-131">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="27594-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27594-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="27594-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="27594-133">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="27594-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27594-134"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="27594-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="27594-135">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="27594-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="27594-136">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="27594-136">See Also</span></span>

[<span data-ttu-id="27594-137">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="27594-137">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)
