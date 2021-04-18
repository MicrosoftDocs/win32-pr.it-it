---
description: L'API di registrazione certificati supporta gli attributi seguenti. È possibile creare un singolo attributo usando l'interfaccia corrispondente identificata in ognuna delle sezioni seguenti.
ms.assetid: e14fd472-1974-4ad2-b35a-3ab58ba0d707
title: Attributi supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3bfff5785a0b891e98e6d78d59b4688e2d5c11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307701"
---
# <a name="supported-attributes"></a>Attributi supportati

L'API di registrazione certificati supporta gli attributi seguenti. È possibile creare un singolo attributo usando l'interfaccia corrispondente identificata in ognuna delle sezioni seguenti.

## <a name="clientid"></a>ClientId

L'interfaccia [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) può essere utilizzata per definire un attributo che contiene informazioni sul computer client che ha inviato la richiesta di certificato. Le informazioni possono essere usate per la diagnostica.

**Si applica a:** \#Richiesta PKCS 10 o CMC.

**OID:** \_Informazioni sul client di richiesta OID XCN \_ \_ \_ (1.3.6.1.4.1.311.21.20)

## <a name="extensions"></a>Estensioni

L'interfaccia [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) può essere usata per definire un set di estensioni del certificato X. 509 versione 3. Sono supportate le estensioni seguenti. Per ulteriori informazioni, vedere l'argomento interfacce di estensione.



| Estensione              | Descrizione                                                                                                                                                                                                                      |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlternativeNames       | Contiene una o più forme nome alternativo dell'emittente associata al certificato.                                                                                                                                       |
| AuthorityKeyIdentifier | Contiene un identificatore di chiave univoco per distinguere tra più chiavi di firma del certificato dell' [*autorità di certificazione*](/windows/desktop/SecGloss/c-gly) (CA). |
| BasicConstraints       | Indica se l'oggetto può fungere da autorità di certificazione.                                                                                                                                                                                   |
| CertificatePolicies    | Identifica i criteri e le informazioni facoltative sui qualificatori associati al certificato.                                                                                                                                      |
| MSApplicationPolicies  | Identifica uno o più utilizzi per il certificato. Questa estensione è simile all'estensione campo EnhancedKeyUsage, ma è definita da Microsoft.                                                                                           |
| Campo EnhancedKeyUsage       | Identifica uno o più utilizzi della chiave pubblica contenuta nel certificato. L'estensione utilizzo chiavi avanzato può essere usata in aggiunta a o al posto dell'estensione utilizzo chiave.                                                  |
| KeyUsage               | Identifica le restrizioni sulle operazioni che possono essere eseguite dalla chiave pubblica contenuta nel certificato.                                                                                                                  |
| SmimeCapabilities      | Segnala le funzionalità di decrittografia di un destinatario di posta elettronica al mittente del messaggio di posta elettronica per consentire al mittente di scegliere l'algoritmo simmetrico più sicuro supportato da entrambe le parti.                                                      |
| SubjectKeyIdentifier   | Contiene un identificatore di chiave univoco che può essere usato per distinguere tra più chiavi di firma associate al proprietario del certificato.                                                                                          |
| Modello               | Identifica il modello da utilizzare per l'emissione o il rinnovo di un certificato. L'estensione contiene l'identificatore di oggetto (OID) del modello.                                                                                       |
| TemplateName           | Identifica il modello da utilizzare per l'emissione o il rinnovo di un certificato. L'estensione contiene il nome del modello.                                                                                                          |



 

**Si applica a:** \#Richiesta PKCS 10.

**OID:** \_OID XCN \_ RSA \_ certExtensions (1.2.840.113549.1.9.14)

## <a name="archivekey"></a>ArchiveKey

L'interfaccia [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) può essere usata per definire un attributo che contiene una chiave privata crittografata inviata a una CA per l'archiviazione.

**Si applica a:** Richiesta CMC.

**OID:** \_ \_ Chiave archiviata OID \_ XCN \_ attr (1.3.6.1.4.1.311.21.13)

## <a name="archivekeyhash"></a>ArchiveKeyHash

L'interfaccia [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) può essere usata per definire un hash della chiave privata contenuta nell'attributo **ArchiveKey** .

**Si applica a:** Richiesta CMC.

**OID:** \_Hash della \_ chiave crittografata OID XCN \_ \_ (1.3.6.1.4.1.311.21.21)

## <a name="cspprovider"></a>CspProvider

L'interfaccia [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider) può essere utilizzata per definire un attributo che contiene informazioni sul [*provider del servizio di crittografia*](/windows/desktop/SecGloss/c-gly) (CSP) utilizzato dal richiedente per le operazioni di crittografia.

**Si applica a:** \#Richiesta PKCS 10. Questo attributo viene creato automaticamente quando si crea un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .

**OID:** \_ \_ Provider CSP di registrazione XCN \_ \_ (1.3.6.1.4.1.311.13.2.2)

## <a name="osversion"></a>OSVersion

L'interfaccia [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) può essere usata per creare un attributo che contiene le informazioni sulla versione del sistema operativo client. Le informazioni possono essere utilizzate dalla CA per determinare il tipo di elaborazione da applicare durante la creazione del certificato.

**Si applica a:** \#Richiesta PKCS 10 o CMC.

**OID:** \_Versione del \_ sistema operativo OID XCN \_ (1.3.6.1.4.1.311.13.2.3)

## <a name="renewalcertificate"></a>RenewalCertificate

L'interfaccia [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) può essere utilizzata per creare un attributo che contiene il certificato da rinnovare.

**Si applica a:** \#Richiesta PKCS 10. Questo attributo viene creato automaticamente se si crea una \# richiesta PKCS 10 avviando il certificato da rinnovare.

**OID:** \_Certificato di \_ rinnovo OID XCN \_ (1.3.6.1.4.1.311.13.1)

 

 
