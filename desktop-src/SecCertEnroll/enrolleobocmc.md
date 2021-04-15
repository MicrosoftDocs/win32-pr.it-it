---
description: Consente di creare una richiesta di certificato CMC per conto di un altro utente e di registrare l'utente in una gerarchia di certificati.
ms.assetid: 14cc76c9-0e2b-498f-b058-244af6e9111e
title: enrollEOBOCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca888d949054d695056d42045335f17dfca2f4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526994"
---
# <a name="enrolleobocmc"></a><span data-ttu-id="e3ca7-103">enrollEOBOCMC</span><span class="sxs-lookup"><span data-stu-id="e3ca7-103">enrollEOBOCMC</span></span>

<span data-ttu-id="e3ca7-104">L'esempio enrollEOBOCMC consente di creare una richiesta di certificato CMC per conto di un altro utente e di registrare l'utente in una gerarchia di certificati.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-104">The enrollEOBOCMC sample creates a CMC certificate request on behalf of another user and enrolls the user in a certificate hierarchy.</span></span> <span data-ttu-id="e3ca7-105">Per conto di un altro utente, la registrazione richiede che la richiesta di certificato venga firmata utilizzando un certificato dell'agente di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-105">Enrollment on behalf of another user requires that the certificate request be signed by using an enrollment agent certificate.</span></span>

## <a name="location"></a><span data-ttu-id="e3ca7-106">Location</span><span class="sxs-lookup"><span data-stu-id="e3ca7-106">Location</span></span>

<span data-ttu-id="e3ca7-107">Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ enrollEOBOCMC</span><span class="sxs-lookup"><span data-stu-id="e3ca7-107">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollEOBOCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="e3ca7-108">Discussione</span><span class="sxs-lookup"><span data-stu-id="e3ca7-108">Discussion</span></span>

<span data-ttu-id="e3ca7-109">Esempio enrollEOBOCMC:</span><span class="sxs-lookup"><span data-stu-id="e3ca7-109">The enrollEOBOCMC sample:</span></span>

1.  <span data-ttu-id="e3ca7-110">Elabora gli argomenti della riga di comando seguenti:</span><span class="sxs-lookup"><span data-stu-id="e3ca7-110">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="e3ca7-111">Nome di un modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-111">The name of a certificate template.</span></span>
    -   <span data-ttu-id="e3ca7-112">Nome dell'utente che ha richiesto il certificato.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-112">The name of the user requesting the certificate.</span></span>
    -   <span data-ttu-id="e3ca7-113">Nome di un file PFX (Personal Information Exchange) in cui salvare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-113">The name of a Personal Information Exchange (PFX) file in which to save the request.</span></span>
    -   <span data-ttu-id="e3ca7-114">Password da utilizzare con il file PFX.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-114">A password to use with the PFX file.</span></span>
    -   <span data-ttu-id="e3ca7-115">Nome del modello di agente di registrazione facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-115">An optional enrollment agent template name.</span></span> <span data-ttu-id="e3ca7-116">Il modello viene usato per creare un certificato dell'agente di registrazione, se non ne esiste alcuno nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-116">The template is used to create an enrollment agent certificate if none exists in the certificate store.</span></span>
2.  <span data-ttu-id="e3ca7-117">Crea un oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e lo inizializza usando il modello di certificato specificato nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-117">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the certificate template specified on the command line.</span></span>
3.  <span data-ttu-id="e3ca7-118">Aggiunge il nome del richiedente all'oggetto della richiesta CMC.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-118">Adds the name of the requester to the CMC request object.</span></span>
4.  <span data-ttu-id="e3ca7-119">Recupera un certificato dell'agente di registrazione esistente o, se non è possibile trovarne uno, crea una richiesta di certificato dal modello dell'agente di registrazione specificato nella riga di comando e tenta di registrarla.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-119">Retrieves an existing enrollment agent certificate or, if one cannot be found, creates a certificate request from the enrollment agent template specified on the command line and attempts to enroll it.</span></span>
5.  <span data-ttu-id="e3ca7-120">Verifica la catena di certificati che contiene il certificato dell'agente di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-120">Verifies the certificate chain that contains the enrollment agent certificate.</span></span>
6.  <span data-ttu-id="e3ca7-121">Crea un oggetto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inizializza usando il certificato dell'agente di registrazione, recupera la raccolta [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) dall'oggetto della richiesta CMC e aggiunge l'oggetto certificato di firma dell'agente di registrazione alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-121">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the enrollment agent certificate, retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the CMC request object, and adds the enrollment agent signing certificate object to the collection.</span></span> <span data-ttu-id="e3ca7-122">L'oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) illustrato nel passaggio successivo usa il certificato per firmare la richiesta CMC.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-122">The [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object discussed in the next step uses the certificate to sign the CMC request.</span></span>
7.  <span data-ttu-id="e3ca7-123">Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inizializza usando la richiesta CMC, tenta di registrarlo e controlla lo stato di avanzamento del processo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-123">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request, attempts to enroll it, and checks the progress of the enrollment process.</span></span>
8.  <span data-ttu-id="e3ca7-124">Esporta il certificato installato in un file PFX.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-124">Exports the installed certificate to a PFX file.</span></span> <span data-ttu-id="e3ca7-125">Il file è protetto tramite la password specificata nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-125">The file is protected by using the password specified on the command line.</span></span> <span data-ttu-id="e3ca7-126">La funzione EncodeToFileW è definita in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-126">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>
9.  <span data-ttu-id="e3ca7-127">Elimina il certificato dall'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-127">Deletes the certificate from the certificate store.</span></span> <span data-ttu-id="e3ca7-128">Le funzioni usate nell'esempio di codice seguente sono reperibili nella documentazione di CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-128">The functions used in the following code example can be found in the CryptoAPI documentation.</span></span>
10. <span data-ttu-id="e3ca7-129">Elimina la chiave privata dal computer.</span><span class="sxs-lookup"><span data-stu-id="e3ca7-129">Deletes the private key from the computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3ca7-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e3ca7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3ca7-131">Richiesta EOBO di CMC</span><span class="sxs-lookup"><span data-stu-id="e3ca7-131">CMC EOBO Request</span></span>](cmc-eobo-request.md)
</dt> <dt>

[<span data-ttu-id="e3ca7-132">\#Richiesta PKCS 10</span><span class="sxs-lookup"><span data-stu-id="e3ca7-132">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="e3ca7-133">Uso degli esempi inclusi</span><span class="sxs-lookup"><span data-stu-id="e3ca7-133">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



