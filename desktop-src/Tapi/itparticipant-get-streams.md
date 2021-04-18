---
description: Il \_ metodo Get Streams crea una raccolta di flussi associati al partecipante corrente.
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: 'Metodo ITParticipant:: get_Streams (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a920929c71e01632edcd8c4c78029b479d8b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327991"
---
# <a name="itparticipantget_streams-method"></a><span data-ttu-id="08a43-103">Metodo ITParticipant:: Get \_ Streams</span><span class="sxs-lookup"><span data-stu-id="08a43-103">ITParticipant::get\_Streams method</span></span>

<span data-ttu-id="08a43-104">\[**ottenere \_ I flussi** non sono disponibili per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="08a43-104">\[**get\_Streams** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="08a43-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="08a43-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="08a43-106">Il metodo **get \_ Streams** crea una raccolta di flussi associati al partecipante corrente.</span><span class="sxs-lookup"><span data-stu-id="08a43-106">The **get\_Streams** method creates a collection of streams associated with the current participant.</span></span> <span data-ttu-id="08a43-107">Questo metodo viene fornito per le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="08a43-107">This method is provided for Automation client applications, such as those written in Visual Basic.</span></span> <span data-ttu-id="08a43-108">Le applicazioni C e C++ devono usare il metodo [**EnumerateStreams**](itparticipant-enumeratestreams.md) .</span><span class="sxs-lookup"><span data-stu-id="08a43-108">C and C++ applications must use the [**EnumerateStreams**](itparticipant-enumeratestreams.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="08a43-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08a43-109">Syntax</span></span>


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a><span data-ttu-id="08a43-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="08a43-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08a43-111">*pVariant* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="08a43-111">*pVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08a43-112">Puntatore a **Variant** contenente un [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) di puntatori dell'interfaccia [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .</span><span class="sxs-lookup"><span data-stu-id="08a43-112">Pointer to **VARIANT** containing an [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) of [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08a43-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08a43-113">Return value</span></span>

<span data-ttu-id="08a43-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="08a43-114">This method can return one of these values.</span></span>



| <span data-ttu-id="08a43-115">Valore</span><span class="sxs-lookup"><span data-stu-id="08a43-115">Value</span></span>                                                                                         | <span data-ttu-id="08a43-116">Significato</span><span class="sxs-lookup"><span data-stu-id="08a43-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="08a43-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="08a43-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="08a43-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="08a43-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="08a43-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="08a43-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="08a43-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="08a43-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="08a43-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="08a43-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="08a43-122">Il parametro *pVariant* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="08a43-122">The *pVariant* parameter is not a valid pointer.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="08a43-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="08a43-123">Remarks</span></span>

<span data-ttu-id="08a43-124">TAPI chiama il metodo **AddRef** sull'interfaccia [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) restituita dai **\_ flussi ITParticipant:: Get**.</span><span class="sxs-lookup"><span data-stu-id="08a43-124">TAPI calls the **AddRef** method on the [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface returned by **ITParticipant::get\_Streams**.</span></span> <span data-ttu-id="08a43-125">L'applicazione deve chiamare **Release** sull'interfaccia **ITStream** per liberare risorse associate.</span><span class="sxs-lookup"><span data-stu-id="08a43-125">The application must call **Release** on the **ITStream** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="08a43-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08a43-126">Requirements</span></span>



| <span data-ttu-id="08a43-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="08a43-127">Requirement</span></span> | <span data-ttu-id="08a43-128">Valore</span><span class="sxs-lookup"><span data-stu-id="08a43-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="08a43-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="08a43-129">TAPI version</span></span><br/> | <span data-ttu-id="08a43-130">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="08a43-130">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="08a43-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08a43-131">Header</span></span><br/>       | <dl> <span data-ttu-id="08a43-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="08a43-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="08a43-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="08a43-133">Library</span></span><br/>      | <dl> <span data-ttu-id="08a43-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08a43-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="08a43-135">DLL</span><span class="sxs-lookup"><span data-stu-id="08a43-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="08a43-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08a43-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08a43-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08a43-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a43-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="08a43-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="08a43-139">**EnumerateStreams**</span><span class="sxs-lookup"><span data-stu-id="08a43-139">**EnumerateStreams**</span></span>](itparticipant-enumeratestreams.md)
</dt> <dt>

[<span data-ttu-id="08a43-140">**IEnumStream**</span><span class="sxs-lookup"><span data-stu-id="08a43-140">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[<span data-ttu-id="08a43-141">**ITCollection**</span><span class="sxs-lookup"><span data-stu-id="08a43-141">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[<span data-ttu-id="08a43-142">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="08a43-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

