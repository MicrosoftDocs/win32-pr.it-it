---
description: In questo argomento viene descritto come firmare un documento XPS.
ms.assetid: fbe64aed-6b07-49de-910c-18be68cb65a2
title: Firmare un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef544b2c34af19282d697676d22903948355d23e18e1c646df691c720052cc4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033879"
---
# <a name="sign-a-document"></a>Firmare un documento

In questo argomento viene descritto come firmare un documento XPS.

Prima di usare gli esempi di codice seguenti nel programma, leggere la dichiarazione di non responsabilità in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).

Per firmare un documento XPS, caricarlo prima di tutto in un gestore delle firme, come descritto in [Inizializzare il gestore delle firme.](initialize-the-signature-manager.md)

Per firmare un documento caricato in un gestore delle firme:

1.  Creare [**un'istanza di un'interfaccia IXpsSigningOptions.**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
2.  Impostare i criteri di firma.
3.  Impostare il metodo di firma. Le costanti stringa URI del metodo di firma sono definite in cryptxml.h. Per altre informazioni sui valori validi del metodo di firma, vedere [**IXpsSigningOptions::SetSignatureMethod.**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
4.  Impostare il metodo digest. Le costanti stringa URI del metodo digest sono definite in cryptxml.h. Per informazioni sui valori validi del metodo digest, vedere [**IXpsSigningOptions::SetDigestMethod.**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
5.  Caricare il certificato come descritto in [Caricare un certificato da un file](load-a-certificate-from-a-file.md).
6.  Verificare che il certificato supporti il metodo di firma, come descritto in [Verificare che un certificato supporti un metodo di firma.](verify-a-certificate-supports-a-signature-method.md)
7.  Verificare che il metodo digest sia supportato dal sistema, come descritto in [Verify the System Supports a Digest Method](verify-a-certificate-supports-a-digest-method.md).
8.  Se necessario, incorporare i certificati della catena di certificati nel documento XPS come descritto in [Incorporare](embedding-certificate-trust-chains-in-a-document.md)catene di certificati in un documento .
9.  Firmare il documento XPS.

Nell'esempio di codice seguente viene illustrato come utilizzare i passaggi precedenti in un programma.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Passaggi successivi**
</dt> <dt>

[Aggiungere una richiesta di firma a un documento XPS](add-a-signature-request-to-a-document.md)
</dt> <dt>

[Verificare le firme dei documenti](verify-document-signatures.md)
</dt> <dt>

**Usato in questa sezione**
</dt> <dt>

[**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**IXpsSignatureManager::CreateSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions)
</dt> <dt>

[**IXpsSignatureManager::Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign)
</dt> <dt>

[**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

[**IXpsSigningOptions::SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
</dt> <dt>

[**IXpsSigningOptions::SetPolicy**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy)
</dt> <dt>

[**IXpsSigningOptions::SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
</dt> <dt>

[**CRITERI DI \_ FIRMA \_ XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

**Per altre informazioni**
</dt> <dt>

[API di crittografia](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Funzioni di crittografia](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Caricare un certificato da un file](load-a-certificate-from-a-file.md)
</dt> <dt>

[Verificare che un certificato supporti un metodo di firma](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Verificare che il sistema supporti un metodo digest](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Incorporare catene di certificati in un documento](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[Errori dell'API di firma digitale XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Errori dei documenti XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
