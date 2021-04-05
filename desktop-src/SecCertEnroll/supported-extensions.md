---
description: È possibile usare l'interfaccia IX509Extension per definire un'estensione arbitraria.
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: Estensioni supportate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd55886b03cdea5783f918182c84382910510918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752162"
---
# <a name="supported-extensions"></a>Estensioni supportate

È possibile usare l'interfaccia [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) per definire un'estensione arbitraria. L'API di registrazione certificati fornisce anche le interfacce derivate da **IX509Extension** per consentire di creare facilmente le estensioni più comuni. Nell'elenco seguente vengono identificate le estensioni comuni supportate dalle autorità di certificazione Microsoft e gli identificatori e le interfacce di oggetto che è possibile utilizzare per crearli.

## <a name="alternativenames"></a>AlternativeNames

L'estensione dei nomi alternativi può essere usata per definire uno o più moduli nome alternativi per l'oggetto della richiesta di certificato. Esempi di forme alternative includono indirizzi email, nomi DNS; indirizzi IP e URI.

**Interfaccia:** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)

**OID:** \_Oggetto Oid \_ XCN \_ ALT \_ name2 (2.5.29.17)

## <a name="authorityinformationaccess"></a>AuthorityInformationAccess

L'estensione di accesso alle informazioni sull'autorità identifica come accedere alle informazioni e ai servizi della CA. Il valore dell'estensione contiene una sequenza di URI.

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ Authority \_ info \_ Access (1.3.6.1.5.5.7.1.1)

## <a name="authoritykeyidentifier"></a>AuthorityKeyIdentifier

L'estensione dell'identificatore di chiave dell'autorità consente l'identificazione della chiave pubblica dell'autorità di certificazione che corrisponde alla chiave privata della CA che ha firmato un certificato emesso. Viene usato dal percorso del certificato per la creazione di software in un server Windows per trovare il certificato della CA. Quando un'autorità di certificazione emette un certificato, il valore dell'estensione viene impostato in modo uguale all'estensione **SubjectKeyIdentifier** nel certificato di firma della CA. Il valore è in genere un hash SHA-1 della chiave pubblica.

**Interfaccia:** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)

**OID:** \_Chiave dell' \_ autorità OID XCN \_ \_ IDENTIFIER2 (2.5.29.35)

## <a name="basicconstraints"></a>BasicConstraints

L'estensione dei vincoli di base può essere usata per determinare se l'entità può essere usata come autorità di certificazione (CA) e, in caso affermativo, il numero di CA subordinate che possono esistere al di sotto di esso nella catena di certificati.

**Interfaccia:** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)

**OID:** XCN \_ OID \_ Basic \_ CONSTRAINTS2 (2.5.29.19)

## <a name="certificatepolicies"></a>CertificatePolicies

È possibile utilizzare l'estensione criteri certificati per identificare i criteri con cui il certificato è stato emesso ed è possibile utilizzarne gli scopi. Sono identificati da una raccolta di identificatori di oggetto (OID). I criteri vengono personalizzati per i requisiti di un'organizzazione.

**Interfaccia:** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)

**OID:** \_ \_ Criteri certificato OID XCN \_ (2.5.29.32)

## <a name="crldistributionpoints"></a>CrlDistributionPoints

L'estensione dei punti di distribuzione dell'elenco di revoche di certificati (CRL) contiene l'URI dell'elenco di revoche di certificati (CRL) di base.

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ CRL \_ punti di dist \_ (2.5.29.31)

## <a name="enhancedkeyusage"></a>Campo EnhancedKeyUsage

L'estensione utilizzo chiavi avanzato può essere usata per definire uno o più usi della chiave pubblica contenuta nel certificato.

**Interfaccia:** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)

**OID:** \_ \_ Utilizzo chiavi avanzato OID XCN \_ \_ (2.5.29.37)

## <a name="freshestcrl"></a>FreshestCRL

L'estensione CRL più aggiornata contiene l'URI del Delta CRL. Per questa estensione e l'estensione **CrlDistributionPoints** viene utilizzata la stessa sintassi ASN. 1.

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID più \_ recente \_ CRL (2.5.29.46)

## <a name="keyusage"></a>KeyUsage

L'estensione utilizzo chiave può essere utilizzata per definire restrizioni sulle operazioni che possono essere eseguite dalla chiave pubblica contenuta nel certificato. Ad esempio, è possibile specificare che la chiave pubblica deve essere utilizzata solo per creare una firma digitale, firmare un elenco di revoche di certificati (CRL) o crittografare un'altra chiave.

**Interfaccia:** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)

**OID:** \_ \_ Utilizzo chiave OID XCN \_ (2.5.29.15)

