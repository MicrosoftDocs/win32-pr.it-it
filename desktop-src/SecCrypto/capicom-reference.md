---
description: Fornisce servizi che consentono agli sviluppatori di applicazioni di aggiungere la sicurezza in base alla crittografia per le applicazioni.
ms.assetid: 9a2add82-53f9-49ed-b20c-019f95e7d260
title: Riferimento a CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b828f3b5b35e3e0ef799529f866c23416c8df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318945"
---
# <a name="capicom-reference"></a>Riferimento a CAPICOM

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]

Il client COM CAPICOM fornisce servizi che consentono agli sviluppatori di applicazioni di aggiungere la sicurezza in base alla [*crittografia*](../secgloss/c-gly.md) alle applicazioni. CryptoAPI include funzionalità per l'autenticazione tramite [*firme digitali*](../secgloss/d-gly.md), per l'inviluppo dei messaggi e per la crittografia e la decrittografia dei dati.



| Category                    | Descrizione                                                                                                                |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Oggetti archivio certificati   | Oggetti disponibili per l'utilizzo di archivi certificati e certificati in tali archivi.                                       |
| Oggetti firma digitale   | Oggetti utilizzati per la firma digitale dei dati e per la verifica delle firme digitali.                                                      |
| Oggetti dati in busta      | Oggetti utilizzati per creare messaggi di dati in busta per la privacy e per decrittografare i dati nei messaggi in busta digitale.                      |
| Oggetti di crittografia dei dati     | Oggetti usati per crittografare i dati e decrittografare i dati crittografati.                                                                |
| Oggetti ausiliari           | Oggetti utilizzati per modificare i comportamenti predefiniti e per gestire i certificati, gli archivi certificati e i messaggi dell'interfaccia utente. |
| Interfacce di interoperabilità | Interfacce che consentono di usare le derivazioni di CryptoAPI insieme a capicol 2,0.                                          |
| Tipi di enumerazione           | Tipi di enumerazione usati con CAPICOM.                                                                                       |



 

## <a name="certificate-store-objects"></a>Oggetti archivio certificati

Gli oggetti seguenti funzionano con gli [*archivi certificati*](../secgloss/c-gly.md) e i certificati in tali archivi. CAPICOM supporta l'uso degli archivi certificati utente corrente, computer locale, memoria e Active Directory.



| Oggetto                                             | Descrizione                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Certificato**](certificate.md)                 | Un singolo certificato digitale.                                                                                           |
| [**CertificatePolicies**](certificatepolicies.md) | Raccolta di oggetti [**PolicyInformation**](policyinformation.md) .                                                 |
| [**Certificati**](certificates.md)               | Raccolta di oggetti [**Certificate**](certificate.md) .                                                               |
| [**CertificateStatus**](certificatestatus.md)     | Fornisce informazioni sullo stato di un certificato.                                                                           |
| [**Catena**](chain.md)                             | Crea e verifica una catena di convalida del certificato basata su un certificato digitale.                                       |
| [**ExtendedProperties**](extendedproperties.md)   | Rappresenta una raccolta di oggetti [**ExtendedProperty**](extendedproperty.md) .                                        |
| [**ExtendedProperty**](extendedproperty.md)       | Rappresenta una proprietà estesa a Microsoft.                                                                               |
| [**Estensione**](extension.md)                     | Rappresenta una singola estensione del certificato.                                                                              |
| [**Estensioni**](extensions.md)                   | Rappresenta una raccolta di oggetti di [**estensione**](extension.md) .                                                      |
| [**PrivateKey**](privatekey.md)                   | Rappresenta una chiave privata.                                                                                               |
| [**PublicKey**](publickey.md)                     | Rappresenta una chiave pubblica in un oggetto [**certificato**](certificate.md) .                                                 |
| [**Store**](store.md)                             | Fornisce le proprietà e i metodi per scegliere, gestire e usare gli archivi certificati e i certificati in tali archivi. |
| [**Modello**](template.md)                       | Rappresenta il modello di estensione del certificato del certificato.                                                       |



 

## <a name="digital-signature-objects"></a>Oggetti firma digitale

