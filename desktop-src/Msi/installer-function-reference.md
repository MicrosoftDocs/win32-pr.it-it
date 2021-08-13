---
description: Per abilitare Windows programma di installazione nell'applicazione, è necessario usare le funzioni del programma di installazione. Le tabelle in questo argomento identificano le funzioni in base alla categoria.
ms.assetid: 05a16915-6b47-4d51-b62a-5a4d92b87e50
title: Informazioni di riferimento sulla funzione Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ab6a77bd3aa02be85f0d2a3cb11a864861535360f5741c6566f77e9fc1aa11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630546"
---
# <a name="installer-function-reference"></a>Informazioni di riferimento sulla funzione Installer

Per abilitare Windows programma di installazione nell'applicazione, è necessario usare le funzioni del programma di installazione. Le tabelle in questo argomento identificano le funzioni in base alla categoria.

## <a name="user-interface-and-logging-functions"></a>Interfaccia utente e di registrazione



| Nome                                                     | Descrizione                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)             | Abilita l'interfaccia utente interna del programma di installazione.                                 |
| [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)             | Abilita un gestore dell'interfaccia utente esterno che riceve messaggi in formato stringa. |
| [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) | Abilita un gestore dell'interfaccia utente esterno che riceve i messaggi in un formato di record. |
| [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)                     | Imposta la modalità di registrazione per tutte le installazioni nel processo chiamante.                       |



 

## <a name="handle-management-functions"></a>Gestire le funzioni di gestione



| Nome                                             | Descrizione                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)         | Chiude un handle di installazione aperto.                           |
| [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) | Chiude tutti gli handle di installazione aperti. Non usare per la pulizia. |



 

## <a name="installation-and-configuration-functions"></a>Funzioni di installazione e configurazione



| Nome                                                                     | Descrizione                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)                       | Annuncia un prodotto.                                                                                                                                                                                                        |
| [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)                   | Annuncia un prodotto.                                                                                                                                                                                                        |
| [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)                         | Copia un file script di annuncio nei percorsi specificati.                                                                                                                                                                    |
| [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)                           | Installa o rimuove un'applicazione o una suite di applicazioni.                                                                                                                                                                     |
| [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)                       | Installa o rimuove un'applicazione o una suite di applicazioni.                                                                                                                                                                     |
| [**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)                   | Installa o rimuove un'applicazione o una suite di applicazioni. È possibile specificare una riga di comando del prodotto.                                                                                                                            |
| [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)                       | Reinstalla o ripristina un'installazione di .                                                                                                                                                                                       |
| [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)                       | Configura lo stato installato di una funzionalità.                                                                                                                                                                                 |
| [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)                       | Convalida o ripristina le funzionalità.                                                                                                                                                                                               |
| [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)         | Installa i componenti mancanti.                                                                                                                                                                                                 |
| [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)                   | Installa i file mancanti.                                                                                                                                                                                                      |
| [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)                         | Notifica e aggiorna le informazioni interne Windows Installer con modifiche ai SID utente. Disponibile a partire da Windows Installer 3.1.                                                                                   |
| [**MsiProcessAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiprocessadvertisescripta)           | Elabora un file script di annuncio in percorsi specificati.                                                                                                                                                                 |
| [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)                 | Aggiunge o riordina le origini di una patch o di un prodotto in un contesto specificato.                                                                                                                                                   |
| [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)             | Aggiunge o riordina le origini di una patch o di un prodotto in un contesto specificato. Crea un elenco di origine per una patch che non esiste in un contesto specificato. Disponibile in Windows Installer 3.0.                                |
| [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)             | Rimuove un'origine esistente per un prodotto o una patch in un contesto specificato. Disponibile in Windows Installer 3.0.                                                                                                               |
| [**MsiSourceListClearAll**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)                   | Rimuove tutte le origini esistenti di un tipo di origine specifico per un'istanza di prodotto specificata.                                                                                                                                 |
| [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)               | Rimuove tutte le origini esistenti di un tipo di origine specifico per un'istanza di prodotto specificata. Disponibile in Windows Installer 3.0.                                                                                            |
| [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)     | Rimuove la registrazione dell'origine corrente del prodotto o della patch, registrata come proprietà "LastUsedSource". Questa funzione non influisce sull'elenco di origine registrato.                                      |
| [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) | Rimuove la registrazione dell'origine corrente del prodotto o della patch, registrata come proprietà "LastUsedSource". Questa funzione non influisce sull'elenco di origine registrato. Disponibile in Windows Installer 3.0. |
| [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)                     | Recupera informazioni sull'elenco di origine per un prodotto o una patch in un contesto specifico.                                                                                                                                    |
| [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)                     | Imposta l'origine utilizzata più di recente per un prodotto o una patch in un contesto specificato. Disponibile in Windows Installer 3.0.                                                                                                       |
| [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)       | Enumera l'elenco dei dischi registrati per l'origine supporto per una patch o un prodotto. Disponibile in Windows Installer 3.0.                                                                                                    |
| [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)           | Aggiunge o aggiorna un disco dell'origine supporto di un prodotto registrato o di una patch. Disponibile in Windows Installer 3.0.                                                                                                            |
| [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)      | Rimuove un disco registrato esistente nell'origine supporto per un prodotto o una patch in un contesto specifico. Disponibile in Windows Installer 3.0.                                                                                |
| [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)             | Enumera le origini nell'elenco di origine di una patch o di un prodotto specificato. Disponibile in Windows Installer 3.0.                                                                                                              |



 

