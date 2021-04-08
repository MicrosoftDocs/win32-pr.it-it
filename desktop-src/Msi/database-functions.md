---
description: Questo materiale è destinato agli sviluppatori che scrivono programmi di installazione e sviluppatori che desiderano ottenere altre informazioni sulle tabelle del database del programma di installazione. Per informazioni generali sul programma di installazione, vedere informazioni su Windows Installer.
ms.assetid: 95516437-9708-4f4e-a5c2-7bcd4741c776
title: Funzioni di database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a4233437d24944c8bb7fe5c7de6412e700022b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752799"
---
# <a name="database-functions"></a>Funzioni di database

Questo materiale è destinato agli sviluppatori che scrivono programmi di installazione e sviluppatori che desiderano ottenere altre informazioni sulle tabelle del database del programma di installazione. Per informazioni generali sul programma di installazione, vedere [informazioni su Windows Installer](about-windows-installer.md).

È possibile utilizzare le funzioni di accesso del programma di installazione per accedere al database e al processo di installazione. Queste funzioni devono essere utilizzate solo da azioni di installazione personalizzate e strumenti di creazione. Alcune funzioni di accesso del programma di installazione richiedono stringhe di query SQL per eseguire query sul database. Le query devono rispettare la [sintassi SQL](sql-syntax.md)del programma di installazione.

Questo argomento elenca le funzioni di accesso al database del programma di installazione per categoria.

## <a name="general-database-access-functions"></a>Funzioni di accesso al database generali



| Funzione                                                             | Descrizione                                                                             |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)                       | Consente di eseguire il commit delle modifiche in un database.                                                          |
| [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa)       | Restituisce i nomi di tutte le colonne chiave primaria.                                       |
| [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta) | Restituisce un'enumerazione che descrive lo stato di una tabella.                                 |
| [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)                   | Prepara una query di database e crea un oggetto visualizzazione.                                    |
| [**Funzione MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase)                 | Restituisce il database attivo per l'installazione.                                       |
| [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)                 | Restituisce i nomi o le definizioni delle colonne.                                                    |
| [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)                           | Apre un file di database per l'accesso ai dati.                                                  |
| [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)                                 | Rilascia il set di risultati per una visualizzazione eseguita.                                           |
| [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)                             | Esegue la query di visualizzazione e fornisce i parametri richiesti.                               |
| [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)                                 | Recupera il record sequenziale successivo dalla visualizzazione.                                       |
| [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)                           | Restituisce l'errore che si è verificato nella funzione [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) . |
| [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)                               | Aggiorna un record recuperato.                                                               |



 

## <a name="database-management-functions"></a>Funzioni di gestione di database



| Funzione                                                               | Descrizione                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) | Crea informazioni di riepilogo per una trasformazione esistente.           |
| [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)         | Applica una trasformazione a un database.                               |
| [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)                         | Esporta una tabella da un database aperto in un file di archivio di testo.    |
| [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)   | Genera un file di trasformazione di differenze tra due database. |
| [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)                         | Importa una tabella di archivio di testo del programma di installazione in un database aperto.   |
| [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)                           | Unisce due database.                                   |
| [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)                     | Restituisce lo stato del database.                               |



 

## <a name="record-processing-functions"></a>Funzioni di elaborazione dei record



| Funzione                                                 | Descrizione                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------|
| [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord)               | Crea un nuovo oggetto record con il numero di campi specificato.      |
| [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)               | Formatta i dati e le proprietà dei campi del record utilizzando una stringa di formato. |
| [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata)         | Imposta su null tutti i campi di un record.                            |
| [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize)           | Restituisce la lunghezza di un campo di record.                           |
| [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) | Restituisce il numero di campi in un record.                       |
| [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger)       | Restituisce il valore intero da un campo di record.                  |
| [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)         | Restituisce il valore stringa di un campo di record.                     |
| [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull)               | Indica se un campo di record è null.                         |
| [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream)       | Legge i byte da un campo del flusso di record in un buffer.           |
| [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)       | Imposta un campo di record in un campo integer.                        |
| [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)         | Imposta un campo del flusso di record da un file.                         |
| [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)         | Copia una stringa nel campo designato.                      |



 