Gli oggetti seguenti vengono esportati per la firma digitale dei dati e per la verifica delle firme digitali.



| Oggetto                           | Descrizione                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Fornisce funzionalità per la firma di contenuto con una firma digitale Authenticode. |
| [**SignedData**](signeddata.md) | Oggetto utilizzato per firmare i dati e verificare la firma sui dati firmati.               |
| [**Firmatario**](signer.md)         | Informazioni su un singolo firmatario di dati, incluso il certificato del firmatario.           |
| [**Firmatari**](signers.md)       | Raccolta di oggetti [**firmatari**](signer.md) .                                    |



 

## <a name="enveloped-data-objects"></a>Oggetti dati in busta

Gli oggetti seguenti vengono esportati per creare messaggi di dati in busta per la privacy e per decrittografare i dati nei messaggi in busta digitale.



| Oggetto                                 | Descrizione                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnvelopedData**](envelopeddata.md) | Oggetti utilizzati per creare, inviare e ricevere dati in busta. I dati in busta digitale vengono crittografati in modo che solo i destinatari desiderati possano decrittografarli. |
| [**Destinatari**](recipients.md)       | Raccolta degli oggetti [**certificato**](certificate.md) dei destinatari desiderati di un messaggio in busta digitale.                           |



 

## <a name="data-encryption-objects"></a>Oggetti di crittografia dei dati

L'oggetto seguente viene esportato per crittografare i dati arbitrari per la privacy e per decrittografare i dati crittografati.



| Oggetto                                 | Descrizione                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**EncryptedData**](encrypteddata.md) | Oggetti utilizzati per crittografare i dati. I dati crittografati in un oggetto [**EncryptedData**](encrypteddata.md) possono essere decrittografati. |



 

## <a name="auxiliary-objects"></a>Oggetti ausiliari

Gli oggetti seguenti vengono esportati per modificare i comportamenti predefiniti di altri oggetti e per gestire certificati, archivi certificati e messaggi.



| Oggetto                                         | Descrizione                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](algorithm.md)                 | Imposta l'algoritmo e la [*lunghezza della chiave*](../secgloss/k-gly.md) da utilizzare nelle operazioni di crittografia. |
| [**Attributo**](attribute.md)                 | Fornisce una singola parte di informazioni aggiuntive su una firma, ad esempio l'ora di firma.                                                    |
| [**Attributi**](attributes.md)               | Raccolta di oggetti [**attributo**](attribute.md) .                                                                                           |
| [**BasicConstraints**](basicconstraints.md)   | Fornisce accesso in sola lettura ai vincoli di base sull'utilizzo di un certificato.                                                                    |
| [**EKU**](eku.md)                             | Fornisce l'accesso alle proprietà EKU dei certificati.                                                                                              |
| [**EKU**](ekus.md)                           | Raccolta di oggetti [**EKU**](eku.md) .                                                                                                       |
| [**EncodedData**](encodeddata.md)             | Rappresenta un blocco di dati codificati.                                                                                                             |
| [**ExtendedKeyUsage**](extendedkeyusage.md)   | Fornisce accesso in sola lettura alle proprietà di utilizzo chiavi estese dei certificati.                                                                 |
| [**HashedData**](hasheddata.md)               | Fornisce la funzionalità per l'applicazione di un algoritmo hash a una stringa.                                                                               |
| [**KeyUsage**](keyusage.md)                   | Fornisce accesso in sola lettura alle proprietà di utilizzo chiave dei certificati.                                                                              |
| [**OID**](oid.md)                             | Rappresenta un identificatore di oggetto utilizzato da diverse proprietà di CAPICOM.                                                                     |
| [**OID**](oids.md)                           | Rappresenta una raccolta di oggetti [**OID**](oid.md) .                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Consente di accedere ai criteri OID di un'estensione.                                                                                             |
| [**Qualifier**](qualifier.md)                 | Rappresenta un puntatore CPS (Certification Practice Statement) o un qualificatore di avviso utente.                                                           |
| [**Qualificatori**](qualifiers.md)               | Rappresenta una raccolta di qualificatori.                                                                                                          |
| [**Impostazioni**](settings.md)                   | Abilita o Disabilita le finestre di dialogo per richiedere l'identità del firmatario o del mittente se tale identità non è specificata.                                     |
| [**Utilità**](utilities.md)                 | Fornisce funzionalità per le attività comuni.                                                                                                        |



 

