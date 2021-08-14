---
description: L'API di registrazione certificati supporta gli attributi seguenti. È possibile creare un singolo attributo usando l'interfaccia corrispondente identificata in ognuna delle sezioni seguenti.
ms.assetid: e14fd472-1974-4ad2-b35a-3ab58ba0d707
title: Attributi supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8c7945113e764d835a685251adaec9149527b2d8f2d535a5dd24f26a5623bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774414"
---
# <a name="supported-attributes"></a>Attributi supportati

L'API di registrazione certificati supporta gli attributi seguenti. È possibile creare un singolo attributo usando l'interfaccia corrispondente identificata in ognuna delle sezioni seguenti.

## <a name="clientid"></a>ClientId

[**L'interfaccia IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) può essere usata per definire un attributo che contiene informazioni sul computer client che ha inviato la richiesta di certificato. Le informazioni possono essere usate per la diagnostica.

**Si applica a:** Richiesta PKCS \# 10 o CMC.

**OID:** XCN \_ OID \_ REQUEST CLIENT INFO \_ \_ (1.3.6.1.4.1.311.21.20)

## <a name="extensions"></a>Estensioni

[**L'interfaccia IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) può essere usata per definire un set di estensioni di certificato X.509 versione 3. Sono supportate le estensioni seguenti. Per altre informazioni, vedere l'argomento Interfacce di estensione.



| Estensione              | Descrizione                                                                                                                                                                                                                      |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlternativeNames       | Contiene uno o più formati di nome alternativo dell'autorità emittente associata al certificato.                                                                                                                                       |
| AuthorityKeyIdentifier | Contiene un identificatore di chiave univoco per distinguere tra più chiavi di firma del certificato [*dell'autorità di certificazione*](/windows/desktop/SecGloss/c-gly) (CA). |
| Proprietà BasicConstraints       | Indica se l'oggetto può fungere da CA.                                                                                                                                                                                   |
| CertificatePolicies    | Identifica i criteri e le informazioni facoltative sul qualificatore associate al certificato.                                                                                                                                      |
| MSApplicationPolicies  | Identifica uno o più utilizzi del certificato. Questa estensione è simile all'estensione EnhancedKeyUsage, ma è definita da Microsoft.                                                                                           |
| EnhancedKeyUsage       | Identifica uno o più utilizzi della chiave pubblica contenuta nel certificato. L'estensione per l'utilizzo chiavi avanzato può essere usata in aggiunta o al posto dell'estensione per l'utilizzo delle chiavi.                                                  |
| KeyUsage               | Identifica le restrizioni relative alle operazioni che possono essere eseguite dalla chiave pubblica contenuta nel certificato.                                                                                                                  |
| SmimeCapabilities      | Segnala le funzionalità di decrittografia di un destinatario di posta elettronica al mittente di posta elettronica per consentire al mittente di scegliere l'algoritmo simmetrico più sicuro supportato da entrambe le parti.                                                      |
| SubjectKeyIdentifier   | Contiene un identificatore di chiave univoca che può essere utilizzato per distinguere tra più chiavi di firma associate al proprietario del certificato.                                                                                          |
| Modello               | Identifica il modello da utilizzare per il rilascio o il rinnovo di un certificato. L'estensione contiene l'identificatore di oggetto (OID) del modello.                                                                                       |
| Templatename           | Identifica il modello da utilizzare per il rilascio o il rinnovo di un certificato. L'estensione contiene il nome del modello.                                                                                                          |



 

**Si applica a:** Richiesta PKCS \# 10.

**OID:** XCN \_ OID \_ RSA \_ certExtensions (1.2.840.113549.1.9.14)

## <a name="archivekey"></a>Chiave di archiviazione

[**L'interfaccia IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) può essere usata per definire un attributo che contiene una chiave privata crittografata inviata a un'autorità di certificazione per l'archiviazione.

**Si applica a:** Richiesta CMC.

**OID:** XCN \_ OID \_ ARCHIVED \_ KEY \_ ATTR (1.3.6.1.4.1.311.21.13)

## <a name="archivekeyhash"></a>ArchiveKeyHash

[**L'interfaccia IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) può essere usata per definire un hash della chiave privata contenuta nell'attributo **ArchiveKey.**

**Si applica a:** Richiesta CMC.

**OID:** \_XCN OID \_ ENCRYPTED KEY HASH \_ \_ (1.3.6.1.4.1.311.21.21)

## <a name="cspprovider"></a>Provider di servizi di configurazione

[**L'interfaccia IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider) può essere usata per definire un attributo che contiene informazioni sul [*provider*](/windows/desktop/SecGloss/c-gly) del servizio di crittografia (CSP) usato dal richiedente per le operazioni di crittografia.

**Si applica a:** Richiesta PKCS \# 10. Questo attributo viene creato automaticamente quando si crea un [**oggetto IX509CertificateRequestPkcs10.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)

**OID:** PROVIDER CSP DI REGISTRAZIONE OID XCN \_ \_ \_ \_ (1.3.6.1.4.1.311.13.2.2)

## <a name="osversion"></a>OSVersion

[**L'interfaccia IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) può essere usata per creare un attributo che contiene informazioni sulla versione relative al sistema operativo client. Le informazioni possono essere utilizzate dalla CA per determinare il tipo di elaborazione da applicare durante la creazione del certificato.

**Si applica a:** Richiesta PKCS \# 10 o CMC.

**OID:** XCN \_ OID \_ OS \_ VERSION (1.3.6.1.4.1.311.13.2.3)

## <a name="renewalcertificate"></a>RenewalCertificate

[**L'interfaccia IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) può essere usata per creare un attributo che contiene il certificato da rinnovare.

**Si applica a:** Richiesta PKCS \# 10. Questo attributo viene creato automaticamente se si crea una richiesta PKCS 10 avviando la richiesta con \# il certificato da rinnovare.

**OID:** CERTIFICATO DI RINNOVO OID XCN \_ \_ \_ (1.3.6.1.4.1.311.13.1)

 

 
