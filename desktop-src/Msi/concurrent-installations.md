---
description: Le installazioni simultanee, denominate anche installazioni annidate, sono una funzionalità deprecata del programma di Windows installazione.
ms.assetid: 579ae4ee-47a0-440e-81ca-ea8bf60c5349
title: Installazioni simultanee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09264df8c47c08f7d1512b46d65572d3572d5190f960254c8ed13182dd668657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144408"
---
# <a name="concurrent-installations"></a>Installazioni simultanee

Le installazioni simultanee, denominate anche installazioni annidate, sono una funzionalità deprecata del programma di Windows installazione. Le applicazioni installate con installazioni simultanee possono avere esito negativo perché sono difficili da usare correttamente per i clienti. Non usare installazioni simultanee per installare prodotti che devono essere rilasciati al pubblico. Le installazioni simultanee possono avere un'applicabilità limitata negli ambienti aziendali controllati quando vengono usate per installare applicazioni non destinate a una versione pubblica. La documentazione relativa alle installazioni simultanee è disponibile per gli autori di pacchetti che vogliono usare installazioni simultanee con applicazioni che non sono per la distribuzione pubblica.

Un'azione di installazione simultanea installa un altro Windows di installazione durante un'installazione attualmente in esecuzione. Un'installazione simultanea viene aggiunta a un pacchetto mediante la creazione di un'azione di installazione simultanea nella [tabella CustomAction](customaction-table.md) e la pianificazione di questa azione personalizzata nelle tabelle di sequenza. Il campo Target della tabella CustomAction contiene una stringa di impostazioni di proprietà pubbliche usate dall'installazione simultanea. Il campo Source della tabella CustomAction identifica il pacchetto simultaneo. Un'azione di installazione simultanea può solo reinstallare o rimuovere un'applicazione installata dal pacchetto di installazione dell'applicazione corrente.

Il tipo di azione di installazione simultanea viene specificato nel campo Tipo della tabella CustomAction. A seconda del tipo di azione personalizzata, il pacchetto per l'applicazione simultanea può risiedere in una risorsa di archiviazione secondaria del pacchetto principale, come file in un percorso specificato da una proprietà o come applicazione annunciata nel computer dell'utente. I tipi di azioni personalizzate seguenti eseguono un'installazione simultanea.



| Tipo di azione personalizzata                                 | Descrizione                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------|
| [Tipo di azione personalizzata 7](custom-action-type-7.md)   | Installazione simultanea di un prodotto che risiede nel pacchetto di installazione.      |
| [Tipo di azione personalizzata 23](custom-action-type-23.md) | Installazione simultanea di un pacchetto di installazione all'interno dell'albero di origine corrente. |
| [Tipo di azione personalizzata 39](custom-action-type-39.md) | Installazione simultanea di un pacchetto di installazione annunciato.                     |



 

Un'installazione simultanea condivide la stessa interfaccia utente e le stesse impostazioni di registrazione dell'installazione principale.

