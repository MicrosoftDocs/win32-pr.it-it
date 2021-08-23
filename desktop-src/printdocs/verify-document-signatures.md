---
description: Questo argomento descrive come verificare le firme in un documento XPS e come verificare i certificati correlati a tali firme.
ms.assetid: fd12abaf-dc0f-4db1-837d-c116627bcc7e
title: Verificare le firme e i certificati dei documenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adfc3dbb6eefedcc3bc14d79340893b60dc32dc7cd9b50b653913c1261d8eac6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033839"
---
# <a name="verify-document-signatures-and-certificates"></a>Verificare le firme e i certificati dei documenti

Questo argomento descrive come verificare le firme in un documento XPS e come verificare i certificati correlati a tali firme.

Prima di usare gli esempi di codice seguenti nel programma, leggere la dichiarazione di non responsabilità in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).

Nell'esempio di codice seguente vengono verificate le firme digitali presenti in un documento XPS.

Per controllare le firme in un documento XPS, seguire questa procedura:

1.  Caricare il documento in un gestore delle firme, come descritto in [Inizializzare Gestione firme](initialize-the-signature-manager.md).
2.  Ottenere la raccolta di firme dal gestore delle firme digitali.
3.  Ottiene il numero di firme nella raccolta.
4.  Per ogni firma nella raccolta, chiamare il [**metodo Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) come illustrato nell'esempio di codice seguente.


```C++
HRESULT
VerifyAllDigitalSignaturesAndAuthenticateCertificates(
    IXpsSignatureManager *signatureManager
)
{
    HRESULT                       hr                              = S_OK;
    IXpsSignature                 *signature                      = NULL;
    IXpsSignatureCollection       *signaturesInDocument           = NULL;
    UINT32                        numberOfSignaturesInDocument    = NULL;

    hr = signatureManager->GetSignatures(&signaturesInDocument);
    if (SUCCEEDED(hr)) {
        hr = signaturesInDocument->GetCount(&numberOfSignaturesInDocument);
    }

    if (SUCCEEDED(hr)) {
        // Check each signature in the XPS document that was opened in
        //  the signature manager.
        for (UINT32 index = 0; index < numberOfSignaturesInDocument; index++)
        {
            // Get the signature in the current index of the 
            //  IXpsSignatureCollection object
            hr = signaturesInDocument->GetAt(index, &signature);

            if (SUCCEEDED(hr)) {
                PCCERT_CONTEXT       signingCertificate = NULL;
                XPS_SIGNATURE_STATUS signatureStatus; 

                signatureStatus = XPS_SIGNATURE_STATUS_BROKEN;
                // Verify the signature and authenticate 
                //  its signing certificate
                hr = VerifySignatureAndCertificates (
                        signature,
                        &signingCertificate,
                        &signatureStatus);
                if (FAILED(hr)) {
                    // If a FACILITY_SECURITY error code is returned then 
                    //  the current certificate was not the 
                    //    signing certificate, so continue with 
                    //  the enumeration.
                    if (HRESULT_FACILITY(hr) != FACILITY_SECURITY)
                    {
                        // If the error was not a FACILITY_SECURITY error  
                        //  then exit and return the error
                        break; // out of for loop
                    }
                }
                // release pointers for next loop
                if (NULL != signature) {
                    signature->Release(); 
                    signature = NULL; 
                }
                if (NULL != signingCertificate) {
                    CertFreeCertificateContext (signingCertificate); 
                    signingCertificate = NULL;
                }
            }
        }
    }
    if (NULL != signaturesInDocument) signaturesInDocument->Release();
    
    return hr;
}
```



Per verificare una firma digitale, verificare innanzitutto la firma creata dal certificato di firma e quindi convalidare il certificato di firma. Il metodo di convalida usato nell'esempio di codice seguente memorizza nella cache i certificati in un archivio certificati temporaneo, che le funzioni api Crypto usano quando vengono chiamati più avanti in questo esempio.

Per creare un archivio certificati temporaneo, seguire questa procedura:

1.  Creare un archivio certificati temporaneo per contenere i certificati usati dalla firma.
2.  Scorrere il set di certificati della firma e caricare ogni certificato nell'archivio certificati temporaneo.


