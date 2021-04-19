---
description: Il metodo EnumerateStreams enumera i flussi attualmente presenti nei partecipanti. Questo metodo viene fornito per le applicazioni C e C++. Le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic, devono usare il \_ metodo Get Streams.
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: 'Metodo ITParticipant:: EnumerateStreams (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbc92c617ed4baee3ecc33aec65cbdcf50986a27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330258"
---
# <a name="itparticipantenumeratestreams-method"></a><span data-ttu-id="3c223-105">Metodo ITParticipant:: EnumerateStreams</span><span class="sxs-lookup"><span data-stu-id="3c223-105">ITParticipant::EnumerateStreams method</span></span>

<span data-ttu-id="3c223-106">\[**EnumerateStreams** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3c223-106">\[**EnumerateStreams** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3c223-107">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="3c223-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3c223-108">Il metodo **EnumerateStreams** enumera i flussi attualmente presenti nei partecipanti.</span><span class="sxs-lookup"><span data-stu-id="3c223-108">The **EnumerateStreams** method enumerates streams currently with the participants.</span></span> <span data-ttu-id="3c223-109">Questo metodo viene fornito per le applicazioni C e C++.</span><span class="sxs-lookup"><span data-stu-id="3c223-109">This method is provided for C and C++ applications.</span></span> <span data-ttu-id="3c223-110">Le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic, devono usare il metodo [**get \_ Streams**](itparticipant-get-streams.md) .</span><span class="sxs-lookup"><span data-stu-id="3c223-110">Automation client applications, such as those written in Visual Basic, must use the [**get\_Streams**](itparticipant-get-streams.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c223-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c223-111">Syntax</span></span>


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a><span data-ttu-id="3c223-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c223-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c223-113">*ppEnumStream* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3c223-113">*ppEnumStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c223-114">Puntatore al puntatore all'interfaccia [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) .</span><span class="sxs-lookup"><span data-stu-id="3c223-114">Pointer to [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c223-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c223-115">Return value</span></span>

<span data-ttu-id="3c223-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="3c223-116">This method can return one of these values.</span></span>



| <span data-ttu-id="3c223-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3c223-117">Value</span></span>                                                                                     | <span data-ttu-id="3c223-118">Significato</span><span class="sxs-lookup"><span data-stu-id="3c223-118">Meaning</span></span>                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3c223-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3c223-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="3c223-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="3c223-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3c223-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="3c223-121"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="3c223-122">Il parametro *ppEnumStream* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="3c223-122">The *ppEnumStream* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3c223-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c223-123">Remarks</span></span>

<span data-ttu-id="3c223-124">TAPI chiama il metodo **AddRef** sull'interfaccia [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) restituita da **ITParticipant:: EnumerateStreams**.</span><span class="sxs-lookup"><span data-stu-id="3c223-124">TAPI calls the **AddRef** method on the [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) interface returned by **ITParticipant::EnumerateStreams**.</span></span> <span data-ttu-id="3c223-125">L'applicazione deve chiamare **Release** sull'interfaccia **IEnumStream** per liberare risorse associate.</span><span class="sxs-lookup"><span data-stu-id="3c223-125">The application must call **Release** on the **IEnumStream** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c223-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c223-126">Requirements</span></span>



| <span data-ttu-id="3c223-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c223-127">Requirement</span></span> | <span data-ttu-id="3c223-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3c223-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3c223-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="3c223-129">TAPI version</span></span><br/> | <span data-ttu-id="3c223-130">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3c223-130">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="3c223-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c223-131">Header</span></span><br/>       | <dl> <span data-ttu-id="3c223-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c223-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c223-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="3c223-133">Library</span></span><br/>      | <dl> <span data-ttu-id="3c223-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c223-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="3c223-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3c223-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="3c223-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c223-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c223-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c223-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c223-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="3c223-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="3c223-139">**ottenere i \_ flussi**</span><span class="sxs-lookup"><span data-stu-id="3c223-139">**get\_Streams**</span></span>](itparticipant-get-streams.md)
</dt> <dt>

[<span data-ttu-id="3c223-140">**IEnumStream**</span><span class="sxs-lookup"><span data-stu-id="3c223-140">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




