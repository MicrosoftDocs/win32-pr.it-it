---
description: Consente di creare una richiesta di certificato CMC e di registrare un computer in una gerarchia di certificati.
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: enrollCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2910e6a6ca784aaeb9ca97dc8de106932bd64c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752735"
---
# <a name="enrollcustomcmc"></a><span data-ttu-id="dc2bd-103">enrollCustomCMC</span><span class="sxs-lookup"><span data-stu-id="dc2bd-103">enrollCustomCMC</span></span>

<span data-ttu-id="dc2bd-104">Nell'esempio enrollCustomCMC viene creata una richiesta di certificato CMC e viene registrato un computer in una gerarchia di certificati.</span><span class="sxs-lookup"><span data-stu-id="dc2bd-104">The enrollCustomCMC sample creates a CMC certificate request and enrolls a computer in a certificate hierarchy.</span></span>

## <a name="location"></a><span data-ttu-id="dc2bd-105">Location</span><span class="sxs-lookup"><span data-stu-id="dc2bd-105">Location</span></span>

<span data-ttu-id="dc2bd-106">Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ enrollCustomCMC</span><span class="sxs-lookup"><span data-stu-id="dc2bd-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCustomCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="dc2bd-107">Discussione</span><span class="sxs-lookup"><span data-stu-id="dc2bd-107">Discussion</span></span>

<span data-ttu-id="dc2bd-108">Esempio enrollCustomCMC:</span><span class="sxs-lookup"><span data-stu-id="dc2bd-108">The enrollCustomCMC sample:</span></span>

1.  <span data-ttu-id="dc2bd-109">Elabora gli argomenti della riga di comando seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc2bd-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="dc2bd-110">Coppia nome/valore personalizzata da aggiungere alla richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="dc2bd-110">A custom name/value pair to add to the certificate request.</span></span>
    -   <span data-ttu-id="dc2bd-111">Nome soggetto alternativo.</span><span class="sxs-lookup"><span data-stu-id="dc2bd-111">An alternative subject name.</span></span>
    -   <span data-ttu-id="dc2bd-112">Identificatore di oggetto (OID) per l'estensione utilizzo chiavi avanzato (EKU).</span><span class="sxs-lookup"><span data-stu-id="dc2bd-112">An object identifier (OID) for the Enhanced Key Usage (EKU) extension.</span></span>
2.  <span data-ttu-id="dc2bd-113">Crea un oggetto richiesta [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e lo inizializza usando il contesto del computer.</span><span class="sxs-lookup"><span data-stu-id="dc2bd-113">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) request object and initializes it by using the computer context.</span></span>
3.  <span data-ttu-id="dc2bd-114">Usa la \# richiesta PKCS 10 per inizializzare un oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="dc2bd-114">Uses the PKCS \#10 request to initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
4.  <span data-ttu-id="dc2bd-115">Crea un oggetto [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) usando l'OID specificato nella riga di comando e lo aggiunge alla raccolta Extensions per la richiesta CMC.</span><span class="sxs-lookup"><span data-stu-id="dc2bd-115">Creates an [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) object by using the OID specified on the command line and adds it to the extensions collection for the CMC request.</span></span>
5.  <span data-ttu-id="dc2bd-116">Crea l'oggetto [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) usando il nome specificato nella riga di comando, lo aggiunge alla raccolta [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) , usa la raccolta per inizializzare un'estensione [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) e la aggiunge alla raccolta Extensions per la richiesta CMC.</span><span class="sxs-lookup"><span data-stu-id="dc2bd-116">Creates [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) object by using the name specified on the command line, adds it to the [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) collection, uses the collection to initialize an [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) extension and adds this to the extensions collection for the CMC request.</span></span>
6.  <span data-ttu-id="dc2bd-117">Crea un oggetto [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) usando il nome e il valore specificati nella riga di comando e lo aggiunge alla raccolta [**IX509NAMEVALUEPAIRS**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) nella richiesta CMC.</span><span class="sxs-lookup"><span data-stu-id="dc2bd-117">Creates an [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) object by using the name and value specified on the command line, and adds it to the [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) collection on the CMC request.</span></span>
7.  <span data-ttu-id="dc2bd-118">Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inizializza usando l'oggetto della richiesta CMC e recupera una stringa che contiene una richiesta con codifica Base64.</span><span class="sxs-lookup"><span data-stu-id="dc2bd-118">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request object, and retrieves a string that contains a base64-encoded request.</span></span>
8.  <span data-ttu-id="dc2bd-119">Crea un oggetto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e lo usa per recuperare una stringa che contiene la configurazione della CA.</span><span class="sxs-lookup"><span data-stu-id="dc2bd-119">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and use it to retrieve a string that contains the CA configuration.</span></span>
9.  <span data-ttu-id="dc2bd-120">Crea un oggetto CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) e lo usa più le stringhe che contengono la configurazione della CA e la richiesta di certificato per inviare la richiesta all'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="dc2bd-120">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
10. <span data-ttu-id="dc2bd-121">Controlla lo stato dell'invio e, in caso di esito positivo, installa il certificato nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="dc2bd-121">Checks the submission status and, if successful, installs the certificate to the certificate store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc2bd-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc2bd-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc2bd-123">Richiesta CMC</span><span class="sxs-lookup"><span data-stu-id="dc2bd-123">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="dc2bd-124">\#Richiesta PKCS 10</span><span class="sxs-lookup"><span data-stu-id="dc2bd-124">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="dc2bd-125">Uso degli esempi inclusi</span><span class="sxs-lookup"><span data-stu-id="dc2bd-125">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
