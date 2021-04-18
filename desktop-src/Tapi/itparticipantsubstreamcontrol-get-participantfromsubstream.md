---
description: Il \_ metodo Get ParticipantFromSubStream consente a un'applicazione di individuare i partecipanti associati a un determinato flusso di dati.
ms.assetid: 0e42b4f0-d5b6-4b33-b7e5-dc525524ece7
title: 'Metodo ITParticipantSubStreamControl:: get_ParticipantFromSubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a507665e7f81339ce10961d69e08e76f60bb2be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330468"
---
# <a name="itparticipantsubstreamcontrolget_participantfromsubstream-method"></a><span data-ttu-id="77b03-103">Metodo ITParticipantSubStreamControl:: Get \_ ParticipantFromSubStream</span><span class="sxs-lookup"><span data-stu-id="77b03-103">ITParticipantSubStreamControl::get\_ParticipantFromSubStream method</span></span>

<span data-ttu-id="77b03-104">\[**ottenere \_ ParticipantFromSubStream** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="77b03-104">\[**get\_ParticipantFromSubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="77b03-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="77b03-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="77b03-106">Il metodo **get \_ ParticipantFromSubStream** consente a un'applicazione di individuare i partecipanti associati a un determinato flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="77b03-106">The **get\_ParticipantFromSubStream** method allows an application to discover which participants are associated with a given substream.</span></span>

## <a name="syntax"></a><span data-ttu-id="77b03-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77b03-107">Syntax</span></span>


```C++
HRESULT get_ParticipantFromSubStream(
  [in]  ITSubStream   *pITSubStream,
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a><span data-ttu-id="77b03-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="77b03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77b03-109">*pITSubStream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77b03-109">*pITSubStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77b03-110">Puntatore all'interfaccia [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .</span><span class="sxs-lookup"><span data-stu-id="77b03-110">Pointer to [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="77b03-111">*ppParticipant* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="77b03-111">*ppParticipant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77b03-112">Puntatore alla matrice di puntatori dell'interfaccia [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="77b03-112">Pointer to array of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77b03-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="77b03-113">Return value</span></span>

<span data-ttu-id="77b03-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="77b03-114">This method can return one of these values.</span></span>



| <span data-ttu-id="77b03-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="77b03-115">Return code</span></span>                                                                                     | <span data-ttu-id="77b03-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77b03-116">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="77b03-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="77b03-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="77b03-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="77b03-118">Method succeeded.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="77b03-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="77b03-119"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="77b03-120">Il parametro *pITSubStream* o *ppParticipant* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="77b03-120">The *pITSubStream* or *ppParticipant* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="77b03-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="77b03-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>    | <span data-ttu-id="77b03-122">Il parametro *pITSubStream* non punta a un'interfaccia valida.</span><span class="sxs-lookup"><span data-stu-id="77b03-122">The *pITSubStream* parameter does not point to valid interface.</span></span><br/>         |
| <dl> <span data-ttu-id="77b03-123"><dt>**TAPI \_ E \_ noitems**</dt></span><span class="sxs-lookup"><span data-stu-id="77b03-123"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="77b03-124">Nessun partecipante associato al sottoflusso.</span><span class="sxs-lookup"><span data-stu-id="77b03-124">There are no participants associated with the substream.</span></span><br/>                |
| <dl> <span data-ttu-id="77b03-125"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="77b03-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="77b03-126">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="77b03-126">Insufficient memory exists to perform the operation.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="77b03-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77b03-127">Requirements</span></span>



| <span data-ttu-id="77b03-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="77b03-128">Requirement</span></span> | <span data-ttu-id="77b03-129">Valore</span><span class="sxs-lookup"><span data-stu-id="77b03-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77b03-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="77b03-130">TAPI version</span></span><br/> | <span data-ttu-id="77b03-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="77b03-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="77b03-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77b03-132">Header</span></span><br/>       | <dl> <span data-ttu-id="77b03-133"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="77b03-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="77b03-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="77b03-134">Library</span></span><br/>      | <dl> <span data-ttu-id="77b03-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77b03-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="77b03-136">DLL</span><span class="sxs-lookup"><span data-stu-id="77b03-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="77b03-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77b03-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="77b03-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77b03-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77b03-139">**ITParticipantSubStreamControl**</span><span class="sxs-lookup"><span data-stu-id="77b03-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="77b03-140">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="77b03-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="77b03-141">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="77b03-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

