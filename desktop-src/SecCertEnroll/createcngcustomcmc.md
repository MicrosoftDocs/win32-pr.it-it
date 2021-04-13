---
description: Crea un oggetto richiesta CMC da una richiesta PKCS 10 annidata interna \# .
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: createCNGCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669a52901981ea910ee3d1704ba892fb96664470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342731"
---
# <a name="createcngcustomcmc"></a><span data-ttu-id="9083c-103">createCNGCustomCMC</span><span class="sxs-lookup"><span data-stu-id="9083c-103">createCNGCustomCMC</span></span>

<span data-ttu-id="9083c-104">L'esempio createCNGCustomCMC crea un oggetto richiesta CMC da una richiesta PKCS 10 annidata interna \# .</span><span class="sxs-lookup"><span data-stu-id="9083c-104">The createCNGCustomCMC sample creates a CMC request object from an inner nested PKCS \#10 request.</span></span> <span data-ttu-id="9083c-105">La richiesta interna viene creata utilizzando una [*chiave privata*](/windows/desktop/SecGloss/p-gly)asimmetrica.</span><span class="sxs-lookup"><span data-stu-id="9083c-105">The inner request is created by using an asymmetric [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="9083c-106">La chiave privata viene creata usando il provider di crittografia CNG (Cryptography API: Next Generation) e l'algoritmo specificato nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="9083c-106">The private key is created by using the Cryptography API: Next Generation (CNG) cryptographic provider and the algorithm specified on the command line.</span></span> <span data-ttu-id="9083c-107">Per la chiave privata vengono inoltre impostate opzioni personalizzate, ad esempio i criteri di esportazione e il livello di protezione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="9083c-107">Custom options such as export policy and key protection level are also set on the private key.</span></span>

## <a name="location"></a><span data-ttu-id="9083c-108">Location</span><span class="sxs-lookup"><span data-stu-id="9083c-108">Location</span></span>

<span data-ttu-id="9083c-109">Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ createCNGCustomCMC</span><span class="sxs-lookup"><span data-stu-id="9083c-109">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\createCNGCustomCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="9083c-110">Discussione</span><span class="sxs-lookup"><span data-stu-id="9083c-110">Discussion</span></span>

<span data-ttu-id="9083c-111">Esempio createCNGCustomCMC:</span><span class="sxs-lookup"><span data-stu-id="9083c-111">The createCNGCustomCMC sample:</span></span>