```C++
HRESULT VerifySignatureAndCertificates (
    IXpsSignature           *signature,
    PCCERT_CONTEXT          *signingCertificate,
    XPS_SIGNATURE_STATUS    *signatureStatus
)
{
    HRESULT                         hr                        = S_OK;
    BOOL                            moreCertificates          = FALSE;
    IOpcCertificateEnumerator       *certificatesInSignature  = NULL;
    
    HCERTSTORE                      signatureCertificateStore = NULL;
    
    // Create a temporary certificate store.  
    signatureCertificateStore = CertOpenStore(
        CERT_STORE_PROV_MEMORY, 
        X509_ASN_ENCODING, 
        NULL, 
        0, 
        NULL);

    // Create a certificate enumerator to store the certificates 
    //  that are associated with the current signature.
    hr = signature->GetCertificateEnumerator(&certificatesInSignature);

    if (SUCCEEDED(hr))
    {
    // We need to call the MoveNext method to initialize the enumerator.
        hr = certificatesInSignature->MoveNext(&moreCertificates);
    }
    if (SUCCEEDED(hr))
    {
        // Iterate through the certificates in the signature, 
        //  and add each one to the temporary certificate store.  
        //  This temporary  certificate store simplifies 
        //  authentication of the signing certificate.
        while (moreCertificates)
        {
            PCCERT_CONTEXT certificate  = NULL;
            hr = certificatesInSignature->GetCurrent(&certificate);
            if (SUCCEEDED(hr))
            {
                // got the next certificate so
                // add the current certificate to the temporary certificate store.
                if (!CertAddCertificateContextToStore(signatureCertificateStore,
                    certificate,
                    CERT_STORE_ADD_REPLACE_EXISTING,
                    NULL))
                {
                    hr = E_FAIL;
                    // ERROR: could not add the certificate to the certificate store
                    break; // out of while loop
                }
                CertFreeCertificateContext (certificate);
            }
            else
            {
                // unable to get the certificate so skip
            }

            // move to next certificate in set
            if (FAILED(hr = certificatesInSignature->MoveNext(&moreCertificates)))
            {
                // ERROR: could not move to the next certificate in the enumerator
                break; // out of while loop
            }
            // moreCertificates == FALSE when the end of the set has been reached.
        }//End while
    }
    if (NULL != certificatesInSignature) certificatesInSignature->Release();

```



Per verificare la firma digitale e il certificato usato per firmare il documento, seguire questa procedura:

1.  Trovare il certificato di firma tramite l'iterazione dei certificati usati dalla firma.
2.  Testare il certificato verificando la firma rispetto al certificato. Il certificato di firma viene trovato quando il metodo [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) restituisce lo stato [**XPS \_ SIGNATURE \_ STATUS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status) **\_ \_ \_ VALID** o **XPS SIGNATURE STATUS \_ \_ \_ QUESTIONABLE** e non restituisce un **errore FACILITY \_ SECURITY.**


```C++
    // Reset the enumerator
    hr = signature->GetCertificateEnumerator(&certificatesInSignature);
    if (SUCCEEDED (hr))
    {
        moreCertificates = FALSE;
        hr = certificatesInSignature->MoveNext(&moreCertificates);
    }
    if (SUCCEEDED(hr))
    {
        // Iterate through the certificates in the signature,
        //  and call the IXpsSignature.Verify() method
        //  on each certificate.  
        // A signature can include an entire certificate chain, and so 
        //  only one of the certificates found in this enumeration 
        //  is the certificate that was used to sign the package. 
        //  The signing certificate is the one to authenticate.  
        // To find the signing certificate,  iterate through 
        //  the certificates in the signature and select the certificate that 
        //  returns an XPS_SIGNATURE_STATUS of XPS_SIGNATURE_STATUS_VALID
        //  or XPS_SIGNATURE_STATUS_QUESTIONABLE and does not return a
        //  FACILITY_SECURITY error.
        XPS_SIGNATURE_STATUS localSignatureStatus;
        localSignatureStatus = XPS_SIGNATURE_STATUS_INCOMPLIANT;
        do
        {
            PCCERT_CONTEXT certificate = NULL;
            DWORD certificateStatus = NULL;

            if (FAILED(hr = certificatesInSignature->GetCurrent(&certificate)))
            {
                // We will skip corrupted certificates
                // free this one and move to the next
                CertFreeCertificateContext (certificate);
                hr = certificatesInSignature->MoveNext(&moreCertificates);
                if (FAILED(hr))
                {
                    // ERROR: could not move to the next 
                    //  certificate in the enumerator
                    break; // out of do loop with failed hr
                }
                // continue with next loop iteration
                continue;
            }
            
            // Verify that the signature conforms to the XPS signing policy.
            hr = signature->Verify(certificate, &localSignatureStatus);
            if (FAILED(hr))
            {
                // If a FACILITY_SECURITY error code is returned, then the
                //  current certificate was not the signing certificate,
                //  so continue to the next certificate.
                if (HRESULT_FACILITY(hr) == FACILITY_SECURITY)
                {
                    // free this one and move to the next
                    CertFreeCertificateContext (certificate);
                    hr = certificatesInSignature->MoveNext(&moreCertificates);
                    if (FAILED(hr))
                    {
                        // ERROR: could not move to the next certificate 
                        //  in the enumerator
                        break; // out of do loop with failed hr
                    }
                    continue;
                }
                // ERROR: An attempt to verify the signature has failed
                break; // out of do loop with failed hr
            }
            // if verification was successful, localSignatureStatus will
            //  contain the status of the signature.
            //
            // do loop continues in next code example
```