## <a name="interoperability-interfaces"></a>Interfacce di interoperabilità

Le interfacce seguenti consentono di usare le derivazioni di CryptoAPI insieme a capicol 2,0.



| Interfaccia                              | Descrizione                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertContext**](icertcontext.md)   | Consente di accedere al contesto di un oggetto [**certificato**](certificate.md) CAPICOM X. 509v3. Questo contesto consente l'uso del certificato di CAPICOM in altre derivazioni di CryptoAPI. |
| [**ICertStore**](icertstore.md)       | Consente di accedere al contesto di un oggetto [**Archivio**](store.md) CAPICOM. Questo contesto consente l'uso dell'archivio certificati CAPICOM in altre derivazioni di CryptoAPI.               |
| [**IChainContext**](ichaincontext.md) | Fornisce l'accesso al contesto di un oggetto [**Chain**](chain.md) di capico. Questo contesto consente l'uso della catena di certificati del certificato CAPICOM in altre derivazioni di CryptoAPI.         |



 

## <a name="enumeration-types"></a>Tipi di enumerazione

CAPICOM definisce i tipi di enumerazione seguenti:

-   [**\_percorso di ricerca di \_ Active \_ directory \_ di CAPICOM**](capicom-active-directory-search-location.md)
-   [**CAPICOM ( \_ attributo)**](capicom-attribute.md)
-   [**tipo di informazioni del \_ certificato CAPICOM \_ \_**](capicom-cert-info-type.md)
-   [**tipo di ricerca del certificato capicol \_ \_ \_**](capicom-certificate-find-type.md)
-   [**\_ \_ opzione Includi certificato capicol \_**](capicom-certificate-include-option.md)
-   [**nome del certificato capicol \_ \_ Salva \_ come \_**](capicom-certificate-save-as-type.md)
-   [**i certificati capicol \_ \_ salvano \_ come \_ tipo**](capicom-certificates-save-as-type.md)
-   [**\_flag di controllo CAPICOM \_**](capicom-check-flag.md)
-   [**EKU di CAPICOM \_**](capicom-eku.md)
-   [**\_tipo di codifica CAPICOM \_**](capicom-encoding-type.md)
-   [**\_algoritmo di crittografia CAPICOM \_**](capicom-encryption-algorithm.md)
-   [**lunghezza della chiave di \_ crittografia CAPICOM \_ \_**](capicom-encryption-key-length.md)
-   [**codice di errore di CAPICOM \_ \_**](capicom-error-code.md)
-   [**\_flag di esportazione CAPICOM \_**](capicom-export-flag.md)
-   [**\_algoritmo hash CAPICOM \_**](capicom-hash-algorithm.md)
-   [**\_percorso della chiave CAPICOM \_**](capicom-key-location.md)
-   [**specifica chiave capicol \_ \_**](capicom-key-spec.md)
-   [**FLAG di archiviazione della \_ chiave CAPICOM \_ \_**](capicom-key-storage-flag.md)
-   [**\_OID CAPICOM**](capicom-oid.md)
-   [**CAPICOM \_ propid**](capicom-propid.md)
-   [**tipo capicol \_ dimostrativo \_**](capicom-prov-type.md)
-   [**tipo di segreto capicot \_ \_**](capicom-secret-type.md)
-   [**\_ \_ flag di verifica dati firmati capicol \_ \_**](capicom-signed-data-verify-flag.md)
-   [**\_percorso archivio CAPICOM \_**](capicom-store-location.md)
-   [**\_modalità di apertura archivio \_ CAPICOM \_**](capicom-store-open-mode.md)
-   [**\_ \_ Salva \_ come tipo di archivio \_ CAPICOM**](capicom-store-save-as-type.md)

 

 
