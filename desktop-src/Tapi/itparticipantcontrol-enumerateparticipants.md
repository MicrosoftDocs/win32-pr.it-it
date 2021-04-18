---
description: Il metodo EnumerateParticipants enumera i partecipanti associati alla conferenza corrente.
ms.assetid: 90a2b5f1-8749-42cd-92d4-f5ee4e680eae
title: 'Metodo ITParticipantControl:: EnumerateParticipants (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54079860a64f366826cda3a0339424148bff1214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324590"
---
# <a name="itparticipantcontrolenumerateparticipants-method"></a><span data-ttu-id="d8598-103">Metodo ITParticipantControl:: EnumerateParticipants</span><span class="sxs-lookup"><span data-stu-id="d8598-103">ITParticipantControl::EnumerateParticipants method</span></span>

<span data-ttu-id="d8598-104">\[**EnumerateParticipants** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d8598-104">\[**EnumerateParticipants** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d8598-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="d8598-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d8598-106">Il metodo **EnumerateParticipants** enumera i partecipanti associati alla conferenza corrente.</span><span class="sxs-lookup"><span data-stu-id="d8598-106">The **EnumerateParticipants** method enumerates participants associated with the current conference.</span></span> <span data-ttu-id="d8598-107">Questo metodo viene fornito per le applicazioni C e C++.</span><span class="sxs-lookup"><span data-stu-id="d8598-107">This method is provided for C and C++ applications.</span></span> <span data-ttu-id="d8598-108">Le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic, devono usare il metodo [**get \_ participates**](itparticipantcontrol-get-participants.md) .</span><span class="sxs-lookup"><span data-stu-id="d8598-108">Automation client applications, such as those written in Visual Basic, must use the [**get\_Participants**](itparticipantcontrol-get-participants.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8598-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8598-109">Syntax</span></span>


```C++
HRESULT EnumerateParticipants(
  [out] IEnumParticipant **ppEnumParticipants
);
```



## <a name="parameters"></a><span data-ttu-id="d8598-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8598-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8598-111">*ppEnumParticipants* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d8598-111">*ppEnumParticipants* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8598-112">Puntatore all'interfaccia [**IEnumParticipant**](ienumparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="d8598-112">Pointer to [**IEnumParticipant**](ienumparticipant.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8598-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8598-113">Return value</span></span>

<span data-ttu-id="d8598-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="d8598-114">This method can return one of these values.</span></span>



| <span data-ttu-id="d8598-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d8598-115">Value</span></span>                                                                                         | <span data-ttu-id="d8598-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d8598-116">Meaning</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="d8598-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d8598-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d8598-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d8598-118">Method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="d8598-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="d8598-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d8598-120">Il parametro *ppEnumParticipants* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="d8598-120">The *ppEnumParticipants* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="d8598-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="d8598-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d8598-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d8598-122">Insufficient memory exists to perform the operation.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="d8598-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8598-123">Remarks</span></span>

<span data-ttu-id="d8598-124">TAPI chiama il metodo **AddRef** sull'interfaccia [**IEnumParticipant**](ienumparticipant.md) restituita da **ITParticipantControl:: EnumerateParticipants**.</span><span class="sxs-lookup"><span data-stu-id="d8598-124">TAPI calls the **AddRef** method on the [**IEnumParticipant**](ienumparticipant.md) interface returned by **ITParticipantControl::EnumerateParticipants**.</span></span> <span data-ttu-id="d8598-125">L'applicazione deve chiamare **Release** sull'interfaccia **IEnumParticipant** per liberare risorse associate.</span><span class="sxs-lookup"><span data-stu-id="d8598-125">The application must call **Release** on the **IEnumParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8598-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8598-126">Requirements</span></span>



| <span data-ttu-id="d8598-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8598-127">Requirement</span></span> | <span data-ttu-id="d8598-128">Valore</span><span class="sxs-lookup"><span data-stu-id="d8598-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8598-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="d8598-129">TAPI version</span></span><br/> | <span data-ttu-id="d8598-130">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d8598-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d8598-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8598-131">Header</span></span><br/>       | <dl> <span data-ttu-id="d8598-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8598-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="d8598-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="d8598-133">Library</span></span><br/>      | <dl> <span data-ttu-id="d8598-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8598-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d8598-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d8598-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="d8598-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8598-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d8598-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8598-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8598-138">**ITParticipantControl**</span><span class="sxs-lookup"><span data-stu-id="d8598-138">**ITParticipantControl**</span></span>](itparticipantcontrol.md)
</dt> <dt>

[<span data-ttu-id="d8598-139">**Ricevi \_ i partecipanti**</span><span class="sxs-lookup"><span data-stu-id="d8598-139">**get\_Participants**</span></span>](itparticipantcontrol-get-participants.md)
</dt> <dt>

[<span data-ttu-id="d8598-140">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="d8598-140">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="d8598-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="d8598-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




