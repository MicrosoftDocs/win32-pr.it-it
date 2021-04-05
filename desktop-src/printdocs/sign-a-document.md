---
description: In questo argomento viene descritto come firmare un documento XPS.
ms.assetid: fbe64aed-6b07-49de-910c-18be68cb65a2
title: Firmare un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4ad07323a26d21f9010c3fd54c708880b90173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881390"
---
# <a name="sign-a-document"></a><span data-ttu-id="24ee2-103">Firmare un documento</span><span class="sxs-lookup"><span data-stu-id="24ee2-103">Sign a Document</span></span>

<span data-ttu-id="24ee2-104">In questo argomento viene descritto come firmare un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="24ee2-104">This topic describes how to sign an XPS document.</span></span>

<span data-ttu-id="24ee2-105">Prima di usare gli esempi di codice seguenti nel programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione della firma digitale](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="24ee2-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="24ee2-106">Per firmare un documento XPS, caricarlo prima in un gestore delle firme come descritto in [inizializzazione di gestione firme](initialize-the-signature-manager.md).</span><span class="sxs-lookup"><span data-stu-id="24ee2-106">To sign an XPS document, first load it into a signature manager as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>

<span data-ttu-id="24ee2-107">Per firmare un documento che è stato caricato in un gestore delle firme:</span><span class="sxs-lookup"><span data-stu-id="24ee2-107">To sign a document that has been loaded into a signature manager:</span></span>

1.  <span data-ttu-id="24ee2-108">Creare un'istanza di un'interfaccia [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) .</span><span class="sxs-lookup"><span data-stu-id="24ee2-108">Instantiate an [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) interface.</span></span>
2.  <span data-ttu-id="24ee2-109">Impostare i criteri di firma.</span><span class="sxs-lookup"><span data-stu-id="24ee2-109">Set the signing policy.</span></span>
3.  <span data-ttu-id="24ee2-110">Impostare il metodo di firma.</span><span class="sxs-lookup"><span data-stu-id="24ee2-110">Set the signature method.</span></span> <span data-ttu-id="24ee2-111">Le costanti di stringa URI del metodo Signature sono definite in cryptxml. h.</span><span class="sxs-lookup"><span data-stu-id="24ee2-111">Signature method URI string constants are defined in cryptxml.h.</span></span> <span data-ttu-id="24ee2-112">Per ulteriori informazioni sui valori validi per il metodo di firma, vedere [**IXpsSigningOptions:: SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).</span><span class="sxs-lookup"><span data-stu-id="24ee2-112">For more information about valid signature method values, see [**IXpsSigningOptions::SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).</span></span>
4.  <span data-ttu-id="24ee2-113">Impostare il metodo digest.</span><span class="sxs-lookup"><span data-stu-id="24ee2-113">Set the digest method.</span></span> <span data-ttu-id="24ee2-114">Le costanti di stringa URI del metodo digest sono definite in cryptxml. h.</span><span class="sxs-lookup"><span data-stu-id="24ee2-114">Digest method URI string constants are defined in cryptxml.h.</span></span> <span data-ttu-id="24ee2-115">Per informazioni sui valori validi dei metodi digest, vedere [**IXpsSigningOptions:: SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).</span><span class="sxs-lookup"><span data-stu-id="24ee2-115">For information about valid digest method values, see [**IXpsSigningOptions::SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).</span></span>
5.  <span data-ttu-id="24ee2-116">Caricare il certificato come descritto in [caricare un certificato da un file](load-a-certificate-from-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="24ee2-116">Load the certificate as described in [Load a Certificate From a File](load-a-certificate-from-a-file.md).</span></span>
6.  <span data-ttu-id="24ee2-117">Verificare che il certificato supporti il metodo di firma, come descritto in [verificare che un certificato supporti un metodo di firma](verify-a-certificate-supports-a-signature-method.md).</span><span class="sxs-lookup"><span data-stu-id="24ee2-117">Verify that the certificate supports the signature method, as described in [Verify That a Certificate Supports a Signature Method](verify-a-certificate-supports-a-signature-method.md).</span></span>
7.  <span data-ttu-id="24ee2-118">Verificare che il metodo digest sia supportato dal sistema, come descritto in [verificare che il sistema supporti un metodo digest](verify-a-certificate-supports-a-digest-method.md).</span><span class="sxs-lookup"><span data-stu-id="24ee2-118">Verify that the digest method is supported by the system, as described in [Verify the System Supports a Digest Method](verify-a-certificate-supports-a-digest-method.md).</span></span>
8.  <span data-ttu-id="24ee2-119">Se necessario, incorporare i certificati della catena di certificati attendibili nel documento XPS come descritto in [incorporare le catene di certificati in un documento](embedding-certificate-trust-chains-in-a-document.md).</span><span class="sxs-lookup"><span data-stu-id="24ee2-119">If required, embed the certificates of the certificate trust chain in the XPS document as described in [Embed Certificate Chains in a Document](embedding-certificate-trust-chains-in-a-document.md).</span></span>
9.  <span data-ttu-id="24ee2-120">Firmare il documento XPS.</span><span class="sxs-lookup"><span data-stu-id="24ee2-120">Sign the XPS document.</span></span>

<span data-ttu-id="24ee2-121">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare i passaggi precedenti in un programma.</span><span class="sxs-lookup"><span data-stu-id="24ee2-121">The following code example illustrates how to use the preceding steps in a program.</span></span>


```C++
    // this example requires:
    //        cryptxml.h
    // and refers to local methods that are described
    // in other topics

    HRESULT                hr               = S_OK;
    BOOL                   supported        = FALSE;
    BOOL                   succeeded        = FALSE;
    IXpsSigningOptions     *signingOptions  = NULL;
    IXpsSignature          *signature       = NULL;
    PCCERT_CONTEXT         certificate      = NULL;
    
    // Instantiate an IXpsSigningOptions interface.
    hr = signatureManager->CreateSigningOptions (&signingOptions);
    
    if (SUCCEEDED(hr)) {
        // Set the signing policy to indicate the document parts 
        //  to sign.
        hr = signingOptions->SetPolicy (XPS_SIGN_POLICY_CORE_PROPERTIES);
    }

    if (SUCCEEDED(hr)) {
        // Set the digital signature method to use to generate the 
        //    signature hash value. 
        //
        // The signature method used in this example is 
        //    defined in cryptxml.h.
        hr = signingOptions->SetSignatureMethod (
            wszURI_XMLNS_DIGSIG_RSA_SHA1);
    }

    if (SUCCEEDED(hr)) {
        // Set the digest method to use.
        //
        // The digest method used in this example is 
        //    defined in cryptxml.h.
        hr = signingOptions->SetDigestMethod (wszURI_XMLNS_DIGSIG_SHA1);
    }

    if (SUCCEEDED(hr)) {
        // Load a certificate from a certificate file
        hr = LoadCertificateFromFile (signingCertificate, &certificate);
    }

    if (SUCCEEDED(hr)) {
        // Verify the certificate supports the digest method
        supported = SupportsDigestAlgorithm (
            wszURI_XMLNS_DIGSIG_SHA1);
        if (!supported) hr = E_FAIL;
    }

    if (SUCCEEDED(hr)) {
        // Verify the signature method is supported by the certificate
        //  and the system
        supported = SupportsSignatureAlgorithm(
            wszURI_XMLNS_DIGSIG_RSA_SHA1, certificate);
        if (!supported) hr = E_FAIL;
    }

    if (SUCCEEDED(hr)) {
        // Embed the certificate trust chain in the XPS package (optional).
        hr = EmbedCertificateChainInXpsPackage (signingOptions, certificate);
    }

    if (SUCCEEDED(hr)) {
        // Sign the XPS document
        hr = signatureManager->Sign (signingOptions, certificate, &signature);
    }

 //<Free the certificate context
    if (NULL != certificate) CertFreeCertificateContext (certificate);

    if (NULL != signingOptions) signingOptions->Release();
    if (NULL != signature) signature->Release();
```



## <a name="related-topics"></a><span data-ttu-id="24ee2-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24ee2-122">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="24ee2-123">**Passaggi successivi**</span><span class="sxs-lookup"><span data-stu-id="24ee2-123">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="24ee2-124">Aggiungere una richiesta di firma a un documento XPS</span><span class="sxs-lookup"><span data-stu-id="24ee2-124">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
</dt> <dt>

[<span data-ttu-id="24ee2-125">Verificare le firme del documento</span><span class="sxs-lookup"><span data-stu-id="24ee2-125">Verify Document Signatures</span></span>](verify-document-signatures.md)
</dt> <dt>

<span data-ttu-id="24ee2-126">**Usato in questa sezione**</span><span class="sxs-lookup"><span data-stu-id="24ee2-126">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="24ee2-127">**CertFreeCertificateContext**</span><span class="sxs-lookup"><span data-stu-id="24ee2-127">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[<span data-ttu-id="24ee2-128">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="24ee2-128">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="24ee2-129">**IXpsSignatureManager::CreateSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="24ee2-129">**IXpsSignatureManager::CreateSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions)
</dt> <dt>

[<span data-ttu-id="24ee2-130">**IXpsSignatureManager:: Sign**</span><span class="sxs-lookup"><span data-stu-id="24ee2-130">**IXpsSignatureManager::Sign**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign)
</dt> <dt>

[<span data-ttu-id="24ee2-131">**IXpsSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="24ee2-131">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

[<span data-ttu-id="24ee2-132">**IXpsSigningOptions::SetDigestMethod**</span><span class="sxs-lookup"><span data-stu-id="24ee2-132">**IXpsSigningOptions::SetDigestMethod**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
</dt> <dt>

[<span data-ttu-id="24ee2-133">**IXpsSigningOptions:: sepolicy**</span><span class="sxs-lookup"><span data-stu-id="24ee2-133">**IXpsSigningOptions::SetPolicy**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy)
</dt> <dt>

[<span data-ttu-id="24ee2-134">**IXpsSigningOptions::SetSignatureMethod**</span><span class="sxs-lookup"><span data-stu-id="24ee2-134">**IXpsSigningOptions::SetSignatureMethod**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
</dt> <dt>

[<span data-ttu-id="24ee2-135">**\_criteri di firma XPS \_**</span><span class="sxs-lookup"><span data-stu-id="24ee2-135">**XPS\_SIGN\_POLICY**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

<span data-ttu-id="24ee2-136">**Per ulteriori informazioni**</span><span class="sxs-lookup"><span data-stu-id="24ee2-136">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="24ee2-137">API di crittografia</span><span class="sxs-lookup"><span data-stu-id="24ee2-137">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="24ee2-138">Funzioni di crittografia</span><span class="sxs-lookup"><span data-stu-id="24ee2-138">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="24ee2-139">Caricare un certificato da un file</span><span class="sxs-lookup"><span data-stu-id="24ee2-139">Load a Certificate From a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="24ee2-140">Verificare che un certificato supporti un metodo di firma</span><span class="sxs-lookup"><span data-stu-id="24ee2-140">Verify a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="24ee2-141">Verificare che il sistema supporti un metodo digest</span><span class="sxs-lookup"><span data-stu-id="24ee2-141">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="24ee2-142">Incorporare catene di certificati in un documento</span><span class="sxs-lookup"><span data-stu-id="24ee2-142">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[<span data-ttu-id="24ee2-143">Errori dell'API firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="24ee2-143">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="24ee2-144">Errori del documento XPS</span><span class="sxs-lookup"><span data-stu-id="24ee2-144">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="24ee2-145">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="24ee2-145">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
