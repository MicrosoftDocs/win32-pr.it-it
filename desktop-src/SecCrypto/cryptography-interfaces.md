---
description: Elenca le interfacce fornite da CryptoAPI.
ms.assetid: f94f0264-78b8-4a28-9d3a-dda55db29897
title: Interfacce di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccf5284f5c2107e741fd91e2936ff3dea0853e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343131"
---
# <a name="cryptography-interfaces"></a>Interfacce di crittografia

Le interfacce di crittografia sono classificate in base all'utilizzo come indicato di seguito:

-   [Interfacce di esportazione del motore Server](#server-engine-export-interfaces)
-   [Interfacce di importazione del motore Server](#server-engine-import-interfaces)
-   [Interfacce di codifica](#encoding-interfaces)
-   [Interfacce di registrazione certificati](#certificate-enrollment-interfaces)
-   [Interfacce di interoperabilità di capicol](#capicom-interoperability-interfaces)

## <a name="server-engine-export-interfaces"></a>Interfacce di esportazione del motore Server

Nell'argomento di riferimento seguente vengono descritte le interfacce esportate dal motore del server e chiamate da oggetti esterni.



| Interfaccia                                                                | Descrizione                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin)                                         | Utilizzato dai programmi di amministrazione per gestire richieste, certificati e revoche.                                                                                                                                                              |
| [**ICertAdmin2**](/windows/desktop/api/Certadm/nn-certadm-icertadmin2)                                       | Utilizzato dai programmi di amministrazione per gestire richieste, certificati e revoche. Sostituisce [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin).                                                                                                                 |
| [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)                                       | Utilizzato dai client per ottenere informazioni sui server disponibili.                                                                                                                                                                                 |
| [**ICertConfig2**](/windows/desktop/api/Certcli/nn-certcli-icertconfig2)                                     | Utilizzato dai client per ottenere informazioni sui server disponibili. Sostituisce [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig).                                                                                                                                  |
| [**ICertGetConfig**](/windows/desktop/api/Certcli/nn-certcli-icertgetconfig)                                 | Fornisce la funzionalità per il recupero dei dati di configurazione pubblica (specificati durante l'installazione del client) per un server di [*Servizi certificati*](../secgloss/c-gly.md) .                |
| [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest)                                     | Utilizzato per inviare una richiesta al server e ottenere i risultati della richiesta.                                                                                                                                                                        |
| [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2)                                   | Utilizzato per inviare una richiesta al server e ottenere i risultati della richiesta. Sostituisce [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest).                                                                                                                       |
| [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit)                               | Usato dai [moduli di uscita](exit-modules.md) per ottenere le proprietà del certificato e della richiesta.                                                                                                                                                             |
| [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy)                           | Usato dal [modulo criteri](policy-modules.md) per ottenere e impostare le proprietà del certificato e della richiesta.                                                                                                                                              |
| [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview)                                           | Utilizzato dai client per [la visualizzazione del database di Servizi certificati](viewing-the-certificate-services-database.md).                                                                                                                                 |
| [**ICertView2**](/windows/desktop/api/Certview/nn-certview-icertview2)                                         | Utilizzato dai client per la visualizzazione del database di Servizi certificati. Sostituisce [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview).                                                                                                                                       |
| [**IEnumCERTVIEWATTRIBUTE**](/windows/desktop/api/Certview/nn-certview-ienumcertviewattribute)                 | Utilizzato dai client per accedere agli attributi del certificato per una riga nella vista Servizi certificati.                                                                                                                                                |
| [**IEnumCERTVIEWCOLUMN**](/windows/desktop/api/Certview/nn-certview-ienumcertviewcolumn)                       | Utilizzato dai client per accedere alle colonne di dati di una riga nella vista Servizi certificati.                                                                                                                                                           |
| [**IEnumCERTVIEWEXTENSION**](/windows/desktop/api/Certview/nn-certview-ienumcertviewextension)                 | Utilizzato dai client per accedere ai dati dell'estensione del certificato per una riga nella vista Servizi certificati.                                                                                                                                            |
| [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow)                             | Utilizzato dai client per enumerare le righe della visualizzazione dei servizi certificati.                                                                                                                                                                         |
| [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin)                                         | Utilizzato dai programmi di amministrazione per configurare i server risponditore OCSP (Online Certificate Status Protocol).                                                                                                                                       |
| [**IOCSPCAConfiguration**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfiguration)                     | Fornisce funzionalità per configurare un servizio risponditore OCSP per gestire le richieste di stato per un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA) specifica.<br/> |
| [**IOCSPCAConfigurationCollection**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfigurationcollection) | Fornisce la funzionalità per gestire le configurazioni della CA per le quali un servizio risponditore OCSP è in grado di gestire le richieste.                                                                                                                                 |
| [**IOCSPProperty**](/windows/desktop/api/Certadm/nn-certadm-iocspproperty)                                   | Fornisce la funzionalità per configurare un attributo del server risponditore OCSP.                                                                                                                                                                         |
| [**IOCSPPropertyCollection**](/windows/desktop/api/Certadm/nn-certadm-iocsppropertycollection)               | Utilizzato dai programmi di amministrazione per gestire gli attributi del server risponditore OCSP.                                                                                                                                                                     |



 

## <a name="server-engine-import-interfaces"></a>Interfacce di importazione del motore Server

Negli argomenti di riferimento seguenti vengono descritte le interfacce importate dal motore del server.



| Interfaccia                                      | Descrizione                                                                                                                            |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit)                 | Esportati da moduli di uscita. Utilizzato dal motore del server per fornire i certificati completati e le informazioni di revoca.                       |
| [**ICertExit2**](/windows/desktop/api/Certexit/nn-certexit-icertexit2)               | Aggiunge il metodo [**GetManageModule**](/windows/desktop/api/Certexit/nf-certexit-icertexit2-getmanagemodule) a [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit).                               |
| [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) | Esportati da criteri o da moduli di uscita. Usato per visualizzare le informazioni sul modulo o per visualizzare un'interfaccia utente per la configurazione del modulo. |
| [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy)             | Esportato dal modulo criteri. Utilizzato dal motore del server per controllare le richieste e ottenere le proprietà per i certificati.                        |
| [**ICertPolicy2**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy2)           | Aggiunge il metodo [**GetManageModule**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy2-getmanagemodule) a [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy).                         |



 

## <a name="encoding-interfaces"></a>Interfacce di codifica

Gli argomenti di riferimento seguenti descrivono le interfacce che possono essere esportate dai [gestori di estensione](writing-custom-extension-handlers.md) e vengono importate dal modulo criteri.



| Interfaccia                                                | Descrizione                                                                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname)         | Utilizzato dal [modulo criteri](policy-modules.md) per gestire le estensioni dei nomi alternativi.                                                                                                                                                          |
| [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring)     | Utilizzato dal modulo criteri per gestire le stringhe di bit utilizzate nelle estensioni del certificato.                                                                                                                                                               |
| [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo) | Utilizzato dal modulo criteri per gestire le matrici di informazioni di distribuzione dell' [*elenco di revoche di certificati*](../secgloss/c-gly.md) (CRL) utilizzate nelle estensioni del certificato. |
| [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray)     | Utilizzato dal modulo criteri per gestire le matrici di **date** utilizzate nelle estensioni del certificato.                                                                                                                                                           |
| [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)     | Utilizzato dal modulo criteri per gestire matrici **lunghe** utilizzate nelle estensioni del certificato.                                                                                                                                                           |
| [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray) | Utilizzato dal modulo criteri per gestire le matrici di **stringhe** utilizzate nelle estensioni del certificato.                                                                                                                                                         |



 

## <a name="certificate-enrollment-interfaces"></a>Interfacce di registrazione certificati

In questa sezione vengono descritti gli oggetti, i metodi e le proprietà del controllo di registrazione certificati e l'oggetto, i metodi e le proprietà disponibili nel controllo registrazione smart card. Sono incluse le interfacce seguenti.



| Interfaccia                                                                                  | Descrizione                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll)                                                               | Una delle numerose interfacce che rappresentano il controllo di registrazione del certificato. Si tratta principalmente di un aspetto interessante se non si utilizza l'automazione.                                                                        |
| [**ICEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll2)                                                             | Una delle numerose interfacce che rappresentano il controllo di registrazione del certificato. Si tratta principalmente di un aspetto interessante se non si utilizza l'automazione.                                                                        |
| [**ICEnroll3**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll3)                                                             | Una delle numerose interfacce che rappresentano il controllo di registrazione del certificato. Si tratta principalmente di un aspetto interessante se non si utilizza l'automazione.                                                                        |
| [**ICertificateEnrollmentPolicyServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentpolicyserversetup) | Rappresenta il servizio Web del criterio di registrazione certificati (CEP) in Active Directory Servizi certificati (ADC). Il servizio consente a utenti e computer di ottenere informazioni sui criteri di registrazione dei certificati. |
| [**ICertificateEnrollmentServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentserversetup)             | Rappresenta il Servizio Web di registrazione certificati (CES) negli ADC. Il servizio consente a utenti e computer di registrare e rinnovare i certificati.                                                               |
| [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4)                                                             | Una delle numerose interfacce che rappresentano il controllo di registrazione del certificato. Si tratta principalmente di un aspetto interessante se non si utilizza l'automazione.                                                                        |
| [**IEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll)                                                                 | Una delle numerose interfacce che rappresentano il controllo di registrazione del certificato. L'interfaccia è principalmente di interesse se non si usa l'automazione.                                                             |
| [**IEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll2)                                                               | Una delle numerose interfacce che rappresentano il controllo di registrazione del certificato. L'interfaccia è principalmente di interesse se non si usa l'automazione.                                                             |
| [**IEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll4)                                                               | Una delle numerose interfacce che rappresentano il controllo di registrazione del certificato. L'interfaccia è principalmente di interesse se non si usa l'automazione.                                                             |
| [**ISCrdEnr**](iscrdenr.md)                                                               | Rappresenta il controllo di registrazione della smart card. Si tratta principalmente di un aspetto interessante se non si utilizza l'automazione.                                                                                                       |



 

## <a name="capicom-interoperability-interfaces"></a>Interfacce di interoperabilità di capicol

Negli argomenti di riferimento seguenti vengono descritte le interfacce che consentono la derivazione di CryptoAPI per interagire con CAPICOM 2,0.



| Interfaccia                              | Descrizione                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertContext**](icertcontext.md)   | Consente di accedere al contesto di un oggetto [**certificato**](certificate.md) CAPICOM X. 509v3. Questo contesto consente l'uso del certificato di CAPICOM in altre derivazioni di CryptoAPI. |
| [**ICertStore**](icertstore.md)       | Consente di accedere al contesto di un oggetto [**Archivio**](store.md) CAPICOM. Questo contesto consente l'uso dell'archivio certificati CAPICOM in altre derivazioni di CryptoAPI.               |
| [**IChainContext**](ichaincontext.md) | Fornisce l'accesso al contesto di un oggetto [**Chain**](chain.md) di capico. Questo contesto consente l'uso della catena di certificati del certificato CAPICOM in altre derivazioni di CryptoAPI.         |



 

 

 
