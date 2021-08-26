---
description: Di seguito è riportato un esempio di tabella di sequenza.
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: Esempio dettagliato della tabella sequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc6e9715850d05231080cd8cd832ac7f39c1e3044628bb307afb51bf92c2210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040191"
---
# <a name="sequence-table-detailed-example"></a>Esempio dettagliato della tabella sequence

Di seguito è riportato un esempio di tabella di sequenza.



| Azione                                          | Condition                                                       | Sequenza |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [LaunchConditions](launchconditions-action.md) |                                                                 |          |
| [Appsearch](appsearch-action.md)               |                                                                 | 200      |
| [CCPSearch](ccpsearch-action.md)               | CCP \_ TEST                                                       | 300      |
| CCPDialog                                       | NOT \_ CCP \_ SUCCESS                                               | 400      |
| MyCustomConfig                                  | NON [ **installato**](installed.md)                              | 500      |
| [CostInitialize](costinitialize-action.md)     |                                                                 | 600      |
| [FileCost](filecost-action.md)                 |                                                                 | 700      |
| [CostFinalize](costfinalize-action.md)         |                                                                 | 800      |
| InstallDialog                                   | NON [ **installato**](installed.md)                              | 900      |
| Finestra di dialogo Manutenzione                               | [**Installato**](installed.md) AND NOT [ **Resume**](resume.md) | 1000     |
| ActionDialog                                    |                                                                 | 1100     |
| [RegisterProduct](registerproduct-action.md)   |                                                                 | 1200     |
| [InstallValidate](installvalidate-action.md)   |                                                                 | 1300     |
| [InstallFiles](installfiles-action.md)         |                                                                 | 1400     |
| MyCustomAction                                  | $MyComponent > 2                                             | 1500     |
| [InstallFinalize](installfinalize-action.md)   |                                                                 | 1600     |



 

Le azioni seguenti in questa tabella di sequenza sono definite dal programma di installazione e sono esempi di azioni standard:

[LaunchConditions](launchconditions-action.md)

 

[Appsearch](appsearch-action.md)

 

[CCPSearch](ccpsearch-action.md)

 

[CostInitialize](costinitialize-action.md)

 

[FileCost](filecost-action.md)

 

[CostFinalize](costfinalize-action.md)

 

[RegisterProduct](registerproduct-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallValidate](installvalidate-action.md)

Le azioni seguenti sono state definite dall'autore [](custom-actions.md) della tabella e sono esempi di azioni personalizzate e devono essere elencate nella [tabella CustomAction](customaction-table.md):

MyCustomConfig

 

MyCustomAction

Le voci rimanenti nel campo Azione sono chiavi esterne nella [tabella Dialog](dialog-table.md). Specificano i nomi delle finestre di dialogo che verranno visualizzate se il campo della condizione restituisce True.

CCPDialog

 

InstallDialog

 

Finestra di dialogo Manutenzione

 

ActionDialog

La colonna Condizione fa in modo che il programma di installazione salti l'azione se la proprietà o l'espressione in questo campo è False. La [**proprietà Installed**](installed.md) e la proprietà [**RESUME**](resume.md) sono esempi di proprietà impostate dal programma di installazione. La [**proprietà Installed**](installed.md) è impostata su true se il prodotto è già installato e la proprietà [**RESUME**](resume.md) viene impostata se si riprende un'installazione sospesa. Le proprietà CCP TEST e NOT CCP SUCCESS sono esempi di proprietà che possono essere impostate dalla riga di comando dall'utente che \_ \_ installa \_ l'applicazione.

Tutte le azioni vengono eseguite in sequenza con i passaggi condizionali seguenti:

-   CPPSearch viene eseguito solo se CCP \_ TEST è impostato.
-   CCPDialog viene eseguito solo se l'opzione NOT \_ CCP \_ SUCCESS è impostata.
-   MaintenanceDialog viene eseguito solo se il prodotto è già installato e se non si tratta di un'installazione ripresa dopo la sospensione.
-   MyCustomAction viene eseguito solo se l'espressione nella colonna Condizione è True. L'espressione $MyComponent > 2 fa riferimento allo stato dell'azione del componente denominato MyComponent. Questa condizione indica che MyCustomAction deve essere eseguito solo se MyComponent è impostato per l'installazione. Per altre informazioni sugli stati Azione e Selezione, vedere la [**proprietà FeatureRequestState,**](session-featurerequeststate.md) la [tabella Feature](feature-table.md)e l'azione [InstallFiles](installfiles-action.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo delle proprietà](using-properties.md)
</dt> <dt>

[Sintassi di istruzioni condizionali](conditional-statement-syntax.md)
</dt> </dl>

 

 



