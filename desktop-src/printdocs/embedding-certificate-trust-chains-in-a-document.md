---
description: In questo argomento viene descritto come incorporare i certificati che costituiscono una catena di certificati in un documento XPS.
ms.assetid: c6aae8ff-2e1e-43de-9105-171e4187d193
title: Incorporare catene di certificati in un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee6476e0c187cf1a62915f0a3ab2b7949586baa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311538"
---
# <a name="embed-certificate-chains-in-a-document"></a><span data-ttu-id="25271-103">Incorporare catene di certificati in un documento</span><span class="sxs-lookup"><span data-stu-id="25271-103">Embed Certificate Chains in a Document</span></span>

<span data-ttu-id="25271-104">In questo argomento viene descritto come incorporare i certificati che costituiscono una catena di certificati in un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="25271-104">This topic describes how to embed the certificates that make up a certificate chain into an XPS document.</span></span> <span data-ttu-id="25271-105">Una catena di certificati è costituita da tutti i certificati, ad eccezione del certificato radice, necessari per certificare il soggetto identificato dal certificato finale.</span><span class="sxs-lookup"><span data-stu-id="25271-105">A certificate chain consists of all the certificates, except the root certificate, that are needed to certify the subject identified by the end certificate.</span></span>

<span data-ttu-id="25271-106">Per incorporare una catena di certificati in un documento XPS, creare innanzitutto la catena di certificati come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="25271-106">To embed a certificate chain into an XPS document, first create the certificate chain as illustrated in the following code example.</span></span>

<span data-ttu-id="25271-107">Il metodo **CreateCertificateChain** nell'esempio di codice accetta *certificateStore* come parametro, ovvero un valore **HCERTSTORE** .</span><span class="sxs-lookup"><span data-stu-id="25271-107">The **CreateCertificateChain** method in the code example accepts *certificateStore* as a parameter, which is an **HCERTSTORE** value.</span></span> <span data-ttu-id="25271-108">Se questo valore è **null**, i certificati verranno recuperati dal server di certificazione del computer client.</span><span class="sxs-lookup"><span data-stu-id="25271-108">If this value is **NULL**, the certificates will be retrieved from the client computer's certificate server.</span></span> <span data-ttu-id="25271-109">Se il valore è l'handle per un archivio certificati, i certificati verranno recuperati da tale archivio a cui fa riferimento *certificateStore* e dal server di certificati del computer client.</span><span class="sxs-lookup"><span data-stu-id="25271-109">If the value is the handle to a certificate store, the certificates will be retrieved from that store referenced by *certificateStore* as well as from the client computer's certificate server.</span></span>


```C++
HRESULT 
CreateCertificateChain (
    __in PCCERT_CONTEXT            certificate,
    __in HCERTSTORE                certificateStore,
    __out PCCERT_CHAIN_CONTEXT* certificateChain
)
{
    HRESULT  hr = S_OK;

    CERT_CHAIN_PARA certificateChainParameters = {0};

    certificateChainParameters.cbSize = sizeof(CERT_CHAIN_PARA);
    certificateChainParameters.RequestedUsage.dwType = USAGE_MATCH_TYPE_AND;

    // CertGetCertificateChain builds a certificate chain that starts 
    //  from the PCCERT_CONTEXT structure provided by the caller.
    //  After the certificate chain has been successfully created, 
    //  then the authenticity of the certificate can be determined 
    //  by examining the errors, if any, that occurred while the chain
    //  was created.
    BOOL successCreatingCertChain = CertGetCertificateChain (
        NULL,
        certificate,
        NULL,
        certificateStore,
        &certificateChainParameters,
        CERT_CHAIN_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT,
        NULL,
        certificateChain);

    if (!successCreatingCertChain)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    return hr;
}
```



<span data-ttu-id="25271-110">Nell'esempio di codice riportato di seguito viene creata una catena di certificati da certificati e quindi tali certificati vengono aggiunti a un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="25271-110">The following code example creates a certificate chain from certificates and then adds these certificates to an XPS document.</span></span> <span data-ttu-id="25271-111">Si noti che [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) crea la catena di certificati in cui il certificato di firma è il primo e il certificato radice è l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="25271-111">Note that [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) creates the certificate chain in which the signing certificate is first and the root certificate is last.</span></span> <span data-ttu-id="25271-112">Il certificato di firma e il certificato radice non sono stati aggiunti in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="25271-112">The signing certificate and the root certificate are not added in this example.</span></span> <span data-ttu-id="25271-113">I certificati di firma verranno aggiunti con una chiamata al metodo [**IXpsSignatureManager:: Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) , che deve essere l'ultimo metodo di firma chiamato sul documento.</span><span class="sxs-lookup"><span data-stu-id="25271-113">The signing certificates will be added with a call to the [**IXpsSignatureManager::Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) method, which should be the last signature method called on the document.</span></span> <span data-ttu-id="25271-114">Il certificato radice non viene aggiunto quando il documento è firmato, perché deve essere fornito dal server di certificati del computer client quando la firma viene convalidata.</span><span class="sxs-lookup"><span data-stu-id="25271-114">The root certificate is not added when the document is signed, because it must be provided by the client computer's certificate server when the signature is validated.</span></span>


