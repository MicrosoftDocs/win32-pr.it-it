---
description: L'interfaccia IKeyFrameControl viene implementata da H. 323 MSP ed è disponibile solo negli oggetti flusso H. 323.
ms.assetid: 68cb1df1-f7fa-447a-8ea5-80dc1e802760
title: Interfaccia IKeyFrameControl (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c326c6a492777d7c41ae450a1c502c343aeb8cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329328"
---
# <a name="ikeyframecontrol-interface"></a><span data-ttu-id="df7df-103">Interfaccia IKeyFrameControl</span><span class="sxs-lookup"><span data-stu-id="df7df-103">IKeyFrameControl interface</span></span>

<span data-ttu-id="df7df-104">\[**IKeyFrameControl** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="df7df-104">\[**IKeyFrameControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="df7df-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="df7df-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="df7df-106">L'interfaccia **IKeyFrameControl** viene implementata da [h. 323 msp](h323-msp.md) ed è disponibile solo negli oggetti flusso h. 323.</span><span class="sxs-lookup"><span data-stu-id="df7df-106">The **IKeyFrameControl** interface is implemented by the [H.323 MSP](h323-msp.md) and is available only on H.323 stream objects.</span></span> <span data-ttu-id="df7df-107">Questa interfaccia espone i metodi che consentono la creazione e la manipolazione di terminali che possono comunicare tra client H323 e SDP.</span><span class="sxs-lookup"><span data-stu-id="df7df-107">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span> <span data-ttu-id="df7df-108">Dispone di due metodi che consentono all'applicazione di richiedere all'endpoint remoto di aggiornare l'immagine video con un fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="df7df-108">It has two methods that allow the application to ask the remote endpoint to update the video image with a keyframe.</span></span>

## <a name="members"></a><span data-ttu-id="df7df-109">Membri</span><span class="sxs-lookup"><span data-stu-id="df7df-109">Members</span></span>

<span data-ttu-id="df7df-110">L'interfaccia **IKeyFrameControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="df7df-110">The **IKeyFrameControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="df7df-111">**IKeyFrameControl** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="df7df-111">**IKeyFrameControl** also has these types of members:</span></span>

-   [<span data-ttu-id="df7df-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="df7df-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="df7df-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="df7df-113">Methods</span></span>

<span data-ttu-id="df7df-114">L'interfaccia **IKeyFrameControl** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="df7df-114">The **IKeyFrameControl** interface has these methods.</span></span>



| <span data-ttu-id="df7df-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="df7df-115">Method</span></span>                                                                  | <span data-ttu-id="df7df-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df7df-116">Description</span></span>                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df7df-117">**PeriodicUpdatePicture**</span><span class="sxs-lookup"><span data-stu-id="df7df-117">**PeriodicUpdatePicture**</span></span>](ikeyframecontrol-periodicupdatepicture.md) | <span data-ttu-id="df7df-118">Configura un timer nel flusso che richiederà periodicamente gli aggiornamenti delle immagini.</span><span class="sxs-lookup"><span data-stu-id="df7df-118">Configures a timer in the stream that will ask for picture updates periodically.</span></span><br/> |
| [<span data-ttu-id="df7df-119">**UpdatePicture**</span><span class="sxs-lookup"><span data-stu-id="df7df-119">**UpdatePicture**</span></span>](ikeyframecontrol-updatepicture.md)                 | <span data-ttu-id="df7df-120">Chiede al mittente del video di aggiornare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="df7df-120">Asks the video sender to update the picture.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="df7df-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df7df-121">Requirements</span></span>



| <span data-ttu-id="df7df-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="df7df-122">Requirement</span></span> | <span data-ttu-id="df7df-123">Valore</span><span class="sxs-lookup"><span data-stu-id="df7df-123">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df7df-124">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="df7df-124">TAPI version</span></span><br/> | <span data-ttu-id="df7df-125">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="df7df-125">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="df7df-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df7df-126">Header</span></span><br/>       | <dl> <span data-ttu-id="df7df-127"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="df7df-127"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="df7df-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="df7df-128">Library</span></span><br/>      | <dl> <span data-ttu-id="df7df-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df7df-129"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="df7df-130">DLL</span><span class="sxs-lookup"><span data-stu-id="df7df-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="df7df-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df7df-131"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="df7df-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df7df-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df7df-133">MSP H323</span><span class="sxs-lookup"><span data-stu-id="df7df-133">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

