---
description: Implementa le interfacce IX509PrivateKey e IX509PublicKey.
ms.assetid: 1358053e-ed4e-4482-b160-5b9b1024c771
title: Funzioni chiave privata e pubblica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c1d8ec481c87337e7d7e56cffee47f1f483b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314141"
---
# <a name="private-and-public-key-functions"></a>Funzioni chiave privata e pubblica

CertEnroll.dll implementa le interfacce [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) e [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) . È possibile, ad esempio, usare l'interfaccia [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) per eseguire le azioni seguenti su una [*chiave privata*](/windows/desktop/SecGloss/p-gly):

-   Creare, aprire, chiudere, importare, esportare ed eliminare la chiave.
-   Specificare o recuperare l' [*algoritmo a chiave pubblica*](/windows/desktop/SecGloss/p-gly).
-   Specificare o recuperare informazioni sul provider del [*servizio di crittografia*](/windows/desktop/SecGloss/c-gly) (CSP) disponibile che supporta l'algoritmo a chiave pubblica.
-   Specificare o recuperare il [*certificato*](/windows/desktop/SecGloss/c-gly) associato alla [*chiave privata*](/windows/desktop/SecGloss/p-gly).
-   Specificare o recuperare il nome del [*contenitore di chiavi*](/windows/desktop/SecGloss/k-gly).
-   Specificare o recuperare una descrizione e un nome visualizzato per la chiave.
-   Specificare o recuperare i vincoli di esportazione posizionati su una chiave privata.
-   Specificare o recuperare un valore booleano che indica se la chiave esiste.
-   Specificare o recuperare un valore che indica la modalità di protezione della chiave prima dell'utilizzo.
-   Specificare o recuperare un valore che indica se la chiave può essere utilizzata per la firma, la crittografia o entrambi.
-   Specificare o recuperare un valore che identifichi lo scopo specifico per cui è possibile usare la chiave.
-   Specificare o recuperare la lunghezza della chiave.
-   Specificare o recuperare un valore che indica se la chiave viene utilizzata o salvata nel contesto di un computer o di un utente.
-   Recuperare un valore booleano che specifica se la chiave è stata aperta.
-   Specificare un numero di identificazione personale per accedere a una chiave privata in una [*Smart Card*](/windows/desktop/SecGloss/s-gly).
-   Specificare o recuperare il nome del CSP associato alla chiave.
-   Specificare o recuperare il [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) per la chiave.

Ognuna delle sezioni seguenti identifica una funzione esportata da Xenroll.dll che può essere utilizzata per gestire una [*chiave crittografica*](/windows/desktop/SecGloss/c-gly). In ogni argomento viene inoltre illustrato come utilizzare CertEnroll.dll per sostituire la funzione o indicare che non esiste alcun mapping tra le due librerie:

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

La funzione [**ContainerNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_containernamewstr) in Xenroll.dll specifica o Recupera il nome del [*contenitore di chiavi*](/windows/desktop/SecGloss/k-gly).

Quando si usa CertEnroll.dll, è possibile eseguire le azioni seguenti per recuperare il nome di un contenitore di chiavi:

1.  Chiamare la proprietà [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) su un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) esistente.
2.  Chiamare il metodo [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sulla richiesta restituita dal passaggio 1 per recuperare la richiesta più interna.
3.  Chiamare **QueryInterface** sull'oggetto [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) restituito dal passaggio 2 per eseguire il cast a un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Chiamare la proprietà [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) nella richiesta PKCS \# 10.
5.  Chiamare la proprietà [**containerName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_containername) nell'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) recuperato dal passaggio 4.

## <a name="genkeyflags"></a>GenKeyFlags

La funzione [**GenKeyFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags) definita in Xenroll.dll specifica o recupera i flag utilizzati per generare una chiave privata o una [*coppia di chiavi pubblica/privata*](/windows/desktop/SecGloss/p-gly).

Quando si usa CertEnroll.dll, è possibile specificare una serie di proprietà diverse che determineranno la modalità di creazione di una chiave privata. Per ulteriori informazioni, vedere [**create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create).

## <a name="getkeylen"></a>GetKeyLen

La funzione [**GetKeyLen**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getkeylen) definita in Xenroll.dll recupera la dimensione massima o minima della chiave di crittografia.

Quando si usa CertEnroll.dll, è possibile chiamare la proprietà [**length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) su un oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) o [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) per recuperare la dimensione della chiave in bit.

