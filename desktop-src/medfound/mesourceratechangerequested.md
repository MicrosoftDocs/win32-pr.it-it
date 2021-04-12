---
description: "Generato da un'origine multimediale per richiedere una nuova velocità di riproduzione. L'applicazione deve chiamare IMFRateControl:: serate con la frequenza richiesta. Un'origine multimediale potrebbe generare questo evento se non può continuare la riproduzione alla frequenza corrente."
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: Evento MESourceRateChangeRequested (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973a509541f3ec3d4f6a235b8f1277a20f7ed1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226655"
---
# <a name="mesourceratechangerequested-event"></a><span data-ttu-id="82711-105">Evento MESourceRateChangeRequested</span><span class="sxs-lookup"><span data-stu-id="82711-105">MESourceRateChangeRequested event</span></span>

<span data-ttu-id="82711-106">Generato da un'origine multimediale per richiedere una nuova velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="82711-106">Raised by a media source to request a new playback rate.</span></span> <span data-ttu-id="82711-107">L'applicazione deve chiamare [**IMFRateControl:: serate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) con la frequenza richiesta.</span><span class="sxs-lookup"><span data-stu-id="82711-107">The application should call [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) with the requested rate.</span></span> <span data-ttu-id="82711-108">Un'origine multimediale potrebbe generare questo evento se non può continuare la riproduzione alla frequenza corrente.</span><span class="sxs-lookup"><span data-stu-id="82711-108">A media source might raise this event if it cannot continue playback at the current rate.</span></span>

## <a name="event-values"></a><span data-ttu-id="82711-109">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="82711-109">Event values</span></span>

<span data-ttu-id="82711-110">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="82711-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="82711-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="82711-111">VARTYPE</span></span>           | <span data-ttu-id="82711-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82711-112">Description</span></span>                                             |
|-------------------|---------------------------------------------------------|
| <span data-ttu-id="82711-113">\_R4 VT</span><span class="sxs-lookup"><span data-stu-id="82711-113">VT\_R4</span></span><br/> | <span data-ttu-id="82711-114">La nuova frequenza di riproduzione richiesta.</span><span class="sxs-lookup"><span data-stu-id="82711-114">The requested new playback rate.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="82711-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="82711-115">Attributes</span></span>

<span data-ttu-id="82711-116">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="82711-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="82711-117">Attributo</span><span class="sxs-lookup"><span data-stu-id="82711-117">Attribute</span></span>                                                                    | <span data-ttu-id="82711-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82711-118">Description</span></span>                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="82711-119">**MF \_ evento \_ do \_ assottigliamento**</span><span class="sxs-lookup"><span data-stu-id="82711-119">**MF\_EVENT\_DO\_THINNING**</span></span>](mf-event-do-thinning-attribute.md)<br/> | <span data-ttu-id="82711-120">Specifica se l'origine multimediale richiede anche l'assottigliamento.</span><span class="sxs-lookup"><span data-stu-id="82711-120">Specifies whether the media source also requests thinning.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="82711-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82711-121">Requirements</span></span>



| <span data-ttu-id="82711-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="82711-122">Requirement</span></span> | <span data-ttu-id="82711-123">Valore</span><span class="sxs-lookup"><span data-stu-id="82711-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82711-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82711-124">Minimum supported client</span></span><br/> | <span data-ttu-id="82711-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="82711-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="82711-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82711-126">Minimum supported server</span></span><br/> | <span data-ttu-id="82711-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="82711-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="82711-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82711-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="82711-129"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82711-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82711-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82711-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82711-131">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="82711-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




