---
description: È possibile usare l'interfaccia IX509Extension per definire un'estensione arbitraria.
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: Estensioni supportate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0362bc289e8f0631520a7d9d56ff4bed1af2c698c721db703b27b0ecee5a1629
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101110"
---
# <a name="supported-extensions"></a>Estensioni supportate

È possibile usare [**l'interfaccia IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) per definire un'estensione arbitraria. L'API di registrazione certificati fornisce anche interfacce derivate da **IX509Extension** per consentire di creare facilmente una delle estensioni più comuni. Nell'elenco seguente vengono identificate le estensioni comuni supportate dalle autorità di certificazione Microsoft e gli identificatori di oggetto e le interfacce che è possibile utilizzare per crearle.

## <a name="alternativenames"></a>AlternativeNames

L'estensione dei nomi alternativi può essere usata per definire uno o più moduli di nomi alternativi per l'oggetto della richiesta di certificato. Esempi di forme alternative includono indirizzi email, nomi DNS; indirizzi IP e URI.

**Interfaccia:** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)

**OID:** XCN \_ OID \_ SUBJECT ALT \_ \_ NAME2 (2.5.29.17)

## <a name="authorityinformationaccess"></a>AuthorityInformationAccess

L'estensione di accesso alle informazioni dell'autorità identifica come accedere alle informazioni e ai servizi della CA. Il valore dell'estensione contiene una sequenza di URI.

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ AUTHORITY INFO ACCESS \_ \_ (1.3.6.1.5.5.7.1.1)

## <a name="authoritykeyidentifier"></a>AuthorityKeyIdentifier

L'estensione dell'identificatore di chiave dell'autorità consente l'identificazione della chiave pubblica della CA corrispondente alla chiave privata della CA che ha firmato un certificato emesso. Viene usato dal software di creazione del percorso del certificato in un server Windows per trovare il certificato della CA. Quando un'autorità di certificazione emissione di un certificato, il valore dell'estensione viene impostato su uguale **all'estensione SubjectKeyIdentifier** nel certificato di firma della CA. Il valore è in genere un hash SHA-1 della chiave pubblica.

**Interfaccia:** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)

**OID:** XCN \_ OID \_ AUTHORITY KEY \_ \_ IDENTIFIER2 (2.5.29.35)

## <a name="basicconstraints"></a>Proprietà BasicConstraints

L'estensione dei vincoli di base può essere usata per identificare se l'entità può essere utilizzata come autorità di certificazione (CA) e, in tal caso, il numero di CA subordinate che possono esistere sotto di essa nella catena di certificati.

**Interfaccia:** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)

**OID:** XCN \_ OID \_ BASIC \_ CONSTRAINTS2 (2.5.29.19)

## <a name="certificatepolicies"></a>CertificatePolicies

L'estensione dei criteri certificato può essere usata per identificare i criteri in base ai quali è stato emesso il certificato e gli scopi per cui può essere usato. Questi sono identificati da una raccolta di identificatori di oggetto (OID). I criteri vengono personalizzati in base ai requisiti di un'organizzazione.

**Interfaccia:** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)

**OID:** XCN \_ OID \_ CERT \_ POLICIES (2.5.29.32)

## <a name="crldistributionpoints"></a>CrlDistributionPoints

L'estensione dei punti di distribuzione dell'elenco di revoche di certificati (CRL) contiene l'URI dell'elenco di revoche di certificati (CRL) di base.

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ CRL \_ DIST \_ POINTS (2.5.29.31)

## <a name="enhancedkeyusage"></a>EnhancedKeyUsage

L'estensione per l'utilizzo chiavi avanzato può essere usata per definire uno o più usi della chiave pubblica contenuta nel certificato.

**Interfaccia:** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)

**OID:** UTILIZZO CHIAVI AVANZATO OID XCN \_ \_ \_ \_ (2.5.29.37)

## <a name="freshestcrl"></a>FreshestCRL

L'estensione CRL più recente contiene l'URI del delta CRL. La stessa sintassi ASN.1 viene usata per questa estensione e **l'estensione CrlDistributionPoints.**

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ FRESHEST \_ CRL (2.5.29.46)

## <a name="keyusage"></a>KeyUsage

L'estensione per l'utilizzo delle chiavi può essere usata per definire restrizioni sulle operazioni che possono essere eseguite dalla chiave pubblica contenuta nel certificato. Ad esempio, è possibile specificare che la chiave pubblica deve essere usata solo per creare una firma digitale, firmare un elenco di revoche di certificati (CRL) o crittografare un'altra chiave.

**Interfaccia:** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)

**OID:** UTILIZZO DELLA CHIAVE OID XCN \_ \_ \_ (2.5.29.15)

