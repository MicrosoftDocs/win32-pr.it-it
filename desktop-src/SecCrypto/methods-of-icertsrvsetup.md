---
description: I metodi seguenti sono definiti dall'interfaccia ICertSrvSetup. I metodi di accesso alle proprietà non sono visualizzati qui. Per visualizzare le proprietà di ICertSrvSetup, vedere Proprietà di ICertSrvSetup.
ms.assetid: cb7f288b-30a0-4c3b-b7bc-3055166d2302
title: Metodi di ICertSrvSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a4e3482de2c8c62db854b86d21e739993bc3bc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879482"
---
# <a name="methods-of-icertsrvsetup"></a>Metodi di ICertSrvSetup

I metodi seguenti sono definiti dall'interfaccia [**ICertSrvSetup**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetup) . I metodi di accesso alle proprietà non sono visualizzati qui. Per visualizzare le proprietà di **ICertSrvSetup**, vedere [proprietà di ICertSrvSetup](properties-of-icertsrvsetup.md).



| Metodo                                                                         | Descrizione                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAImportPFX**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-caimportpfx)                               | Importa un certificato dell'autorità di certificazione (CA) e la relativa chiave privata associata nell'archivio "LocalMachine".                                                                                                                                          |
| [**GetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getcasetupproperty)                 | Ottiene un valore della proprietà per una configurazione della CA.                                                                                                                                                                                                             |
| [**GetExistingCACertificates**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getexistingcacertificates)   | Ottiene la raccolta di oggetti **CCertSrvSetupKeyInformation** che rappresentano i certificati CA validi attualmente installati nel computer.                                                                                                                  |
| [**Gethashalgorithm**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-gethashalgorithmlist)             | Ottiene l'elenco di algoritmi hash supportati dal [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) specificato per un algoritmo di firma della chiave asimmetrica. |
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getkeylengthlist)                     | Ottiene l'elenco delle lunghezze di chiave supportate dal CSP specificato.                                                                                                                                                                                              |
| [**GetPrivateKeyContainerList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprivatekeycontainerlist) | Ottiene l'elenco di nomi di contenitori di chiavi archiviati dal CSP specificato per gli algoritmi della chiave di firma asimmetrica.                                                                                                                                                 |
| [**GetProviderName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprovidernamelist)               | Ottiene l'elenco dei CSP che forniscono algoritmi di firma della chiave asimmetrica nel computer.                                                                                                                                                                   |
| [**GetSupportedCATypes**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getsupportedcatypes)               | Ottiene i tipi di CA che possono essere installati in un computer nel contesto del chiamante.                                                                                                                                                                       |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-initializedefaults)                 | Inizializza un oggetto **CCertSrvSetup** con i valori predefiniti per consentire l'installazione di un ruolo CA.                                                                                                                                                           |
| [**Installazione**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-install)                                       | Installa un ruolo CA come configurato nell'oggetto **CCertSrvSetup** .                                                                                                                                                                                         |
| [**IsPropertyEditable**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-ispropertyeditable)                 | Indica al chiamante se una proprietà specificata può essere modificata.                                                                                                                                                                                       |
| [**Comandi**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-postuninstall)                           | Non è implementato ed è riservato per un utilizzo futuro.                                                                                                                                                                                                        |
| [**Disinstallazione**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-preuninstall)                             | Salva temporaneamente informazioni sullo stato specifiche del ruolo.                                                                                                                                                                                                        |
| [**SetCADistinguishedName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcadistinguishedname)         | Imposta un nome comune della CA e un suffisso del nome distinto facoltativo.                                                                                                                                                                                          |
| [**SetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcasetupproperty)                 | Imposta un valore della proprietà per una configurazione della CA.                                                                                                                                                                                                             |
| [**SetDatabaseInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setdatabaseinformation)         | Imposta le informazioni correlate al database per il ruolo CA.                                                                                                                                                                                                    |
| [**SetParentCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setparentcainformation)         | Imposta le informazioni sulla CA padre per una configurazione della CA subordinata.                                                                                                                                                                                        |
| [**SetWebCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setwebcainformation)               | Imposta le informazioni sulla CA per il ruolo registrazione Web autorità di certificazione.                                                                                                                                                                                                   |



 

 

 
