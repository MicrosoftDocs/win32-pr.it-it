---
description: Elenca le interfacce fornite da CryptoAPI.
ms.assetid: f94f0264-78b8-4a28-9d3a-dda55db29897
title: Interfacce di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5937dce6da8ffa3396c885d00c895b845de9889c2688c6daef4eba5db0beb90b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876101"
---
# <a name="cryptography-interfaces"></a>Interfacce di crittografia

Le interfacce di crittografia vengono categorizzate in base all'utilizzo, come indicato di seguito:

-   [Interfacce di esportazione del motore del server](#server-engine-export-interfaces)
-   [Interfacce di importazione del motore del server](#server-engine-import-interfaces)
-   [Interfacce di codifica](#encoding-interfaces)
-   [Interfacce di registrazione certificati](#certificate-enrollment-interfaces)
-   [Interfacce di interoperabilità CAPICOM](#capicom-interoperability-interfaces)

## <a name="server-engine-export-interfaces"></a>Interfacce di esportazione del motore del server

Nell'argomento di riferimento seguente vengono descritte le interfacce esportate dal motore del server e chiamate da oggetti esterni.



| Interfaccia                                                                | Descrizione                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin)                                         | Usato dai programmi di amministrazione per gestire richieste, certificati e revoche.                                                                                                                                                              |
| [**ICertAdmin2**](/windows/desktop/api/Certadm/nn-certadm-icertadmin2)                                       | Usato dai programmi di amministrazione per gestire richieste, certificati e revoche. Sostituisce [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin).                                                                                                                 |
| [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)                                       | Usato dai client per ottenere informazioni sui server disponibili.                                                                                                                                                                                 |
| [**ICertConfig2**](/windows/desktop/api/Certcli/nn-certcli-icertconfig2)                                     | Usato dai client per ottenere informazioni sui server disponibili. Sostituisce [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig).                                                                                                                                  |
| [**ICertGetConfig**](/windows/desktop/api/Certcli/nn-certcli-icertgetconfig)                                 | Fornisce funzionalità per il recupero dei dati di configurazione pubblici (specificati durante l'installazione del client) per un server [*di Servizi*](../secgloss/c-gly.md) certificati.                |
| [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest)                                     | Usato per inviare una richiesta al server e ottenere i risultati della richiesta.                                                                                                                                                                        |
| [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2)                                   | Usato per inviare una richiesta al server e ottenere i risultati della richiesta. Sostituisce [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest).                                                                                                                       |
| [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit)                               | Usato dai [moduli di uscita](exit-modules.md) per ottenere le proprietà del certificato e della richiesta.                                                                                                                                                             |
| [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy)                           | Usato dal modulo [dei criteri per](policy-modules.md) ottenere e impostare le proprietà del certificato e della richiesta.                                                                                                                                              |
| [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview)                                           | Utilizzato dai client per [la visualizzazione del database di Servizi certificati](viewing-the-certificate-services-database.md).                                                                                                                                 |
| [**ICertView2**](/windows/desktop/api/Certview/nn-certview-icertview2)                                         | Utilizzato dai client per la visualizzazione del database di Servizi certificati. Sostituisce [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview).                                                                                                                                       |
| [**IEnumCERTVIEWATTRIBUTE**](/windows/desktop/api/Certview/nn-certview-ienumcertviewattribute)                 | Usato dai client per accedere agli attributi del certificato per una riga nella visualizzazione Servizi certificati.                                                                                                                                                |
| [**IEnumCERTVIEWCOLUMN**](/windows/desktop/api/Certview/nn-certview-ienumcertviewcolumn)                       | Utilizzato dai client per accedere alle colonne di dati di una riga nella vista Servizi certificati.                                                                                                                                                           |
| [**IEnumCERTVIEWEXTENSION**](/windows/desktop/api/Certview/nn-certview-ienumcertviewextension)                 | Usato dai client per accedere ai dati dell'estensione del certificato per una riga nella visualizzazione Servizi certificati.                                                                                                                                            |
| [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow)                             | Usato dai client per enumerare le righe della vista Servizi certificati.                                                                                                                                                                         |
| [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin)                                         | Utilizzato dai programmi di amministrazione per configurare i server risponditore OCSP (Online Certificate Status Protocol).                                                                                                                                       |
| [**IOCSPCAConfiguration**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfiguration)                     | Fornisce la funzionalità per configurare un servizio risponditore OCSP per gestire le richieste di stato per un'autorità [*di certificazione (CA)*](../secgloss/c-gly.md) specifica.<br/> |
| [**IOCSPCAConfigurationCollection**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfigurationcollection) | Fornisce funzionalità per gestire le configurazioni della CA per cui un servizio risponditore OCSP può gestire le richieste.                                                                                                                                 |
| [**IOCSPProperty**](/windows/desktop/api/Certadm/nn-certadm-iocspproperty)                                   | Fornisce la funzionalità per configurare un attributo del server risponditore OCSP.                                                                                                                                                                         |
| [**IOCSPPropertyCollection**](/windows/desktop/api/Certadm/nn-certadm-iocsppropertycollection)               | Utilizzato dai programmi di amministrazione per gestire gli attributi del server risponditore OCSP.                                                                                                                                                                     |



 

## <a name="server-engine-import-interfaces"></a>Interfacce di importazione del motore del server

Negli argomenti di riferimento seguenti vengono descritte le interfacce importate dal motore del server.



| Interfaccia                                      | Descrizione                                                                                                                            |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit)                 | Esportato dai moduli di uscita. Usato dal motore del server per recapitare i certificati e le informazioni di revoca completati.                       |
| [**ICertExit2**](/windows/desktop/api/Certexit/nn-certexit-icertexit2)               | Aggiunge il [**metodo GetManageModule**](/windows/desktop/api/Certexit/nf-certexit-icertexit2-getmanagemodule) a [**ICertExit.**](/windows/desktop/api/Certexit/nn-certexit-icertexit)                               |
| [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) | Esportato in base ai criteri o ai moduli di uscita. Consente di visualizzare le informazioni sul modulo o di visualizzare un'interfaccia utente per la configurazione del modulo. |
| [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy)             | Esportato dal modulo dei criteri. Usato dal motore del server per controllare le richieste e ottenere le proprietà per i certificati.                        |
| [**ICertPolicy2**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy2)           | Aggiunge il [**metodo GetManageModule**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy2-getmanagemodule) a [**ICertPolicy.**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy)                         |



 

## <a name="encoding-interfaces"></a>Interfacce di codifica

Negli argomenti di riferimento seguenti vengono descritte [](writing-custom-extension-handlers.md) le interfacce che possono essere esportate dai gestori di estensioni e importate dal modulo dei criteri.



| Interfaccia                                                | Descrizione                                                                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname)         | Usato dal modulo [dei criteri per](policy-modules.md) gestire estensioni di nomi alternativi.                                                                                                                                                          |
| [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring)     | Usato dal modulo dei criteri per gestire le stringhe di bit usate nelle estensioni di certificato.                                                                                                                                                               |
| [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo) | Utilizzato dal modulo dei criteri per gestire [*le matrici di*](../secgloss/c-gly.md) informazioni di distribuzione dell'elenco di revoche di certificati (CRL) usate nelle estensioni di certificato. |
| [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray)     | Utilizzato dal modulo dei criteri per gestire le **matrici Date** usate nelle estensioni del certificato.                                                                                                                                                           |
| [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)     | Usato dal modulo dei criteri per gestire **le matrici Long** usate nelle estensioni del certificato.                                                                                                                                                           |
| [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray) | Utilizzato dal modulo dei criteri per gestire **le matrici STRING** usate nelle estensioni di certificato.                                                                                                                                                         |



 

## <a name="certificate-enrollment-interfaces"></a>Interfacce di registrazione certificati

Questa sezione descrive gli oggetti, i metodi e le proprietà del controllo registrazione certificati e l'oggetto, i metodi e le proprietà disponibili nel controllo di registrazione smart card. Sono incluse le interfacce seguenti.



| Interfaccia                                                                                  | Descrizione                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll)                                                               | Una delle diverse interfacce che rappresentano il controllo registrazione certificati. È importante soprattutto se non si usa Automazione.                                                                        |
| [**ICEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll2)                                                             | Una delle diverse interfacce che rappresentano il controllo registrazione certificati. È importante soprattutto se non si usa Automazione.                                                                        |
| [**ICEnroll3**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll3)                                                             | Una delle diverse interfacce che rappresentano il controllo registrazione certificati. È importante soprattutto se non si usa Automazione.                                                                        |
| [**ICertificateEnrollmentPolicyServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentpolicyserversetup) | Rappresenta il servizio Web CEP (Certificate Enrollment Policy) all'interno di Servizi certificati Active Directory (ADCS). Il servizio consente a utenti e computer di ottenere informazioni sui criteri di registrazione certificati. |
| [**ICertificateEnrollmentServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentserversetup)             | Rappresenta il Servizio Web di registrazione certificati (CES) all'interno di ADCS. Il servizio consente a utenti e computer di registrarsi e rinnovare i certificati.                                                               |
| [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4)                                                             | Una delle diverse interfacce che rappresentano il controllo registrazione certificati. È importante soprattutto se non si usa Automazione.                                                                        |
| [**IEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll)                                                                 | Una delle diverse interfacce che rappresentano il controllo registrazione certificati. L'interfaccia è principalmente di interesse se non si usa Automazione.                                                             |
| [**IEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll2)                                                               | Una delle diverse interfacce che rappresentano il controllo registrazione certificati. L'interfaccia è principalmente di interesse se non si usa Automazione.                                                             |
| [**IEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll4)                                                               | Una delle diverse interfacce che rappresentano il controllo registrazione certificati. L'interfaccia è principalmente di interesse se non si usa Automazione.                                                             |
| [**ISCrdEnr**](iscrdenr.md)                                                               | Rappresenta il controllo smart card registrazione. È importante soprattutto se non si usa Automazione.                                                                                                       |



 

## <a name="capicom-interoperability-interfaces"></a>Interfacce di interoperabilità CAPICOM

Negli argomenti di riferimento seguenti vengono descritte le interfacce che consentono alle derivazioni di CryptoAPI di funzionare insieme a CAPICOM 2.0.



| Interfaccia                              | Descrizione                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertContext**](icertcontext.md)   | Fornisce l'accesso al contesto di un oggetto certificato [](certificate.md) CAPICOM X.509v3. Questo contesto consente l'uso del certificato CAPICOM in altre derivazioni di CryptoAPI. |
| [**ICertStore**](icertstore.md)       | Fornisce l'accesso al contesto di un oggetto ARCHIVIO [**CAPICOM.**](store.md) Questo contesto consente l'uso dell'archivio certificati CAPICOM in altre derivazioni di CryptoAPI.               |
| [**IChainContext**](ichaincontext.md) | Fornisce l'accesso al contesto di un oggetto [**CapiCOM Chain.**](chain.md) Questo contesto consente l'uso della catena di attendibilità dei certificati CAPICOM in altre derivazioni di CryptoAPI.         |



 

 

 
