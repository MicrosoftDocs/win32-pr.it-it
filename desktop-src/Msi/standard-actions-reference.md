---
description: Il Windows installer include le azioni standard seguenti.
ms.assetid: 219b5eb6-501f-4e30-b398-4ed5e0cdf2ab
title: Informazioni di riferimento su Azioni standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e88b4b60e3dd13dc4830a1ea4ba2d16a439546d1ced3dc2a8b7552780548d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627631"
---
# <a name="standard-actions-reference"></a>Informazioni di riferimento su Azioni standard

Il Windows installer include le azioni standard seguenti.



| Nome azione                                                     | Breve descrizione dell'azione                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AMMINISTRAZIONE](admin-action.md)                                       | Azione di primo livello usata per un'installazione amministrativa.                                                                                                                   |
| [Pubblicizzare](advertise-action.md)                               | Azione di primo livello chiamata per installare o rimuovere i componenti annunciati.                                                                                                         |
| [AllocateRegistrySpace](allocateregistryspace-action.md)       | Verifica che lo spazio disponibile specificato da [**AVAILABLEFREEREG**](availablefreereg.md) esista nel Registro di sistema.                                                               |
| [Appsearch](appsearch-action.md)                               | Cerca le versioni precedenti dei prodotti e determina che vengono installati gli aggiornamenti.                                                                                        |
| [BindImage](bindimage-action.md)                               | Associa i file eseguibili alle DLL importate.                                                                                                                                           |
| [CCPSearch](ccpsearch-action.md)                               | Usa le firme di file per verificare che i prodotti idonei siano installati in un sistema prima che venga eseguita l'installazione di un aggiornamento.                                              |
| [CostFinalize](costfinalize-action.md)                         | Termina il processo di determinazione costi dell'installazione interna avviato [dall'azione CostInitialize](costinitialize-action.md).                                                               |
| [CostInitialize](costinitialize-action.md)                     | Avvia il processo di costing dell'installazione.                                                                                                                                      |
| [CreateFolders](createfolders-action.md)                       | Crea cartelle vuote per i componenti.                                                                                                                                         |
| [CreateShortcuts](createshortcuts-action.md)                   | Crea collegamenti.                                                                                                                                                            |
| [DeleteServices](deleteservices-action.md)                     | Rimuove i servizi di sistema.                                                                                                                                                      |
| [DisableRollback](disablerollback-action.md)                   | Disabilita il rollback per il resto dell'installazione.                                                                                                                      |
| [DuplicateFiles](duplicatefiles-action.md)                     | Duplica i file installati dall'azione InstallFiles.                                                                                                                        |
| [ExecuteAction](executeaction-action.md)                       | Controlla la [**proprietà EXECUTEACTION**](executeaction.md) per determinare quale azione di primo livello inizia la sequenza di esecuzione e quindi esegue tale azione.                          |
| [FileCost](filecost-action.md)                                 | Inizializza il calcolo del costo del disco con il programma di installazione. La determinazione dei costi del disco non viene finalizzata fino a quando non viene eseguita l'azione CostFinalize.                                                |
| [FindRelatedProducts](findrelatedproducts-action.md)           | Rileva la corrispondenza tra la [tabella Di aggiornamento](upgrade-table.md) e i prodotti installati.                                                                                 |
| [ForceReboot](forcereboot-action.md)                           | Usato nella sequenza di azioni per richiedere all'utente un riavvio del sistema durante l'installazione.                                                                           |
| [Installare](install-action.md)                                   | Azione di primo livello chiamata per installare o rimuovere componenti.                                                                                                                    |
| [InstallAdminPackage](installadminpackage-action.md)           | Copia il database del programma di installazione nel punto di installazione amministrativa.                                                                                                       |
| [InstallExecute](installexecute-action.md)                     | Esegue uno script contenente tutte le operazioni nella sequenza di azioni dall'avvio dell'installazione o dall'ultima azione InstallFinalize. Non termina la transazione.   |
| [InstallFiles](installfiles-action.md)                         | Copia i file dall'origine alla directory di destinazione.                                                                                                                    |
| [InstallFinalize](installfinalize-action.md)                   | Esegue uno script contenente tutte le operazioni nella sequenza di azioni dall'avvio dell'installazione o dall'ultima azione InstallFinalize. Contrassegna il termine della transazione. |
| [InstallInitialize](installinitialize-action.md)               | Contrassegna l'inizio di una transazione.                                                                                                                                         |
| [InstallSFPCatalogFile](installsfpcatalogfile-action.md)       | L'azione InstallSFPCatalogFile installa i cataloghi usati da Windows me per Windows Protezione file.                                                                        |
| [InstallValidate](installvalidate-action.md)                   | Verifica che tutti i volumi con costi con attributi dispongano di spazio sufficiente per l'installazione.                                                                                   |
| [IsolateComponents](isolatecomponents-action.md)               | Elabora la [tabella IsolatedComponent](isolatedcomponent-table.md)                                                                                                          |
| [LaunchConditions](launchconditions-action.md)                 | Valuta un set di istruzioni condizionali contenute nella tabella LaunchCondition che devono restituire true prima che l'installazione possa continuare.                          |
| [MigrateFeatureStates](migratefeaturestates-action.md)         | Esegue la migrazione degli stati delle funzionalità correnti all'installazione in sospeso.                                                                                                                  |
| [MoveFiles](movefiles-action.md)                               | Individua i file esistenti e sposta o copia i file in un nuovo percorso.                                                                                                     |
| [MsiConfigureServices](msiconfigureservices-action.md)         | Configura un servizio per il sistema. **[Windows Installer 4.5 e versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato.<br/>                           |
| [Azione MsiPublishAssemblies](msipublishassemblies-action.md)  | Gestisce l'annuncio degli assembly Common Language Runtime e degli assembly Win32 installati.                                                                |
| [MsiUnpublishAssemblies](msiunpublishassemblies-action.md)     | Gestisce l'annuncio degli assembly Common Language Runtime e degli assembly Win32 che vengono rimossi.                                                                  |
| [InstallODBC](installodbc-action.md)                           | Installa i driver ODBC, i traduttori e le origini dati.                                                                                                                     |
| [InstallServices](installservices-action.md)                   | Registra un servizio con il sistema.                                                                                                                                          |
| [PatchFiles](patchfiles-action.md)                             | Esegue una query nella tabella Patch per determinare quali patch vengono applicate a file specifici e quindi esegue l'applicazione di patch per byte dei file.                                       |
| [ProcessComponents](processcomponents-action.md)               | Registra i componenti, i relativi percorsi chiave e i client dei componenti.                                                                                                                 |
| [PublishComponents](publishcomponents-action.md)               | Annuncia i componenti specificati nella tabella PublishComponent.                                                                                                            |
| [PublishFeatures](publishfeatures-action.md)                   | Scrive lo stato delle funzionalità di ogni funzionalità nel Registro di sistema                                                                                                             |
| [PublishProduct](publishproduct-action.md)                     | Pubblica le informazioni sul prodotto con il sistema.                                                                                                                                |
| [RegisterClassInfo](registerclassinfo-action.md)               | Gestisce la registrazione delle informazioni sulla classe COM con il sistema.                                                                                                            |
| [RegisterComPlus](registercomplus-action.md)                   | L'azione RegisterComPlus registra le applicazioni COM+.                                                                                                                       |
| [RegisterExtensionInfo](registerextensioninfo-action.md)       | Registra le informazioni correlate all'estensione con il sistema.                                                                                                                      |
| [RegisterFonts](registerfonts-action.md)                       | Registra i tipi di carattere installati con il sistema.                                                                                                                                    |
| [RegisterMIMEInfo](registermimeinfo-action.md)                 | Registra le informazioni MIME con il sistema.                                                                                                                                   |
| [RegisterProduct](registerproduct-action.md)                   | Registra le informazioni sul prodotto con il programma di installazione e archivia il database del programma di installazione nel computer locale.                                                                     |
| [RegisterProgIdInfo](registerprogidinfo-action.md)             | Registra le informazioni progId OLE con il sistema.                                                                                                                             |
| [RegisterTypeLibraries](registertypelibraries-action.md)       | Registra le librerie dei tipi con il sistema.                                                                                                                                     |
| [RegisterUser](registeruser-action.md)                         | Registra le informazioni utente per identificare l'utente di un prodotto.                                                                                                                 |
| [RemoveDuplicateFiles](removeduplicatefiles-action.md)         | Elimina i file installati dall'azione DuplicateFiles.                                                                                                                         |
| [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) | Modifica i valori delle variabili di ambiente.                                                                                                                                 |
| [RemoveExistingProducts](removeexistingproducts-action.md)     | Rimuove le versioni installate di un prodotto.                                                                                                                                      |
| [RemoveFiles](removefiles-action.md)                           | Rimuove i file installati in precedenza dall'azione InstallFiles.                                                                                                                |
| [RemoveFolders](removefolders-action.md)                       | Rimuove le cartelle vuote collegate ai componenti impostati per la rimozione.                                                                                                                 |
| [RemoveIniValues](removeinivalues-action.md)                   | Elimina .ini file associate a un componente specificato nella tabella IniFile.                                                                                     |
| [RemoveODBC](removeodbc-action.md)                             | Rimuove origini dati, convertitori e driver ODBC.                                                                                                                          |
| [RemoveRegistryValues](removeregistryvalues-action.md)         | Rimuove le chiavi del Registro di sistema di un'applicazione create dalla tabella Del Registro di sistema.                                                                                            |
| [RemoveShortcuts](removeshortcuts-action.md)                   | Gestisce la rimozione di un collegamento annunciato la cui funzionalità è selezionata per la disinstallazione.                                                                                   |
| [ResolveSource](resolvesource-action.md)                       | Determina il percorso di origine e imposta la [**proprietà SourceDir.**](sourcedir.md)                                                                                          |
| [RMCCPSearch](rmccpsearch-action.md)                           | Usa le firme di file per verificare che i prodotti idonei siano installati in un sistema prima che venga eseguita un'installazione dell'aggiornamento.                                              |
| [ScheduleReboot](schedulereboot-action.md)                     | Richiede all'utente un riavvio del sistema al termine dell'installazione.                                                                                                         |
| [SelfRegModules](selfregmodules-action.md)                     | Elabora i moduli nella tabella SelfReg e li registra se sono installati.                                                                                              |
| [SelfUnregModules](selfunregmodules-action.md)                 | Annulla la registrazione dei moduli nella tabella SelfReg impostati per la disinstallazione.                                                                                                  |
| [SEQUENCE](sequence-action.md)                                 | Esegue le azioni in una tabella specificata dalla [**proprietà SEQUENCE.**](sequence.md)                                                                                           |
| [Azione SetODBCFolders](setodbcfolders-action.md)              | Verifica la presenza di driver ODBC esistenti nel sistema e imposta la directory di destinazione per i nuovi driver ODBC.                                                                                   |
| [StartServices](startservices-action.md)                       | Avvia i servizi di sistema.                                                                                                                                                       |
| [StopServices](stopservices-action.md)                         | Arresta i servizi di sistema.                                                                                                                                                        |
| [UnpublishComponents](unpublishcomponents-action.md)           | Gestisce l'annullamento della inversione dei componenti dalla tabella PublishComponent e rimuove le informazioni sui componenti pubblicati.                                                 |
| [UnpublishFeatures](unpublishfeatures-action.md)               | Rimuove le informazioni di mapping dello stato di selezione e del componente funzionalità dal Registro di sistema.                                                                               |
| [UnregisterClassInfo](unregisterclassinfo-action.md)           | Gestisce la rimozione di classi COM dal Registro di sistema.                                                                                                                  |
| [Annullare la registrazione diComPlus](unregistercomplus-action.md)               | L'azione UnregisterComPlus rimuove le applicazioni COM+ dal Registro di sistema.                                                                                                     |
| [UnregisterExtensionInfo](unregisterextensioninfo-action.md)   | Gestisce la rimozione delle informazioni correlate all'estensione dal sistema.                                                                                                         |
| [UnregisterFonts](unregisterfonts-action.md)                   | Rimuove dal sistema le informazioni di registrazione sui tipi di carattere installati.                                                                                                       |
| [Annullare la registrazione diMIMEInfo](unregistermimeinfo-action.md)             | Annulla la registrazione delle informazioni relative a MIME dal Registro di sistema.                                                                                                                |
| [UnregisterProgIdInfo](unregisterprogidinfo-action.md)         | Gestisce l'annullamento della registrazione delle informazioni ProgId OLE con il sistema.                                                                                                         |
| [UnregisterTypeLibraries](unregistertypelibraries-action.md)   | Annulla la registrazione delle librerie dei tipi con il sistema.                                                                                                                                   |
| [ValidateProductID](validateproductid-action.md)               | Imposta [**la proprietà ProductID**](productid.md) sull'identificatore di prodotto completo.                                                                                                  |
| [WriteEnvironmentStrings](writeenvironmentstrings-action.md)   | Modifica i valori delle variabili di ambiente.                                                                                                                                 |
| [WriteIniValues](writeinivalues-action.md)                     | Scrive .ini informazioni sul file.                                                                                                                                                 |
| [WriteRegistryValues](writeregistryvalues-action.md)           | Configura le informazioni del Registro di sistema.                                                                                                                                                 |



 

 

 




