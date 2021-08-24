---
description: I metodi seguenti sono definiti dall'interfaccia ICertSrvSetup. I metodi di accesso alle proprietà non vengono visualizzati qui. Per visualizzare le proprietà per ICertSrvSetup, vedere Proprietà di ICertSrvSetup.
ms.assetid: cb7f288b-30a0-4c3b-b7bc-3055166d2302
title: Metodi di ICertSrvSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28274e1f59a4c229587f7e9f73222381ca89cff1a112ef7dc633f7a0c32dd434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407891"
---
# <a name="methods-of-icertsrvsetup"></a>Metodi di ICertSrvSetup

I metodi seguenti sono definiti [**dall'interfaccia ICertSrvSetup.**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetup) I metodi di accesso alle proprietà non vengono visualizzati qui. Per visualizzare le proprietà per **ICertSrvSetup,** vedere [Proprietà di ICertSrvSetup](properties-of-icertsrvsetup.md).



| Metodo                                                                         | Descrizione                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAImportPFX**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-caimportpfx)                               | Importa un certificato dell'autorità di certificazione (CA) e la chiave privata associata nell'archivio "LocalMachine".                                                                                                                                          |
| [**GetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getcasetupproperty)                 | Ottiene un valore della proprietà per una configurazione della CA.                                                                                                                                                                                                             |
| [**GetExistingCACertificates**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getexistingcacertificates)   | Ottiene la raccolta di **oggetti CCertSrvSetupKeyInformation** che rappresentano certificati CA validi attualmente installati nel computer.                                                                                                                  |
| [**GetHashAlgorithmList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-gethashalgorithmlist)             | Ottiene l'elenco di algoritmi hash supportati dal [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP) specificato per un algoritmo di firma a chiave asimmetrica. |
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getkeylengthlist)                     | Ottiene l'elenco di lunghezze di chiave supportate dal provider di servizi di configurazione specificato.                                                                                                                                                                                              |
| [**GetPrivateKeyContainerList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprivatekeycontainerlist) | Ottiene l'elenco dei nomi dei contenitori di chiavi archiviati dal provider di servizi di crittografia specificato per gli algoritmi a chiave di firma asimmetrica.                                                                                                                                                 |
| [**GetProviderNameList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprovidernamelist)               | Ottiene l'elenco di CSP che forniscono algoritmi di firma a chiave asimmetrica nel computer.                                                                                                                                                                   |
| [**GetSupportedCATypes**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getsupportedcatypes)               | Ottiene i tipi di CA che possono essere installate in un computer nel contesto del chiamante.                                                                                                                                                                       |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-initializedefaults)                 | Inizializza un oggetto **CCertSrvSetup con** i valori predefiniti per abilitare l'installazione di un ruolo ca.                                                                                                                                                           |
| [**Installazione**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-install)                                       | Installa un ruolo ca come configurato **nell'oggetto CCertSrvSetup.**                                                                                                                                                                                         |
| [**IsPropertyEditable**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-ispropertyeditable)                 | Indica al chiamante se una proprietà specificata può essere modificata.                                                                                                                                                                                       |
| [**PostUnInstall**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-postuninstall)                           | Non è implementato ed è riservato per un uso futuro.                                                                                                                                                                                                        |
| [**PreInstallazione**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-preuninstall)                             | Salva temporaneamente le informazioni sullo stato specifiche del ruolo.                                                                                                                                                                                                        |
| [**SetCADistinguishedName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcadistinguishedname)         | Imposta un nome comune della CA e un suffisso del nome distinto facoltativo.                                                                                                                                                                                          |
| [**SetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcasetupproperty)                 | Imposta un valore della proprietà per una configurazione della CA.                                                                                                                                                                                                             |
| [**SetDatabaseInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setdatabaseinformation)         | Imposta le informazioni correlate al database per il ruolo CA.                                                                                                                                                                                                    |
| [**SetParentCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setparentcainformation)         | Imposta le informazioni sulla CA padre per una configurazione della CA subordinata.                                                                                                                                                                                        |
| [**SetWebCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setwebcainformation)               | Imposta le informazioni sulla CA per il ruolo Registrazione Web CA.                                                                                                                                                                                                   |



 

 

 
