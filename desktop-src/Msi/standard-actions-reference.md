---
description: Il Windows Installer presenta le seguenti azioni standard.
ms.assetid: 219b5eb6-501f-4e30-b398-4ed5e0cdf2ab
title: Guida di riferimento alle azioni standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5104c39639ff2bc7b504996467cf707eb52bb014
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227057"
---
# <a name="standard-actions-reference"></a>Guida di riferimento alle azioni standard

Il Windows Installer presenta le seguenti azioni standard.



| Nome azione                                                     | Breve descrizione dell'azione                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AMMINISTRAZIONE](admin-action.md)                                       | Azione di primo livello utilizzata per un'installazione amministrativa.                                                                                                                   |
| [PUBBLICIZZARE](advertise-action.md)                               | Azione di primo livello chiamata per installare o rimuovere i componenti annunciati.                                                                                                         |
| [AllocateRegistrySpace](allocateregistryspace-action.md)       | Verifica che lo spazio libero specificato da [**AVAILABLEFREEREG**](availablefreereg.md) esista nel registro di sistema.                                                               |
| [AppSearch](appsearch-action.md)                               | Cerca le versioni precedenti dei prodotti e determina l'installazione degli aggiornamenti.                                                                                        |
| [Azione BindImage sul](bindimage-action.md)                               | Associa i file eseguibili alle DLL importate.                                                                                                                                           |
| [CCPSearch](ccpsearch-action.md)                               | Usa le firme dei file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.                                              |
| [CostFinalize secondo](costfinalize-action.md)                         | Termina il processo di determinazione dei costi di installazione interna avviato dall' [azione CostInitialize](costinitialize-action.md).                                                               |
| [CostInitialize](costinitialize-action.md)                     | Avvia il processo di determinazione dei costi di installazione.                                                                                                                                      |
| [CreateFolders](createfolders-action.md)                       | Crea cartelle vuote per i componenti.                                                                                                                                         |
| [CreateShortcuts](createshortcuts-action.md)                   | Crea i collegamenti.                                                                                                                                                            |
| [DeleteServices](deleteservices-action.md)                     | Rimuove i servizi di sistema.                                                                                                                                                      |
| [DisableRollback](disablerollback-action.md)                   | Disabilita il rollback per il resto dell'installazione.                                                                                                                      |
| [DuplicateFiles](duplicatefiles-action.md)                     | Duplica i file installati dall'azione InstallFiles.                                                                                                                        |
| [ExecuteAction](executeaction-action.md)                       | Controlla la proprietà [**EXECUTEACTION**](executeaction.md) per determinare quale azione di primo livello inizia la sequenza di esecuzione, quindi esegue tale azione.                          |
| [Filecost](filecost-action.md)                                 | Inizializza il calcolo dei costi del disco con il programma di installazione. Il costo del disco non è finalizzato fino a quando non viene eseguita l'azione CostFinalize secondo.                                                |
| [FindRelatedProducts](findrelatedproducts-action.md)           | Rileva la corrispondenza tra la [tabella di aggiornamento](upgrade-table.md) e i prodotti installati.                                                                                 |
| [ForceReboot](forcereboot-action.md)                           | Utilizzato nella sequenza di azione per richiedere all'utente il riavvio del sistema durante l'installazione.                                                                           |
| [INSTALLARE](install-action.md)                                   | Azione di primo livello chiamata per installare o rimuovere i componenti.                                                                                                                    |
| [InstallAdminPackage](installadminpackage-action.md)           | Copia il database del programma di installazione nel punto di installazione amministrativa.                                                                                                       |
| [InstallExecute](installexecute-action.md)                     | Esegue uno script contenente tutte le operazioni nella sequenza di azione a partire dall'inizio dell'installazione o dall'ultima azione InstallFinalize. Non termina la transazione.   |
| [InstallFiles](installfiles-action.md)                         | Copia i file dall'origine alla directory di destinazione.                                                                                                                    |
| [InstallFinalize](installfinalize-action.md)                   | Esegue uno script contenente tutte le operazioni nella sequenza di azione a partire dall'inizio dell'installazione o dall'ultima azione InstallFinalize. Contrassegna il termine della transazione. |
| [InstallInitialize](installinitialize-action.md)               | Contrassegna l'inizio di una transazione.                                                                                                                                         |
| [InstallSFPCatalogFile](installsfpcatalogfile-action.md)       | L'azione InstallSFPCatalogFile installa i cataloghi usati da Windows me per la protezione dei file di Windows.                                                                        |
| [InstallValidate](installvalidate-action.md)                   | Verifica che tutti i volumi con costi con attributi dispongano di spazio sufficiente per l'installazione.                                                                                   |
| [IsolateComponents](isolatecomponents-action.md)               | Elabora la [tabella IsolatedComponent](isolatedcomponent-table.md)                                                                                                          |
| [LaunchConditions](launchconditions-action.md)                 | Valuta un set di istruzioni condizionali contenute nella tabella LaunchCondition che devono essere tutte restituite true prima che l'installazione possa continuare.                          |
| [MigrateFeatureStates](migratefeaturestates-action.md)         | Esegue la migrazione degli Stati della funzionalità corrente all'installazione in sospeso.                                                                                                                  |
| [MoveFiles](movefiles-action.md)                               | Individua i file esistenti e li sposta o li copia in una nuova posizione.                                                                                                     |
| [MsiConfigureServices](msiconfigureservices-action.md)         | Configura un servizio per il sistema. **[Windows Installer 4,5 e versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.<br/>                           |
| [Azione MsiPublishAssemblies](msipublishassemblies-action.md)  | Gestisce l'annuncio degli assembly Common Language Runtime e degli assembly Win32 in fase di installazione.                                                                |
| [MsiUnpublishAssemblies](msiunpublishassemblies-action.md)     | Gestisce l'annuncio di Common Language Runtime assembly e gli assembly Win32 da rimuovere.                                                                  |
| [InstallODBC](installodbc-action.md)                           | Consente di installare driver, traduttori e origini dati ODBC.                                                                                                                     |
| [InstallServices](installservices-action.md)                   | Registra un servizio con il sistema.                                                                                                                                          |
| [PatchFiles](patchfiles-action.md)                             | Esegue una query sulla tabella patch per determinare quali patch vengono applicate a file specifici e quindi esegue l'applicazione di patch per byte dei file.                                       |
| [ProcessComponents](processcomponents-action.md)               | Registra i componenti, i percorsi chiave e i client dei componenti.                                                                                                                 |
| [PublishComponents](publishcomponents-action.md)               | Annuncia i componenti specificati nella tabella PublishComponent.                                                                                                            |
| [PublishFeatures](publishfeatures-action.md)                   | Scrive lo stato della funzionalità di ogni funzionalità nel registro di sistema                                                                                                             |
| [PublishProduct](publishproduct-action.md)                     | Pubblica le informazioni sul prodotto con il sistema.                                                                                                                                |
| [RegisterClassInfo](registerclassinfo-action.md)               | Gestisce la registrazione delle informazioni della classe COM con il sistema.                                                                                                            |
| [RegisterComPlus](registercomplus-action.md)                   | L'azione RegisterComPlus registra le applicazioni COM+.                                                                                                                       |
| [RegisterExtensionInfo](registerextensioninfo-action.md)       | Registra le informazioni correlate all'estensione con il sistema.                                                                                                                      |
| [RegisterFonts](registerfonts-action.md)                       | Registra i tipi di carattere installati con il sistema.                                                                                                                                    |
| [RegisterMIMEInfo](registermimeinfo-action.md)                 | Registra le informazioni MIME con il sistema.                                                                                                                                   |
| [RegisterProduct](registerproduct-action.md)                   | Registra le informazioni sul prodotto con il programma di installazione e archivia il database del programma di installazione nel computer locale.                                                                     |
| [RegisterProgIdInfo](registerprogidinfo-action.md)             | Registra le informazioni sul ProgId OLE con il sistema.                                                                                                                             |
| [RegisterTypeLibraries](registertypelibraries-action.md)       | Registra le librerie dei tipi con il sistema.                                                                                                                                     |
| [RegisterUser](registeruser-action.md)                         | Registra le informazioni utente per identificare l'utente di un prodotto.                                                                                                                 |
| [RemoveDuplicateFiles](removeduplicatefiles-action.md)         | Elimina i file installati dall'azione DuplicateFiles.                                                                                                                         |
| [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) | Modifica i valori delle variabili di ambiente.                                                                                                                                 |
| [RemoveExistingProducts](removeexistingproducts-action.md)     | Rimuove le versioni installate di un prodotto.                                                                                                                                      |
| [RemoveFiles](removefiles-action.md)                           | Rimuove i file installati in precedenza dall'azione InstallFiles.                                                                                                                |
| [RemoveFolders](removefolders-action.md)                       | Rimuove le cartelle vuote collegate ai componenti impostati per la rimozione.                                                                                                                 |
| [RemoveIniValues](removeinivalues-action.md)                   | Elimina le informazioni sul file ini associate a un componente specificato nella tabella IniFile.                                                                                     |
| [RemoveODBC](removeodbc-action.md)                             | Rimuove origini dati, convertitori e driver ODBC.                                                                                                                          |
| [RemoveRegistryValues](removeregistryvalues-action.md)         | Rimuove le chiavi del registro di sistema di un'applicazione create dalla tabella del registro di sistema.                                                                                            |
| [RemoveShortcuts](removeshortcuts-action.md)                   | Gestisce la rimozione di un collegamento annunciato la cui funzionalità è selezionata per la disinstallazione.                                                                                   |
| [ResolveSource](resolvesource-action.md)                       | Determina il percorso di origine e imposta la proprietà [**SourceDir**](sourcedir.md) .                                                                                          |
| [RMCCPSearch](rmccpsearch-action.md)                           | Usa le firme dei file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.                                              |
| [ScheduleReboot](schedulereboot-action.md)                     | Richiede all'utente un riavvio del sistema alla fine dell'installazione.                                                                                                         |
| [SelfRegModules](selfregmodules-action.md)                     | Elabora i moduli nella tabella SelfReg e li registra se sono installati.                                                                                              |
| [SelfUnregModules](selfunregmodules-action.md)                 | Annulla la registrazione dei moduli nella tabella SelfReg impostati per la disinstallazione.                                                                                                  |
| [SEQUENCE](sequence-action.md)                                 | Esegue le azioni in una tabella specificata dalla proprietà [**Sequence**](sequence.md) .                                                                                           |
| [Azione SetODBCFolders](setodbcfolders-action.md)              | Controlla il sistema per i driver ODBC esistenti e imposta la directory di destinazione per i nuovi driver ODBC.                                                                                   |
| [StartServices](startservices-action.md)                       | Avvia i servizi di sistema.                                                                                                                                                       |
| [StopServices](stopservices-action.md)                         | Arresta i servizi di sistema.                                                                                                                                                        |
| [UnpublishComponents](unpublishcomponents-action.md)           | Gestisce l'unannuncio dei componenti dalla tabella PublishComponent e rimuove le informazioni sui componenti pubblicati.                                                 |
| [UnpublishFeatures](unpublishfeatures-action.md)               | Rimuove le informazioni di mapping dello stato di selezione e del componente della funzionalità dal registro di sistema.                                                                               |
| [UnregisterClassInfo](unregisterclassinfo-action.md)           | Gestisce la rimozione delle classi COM dal registro di sistema.                                                                                                                  |
| [UnregisterComPlus](unregistercomplus-action.md)               | L'azione UnregisterComPlus rimuove le applicazioni COM+ dal registro di sistema.                                                                                                     |
| [UnregisterExtensionInfo](unregisterextensioninfo-action.md)   | Gestisce la rimozione delle informazioni relative all'estensione dal sistema.                                                                                                         |
| [UnregisterFonts](unregisterfonts-action.md)                   | Rimuove le informazioni di registrazione sui tipi di carattere installati dal sistema.                                                                                                       |
| [UnregisterMIMEInfo](unregistermimeinfo-action.md)             | Annulla la registrazione delle informazioni relative a MIME dal registro di sistema.                                                                                                                |
| [UnregisterProgIdInfo](unregisterprogidinfo-action.md)         | Gestisce l'annullamento della registrazione delle informazioni sul ProgId OLE con il sistema.                                                                                                         |
| [UnregisterTypeLibraries](unregistertypelibraries-action.md)   | Annulla la registrazione delle librerie dei tipi con il sistema.                                                                                                                                   |
| [ValidateProductID](validateproductid-action.md)               | Imposta la proprietà [**ProductID**](productid.md) sull'identificatore completo del prodotto.                                                                                                  |
| [WriteEnvironmentStrings](writeenvironmentstrings-action.md)   | Modifica i valori delle variabili di ambiente.                                                                                                                                 |
| [WriteIniValues](writeinivalues-action.md)                     | Scrive le informazioni sul file ini.                                                                                                                                                 |
| [WriteRegistryValori consente](writeregistryvalues-action.md)           | Imposta le informazioni del registro di sistema.                                                                                                                                                 |



 

 

 




