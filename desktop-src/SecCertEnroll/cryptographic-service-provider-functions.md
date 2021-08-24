---
description: Funzioni esportate da Xenroll.dll che possono essere usate per gestire un provider del servizio di crittografia.
ms.assetid: 4f6f353d-6b06-45b4-8808-56998d3727a4
title: Funzioni del provider del servizio di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 947d9c4f2529071b28052ae5ca34f811d4657c3fd4cede23285999cbaa13a72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883081"
---
# <a name="cryptographic-service-provider-functions"></a>Funzioni del provider del servizio di crittografia

Ognuna delle sezioni seguenti identifica una funzione esportata da Xenroll.dll che può essere usata per gestire un provider del servizio di crittografia. Ogni argomento illustra anche come usare CertEnroll.dll sostituire la funzione o indica che non esiste alcun mapping tra le due librerie:

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

La [**funzione EnumAlgs**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-enumalgs) in Xenroll.dll recupera una raccolta di algoritmi di crittografia.

Quando si CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare informazioni sugli algoritmi supportati da un provider del [*servizio*](/windows/desktop/SecGloss/c-gly) di crittografia (CSP):

1.  Chiamare la [**proprietà Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) su un oggetto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) esistente.
2.  Chiamare il [**metodo GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sulla richiesta restituita dal passaggio 1 per recuperare la richiesta più interna.
3.  Chiamare **QueryInterface sull'oggetto** [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) restituito dal passaggio 2 per eseguire il cast a [**un oggetto IX509CertificateRequestPkcs10.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
4.  Chiamare la [**proprietà PrivateKey**](/windows/desktop/SecCrypto/privatekey) nella richiesta PKCS \# 10.
5.  Chiamare la [**proprietà CspInformations**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) sull'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperato dal passaggio 4.
6.  Chiamare la [**proprietà CspAlgorithms**](/windows/desktop/api/CertEnroll/nf-certenroll-icspinformation-get_cspalgorithms) su un oggetto [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) specifico nella raccolta [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) recuperata nel passaggio 5.

## <a name="enumcontainerswstr"></a>enumContainersWStr

La [**funzione enumContainersWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumcontainerswstr) in Xenroll.dll recupera un contenitore di chiavi dalla raccolta in base all'indice.

La CertEnroll.dll non implementa direttamente questa funzionalità.

## <a name="enumproviderswstr"></a>enumProvidersWStr

La [**funzione enumProvidersWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumproviderswstr) in Xenroll.dll recupera un provider di servizi di configurazione dalla raccolta in base all'indice.

Quando si CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare la raccolta di contenitori crittografici:

1.  Chiamare la [**proprietà Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) su un oggetto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) esistente.
2.  Chiamare il [**metodo GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sulla richiesta restituita dal passaggio 1 per recuperare la richiesta più interna.
3.  Chiamare **QueryInterface sull'oggetto** [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) restituito dal passaggio 2 per eseguire il cast a [**un oggetto IX509CertificateRequestPkcs10.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
4.  Chiamare la [**proprietà PrivateKey**](/windows/desktop/SecCrypto/privatekey) nella richiesta PKCS \# 10.
5.  Chiamare la [**proprietà CspInformations**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) sull'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperato dal passaggio 4.

## <a name="getalgnamewstr"></a>GetAlgNameWStr

La [**funzione GetAlgNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getalgnamewstr) in Xenroll.dll recupera il nome di un algoritmo [*di crittografia*](/windows/desktop/SecGloss/c-gly).

Quando si usa CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare il nome dell'algoritmo:

1.  Chiamare la [**proprietà Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) su un oggetto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) esistente.
2.  Chiamare il [**metodo GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sulla richiesta restituita dal passaggio 1 per recuperare la richiesta più interna.
3.  Chiamare **QueryInterface sull'oggetto** [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) restituito dal passaggio 2 per eseguire il cast a [**un oggetto IX509CertificateRequestPkcs10.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
4.  Chiamare la [**proprietà PrivateKey**](/windows/desktop/SecCrypto/privatekey) nella richiesta PKCS \# 10.
5.  Chiamare la [**proprietà Algorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm) sull'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) per recuperare l'identificatore dell'oggetto algoritmo.
6.  Chiamare la [**proprietà FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) sull'interfaccia [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) per recuperare il nome visualizzato dell'algoritmo.

## <a name="getprovidertypewstr"></a>getProviderTypeWStr

La [**funzione getProviderTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprovidertypewstr) in Xenroll.dll recupera il tipo di provider del servizio di crittografia.

Quando si CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare il tipo di provider:

1.  Chiamare la [**proprietà Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) su un oggetto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) esistente.
2.  Chiamare il [**metodo GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sulla richiesta restituita dal passaggio 1 per recuperare la richiesta più interna.
3.  Chiamare **QueryInterface sull'oggetto** [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) restituito dal passaggio 2 per eseguire il cast a [**un oggetto IX509CertificateRequestPkcs10.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
4.  Chiamare la [**proprietà PrivateKey**](/windows/desktop/SecCrypto/privatekey) nella richiesta PKCS \# 10.
5.  Chiamare la [**proprietà ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) sull'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperato dal passaggio 4.

## <a name="hashalgid"></a>HashAlgID

La [**funzione HashAlgID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_hashalgid) in Xenroll.dll un valore intero che contiene l'ID dell'algoritmo usato per firmare una richiesta.

Quando si CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare l'algoritmo hash:

-   Recuperare [**un'interfaccia IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) chiamando la proprietà [**SignatureInformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) in una richiesta PKCS 10 o CMC o la proprietà SignerCertificate in una richiesta \# [*PKCS \# 7.*](/windows/desktop/SecGloss/p-gly) [](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate)
-   Chiamare la [**proprietà HashAlgorithm sull'oggetto**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) informazioni sulla firma per recuperare l'identificatore dell'oggetto algoritmo hash.

## <a name="hashalgorithmwstr"></a>HashAlgorithmWStr

La [**funzione HashAlgorithmWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_hashalgorithmwstr) in Xenroll.dll specifica o recupera un valore stringa che identifica l'algoritmo hash usato per firmare una richiesta.

Quando si CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare l'algoritmo hash:

-   Recuperare [**un'interfaccia IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) chiamando la proprietà [**SignatureInformation**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) in una richiesta PKCS 10 o CMC o la proprietà SignerCertificate in una richiesta \# PKCS [](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) \# 7.
-   Chiamare la [**proprietà HashAlgorithm sull'oggetto**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) informazioni sulla firma per recuperare l'identificatore dell'oggetto algoritmo hash.
-   Chiamare la [**proprietà FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) sull'interfaccia [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) restituita nel passaggio 2 per recuperare il nome visualizzato dell'algoritmo.

## <a name="providerflags"></a>ProviderFlags

La [**funzione ProviderFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providerflags) in Xenroll.dll specifica o recupera i flag usati durante l'acquisizione di un handle per un CSP.

La CertEnroll.dll non esegue perfettamente il mapping di questa funzione, ma è possibile ottenere informazioni dettagliate sulle proprietà dall'oggetto di registrazione e dalla [*chiave privata*](/windows/desktop/SecGloss/p-gly). Per altre informazioni, esaminare le proprietà esposte dalle [**interfacce IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e [**IX509PrivateKey.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)

## <a name="providernamewstr"></a>ProviderNameWStr

La [**funzione ProviderNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr) in Xenroll.dll specifica o recupera il nome di un CSP.

Quando si CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare il nome del provider:

1.  Chiamare la [**proprietà Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) su un oggetto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) esistente.
2.  Chiamare il [**metodo GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sulla richiesta restituita dal passaggio 1 per recuperare la richiesta più interna.
3.  Chiamare **QueryInterface sull'oggetto** [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) restituito dal passaggio 2 per eseguire il cast a [**un oggetto IX509CertificateRequestPkcs10.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
4.  Chiamare la [**proprietà PrivateKey**](/windows/desktop/SecCrypto/privatekey) nella richiesta PKCS \# 10.
5.  Chiamare la [**proprietà ProviderName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername) sull'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperato dal passaggio 4.

## <a name="providertype"></a>ProviderType

La [**funzione ProviderType**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype) in Xenroll.dll specifica o recupera un valore integer che identifica il tipo di CSP.

Quando si CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare il tipo di provider:

1.  Chiamare la [**proprietà Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) su un oggetto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) esistente.
2.  Chiamare il [**metodo GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sulla richiesta restituita dal passaggio 1 per recuperare la richiesta più interna.
3.  Chiamare **QueryInterface sull'oggetto** [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) restituito dal passaggio 2 per eseguire il cast a [**un oggetto IX509CertificateRequestPkcs10.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
4.  Chiamare la [**proprietà PrivateKey**](/windows/desktop/SecCrypto/privatekey) nella richiesta PKCS \# 10.
5.  Chiamare la [**proprietà ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) sull'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperato dal passaggio 4.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)
</dt> <dt>

[**ICspAlgorithms**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)
</dt> <dt>

[**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)
</dt> <dt>

[**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations)
</dt> <dt>

[**Registrazione IX509**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
