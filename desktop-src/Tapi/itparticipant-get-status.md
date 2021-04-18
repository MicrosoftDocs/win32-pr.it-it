---
description: Il \_ metodo Get Status restituisce un \_ bool Variant che indica lo stato del partecipante.
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: 'Metodo ITParticipant:: get_Status (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de39ac0833f856e35cc120b4f4e5b00bcd617de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327992"
---
# <a name="itparticipantget_status-method"></a><span data-ttu-id="e8cb6-103">Metodo ITParticipant:: Get \_ status</span><span class="sxs-lookup"><span data-stu-id="e8cb6-103">ITParticipant::get\_Status method</span></span>

<span data-ttu-id="e8cb6-104">\[**ottenere \_ Lo stato** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e8cb6-104">\[**get\_Status** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e8cb6-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="e8cb6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e8cb6-106">Il metodo **get \_ status** restituisce un \_ bool Variant che indica lo stato del partecipante.</span><span class="sxs-lookup"><span data-stu-id="e8cb6-106">The **get\_Status** method returns a VARIANT\_BOOL indicating participant status.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8cb6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8cb6-107">Syntax</span></span>


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="e8cb6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8cb6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8cb6-109">*pITStream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8cb6-109">*pITStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8cb6-110">Puntatore all'interfaccia [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .</span><span class="sxs-lookup"><span data-stu-id="e8cb6-110">Pointer to [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e8cb6-111">*pStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e8cb6-111">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8cb6-112">VARIANT \_ true se il partecipante è abilitato nel flusso, VARIANT \_ false se è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="e8cb6-112">VARIANT\_TRUE if the participant is enabled on the stream, VARIANT\_FALSE if it is disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8cb6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8cb6-113">Return value</span></span>

<span data-ttu-id="e8cb6-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="e8cb6-114">This method can return one of these values.</span></span>



| <span data-ttu-id="e8cb6-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e8cb6-115">Return code</span></span>                                                                                   | <span data-ttu-id="e8cb6-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8cb6-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e8cb6-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e8cb6-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e8cb6-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="e8cb6-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="e8cb6-119"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="e8cb6-119"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e8cb6-120">Metodo non implementato.</span><span class="sxs-lookup"><span data-stu-id="e8cb6-120">Method not implemented.</span></span><br/>                                        |
| <dl> <span data-ttu-id="e8cb6-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="e8cb6-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e8cb6-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e8cb6-122">Insufficient memory exists to perform the operation.</span></span><br/>           |
| <dl> <span data-ttu-id="e8cb6-123"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="e8cb6-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e8cb6-124">Il parametro *pITStream* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="e8cb6-124">The *pITStream* parameter is not a valid pointer.</span></span><br/>              |
| <dl> <span data-ttu-id="e8cb6-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e8cb6-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e8cb6-126">Il parametro *pITStream* non punta a un'interfaccia valida.</span><span class="sxs-lookup"><span data-stu-id="e8cb6-126">The *pITStream* parameter does not point to a valid interface.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e8cb6-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8cb6-127">Remarks</span></span>

<span data-ttu-id="e8cb6-128">L'abilitazione o la disabilitazione dello stato di un partecipante in un flusso consente a un'applicazione di disattivare essenzialmente un determinato partecipante.</span><span class="sxs-lookup"><span data-stu-id="e8cb6-128">Enabling or disabling a participant's status on a stream allows an application to essentially mute a given participant.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8cb6-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8cb6-129">Requirements</span></span>



| <span data-ttu-id="e8cb6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8cb6-130">Requirement</span></span> | <span data-ttu-id="e8cb6-131">Valore</span><span class="sxs-lookup"><span data-stu-id="e8cb6-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e8cb6-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="e8cb6-132">TAPI version</span></span><br/> | <span data-ttu-id="e8cb6-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e8cb6-133">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="e8cb6-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8cb6-134">Header</span></span><br/>       | <dl> <span data-ttu-id="e8cb6-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8cb6-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e8cb6-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="e8cb6-136">Library</span></span><br/>      | <dl> <span data-ttu-id="e8cb6-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8cb6-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="e8cb6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e8cb6-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="e8cb6-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8cb6-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8cb6-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8cb6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8cb6-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="e8cb6-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="e8cb6-142">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="e8cb6-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="e8cb6-143">**Inserisci \_ stato**</span><span class="sxs-lookup"><span data-stu-id="e8cb6-143">**put\_Status**</span></span>](itparticipant-put-status.md)
</dt> </dl>

 

