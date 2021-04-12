---
description: Per creare richieste di certificato, è possibile usare le interfacce seguenti.
ms.assetid: 6021db79-ac90-4e0c-afbd-0f926abcab78
title: Interfacce di richiesta di certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e18a4f8e1ce60348ffdf52afe210247f6d20a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129891"
---
# <a name="certificate-request-interfaces"></a><span data-ttu-id="2fce1-103">Interfacce di richiesta di certificato</span><span class="sxs-lookup"><span data-stu-id="2fce1-103">Certificate Request Interfaces</span></span>

<span data-ttu-id="2fce1-104">Per creare richieste di certificato, è possibile usare le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="2fce1-104">The following interfaces can be used to create certificate requests.</span></span>



| <span data-ttu-id="2fce1-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="2fce1-105">Interface</span></span>                                                                          | <span data-ttu-id="2fce1-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fce1-106">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fce1-107">**IX509CertificateRequest**</span><span class="sxs-lookup"><span data-stu-id="2fce1-107">**IX509CertificateRequest**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                         | <span data-ttu-id="2fce1-108">Rappresenta l'interfaccia di primo livello astratta per una richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="2fce1-108">Represents the abstract top-level interface for a certificate request.</span></span>                                                                                        |
| [<span data-ttu-id="2fce1-109">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="2fce1-109">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)   | <span data-ttu-id="2fce1-110">Consente di creare certificati direttamente senza passare attraverso un'autorità di certificazione o di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2fce1-110">Enables you to create certificates directly without going through a registration or certification authority.</span></span>                                                  |
| [<span data-ttu-id="2fce1-111">**IX509CertificateRequestCertificate2**</span><span class="sxs-lookup"><span data-stu-id="2fce1-111">**IX509CertificateRequestCertificate2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcertificate2) | <span data-ttu-id="2fce1-112">Estende l'interfaccia [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) per abilitare l'inizializzazione da un modello.</span><span class="sxs-lookup"><span data-stu-id="2fce1-112">Extends the [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) interface to enable initialization from a template.</span></span>              |
| [<span data-ttu-id="2fce1-113">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="2fce1-113">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                   | <span data-ttu-id="2fce1-114">Rappresenta una richiesta CMC.</span><span class="sxs-lookup"><span data-stu-id="2fce1-114">Represents a CMC request.</span></span>                                                                                                                                     |
| [<span data-ttu-id="2fce1-115">**IX509CertificateRequestCmc2**</span><span class="sxs-lookup"><span data-stu-id="2fce1-115">**IX509CertificateRequestCmc2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcmc2)                 | <span data-ttu-id="2fce1-116">Estende l'interfaccia [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) per abilitare l'inizializzazione da un modello.</span><span class="sxs-lookup"><span data-stu-id="2fce1-116">Extends the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) interface to enable initialization from a template.</span></span>                              |
| [<span data-ttu-id="2fce1-117">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="2fce1-117">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)             | <span data-ttu-id="2fce1-118">Rappresenta una \# richiesta PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="2fce1-118">Represents a PKCS \#10 request.</span></span>                                                                                                                               |
| [<span data-ttu-id="2fce1-119">**IX509CertificateRequestPkcs10V2**</span><span class="sxs-lookup"><span data-stu-id="2fce1-119">**IX509CertificateRequestPkcs10V2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v2)         | <span data-ttu-id="2fce1-120">Estende l'interfaccia [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) per abilitare l'inizializzazione da un modello.</span><span class="sxs-lookup"><span data-stu-id="2fce1-120">Extends the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) interface to enable initialization from a template.</span></span>                        |
| [<span data-ttu-id="2fce1-121">**IX509CertificateRequestPkcs10V3**</span><span class="sxs-lookup"><span data-stu-id="2fce1-121">**IX509CertificateRequestPkcs10V3**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3)         | <span data-ttu-id="2fce1-122">Estende l'interfaccia [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e aggiunge le proprietà che abilitano l'attestazione del certificato TPM.</span><span class="sxs-lookup"><span data-stu-id="2fce1-122">Extends the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) interface and adds properties that enable TPM certificate attestation.</span></span> |
| [<span data-ttu-id="2fce1-123">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="2fce1-123">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               | <span data-ttu-id="2fce1-124">Rappresenta una \# richiesta PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="2fce1-124">Represents a PKCS \#7 request.</span></span>                                                                                                                                |
| [<span data-ttu-id="2fce1-125">**IX509CertificateRequestPkcs7V2**</span><span class="sxs-lookup"><span data-stu-id="2fce1-125">**IX509CertificateRequestPkcs7V2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs7v2)           | <span data-ttu-id="2fce1-126">Estende l'interfaccia [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) per abilitare l'inizializzazione da un modello.</span><span class="sxs-lookup"><span data-stu-id="2fce1-126">Extends the [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) interface to enable initialization from a template.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="2fce1-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2fce1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fce1-128">Interfacce CertEnroll</span><span class="sxs-lookup"><span data-stu-id="2fce1-128">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



