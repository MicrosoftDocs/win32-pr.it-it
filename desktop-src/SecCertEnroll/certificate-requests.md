---
description: L'SDK di registrazione certificati può essere usato per creare richieste di \# \# certificato autofirmato e PKCS 10, PKCS 7, CMC.
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: Richieste di certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690f3a5117abfa0ae262f0a8fa38f68528abf02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308124"
---
# <a name="certificate-requests"></a><span data-ttu-id="a64bf-103">Richieste di certificati</span><span class="sxs-lookup"><span data-stu-id="a64bf-103">Certificate Requests</span></span>

<span data-ttu-id="a64bf-104">L'SDK di registrazione certificati può essere usato per creare richieste di \# \# certificato autofirmato e PKCS 10, PKCS 7, CMC.</span><span class="sxs-lookup"><span data-stu-id="a64bf-104">The Certificate Enrollment SDK can be used to create PKCS \#10, PKCS \#7, CMC, and self-signed certificate requests.</span></span> <span data-ttu-id="a64bf-105">Ogni tipo di richiesta è rappresentato da una delle interfacce elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a64bf-105">Each type of request is represented by one of the interfaces listed in the following table.</span></span> <span data-ttu-id="a64bf-106">Tutte le interfacce di richiesta ereditano direttamente o indirettamente dall'interfaccia [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) .</span><span class="sxs-lookup"><span data-stu-id="a64bf-106">All request interfaces inherit directly or indirectly from the [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) interface.</span></span> 

| <span data-ttu-id="a64bf-107">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="a64bf-107">Interface</span></span>                                                                        | <span data-ttu-id="a64bf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a64bf-108">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a64bf-109">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="a64bf-109">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | <span data-ttu-id="a64bf-110">Rappresenta una \# richiesta PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="a64bf-110">Represents a PKCS \#10 request.</span></span> <span data-ttu-id="a64bf-111">Questa interfaccia eredita da [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span><span class="sxs-lookup"><span data-stu-id="a64bf-111">This interface inherits from [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span></span>                   |
| [<span data-ttu-id="a64bf-112">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="a64bf-112">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | <span data-ttu-id="a64bf-113">Rappresenta una \# richiesta PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="a64bf-113">Represents a PKCS \#7 request.</span></span> <span data-ttu-id="a64bf-114">Questa interfaccia eredita da [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span><span class="sxs-lookup"><span data-stu-id="a64bf-114">This interface inherits from [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span></span>                    |
| [<span data-ttu-id="a64bf-115">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="a64bf-115">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | <span data-ttu-id="a64bf-116">Rappresenta un certificato autofirmato.</span><span class="sxs-lookup"><span data-stu-id="a64bf-116">Represents a self-signed certificate.</span></span> <span data-ttu-id="a64bf-117">Questa interfaccia eredita da [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10).</span><span class="sxs-lookup"><span data-stu-id="a64bf-117">This interface inherits from [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10).</span></span> |
| [<span data-ttu-id="a64bf-118">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="a64bf-118">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | <span data-ttu-id="a64bf-119">Rappresenta una richiesta CMC.</span><span class="sxs-lookup"><span data-stu-id="a64bf-119">Represents a CMC request.</span></span> <span data-ttu-id="a64bf-120">Questa interfaccia eredita da [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).</span><span class="sxs-lookup"><span data-stu-id="a64bf-120">This interface inherits from [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).</span></span>               |



 

<span data-ttu-id="a64bf-121">Nella figura seguente viene illustrata la struttura di ereditarietà degli oggetti Request supportati dall'API di registrazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="a64bf-121">The following illustration shows the inheritance structure of the request objects supported by the Certificate Enrollment API.</span></span> <span data-ttu-id="a64bf-122">Un oggetto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) serve, direttamente o indirettamente, come classe di base per tutti gli oggetti richiesta disponibili.</span><span class="sxs-lookup"><span data-stu-id="a64bf-122">An [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) object serves, directly or indirectly, as the base class for all of the available request objects.</span></span>

![struttura di ereditarietà per le interfacce di richiesta](images/certificate-request-inheritance.png)

<span data-ttu-id="a64bf-124">Indipendentemente dal tipo, una richiesta di certificato contiene informazioni sull'oggetto che effettua la richiesta, la chiave pubblica del soggetto, un set di attributi, un set di estensioni X. 509 versione 3 (che possono essere inviate come parte degli attributi) e una firma.</span><span class="sxs-lookup"><span data-stu-id="a64bf-124">Regardless of type, a certificate request contains information about the subject making the request, the subject's public key, a set of attributes, a set of X.509 version 3 extensions (which may be submitted as part of the attributes), and a signature.</span></span> <span data-ttu-id="a64bf-125">Questi problemi sono trattati negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a64bf-125">These issues are addressed by the following topics:</span></span>

-   [<span data-ttu-id="a64bf-126">Nomi soggetto</span><span class="sxs-lookup"><span data-stu-id="a64bf-126">Subject Names</span></span>](subject-names.md)
-   [<span data-ttu-id="a64bf-127">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="a64bf-127">Attributes</span></span>](attributes.md)
-   [<span data-ttu-id="a64bf-128">Estensioni</span><span class="sxs-lookup"><span data-stu-id="a64bf-128">Extensions</span></span>](extensions.md)

## <a name="related-topics"></a><span data-ttu-id="a64bf-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a64bf-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a64bf-130">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="a64bf-130">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[<span data-ttu-id="a64bf-131">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="a64bf-131">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[<span data-ttu-id="a64bf-132">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="a64bf-132">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[<span data-ttu-id="a64bf-133">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="a64bf-133">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> </dl>

 

 



