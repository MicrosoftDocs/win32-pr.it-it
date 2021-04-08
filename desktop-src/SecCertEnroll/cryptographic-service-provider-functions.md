---
description: Funzioni esportate da Xenroll.dll che possono essere utilizzate per gestire un provider di crittografia.
ms.assetid: 4f6f353d-6b06-45b4-8808-56998d3727a4
title: Funzioni del provider del servizio di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a981b418271ba834352c0301c005b39742729a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750023"
---
# <a name="cryptographic-service-provider-functions"></a>Funzioni del provider del servizio di crittografia

Ognuna delle sezioni seguenti identifica una funzione esportata da Xenroll.dll utilizzabile per la gestione di un provider di crittografia. In ogni argomento viene inoltre illustrato come utilizzare CertEnroll.dll per sostituire la funzione o indicare che non esiste alcun mapping tra le due librerie:

-   [EnumAlgs](#enumalgs)
-   [enumContainersWStr](#enumcontainerswstr)
-   [enumProvidersWStr](#enumproviderswstr)
-   [GetAlgNameWStr](#getalgnamewstr)
-   [getProviderTypeWStr](#getprovidertypewstr)
-   [HashAlgID](#hashalgid)
-   [HashAlgorithmWStr](#hashalgorithmwstr)
-   [ProviderFlags](#providerflags)
-   [ProviderNameWStr](#providernamewstr)
-   [ProviderType](#getprovidertypewstr)
-   [Argomenti correlati](#related-topics)

## <a name="enumalgs"></a>EnumAlgs

La funzione [**EnumAlgs**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-enumalgs) in Xenroll.dll recupera una raccolta di algoritmi di crittografia.

Quando si utilizza CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare informazioni sugli algoritmi supportati da un [*provider del servizio di crittografia*](/windows/desktop/SecGloss/c-gly) (CSP):

1.  Chiamare la proprietà [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) su un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) esistente.
2.  Chiamare il metodo [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sulla richiesta restituita dal passaggio 1 per recuperare la richiesta più interna.
3.  Chiamare **QueryInterface** sull'oggetto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) restituito dal passaggio 2 per eseguire il cast a un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Chiamare la proprietà [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) nella richiesta PKCS \# 10.
5.  Chiamare la proprietà [**CspInformations**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) nell'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperato dal passaggio 4.
6.  Chiamare la proprietà [**CspAlgorithms**](/windows/desktop/api/CertEnroll/nf-certenroll-icspinformation-get_cspalgorithms) su un oggetto [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) specifico nella raccolta [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) recuperata nel passaggio 5.

## <a name="enumcontainerswstr"></a>enumContainersWStr

La funzione [**enumContainersWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumcontainerswstr) in Xenroll.dll recupera un contenitore di chiavi dalla raccolta in base all'indice.

La libreria CertEnroll.dll non implementa direttamente questa funzionalità.

## <a name="enumproviderswstr"></a>enumProvidersWStr

La funzione [**enumProvidersWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumproviderswstr) in Xenroll.dll recupera un CSP dalla raccolta in base all'indice.

Quando si usa CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare la raccolta di contenitori di crittografia:

1.  Chiamare la proprietà [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) su un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) esistente.
2.  Chiamare il metodo [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sulla richiesta restituita dal passaggio 1 per recuperare la richiesta più interna.
3.  Chiamare **QueryInterface** sull'oggetto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) restituito dal passaggio 2 per eseguire il cast a un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Chiamare la proprietà [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) nella richiesta PKCS \# 10.
5.  Chiamare la proprietà [**CspInformations**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) nell'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperato dal passaggio 4.

## <a name="getalgnamewstr"></a>GetAlgNameWStr

La funzione [**GetAlgNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getalgnamewstr) in Xenroll.dll Recupera il nome di un [*algoritmo di crittografia*](/windows/desktop/SecGloss/c-gly).

Quando si usa CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare il nome dell'algoritmo:

1.  Chiamare la proprietà [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) su un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) esistente.
2.  Chiamare il metodo [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sulla richiesta restituita dal passaggio 1 per recuperare la richiesta più interna.
3.  Chiamare **QueryInterface** sull'oggetto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) restituito dal passaggio 2 per eseguire il cast a un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Chiamare la proprietà [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) nella richiesta PKCS \# 10.
5.  Chiamare la proprietà [**Algorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm) nell'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) per recuperare l'identificatore dell'oggetto dell'algoritmo.
6.  Chiamare la proprietà [**FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) sull'interfaccia [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) per recuperare il nome visualizzato dell'algoritmo.

## <a name="getprovidertypewstr"></a>getProviderTypeWStr

La funzione [**getProviderTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprovidertypewstr) in Xenroll.dll Recupera il tipo di provider di crittografia.

Quando si utilizza CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare il tipo di provider:

1.  Chiamare la proprietà [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) su un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) esistente.
2.  Chiamare il metodo [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sulla richiesta restituita dal passaggio 1 per recuperare la richiesta più interna.
3.  Chiamare **QueryInterface** sull'oggetto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) restituito dal passaggio 2 per eseguire il cast a un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Chiamare la proprietà [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) nella richiesta PKCS \# 10.
5.  Chiamare la proprietà [**ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) nell'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperato dal passaggio 4.

## <a name="hashalgid"></a>HashAlgID

La funzione [**HashAlgID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_hashalgid) in Xenroll.dll recupera un valore integer contenente l'ID dell'algoritmo usato per firmare una richiesta.

Quando si usa CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare l'algoritmo hash:

-   Recuperare un'interfaccia [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) chiamando la proprietà [**SignatureInformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) in una richiesta PKCS \# 10 o CMC o la proprietà [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) in una richiesta [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) .
-   Chiamare la proprietà [**HashAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) sull'oggetto informazioni sulla firma per recuperare l'identificatore di oggetto dell'algoritmo hash.

## <a name="hashalgorithmwstr"></a>HashAlgorithmWStr

La funzione [**HashAlgorithmWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_hashalgorithmwstr) in Xenroll.dll specifica o recupera un valore stringa che identifica l'algoritmo hash usato per firmare una richiesta.

Quando si usa CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare l'algoritmo hash:

-   Recuperare un'interfaccia [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) chiamando la proprietà [**SignatureInformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) in una richiesta PKCS \# 10 o CMC o la proprietà [**SignerCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) in una richiesta PKCS \# 7.
-   Chiamare la proprietà [**HashAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) sull'oggetto informazioni sulla firma per recuperare l'identificatore di oggetto dell'algoritmo hash.
-   Chiamare la proprietà [**FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) nell'interfaccia [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) restituita nel passaggio 2 per recuperare il nome visualizzato dell'algoritmo.

## <a name="providerflags"></a>ProviderFlags

La funzione [**ProviderFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providerflags) in Xenroll.dll specifica o recupera i flag utilizzati durante l'acquisizione di un handle per un CSP.

La libreria CertEnroll.dll non esegue correttamente il mapping di questa funzione, ma è possibile ottenere informazioni dettagliate sulle proprietà dall'oggetto di registrazione e dalla [*chiave privata*](/windows/desktop/SecGloss/p-gly). Per ulteriori informazioni, esaminare le proprietà esposte dalle interfacce [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) .

## <a name="providernamewstr"></a>ProviderNameWStr

La funzione [**ProviderNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr) in Xenroll.dll specifica o Recupera il nome di un CSP.

Quando si utilizza CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare il nome del provider:

1.  Chiamare la proprietà [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) su un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) esistente.
2.  Chiamare il metodo [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sulla richiesta restituita dal passaggio 1 per recuperare la richiesta più interna.
3.  Chiamare **QueryInterface** sull'oggetto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) restituito dal passaggio 2 per eseguire il cast a un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Chiamare la proprietà [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) nella richiesta PKCS \# 10.
5.  Chiamare la proprietà [**providerName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername) nell'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperato dal passaggio 4.

## <a name="providertype"></a>ProviderType

La funzione [**ProviderType**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype) in Xenroll.dll specifica o recupera un valore integer che identifica il tipo del CSP.

Quando si utilizza CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare il tipo di provider:

1.  Chiamare la proprietà [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) su un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) esistente.
2.  Chiamare il metodo [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sulla richiesta restituita dal passaggio 1 per recuperare la richiesta più interna.
3.  Chiamare **QueryInterface** sull'oggetto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) restituito dal passaggio 2 per eseguire il cast a un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Chiamare la proprietà [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) nella richiesta PKCS \# 10.
5.  Chiamare la proprietà [**ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) nell'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperato dal passaggio 4.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)
</dt> <dt>

[**ICspAlgorithms**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)
</dt> <dt>

[**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)
</dt> <dt>

[**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations)
</dt> <dt>

[**Metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