1.  <span data-ttu-id="9083c-112">Elabora gli argomenti della riga di comando seguenti:</span><span class="sxs-lookup"><span data-stu-id="9083c-112">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="9083c-113">Nome di un provider del [*servizio di crittografia*](/windows/desktop/SecGloss/c-gly) (CSP) CNG.</span><span class="sxs-lookup"><span data-stu-id="9083c-113">The name of a CNG [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span>
    -   <span data-ttu-id="9083c-114">Nome dell'algoritmo utilizzato per generare una chiave privata asimmetrica.</span><span class="sxs-lookup"><span data-stu-id="9083c-114">The name of the algorithm used to generate an asymmetric private key.</span></span>
    -   <span data-ttu-id="9083c-115">Nome dell'algoritmo utilizzato per eseguire l' [*hashing*](/windows/desktop/SecGloss/h-gly) della [*richiesta di certificato*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="9083c-115">The name of the algorithm used to [*hash*](/windows/desktop/SecGloss/h-gly) the [*certificate request*](/windows/desktop/SecGloss/c-gly).</span></span>
    -   <span data-ttu-id="9083c-116">Un file di output in cui salvare la richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="9083c-116">An output file in which to save the certificate request.</span></span>
    -   <span data-ttu-id="9083c-117">Stringa facoltativa (AlternateSignature) che, se presente, specifica che deve essere utilizzato un algoritmo discreto anziché un algoritmo di firma combinato.</span><span class="sxs-lookup"><span data-stu-id="9083c-117">An optional string (AlternateSignature) which, if present, specifies that a discrete rather than a combined signature algorithm be used.</span></span> <span data-ttu-id="9083c-118">Per ulteriori informazioni, vedere la proprietà [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) .</span><span class="sxs-lookup"><span data-stu-id="9083c-118">For more information, see the [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) property.</span></span>
2.  <span data-ttu-id="9083c-119">Crea un oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) e imposta le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="9083c-119">Creates an [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object and sets the following properties:</span></span>
    -   [<span data-ttu-id="9083c-120">**LegacyCsp**</span><span class="sxs-lookup"><span data-stu-id="9083c-120">**LegacyCsp**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [<span data-ttu-id="9083c-121">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="9083c-121">**ProviderName**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [<span data-ttu-id="9083c-122">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="9083c-122">**Algorithm**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [<span data-ttu-id="9083c-123">**Protezione di dati**</span><span class="sxs-lookup"><span data-stu-id="9083c-123">**KeyProtection**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [<span data-ttu-id="9083c-124">**ExportPolicy**</span><span class="sxs-lookup"><span data-stu-id="9083c-124">**ExportPolicy**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  <span data-ttu-id="9083c-125">Crea una chiave privata asimmetrica.</span><span class="sxs-lookup"><span data-stu-id="9083c-125">Creates an asymmetric private key.</span></span>
4.  <span data-ttu-id="9083c-126">Crea un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e lo inizializza usando la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="9083c-126">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and initializes it by using the private key.</span></span>
5.  <span data-ttu-id="9083c-127">Crea un oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e lo inizializza usando l' \# oggetto richiesta PKCS 10 creato nel passaggio 4.</span><span class="sxs-lookup"><span data-stu-id="9083c-127">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the PKCS \#10 request object created in step 4.</span></span>
6.  <span data-ttu-id="9083c-128">Imposta il flag dell'algoritmo di firma alternativo su **Variant \_ true** o **Variant \_ false** a seconda che nella riga di comando sia specificata una stringa di firma alternativa.</span><span class="sxs-lookup"><span data-stu-id="9083c-128">Sets the alternate signature algorithm flag to **VARIANT\_TRUE** or **VARIANT\_FALSE** depending on whether an alternate signature string is specified on the command line.</span></span> <span data-ttu-id="9083c-129">Per ulteriori informazioni, vedere [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).</span><span class="sxs-lookup"><span data-stu-id="9083c-129">For more information, see [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).</span></span>
7.  <span data-ttu-id="9083c-130">Crea un [*identificatore di oggetto*](/windows/desktop/SecGloss/o-gly) (OID) dell' [*algoritmo hash*](/windows/desktop/SecGloss/h-gly) dal nome dell'algoritmo specificato nella riga di comando e imposta l'OID nell'oggetto della richiesta CMC.</span><span class="sxs-lookup"><span data-stu-id="9083c-130">Creates a [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) from the algorithm name specified on the command line and sets the OID on the CMC request object.</span></span>
8.  <span data-ttu-id="9083c-131">Firma la richiesta di certificato e la codifica usando [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).</span><span class="sxs-lookup"><span data-stu-id="9083c-131">Signs the certificate request and encodes it by using [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).</span></span>
9.  <span data-ttu-id="9083c-132">Recupera una stringa che contiene la richiesta di certificato CMC codificata e la Salva in un file.</span><span class="sxs-lookup"><span data-stu-id="9083c-132">Retrieves a string that contains the encoded CMC certificate request and saves it to a file.</span></span> <span data-ttu-id="9083c-133">La funzione EncodeToFileW è definita in EnrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="9083c-133">The EncodeToFileW function is defined in EnrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9083c-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9083c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9083c-135">Richiesta CMC</span><span class="sxs-lookup"><span data-stu-id="9083c-135">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="9083c-136">\#Richiesta PKCS 10</span><span class="sxs-lookup"><span data-stu-id="9083c-136">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="9083c-137">Uso degli esempi inclusi</span><span class="sxs-lookup"><span data-stu-id="9083c-137">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> <dt>

[<span data-ttu-id="9083c-138">**IX509PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="9083c-138">**IX509PrivateKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
