---
description: Inizializza un \# oggetto richiesta di certificato PKCS 10, ne esegue il wrapping in un oggetto richiesta CMC, Invia la richiesta CMC a un'autorità di certificazione dell'organizzazione (Enterprise) e salva il certificato restituito dalla CA in un file.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: enrollFromPublicKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b336d04727f4bb4b90674bad6bb6c429465a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752727"
---
# <a name="enrollfrompublickey"></a><span data-ttu-id="7430a-103">enrollFromPublicKey</span><span class="sxs-lookup"><span data-stu-id="7430a-103">enrollFromPublicKey</span></span>

<span data-ttu-id="7430a-104">Nell'esempio enrollFromPublicKey viene inizializzato un \# oggetto richiesta di certificato PKCS 10, ne viene eseguito il wrapping in un oggetto richiesta CMC, viene inviata la richiesta CMC a un'autorità di certificazione dell'organizzazione (Enterprise) e il certificato restituito dalla CA viene salvato in un file.</span><span class="sxs-lookup"><span data-stu-id="7430a-104">The enrollFromPublicKey sample initializes a PKCS \#10 certificate request object, wraps it in a CMC request object, submits the CMC request to an enterprise certification authority (CA), and saves the certificate returned by the CA in a file.</span></span>

## <a name="location"></a><span data-ttu-id="7430a-105">Location</span><span class="sxs-lookup"><span data-stu-id="7430a-105">Location</span></span>

<span data-ttu-id="7430a-106">Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ enrollFromPublicKey</span><span class="sxs-lookup"><span data-stu-id="7430a-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollFromPublicKey folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="7430a-107">Discussione</span><span class="sxs-lookup"><span data-stu-id="7430a-107">Discussion</span></span>

<span data-ttu-id="7430a-108">Esempio enrollFromPublicKey:</span><span class="sxs-lookup"><span data-stu-id="7430a-108">The enrollFromPublicKey sample:</span></span>

1.  <span data-ttu-id="7430a-109">Elabora gli argomenti della riga di comando seguenti:</span><span class="sxs-lookup"><span data-stu-id="7430a-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="7430a-110">Nome di un modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="7430a-110">The name of a certificate template.</span></span>
    -   <span data-ttu-id="7430a-111">Nome di un file in cui salvare il certificato installato come matrice di byte con codifica Base64.</span><span class="sxs-lookup"><span data-stu-id="7430a-111">The name of a file in which to save the installed certificate as a base64-encoded byte array.</span></span>
    -   <span data-ttu-id="7430a-112">Nome facoltativo del modello di certificato di firma.</span><span class="sxs-lookup"><span data-stu-id="7430a-112">An optional signing certificate template name.</span></span> <span data-ttu-id="7430a-113">Il modello viene usato per creare un certificato di firma, se non ne esiste alcuno nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="7430a-113">The template is used to create a signing certificate if none exists in the certificate store.</span></span>
2.  <span data-ttu-id="7430a-114">Crea un oggetto chiave privata [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) e chiama il metodo [**create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) per creare una chiave privata asimmetrica usando i valori predefiniti del [**provider di crittografia**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) , della chiave e della chiave per il computer corrente.</span><span class="sxs-lookup"><span data-stu-id="7430a-114">Creates an [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) private key object and calls the [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) method to create an asymmetric private key using the default cryptographic provider, key size, and [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) values for the current computer.</span></span>
3.  <span data-ttu-id="7430a-115">Recupera la parte della chiave pubblica dell'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) .</span><span class="sxs-lookup"><span data-stu-id="7430a-115">Retrieves the public key portion of the [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object.</span></span>
4.  <span data-ttu-id="7430a-116">Crea un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e lo inizializza usando il modello specificato nella riga di comando e la chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="7430a-116">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and initializes it by using the template specified on the command line and the public key.</span></span>
5.  <span data-ttu-id="7430a-117">Crea un oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e lo inizializza usando l' \# oggetto richiesta PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="7430a-117">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the PKCS \#10 request object.</span></span>
6.  <span data-ttu-id="7430a-118">Recupera un certificato di firma esistente o, se non è possibile trovarne uno, crea una richiesta di certificato dal modello specificato nella riga di comando e tenta di registrarla.</span><span class="sxs-lookup"><span data-stu-id="7430a-118">Retrieves an existing signing certificate or, if one cannot be found, creates a certificate request from the template specified on the command line and attempts to enroll it.</span></span> <span data-ttu-id="7430a-119">FindCertByKeyUsage è definito in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="7430a-119">The findCertByKeyUsage is defined in enrollCommon.cpp.</span></span>
7.  <span data-ttu-id="7430a-120">Verifica la catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="7430a-120">Verifies the certificate chain.</span></span>
8.  <span data-ttu-id="7430a-121">Crea un oggetto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inizializza usando il certificato di firma, recupera la raccolta [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) dall'oggetto della richiesta CMC e aggiunge l'oggetto certificato di firma alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="7430a-121">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the signing certificate, retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the CMC request object, and adds the signing certificate object to the collection.</span></span>
9.  <span data-ttu-id="7430a-122">Codifica la richiesta CMC usando [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).</span><span class="sxs-lookup"><span data-stu-id="7430a-122">Encodes the CMC request by using [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).</span></span>
10. <span data-ttu-id="7430a-123">Crea un oggetto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e lo usa per recuperare una stringa che contiene la configurazione della CA.</span><span class="sxs-lookup"><span data-stu-id="7430a-123">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and uses it to retrieve a string that contains the CA configuration.</span></span>
11. <span data-ttu-id="7430a-124">Crea un oggetto CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) e lo usa più le stringhe che contengono la configurazione della CA e la richiesta di certificato per inviare la richiesta all'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="7430a-124">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
12. <span data-ttu-id="7430a-125">Controlla lo stato del processo di registrazione e salva il certificato installato in un file.</span><span class="sxs-lookup"><span data-stu-id="7430a-125">Checks the status of the enrollment process and saves the installed certificate to a file.</span></span> <span data-ttu-id="7430a-126">La funzione EncodeToFileW è definita in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="7430a-126">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7430a-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7430a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7430a-128">Richiesta CMC</span><span class="sxs-lookup"><span data-stu-id="7430a-128">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="7430a-129">\#Richiesta PKCS 10</span><span class="sxs-lookup"><span data-stu-id="7430a-129">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="7430a-130">Uso degli esempi inclusi</span><span class="sxs-lookup"><span data-stu-id="7430a-130">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