## <a name="msapplicationpolicies"></a>MSApplicationPolicies

L'estensione dei criteri di applicazione Microsoft può essere usata da un'applicazione per filtrare i certificati in base all'uso consentito. Gli usi consentiti sono identificati dagli OID. Questa estensione è simile **all'estensione EnhancedKeyUsage,** ma con semantica più rigida applicata alla CA padre. L'estensione è specifica di Microsoft.

**Interfaccia:** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)

**OID:** XCN \_ OID \_ APPLICATION \_ CERT POLICIES \_ (1.3.6.1.4.1.311.21.10)

## <a name="nameconstraints"></a>Proprietà NameConstraints

L'estensione dei vincoli di nome viene utilizzata per identificare lo spazio dei nomi all'interno del quale devono trovarsi tutti i nomi di soggetto dei certificati in una gerarchia di certificati. L'estensione è usata solo in un certificato di autorità di certificazione.

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** VINCOLI DEI NOMI OID XCN \_ \_ \_ (2.5.29.30)

## <a name="policyconstraints"></a>Proprietà PolicyConstraints

L'estensione dei vincoli dei criteri viene aggiunta ai certificati della CA per vincolare la convalida del percorso proibindo il mapping dei criteri o richiedendo che ogni certificato nella gerarchia contenga un identificatore di criteri accettabile.

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** VINCOLI DEI CRITERI OID XCN \_ \_ \_ (2.5.29.36)

## <a name="policymappings"></a>PolicyMappings

L'estensione dei mapping dei criteri viene usata per identificare i criteri in una CA subordinata che corrispondono ai criteri nella CA emittente. Il valore dell'estensione contiene una sequenza di mapping dei criteri della CA emittente e della CA subordinata rappresentati da identificatori di oggetto.

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** MAPPING DEI CRITERI OID XCN \_ \_ \_ (2.5.29.33)

## <a name="privatekeyusageperiod"></a>PrivateKeyUsagePeriod

L'estensione del periodo di utilizzo della chiave privata viene usata per specificare un periodo di validità diverso per la chiave privata rispetto al certificato a cui è associata la chiave.

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ PRIVATEKEY \_ USAGE PERIOD \_ (2.5.29.16)

## <a name="smimecapabilities"></a>SmimeCapabilities

L'estensione delle funzionalità Secure/Multipurpose Internet Mail Extensions (S/MIME) può essere usata per segnalare le funzionalità di decrittografia di un destinatario di posta elettronica al mittente del messaggio di posta elettronica in modo che il mittente possa scegliere l'algoritmo di crittografia più sicuro supportato da entrambe le parti. Il valore dell'estensione contiene una raccolta di OID dell'algoritmo di crittografia simmetrica e un livello di crittografia facoltativo per ognuno.

**Interfaccia:** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)

**OID:** XCN \_ OID \_ RSA \_ SMIMECapabilities (1.2.840.113549.1.9.15)

## <a name="subjectdirectoryattributes"></a>SubjectDirectoryAttributes

L'estensione degli attributi della directory del soggetto può essere usata per comunicare gli attributi di identificazione, ad esempio la nazionalità del soggetto del certificato. Il valore dell'estensione è una sequenza di coppie di valori OID.

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ SUBJECT \_ DIR \_ ATTRS (2.5.29.9)

## <a name="subjectkeyidentifier"></a>SubjectKeyIdentifier

L'estensione dell'identificatore di chiave del soggetto può essere usata per distinguere tra più chiavi pubbliche utilizzate dal soggetto del certificato. Il valore dell'estensione è in genere un hash SHA-1 della chiave.

**Interfaccia:** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)

**OID:** IDENTIFICATORE DELLA CHIAVE DEL SOGGETTO OID XCN \_ \_ \_ \_ (2.5.29.14)

## <a name="template"></a>Modello

L'estensione del modello può essere usata per identificare il modello della versione 2 da usare quando si emette o si rinnova un certificato. Il valore dell'estensione contiene l'OID del modello e informazioni facoltative sulla versione. L'estensione è specifica di Microsoft.

**Interfaccia:** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)

**OID:** MODELLO DI CERTIFICATO OID XCN \_ \_ \_ (1.3.6.1.4.1.311.21.7)

## <a name="templatename"></a>Templatename

L'estensione del nome del modello può essere usata per identificare il modello della versione 1 da usare quando si emette o si rinnova un certificato. Il valore dell'estensione contiene il nome del modello. L'estensione è specifica di Microsoft.

**Interfaccia:** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

**OID:** ESTENSIONE XCN \_ OID \_ ENROLL \_ CERTTYPE \_ (1.3.6.1.4.1.311.20.2)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Estensioni](extensions.md)
</dt> </dl>

 

 



