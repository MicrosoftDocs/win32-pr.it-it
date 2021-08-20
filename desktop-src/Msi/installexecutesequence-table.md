---
description: La tabella InstallExecuteSequence elenca le azioni eseguite quando viene eseguita l'azione INSTALL di primo livello.
ms.assetid: 995d4159-bfc9-48b2-8328-3ae8251d785d
title: Tabella InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d48fb83bd8f3c947feb81ab95df490572ba1ee68d423957759a95c323005070
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142167"
---
# <a name="installexecutesequence-table"></a>Tabella InstallExecuteSequence

La tabella InstallExecuteSequence elenca le azioni eseguite quando viene eseguita [l'azione INSTALL](install-action.md) di primo livello.

Le azioni nella sequenza di installazione fino all'azione [InstallValidate](installvalidate-action.md)e alle finestre di dialogo di uscita si trovano nella [tabella InstallUISequence](installuisequence-table.md). Tutte le azioni da InstallValidate fino alla fine della sequenza di installazione sono nella tabella InstallExecuteSequence. Poiché la tabella InstallExecuteSequence deve essere autonoma, include tutte le azioni di inizializzazione necessarie, ad esempio [LaunchConditions,](launchconditions-action.md) [CostInitialize,](costinitialize-action.md) [FileCost](filecost-action.md)e [CostFinalize.](costfinalize-action.md)

[Le azioni personalizzate](custom-actions.md) che richiedono un'interfaccia utente devono [**usare MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) anziché le finestre di dialogo create usando la [tabella Dialog](dialog-table.md).

La tabella InstallExecuteSequence contiene le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Azione    | [Identificatore](identifier.md) | S   | N        |
| Condition | [Condition](condition.md)   | N   | S        |
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

Questo campo contiene un'espressione condizionale. Se l'espressione restituisce False, l'azione viene ignorata. Se la sintassi dell'espressione non è valida, la sequenza termina e restituisce iesBadActionData. Per informazioni sulla sintassi delle istruzioni condizionali, vedere [Sintassi delle istruzioni condizionali.](conditional-statement-syntax.md)

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Numero che determina la posizione della sequenza in cui deve essere eseguita l'azione.

Un valore positivo rappresenta la posizione della sequenza. Un valore Null indica che l'azione non viene eseguita. I valori negativi seguenti indicano che questa azione deve essere eseguita se il programma di installazione restituisce il flag di terminazione associato. Ogni flag di terminazione (valore negativo) può essere usato senza più di un'azione. Più azioni possono avere flag di terminazione, ma devono essere flag diversi. I flag di terminazione (valori negativi) vengono in genere usati con [le finestre di dialogo](dialog-boxes.md).



| Flag di terminazione          | Valore | Descrizione                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Completamento. Utilizzato con [le finestre di](exit-dialog.md) dialogo Di uscita.               |
| msiDoActionStatusUserExit | -2    | L'utente termina l'installazione. Usato con [le finestre di dialogo UserExit.](userexit-dialog.md)     |
| msiDoActionStatusFailure  | -3    | Termina l'uscita irreversibile. Utilizzato con una finestra [di dialogo FatalError.](fatalerror-dialog.md) |
| msiDoActionStatusSuspend  | -4    | L'installazione è sospesa.                                                                |



 

Zero, tutti gli altri numeri negativi o un valore Null indicano che l'azione non viene mai eseguita.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il testo localizzato per la visualizzazione o la registrazione dello stato di avanzamento è specificato nella [tabella ActionText](actiontext-table.md).

Per un esempio di tabella di sequenza, vedere [Uso di una tabella di sequenza.](using-a-sequence-table.md)

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

 

 



