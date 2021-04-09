---
description: 'Altre informazioni su: funzione JetGetSessionParameter'
title: JetGetSessionParameter (funzione)
TOCTitle: JetGetSessionParameter Function
ms:assetid: 36fbcc06-a72d-4bfb-976b-1b705487732a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835039(v=EXCHG.10)
ms:contentKeyID: 49894661
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetGetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0ac02142d48009d668d903b39163b425d738b55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878577"
---
# <a name="jetgetsessionparameter-function"></a><span data-ttu-id="2705c-103">JetGetSessionParameter (funzione)</span><span class="sxs-lookup"><span data-stu-id="2705c-103">JetGetSessionParameter Function</span></span>


<span data-ttu-id="2705c-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2705c-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="2705c-105">La funzione **JetGetSessionParameter** legge il parametro Session per la sessione specificata.</span><span class="sxs-lookup"><span data-stu-id="2705c-105">The **JetGetSessionParameter** function reads the session parameter for the given session.</span></span>

<span data-ttu-id="2705c-106">La funzione **JetGetSessionParameter** è stata introdotta nel sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2705c-106">The **JetGetSessionParameter** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetGetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __out_cap_post_count_(cbParamMax, *pcbParamActual)  void* pvParam,
  __in          unsigned long cbParamMax,
  __out_opt_    unsigned long pcbParamActual
);
```

### <a name="parameters"></a><span data-ttu-id="2705c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2705c-107">Parameters</span></span>

<span data-ttu-id="2705c-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="2705c-108">*sesid*</span></span>

<span data-ttu-id="2705c-109">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="2705c-109">The session to use for this call.</span></span>

<span data-ttu-id="2705c-110">Quando specificato, l'istanza specificata viene ignorata e viene utilizzata l'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="2705c-110">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="2705c-111">*sesparamid*</span><span class="sxs-lookup"><span data-stu-id="2705c-111">*sesparamid*</span></span>

<span data-ttu-id="2705c-112">ID del parametro della sessione da impostare.</span><span class="sxs-lookup"><span data-stu-id="2705c-112">The ID of the session parameter to set.</span></span>

<span data-ttu-id="2705c-113">*pvParam*</span><span class="sxs-lookup"><span data-stu-id="2705c-113">*pvParam*</span></span>

<span data-ttu-id="2705c-114">Dati in questo parametro della sessione.</span><span class="sxs-lookup"><span data-stu-id="2705c-114">Data in this session parameter.</span></span>

<span data-ttu-id="2705c-115">*cbParamMax*</span><span class="sxs-lookup"><span data-stu-id="2705c-115">*cbParamMax*</span></span>

<span data-ttu-id="2705c-116">Dimensione massima del set di dati in questo parametro della sessione.</span><span class="sxs-lookup"><span data-stu-id="2705c-116">The maximum size of the data set in this session parameter.</span></span>

<span data-ttu-id="2705c-117">*pcbParamActual*</span><span class="sxs-lookup"><span data-stu-id="2705c-117">*pcbParamActual*</span></span>

<span data-ttu-id="2705c-118">Dimensioni effettive del set di dati in questo parametro della sessione.</span><span class="sxs-lookup"><span data-stu-id="2705c-118">The actual size of the data set in this session parameter.</span></span>

### <a name="return-value"></a><span data-ttu-id="2705c-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2705c-119">Return value</span></span>

<span data-ttu-id="2705c-120">In caso di esito positivo, il buffer di output appropriato per il parametro della sessione richiesto verrà impostato sul valore di tale parametro della sessione.</span><span class="sxs-lookup"><span data-stu-id="2705c-120">On success, the output buffer appropriate for the requested session parameter will be set to the value of that session parameter.</span></span>

<span data-ttu-id="2705c-121">In caso di errore, lo stato dei buffer di output sarà indefinito.</span><span class="sxs-lookup"><span data-stu-id="2705c-121">On failure, the state of the output buffers will be undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2705c-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="2705c-122">Remarks</span></span>

<span data-ttu-id="2705c-123">Il parametro Session viene usato per la durata della sessione o finché non viene reimpostato il valore.</span><span class="sxs-lookup"><span data-stu-id="2705c-123">The session parameter is used for the lifetime of the session or until the value is reset.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2705c-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2705c-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2705c-125"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2705c-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2705c-126">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2705c-126">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2705c-127"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2705c-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2705c-128">Richiede Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2705c-128">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2705c-129"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="2705c-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2705c-130">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="2705c-130">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2705c-131"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="2705c-131"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2705c-132">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2705c-132">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2705c-133"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2705c-133"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2705c-134">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2705c-134">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2705c-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2705c-135">See also</span></span>

[<span data-ttu-id="2705c-136">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="2705c-136">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="2705c-137">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2705c-137">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2705c-138">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="2705c-138">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="2705c-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2705c-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2705c-140">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="2705c-140">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="2705c-141">JetInit</span><span class="sxs-lookup"><span data-stu-id="2705c-141">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="2705c-142">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="2705c-142">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="2705c-143">JetStopService</span><span class="sxs-lookup"><span data-stu-id="2705c-143">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="2705c-144">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="2705c-144">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
