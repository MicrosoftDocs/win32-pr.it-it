---
description: Le installazioni simultanee, denominate anche installazioni annidate, sono una funzionalità deprecata del Windows Installer.
ms.assetid: 579ae4ee-47a0-440e-81ca-ea8bf60c5349
title: Installazioni simultanee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d89f2ef4af062c8151935fefab471603f79d7633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883013"
---
# <a name="concurrent-installations"></a>Installazioni simultanee

Le installazioni simultanee, denominate anche installazioni annidate, sono una funzionalità deprecata del Windows Installer. Le applicazioni installate con installazioni simultanee possono avere esito negativo perché risultano difficoltose per il servizio dei clienti. Non usare installazioni simultanee per installare i prodotti destinati a essere rilasciati al pubblico. Le installazioni simultanee possono avere un'applicabilità limitata negli ambienti aziendali controllati quando vengono usate per installare le applicazioni che non sono destinate alla versione pubblica. La documentazione sulle installazioni simultanee è disponibile per gli autori di pacchetti che vogliono usare installazioni simultanee con applicazioni non per la distribuzione pubblica.

Un'azione di installazione simultanea installa un altro pacchetto Windows Installer durante un'installazione attualmente in esecuzione. Un'installazione simultanea viene aggiunta a un pacchetto mediante la creazione di un'azione di installazione simultanea nella [tabella CustomAction](customaction-table.md) e la pianificazione di questa azione personalizzata nelle tabelle di sequenza. Il campo di destinazione della tabella CustomAction contiene una stringa di impostazioni di proprietà pubbliche utilizzate dall'installazione simultanea. Il campo di origine della tabella CustomAction identifica il pacchetto simultaneo. Un'azione di installazione simultanea può reinstallare o rimuovere solo un'applicazione installata dal pacchetto di installazione dell'applicazione corrente.

Il tipo di azione di installazione simultanea è specificato nel campo Type della tabella CustomAction. A seconda del tipo di azione personalizzata, il pacchetto per l'applicazione simultanea può risiedere in un sottoarchivio del pacchetto principale, come file in una posizione specificata da una proprietà o come applicazione annunciata nel computer dell'utente. I tipi di azioni personalizzate seguenti eseguono un'installazione simultanea.



| Tipo di azione personalizzata                                 | Descrizione                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------|
| [Tipo di azione personalizzata 7](custom-action-type-7.md)   | Installazione simultanea di un prodotto che risiede nel pacchetto di installazione.      |
| [Tipo di azione personalizzata 23](custom-action-type-23.md) | Installazione simultanea di un pacchetto di installazione nell'albero di origine corrente. |
| [Tipo di azione personalizzata 39](custom-action-type-39.md) | Installazione simultanea di un pacchetto del programma di installazione annunciato.                     |



 

Un'installazione simultanea condivide la stessa interfaccia utente e le stesse impostazioni di registrazione dell'installazione principale.

Le azioni di installazione simultanee devono essere inserite tra l' [azione InstallInitialize](installinitialize-action.md) e l' [azione InstallFinalize](installfinalize-action.md) della sequenza di azione dell'installazione principale. Al rollback dell'installazione principale, il programma di installazione eseguirà il rollback anche dell'installazione simultanea. L'uso dell' [esecuzione posticipata](deferred-execution-custom-actions.md) con le azioni di installazione simultanea non è necessario perché il programma di installazione combina le informazioni di rollback dalle installazioni simultanee e principali. Tutte le modifiche vengono annullate durante un'installazione di rollback.

I valori restituiti per le azioni di installazione simultanee sono identici a quelli per altre azioni personalizzate. Vedere [valori restituiti dell'azione personalizzata](custom-action-return-values.md).

Anche le azioni standard o personalizzate che specificano un riavvio automatico del sistema o richiedono il riavvio dell'utente possono eseguire il riavvio o la richiesta dall'interno di un'installazione simultanea.

Quando il programma di installazione avvia un'installazione simultanea, blocca tutte le altre installazioni fino al completamento dell'installazione simultanea e prima di continuare con l'installazione principale. Il programma di installazione può eseguire installazioni simultanee come azioni personalizzate sincrone. Vedere [azioni personalizzate sincrone e asincrone](synchronous-and-asynchronous-custom-actions.md). I flag di opzione descritti in [Opzioni di elaborazione personalizzate per l'azione restituita](custom-action-return-processing-options.md) devono essere impostati su None (+ 0) o **msidbCustomActionTypeContinue** (+ 64).