Le azioni di installazione simultanee devono essere inserite tra [l'azione InstallInitialize](installinitialize-action.md) [e l'azione InstallFinalize](installfinalize-action.md) della sequenza di azioni dell'installazione principale. Dopo il rollback dell'installazione principale, anche il programma di installazione rollbackrà l'installazione simultanea. L'uso [dell'esecuzione posticipata](deferred-execution-custom-actions.md) con le azioni di installazione simultanee non è necessario perché il programma di installazione combina le informazioni di rollback dalle installazioni simultanee e principali. Tutte le modifiche vengono annullate in seguito a un'installazione di rollback.

I valori restituiti per le azioni di installazione simultanee sono gli stessi di altre azioni personalizzate. Vedere [Valori restituiti dell'azione personalizzata.](custom-action-return-values.md)

Le azioni standard o personalizzate che specificano un riavvio automatico del sistema o richiedono il riavvio dell'utente possono anche eseguire il riavvio o la richiesta dall'interno di un'installazione simultanea.

Una volta avviata un'installazione simultanea, il programma di installazione blocca tutte le altre installazioni fino al completamento dell'installazione simultanea e prima di continuare l'installazione principale. Il programma di installazione può eseguire installazioni simultanee solo come azioni personalizzate sincrone. Vedere [Azioni personalizzate sincrone e asincrone.](synchronous-and-asynchronous-custom-actions.md) I flag di opzione descritti in [Custom Action Return Processing Options](custom-action-return-processing-options.md) devono essere impostati su none (+0) o **msidbCustomActionTypeContinue** (+64).

Un'azione di installazione simultanea può installare un'applicazione da eseguire in locale, da eseguire dall'origine, da reinstallare o da rimuovere nello stesso modo in cui si usa [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) per un'installazione normale. Per specificare il tipo di installazione, passare la proprietà [**ADDLOCAL**](addlocal.md), [**ADDSOURCE**](addsource.md), [**REINSTALL**](reinstall.md)o [**REMOVE**](remove.md) all'azione di installazione simultanea.

Le azioni di installazione simultanee possono essere create in coppie, un'azione usata per l'installazione e l'altra azione usata per rimuovere l'installazione simultanea. Per [l'installazione viene in genere](custom-action-type-7.md) usato un tipo di azione personalizzata 7 o un'azione personalizzata di tipo [23.](custom-action-type-23.md) [Un'azione personalizzata di tipo 39](custom-action-type-39.md) viene in genere usata per rimuovere l'installazione simultanea quando il prodotto padre viene disinstallato. Il record per l'azione personalizzata di rimozione nella tabella [CustomAction](customaction-table.md) può avere il GUID del codice prodotto nel campo Source e "REMOVE=ALL" nel campo Target. Le due azioni personalizzate devono essere scritte nella tabella della sequenza di azioni con condizioni che si escludono a vicenda. Ad esempio, l'azione personalizzata che installa il prodotto può avere "NOT Installato" nel campo Condizione e l'azione personalizzata rimuove l'installazione simultanea può avere REMOVE="ALL" nel campo Condizione.

Non esiste alcun metodo per eseguire query su un pacchetto per il relativo costo. Ciò rende difficile il costo di un'installazione simultanea. È necessario aggiungere righe alla [tabella ReserveCost per](reservecost-table.md) indicare le cartelle e i costi peggiori del componente associato all'installazione simultanea.

Le uniche [opzioni di elaborazione di](custom-action-return-processing-options.md) restituzione delle azioni personalizzate disponibili con le azioni di installazione simultanee sono nessuna (+0) o **msidbCustomActionTypeContinue** (+64).

Si noti che un'installazione padre non può chiamare il proprio pacchetto come azione di installazione simultanea.

Si noti che se un'installazione per computer tenta di eseguire un'installazione simultanea per utente, il programma di installazione registra l'installazione padre in base all'utente per impostazione predefinita. Ciò può causare la rimozione non corretta dell'applicazione da parte del programma di installazione, perché il programma di installazione tenta di disinstallare l'applicazione per ogni computer quando viene effettivamente registrata come per utente. Per forzare lo stato di un'installazione simultanea per tenere traccia dello stato dell'installazione padre, immettere ALLUSERS=" ALLUSERS " nella colonna Target della \[ \] tabella [CustomAction](customaction-table.md). In questo caso, l'installazione simultanea è per computer se l'elemento padre è per computer e l'installazione simultanea è per utente se l'elemento padre è per utente.

Gli sviluppatori devono prendere nota degli avvisi seguenti durante la creazione di installazioni simultanee.

-   Le installazioni simultanee non possono condividere componenti.
-   Un'installazione amministrativa non può contenere anche un'installazione simultanea.
-   L'applicazione di patch e l'aggiornamento potrebbero non funzionare con installazioni simultanee.
-   Il programma di installazione potrebbe non costare correttamente un'installazione simultanea.
-   Le barre di stato integrate non possono essere usate con installazioni simultanee.
-   Le risorse che devono essere annunciate non possono essere installate dall'installazione simultanea.
-   Un pacchetto che esegue un'installazione simultanea di un'applicazione deve anche disinstallare l'applicazione simultanea quando viene disinstallato il prodotto padre.

Per evitare che un pacchetto venga installato come installazione simultanea, aggiungere una delle istruzioni condizionali seguenti alla [tabella LaunchCondition.](launchcondition-table.md) In questo modo si impedisce che il pacchetto venga installato da un'azione di installazione simultanea eseguita da un'altra installazione. Ciò non impedisce la rimozione del pacchetto tramite [l'azione RemoveExistingProducts.](removeexistingproducts-action.md) Vedere anche la [**proprietà ParentOriginalDatabase**](parentoriginaldatabase.md) e [**la proprietà ParentProductCode.**](parentproductcode.md)

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

 

 



