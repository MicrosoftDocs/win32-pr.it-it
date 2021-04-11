---
description: Legge una richiesta di certificato CMC esistente da un file, ne esegue il wrapping in un'altra richiesta CMC, firma questa richiesta esterna, la invia a un'autorità di certificazione (CA) e salva la risposta del certificato dalla CA a un file.
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: enrollNestedCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1df25a1bc7f6ce16a67f66ff58dc371a526813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225898"
---
# <a name="enrollnestedcmc"></a><span data-ttu-id="6faae-103">enrollNestedCMC</span><span class="sxs-lookup"><span data-stu-id="6faae-103">enrollNestedCMC</span></span>

<span data-ttu-id="6faae-104">L'esempio enrollNestedCMC legge una richiesta di certificato CMC esistente da un file, ne esegue il wrapping in un'altra richiesta CMC, firma questa richiesta esterna, la invia a un'autorità di certificazione (CA) e salva la risposta del certificato dalla CA a un file.</span><span class="sxs-lookup"><span data-stu-id="6faae-104">The enrollNestedCMC sample reads an existing CMC certificate request from a file, wraps it in another CMC request, signs this outer request, submits it to a certification authority (CA), and saves the certificate response from the CA to a file.</span></span>

## <a name="location"></a><span data-ttu-id="6faae-105">Location</span><span class="sxs-lookup"><span data-stu-id="6faae-105">Location</span></span>

<span data-ttu-id="6faae-106">Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ X509 registrazione certificati \\ VC \\ enrollNestedCMC</span><span class="sxs-lookup"><span data-stu-id="6faae-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\X509 Certificate Enrollment\\VC\\enrollNestedCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="6faae-107">Discussione</span><span class="sxs-lookup"><span data-stu-id="6faae-107">Discussion</span></span>

<span data-ttu-id="6faae-108">Esempio enrollNestedCMC:</span><span class="sxs-lookup"><span data-stu-id="6faae-108">The enrollNestedCMC sample:</span></span>

1.  <span data-ttu-id="6faae-109">Elabora gli argomenti della riga di comando seguenti:</span><span class="sxs-lookup"><span data-stu-id="6faae-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="6faae-110">Nome del file di input.</span><span class="sxs-lookup"><span data-stu-id="6faae-110">The name of the input file.</span></span>
    -   <span data-ttu-id="6faae-111">Nome del file di output.</span><span class="sxs-lookup"><span data-stu-id="6faae-111">The name of the output file.</span></span>
    -   <span data-ttu-id="6faae-112">Modello di richiesta facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6faae-112">An optional request template.</span></span>
2.  <span data-ttu-id="6faae-113">Legge una richiesta CMC esistente da un file come matrice di byte codificata in base63, converte la matrice di byte in un **BSTR**, crea un oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e USA **BSTR** per inizializzare l'oggetto Request.</span><span class="sxs-lookup"><span data-stu-id="6faae-113">Reads an existing CMC request from a file as a base63-encoded byte array, converts the byte array to a **BSTR**, creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object, and uses the **BSTR** to initialize the request object.</span></span> <span data-ttu-id="6faae-114">L'oggetto inizializzato diventa la richiesta interna.</span><span class="sxs-lookup"><span data-stu-id="6faae-114">The initialized object becomes the inner request.</span></span>
3.  <span data-ttu-id="6faae-115">Usa l'oggetto richiesta interno creato e inizializzato nel passaggio precedente per inizializzare un'altra richiesta CMC.</span><span class="sxs-lookup"><span data-stu-id="6faae-115">Uses the inner request object created and initialized in the preceding step to initialize another CMC request.</span></span>
4.  <span data-ttu-id="6faae-116">Recupera un certificato di firma esistente o, se non è possibile trovarne uno, crea una richiesta di certificato dal modello specificato nella riga di comando e tenta di registrarla.</span><span class="sxs-lookup"><span data-stu-id="6faae-116">Retrieves an existing signing certificate or, if one cannot be found, creates a certificate request from the template specified on the command line and attempts to enroll it.</span></span> <span data-ttu-id="6faae-117">Le funzioni findCertByTemplate e enrollCertByTemplate sono definite in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="6faae-117">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
5.  <span data-ttu-id="6faae-118">Recupera la raccolta [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) dalla richiesta CMC esterna, crea un nuovo oggetto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inizializza usando il certificato di firma recuperato e lo aggiunge alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="6faae-118">Retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the outer CMC request, creates a new [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the retrieved signing certificate, and adds it to the collection.</span></span>
6.  <span data-ttu-id="6faae-119">Codifica la richiesta CMC usando Distinguished Encoding Rules (DER) e recupera la richiesta come **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="6faae-119">Encodes the CMC request by using Distinguished Encoding Rules (DER) and retrieves the request as a **BSTR**.</span></span>
7.  <span data-ttu-id="6faae-120">Crea un oggetto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e lo usa per recuperare una stringa che contiene la configurazione della CA.</span><span class="sxs-lookup"><span data-stu-id="6faae-120">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and use it to retrieve a string that contains the CA configuration.</span></span>
8.  <span data-ttu-id="6faae-121">Crea un oggetto CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) e lo usa più le stringhe che contengono la configurazione della CA e la richiesta di certificato per inviare la richiesta all'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="6faae-121">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
9.  <span data-ttu-id="6faae-122">Controlla lo stato del processo di registrazione e salva la risposta del certificato dalla CA in un file.</span><span class="sxs-lookup"><span data-stu-id="6faae-122">Checks the status of the enrollment process and saves the certificate response from the CA to a file.</span></span> <span data-ttu-id="6faae-123">La funzione EncodeToFileW è definita in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="6faae-123">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6faae-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6faae-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6faae-125">Richiesta CMC</span><span class="sxs-lookup"><span data-stu-id="6faae-125">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="6faae-126">Uso degli esempi inclusi</span><span class="sxs-lookup"><span data-stu-id="6faae-126">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
