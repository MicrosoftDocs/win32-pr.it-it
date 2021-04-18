---
description: Il \_ metodo Put status imposta lo stato di un partecipante.
ms.assetid: 8478fcf4-00b3-4b77-9859-e5a80ce24be1
title: 'ITParticipant: metodo:p ut_Status (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eadc9832105ecb0cf440b070dbff8b3fe658d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327988"
---
# <a name="itparticipantput_status-method"></a><span data-ttu-id="21087-103">ITParticipant: metodo di \_ stato ut:p</span><span class="sxs-lookup"><span data-stu-id="21087-103">ITParticipant::put\_Status method</span></span>

<span data-ttu-id="21087-104">\[**Inserisci \_ Lo stato** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="21087-104">\[**put\_Status** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="21087-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="21087-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="21087-106">Il metodo **put \_ status** imposta lo stato di un partecipante.</span><span class="sxs-lookup"><span data-stu-id="21087-106">The **put\_Status** method sets the status of a participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="21087-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21087-107">Syntax</span></span>


```C++
HRESULT put_Status(
  [in] ITStream     *pITStream,
  [in] VARIANT_BOOL fEnable
);
```



## <a name="parameters"></a><span data-ttu-id="21087-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="21087-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21087-109">*pITStream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21087-109">*pITStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21087-110">Puntatore all'interfaccia [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .</span><span class="sxs-lookup"><span data-stu-id="21087-110">Pointer to [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="21087-111">*fEnable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21087-111">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21087-112">VARIANT \_ true se il partecipante è abilitato nel flusso, VARIANT \_ false se deve essere disabilitato.</span><span class="sxs-lookup"><span data-stu-id="21087-112">VARIANT\_TRUE if the participant is enabled on the stream, VARIANT\_FALSE if it is to be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21087-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21087-113">Return value</span></span>

<span data-ttu-id="21087-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="21087-114">This method can return one of these values.</span></span>



| <span data-ttu-id="21087-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="21087-115">Return code</span></span>                                                                                   | <span data-ttu-id="21087-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21087-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="21087-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="21087-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="21087-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="21087-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="21087-119"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="21087-119"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="21087-120">Metodo non implementato.</span><span class="sxs-lookup"><span data-stu-id="21087-120">Method not implemented.</span></span><br/>                                        |
| <dl> <span data-ttu-id="21087-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="21087-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="21087-122">Il parametro *pITStream* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="21087-122">The *pITStream* parameter is not a valid pointer.</span></span><br/>              |
| <dl> <span data-ttu-id="21087-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="21087-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="21087-124">Il parametro *pITStream* non punta a un'interfaccia valida.</span><span class="sxs-lookup"><span data-stu-id="21087-124">The *pITStream* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="21087-125"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="21087-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="21087-126">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="21087-126">Insufficient memory exists to perform the operation.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="21087-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="21087-127">Remarks</span></span>

<span data-ttu-id="21087-128">L'abilitazione o la disabilitazione dello stato di un partecipante in un flusso consente a un'applicazione di disattivare essenzialmente un determinato partecipante.</span><span class="sxs-lookup"><span data-stu-id="21087-128">Enabling or disabling a participant's status on a stream allows an application to essentially mute a given participant.</span></span>

## <a name="requirements"></a><span data-ttu-id="21087-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21087-129">Requirements</span></span>



| <span data-ttu-id="21087-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="21087-130">Requirement</span></span> | <span data-ttu-id="21087-131">Valore</span><span class="sxs-lookup"><span data-stu-id="21087-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="21087-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="21087-132">TAPI version</span></span><br/> | <span data-ttu-id="21087-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="21087-133">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="21087-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21087-134">Header</span></span><br/>       | <dl> <span data-ttu-id="21087-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="21087-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="21087-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="21087-136">Library</span></span><br/>      | <dl> <span data-ttu-id="21087-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21087-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="21087-138">DLL</span><span class="sxs-lookup"><span data-stu-id="21087-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="21087-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21087-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21087-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21087-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21087-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="21087-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="21087-142">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="21087-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="21087-143">**ottenere \_ lo stato**</span><span class="sxs-lookup"><span data-stu-id="21087-143">**get\_Status**</span></span>](itparticipant-get-status.md)
</dt> </dl>

 