## <a name="msapplicationpolicies"></a>MSApplicationPolicies

L'estensione criteri per le applicazioni Microsoft può essere utilizzata da un'applicazione per filtrare i certificati sulla base dell'utilizzo consentito. Gli utilizzi consentiti sono identificati da OID. Questa estensione è simile all'estensione **campo EnhancedKeyUsage** ma con una semantica più restrittiva applicata alla CA padre. L'estensione è specifica di Microsoft.

**Interfaccia:** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)

**OID:** \_Criteri del \_ certificato dell'applicazione OID XCN \_ \_ (1.3.6.1.4.1.311.21.10)

## <a name="nameconstraints"></a>NameConstraints

L'estensione vincoli di nome viene utilizzata per identificare lo spazio dei nomi nel quale devono essere individuati tutti i nomi soggetto dei certificati in una gerarchia di certificati. L'estensione è usata solo in un certificato di autorità di certificazione.

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** \_Vincoli di \_ nome OID XCN \_ (2.5.29.30)

## <a name="policyconstraints"></a>PolicyConstraints

L'estensione dei vincoli di criteri viene aggiunta ai certificati della CA per limitare la convalida del percorso proibindo il mapping dei criteri o richiedendo che ogni certificato nella gerarchia contenga un identificatore di criterio accettabile.

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** \_Vincoli dei \_ criteri OID XCN \_ (2.5.29.36)

## <a name="policymappings"></a>PolicyMappings

L'estensione mapping dei criteri viene usata per identificare i criteri in una CA subordinata che corrispondono ai criteri nella CA emittente. Il valore dell'estensione contiene una sequenza di autorità di certificazione emittente e mapping dei criteri della CA subordinata rappresentati dagli identificatori di oggetto.

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** \_Mapping dei \_ criteri OID XCN \_ (2.5.29.33)

## <a name="privatekeyusageperiod"></a>PrivateKeyUsagePeriod

L'estensione del periodo di utilizzo della chiave privata viene usata per specificare un periodo di validità diverso per la chiave privata rispetto al certificato a cui è associata la chiave.

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ OID \_ PRIVATEKEY \_ periodo di utilizzo \_ (2.5.29.16)

## <a name="smimecapabilities"></a>SmimeCapabilities

L'estensione delle funzionalità Secure/Multipurpose Internet Mail Extensions (S/MIME) può essere usata per segnalare le funzionalità di decrittografia di un destinatario di posta elettronica al mittente del messaggio di posta elettronica, in modo che il mittente possa scegliere l'algoritmo di crittografia più sicuro supportato da entrambe le parti. Il valore dell'estensione contiene una raccolta di algoritmi di crittografia simmetrica OID e un livello di crittografia facoltativo per ciascuno di essi.

**Interfaccia:** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)

**OID:** \_OID XCN \_ RSA \_ SMIMECapabilities (1.2.840.113549.1.9.15)

## <a name="subjectdirectoryattributes"></a>SubjectDirectoryAttributes

L'estensione degli attributi della directory oggetto può essere utilizzata per fornire attributi di identificazione, ad esempio la cittadinanza del soggetto del certificato. Il valore dell'estensione è una sequenza di coppie di valori OID.

**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID:** XCN \_ \_ oggetto Oid \_ \_ attrs (2.5.29.9)

## <a name="subjectkeyidentifier"></a>SubjectKeyIdentifier

L'estensione dell'identificatore di chiave del soggetto può essere usata per distinguere tra più chiavi pubbliche utilizzate dal soggetto del certificato. Il valore dell'estensione è in genere un hash SHA-1 della chiave.

**Interfaccia:** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)

**OID:** \_Identificatore di chiave del soggetto XCN OID \_ \_ \_ (2.5.29.14)

## <a name="template"></a>Modello

L'estensione del modello può essere usata per identificare il modello della versione 2 da usare quando si emette o si rinnova un certificato. Il valore dell'estensione contiene l'OID del modello e le informazioni facoltative sulla versione. L'estensione è specifica di Microsoft.

**Interfaccia:** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)

**OID:** \_Modello di \_ certificato OID XCN \_ (1.3.6.1.4.1.311.21.7)

## <a name="templatename"></a>TemplateName

L'estensione del nome del modello può essere usata per identificare il modello della versione 1 da usare quando si emette o si rinnova un certificato. Il valore dell'estensione contiene il nome del modello. L'estensione è specifica di Microsoft.

**Interfaccia:** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

**OID:** XCN \_ OID \_ registrazione \_ \_ estensione tipo certificato (1.3.6.1.4.1.311.20.2)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Estensioni](extensions.md)
</dt> </dl>

 

 



