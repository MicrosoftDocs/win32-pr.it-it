---
description: Crea una \# richiesta PKCS 7 da un certificato esistente ereditando le chiavi pubbliche e private e il modello di certificato.
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34bc7f9d7b7d5ae9fa88db0dd70c177c3aa69da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750018"
---
# <a name="enrollpkcs7"></a><span data-ttu-id="63052-103">enrollPKCS7</span><span class="sxs-lookup"><span data-stu-id="63052-103">enrollPKCS7</span></span>

<span data-ttu-id="63052-104">L'esempio enrollPKCS7 crea una \# richiesta PKCS 7 da un certificato esistente ereditando le chiavi pubbliche e private e il modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="63052-104">The enrollPKCS7 sample creates a PKCS \#7 request from an existing certificate by inheriting the public and private keys and the certificate template.</span></span> <span data-ttu-id="63052-105">Il certificato esistente viene usato per firmare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="63052-105">The existing certificate is used to sign the request.</span></span> <span data-ttu-id="63052-106">In questo esempio l'utente viene registrato in una gerarchia di certificati e viene installata la risposta del certificato.</span><span class="sxs-lookup"><span data-stu-id="63052-106">This sample enrolls the user in a certificate hierarchy and installs the certificate response.</span></span> <span data-ttu-id="63052-107">Nell'esempio viene utilizzato un certificato esistente per registrarsi e installarne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="63052-107">The sample uses an existing certificate to enroll and install a new one.</span></span> <span data-ttu-id="63052-108">Per ulteriori informazioni sul rinnovo di un certificato esistente, vedere [enrollRenewalPKCS7](enrollrenewalpkcs7.md).</span><span class="sxs-lookup"><span data-stu-id="63052-108">For more information about renewing an existing certificate, see [enrollRenewalPKCS7](enrollrenewalpkcs7.md).</span></span>

## <a name="location"></a><span data-ttu-id="63052-109">Location</span><span class="sxs-lookup"><span data-stu-id="63052-109">Location</span></span>

<span data-ttu-id="63052-110">Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ enrollPKCS7</span><span class="sxs-lookup"><span data-stu-id="63052-110">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollPKCS7 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="63052-111">Discussione</span><span class="sxs-lookup"><span data-stu-id="63052-111">Discussion</span></span>

<span data-ttu-id="63052-112">Esempio enrollPKCS7:</span><span class="sxs-lookup"><span data-stu-id="63052-112">The enrollPKCS7 sample:</span></span>

1.  <span data-ttu-id="63052-113">Elabora gli argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="63052-113">Processes the command line arguments.</span></span> <span data-ttu-id="63052-114">La riga di comando deve contenere il nome del modello di certificato usato per trovare un certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="63052-114">The command line should contain the name of the certificate template used to find an existing certificate.</span></span>
2.  <span data-ttu-id="63052-115">Recupera un certificato esistente usando il nome del modello specificato nella riga di comando o, se non è possibile trovare un certificato, tenta di registrare un nuovo certificato creato usando il modello.</span><span class="sxs-lookup"><span data-stu-id="63052-115">Retrieves an existing certificate by using the name of the template specified on the command line or, if a certificate cannot be found, attempts to enroll a new one created by using the template.</span></span> <span data-ttu-id="63052-116">Le funzioni findCertByTemplate e enrollCertByTemplate sono definite in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="63052-116">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="63052-117">Verifica la catena di certificati e converte il certificato in un **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="63052-117">Verifies the certificate chain and converts the certificate to a **BSTR**.</span></span>
4.  <span data-ttu-id="63052-118">Crea un oggetto [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) e lo inizializza utilizzando il certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="63052-118">Creates an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object and initializes it by using the existing certificate.</span></span> <span data-ttu-id="63052-119">Il nuovo \# oggetto della richiesta PKCS 7 eredita le chiavi pubbliche e private e il modello dal certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="63052-119">The new PKCS \#7 request object inherits the private and public keys and template from the existing certificate.</span></span>
5.  <span data-ttu-id="63052-120">Crea un oggetto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inizializza usando il certificato esistente e lo aggiunge all'oggetto della richiesta PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="63052-120">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the existing certificate, and adds it to the PKCS \#7 request object.</span></span>
6.  <span data-ttu-id="63052-121">Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inizializza usando l'oggetto della \# richiesta PKCS 7, tenta di registrarlo con l'autorità di certificazione e monitora lo stato del processo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="63052-121">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the PKCS \#7 request object, attempts to enroll it with the CA and monitors the status of the enrollment process.</span></span> <span data-ttu-id="63052-122">La funzione checkEnrollStatus è definita in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="63052-122">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63052-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63052-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63052-124">Richiesta CMC</span><span class="sxs-lookup"><span data-stu-id="63052-124">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="63052-125">Uso degli esempi inclusi</span><span class="sxs-lookup"><span data-stu-id="63052-125">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



