---
description: La libreria Xenroll.dll è stata rimossa dal sistema operativo e sostituita da CertEnroll.dll.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Mapping Xenroll.dll CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fcaec56967f4c694b85d454bd21407c3af9029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758060"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a><span data-ttu-id="65375-103">Mapping Xenroll.dll CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="65375-103">Mapping Xenroll.dll to CertEnroll.dll</span></span>

<span data-ttu-id="65375-104">Prima di Windows Vista, il controllo di registrazione dei certificati veniva implementato in Xenroll.dll.</span><span class="sxs-lookup"><span data-stu-id="65375-104">Prior to Windows Vista, the Certificate Enrollment Control was implemented in Xenroll.dll.</span></span> <span data-ttu-id="65375-105">La libreria Xenroll.dll è stata rimossa dal sistema operativo e sostituita da CertEnroll.dll.</span><span class="sxs-lookup"><span data-stu-id="65375-105">The Xenroll.dll library has been removed from the operating system and replaced by CertEnroll.dll.</span></span>

<span data-ttu-id="65375-106">Xenroll ha tentato di implementare due set paralleli di interfacce.</span><span class="sxs-lookup"><span data-stu-id="65375-106">Xenroll attempted to implement two parallel sets of interfaces.</span></span> <span data-ttu-id="65375-107">[**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)e [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) sono conformi all'automazione e sono compatibili con i linguaggi di scripting.</span><span class="sxs-lookup"><span data-stu-id="65375-107">[**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3), and [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) were Automation-compliant and compatible with scripting languages.</span></span> <span data-ttu-id="65375-108">Le interfacce corrispondenti,[**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)e [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4), non possono essere generate nello script, ma sono più utili per i programmatori C++.</span><span class="sxs-lookup"><span data-stu-id="65375-108">The corresponding interfaces—[**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2), and [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)—could not be scripted but were more convenient for C++ programmers.</span></span> <span data-ttu-id="65375-109">Man mano che si sono evoluti, i due set di interfacce non rimangono sincronizzati.</span><span class="sxs-lookup"><span data-stu-id="65375-109">As they evolved, the two sets of interfaces did not remain synchronized.</span></span> <span data-ttu-id="65375-110">In particolare, il set di interfacce duali rappresentate più di recente da **ICEnroll4** definisce solo un subset della funzionalità definita da **IEnroll4**.</span><span class="sxs-lookup"><span data-stu-id="65375-110">In particular, the set of dual interfaces represented most recently by **ICEnroll4** defines only a subset of the functionality defined by **IEnroll4**.</span></span>

<span data-ttu-id="65375-111">CertEnroll.dll implementa un set più ampio e strutturato di interfacce COM compatibili con l'automazione.</span><span class="sxs-lookup"><span data-stu-id="65375-111">CertEnroll.dll implements a larger and more structured set of Automation-compliant COM interfaces.</span></span> <span data-ttu-id="65375-112">Negli argomenti seguenti viene illustrato come Xenroll.dll viene eseguito il mapping CertEnroll.dll per diversi tipi di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="65375-112">The following topics discuss how Xenroll.dll maps to CertEnroll.dll for different types of functionality.</span></span>

-   [<span data-ttu-id="65375-113">Funzioni di richiesta di certificato</span><span class="sxs-lookup"><span data-stu-id="65375-113">Certificate Request Functions</span></span>](certificate-request-functions.md)
-   [<span data-ttu-id="65375-114">Funzioni di risposta del certificato</span><span class="sxs-lookup"><span data-stu-id="65375-114">Certificate Response Functions</span></span>](certificate-response-functions.md)
-   [<span data-ttu-id="65375-115">Funzioni attributo</span><span class="sxs-lookup"><span data-stu-id="65375-115">Attribute Functions</span></span>](attribute-functions.md)
-   [<span data-ttu-id="65375-116">Funzioni di estensione</span><span class="sxs-lookup"><span data-stu-id="65375-116">Extension Functions</span></span>](extension-functions.md)
-   [<span data-ttu-id="65375-117">Funzioni di proprietà esterne</span><span class="sxs-lookup"><span data-stu-id="65375-117">External Property Functions</span></span>](external-property-functions.md)
-   [<span data-ttu-id="65375-118">Funzioni chiave privata e pubblica</span><span class="sxs-lookup"><span data-stu-id="65375-118">Private and Public Key Functions</span></span>](private-and-public-key-functions.md)
-   [<span data-ttu-id="65375-119">Funzioni del provider del servizio di crittografia</span><span class="sxs-lookup"><span data-stu-id="65375-119">Cryptographic Service Provider Functions</span></span>](cryptographic-service-provider-functions.md)
-   [<span data-ttu-id="65375-120">Funzioni dell'archivio certificati</span><span class="sxs-lookup"><span data-stu-id="65375-120">Certificate Store Functions</span></span>](certificate-store-functions.md)
-   [<span data-ttu-id="65375-121">Funzioni scambio informazioni personali</span><span class="sxs-lookup"><span data-stu-id="65375-121">Personal Information Exchange Functions</span></span>](personal-information-exchange-functions.md)
-   [<span data-ttu-id="65375-122">Funzioni helper</span><span class="sxs-lookup"><span data-stu-id="65375-122">Helper Functions</span></span>](helper-functions.md)

## <a name="related-topics"></a><span data-ttu-id="65375-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65375-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65375-124">Uso dell'API di registrazione certificati</span><span class="sxs-lookup"><span data-stu-id="65375-124">Using the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
