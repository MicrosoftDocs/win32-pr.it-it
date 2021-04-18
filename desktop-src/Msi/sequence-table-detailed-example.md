---
description: Di seguito è riportato un esempio di una tabella di sequenza.
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: Esempio dettagliato della tabella Sequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4698d5270f2f246fe6e676799ea239e47a950c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318984"
---
# <a name="sequence-table-detailed-example"></a>Esempio dettagliato della tabella Sequence

Di seguito è riportato un esempio di una tabella di sequenza.



| Azione                                          | Condizione                                                       | Sequenza |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [LaunchConditions](launchconditions-action.md) |                                                                 |          |
| [AppSearch](appsearch-action.md)               |                                                                 | 200      |
| [CCPSearch](ccpsearch-action.md)               | \_test CCP                                                       | 300      |
| CCPDialog                                       | \_ \_ esito negativo del CCP                                               | 400      |
| MyCustomConfig                                  | NON [ **installato**](installed.md)                              | 500      |
| [CostInitialize](costinitialize-action.md)     |                                                                 | 600      |
| [Filecost](filecost-action.md)                 |                                                                 | 700      |
| [CostFinalize secondo](costfinalize-action.md)         |                                                                 | 800      |
| InstallDialog                                   | NON [ **installato**](installed.md)                              | 900      |
| MaintenanceDialog                               | [**Installazione**](installed.md) completata E non [ **riprendere**](resume.md) | 1000     |
| ActionDialog                                    |                                                                 | 1100     |
| [RegisterProduct](registerproduct-action.md)   |                                                                 | 1200     |
| [InstallValidate](installvalidate-action.md)   |                                                                 | 1300     |
| [InstallFiles](installfiles-action.md)         |                                                                 | 1400     |
| MyCustomAction                                  | $MyComponent > 2                                             | 1500     |
| [InstallFinalize](installfinalize-action.md)   |                                                                 | 1600     |



 

Le azioni seguenti in questa tabella di sequenza sono definite dal programma di installazione e sono esempi di azioni standard:

[LaunchConditions](launchconditions-action.md)

 

[AppSearch](appsearch-action.md)

 

[CCPSearch](ccpsearch-action.md)

 

[CostInitialize](costinitialize-action.md)

 

[Filecost](filecost-action.md)

 

[CostFinalize secondo](costfinalize-action.md)

 

[RegisterProduct](registerproduct-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallValidate](installvalidate-action.md)

Le azioni seguenti sono state definite dall'autore della tabella e sono esempi di [azioni personalizzate](custom-actions.md) e devono essere elencate nella [tabella CustomAction](customaction-table.md):

MyCustomConfig

 

MyCustomAction

Le voci rimanenti nel campo azione sono chiavi esterne nella [tabella della finestra di dialogo](dialog-table.md). Specificano i nomi delle finestre di dialogo che verranno visualizzate se il campo condizione restituisce true.

CCPDialog

 

InstallDialog

 

MaintenanceDialog

 

ActionDialog

La colonna Condition impedisce al programma di installazione di ignorare l'azione se la proprietà o l'espressione in questo campo è false. La proprietà [**installata**](installed.md) e la proprietà [**Resume**](resume.md) sono esempi di proprietà impostate dal programma di installazione. La proprietà [**installata**](installed.md) è impostata su true se il prodotto è già installato e la proprietà [**Resume**](resume.md) viene impostata in caso di ripresa di un'installazione sospesa. Il \_ test CCP e le \_ proprietà non \_ riuscite CCP sono esempi di proprietà che possono essere impostate dalla riga di comando dall'utente che installa l'applicazione.

Tutte le azioni vengono eseguite in sequenza con i passaggi condizionali seguenti:

-   CPPSearch viene eseguito solo se \_ è impostato il test CCP.
-   CCPDialog viene eseguito solo se non \_ \_ è stata impostata la funzione CCP riuscita.
-   MaintenanceDialog viene eseguito solo se questo prodotto è già installato e se non si tratta di un'installazione che verrà ripresa dopo essere stata sospesa.
-   MyCustomAction viene eseguito solo se l'espressione nella colonna condizione è true. L'espressione $MyComponent > 2 fa riferimento allo stato dell'azione del componente denominato "componente". Questa condizione indica che MyCustomAction deve essere eseguito solo se il componente è impostato per l'installazione. Per altre informazioni sugli Stati delle azioni e sugli stati di selezione, vedere la proprietà [**FeatureRequestState**](session-featurerequeststate.md) , la [tabella delle funzionalità](feature-table.md)e l' [azione InstallFiles](installfiles-action.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo delle proprietà](using-properties.md)
</dt> <dt>

[Sintassi dell'istruzione condizionale](conditional-statement-syntax.md)
</dt> </dl>

 

 



