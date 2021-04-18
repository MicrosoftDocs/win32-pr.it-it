---
description: Il metodo SwitchTerminalToSubStream imposta un terminale sul sottoflusso del partecipante.
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: 'Metodo ITParticipantSubStreamControl:: SwitchTerminalToSubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f10401b2cf1598c76537ebd3a7049d67bf0657
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333665"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a><span data-ttu-id="f1edc-103">Metodo ITParticipantSubStreamControl:: SwitchTerminalToSubStream</span><span class="sxs-lookup"><span data-stu-id="f1edc-103">ITParticipantSubStreamControl::SwitchTerminalToSubStream method</span></span>

<span data-ttu-id="f1edc-104">\[**SwitchTerminalToSubStream** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f1edc-104">\[**SwitchTerminalToSubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f1edc-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="f1edc-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f1edc-106">Il metodo **SwitchTerminalToSubStream** imposta un terminale sul sottoflusso del partecipante.</span><span class="sxs-lookup"><span data-stu-id="f1edc-106">The **SwitchTerminalToSubStream** method sets a terminal to the participant substream.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1edc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1edc-107">Syntax</span></span>


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="f1edc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1edc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1edc-109">*pITTerminal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1edc-109">*pITTerminal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1edc-110">Puntatore all'interfaccia [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .</span><span class="sxs-lookup"><span data-stu-id="f1edc-110">Pointer to [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface.</span></span>

</dd> <dt>

<span data-ttu-id="f1edc-111">*pITSubStream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1edc-111">*pITSubStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1edc-112">Puntatore all'interfaccia [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .</span><span class="sxs-lookup"><span data-stu-id="f1edc-112">Pointer to [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1edc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1edc-113">Return value</span></span>

<span data-ttu-id="f1edc-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="f1edc-114">This method can return one of these values.</span></span>



| <span data-ttu-id="f1edc-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f1edc-115">Return code</span></span>                                                                                     | <span data-ttu-id="f1edc-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1edc-116">Description</span></span>                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1edc-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f1edc-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="f1edc-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f1edc-118">Method succeeded.</span></span><br/>                                                                       |
| <dl> <span data-ttu-id="f1edc-119"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="f1edc-119"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>    | <span data-ttu-id="f1edc-120">Non è possibile accedere alle informazioni del partecipante per il flusso.</span><span class="sxs-lookup"><span data-stu-id="f1edc-120">Participant information for the stream could not be accessed.</span></span><br/>                           |
| <dl> <span data-ttu-id="f1edc-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f1edc-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>    | <span data-ttu-id="f1edc-122">Il *pParticipant* o il parametro *pITSubStream* non punta a un'interfaccia valida.</span><span class="sxs-lookup"><span data-stu-id="f1edc-122">The *pParticipant* or the *pITSubStream* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="f1edc-123"><dt>**TAPI \_ E \_ noitems**</dt></span><span class="sxs-lookup"><span data-stu-id="f1edc-123"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="f1edc-124">Il sottoflusso non è pronto.</span><span class="sxs-lookup"><span data-stu-id="f1edc-124">The substream is not ready.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="f1edc-125"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="f1edc-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="f1edc-126">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f1edc-126">Insufficient memory exists to perform the operation.</span></span><br/>                                    |



 

## <a name="requirements"></a><span data-ttu-id="f1edc-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1edc-127">Requirements</span></span>



| <span data-ttu-id="f1edc-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1edc-128">Requirement</span></span> | <span data-ttu-id="f1edc-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f1edc-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1edc-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f1edc-130">TAPI version</span></span><br/> | <span data-ttu-id="f1edc-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f1edc-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f1edc-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1edc-132">Header</span></span><br/>       | <dl> <span data-ttu-id="f1edc-133"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1edc-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="f1edc-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="f1edc-134">Library</span></span><br/>      | <dl> <span data-ttu-id="f1edc-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1edc-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f1edc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f1edc-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="f1edc-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1edc-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f1edc-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1edc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1edc-139">**ITParticipantSubStreamControl**</span><span class="sxs-lookup"><span data-stu-id="f1edc-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="f1edc-140">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="f1edc-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="f1edc-141">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="f1edc-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[<span data-ttu-id="f1edc-142">**ITTerminal**</span><span class="sxs-lookup"><span data-stu-id="f1edc-142">**ITTerminal**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> </dl>

 