Dopo aver trovato il certificato di firma, seguire questa procedura:

1.  Salvare lo stato della firma restituito.
2.  Aggiornare lo stato locale, se necessario, per eseguire i test dei certificati successivi:
    1.  Se lo stato della firma ha esito positivo, impostare lo stato locale su discutibile per testare i certificati.
    2.  Se lo stato della firma non è conforme, lasciare lo stato locale non conforme.
    3.  Se lo stato della firma è interrotto o incompleto, impostare lo stato locale su interrotto.

Lo stato di firma **XPS \_ SIGNATURE STATUS \_ \_ INCOMPLIANT** indica che parti del documento XPS che non devono essere state firmate sono state firmate o parti del documento XPS che dovevano essere firmate non sono state firmate. Se [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) restituisce questo stato della firma, un ulteriore controllo della firma non sarà necessario.


```C++
            // continuing do loop from previous code example
            *signingCertificate = certificate;
            *signatureStatus = localSignatureStatus;
            
            // note that this test should only downgrade the 
            // signature status, it should not upgrade it.
            switch (localSignatureStatus) {
                case XPS_SIGNATURE_STATUS_VALID:
                case XPS_SIGNATURE_STATUS_QUESTIONABLE:
                    // the signature is valid or questionable so
                    // save the actual status and set the new status
                    // to questionable so the certificates will be checked.
                    localSignatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    break;

                case XPS_SIGNATURE_STATUS_INCOMPLIANT:
                    // the signature is not compliant 
                    break;

                case XPS_SIGNATURE_STATUS_INCOMPLETE:
                case XPS_SIGNATURE_STATUS_BROKEN:
                    // The Windows 7 XPS viewer displays incomplete signatures
                    // and broken signatures as broken.
                    *signatureStatus = XPS_SIGNATURE_STATUS_BROKEN;
                    localSignatureStatus = XPS_SIGNATURE_STATUS_BROKEN;
                    break;

                default:
                    // there should be no other possible status values
                    break;
            }
            // do loop continues in next code example
```



Per verificare l'attendibilità del certificato se lo stato della firma era valido o discutibile, seguire questa procedura:

1.  Ottenere lo stato di attendibilità del certificato.
2.  Valutare lo stato di attendibilità del certificato restituito.
3.  Restituisce lo stato risultante.

L'esempio di codice successivo non verifica ogni possibile stato di attendibilità del certificato. Per altri dettagli sui valori di stato che possono essere restituiti, vedere [**CERT \_ TRUST \_ STATUS**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status).