## <a name="component-specific-functions"></a>Component-Specific funzioni



| Nome                                                                     | Descrizione                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)                         | Installa e restituisce il percorso completo del componente per un assembly.                                                                                                                                                                 |
| [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)                       | Installa e restituisce il percorso completo del componente.                                                                                                                                                                  |
| [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)     | Installa e restituisce il percorso completo del componente di un componente completo.                                                                                                                                                        |
| [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) | Installa e restituisce il percorso completo del componente di un componente completo pubblicato da un prodotto.                                                                                                                         |
| [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)                       | Restituisce il percorso completo o la chiave del Registro di sistema a un componente installato.                                                                                                                                                              |
| [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)                   | Restituisce il percorso completo o la chiave del Registro di sistema a un componente installato tra gli account utente e il contesto di installazione. **[Windows Installer 4.5 e versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato.<br/> |
| [**MsiLocateComponent**](/windows/desktop/api/Msi/nf-msi-msilocatecomponenta)                         | Restituisce il percorso completo di un componente installato senza codice prodotto.                                                                                                                                                       |
| [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)                 | Restituisce lo stato installato per un componente. Può eseguire query sui componenti di un'istanza di un prodotto installato in account utente diversi dall'utente corrente. Disponibile in Windows Installer 3.0 o versione successiva.                        |



 

## <a name="application-only-functions"></a>Application-Only funzioni



| Nome                                             | Descrizione                                                            |
|--------------------------------------------------|------------------------------------------------------------------------|
| [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) | Archivia le informazioni utente da un'installazione guidata.                   |
| [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)           | Incrementa il numero di utilizzi per una funzionalità e indica lo stato di installazione. |
| [**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)       | Incrementa il numero di utilizzi per una funzionalità e indica lo stato di installazione. |
| [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)   | Restituisce il codice prodotto usando il codice del componente.                         |



 

## <a name="system-status-functions"></a>Funzioni di stato del sistema



| Nome                                                             | Descrizione                                                                                                                                                                                                                       |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)                       | Enumera i prodotti annunciati.                                                                                                                                                                                                   |
| [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)                   | Enumera tutte le istanze di prodotti annunciati o installati in un contesto specificato. Disponibile in Windows Installer 3.0 o versione successiva.                                                                                    |
| [**MsiEnumRelatedProducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)         | Enumera i prodotti attualmente installati con un codice di aggiornamento specificato.                                                                                                                                                          |
| [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)                       | Enumera le funzionalità pubblicate.                                                                                                                                                                                                    |
| [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)                   | Enumera i componenti installati.                                                                                                                                                                                              |
| [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)               | Enumera i componenti installati tra gli account utente e il contesto di installazione. **[Windows Installer 4.5 e versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato.<br/>                                 |
| [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)                         | Enumera i client di un componente installato.                                                                                                                                                                                 |
| [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)                     | Enumera i client di un componente installato tra gli account utente e il contesto di installazione. **[Windows Installer 4.5 e versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato.<br/>                    |
| [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) | Enumera i qualificatori annunciati per un componente.                                                                                                                                                                             |
| [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)             | Restituisce lo stato installato di una funzionalità.                                                                                                                                                                                         |
| [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)         | Restituisce lo stato installato per una funzionalità del prodotto. Può eseguire query sulle funzionalità di un'istanza di un prodotto installato in account utente diversi dall'utente corrente. Disponibile in Windows Installer 3.0 o versione successiva.                        |
| [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)             | Restituisce lo stato installato per un'applicazione o un gruppo di applicazioni.                                                                                                                                                              |
| [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)                 | Restituisce le metriche di utilizzo per una funzionalità.                                                                                                                                                                                              |
| [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)                   | Restituisce informazioni sul prodotto per i prodotti pubblicati e installati.                                                                                                                                                                 |
| [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)               | Restituisce informazioni sul prodotto per i prodotti annunciati e installati. Può recuperare informazioni su un'istanza di un prodotto installato con un account utente diverso dall'utente corrente. Disponibile in Windows Installer 3.0 o versione successiva. |
| [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)                         | Restituisce le informazioni utente registrate per un prodotto installato.                                                                                                                                                                     |



 

## <a name="product-query-functions"></a>Funzioni di query sul prodotto



| Nome                                                               | Descrizione                                                                            |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta)                           | Apre un prodotto da usare con le funzioni che accedono al database.                    |
| [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)                           | Apre un pacchetto da usare con le funzioni che accedono al database.                    |
| [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)                       | Apre un pacchetto da usare con le funzioni che accedono al database.                    |
| [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)               | Verifica se il prodotto è installato con privilegi elevati.                      |
| [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) | Restituisce informazioni sul prodotto per un file script del programma di installazione.                              |
| [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)             | Recupera le proprietà nel database del prodotto.                                          |
| [**MsiGetShortcutTarget**](/windows/desktop/api/Msi/nf-msi-msigetshortcuttargeta)               | Esamina un collegamento e restituisce il prodotto, il nome della funzionalità e il componente, se disponibile. |
| [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)                     | Restituisce informazioni descrittive per una funzionalità.                                         |
| [**MsiVerifyPackage**](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)                       | Verifica che un file specificato sia un pacchetto di installazione.                             |



 

## <a name="patching-functions"></a>Funzioni di applicazione di patch



| Nome                                                                   | Descrizione                                                                                                                                                        |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)                                 | Richiama un'installazione e applica un pacchetto di patch.                                                                                                               |
| [**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)                    | Restituisce il GUID per ogni patch applicata a un prodotto e un elenco di trasformazioni di ogni patch applicata al prodotto.                                  |
| [**MsiGetPatchInfo**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoa)                             | Restituisce informazioni su una patch.                                                                                                                                 |
| [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)                           | Disinstalla una patch da un prodotto. Disponibile in Windows Installer 3.0.                                                                                             |
| [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)         | Determina la sequenza di applicazione migliore per un set di patch e prodotti. Disponibile in Windows Installer 3.0.                                                     |
| [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)             | Applica una o più patch ai prodotti. Disponibile in Windows Installer 3.0.                                                                                       |
| [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)                           | Enumera tutte le patch applicate per un prodotto in un determinato contesto o in tutti i contesti. Disponibile in Windows Installer 3.0.                                   |
| [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)                     | Quando viene fornito un elenco di file con estensione msp, questa funzione recupera l'elenco dei file che possono essere aggiornati dalle patch per il file targe. Disponibile in Windows Installer 4.0. |
| [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)                         | Esegue una query per ottenere informazioni sull'applicazione di una patch specificata a un prodotto specificato. Disponibile in Windows Installer 3.0.                                     |
| [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)               | Estrae informazioni da una patch. Disponibile in Windows Installer 3.0.                                                                                             |
| [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) | Determina il set migliore di patch necessarie per aggiornare un prodotto o un set di prodotti. Disponibile in Windows Installer 3.0.                                            |



 

