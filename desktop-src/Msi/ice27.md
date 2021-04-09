---
description: ICE27 convalida le tabelle di sequenza di un pacchetto di installazione per le azioni valide, le restrizioni della sequenza di azione e l'organizzazione nelle sezioni ricerca, determinazione costi, selezione ed esecuzione.
ms.assetid: c5292a3c-57bb-4203-96a1-6d747f554178
title: ICE27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb4b90b313f5f78874fb93ce9d32c3650b97064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880738"
---
# <a name="ice27"></a>ICE27

ICE27 convalida le [*tabelle di sequenza*](s-gly.md) di un pacchetto di installazione per le azioni valide, le restrizioni della sequenza di azione e l'organizzazione nelle sezioni ricerca, determinazione costi, selezione ed esecuzione.

L'azione personalizzata ICE27 convalida quanto segue:

-   Le azioni elencate nella colonna azione delle tabelle di sequenza sono un'azione [standard](standard-actions.md), un'azione personalizzata elencata nella [tabella CustomAction](customaction-table.md)o una finestra di dialogo elencata nella tabella della [finestra di dialogo](dialog-table.md).
-   Tali azioni soggette a restrizioni di sequenziazione sono nell'ordine relativo corretto tra loro nella sequenza di azione. Le restrizioni di sequenziazione vengono generate quando un'azione dipende da un'altra.
-   Le azioni limitate a una particolare sezione della sequenza si trovano a cui appartengono. ICE27 convalida la seguente organizzazione delle tabelle di sequenza. Si noti che non tutte le tabelle di sequenza hanno ogni sezione. Vedere le tabelle di sequenza suggerite in [uso di una tabella di sequenza](using-a-sequence-table.md).



| Sezione della tabella Sequence | Intervallo nella sequenza di azione                                                                       | Azioni che appartengono alla sezione                                                                                                                                                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cerca                 | {Start} in [CostInitialize](costinitialize-action.md)                                         | Azioni che cercano le applicazioni esistenti. [AppSearch](appsearch-action.md)<br/> [CCPSearch](ccpsearch-action.md)<br/>                                                                                                         |
| Costano                | Azione da [CostInitialize](costinitialize-action.md) a [CostFinalize secondo](costfinalize-action.md)  | Azioni che eseguono il [costo del file](file-costing.md). [CostInitialize](costinitialize-action.md)<br/> [Filecost](filecost-action.md)<br/> [CostFinalize secondo](costfinalize-action.md)<br/>                                           |
| Selezione              | Da [CostFinalize secondo](costfinalize-action.md) a [InstallValidate](installvalidate-action.md)       | Azioni che impostano le cartelle o gli Stati delle funzionalità. [Azione SetODBCFolders](setodbcfolders-action.md)<br/>                                                                                                                                        |
| Esecuzione              | Da [InstallValidate](installvalidate-action.md) a [InstallFinalize](installfinalize-action.md) | Azioni script, ad esempio registrazione, pubblicazione, installazione (in cui vengono copiati i file). Si noti che l' [azione InstallFinalize](installfinalize-action.md) deve essere presente nella tabella se e solo se sono presenti azioni nella sezione esecuzione.<br/> |
| Postesecuzione          | [InstallFinalize](installfinalize-action.md) a {end}                                         | [RemoveExistingProducts](removeexistingproducts-action.md)                                                                                                                                                                                      |



 

ICE27 convalida le tabelle seguenti:

-   [AdvtExecuteSequence](advtexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Risultato

ICE27 Invia un messaggio di errore se sono presenti tabelle di sequenza nel pacchetto con sequenza di azioni o organizzazione non valida.

## <a name="example"></a>Esempio



| Errore ICE27                                                                                                                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azione sconosciuta:' action1' della tabella InstallExecuteSequnence. Non è un'azione standard e non è stata trovata nelle tabelle CustomAction o Dialog    | Nella tabella di sequenza è presente un'azione che indica che non si tratta di [azioni standard](standard-actions.md), di un'azione personalizzata elencata nella [tabella CustomAction](customaction-table.md)o di una finestra di dialogo elencata nella [tabella della finestra di dialogo](dialog-table.md).                                                                                                                                                                                                                                                                       |
| ' Action2' nella tabella InstallExecute in una posizione errata. Corrente: ricerca, corrette: determinazione del costo                                                 | In una tabella di sequenza è presente un'azione erroneamente posizionata rispetto al numero di sequenza nella colonna sequenza. "Current" indica la posizione corrente dell'azione nelle sezioni Search, Costing, Selection o Execution della tabella di sequenza indicata.<br/> "Correct" indica la sezione a cui appartiene l'azione.<br/> Per correggere l'errore, modificare il numero di sequenza dell'azione nella sezione corretta. Si noti che alcune azioni possono trovarsi in più di una sezione.<br/> |
| L'azione ' InstallFinalize ' nella tabella InstallExecuteSequence può essere chiamata solo quando sono presenti operazioni script da eseguire             | In una tabella di sequenza è presente un' [azione InstallFinalize](installfinalize-action.md) che non contiene alcuna operazione script nella sezione Execution della tabella. Aggiungere azioni alla sezione Execution oppure rimuovere l'azione InstallFinalize dalla tabella.<br/>                                                                                                                                                                                                                                                        |
| InstallFinalize deve essere chiamato nella tabella InstallExecuteSequence perché sono presenti operazioni di script da eseguire                            | È presente una tabella di sequenza contenente le azioni nella sezione di esecuzione che non include l' [azione InstallFinalize](installfinalize-action.md). Aggiungere l'azione InstallFinalize a questa tabella di sequenza e assegnarle il numero di sequenza più grande per inserirlo per ultimo nella sequenza di azione.<br/>                                                                                                                                                                                                                            |
| Azione:' Action3' nella tabella InstallExecuteSequence deve essere precedente all'azione ' action5'. Current seq \# : 1200. Seq dipendente \# : 1100 | Nella tabella di sequenza indicata è presente un'azione sequenziata dopo un'azione dipendente. Modificare il numero di sequenza sull'azione dipendente in modo che venga prima dell'azione.<br/>                                                                                                                                                                                                                                                                                                                                    |
| Azione:' action4' nella tabella InstallExecuteSequence deve essere successiva all'azione ' Action6'.                                             | Nella tabella di sequenza indicata è presente un'azione sequenziata prima di un'azione da cui dipende. Modificare il numero di sequenza sull'azione in modo che venga eseguita dopo l'azione dipendente.<br/>                                                                                                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




