---
description: Elenca gli oggetti forniti da CryptoAPI.
ms.assetid: 4ab16355-1341-4c7a-b570-bd33f11dde00
title: Oggetti di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff5e9495d64c38272bac54ffac03d1d087b9286887b4e4e520c6a447765efac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768373"
---
# <a name="cryptography-objects"></a>Oggetti di crittografia

Gli oggetti di crittografia vengono classificati in base all'utilizzo come segue:

-   [Oggetti archivio certificati](#certificate-store-objects)
-   [Oggetti firma digitale](#digital-signature-objects)
-   [Oggetti dati in busta](#enveloped-data-objects)
-   [Oggetti di crittografia dei dati](#data-encryption-objects)
-   [Oggetti ausiliari](#auxiliary-objects)
-   [Oggetti di registrazione certificati](#certificate-enrollment-objects)

## <a name="certificate-store-objects"></a>Oggetti archivio certificati

Gli oggetti seguenti funzionano con [*gli archivi certificati*](../secgloss/c-gly.md) e i certificati in tali archivi. CAPICOM supporta l'uso di utenti correnti, computer locale, memoria e archivi certificati di Active Directory.



| Oggetto                                             | Descrizione                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Certificato**](certificate.md)                 | Un singolo certificato digitale.                                                                                           |
| [**CertificatePolicies**](certificatepolicies.md) | Raccolta di [**oggetti PolicyInformation.**](policyinformation.md)                                                 |
| [**Certificati**](certificates.md)               | Raccolta di [**oggetti**](certificate.md) Certificate.                                                               |
| [**CertificateStatus**](certificatestatus.md)     | Fornisce informazioni sullo stato di un certificato.                                                                           |
| [**Catena**](chain.md)                             | Crea e controlla una catena di convalida del certificato basata su un certificato digitale.                                       |
| [**ExtendedProperties**](extendedproperties.md)   | Rappresenta una raccolta di [**oggetti ExtendedProperty.**](extendedproperty.md)                                        |
| [**Extendedproperty**](extendedproperties.md)     | Rappresenta una proprietà estesa da Microsoft.                                                                               |
| [**Estensione**](extension.md)                     | Rappresenta una singola estensione di certificato.                                                                              |
| [**Estensioni**](extensions.md)                   | Rappresenta una raccolta di [**oggetti Extension.**](extension.md)                                                      |
| [**PrivateKey**](privatekey.md)                   | Rappresenta una chiave privata.                                                                                               |
| [**Publickey**](publickey.md)                     | Rappresenta una chiave pubblica in un [**oggetto**](certificate.md) Certificate.                                                 |
| [**Archiviazione**](store.md)                             | Fornisce le proprietà e i metodi per scegliere, gestire e utilizzare gli archivi certificati e i certificati in tali archivi. |
| [**Modello**](template.md)                       | Rappresenta il modello di estensione del certificato.                                                       |



 

## <a name="digital-signature-objects"></a>Oggetti firma digitale

Gli oggetti seguenti vengono esportati per firmare digitalmente i dati e per verificare le firme digitali.



| Oggetto                           | Descrizione                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Oggetto usato per firmare il codice con una firma digitale Authenticode e per verificare la firma nel codice firmato. |
| [**SignedData**](signeddata.md) | Oggetto utilizzato per firmare i dati e per verificare la firma sui dati firmati.                                        |
| [**Firmatario**](signer.md)         | Informazioni su un singolo firmatario di dati, incluso il certificato del firmatario.                                    |
| [**Firmatari**](signers.md)       | Raccolta di [**oggetti Signer.**](signer.md)                                                             |



 

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
| [**NoticeNumbers**](noticenumbers.md)         | Rappresenta una raccolta di [**oggetti Extension.**](extension.md)                                                                              |
| [**Oid**](oid.md)                             | Rappresenta un identificatore di oggetto utilizzato da diverse proprietà CAPICOM.                                                                     |
| [**Oid**](oids.md)                           | Rappresenta una raccolta di [**oggetti OID.**](oid.md)                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Fornisce l'accesso agli OID dei criteri di un'estensione.                                                                                             |
| [**Qualifier**](qualifier.md)                 | Rappresenta un puntatore CPS (Certification Practice Statement) o un qualificatore di avviso utente.                                                           |
| [**Qualificatori**](qualifiers.md)               | Rappresenta una raccolta di qualificatori.                                                                                                          |
| [**Impostazioni**](settings.md)                   | Abilita o disabilita le finestre di dialogo per richiedere l'identità del firmatario o del mittente se tale identità non è specificata.                                     |
| [**Utilità**](utilities.md)                 | Fornisce funzionalità per le attività comuni.                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a>Oggetti di registrazione certificati

L'oggetto seguente viene usato per la registrazione del certificato.



| Oggetto                     | Descrizione                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Registrazione di C**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)) | Oggetto che rappresenta il controllo di registrazione certificati. Viene usato principalmente quando si esegue la programmazione in Visual Basic o in un altro linguaggio di automazione. |



 

 

 
