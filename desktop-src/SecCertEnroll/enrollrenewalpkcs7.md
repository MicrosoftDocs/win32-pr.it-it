---
description: Crea un \# oggetto richiesta PKCS 7 per rinnovare un certificato esistente. L'oggetto Request utilizza una nuova coppia di chiavi, ma mantiene il provider del crittografico associato al certificato da rinnovare.
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8795758a2744dcee07a100f87eb1db0a1af49eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529389"
---
# <a name="enrollrenewalpkcs7"></a><span data-ttu-id="d8e44-104">enrollRenewalPKCS7</span><span class="sxs-lookup"><span data-stu-id="d8e44-104">enrollRenewalPKCS7</span></span>

<span data-ttu-id="d8e44-105">L'esempio enrollRenewalPKCS7 crea un \# oggetto richiesta PKCS 7 per rinnovare un certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="d8e44-105">The enrollRenewalPKCS7 sample creates a PKCS \#7 request object to renew an existing certificate.</span></span> <span data-ttu-id="d8e44-106">L'oggetto Request utilizza una nuova coppia di chiavi, ma mantiene il provider del crittografico associato al certificato da rinnovare.</span><span class="sxs-lookup"><span data-stu-id="d8e44-106">The request object uses a new key pair but retains the cryptographic provider associated with the certificate being renewed.</span></span>

## <a name="location"></a><span data-ttu-id="d8e44-107">Location</span><span class="sxs-lookup"><span data-stu-id="d8e44-107">Location</span></span>

<span data-ttu-id="d8e44-108">Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ enrollRenewalPKCS7</span><span class="sxs-lookup"><span data-stu-id="d8e44-108">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollRenewalPKCS7 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="d8e44-109">Discussione</span><span class="sxs-lookup"><span data-stu-id="d8e44-109">Discussion</span></span>

<span data-ttu-id="d8e44-110">Esempio enrollRenewalPKCS7:</span><span class="sxs-lookup"><span data-stu-id="d8e44-110">The enrollRenewalPKCS7 sample:</span></span>

1.  <span data-ttu-id="d8e44-111">Elabora gli argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="d8e44-111">Processes the command line arguments.</span></span> <span data-ttu-id="d8e44-112">La riga di comando deve contenere il nome del modello utilizzato per creare la richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="d8e44-112">The command line should contain the name of the template used to create the certificate request.</span></span>
2.  <span data-ttu-id="d8e44-113">Recupera un certificato esistente usando il nome del modello specificato nella riga di comando o, se non è possibile trovare un certificato, tenta di registrarne uno usando il modello.</span><span class="sxs-lookup"><span data-stu-id="d8e44-113">Retrieves an existing certificate by using the name of the template specified on the command line or, if a certificate cannot be found, attempts to enroll one by using the template.</span></span> <span data-ttu-id="d8e44-114">Le funzioni findCertByTemplate e enrollCertByTemplate sono definite in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="d8e44-114">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="d8e44-115">Verifica la catena di certificati e converte il certificato in un **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="d8e44-115">Verifies the certificate chain and converts the certificate to a **BSTR**.</span></span>
4.  <span data-ttu-id="d8e44-116">Crea un oggetto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) e lo inizializza utilizzando il certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="d8e44-116">Creates an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object and initializes it by using the existing certificate.</span></span> <span data-ttu-id="d8e44-117">Poiché il parametro *inheritOptions* è impostato su InheritDefault, viene creata una nuova coppia di chiavi per la richiesta, ma viene utilizzato il provider del sistema di crittografia nel certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="d8e44-117">Because the *inheritOptions* parameter is set to InheritDefault, a new key pair is created for the request but the cryptographic provider in the existing certificate is used.</span></span> <span data-ttu-id="d8e44-118">Per ulteriori informazioni, vedere il metodo [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) .</span><span class="sxs-lookup"><span data-stu-id="d8e44-118">For more information, see the [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) method.</span></span>
5.  <span data-ttu-id="d8e44-119">Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inizializza usando l'oggetto della \# richiesta PKCS 7, tenta di registrarlo con l'autorità di certificazione e monitora lo stato del processo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="d8e44-119">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the PKCS \#7 request object, attempts to enroll it with the CA and monitors the status of the enrollment process.</span></span> <span data-ttu-id="d8e44-120">La funzione checkEnrollStatus è definita in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="d8e44-120">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8e44-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d8e44-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8e44-122">Richiesta CMC</span><span class="sxs-lookup"><span data-stu-id="d8e44-122">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="d8e44-123">\#Richiesta di rinnovo PKCS 7</span><span class="sxs-lookup"><span data-stu-id="d8e44-123">PKCS \#7 Renewal Request</span></span>](pkcs--7--renewal-request.md)
</dt> <dt>

[<span data-ttu-id="d8e44-124">Uso degli esempi inclusi</span><span class="sxs-lookup"><span data-stu-id="d8e44-124">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