```C++
HRESULT
EmbedCertificateChainInXpsPackage (
    __in IXpsSigningOptions *signingOptions,
    __in PCCERT_CONTEXT signingCertificate
)
{
    HRESULT                 hr                           = S_OK;
    PCCERT_CHAIN_CONTEXT    certificateChainContext      = NULL;
    IOpcCertificateSet      *certificateSetToUpdate      = NULL;
    DWORD                   certificateChainContextIndex = 0;

    // Create the entire certificate chain that originates 
    //  from the certificate that is used to sign the XPS document.
    hr = CreateCertificateChain(
        signingCertificate, 
        NULL, 
        &certificateChainContext);

    if (SUCCEEDED(hr))
    {
        // The signing options of an XPS document contain a pointer to 
        //  an IOpcCertificateSet interface that can be retrieved by 
        //  calling the GetCertificateSet method.
        hr = signingOptions->GetCertificateSet(&certificateSetToUpdate);
    }
    if (SUCCEEDED(hr))
    {
        // for each certificate chain context in this certificate...
        for (certificateChainContextIndex = 0; 
             certificateChainContextIndex < certificateChainContext->cChain; 
             certificateChainContextIndex++)
        {
            // inside a certificate chain context, 
            DWORD adjustedSimpleChainStartIndex = 0;
            DWORD adjustedSimpleChainEndIndex = 0;
            DWORD simpleCertChainIndex = 0;
            CERT_SIMPLE_CHAIN  *simpleCertificateChainWithinContext = NULL;

            // get the information about the certificate chain
            //  set the first item in the certificate chain to load
            //  Ignore the first PCCERT_CONTEXT in the first CERT_SIMPLE_CHAIN
            //  because this is the certificate that was used to build
            //  the chain and is already loaded in the document
            if (certificateChainContextIndex == 0)
            {
                adjustedSimpleChainStartIndex = 1;
            }
            else
            {
                adjustedSimpleChainStartIndex = 0;
            }
                    
            //  get the last item in the certificate chain
            simpleCertificateChainWithinContext = 
                certificateChainContext->rgpChain[certificateChainContextIndex];
            adjustedSimpleChainEndIndex = 
                simpleCertificateChainWithinContext->cElement;

            // Ignore the last PCCERT_CONTEXT in the last CERT_SIMPLE_CHAIN
            //  because this is the root certificate that must be retrieved
            //  from the client computer's certificate server.
            if (certificateChainContextIndex == certificateChainContext->cChain - 1)
            {
                if (adjustedSimpleChainEndIndex != 0)
                {
                    adjustedSimpleChainEndIndex = adjustedSimpleChainEndIndex - 1;
                }
            }

            // for each certificate chain in this context...
            for (simpleCertChainIndex = adjustedSimpleChainStartIndex; 
                 simpleCertChainIndex < adjustedSimpleChainEndIndex;
                 simpleCertChainIndex++)
            {
                // Add the certificate to the XPS document.
                PCCERT_CONTEXT certificateToEmbed = 
                    simpleCertificateChainWithinContext->rgpElement[simpleCertChainIndex]->pCertContext;
                if (FAILED(hr = certificateSetToUpdate->Add(certificateToEmbed)))
                {
                    break; // out of for loop with failed hr
                }
            }
        }
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="25271-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="25271-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="25271-116">**Passaggi successivi**</span><span class="sxs-lookup"><span data-stu-id="25271-116">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="25271-117">Caricare un certificato da un file</span><span class="sxs-lookup"><span data-stu-id="25271-117">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="25271-118">Verificare che un certificato supporti un metodo di firma</span><span class="sxs-lookup"><span data-stu-id="25271-118">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="25271-119">Verificare che il sistema supporti un metodo digest</span><span class="sxs-lookup"><span data-stu-id="25271-119">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

<span data-ttu-id="25271-120">**Usato in questo esempio**</span><span class="sxs-lookup"><span data-stu-id="25271-120">**Used in This Example**</span></span>
</dt> <dt>

[<span data-ttu-id="25271-121">**contesto del certificato \_**</span><span class="sxs-lookup"><span data-stu-id="25271-121">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="25271-122">**CertGetCertificateChain**</span><span class="sxs-lookup"><span data-stu-id="25271-122">**CertGetCertificateChain**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[<span data-ttu-id="25271-123">**\_informazioni Oid \_ crypt**</span><span class="sxs-lookup"><span data-stu-id="25271-123">**CRYPT\_OID\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

[<span data-ttu-id="25271-124">**IOpcCertificateSet**</span><span class="sxs-lookup"><span data-stu-id="25271-124">**IOpcCertificateSet**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset)
</dt> <dt>

[<span data-ttu-id="25271-125">**IXpsSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="25271-125">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

<span data-ttu-id="25271-126">**Per ulteriori informazioni**</span><span class="sxs-lookup"><span data-stu-id="25271-126">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="25271-127">API di crittografia</span><span class="sxs-lookup"><span data-stu-id="25271-127">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="25271-128">Funzioni di crittografia</span><span class="sxs-lookup"><span data-stu-id="25271-128">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="25271-129">Certificati digitali</span><span class="sxs-lookup"><span data-stu-id="25271-129">Digital Certificates</span></span>](/windows/desktop/SecCrypto/digital-certificates)
</dt> <dt>

[<span data-ttu-id="25271-130">Catene di certificati</span><span class="sxs-lookup"><span data-stu-id="25271-130">Certificate Chains</span></span>](/windows/desktop/SecCrypto/certificate-chains)
</dt> <dt>

[<span data-ttu-id="25271-131">Verifica dell'attendibilità del certificato</span><span class="sxs-lookup"><span data-stu-id="25271-131">Certificate Trust Verification</span></span>](/windows/desktop/SecCrypto/certificate-trust-verification)
</dt> <dt>

[<span data-ttu-id="25271-132">Errori dell'API firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="25271-132">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="25271-133">Errori del documento XPS</span><span class="sxs-lookup"><span data-stu-id="25271-133">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="25271-134">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="25271-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
