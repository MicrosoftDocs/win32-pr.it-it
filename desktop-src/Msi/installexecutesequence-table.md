---
description: Nella tabella InstallExecuteSequence sono elencate le azioni che vengono eseguite quando viene eseguita l'azione di installazione di livello superiore.
ms.assetid: 995d4159-bfc9-48b2-8328-3ae8251d785d
title: Tabella InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d110debacab19739c3da69abf3948d11bb7aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878986"
---
# <a name="installexecutesequence-table"></a>Tabella InstallExecuteSequence

Nella tabella InstallExecuteSequence sono elencate le azioni che vengono eseguite quando viene eseguita l' [azione di installazione](install-action.md) di livello superiore.

Le azioni nella sequenza di installazione fino all' [azione InstallValidate](installvalidate-action.md)e a tutte le finestre di dialogo di uscita si trovano nella [tabella InstallUISequence](installuisequence-table.md). Tutte le azioni da InstallValidate fino alla fine della sequenza di installazione si trovano nella tabella InstallExecuteSequence. Poiché è necessario che la tabella InstallExecuteSequence sia autonoma, sono necessarie azioni di inizializzazione, ad esempio [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [filecost](filecost-action.md)e [CostFinalize secondo](costfinalize-action.md) .

Le [azioni personalizzate](custom-actions.md) che richiedono un'interfaccia utente devono usare [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) anziché le finestre di dialogo Create con la [tabella della finestra di dialogo](dialog-table.md).

La tabella InstallExecuteSequence include le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Azione    | [Identificatore](identifier.md) | S   | N        |
| Condizione | [Condition](condition.md)   | N   | S        |
| Sequenza  | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Nome dell'azione da eseguire. Si tratta di un'azione predefinita o di un'azione personalizzata.

Chiave della tabella primaria.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Questo campo contiene un'espressione condizionale. Se l'espressione restituisce false, l'azione viene ignorata. Se la sintassi dell'espressione non è valida, la sequenza termina, restituendo iesBadActionData. Per informazioni sulla sintassi delle istruzioni condizionali, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Numero che determina la posizione della sequenza in cui deve essere eseguita l'azione.

Un valore positivo rappresenta la posizione della sequenza. Un valore null indica che l'azione non viene eseguita. I seguenti valori negativi indicano che questa azione deve essere eseguita se il programma di installazione restituisce il flag di terminazione associato. Ogni flag di terminazione (valore negativo) può essere utilizzato senza più di un'azione. Più azioni possono avere flag di terminazione, ma devono essere flag diversi. I flag di terminazione (valori negativi) vengono in genere utilizzati con le [finestre di dialogo](dialog-boxes.md).



| Flag di terminazione          | Valore | Descrizione                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Operazione completata. Utilizzato con le finestre di dialogo di [uscita](exit-dialog.md) .               |
| msiDoActionStatusUserExit | -2    | L'utente termina l'installazione. Utilizzato con le finestre di dialogo [UserExit](userexit-dialog.md) .     |
| msiDoActionStatusFailure  | -3    | Terminazione irreversibile. Utilizzato con le finestre di dialogo [FatalError](fatalerror-dialog.md) . |
| msiDoActionStatusSuspend  | -4    | L'installazione è stata sospesa.                                                                |



 

Zero, tutti gli altri numeri negativi o un valore null indicano che l'azione non viene mai eseguita.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il testo localizzato per la visualizzazione o la registrazione dello stato di avanzamento è specificato nella [tabella ActionText](actiontext-table.md).

Per un esempio di una tabella di sequenza, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE46](ice46.md)  
[ICE63](ice63.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE83](ice83.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
</dl>

 

 



