---
description: Il metodo Create crea un nuovo supporto con proprietà predefinite, lo aggiunge alla raccolta in corrispondenza dell'indice specificato e restituisce un puntatore all'interfaccia ITMedia.
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: 'Metodo ITMediaCollection:: Create (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8033fb2f541f5451f918845858df756b32361f54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332920"
---
# <a name="itmediacollectioncreate-method"></a><span data-ttu-id="19a4d-103">Metodo ITMediaCollection:: create</span><span class="sxs-lookup"><span data-stu-id="19a4d-103">ITMediaCollection::Create method</span></span>

<span data-ttu-id="19a4d-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="19a4d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="19a4d-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="19a4d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="19a4d-106">Il metodo **create** crea un nuovo supporto con proprietà predefinite, lo aggiunge alla raccolta in corrispondenza dell'indice specificato e restituisce un puntatore all'interfaccia [**ITmedia**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="19a4d-106">The **Create** method creates a new media with default properties, adds it to the collection at the specified index, and returns a pointer to the [**ITMedia**](itmedia.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="19a4d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19a4d-107">Syntax</span></span>


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a><span data-ttu-id="19a4d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="19a4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19a4d-109">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="19a4d-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a4d-110">Indice per il nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="19a4d-110">Index for the new item.</span></span> <span data-ttu-id="19a4d-111">Il valore minimo per l'indice è 1 e il valore massimo per l'indice è il numero corrente di elementi + 1.</span><span class="sxs-lookup"><span data-stu-id="19a4d-111">The minimum value for the index is 1, and the maximum value for the index is the current number of items + 1.</span></span>

</dd> <dt>

<span data-ttu-id="19a4d-112">*ppMedia* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="19a4d-112">*ppMedia* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19a4d-113">Puntatore all'interfaccia [**ITmedia**](itmedia.md) creata.</span><span class="sxs-lookup"><span data-stu-id="19a4d-113">Pointer to [**ITMedia**](itmedia.md) interface created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19a4d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19a4d-114">Return value</span></span>

<span data-ttu-id="19a4d-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="19a4d-115">This method can return one of these values.</span></span>



| <span data-ttu-id="19a4d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="19a4d-116">Value</span></span>                                                                                         | <span data-ttu-id="19a4d-117">Significato</span><span class="sxs-lookup"><span data-stu-id="19a4d-117">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="19a4d-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="19a4d-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="19a4d-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="19a4d-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="19a4d-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="19a4d-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="19a4d-121">Il parametro *ppMedia* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="19a4d-121">The *ppMedia* parameter is not a valid pointer.</span></span><br/>      |
| <dl> <span data-ttu-id="19a4d-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="19a4d-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="19a4d-123">Il parametro di *Indice* non è valido.</span><span class="sxs-lookup"><span data-stu-id="19a4d-123">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="19a4d-124"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="19a4d-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="19a4d-125">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="19a4d-125">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="19a4d-126"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="19a4d-126"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="19a4d-127">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="19a4d-127">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="19a4d-128"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="19a4d-128"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="19a4d-129">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="19a4d-129">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="19a4d-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="19a4d-130">Remarks</span></span>

<span data-ttu-id="19a4d-131">La maggior parte degli elenchi C e C++ sono basati su 0, ma questo indice è basato su 1 per la compatibilità con Visual Basic, ovvero il primo elemento ha un numero di indice pari a 1.</span><span class="sxs-lookup"><span data-stu-id="19a4d-131">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

<span data-ttu-id="19a4d-132">TAPI chiama il metodo **AddRef** sull'interfaccia [**ITmedia**](itmedia.md) restituita da **ITMediaCollection:: create**.</span><span class="sxs-lookup"><span data-stu-id="19a4d-132">TAPI calls the **AddRef** method on the [**ITMedia**](itmedia.md) interface returned by **ITMediaCollection::Create**.</span></span> <span data-ttu-id="19a4d-133">L'applicazione deve chiamare **Release** sull'interfaccia [**ITmedia**](itmedia.md) per liberare risorse associate.</span><span class="sxs-lookup"><span data-stu-id="19a4d-133">The application must call **Release** on the [**ITMedia**](itmedia.md) interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="19a4d-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19a4d-134">Requirements</span></span>



| <span data-ttu-id="19a4d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="19a4d-135">Requirement</span></span> | <span data-ttu-id="19a4d-136">Valore</span><span class="sxs-lookup"><span data-stu-id="19a4d-136">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19a4d-137">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="19a4d-137">TAPI version</span></span><br/> | <span data-ttu-id="19a4d-138">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="19a4d-138">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="19a4d-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19a4d-139">Header</span></span><br/>       | <dl> <span data-ttu-id="19a4d-140"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="19a4d-140"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="19a4d-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="19a4d-141">Library</span></span><br/>      | <dl> <span data-ttu-id="19a4d-142"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19a4d-142"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="19a4d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="19a4d-143">DLL</span></span><br/>          | <dl> <span data-ttu-id="19a4d-144"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19a4d-144"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19a4d-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19a4d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19a4d-146">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="19a4d-146">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="19a4d-147">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="19a4d-147">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




