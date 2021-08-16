---
description: Implementa le interfacce IX509PrivateKey e IX509PublicKey.
ms.assetid: 1358053e-ed4e-4482-b160-5b9b1024c771
title: Funzioni di chiave privata e pubblica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6f210393ffaeb676e0190d391692225f25e0cfb4bc3acbcd2c3c188bf40a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774424"
---
# <a name="private-and-public-key-functions"></a>Funzioni di chiave privata e pubblica

CertEnroll.dll implementa le [**interfacce IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) e [**IX509PublicKey.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) È ad esempio possibile usare [**l'interfaccia IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) per eseguire le azioni seguenti su [*una chiave privata:*](/windows/desktop/SecGloss/p-gly)

-   Creare, aprire, chiudere, importare, esportare ed eliminare la chiave.
-   Specificare o recuperare [*l'algoritmo a chiave pubblica*](/windows/desktop/SecGloss/p-gly).
-   Specificare o recuperare informazioni sul provider del servizio [*di crittografia*](/windows/desktop/SecGloss/c-gly) (CSP) disponibile che supporta l'algoritmo a chiave pubblica.
-   Specificare o recuperare il [*certificato*](/windows/desktop/SecGloss/c-gly) associato alla [*chiave privata*](/windows/desktop/SecGloss/p-gly).
-   Specificare o recuperare il nome del [*contenitore di chiavi.*](/windows/desktop/SecGloss/k-gly)
-   Specificare o recuperare una descrizione di e un nome visualizzato per la chiave.
-   Specificare o recuperare i vincoli di esportazione in una chiave privata.
-   Specificare o recuperare un valore booleano che indica se la chiave esiste.
-   Specificare o recuperare un valore che indica come la chiave è protetta prima dell'uso.
-   Specificare o recuperare un valore che indica se la chiave può essere usata per la firma, la crittografia o entrambi.
-   Specificare o recuperare un valore che identifica lo scopo specifico per cui è possibile usare la chiave.
-   Specificare o recuperare la lunghezza della chiave.
-   Specificare o recuperare un valore che indica se la chiave viene usata o salvata nel contesto di un computer o di un utente.
-   Recuperare un valore booleano che specifica se la chiave è stata aperta.
-   Specificare un numero di identificazione personale per accedere a una chiave privata in un [*smart card*](/windows/desktop/SecGloss/s-gly).
-   Specificare o recuperare il nome del provider di servizi di configurazione associato alla chiave.
-   Specificare o recuperare il [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) per la chiave.

Ognuna delle sezioni seguenti identifica una funzione esportata da Xenroll.dll che può essere usata per gestire una [*chiave crittografica*](/windows/desktop/SecGloss/c-gly). Ogni argomento illustra anche come usare CertEnroll.dll per sostituire la funzione o indica che non esiste alcun mapping tra le due librerie:

-   [ContainerNameWStr](#containernamewstr)
-   [GenKeyFlags](#genkeyflags)
-   [GetKeyLen](#getkeylenex)
-   [GetKeyLenEx](#getkeylenex)
-   [GetSupportedKeySpec](#getsupportedkeyspec)
-   [KeySpec](#getsupportedkeyspec)
-   [LimitExchangeKeyToEncipherment](#limitexchangekeytoencipherment)
-   [PVKFileNameWStr](#pvkfilenamewstr)
-   [ReuseHardwareKeyIfUnableToGenNew](#reusehardwarekeyifunabletogennew)
-   [UseExistingKeySet](#useexistingkeyset)
-   [Argomenti correlati](#related-topics)

## <a name="containernamewstr"></a>ContainerNameWStr

La [**funzione ContainerNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_containernamewstr) in Xenroll.dll specifica o recupera il nome del [*contenitore di chiavi.*](/windows/desktop/SecGloss/k-gly)

Quando si CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare il nome di un contenitore di chiavi:

1.  Chiamare la [**proprietà Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) su un [**oggetto IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) esistente.
2.  Chiamare il [**metodo GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sulla richiesta restituita dal passaggio 1 per recuperare la richiesta più interna.
3.  Chiamare **QueryInterface** [**sull'oggetto IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) restituito dal passaggio 2 per eseguire il cast a [**un oggetto IX509CertificateRequestPkcs10.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
4.  Chiamare la [**proprietà PrivateKey**](/windows/desktop/SecCrypto/privatekey) sulla richiesta PKCS \# 10.
5.  Chiamare la [**proprietà ContainerName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_containername) sull'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperato dal passaggio 4.

## <a name="genkeyflags"></a>GenKeyFlags

La [**funzione GenKeyFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags) definita in Xenroll.dll specifica o recupera i flag usati per generare una chiave privata o una coppia [*di chiavi pubblica/privata.*](/windows/desktop/SecGloss/p-gly)

Quando si CertEnroll.dll, è possibile specificare diverse proprietà che determineranno la modalità di creazione di una chiave privata. Per altre informazioni, vedere [**Creare**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create).

## <a name="getkeylen"></a>GetKeyLen

La [**funzione GetKeyLen**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getkeylen) definita in Xenroll.dll recupera le dimensioni massime o minime della chiave di crittografia.

Quando si usa CertEnroll.dll, è possibile chiamare la proprietà [**Length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) su un oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) o [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) per recuperare le dimensioni della chiave, in bit.

## <a name="getkeylenex"></a>GetKeyLenEx

La [**funzione GetKeyLenEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getkeylenex) definita in Xenroll.dll recupera le dimensioni massime o minime della chiave o la lunghezza di incremento di una chiave di crittografia.

Quando si usa CertEnroll.dll, è possibile chiamare la proprietà [**Length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) su un oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) o [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) per recuperare le dimensioni della chiave, in bit. Se un algoritmo supporta lunghezze di chiave incrementali, è possibile chiamare la [**proprietà IncrementLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_incrementlength) sull'oggetto [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm) per recuperare il valore di incremento. È anche possibile chiamare le [**proprietà MinLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_minlength) e [**MaxLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_maxlength) per recuperare le dimensioni minime e massime delle chiavi.

## <a name="getsupportedkeyspec"></a>GetSupportedKeySpec

La [**funzione GetSupportedKeySpec**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getsupportedkeyspec) definita in Xenroll.dll recupera un valore che indica se un provider di servizi di configurazione supporta le chiavi di scambio, le chiavi di firma o entrambe.

Quando si CertEnroll.dll, è possibile chiamare la [**proprietà KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) sugli oggetti [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) o [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) per recuperare le operazioni supportate dalla chiave.

## <a name="keyspec"></a>KeySpec

La [**funzione KeySpec**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_keyspec) definita in Xenroll.dll specifica o recupera il tipo di chiave.

Quando si CertEnroll.dll, è possibile chiamare la [**proprietà KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) su un [**oggetto IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) per recuperare le operazioni supportate dalla chiave.

## <a name="limitexchangekeytoencipherment"></a>LimitExchangeKeyToEncipherment

La [**funzione LimitExchangeKeyToEncipherment**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_limitexchangekeytoencipherment) definita in Xenroll.dll specifica o recupera un valore booleano che indica se una chiave di crittografia può essere usata solo per la crittografia di dati o chiavi.

CertEnroll.dll non contiene un equivalente diretto per questa funzione. È tuttavia possibile ottenere un risultato quasi equivalente specificando un [**oggetto IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage) e aggiungendolo alla richiesta di certificato.

## <a name="pvkfilenamewstr"></a>PVKFileNameWStr

La [**funzione PVKFileNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_pvkfilenamewstr) definita in Xenroll.dll specifica o recupera il nome di un file che contiene chiavi esportate.

Quando si CertEnroll.dll, è possibile chiamare il [**metodo Export**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-export) su un [**oggetto IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) per esportare una chiave in **un oggetto BSTR.** È possibile chiamare il [**metodo ExportPublicKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-exportpublickey) per esportare la [*parte di chiave*](/windows/desktop/SecGloss/p-gly) pubblica di una coppia di chiavi asimmetriche.

## <a name="reusehardwarekeyifunabletogennew"></a>ReuseHardwareKeyIfUnableToGenNew

La funzione [**ReuseHardwareKeyIfUnableToGenNew**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_reusehardwarekeyifunabletogennew) definita in Xenroll.dll specifica o recupera un valore booleano che indica se una chiave esistente viene riutilizzata quando viene rilevato un errore durante la generazione di una nuova chiave.

Quando si usa CertEnroll.dll, è possibile chiamare il metodo [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) su un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e specificare un valore del tipo di enumerazione [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) per riutilizzare una chiave privata esistente.

## <a name="useexistingkeyset"></a>UseExistingKeySet

La [**funzione UseExistingKeySet**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_useexistingkeyset) definita in Xenroll.dll specifica o recupera un valore booleano che indica se usare chiavi esistenti.

Quando si usa CertEnroll.dll, è possibile chiamare il metodo [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) su un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e specificare un valore del tipo di enumerazione [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) per riutilizzare le chiavi pubbliche e private esistenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll a CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 
