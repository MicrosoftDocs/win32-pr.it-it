---
description: L'interfaccia ITParticipant viene implementata da IPConf MSP. Consente a un'applicazione di recuperare informazioni sui partecipanti alla conferenza e ottenere i puntatori ai flussi associati a tali partecipanti.
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: Interfaccia ITParticipant (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b7aa9d845d8d2489be0850bcc3fcf3f93ccdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331046"
---
# <a name="itparticipant-interface"></a><span data-ttu-id="e9100-104">Interfaccia ITParticipant</span><span class="sxs-lookup"><span data-stu-id="e9100-104">ITParticipant interface</span></span>

<span data-ttu-id="e9100-105">\[**ITParticipant** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e9100-105">\[**ITParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e9100-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="e9100-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e9100-107">L'interfaccia **ITParticipant** viene implementata da [IPConf msp](ipconf-msp.md).</span><span class="sxs-lookup"><span data-stu-id="e9100-107">The **ITParticipant** interface is implemented by the [IPConf MSP](ipconf-msp.md).</span></span> <span data-ttu-id="e9100-108">Consente a un'applicazione di recuperare informazioni sui partecipanti alla conferenza e ottenere i puntatori ai flussi associati a tali partecipanti.</span><span class="sxs-lookup"><span data-stu-id="e9100-108">It allows an application to retrieve information on conference participants, and get pointers to the streams associated with those participants.</span></span>

<span data-ttu-id="e9100-109">Questa interfaccia viene esposta nell'oggetto chiamata quando una chiamata utilizza la conferenza IP.</span><span class="sxs-lookup"><span data-stu-id="e9100-109">This interface is exposed on the call object when a call uses the IP Conferencing.</span></span> <span data-ttu-id="e9100-110">È possibile ottenere un puntatore chiamando **QueryInterface** utilizzando un puntatore [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="e9100-110">A pointer can be obtained by calling **QueryInterface** using an [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) pointer.</span></span>

## <a name="members"></a><span data-ttu-id="e9100-111">Membri</span><span class="sxs-lookup"><span data-stu-id="e9100-111">Members</span></span>

<span data-ttu-id="e9100-112">L'interfaccia **ITParticipant** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e9100-112">The **ITParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e9100-113">**ITParticipant** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e9100-113">**ITParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="e9100-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="e9100-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e9100-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="e9100-115">Methods</span></span>

<span data-ttu-id="e9100-116">L'interfaccia **ITParticipant** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e9100-116">The **ITParticipant** interface has these methods.</span></span>



| <span data-ttu-id="e9100-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="e9100-117">Method</span></span>                                                                      | <span data-ttu-id="e9100-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9100-118">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9100-119">**EnumerateStreams**</span><span class="sxs-lookup"><span data-stu-id="e9100-119">**EnumerateStreams**</span></span>](itparticipant-enumeratestreams.md)                  | <span data-ttu-id="e9100-120">Enumera i flussi associati al partecipante corrente.</span><span class="sxs-lookup"><span data-stu-id="e9100-120">Enumerates streams associated with the current participant.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="e9100-121">**ottenere \_ MediaTypes**</span><span class="sxs-lookup"><span data-stu-id="e9100-121">**get\_MediaTypes**</span></span>](itparticipant-get-mediatypes.md)                     | <span data-ttu-id="e9100-122">Ottiene i [**tipi di supporto**](tapimediatype--constants.md) associati a un partecipante.</span><span class="sxs-lookup"><span data-stu-id="e9100-122">Gets the [**media types**](tapimediatype--constants.md) associated with a participant.</span></span><br/>                                                                      |
| [<span data-ttu-id="e9100-123">**ottenere \_ ParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="e9100-123">**get\_ParticipantTypedInfo**</span></span>](itparticipant-get-participanttypedinfo.md) | <span data-ttu-id="e9100-124">Ottiene una rappresentazione BSTR del tipo di informazioni necessario, ad esempio PTI \_ EMAILADDRESS.</span><span class="sxs-lookup"><span data-stu-id="e9100-124">Gets a BSTR representation of the needed type of information, such as PTI\_EMAILADDRESS.</span></span><br/>                                                                     |
| [<span data-ttu-id="e9100-125">**ottenere \_ lo stato**</span><span class="sxs-lookup"><span data-stu-id="e9100-125">**get\_Status**</span></span>](itparticipant-get-status.md)                             | <span data-ttu-id="e9100-126">Ottiene lo stato del partecipante.</span><span class="sxs-lookup"><span data-stu-id="e9100-126">Gets the status of the participant.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="e9100-127">**ottenere i \_ flussi**</span><span class="sxs-lookup"><span data-stu-id="e9100-127">**get\_Streams**</span></span>](itparticipant-get-streams.md)                           | <span data-ttu-id="e9100-128">Crea una raccolta di flussi associati al partecipante corrente.</span><span class="sxs-lookup"><span data-stu-id="e9100-128">Creates a collection of streams associated with the current participant.</span></span> <span data-ttu-id="e9100-129">Fornito per le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e9100-129">Provided for Automation client applications, such as those written in Visual Basic.</span></span><br/> |
| [<span data-ttu-id="e9100-130">**Inserisci \_ stato**</span><span class="sxs-lookup"><span data-stu-id="e9100-130">**put\_Status**</span></span>](itparticipant-put-status.md)                             | <span data-ttu-id="e9100-131">Imposta un valore che indica se un flusso associato al partecipante è abilitato.</span><span class="sxs-lookup"><span data-stu-id="e9100-131">Sets whether a stream associated with the participant is enabled.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="e9100-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9100-132">Requirements</span></span>



| <span data-ttu-id="e9100-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9100-133">Requirement</span></span> | <span data-ttu-id="e9100-134">Valore</span><span class="sxs-lookup"><span data-stu-id="e9100-134">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e9100-135">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="e9100-135">TAPI version</span></span><br/> | <span data-ttu-id="e9100-136">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e9100-136">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="e9100-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9100-137">Header</span></span><br/>       | <dl> <span data-ttu-id="e9100-138"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9100-138"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9100-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9100-139">Library</span></span><br/>      | <dl> <span data-ttu-id="e9100-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9100-140"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="e9100-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e9100-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="e9100-142"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9100-142"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9100-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9100-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9100-144">MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="e9100-144">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="e9100-145">Interfacce MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="e9100-145">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e9100-146">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="e9100-146">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 