Un'azione di installazione simultanea può installare un'applicazione da eseguire localmente, per l'esecuzione dall'origine, per la reinstallazione o per essere rimossa in modo analogo a quando si usa [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) per un'installazione normale. Per specificare il tipo di installazione, passare la proprietà [**ADDLOCAL**](addlocal.md), [**addsource**](addsource.md), [**REINSTALL**](reinstall.md)o [**Remove**](remove.md) all'azione di installazione simultanea.

Le azioni di installazione simultanee possono essere create in coppie, un'azione utilizzata per l'installazione e l'altra per la rimozione dell'installazione simultanea. Per l'installazione viene in genere usato un tipo di [azione personalizzato 7](custom-action-type-7.md) o un [tipo di azione personalizzata 23](custom-action-type-23.md) . Un [tipo di azione personalizzata 39](custom-action-type-39.md) viene in genere usato per rimuovere l'installazione simultanea quando viene disinstallato il prodotto padre. Il record per l'azione personalizzata di rimozione nella [tabella CustomAction](customaction-table.md) può includere il GUID del codice del prodotto nel campo di origine e "Remove = All" nel campo di destinazione. Le due azioni personalizzate devono essere create nella tabella di sequenza delle azioni con condizioni che si escludono a vicenda. Ad esempio, l'azione personalizzata che installa il prodotto può avere "non installato" nel campo condizione e l'azione personalizzata rimuove l'installazione simultanea può avere REMOVE = "ALL" nel campo condizione.

Non esiste alcun metodo per eseguire query su un pacchetto per il relativo costo. In questo modo, il costo di un'installazione simultanea risulta difficile. Per indicare le cartelle e i costi peggiori del componente associato all'installazione simultanea, è necessario aggiungere le righe alla [tabella ReserveCost](reservecost-table.md) .

Le uniche [Opzioni di elaborazione della restituzione dell'azione personalizzata](custom-action-return-processing-options.md) disponibili con le azioni di installazione simultanee sono None (+ 0) o **msidbCustomActionTypeContinue** (+ 64).

Si noti che un'installazione padre non può chiamare il proprio pacchetto come azione di installazione simultanea.

Si noti che se un'installazione per computer tenta di eseguire un'installazione simultanea per ogni utente, il programma di installazione registra l'installazione padre come utente per impostazione predefinita. Questa operazione può causare la rimozione non corretta dell'applicazione da parte del programma di installazione perché il programma di installazione tenta di disinstallare l'applicazione per computer quando viene effettivamente registrata come per utente. Per forzare lo stato di un'installazione simultanea a tenere traccia dello stato dell'installazione padre, immettere ALLUSERS = " \[ ALLUSERS \] " nella colonna destinazione della [tabella CustomAction](customaction-table.md). In questo caso, l'installazione simultanea è per computer se l'elemento padre è per computer e l'installazione simultanea è per utente se l'elemento padre è per utente.

Gli sviluppatori devono tenere presenti gli avvisi seguenti durante la creazione di installazioni simultanee.

-   Le installazioni simultanee non possono condividere componenti.
-   Un'installazione amministrativa non può contenere anche un'installazione simultanea.
-   L'applicazione di patch e l'aggiornamento potrebbero non funzionare con le installazioni simultanee.
-   Il programma di installazione potrebbe non costare correttamente un'installazione simultanea.
-   Non è possibile usare i ProgressBar integrati con installazioni simultanee.
-   Le risorse che devono essere annunciate non possono essere installate dall'installazione simultanea.
-   Un pacchetto che esegue un'installazione simultanea di un'applicazione deve disinstallare anche l'applicazione simultanea quando viene disinstallato il prodotto padre.

Per impedire l'installazione di un pacchetto come installazione simultanea, aggiungere una delle seguenti istruzioni condizionali alla tabella [LaunchCondition](launchcondition-table.md) . In questo modo si impedisce che il pacchetto venga installato da un'azione di installazione simultanea eseguita da un'altra installazione. Questo non impedisce che il pacchetto venga rimosso dall'azione [RemoveExistingProducts](removeexistingproducts-action.md) . Vedere anche la proprietà [**ParentOriginalDatabase**](parentoriginaldatabase.md) e la proprietà [**ParentProductCode**](parentproductcode.md) .

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

 

 



