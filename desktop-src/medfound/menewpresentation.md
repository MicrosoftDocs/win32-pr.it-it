---
description: Generato da un'origine multimediale che fornisce topologie tramite l'interfaccia IMFMediaSourceTopologyProvider, ad esempio l'origine del sequencer. L'origine genera l'evento quando dispone di una nuova presentazione. La sessione multimediale trasmette questo evento all'applicazione.
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: Evento MENewPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70265a84cc7724fc6f5b6a77be2181149bd82176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226662"
---
# <a name="menewpresentation-event"></a><span data-ttu-id="fcd2d-105">Evento MENewPresentation</span><span class="sxs-lookup"><span data-stu-id="fcd2d-105">MENewPresentation event</span></span>

<span data-ttu-id="fcd2d-106">Generato da un'origine multimediale che fornisce topologie tramite l'interfaccia [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) , ad esempio l'origine del sequencer.</span><span class="sxs-lookup"><span data-stu-id="fcd2d-106">Raised by a media source that provides topologies through the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface, such as the sequencer source.</span></span> <span data-ttu-id="fcd2d-107">L'origine genera l'evento quando dispone di una nuova presentazione.</span><span class="sxs-lookup"><span data-stu-id="fcd2d-107">The source raises the event when it has a new presentation.</span></span> <span data-ttu-id="fcd2d-108">La sessione multimediale trasmette questo evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fcd2d-108">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="fcd2d-109">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="fcd2d-109">Event values</span></span>

<span data-ttu-id="fcd2d-110">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="fcd2d-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="fcd2d-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="fcd2d-111">VARTYPE</span></span>                | <span data-ttu-id="fcd2d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fcd2d-112">Description</span></span>                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd2d-113">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="fcd2d-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="fcd2d-114">Puntatore all'interfaccia [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descrittore della presentazione per la nuova presentazione.</span><span class="sxs-lookup"><span data-stu-id="fcd2d-114">Pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor for the new presentation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="fcd2d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fcd2d-115">Remarks</span></span>

<span data-ttu-id="fcd2d-116">L'applicazione può ottenere la topologia che corrisponde al descrittore di presentazione chiamando [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) sull'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="fcd2d-116">The application can get the topology that corresponds to the presentation descriptor by calling [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) on the media source.</span></span> <span data-ttu-id="fcd2d-117">L'applicazione può quindi accodare la nuova topologia nella sessione multimediale chiamando [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="fcd2d-117">The application can then queue the new topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcd2d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fcd2d-118">Requirements</span></span>



| <span data-ttu-id="fcd2d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcd2d-119">Requirement</span></span> | <span data-ttu-id="fcd2d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fcd2d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd2d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcd2d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fcd2d-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fcd2d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fcd2d-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcd2d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fcd2d-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fcd2d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fcd2d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fcd2d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcd2d-126"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fcd2d-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcd2d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fcd2d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcd2d-128">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fcd2d-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="fcd2d-129">Origine sequencer</span><span class="sxs-lookup"><span data-stu-id="fcd2d-129">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




