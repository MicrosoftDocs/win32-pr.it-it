---
description: Fornisce servizi che consentono agli sviluppatori di applicazioni di aggiungere sicurezza basata sulla crittografia alle applicazioni.
ms.assetid: 9a2add82-53f9-49ed-b20c-019f95e7d260
title: Informazioni di riferimento su CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94bd7f8c2052f53b4dc1e244251ba76c1b10e349e0f43434a926db6dbeb9190
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772112"
---
# <a name="capicom-reference"></a>Informazioni di riferimento su CAPICOM

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [Alternative all'uso di CAPICOM.](alternatives-to-using-capicom.md)\]

Il client COM CAPICOM fornisce servizi che consentono agli sviluppatori di applicazioni di aggiungere sicurezza basata [*sulla crittografia*](../secgloss/c-gly.md) alle applicazioni. CryptoAPI include funzionalità per l'autenticazione [*tramite*](../secgloss/d-gly.md)firme digitali, per l'ambiente dei messaggi e per la crittografia e la decrittografia dei dati.



| Category                    | Descrizione                                                                                                                |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Oggetti archivio certificati   | Oggetti disponibili per l'utilizzo degli archivi certificati e dei certificati in tali archivi.                                       |
| Oggetti firma digitale   | Oggetti utilizzati per firmare digitalmente i dati e per verificare le firme digitali.                                                      |
| Oggetti dati in busta      | Oggetti utilizzati per creare messaggi di dati in busta per la privacy e decrittografare i dati nei messaggi in busta.                      |
| Oggetti di crittografia dei dati     | Oggetti utilizzati per crittografare i dati e decrittografare i dati crittografati.                                                                |
| Oggetti ausiliari           | Oggetti utilizzati per modificare i comportamenti predefiniti e per gestire certificati, archivi certificati e messaggi dell'interfaccia utente. |
| Interfacce di interoperabilità | Interfacce che consentono alle derivazioni di CryptoAPI di funzionare insieme a CAPICOM 2.0.                                          |
| Tipi di enumerazione           | Tipi di enumerazione utilizzati con CAPICOM.                                                                                       |



 

## <a name="certificate-store-objects"></a>Oggetti archivio certificati

Gli oggetti seguenti funzionano con [*gli archivi certificati*](../secgloss/c-gly.md) e i certificati in tali archivi. CAPICOM supporta l'uso degli archivi certificati Utente corrente, Computer locale, Memoria e Active Directory.



| Oggetto                                             | Descrizione                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Certificato**](certificate.md)                 | Un singolo certificato digitale.                                                                                           |
| [**CertificatePolicies**](certificatepolicies.md) | Raccolta di [**oggetti PolicyInformation.**](policyinformation.md)                                                 |
| [**Certificati**](certificates.md)               | Raccolta di [**oggetti**](certificate.md) Certificate.                                                               |
| [**CertificateStatus**](certificatestatus.md)     | Fornisce informazioni sullo stato di un certificato.                                                                           |
| [**Catena**](chain.md)                             | Crea e controlla una catena di convalida del certificato basata su un certificato digitale.                                       |
| [**ExtendedProperties**](extendedproperties.md)   | Rappresenta una raccolta di [**oggetti ExtendedProperty.**](extendedproperty.md)                                        |
| [**Extendedproperty**](extendedproperty.md)       | Rappresenta una proprietà estesa da Microsoft.                                                                               |
| [**Estensione**](extension.md)                     | Rappresenta una singola estensione di certificato.                                                                              |
| [**Estensioni**](extensions.md)                   | Rappresenta una raccolta di [**oggetti Extension.**](extension.md)                                                      |
| [**PrivateKey**](privatekey.md)                   | Rappresenta una chiave privata.                                                                                               |
| [**Publickey**](publickey.md)                     | Rappresenta una chiave pubblica in un [**oggetto**](certificate.md) Certificate.                                                 |
| [**Archiviazione**](store.md)                             | Fornisce le proprietà e i metodi per scegliere, gestire e utilizzare gli archivi certificati e i certificati in tali archivi. |
| [**Modello**](template.md)                       | Rappresenta il modello di estensione del certificato.                                                       |



 

## <a name="digital-signature-objects"></a>Oggetti firma digitale

Gli oggetti seguenti vengono esportati per firmare digitalmente i dati e per verificare le firme digitali.



