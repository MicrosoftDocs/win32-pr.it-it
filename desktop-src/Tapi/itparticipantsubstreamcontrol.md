---
description: L'interfaccia ITParticipantSubStreamControl viene implementata da IPConf MSP.
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: Interfaccia ITParticipantSubStreamControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 799b1a85c6619e1175e620f2c5c5ef851005ba50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333664"
---
# <a name="itparticipantsubstreamcontrol-interface"></a><span data-ttu-id="cbd3b-103">Interfaccia ITParticipantSubStreamControl</span><span class="sxs-lookup"><span data-stu-id="cbd3b-103">ITParticipantSubStreamControl interface</span></span>

<span data-ttu-id="cbd3b-104">\[**ITParticipantSubStreamControl** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cbd3b-104">\[**ITParticipantSubStreamControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cbd3b-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="cbd3b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cbd3b-106">L'interfaccia **ITParticipantSubStreamControl** viene implementata da IPConf msp.</span><span class="sxs-lookup"><span data-stu-id="cbd3b-106">The **ITParticipantSubStreamControl** interface is implemented by the IPConf MSP.</span></span> <span data-ttu-id="cbd3b-107">Questa interfaccia viene esposta nell'oggetto chiamata.</span><span class="sxs-lookup"><span data-stu-id="cbd3b-107">This interface is exposed on the call object.</span></span> <span data-ttu-id="cbd3b-108">Questa interfaccia fornisce metodi che consentono a un'applicazione di individuare o controllare la corrispondenza del sottoflusso al partecipante.</span><span class="sxs-lookup"><span data-stu-id="cbd3b-108">This interface provides methods that allow an application to either discover or control the matching of substream to participant.</span></span> <span data-ttu-id="cbd3b-109">L'interfaccia **ITParticipantSubStreamControl** viene creata chiamando **QueryInterface** in [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span><span class="sxs-lookup"><span data-stu-id="cbd3b-109">The **ITParticipantSubStreamControl** interface is created by calling **QueryInterface** on [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span></span>

## <a name="members"></a><span data-ttu-id="cbd3b-110">Membri</span><span class="sxs-lookup"><span data-stu-id="cbd3b-110">Members</span></span>

<span data-ttu-id="cbd3b-111">L'interfaccia **ITParticipantSubStreamControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cbd3b-111">The **ITParticipantSubStreamControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cbd3b-112">**ITParticipantSubStreamControl** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cbd3b-112">**ITParticipantSubStreamControl** also has these types of members:</span></span>

-   [<span data-ttu-id="cbd3b-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="cbd3b-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cbd3b-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="cbd3b-114">Methods</span></span>

<span data-ttu-id="cbd3b-115">L'interfaccia **ITParticipantSubStreamControl** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="cbd3b-115">The **ITParticipantSubStreamControl** interface has these methods.</span></span>



| <span data-ttu-id="cbd3b-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="cbd3b-116">Method</span></span>                                                                                              | <span data-ttu-id="cbd3b-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbd3b-117">Description</span></span>                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="cbd3b-118">**ottenere \_ ParticipantFromSubStream**</span><span class="sxs-lookup"><span data-stu-id="cbd3b-118">**get\_ParticipantFromSubStream**</span></span>](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | <span data-ttu-id="cbd3b-119">Ottiene i partecipanti associati a un sottoflusso specificato.</span><span class="sxs-lookup"><span data-stu-id="cbd3b-119">Gets participants associated with a given substream.</span></span><br/> |
| [<span data-ttu-id="cbd3b-120">**ottenere \_ SubStreamFromParticipant**</span><span class="sxs-lookup"><span data-stu-id="cbd3b-120">**get\_SubStreamFromParticipant**</span></span>](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | <span data-ttu-id="cbd3b-121">Ottiene i flussi sottoflussi associati a un determinato partecipante.</span><span class="sxs-lookup"><span data-stu-id="cbd3b-121">Gets substreams associated with a given participant.</span></span><br/> |
| [<span data-ttu-id="cbd3b-122">**SwitchTerminalToSubStream**</span><span class="sxs-lookup"><span data-stu-id="cbd3b-122">**SwitchTerminalToSubStream**</span></span>](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | <span data-ttu-id="cbd3b-123">Imposta un partecipante a un sottoflusso.</span><span class="sxs-lookup"><span data-stu-id="cbd3b-123">Sets a participant on a substream.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="cbd3b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbd3b-124">Requirements</span></span>



| <span data-ttu-id="cbd3b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbd3b-125">Requirement</span></span> | <span data-ttu-id="cbd3b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="cbd3b-126">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd3b-127">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="cbd3b-127">TAPI version</span></span><br/> | <span data-ttu-id="cbd3b-128">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="cbd3b-128">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="cbd3b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cbd3b-129">Header</span></span><br/>       | <dl> <span data-ttu-id="cbd3b-130"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbd3b-130"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="cbd3b-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="cbd3b-131">Library</span></span><br/>      | <dl> <span data-ttu-id="cbd3b-132"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cbd3b-132"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cbd3b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cbd3b-133">DLL</span></span><br/>          | <dl> <span data-ttu-id="cbd3b-134"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbd3b-134"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="cbd3b-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbd3b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd3b-136">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="cbd3b-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="cbd3b-137">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="cbd3b-137">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

