---
description: Il \_ metodo Get TimeCollection ottiene un puntatore a un'interfaccia ITTimeCollection per Conference.
ms.assetid: 1cfe3f5a-dcf7-480b-9b23-e17259d8ee9c
title: 'Metodo ITSdp:: get_TimeCollection (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1bac0f38f8c96762d4e36d8d3dfdff2136bdb86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330365"
---
# <a name="itsdpget_timecollection-method"></a><span data-ttu-id="ed946-103">Metodo ITSdp:: Get \_ TimeCollection</span><span class="sxs-lookup"><span data-stu-id="ed946-103">ITSdp::get\_TimeCollection method</span></span>

<span data-ttu-id="ed946-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ed946-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ed946-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="ed946-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ed946-106">Il metodo **get \_ TimeCollection** ottiene un puntatore a un'interfaccia [**ITTimeCollection**](ittimecollection.md) per Conference.</span><span class="sxs-lookup"><span data-stu-id="ed946-106">The **get\_TimeCollection** method gets a pointer to an [**ITTimeCollection**](ittimecollection.md) interface for conference.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed946-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed946-107">Syntax</span></span>


```C++
HRESULT get_TimeCollection(
  [out] ITTimeCollection **ppTimeCollection
);
```



## <a name="parameters"></a><span data-ttu-id="ed946-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed946-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed946-109">*ppTimeCollection* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ed946-109">*ppTimeCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed946-110">Puntatore a [**ITTimeCollection**](ittimecollection.md).</span><span class="sxs-lookup"><span data-stu-id="ed946-110">Pointer to [**ITTimeCollection**](ittimecollection.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed946-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed946-111">Return value</span></span>

<span data-ttu-id="ed946-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="ed946-112">This method can return one of these values.</span></span>



| <span data-ttu-id="ed946-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ed946-113">Value</span></span>                                                                                                                           | <span data-ttu-id="ed946-114">Significato</span><span class="sxs-lookup"><span data-stu-id="ed946-114">Meaning</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ed946-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ed946-115"><dt>**S\_OK**</dt></span></span> </dl>                                            | <span data-ttu-id="ed946-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="ed946-116">Method succeeded.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="ed946-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ed946-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                    | <span data-ttu-id="ed946-118">Il parametro *ppTimeCollection* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="ed946-118">The *ppTimeCollection* parameter is not a valid pointer.</span></span><br/>                         |
| <dl> <span data-ttu-id="ed946-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="ed946-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                   | <span data-ttu-id="ed946-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ed946-120">Insufficient memory exists to perform the operation.</span></span><br/>                             |
| <dl> <span data-ttu-id="ed946-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="ed946-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                          | <span data-ttu-id="ed946-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ed946-122">Unspecified error.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="ed946-123"><dt>**HRESULT \_ dal \_ codice di errore \_ (errore di \_ dati non validi \_ )**</dt></span><span class="sxs-lookup"><span data-stu-id="ed946-123"><dt>**HRESULT\_FROM\_ERROR\_CODE(ERROR\_INVALID\_DATA)**</dt></span></span> </dl> | <span data-ttu-id="ed946-124">Si è verificato un errore interno, in genere a causa dell'errore di un metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="ed946-124">An internal error has occurred, usually due to the failure of a previous method.</span></span><br/> |
| <dl> <span data-ttu-id="ed946-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="ed946-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                       | <span data-ttu-id="ed946-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="ed946-126">This method is not yet implemented.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="ed946-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed946-127">Remarks</span></span>

<span data-ttu-id="ed946-128">È possibile ottenere un puntatore [**ITTimeCollection**](ittimecollection.md) anche usando **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="ed946-128">An [**ITTimeCollection**](ittimecollection.md) pointer could also be obtained using **QueryInterface**.</span></span>

<span data-ttu-id="ed946-129">TAPI chiama il metodo **AddRef** sull'interfaccia [**ITTimeCollection**](ittimecollection.md) restituita da **ITSdp:: Get \_ TimeCollection**.</span><span class="sxs-lookup"><span data-stu-id="ed946-129">TAPI calls the **AddRef** method on the [**ITTimeCollection**](ittimecollection.md) interface returned by **ITSdp::get\_TimeCollection**.</span></span> <span data-ttu-id="ed946-130">L'applicazione deve chiamare **Release** sull'interfaccia **ITTimeCollection** per liberare risorse associate.</span><span class="sxs-lookup"><span data-stu-id="ed946-130">The application must call **Release** on the **ITTimeCollection** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed946-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed946-131">Requirements</span></span>



| <span data-ttu-id="ed946-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed946-132">Requirement</span></span> | <span data-ttu-id="ed946-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ed946-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed946-134">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="ed946-134">TAPI version</span></span><br/> | <span data-ttu-id="ed946-135">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ed946-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ed946-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed946-136">Header</span></span><br/>       | <dl> <span data-ttu-id="ed946-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed946-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed946-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="ed946-138">Library</span></span><br/>      | <dl> <span data-ttu-id="ed946-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed946-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ed946-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ed946-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="ed946-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed946-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed946-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed946-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed946-143">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="ed946-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="ed946-144">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="ed946-144">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> </dl>

 

 




