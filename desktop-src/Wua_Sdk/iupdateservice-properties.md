---
description: L'interfaccia IUpdateService definisce le proprietà seguenti.
ms.assetid: 33bc28e8-0b83-4d58-a03e-ccf2a97887e6
title: Proprietà di IUpdateService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ff3cf92c89a5ba02b7d95f1a1c99f33de3202d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485132"
---
# <a name="iupdateservice-properties"></a><span data-ttu-id="7acb0-103">Proprietà di IUpdateService</span><span class="sxs-lookup"><span data-stu-id="7acb0-103">IUpdateService Properties</span></span>

<span data-ttu-id="7acb0-104">L'interfaccia [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="7acb0-104">The [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) interface defines the following properties.</span></span>



| <span data-ttu-id="7acb0-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7acb0-105">Property</span></span>                                                              | <span data-ttu-id="7acb0-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7acb0-106">Description</span></span>                                                                                     |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7acb0-107">**CanRegisterWithAU**</span><span class="sxs-lookup"><span data-stu-id="7acb0-107">**CanRegisterWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_canregisterwithau)         | <span data-ttu-id="7acb0-108">Ottiene un valore booleano che indica se il servizio può eseguire la registrazione con Aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="7acb0-108">Gets a Boolean value that indicates whether the service can register with Automatic Updates.</span></span>    |
| [<span data-ttu-id="7acb0-109">**ContentValidationCert**</span><span class="sxs-lookup"><span data-stu-id="7acb0-109">**ContentValidationCert**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_contentvalidationcert) | <span data-ttu-id="7acb0-110">Ottiene un hash SHA-1 del certificato utilizzato per firmare il contenuto del servizio.</span><span class="sxs-lookup"><span data-stu-id="7acb0-110">Gets an SHA-1 hash of the certificate that is used to sign the contents of the service.</span></span>         |
| [<span data-ttu-id="7acb0-111">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="7acb0-111">**ExpirationDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_expirationdate)               | <span data-ttu-id="7acb0-112">Ottiene la data di scadenza del file CAB di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="7acb0-112">Gets the date on which the authorization cabinet file expires.</span></span>                                  |
| [<span data-ttu-id="7acb0-113">**IsManaged**</span><span class="sxs-lookup"><span data-stu-id="7acb0-113">**IsManaged**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_ismanaged)                         | <span data-ttu-id="7acb0-114">Ottiene un valore booleano che indica se un servizio è un servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="7acb0-114">Gets a Boolean value that indicates whether a service is a managed service.</span></span>                     |
| [<span data-ttu-id="7acb0-115">**IsRegisteredWithAU**</span><span class="sxs-lookup"><span data-stu-id="7acb0-115">**IsRegisteredWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isregisteredwithau)       | <span data-ttu-id="7acb0-116">Ottiene un valore booleano che indica se un servizio è registrato con Aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="7acb0-116">Gets a Boolean value that indicates whether a service is registered with Automatic Updates.</span></span>     |
| [<span data-ttu-id="7acb0-117">**IsScanPackageService**</span><span class="sxs-lookup"><span data-stu-id="7acb0-117">**IsScanPackageService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isscanpackageservice)   | <span data-ttu-id="7acb0-118">Ottiene un valore booleano che indica se un servizio è basato su un pacchetto di analisi.</span><span class="sxs-lookup"><span data-stu-id="7acb0-118">Gets a Boolean value that indicates whether a service is based on a scan package.</span></span>               |
| [<span data-ttu-id="7acb0-119">**IssueDate**</span><span class="sxs-lookup"><span data-stu-id="7acb0-119">**IssueDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_issuedate)                         | <span data-ttu-id="7acb0-120">Ottiene la data in cui è stato emesso il file CAB di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="7acb0-120">Gets the date on which the authorization cabinet file was issued.</span></span>                               |
| [<span data-ttu-id="7acb0-121">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7acb0-121">**Name**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_name)                                   | <span data-ttu-id="7acb0-122">Ottiene il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="7acb0-122">Gets the name of the service.</span></span>                                                                   |
| [<span data-ttu-id="7acb0-123">**OffersWindowsUpdates**</span><span class="sxs-lookup"><span data-stu-id="7acb0-123">**OffersWindowsUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_offerswindowsupdates)   | <span data-ttu-id="7acb0-124">Ottiene un valore booleano che indica se il servizio corrente offre aggiornamenti da aggiornamenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="7acb0-124">Gets a Boolean value indicates whether the current service offers updates from Windows Updates.</span></span> |
| [<span data-ttu-id="7acb0-125">**RedirectUrls**</span><span class="sxs-lookup"><span data-stu-id="7acb0-125">**RedirectUrls**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_redirecturls)                   | <span data-ttu-id="7acb0-126">Ottiene l'URL per il file CAB del redirector.</span><span class="sxs-lookup"><span data-stu-id="7acb0-126">Gets the URL for the redirector cabinet file.</span></span>                                                   |
| [<span data-ttu-id="7acb0-127">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="7acb0-127">**ServiceID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceid)                         | <span data-ttu-id="7acb0-128">Ottiene l'identificatore per un servizio.</span><span class="sxs-lookup"><span data-stu-id="7acb0-128">Gets the identifier for a service.</span></span>                                                              |
| [<span data-ttu-id="7acb0-129">**ServiceUrl**</span><span class="sxs-lookup"><span data-stu-id="7acb0-129">**ServiceUrl**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceurl)                       | <span data-ttu-id="7acb0-130">Ottiene l'URL per il servizio.</span><span class="sxs-lookup"><span data-stu-id="7acb0-130">Gets the URL for the service.</span></span>                                                                   |
| [<span data-ttu-id="7acb0-131">**SetupPrefix**</span><span class="sxs-lookup"><span data-stu-id="7acb0-131">**SetupPrefix**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_setupprefix)                     | <span data-ttu-id="7acb0-132">Ottiene il prefisso per i file di installazione.</span><span class="sxs-lookup"><span data-stu-id="7acb0-132">Gets the prefix for the setup files.</span></span>                                                            |



 

 

 