| Oggetto                           | Descrizione                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Fornisce funzionalità per firmare il contenuto con una firma digitale Authenticode. |
| [**SignedData**](signeddata.md) | Oggetto utilizzato per firmare i dati e per verificare la firma sui dati firmati.               |
| [**Firmatario**](signer.md)         | Informazioni su un singolo firmatario di dati, incluso il certificato del firmatario.           |
| [**Firmatari**](signers.md)       | Raccolta di [**oggetti Signer.**](signer.md)                                    |



 

## <a name="enveloped-data-objects"></a>Oggetti dati in busta

Gli oggetti seguenti vengono esportati per creare messaggi di dati in busta per la privacy e decrittografare i dati nei messaggi in busta.



| Oggetto                                 | Descrizione                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnvelopedData**](envelopeddata.md) | Oggetti utilizzati per creare, inviare e ricevere dati in busta. I dati in busta vengono crittografati in modo che solo i destinatari previsti possano decrittografarlo. |
| [**Destinatari**](recipients.md)       | Raccolta degli oggetti [**Certificato**](certificate.md) dei destinatari previsti di un messaggio in busta.                           |



 

## <a name="data-encryption-objects"></a>Oggetti di crittografia dei dati

L'oggetto seguente viene esportato per crittografare dati arbitrari per la privacy e decrittografare i dati crittografati.



| Oggetto                                 | Descrizione                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**Encrypteddata**](encrypteddata.md) | Oggetti utilizzati per crittografare i dati. I dati crittografati in un [**oggetto EncryptedData**](encrypteddata.md) possono essere decrittografati. |



 

## <a name="auxiliary-objects"></a>Oggetti ausiliari

Gli oggetti seguenti vengono esportati per modificare i comportamenti predefiniti di altri oggetti e per gestire certificati, archivi certificati e messaggi.



| Oggetto                                         | Descrizione                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](algorithm.md)                 | Imposta l'algoritmo [*e la lunghezza della*](../secgloss/k-gly.md) chiave da utilizzare nelle operazioni di crittografia. |
| [**Attributo**](attribute.md)                 | Fornisce un'unica informazione aggiunta su una firma, ad esempio l'ora della firma.                                                    |
| [**Attributi**](attributes.md)               | Raccolta di [**oggetti**](attribute.md) Attribute.                                                                                           |
| [**Proprietà BasicConstraints**](basicconstraints.md)   | Fornisce l'accesso in sola lettura ai vincoli di base sugli utilizzi di un certificato.                                                                    |
| [**EKU**](eku.md)                             | Fornisce l'accesso alle proprietà EKU dei certificati.                                                                                              |
| [**EKU**](ekus.md)                           | Raccolta di [**oggetti EKU.**](eku.md)                                                                                                       |
| [**EncodedData**](encodeddata.md)             | Rappresenta un blocco di dati codificati.                                                                                                             |
| [**ExtendedKeyUsage**](extendedkeyusage.md)   | Fornisce l'accesso in sola lettura alle proprietà estese di utilizzo delle chiavi dei certificati.                                                                 |
| [**HashedData**](hasheddata.md)               | Fornisce funzionalità per l'applicazione di un algoritmo hash a una stringa.                                                                               |
| [**KeyUsage**](keyusage.md)                   | Fornisce l'accesso in sola lettura alle proprietà di utilizzo delle chiavi dei certificati.                                                                              |
| [**Oid**](oid.md)                             | Rappresenta un identificatore di oggetto utilizzato da diverse proprietà CAPICOM.                                                                     |
| [**Oid**](oids.md)                           | Rappresenta una raccolta di [**oggetti OID.**](oid.md)                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Fornisce l'accesso agli OID dei criteri di un'estensione.                                                                                             |
| [**Qualifier**](qualifier.md)                 | Rappresenta un puntatore CPS (Certification Practice Statement) o un qualificatore di avviso utente.                                                           |
| [**Qualificatori**](qualifiers.md)               | Rappresenta una raccolta di qualificatori.                                                                                                          |
| [**Impostazioni**](settings.md)                   | Abilita o disabilita le finestre di dialogo per richiedere l'identità del firmatario o del mittente se tale identità non è specificata.                                     |
| [**Utilità**](utilities.md)                 | Fornisce funzionalità per le attività comuni.                                                                                                        |



 

## <a name="interoperability-interfaces"></a>Interfacce di interoperabilità

