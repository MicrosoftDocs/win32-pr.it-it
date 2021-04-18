---
description: Nella tabella InstallUISequence sono elencate le azioni che vengono eseguite quando viene eseguita l'azione di installazione di livello superiore e il livello dell'interfaccia utente interna è impostato sull'interfaccia utente completa o sull'interfaccia utente ridotta.
ms.assetid: 076d7c14-e302-4465-aed5-27a4b1f70ac8
title: Tabella InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a4d8d3033645ac1f414e3aff67be2a26d7a6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317128"
---
# <a name="installuisequence-table"></a>Tabella InstallUISequence

Nella tabella InstallUISequence sono elencate le azioni che vengono eseguite quando viene eseguita l' [azione di installazione](install-action.md) di livello superiore e il livello dell'interfaccia utente interna è impostato sull'interfaccia utente completa o sull'interfaccia utente ridotta. Il programma di installazione ignora le azioni in questa tabella se il livello dell'interfaccia utente è impostato su interfaccia utente di base o nessuna interfaccia utente. Vedere [informazioni sull'interfaccia utente](about-the-user-interface.md).

Le azioni della sequenza di installazione fino all' [azione InstallValidate](installvalidate-action.md)e le finestre di dialogo di uscita si trovano nella tabella InstallUISequence. Tutte le azioni da InstallValidate fino alla fine della sequenza di installazione si trovano nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Poiché è necessario che la tabella InstallExecuteSequence sia autonoma, sono necessarie azioni di inizializzazione, ad esempio [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [filecost](filecost-action.md), [CostFinalize secondo](costfinalize-action.md)e [ExecuteAction Action](executeaction-action.md).

La tabella InstallUISequence include le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Azione    | [Identificatore](identifier.md) | S   | N        |
| Condizione | [Condition](condition.md)   | N   | S        |
| Sequenza  | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Nome dell'azione da eseguire. Si tratta di un'azione predefinita, un'azione personalizzata o una procedura guidata dell'interfaccia utente.

Chiave della tabella primaria.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Questo campo contiene un'espressione condizionale. Se l'espressione restituisce false, l'azione viene ignorata. Se la sintassi dell'espressione non è valida, la sequenza termina, restituendo iesBadActionData. Per informazioni sulla sintassi delle istruzioni condizionali, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Il numero in questa colonna determina la posizione della sequenza in cui viene eseguita l'azione.

Un valore positivo rappresenta la posizione della sequenza. Un valore null indica che l'azione non viene mai eseguita. I seguenti valori negativi indicano che questa azione viene eseguita se il programma di installazione restituisce il flag di terminazione associato. Ogni flag di terminazione (valore negativo) può essere utilizzato senza più di un'azione. Più azioni possono avere flag di terminazione, ma devono essere flag diversi. I flag di terminazione (valori negativi) vengono in genere utilizzati con le [finestre di dialogo](dialog-boxes.md).



| Flag di terminazione          | Valore | Descrizione                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Operazione completata. Utilizzato con le finestre di dialogo di [uscita](exit-dialog.md) .               |
| msiDoActionStatusUserExit | -2    | L'utente termina l'installazione. Utilizzato con le finestre di dialogo [UserExit](userexit-dialog.md) .     |
| msiDoActionStatusFailure  | -3    | Terminazione irreversibile. Utilizzato con le finestre di dialogo [FatalError](fatalerror-dialog.md) . |
| msiDoActionStatusSuspend  | -4    | L'installazione è stata sospesa.                                                                |



 

Zero, tutti gli altri numeri negativi o un valore null indicano che l'azione non viene mai eseguita.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il testo localizzato associato per la visualizzazione o la registrazione dello stato di avanzamento è specificato nella [tabella ActionText](actiontext-table.md).

Per un esempio di una tabella di sequenza, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE20](ice20.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE46](ice46.md)  
[ICE75](ice75.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE86](ice86.md)  
</dl>

 

 



