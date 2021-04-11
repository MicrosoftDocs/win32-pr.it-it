---
description: Tipo di evento sconosciuto. È possibile usare questo valore per inizializzare le variabili di tipo MediaEventType, ma un componente non deve mai generare l'evento MEUnknown.
ms.assetid: 786b69f4-8713-41db-829a-c13512baa3f1
title: Evento MEUnknown (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a768fde2939b7e32ed8d1007d2988c2e54cc6726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967050"
---
# <a name="meunknown-event"></a><span data-ttu-id="5b591-104">Evento MEUnknown</span><span class="sxs-lookup"><span data-stu-id="5b591-104">MEUnknown event</span></span>

<span data-ttu-id="5b591-105">Tipo di evento sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="5b591-105">Unknown event type.</span></span> <span data-ttu-id="5b591-106">È possibile usare questo valore per inizializzare le variabili di tipo **MediaEventType**, ma un componente non deve mai generare l'evento MEUnknown</span><span class="sxs-lookup"><span data-stu-id="5b591-106">You can use this value to initialize variables of type **MediaEventType**, but a component should never raise the MEUnknown event</span></span>

## <a name="event-values"></a><span data-ttu-id="5b591-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="5b591-107">Event values</span></span>

<span data-ttu-id="5b591-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="5b591-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5b591-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5b591-109">VARTYPE</span></span>              | <span data-ttu-id="5b591-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b591-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="5b591-111">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="5b591-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="5b591-112">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5b591-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="5b591-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b591-113">Requirements</span></span>



| <span data-ttu-id="5b591-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b591-114">Requirement</span></span> | <span data-ttu-id="5b591-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5b591-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b591-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b591-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5b591-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b591-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5b591-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b591-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5b591-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5b591-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5b591-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b591-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b591-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b591-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b591-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b591-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b591-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5b591-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