Le interfacce seguenti consentono alle derivazioni di CryptoAPI di funzionare insieme a CAPICOM 2.0.



| Interfaccia                              | Descrizione                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertContext**](icertcontext.md)   | Fornisce l'accesso al contesto di un oggetto certificato [](certificate.md) CAPICOM X.509v3. Questo contesto consente l'uso del certificato CAPICOM in altre derivazioni di CryptoAPI. |
| [**ICertStore**](icertstore.md)       | Fornisce l'accesso al contesto di un oggetto ARCHIVIO [**CAPICOM.**](store.md) Questo contesto consente l'uso dell'archivio certificati CAPICOM in altre derivazioni di CryptoAPI.               |
| [**IChainContext**](ichaincontext.md) | Fornisce l'accesso al contesto di un oggetto [**CapiCOM Chain.**](chain.md) Questo contesto consente l'uso della catena di attendibilità dei certificati CAPICOM in altre derivazioni di CryptoAPI.         |



 

## <a name="enumeration-types"></a>Tipi di enumerazione

CAPICOM definisce i tipi di enumerazione seguenti:

-   [**POSIZIONE DI \_ RICERCA DI CAPICOM ACTIVE \_ \_ \_ DIRECTORY**](capicom-active-directory-search-location.md)
-   [**ATTRIBUTO \_ CAPICOM**](capicom-attribute.md)
-   [**TIPO DI INFORMAZIONI SUL CERTIFICATO CAPICOM \_ \_ \_**](capicom-cert-info-type.md)
-   [**TIPO DI RICERCA CERTIFICATO CAPICOM \_ \_ \_**](capicom-certificate-find-type.md)
-   [**OPZIONE DI INCLUSIONE DEL CERTIFICATO CAPICOM \_ \_ \_**](capicom-certificate-include-option.md)
-   [**TIPO \_ DI CERTIFICATO CAPICOM \_ SALVA CON \_ \_ NOME**](capicom-certificate-save-as-type.md)
-   [**TIPO DI CERTIFICATI CAPICOM \_ \_ SALVA CON \_ \_ NOME**](capicom-certificates-save-as-type.md)
-   [**FLAG DI \_ CONTROLLO \_ CAPICOM**](capicom-check-flag.md)
-   [**CAPICOM \_ EKU**](capicom-eku.md)
-   [**TIPO DI CODIFICA \_ \_ CAPICOM**](capicom-encoding-type.md)
-   [**ALGORITMO DI CRITTOGRAFIA \_ \_ CAPICOM**](capicom-encryption-algorithm.md)
-   [**LUNGHEZZA DELLA CHIAVE \_ DI \_ CRITTOGRAFIA \_ CAPICOM**](capicom-encryption-key-length.md)
-   [**CODICE DI \_ ERRORE \_ CAPICOM**](capicom-error-code.md)
-   [**FLAG DI ESPORTAZIONE CAPICOM \_ \_**](capicom-export-flag.md)
-   [**ALGORITMO \_ HASH \_ CAPICOM**](capicom-hash-algorithm.md)
-   [**POSIZIONE \_ DELLA CHIAVE \_ CAPICOM**](capicom-key-location.md)
-   [**SPECIFICA \_ DELLA CHIAVE \_ CAPICOM**](capicom-key-spec.md)
-   [**FLAG DI ARCHIVIAZIONE DELLE CHIAVI CAPICOM \_ \_ \_**](capicom-key-storage-flag.md)
-   [**CAPICOM \_ OID**](capicom-oid.md)
-   [**CAPICOM \_ PROPID**](capicom-propid.md)
-   [**TIPO \_ DI PROV \_ CAPICOM**](capicom-prov-type.md)
-   [**TIPO DI SEGRETO CAPICOM \_ \_**](capicom-secret-type.md)
-   [**FLAG DI VERIFICA \_ \_ DEI DATI FIRMATI \_ CAPICOM \_**](capicom-signed-data-verify-flag.md)
-   [**POSIZIONE DELLO \_ STORE \_ CAPICOM**](capicom-store-location.md)
-   [**MODALITÀ DI \_ APERTURA \_ CAPICOM \_ STORE**](capicom-store-open-mode.md)
-   [**SALVA CON NOME IN CAPICOM \_ \_ \_ \_ STORE**](capicom-store-save-as-type.md)

 

 
