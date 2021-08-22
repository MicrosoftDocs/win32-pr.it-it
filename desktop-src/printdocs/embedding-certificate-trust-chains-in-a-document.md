---
description: Questo argomento descrive come incorporare i certificati che costituiscono una catena di certificati in un documento XPS.
ms.assetid: c6aae8ff-2e1e-43de-9105-171e4187d193
title: Incorporare catene di certificati in un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23e47b4cd0d140d7200fb8aa01642ea5fbb731e49dcc289f596a054b0accbf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447581"
---
# <a name="embed-certificate-chains-in-a-document"></a>Incorporare catene di certificati in un documento

Questo argomento descrive come incorporare i certificati che costituiscono una catena di certificati in un documento XPS. Una catena di certificati è costituita da tutti i certificati, ad eccezione del certificato radice, necessari per certificare il soggetto identificato dal certificato finale.

Per incorporare una catena di certificati in un documento XPS, creare prima di tutto la catena di certificati, come illustrato nell'esempio di codice seguente.

Il **metodo CreateCertificateChain** nell'esempio di codice accetta *certificateStore* come parametro, ovvero un **valore HCERTSTORE.** Se questo valore è **NULL,** i certificati verranno recuperati dal server certificati del computer client. Se il valore è l'handle per un archivio certificati, i certificati verranno recuperati dall'archivio a cui fa riferimento *certificateStore,* nonché dal server certificati del computer client.


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



L'esempio di codice seguente crea una catena di certificati dai certificati e quindi li aggiunge a un documento XPS. Si noti [**che CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) crea la catena di certificati in cui il certificato di firma è primo e il certificato radice è l'ultimo. Il certificato di firma e il certificato radice non vengono aggiunti in questo esempio. I certificati di firma verranno aggiunti con una chiamata al metodo [**IXpsSignatureManager::Sign,**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) che deve essere l'ultimo metodo di firma chiamato sul documento. Il certificato radice non viene aggiunto quando il documento viene firmato, perché deve essere fornito dal server certificati del computer client quando la firma viene convalidata.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Passaggi successivi**
</dt> <dt>

[Caricare un certificato da un file](load-a-certificate-from-a-file.md)
</dt> <dt>

[Verificare che un certificato supporti un metodo di firma](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Verificare che il sistema supporti un metodo digest](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

**Usato in questo esempio**
</dt> <dt>

[**CONTESTO \_ CERT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[**INFORMAZIONI \_ SULL'OID CRYPT \_**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

[**IOpcCertificateSet**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset)
</dt> <dt>

[**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

**Per altre informazioni**
</dt> <dt>

[API di crittografia](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Funzioni di crittografia](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Certificati digitali](/windows/desktop/SecCrypto/digital-certificates)
</dt> <dt>

[Catene di certificati](/windows/desktop/SecCrypto/certificate-chains)
</dt> <dt>

[Verifica dell'attendibilità del certificato](/windows/desktop/SecCrypto/certificate-trust-verification)
</dt> <dt>

[Errori dell'API di firma digitale XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Errori dei documenti XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