## <a name="summary-information-property-functions"></a>Funzioni di proprietà delle informazioni di riepilogo



| Funzione                                                                 | Descrizione                                                            |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)             | Ottiene l'handle per il flusso di informazioni di riepilogo del database del programma di installazione.    |
| [**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)           | Ottiene una singola proprietà dalle informazioni di riepilogo.                   |
| [**MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) | Restituisce il numero di proprietà nel flusso di informazioni di riepilogo.        |
| [**MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist)                   | Scrive le informazioni di riepilogo modificate nel flusso di informazioni di riepilogo. |
| [**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)           | Imposta una singola proprietà di informazioni di riepilogo.                            |



 

## <a name="installer-state-access-functions"></a>Funzioni di accesso allo stato del programma di installazione



| Funzione                                               | Descrizione                                                 |
|--------------------------------------------------------|-------------------------------------------------------------|
| [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)               | Restituisce la lingua numerica dell'installazione corrente.   |
| [**MsiGetLastErrorRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlasterrorrecord) | Restituisce il record degli errori restituito per l'ultima volta per il processo chiamante. |
| [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)                       | Restituisce uno degli Stati di installazione interni booleani.    |
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)               | Ottiene il valore di una proprietà del programma di installazione.                    |
| [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)               | Imposta il valore di una proprietà di installazione.                 |
| [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode)                       | Imposta uno stato booleano del motore interno.                      |



 

## <a name="installer-action-functions"></a>Funzioni di azione del programma di installazione



| Funzione                                             | Descrizione                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)                   | Esegue un'azione predefinita, un'azione personalizzata o un'azione guidata dell'interfaccia utente. |
| [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) | Valuta un'espressione condizionale contenente i nomi e i valori delle proprietà.  |
| [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)       | Invia un record di errore al programma di installazione per l'elaborazione.                    |
| [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)                   | Esegue una sequenza di azioni.                                              |



 

## <a name="installer-location-functions"></a>Funzioni del percorso del programma di installazione



| Funzione                                     | Descrizione                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha) | Restituisce il percorso di origine completo per una cartella nella tabella directory. |
| [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) | Restituisce il percorso di destinazione completo per una cartella nella tabella directory. |
| [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) | Imposta il percorso di destinazione completo per una cartella nella tabella directory.    |



 

## <a name="installer-selection-functions"></a>Funzioni di selezione del programma di installazione



| Funzione                                                     | Descrizione                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [**MsiEnumComponentCosts**](/windows/desktop/api/Msiquery/nf-msiquery-msienumcomponentcostsa)       | Enumera lo spazio su disco richiesto per l'installazione di un componente. |
| [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)         | Ottiene lo stato di un componente.                                    |
| [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)               | Restituisce lo spazio su disco richiesto da una funzionalità.                        |
| [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)             | Ottiene lo stato di una funzionalità.                                         |
| [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) | Restituisce uno stato di installazione valido.                                  |
| [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)         | Imposta un componente sullo stato specificato.                             |
| [**MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa)   | Modifica gli attributi predefiniti di una funzionalità in fase di esecuzione.            |
| [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)             | Imposta una funzionalità sullo stato specificato.                                 |
| [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)             | Imposta il livello di installazione di un'installazione completa del prodotto.          |
| [**MsiVerifyDiskSpace**](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)             | Verifica la presenza di spazio su disco sufficiente.                                    |



 

## <a name="user-interface-functions"></a>Funzioni dell'interfaccia utente



| Funzione                                           | Descrizione                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)   | Abilita la modalità di anteprima dell'interfaccia utente.                             |
| [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) | Visualizza un tabellone con il controllo host nella finestra di dialogo visualizzata. |
| [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)       | Visualizza una finestra di dialogo non modale e inattiva.                         |



 

Tutte le funzioni supportano le chiamate ANSI e Unicode. Per usare queste funzioni, includere MsiQuery. h e il collegamento con MSI. lib.

## <a name="installation-functions"></a>Funzioni di installazione

Oltre alle funzioni di accesso al database elencate in precedenza, è possibile creare un pacchetto di installazione per un'applicazione usando le funzioni del programma di installazione elencate nella sezione riferimento per le funzioni del [programma di installazione](installer-function-reference.md) .

 

 



