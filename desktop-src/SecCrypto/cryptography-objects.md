---
description: Elenca gli oggetti forniti da CryptoAPI.
ms.assetid: 4ab16355-1341-4c7a-b570-bd33f11dde00
title: Oggetti Cryptography
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea3476e7edad1d32fe1e11635bd65622d2a8375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401651"
---
# <a name="cryptography-objects"></a>Oggetti Cryptography

Gli oggetti di crittografia sono suddivisi in categorie in base all'utilizzo come indicato di seguito:

-   [Oggetti archivio certificati](#certificate-store-objects)
-   [Oggetti firma digitale](#digital-signature-objects)
-   [Oggetti dati in busta](#enveloped-data-objects)
-   [Oggetti di crittografia dei dati](#data-encryption-objects)
-   [Oggetti ausiliari](#auxiliary-objects)
-   [Oggetti di registrazione del certificato](#certificate-enrollment-objects)

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
| [**ExtendedProperty**](extendedproperties.md)     | Rappresenta una proprietà estesa a Microsoft.                                                                               |
| [**Estensione**](extension.md)                     | Rappresenta una singola estensione del certificato.                                                                              |
| [**Estensioni**](extensions.md)                   | Rappresenta una raccolta di oggetti di [**estensione**](extension.md) .                                                      |
| [**PrivateKey**](privatekey.md)                   | Rappresenta una chiave privata.                                                                                               |
| [**PublicKey**](publickey.md)                     | Rappresenta una chiave pubblica in un oggetto [**certificato**](certificate.md) .                                                 |
| [**Store**](store.md)                             | Fornisce le proprietà e i metodi per scegliere, gestire e usare gli archivi certificati e i certificati in tali archivi. |
| [**Modello**](template.md)                       | Rappresenta il modello di estensione del certificato del certificato.                                                       |



 

## <a name="digital-signature-objects"></a>Oggetti firma digitale

Gli oggetti seguenti vengono esportati per la firma digitale dei dati e per la verifica delle firme digitali.



| Oggetto                           | Descrizione                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Oggetto utilizzato per firmare il codice con una firma digitale Authenticode e per verificare la firma sul codice firmato. |
| [**SignedData**](signeddata.md) | Oggetto utilizzato per firmare i dati e verificare la firma sui dati firmati.                                        |
| [**Firmatario**](signer.md)         | Informazioni su un singolo firmatario di dati, incluso il certificato del firmatario.                                    |
| [**Firmatari**](signers.md)       | Raccolta di oggetti [**firmatari**](signer.md) .                                                             |



 

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
| [**NoticeNumbers**](noticenumbers.md)         | Rappresenta una raccolta di oggetti di [**estensione**](extension.md) .                                                                              |
| [**OID**](oid.md)                             | Rappresenta un identificatore di oggetto utilizzato da diverse proprietà di CAPICOM.                                                                     |
| [**OID**](oids.md)                           | Rappresenta una raccolta di oggetti [**OID**](oid.md) .                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Consente di accedere ai criteri OID di un'estensione.                                                                                             |
| [**Qualifier**](qualifier.md)                 | Rappresenta un puntatore CPS (Certification Practice Statement) o un qualificatore di avviso utente.                                                           |
| [**Qualificatori**](qualifiers.md)               | Rappresenta una raccolta di qualificatori.                                                                                                          |
| [**Impostazioni**](settings.md)                   | Abilita o Disabilita le finestre di dialogo per richiedere l'identità del firmatario o del mittente se tale identità non è specificata.                                     |
| [**Utilità**](utilities.md)                 | Fornisce funzionalità per le attività comuni.                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a>Oggetti di registrazione del certificato

L'oggetto seguente viene usato per la registrazione del certificato.



| Oggetto                     | Descrizione                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)) | Oggetto che rappresenta il controllo di registrazione del certificato. Viene utilizzato principalmente per la programmazione in Visual Basic o in un altro linguaggio di automazione. |



 

 

 
