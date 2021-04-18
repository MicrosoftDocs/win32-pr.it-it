---
description: Il \_ metodo Get participates crea una raccolta di partecipanti associati alla conferenza corrente.
ms.assetid: 643acc3f-3df1-4f3a-a8fe-5d46864f8cf7
title: 'Metodo ITParticipantControl:: get_Participants (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4a99e0efe7702a3358684b00af5e8faa96461c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327308"
---
# <a name="itparticipantcontrolget_participants-method"></a><span data-ttu-id="2f8cd-103">Metodo ITParticipantControl:: Get \_ participates</span><span class="sxs-lookup"><span data-stu-id="2f8cd-103">ITParticipantControl::get\_Participants method</span></span>

<span data-ttu-id="2f8cd-104">\[**ottenere \_ I partecipanti** non sono disponibili per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2f8cd-104">\[**get\_Participants** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2f8cd-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="2f8cd-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2f8cd-106">Il metodo **get \_ participates** crea una raccolta di partecipanti associati alla conferenza corrente.</span><span class="sxs-lookup"><span data-stu-id="2f8cd-106">The **get\_Participants** method creates a collection of participants associated with the current conference.</span></span> <span data-ttu-id="2f8cd-107">Questo metodo viene fornito per le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2f8cd-107">This method is provided for Automation client applications, such as those written in Visual Basic.</span></span> <span data-ttu-id="2f8cd-108">Le applicazioni C e C++ devono usare il metodo [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) .</span><span class="sxs-lookup"><span data-stu-id="2f8cd-108">C and C++ applications must use the [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f8cd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f8cd-109">Syntax</span></span>


```C++
HRESULT get_Participants(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a><span data-ttu-id="2f8cd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f8cd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f8cd-111">*pVariant* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2f8cd-111">*pVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f8cd-112">Puntatore a **Variant** contenente un [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) di puntatori dell'interfaccia [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="2f8cd-112">Pointer to **VARIANT** containing an [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f8cd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f8cd-113">Return value</span></span>

<span data-ttu-id="2f8cd-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="2f8cd-114">This method can return one of these values.</span></span>



| <span data-ttu-id="2f8cd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2f8cd-115">Value</span></span>                                                                                         | <span data-ttu-id="2f8cd-116">Significato</span><span class="sxs-lookup"><span data-stu-id="2f8cd-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2f8cd-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2f8cd-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2f8cd-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="2f8cd-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2f8cd-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="2f8cd-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2f8cd-120">Il parametro *pVariant* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="2f8cd-120">The *pVariant* parameter is not a valid pointer.</span></span><br/>     |
| <dl> <span data-ttu-id="2f8cd-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="2f8cd-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2f8cd-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="2f8cd-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f8cd-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f8cd-123">Remarks</span></span>

<span data-ttu-id="2f8cd-124">TAPI chiama il metodo **AddRef** sull'interfaccia [**ITParticipant**](itparticipant.md) restituita da **ITParticipantControl:: Get \_ participates**.</span><span class="sxs-lookup"><span data-stu-id="2f8cd-124">TAPI calls the **AddRef** method on the [**ITParticipant**](itparticipant.md) interface returned by **ITParticipantControl::get\_Participants**.</span></span> <span data-ttu-id="2f8cd-125">L'applicazione deve chiamare **Release** sull'interfaccia **ITParticipant** per liberare risorse associate.</span><span class="sxs-lookup"><span data-stu-id="2f8cd-125">The application must call **Release** on the **ITParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f8cd-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f8cd-126">Requirements</span></span>



| <span data-ttu-id="2f8cd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f8cd-127">Requirement</span></span> | <span data-ttu-id="2f8cd-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2f8cd-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f8cd-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="2f8cd-129">TAPI version</span></span><br/> | <span data-ttu-id="2f8cd-130">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2f8cd-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2f8cd-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f8cd-131">Header</span></span><br/>       | <dl> <span data-ttu-id="2f8cd-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f8cd-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="2f8cd-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="2f8cd-133">Library</span></span><br/>      | <dl> <span data-ttu-id="2f8cd-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f8cd-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2f8cd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2f8cd-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="2f8cd-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f8cd-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2f8cd-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f8cd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f8cd-138">**ITParticipantControl**</span><span class="sxs-lookup"><span data-stu-id="2f8cd-138">**ITParticipantControl**</span></span>](itparticipantcontrol.md)
</dt> <dt>

[<span data-ttu-id="2f8cd-139">**EnumerateParticipants**</span><span class="sxs-lookup"><span data-stu-id="2f8cd-139">**EnumerateParticipants**</span></span>](itparticipantcontrol-enumerateparticipants.md)
</dt> <dt>

[<span data-ttu-id="2f8cd-140">**ITCollection**</span><span class="sxs-lookup"><span data-stu-id="2f8cd-140">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[<span data-ttu-id="2f8cd-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="2f8cd-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




