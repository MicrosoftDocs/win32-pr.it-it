---
description: '\_ \_ servizio tipo di contenuto WPD \_'
ms.assetid: 87c4c228-69e0-4b55-b91f-fe6e561f6d18
title: WPD_CONTENT_TYPE_SERVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1655825828867e38ef1962d35bcb0cfebf4ed76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968155"
---
# <a name="wpd_content_type_service"></a><span data-ttu-id="95b1e-103">\_ \_ servizio tipo di contenuto WPD \_</span><span class="sxs-lookup"><span data-stu-id="95b1e-103">WPD\_CONTENT\_TYPE\_SERVICE</span></span>

<span data-ttu-id="95b1e-104">Un oggetto che descrive il tipo come \_ servizio del tipo di contenuto WPD \_ \_ rappresenta un servizio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95b1e-104">An object that describes its type as WPD\_CONTENT\_TYPE\_SERVICE represents a device service.</span></span>

<span data-ttu-id="95b1e-105">Questo tipo di oggetto supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="95b1e-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="95b1e-106">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="95b1e-106">Property Name</span></span>                                                                                        | <span data-ttu-id="95b1e-107">Obbligatorio o facoltativo</span><span class="sxs-lookup"><span data-stu-id="95b1e-107">Required or Optional</span></span>                                                           |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="95b1e-108">\_ID oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="95b1e-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                               | <span data-ttu-id="95b1e-109">Obbligatorio, di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="95b1e-109">Required, read-only.</span></span> <span data-ttu-id="95b1e-110">Un client non può impostare questa proprietà, anche in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="95b1e-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="95b1e-111">\_ \_ ID padre dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="95b1e-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                | <span data-ttu-id="95b1e-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="95b1e-112">Required.</span></span>                                                                      |
| [<span data-ttu-id="95b1e-113">\_nome dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="95b1e-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                           | <span data-ttu-id="95b1e-114">Obbligatorio se l'oggetto rappresenta un file.</span><span class="sxs-lookup"><span data-stu-id="95b1e-114">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="95b1e-115">\_ \_ \_ ID univoco permanente dell'oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="95b1e-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)         | <span data-ttu-id="95b1e-116">Obbligatorio, di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="95b1e-116">Required, read-only.</span></span> <span data-ttu-id="95b1e-117">Un client non può impostare questa proprietà, anche in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="95b1e-117">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="95b1e-118">\_oggetto WPD \_ nascosto</span><span class="sxs-lookup"><span data-stu-id="95b1e-118">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                   | <span data-ttu-id="95b1e-119">Obbligatorio se il servizio non deve essere visualizzato all'utente.</span><span class="sxs-lookup"><span data-stu-id="95b1e-119">Required if the service should not be shown to the user.</span></span>                       |
| [<span data-ttu-id="95b1e-120">\_oggetto WPD \_</span><span class="sxs-lookup"><span data-stu-id="95b1e-120">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                   | <span data-ttu-id="95b1e-121">Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema).</span><span class="sxs-lookup"><span data-stu-id="95b1e-121">Required if the object is a system object (represents a system file).</span></span>          |
| [<span data-ttu-id="95b1e-122">\_ \_ categoria oggetto funzionale \_ WPD</span><span class="sxs-lookup"><span data-stu-id="95b1e-122">WPD\_FUNCTIONAL\_OBJECT\_CATEGORY</span></span>](object-properties.md) | <span data-ttu-id="95b1e-123">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="95b1e-123">Required.</span></span> <span data-ttu-id="95b1e-124">Rappresenta il tipo di servizio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95b1e-124">This represents the device service type.</span></span>                             |
| [<span data-ttu-id="95b1e-125">\_versione del servizio WPD \_</span><span class="sxs-lookup"><span data-stu-id="95b1e-125">WPD\_SERVICE\_VERSION</span></span>](object-properties.md)           | <span data-ttu-id="95b1e-126">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="95b1e-126">Required.</span></span>                                                                      |
| [<span data-ttu-id="95b1e-127">\_tipo di archiviazione WPD \_</span><span class="sxs-lookup"><span data-stu-id="95b1e-127">WPD\_STORAGE\_TYPE</span></span>](object-properties.md)                                                          | <span data-ttu-id="95b1e-128">Obbligatorio se il servizio viene utilizzato per archiviare gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="95b1e-128">Required if the service is used to store objects.</span></span>                              |
| [<span data-ttu-id="95b1e-129">\_capacità di archiviazione WPD \_</span><span class="sxs-lookup"><span data-stu-id="95b1e-129">WPD\_STORAGE\_CAPACITY</span></span>](object-properties.md)                                                      | <span data-ttu-id="95b1e-130">Obbligatorio se il servizio viene utilizzato per archiviare gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="95b1e-130">Required if the service is used to store objects.</span></span>                              |



 

## <a name="typical-resources"></a><span data-ttu-id="95b1e-131">Risorse tipiche</span><span class="sxs-lookup"><span data-stu-id="95b1e-131">Typical Resources</span></span>

<span data-ttu-id="95b1e-132">Questi oggetti non ospitano risorse.</span><span class="sxs-lookup"><span data-stu-id="95b1e-132">These objects do not host resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95b1e-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="95b1e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95b1e-134">**Requisiti per gli oggetti**</span><span class="sxs-lookup"><span data-stu-id="95b1e-134">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