```C++
            // continuing do loop from previous code example
            //
            // at this point, localSignatureStatus should be less than or 
            // equal to what it was before the test.

            // Check the certificate to see if it is valid
            if ((localSignatureStatus == XPS_SIGNATURE_STATUS_VALID) || 
                (localSignatureStatus == XPS_SIGNATURE_STATUS_QUESTIONABLE))
            {
                // This call builds the certificate trust chain from the 
                //  supplied certificate.  The certificate chain is used to
                //  authenticate the supplied certificate.
                hr = GetCertificateTrustStatus (
                    *signingCertificate, 
                    &signatureCertificateStore,
                    &certificateStatus);
                if (FAILED(hr))
                {
                    // ERROR: An attempt to authenticate the certificate 
                    //  has failed
                    break; // out of do loop with failed hr
                }

                // The Crypt API returns a status that can contain more than
                //  one status value.
                // statusFlagMask is set to test all bits except for the
                //  CERT_TRUST_REVOCATION_STATUS_UNKNOWN
                //  CERT_TRUST_IS_OFFLINE_REVOCATION
                //  CERT_TRUST_IS_NOT_TIME_VALID
                //  values because, for this test, these are not considered
                //  to be error conditions.
                DWORD statusFlagMask = ~(
                    CERT_TRUST_REVOCATION_STATUS_UNKNOWN | 
                    CERT_TRUST_IS_OFFLINE_REVOCATION | 
                    CERT_TRUST_IS_NOT_TIME_VALID);

                if (CERT_TRUST_NO_ERROR == (certificateStatus & statusFlagMask))
                {
                    // If *signatureStatus is already 
                    //    XPS_SIGNATURE_STATUS_VALID then there is no need to 
                    //    change the status as the certificate status has no 
                    //    certificate trust errors.
                    // If *signatureStatus is already 
                    //  XPS_SIGNATURE_STATUS_QUESTIONABLE then we will not
                    //  upgrade the trust status of the signature just 
                    //  because there is no trust issue with the certificate.
                }
                else
                {
                    // If trust errors were detected with the certificate, 
                    //  then this XPS signature is given a status of 
                    //  XPS_SIGNATURE_STATUS_QUESTIONABLE
                    *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                }

                // Handle additional certificate errors.  
                //  This is not an exhaustive list of possible errors.

                if (certificateStatus & CERT_TRUST_IS_NOT_TIME_VALID)
                {
                    // The XPS Viewer considers signatures with 
                    //  expired certificates as valid.
                }
                if (certificateStatus & CERT_TRUST_IS_PARTIAL_CHAIN)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }

                if (certificateStatus & CERT_TRUST_IS_NOT_SIGNATURE_VALID)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }

                if (certificateStatus & CERT_TRUST_IS_SELF_SIGNED)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }
                
                if (certificateStatus & CERT_TRUST_IS_UNTRUSTED_ROOT)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }
            }//End if

            hr = certificatesInSignature->MoveNext(&moreCertificates);
            if (FAILED(hr))
            {
                // ERROR: could not move to the next 
                //  certificate in the enumerator
                break; // out of do loop with failed hr
            }
        } while((*signatureStatus != XPS_SIGNATURE_STATUS_VALID) && 
                    moreCertificates);
    } // end if successful

    if (NULL != certificatesInSignature) certificatesInSignature->Release();

    return hr;
}
```



Nell'esempio di codice successivo lo stato di attendibilità del certificato viene ottenuto chiamando il metodo illustrato nell'esempio di codice seguente.


```C++
HRESULT GetCertificateTrustStatus(
    __in PCCERT_CONTEXT certificate,
    __in HCERTSTORE* certificateStore,
    __out DWORD* certificateStatus
)
{
    HRESULT    hr = S_OK;

    // The certificate chain that will be created from 
    //  the PCCERT_CONTEXT object passed in.  
    PCCERT_CHAIN_CONTEXT    certificateChain =    NULL;

    hr = CreateCertificateChain(
        certificate, 
        *certificateStore, 
        &certificateChain);

    if (SUCCEEDED(hr)) { 
        *certificateStatus = 
            certificateChain->TrustStatus.dwErrorStatus;
    }

    return hr;
}
```



La catena di certificati usata nell'esempio di codice precedente viene creata chiamando il metodo illustrato nell'esempio di codice seguente.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Usato in questa sezione**
</dt> <dt>

[**CONTESTO CATENA \_ DI \_ CERTIFICATI**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context)
</dt> <dt>

[**CONTESTO \_ CERT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**STATO DI \_ ATTENDIBILITÀ DEL \_ CERTIFICATO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status)
</dt> <dt>

[**CertAddCertificateContextToStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
</dt> <dt>

[**CertOpenStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore)
</dt> <dt>

[**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[**IOpcCertificateEnumerator**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator)
</dt> <dt>

[**IOpcCertificateEnumerator::GetCurrent**](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-getcurrent)
</dt> <dt>

[**IOpcCertificateEnumerator::MoveNext**](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-movenext)
</dt> <dt>

[**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)
</dt> <dt>

[**IXpsSignature::GetCertificateEnumerator**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getcertificateenumerator)
</dt> <dt>

[**IXpsSignature::Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify)
</dt> <dt>

[**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)
</dt> <dt>

[**IXpsSignatureCollection::GetAt**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturecollection-getat)
</dt> <dt>

[**IXpsSignatureCollection::GetCount**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturecollection-getcount)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**IXpsSignatureManager::GetSignatures**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-getsignatures)
</dt> <dt>

[**STATO \_ DELLA FIRMA \_ XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status)
</dt> <dt>

**Per altre informazioni**
</dt> <dt>

[Incorporare catene di certificati in un documento](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[Errori dell'API di firma digitale XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Errori dei documenti XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
