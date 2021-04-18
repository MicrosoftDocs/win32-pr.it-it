---
description: "Generato dall'origine del sequencer quando il metodo IMFSequencerSource:: UpdateTopology viene completato in modo asincrono."
ms.assetid: f573cbd0-689c-4bfe-846b-6fc8008101c8
title: Evento MESequencerSourceTopologyUpdated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaf03119832937a584178b9f5958b066046c633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309619"
---
# <a name="mesequencersourcetopologyupdated-event"></a><span data-ttu-id="7ca81-103">Evento MESequencerSourceTopologyUpdated</span><span class="sxs-lookup"><span data-stu-id="7ca81-103">MESequencerSourceTopologyUpdated event</span></span>

<span data-ttu-id="7ca81-104">Generato dall'origine del sequencer quando il metodo [**IMFSequencerSource:: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) viene completato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="7ca81-104">Raised by the sequencer source when the [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="7ca81-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="7ca81-105">Event values</span></span>

<span data-ttu-id="7ca81-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="7ca81-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="7ca81-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="7ca81-107">VARTYPE</span></span>            | <span data-ttu-id="7ca81-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ca81-108">Description</span></span>                                                                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca81-109">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="7ca81-109">VT\_UI4</span></span><br/> | <span data-ttu-id="7ca81-110">Identificatore dell'elemento sequencer della topologia da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="7ca81-110">Sequencer element identifier of the topology that is being updated.</span></span> <span data-ttu-id="7ca81-111">L'applicazione specifica questo valore nel parametro *dwID* del metodo [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) .</span><span class="sxs-lookup"><span data-stu-id="7ca81-111">The application specifies this value in the *dwId* parameter of the [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) method.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7ca81-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ca81-112">Remarks</span></span>

<span data-ttu-id="7ca81-113">Questo evento segnala che l'origine del sequencer ha aggiornato la topologia, ma non significa che la topologia è pronta per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="7ca81-113">This event signals that the sequencer source has updated the topology, but does not mean that the topology is ready for playback.</span></span> <span data-ttu-id="7ca81-114">L'applicazione deve attendere l'evento [MESessionTopologyStatus](mesessiontopologystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="7ca81-114">The application should wait for the [MESessionTopologyStatus](mesessiontopologystatus.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ca81-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ca81-115">Requirements</span></span>



| <span data-ttu-id="7ca81-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ca81-116">Requirement</span></span> | <span data-ttu-id="7ca81-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7ca81-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca81-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ca81-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7ca81-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ca81-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7ca81-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ca81-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7ca81-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ca81-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7ca81-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ca81-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ca81-123"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ca81-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ca81-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ca81-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca81-125">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7ca81-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="7ca81-126">Origine sequencer</span><span class="sxs-lookup"><span data-stu-id="7ca81-126">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




