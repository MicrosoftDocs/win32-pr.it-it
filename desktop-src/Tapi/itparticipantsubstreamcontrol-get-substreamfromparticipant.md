---
description: Il \_ metodo Get SubStreamFromParticipant consente a un'applicazione di individuare i flussi sottoflussi associati a un determinato partecipante.
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: 'Metodo ITParticipantSubStreamControl:: get_SubStreamFromParticipant (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0eae68cd62c38348e1a576f114a9e93ac52f9cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333667"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a><span data-ttu-id="b5d80-103">Metodo ITParticipantSubStreamControl:: Get \_ SubStreamFromParticipant</span><span class="sxs-lookup"><span data-stu-id="b5d80-103">ITParticipantSubStreamControl::get\_SubStreamFromParticipant method</span></span>

<span data-ttu-id="b5d80-104">\[**ottenere \_ SubStreamFromParticipant** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b5d80-104">\[**get\_SubStreamFromParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b5d80-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="b5d80-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b5d80-106">Il metodo **get \_ SubStreamFromParticipant** consente a un'applicazione di individuare i flussi sottoflussi associati a un determinato partecipante.</span><span class="sxs-lookup"><span data-stu-id="b5d80-106">The **get\_SubStreamFromParticipant** method allows an application to discover which substreams are associated with a given participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d80-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5d80-107">Syntax</span></span>


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="b5d80-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5d80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5d80-109">*pParticipant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5d80-109">*pParticipant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d80-110">Puntatore all'interfaccia [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="b5d80-110">Pointer to [**ITParticipant**](itparticipant.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="b5d80-111">*ppITSubStream* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5d80-111">*ppITSubStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d80-112">Puntatore alla matrice di puntatori dell'interfaccia [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="b5d80-112">Pointer to array of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5d80-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5d80-113">Return value</span></span>

<span data-ttu-id="b5d80-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="b5d80-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b5d80-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b5d80-115">Return code</span></span>                                                                                   | <span data-ttu-id="b5d80-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5d80-116">Description</span></span>                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5d80-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b5d80-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b5d80-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="b5d80-118">Method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="b5d80-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="b5d80-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b5d80-120">Il parametro *ppITSubStream* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="b5d80-120">The *ppITSubStream* parameter is not a valid pointer.</span></span><br/>             |
| <dl> <span data-ttu-id="b5d80-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b5d80-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b5d80-122">Il parametro *pParticipant* non punta a un'interfaccia valida.</span><span class="sxs-lookup"><span data-stu-id="b5d80-122">The *pParticipant* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="b5d80-123"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="b5d80-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="b5d80-124">Non è possibile accedere alle informazioni del partecipante del flusso.</span><span class="sxs-lookup"><span data-stu-id="b5d80-124">The stream's participant information could not be accessed.</span></span><br/>       |
| <dl> <span data-ttu-id="b5d80-125"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="b5d80-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b5d80-126">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b5d80-126">Insufficient memory exists to perform the operation.</span></span><br/>              |



 

## <a name="requirements"></a><span data-ttu-id="b5d80-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5d80-127">Requirements</span></span>



| <span data-ttu-id="b5d80-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5d80-128">Requirement</span></span> | <span data-ttu-id="b5d80-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b5d80-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d80-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="b5d80-130">TAPI version</span></span><br/> | <span data-ttu-id="b5d80-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b5d80-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b5d80-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5d80-132">Header</span></span><br/>       | <dl> <span data-ttu-id="b5d80-133"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5d80-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="b5d80-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5d80-134">Library</span></span><br/>      | <dl> <span data-ttu-id="b5d80-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5d80-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b5d80-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b5d80-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="b5d80-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5d80-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b5d80-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5d80-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d80-139">**ITParticipantSubStreamControl**</span><span class="sxs-lookup"><span data-stu-id="b5d80-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="b5d80-140">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="b5d80-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="b5d80-141">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="b5d80-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

