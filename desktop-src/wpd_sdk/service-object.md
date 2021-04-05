---
description: Oggetto servizio
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Oggetto servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a3aabfc4e4366c54a5d30dbe5825f178378133d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885314"
---
# <a name="service-object"></a><span data-ttu-id="cc11c-103">Oggetto servizio</span><span class="sxs-lookup"><span data-stu-id="cc11c-103">Service Object</span></span>

<span data-ttu-id="cc11c-104">L'oggetto servizio deve supportare le seguenti proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc11c-104">The service object must support the following properties.</span></span>



| <span data-ttu-id="cc11c-105">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="cc11c-105">Property Name</span></span>                                                                                                                      | <span data-ttu-id="cc11c-106">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="cc11c-106">Required or Optional</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc11c-107">[\_ID oggetto \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc11c-107">[WPD\_OBJECT\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                         | <span data-ttu-id="cc11c-108">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="cc11c-108">Required.</span></span> <span data-ttu-id="cc11c-109">.</span><span class="sxs-lookup"><span data-stu-id="cc11c-109">.</span></span>                                                                           |
| <span data-ttu-id="cc11c-110">[\_ \_ ID padre dell'oggetto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc11c-110">[WPD\_OBJECT\_PARENT\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                   | <span data-ttu-id="cc11c-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="cc11c-111">Required.</span></span>                                                                             |
| <span data-ttu-id="cc11c-112">[\_nome dell'oggetto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc11c-112">[WPD\_OBJECT\_NAME](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                   | <span data-ttu-id="cc11c-113">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="cc11c-113">Required.</span></span>                                                                             |
| <span data-ttu-id="cc11c-114">[\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc11c-114">[WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span> | <span data-ttu-id="cc11c-115">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="cc11c-115">Required.</span></span>                                                                             |
| <span data-ttu-id="cc11c-116">[\_oggetto WPD \_ nascosto](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc11c-116">[WPD\_OBJECT\_ISHIDDEN](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="cc11c-117">Obbligatorio se l'oggetto servizio non deve essere visualizzato all'utente.</span><span class="sxs-lookup"><span data-stu-id="cc11c-117">Required if the service object should not be shown to the user.</span></span>                       |
| <span data-ttu-id="cc11c-118">[\_oggetto WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc11c-118">[WPD\_OBJECT\_ISSYSTEM](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="cc11c-119">Obbligatorio se l'oggetto è un oggetto di sistema (ad esempio, rappresenta un file di sistema).</span><span class="sxs-lookup"><span data-stu-id="cc11c-119">Required if the object is a system object (for example, it represents a system file).</span></span> |
| <span data-ttu-id="cc11c-120">[\_ \_ categoria oggetto funzionale \_ WPD](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc11c-120">[WPD\_FUNCTIONAL\_OBJECT\_CATEGORY](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>     | <span data-ttu-id="cc11c-121">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="cc11c-121">Required.</span></span> <span data-ttu-id="cc11c-122">Rappresenta il tipo di servizio del dispositivo, ad esempio i contatti del servizio.</span><span class="sxs-lookup"><span data-stu-id="cc11c-122">This represents the Device Service type, such as SERVICE Contacts.</span></span>          |
| <span data-ttu-id="cc11c-123">[\_versione del servizio WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc11c-123">[WPD\_SERVICE\_VERSION](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="cc11c-124">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="cc11c-124">Required.</span></span>                                                                             |
| <span data-ttu-id="cc11c-125">[\_tipo di archiviazione WPD \_](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc11c-125">[WPD\_STORAGE\_TYPE](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                | <span data-ttu-id="cc11c-126">Obbligatorio se il servizio viene utilizzato per archiviare gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="cc11c-126">Required if the service is used to store objects.</span></span>                                     |
| <span data-ttu-id="cc11c-127">[\_capacità di archiviazione WPD \_](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc11c-127">[WPD\_STORAGE\_CAPACITY](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))</span></span>                                    | <span data-ttu-id="cc11c-128">Obbligatorio se il servizio viene utilizzato per archiviare gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="cc11c-128">Required if the service is used to store objects.</span></span>                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="cc11c-129">Risorse tipiche</span><span class="sxs-lookup"><span data-stu-id="cc11c-129">Typical Resources</span></span>

<span data-ttu-id="cc11c-130">Questi oggetti in genere non ospitano risorse.</span><span class="sxs-lookup"><span data-stu-id="cc11c-130">These objects typically do not host resources.</span></span>

## <a name="typical-formats"></a><span data-ttu-id="cc11c-131">Formati tipici</span><span class="sxs-lookup"><span data-stu-id="cc11c-131">Typical Formats</span></span>

<span data-ttu-id="cc11c-132">Nell'elenco seguente vengono identificati i formati tipici utilizzati dall'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="cc11c-132">The following list identifies typical formats used by the Service object.</span></span> <span data-ttu-id="cc11c-133">Questo oggetto, tuttavia, non è limitato a questi formati.</span><span class="sxs-lookup"><span data-stu-id="cc11c-133">However, this object is not limited to these formats.</span></span>

-   <span data-ttu-id="cc11c-134">\_formato oggetto WPD non \_ \_ specificato</span><span class="sxs-lookup"><span data-stu-id="cc11c-134">WPD\_OBJECT\_FORMAT\_UNSPECIFIED</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc11c-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc11c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc11c-136">**Requisiti per gli oggetti**</span><span class="sxs-lookup"><span data-stu-id="cc11c-136">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 
