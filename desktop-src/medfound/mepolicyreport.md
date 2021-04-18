---
description: Generato da un output attendibile per inviare informazioni sullo stato relative all'imposizione dei criteri di output.
ms.assetid: 4906f6c3-1570-421f-aef1-914bd338bb1f
title: Evento MEPolicyReport (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0053fb551a69b820beeb4237211cb9af446f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309624"
---
# <a name="mepolicyreport-event"></a><span data-ttu-id="2b9a3-103">Evento MEPolicyReport</span><span class="sxs-lookup"><span data-stu-id="2b9a3-103">MEPolicyReport event</span></span>

<span data-ttu-id="2b9a3-104">Generato da un output attendibile per inviare informazioni sullo stato relative all'imposizione dei criteri di output.</span><span class="sxs-lookup"><span data-stu-id="2b9a3-104">Raised by a trusted output to send status information about the enforcement of the output policy.</span></span>

## <a name="event-values"></a><span data-ttu-id="2b9a3-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="2b9a3-105">Event values</span></span>

<span data-ttu-id="2b9a3-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="2b9a3-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="2b9a3-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2b9a3-107">VARTYPE</span></span>              | <span data-ttu-id="2b9a3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b9a3-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="2b9a3-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="2b9a3-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="2b9a3-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="2b9a3-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="2b9a3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b9a3-111">Remarks</span></span>

<span data-ttu-id="2b9a3-112">Gli attributi e i codici di stato per questo evento dipendono dal sistema di protezione del contenuto specifico applicato dall'output attendibile.</span><span class="sxs-lookup"><span data-stu-id="2b9a3-112">Attributes and status codes for this event depend on the specific content protection system enforced by the trusted output.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b9a3-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b9a3-113">Requirements</span></span>



| <span data-ttu-id="2b9a3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b9a3-114">Requirement</span></span> | <span data-ttu-id="2b9a3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2b9a3-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b9a3-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b9a3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2b9a3-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b9a3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2b9a3-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b9a3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2b9a3-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2b9a3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2b9a3-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b9a3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b9a3-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b9a3-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b9a3-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b9a3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b9a3-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2b9a3-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