## <a name="file-query-functions"></a>Funzioni di query su file



| Nome                                                                     | Descrizione                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)                                 | Accetta il percorso di un file e restituisce un hash a 128 bit del file.                                           |
| [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa) | Accetta il percorso di un file firmato digitalmente e restituisce il certificato e l'hash del firmatario del file. |
| [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona)                           | Restituisce la stringa di versione e la stringa di lingua.                                                             |



 

## <a name="transaction-management-functions"></a>Funzioni di gestione delle transazioni



| Nome                                               | Descrizione                                                                                                                                                                                         |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona) | Avvia l'elaborazione delle transazioni di un'installazione con più pacchetti e restituisce un identificatore per la transazione. Questa funzione è disponibile a partire da Windows Installer 4.5.                    |
| [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)   | Richiede al programma Windows di installazione di rendere il processo corrente il proprietario della transazione installando un'installazione con più pacchetti. Questa funzione è disponibile a partire da Windows Installer 4.5. |
| [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)     | Esegue il commit o il rollback di tutte le installazioni appartenenti alla transazione. Questa funzione è disponibile a partire da Windows Installer 4.5.                                                          |



 

## <a name="database-functions"></a>Funzioni di database

Oltre alle funzioni di Windows Installer identificate nelle tabelle precedenti, è possibile modificare le informazioni nel database di installazione usando le funzioni di accesso al database descritte nella sezione [Funzioni di](database-functions.md) database.

## <a name="installer-structures"></a>Strutture del programma di installazione

Inoltre, alcune informazioni nel database di installazione vengono gestite usando le strutture descritte nella sezione [Strutture del programma di](installer-structures.md) installazione.

 

 




