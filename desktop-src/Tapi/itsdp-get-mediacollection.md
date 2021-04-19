---
description: Il \_ metodo Get mediacollection ottiene un puntatore all'interfaccia ITMediaCollection per la conferenza.
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: 'Metodo ITSdp:: get_MediaCollection (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8812debf8c04fe022f24061660d6ea3bb5f162
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326487"
---
# <a name="itsdpget_mediacollection-method"></a><span data-ttu-id="126b4-103">Metodo ITSdp:: Get \_ mediacollection</span><span class="sxs-lookup"><span data-stu-id="126b4-103">ITSdp::get\_MediaCollection method</span></span>

<span data-ttu-id="126b4-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="126b4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="126b4-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="126b4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="126b4-106">Il metodo **get \_ mediacollection** ottiene un puntatore all'interfaccia [**ITMediaCollection**](itmediacollection.md) per la conferenza.</span><span class="sxs-lookup"><span data-stu-id="126b4-106">The **get\_MediaCollection** method gets a pointer to the [**ITMediaCollection**](itmediacollection.md) interface for the conference.</span></span>

## <a name="syntax"></a><span data-ttu-id="126b4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="126b4-107">Syntax</span></span>


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a><span data-ttu-id="126b4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="126b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="126b4-109">*ppMediaCollection* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="126b4-109">*ppMediaCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="126b4-110">Puntatore a [**ITMediaCollection**](itmediacollection.md).</span><span class="sxs-lookup"><span data-stu-id="126b4-110">Pointer to [**ITMediaCollection**](itmediacollection.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="126b4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="126b4-111">Return value</span></span>

<span data-ttu-id="126b4-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="126b4-112">This method can return one of these values.</span></span>



| <span data-ttu-id="126b4-113">Valore</span><span class="sxs-lookup"><span data-stu-id="126b4-113">Value</span></span>                                                                                                                           | <span data-ttu-id="126b4-114">Significato</span><span class="sxs-lookup"><span data-stu-id="126b4-114">Meaning</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="126b4-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="126b4-115"><dt>**S\_OK**</dt></span></span> </dl>                                            | <span data-ttu-id="126b4-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="126b4-116">Method succeeded.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="126b4-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="126b4-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                    | <span data-ttu-id="126b4-118">Il parametro *ppMediaCollection* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="126b4-118">The *ppMediaCollection* parameter is not a valid pointer.</span></span><br/>                        |
| <dl> <span data-ttu-id="126b4-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="126b4-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                   | <span data-ttu-id="126b4-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="126b4-120">Insufficient memory exists to perform the operation.</span></span><br/>                             |
| <dl> <span data-ttu-id="126b4-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="126b4-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                          | <span data-ttu-id="126b4-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="126b4-122">Unspecified error.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="126b4-123"><dt>**HRESULT \_ dal \_ codice di errore \_ (errore di \_ dati non validi \_ )**</dt></span><span class="sxs-lookup"><span data-stu-id="126b4-123"><dt>**HRESULT\_FROM\_ERROR\_CODE(ERROR\_INVALID\_DATA)**</dt></span></span> </dl> | <span data-ttu-id="126b4-124">Si è verificato un errore interno, in genere a causa dell'errore di un metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="126b4-124">An internal error has occurred, usually due to the failure of a previous method.</span></span><br/> |
| <dl> <span data-ttu-id="126b4-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="126b4-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                       | <span data-ttu-id="126b4-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="126b4-126">This method is not yet implemented.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="126b4-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="126b4-127">Remarks</span></span>

<span data-ttu-id="126b4-128">È possibile ottenere un puntatore [**ITMediaCollection**](itmediacollection.md) anche usando **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="126b4-128">An [**ITMediaCollection**](itmediacollection.md) pointer could also be obtained using **QueryInterface**.</span></span>

<span data-ttu-id="126b4-129">TAPI chiama il metodo **AddRef** sull'interfaccia [**ITMediaCollection**](itmediacollection.md) restituita da **ITSdp:: Get \_ mediacollection**.</span><span class="sxs-lookup"><span data-stu-id="126b4-129">TAPI calls the **AddRef** method on the [**ITMediaCollection**](itmediacollection.md) interface returned by **ITSdp::get\_MediaCollection**.</span></span> <span data-ttu-id="126b4-130">L'applicazione deve chiamare **Release** sull'interfaccia **ITMediaCollection** per liberare risorse associate.</span><span class="sxs-lookup"><span data-stu-id="126b4-130">The application must call **Release** on the **ITMediaCollection** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="126b4-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="126b4-131">Requirements</span></span>



| <span data-ttu-id="126b4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="126b4-132">Requirement</span></span> | <span data-ttu-id="126b4-133">Valore</span><span class="sxs-lookup"><span data-stu-id="126b4-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="126b4-134">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="126b4-134">TAPI version</span></span><br/> | <span data-ttu-id="126b4-135">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="126b4-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="126b4-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="126b4-136">Header</span></span><br/>       | <dl> <span data-ttu-id="126b4-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="126b4-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="126b4-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="126b4-138">Library</span></span><br/>      | <dl> <span data-ttu-id="126b4-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="126b4-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="126b4-140">DLL</span><span class="sxs-lookup"><span data-stu-id="126b4-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="126b4-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="126b4-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="126b4-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="126b4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="126b4-143">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="126b4-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="126b4-144">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="126b4-144">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