## <a name="getkeylenex"></a>GetKeyLenEx

La funzione [**GetKeyLenEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getkeylenex) definita in Xenroll.dll recupera la dimensione massima o minima della chiave o la lunghezza di incremento di una chiave di crittografia.

Quando si usa CertEnroll.dll, è possibile chiamare la proprietà [**length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) su un oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) o [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) per recuperare la dimensione della chiave in bit. Se un algoritmo supporta lunghezze di chiave incrementali, è possibile chiamare la proprietà [**IncrementLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_incrementlength) sull'oggetto [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm) per recuperare il valore di incremento. È anche possibile chiamare le proprietà [**minLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_minlength) e [**MaxLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_maxlength) per recuperare le dimensioni minime e massime della chiave.

## <a name="getsupportedkeyspec"></a>GetSupportedKeySpec

La funzione [**GetSupportedKeySpec**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getsupportedkeyspec) definita in Xenroll.dll recupera un valore che indica se un CSP supporta chiavi di scambio, chiavi di firma o entrambi.

Quando si usa CertEnroll.dll, è possibile chiamare la proprietà chiave [**specifica**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) sugli oggetti [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) o [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) per recuperare le operazioni supportate dalla chiave.

## <a name="keyspec"></a>KeySpec

La funzione di chiave [**specifica**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_keyspec) definita in Xenroll.dll specifica o Recupera il tipo di chiave.

Quando si usa CertEnroll.dll, è possibile chiamare la proprietà chiave [**specifica**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) su un oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) per recuperare le operazioni supportate dalla chiave.

## <a name="limitexchangekeytoencipherment"></a>LimitExchangeKeyToEncipherment

La funzione [**LimitExchangeKeyToEncipherment**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_limitexchangekeytoencipherment) definita in Xenroll.dll specifica o recupera un valore booleano che indica se una chiave di crittografia può essere utilizzata solo per la crittografia di dati o di chiave.

CertEnroll.dll non contiene un equivalente diretto per questa funzione. È possibile, tuttavia, ottenere un risultato quasi equivalente specificando un oggetto [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage) e aggiungendolo alla richiesta di certificato.

## <a name="pvkfilenamewstr"></a>PVKFileNameWStr

La funzione [**PVKFileNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_pvkfilenamewstr) definita in Xenroll.dll specifica o Recupera il nome di un file che contiene le chiavi esportate.

Quando si usa CertEnroll.dll, è possibile chiamare il metodo [**Export**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-export) su un oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) per esportare una chiave in un **BSTR**. È possibile chiamare il metodo [**ExportPublicKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-exportpublickey) per esportare la parte della [*chiave pubblica*](/windows/desktop/SecGloss/p-gly) di una coppia di chiavi asimmetriche.

## <a name="reusehardwarekeyifunabletogennew"></a>ReuseHardwareKeyIfUnableToGenNew

La funzione [**ReuseHardwareKeyIfUnableToGenNew**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_reusehardwarekeyifunabletogennew) definita in Xenroll.dll specifica o recupera un valore booleano che indica se una chiave esistente viene riutilizzata quando si verifica un errore durante la generazione di una nuova chiave.

Quando si utilizza CertEnroll.dll, è possibile chiamare il metodo [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) su un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e specificare un valore del tipo di enumerazione [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) per riutilizzare una chiave privata esistente.

## <a name="useexistingkeyset"></a>UseExistingKeySet

La funzione [**UseExistingKeySet**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_useexistingkeyset) definita in Xenroll.dll specifica o recupera un valore booleano che indica se utilizzare le chiavi esistenti.

Quando si utilizza CertEnroll.dll, è possibile chiamare il metodo [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) su un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e specificare un valore del tipo di enumerazione [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) per riutilizzare le chiavi pubbliche e private esistenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping Xenroll.dll CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 
