---
description: Generato dal motore dei criteri quando l'acquisizione della licenza sta per iniziare. L'acquisizione della licenza viene eseguita usando l'implementazione delle applicazioni dell'interfaccia IMFContentProtectionManager.
ms.assetid: c328743c-a69b-431e-8a05-0e140aad9b4d
title: Evento MELicenseAcquisitionStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914d2580c95cf40986a844a994c1e284c5ad9e22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309634"
---
# <a name="melicenseacquisitionstart-event"></a><span data-ttu-id="86c62-104">Evento MELicenseAcquisitionStart</span><span class="sxs-lookup"><span data-stu-id="86c62-104">MELicenseAcquisitionStart event</span></span>

<span data-ttu-id="86c62-105">Generato dal motore dei criteri quando l'acquisizione della licenza sta per iniziare.</span><span class="sxs-lookup"><span data-stu-id="86c62-105">Raised by the policy engine when license acquisition is about to begin.</span></span> <span data-ttu-id="86c62-106">L'acquisizione della licenza viene eseguita usando l'implementazione dell'applicazione dell'interfaccia [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) .</span><span class="sxs-lookup"><span data-stu-id="86c62-106">License acquisition is performed using the application's implementation of the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

## <a name="event-values"></a><span data-ttu-id="86c62-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="86c62-107">Event values</span></span>

<span data-ttu-id="86c62-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="86c62-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="86c62-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="86c62-109">VARTYPE</span></span>              | <span data-ttu-id="86c62-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86c62-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="86c62-111">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="86c62-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="86c62-112">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="86c62-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="86c62-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="86c62-113">Remarks</span></span>

<span data-ttu-id="86c62-114">Quando l'acquisizione della licenza viene completata, il motore dei criteri genera l'evento [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="86c62-114">When license acquisition is completed, the policy engine raises the [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="86c62-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86c62-115">Requirements</span></span>



| <span data-ttu-id="86c62-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="86c62-116">Requirement</span></span> | <span data-ttu-id="86c62-117">Valore</span><span class="sxs-lookup"><span data-stu-id="86c62-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86c62-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86c62-118">Minimum supported client</span></span><br/> | <span data-ttu-id="86c62-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86c62-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="86c62-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86c62-120">Minimum supported server</span></span><br/> | <span data-ttu-id="86c62-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="86c62-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="86c62-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86c62-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="86c62-123"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86c62-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86c62-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86c62-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c62-125">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="86c62-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




