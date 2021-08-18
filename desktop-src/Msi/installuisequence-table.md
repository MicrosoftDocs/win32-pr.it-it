---
description: La tabella InstallUISequence elenca le azioni eseguite quando viene eseguita l'azione INSTALL di primo livello e il livello dell'interfaccia utente interno è impostato su interfaccia utente completa o ridotta.
ms.assetid: 076d7c14-e302-4465-aed5-27a4b1f70ac8
title: Tabella InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2234ddcad587a495eceb79cc4511100f483bcfd96b388164f6e3c2d6a39eca3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013249"
---
# <a name="installuisequence-table"></a>Tabella InstallUISequence

La tabella InstallUISequence elenca le azioni eseguite quando viene eseguita l'azione [INSTALL](install-action.md) di primo livello e il livello dell'interfaccia utente interno è impostato su interfaccia utente completa o ridotta. Il programma di installazione ignora le azioni in questa tabella se il livello dell'interfaccia utente è impostato su Interfaccia utente di base o nessuna interfaccia utente. Vedere [Informazioni sull'Interfaccia utente](about-the-user-interface.md).

Le azioni nella sequenza di installazione fino all'azione [InstallValidate](installvalidate-action.md)e alle finestre di dialogo di uscita si trovano nella tabella InstallUISequence. Tutte le azioni da InstallValidate fino alla fine della sequenza di installazione sono nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Poiché la tabella InstallExecuteSequence deve essere autonoma, include tutte le azioni di inizializzazione necessarie, ad esempio [LaunchConditions,](launchconditions-action.md) [CostInitialize,](costinitialize-action.md) [FileCost](filecost-action.md)e [CostFinalize](costfinalize-action.md)e [ExecuteAction.](executeaction-action.md)

La tabella InstallUISequence include le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Azione    | [Identificatore](identifier.md) | S   | N        |
| Condition | [Condition](condition.md)   | N   | S        |
| Sequenza  | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Nome dell'azione da eseguire. Si tratta di un'azione predefinita, di un'azione personalizzata o di una procedura guidata dell'interfaccia utente.

Chiave della tabella primaria.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Questo campo contiene un'espressione condizionale. Se l'espressione restituisce False, l'azione viene ignorata. Se la sintassi dell'espressione non è valida, la sequenza termina, restituisce iesBadActionData. Per informazioni sulla sintassi delle istruzioni condizionali, vedere [Sintassi delle istruzioni condizionali](conditional-statement-syntax.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Il numero in questa colonna determina la posizione della sequenza in cui viene eseguita questa azione.

Un valore positivo rappresenta la posizione della sequenza. Un valore Null indica che l'azione non viene mai eseguita. I valori negativi seguenti indicano che questa azione viene eseguita se il programma di installazione restituisce il flag di terminazione associato. Ogni flag di terminazione (valore negativo) può essere usato senza più di un'azione. Più azioni possono avere flag di terminazione, ma devono essere flag diversi. I flag di terminazione (valori negativi) vengono in genere usati con [le finestre di dialogo](dialog-boxes.md).



| Flag di terminazione          | Valore | Descrizione                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Completamento. Usato con [le finestre di](exit-dialog.md) dialogo Esci.               |
| msiDoActionStatusUserExit | -2    | L'utente termina l'installazione. Usato con [le finestre di dialogo UserExit.](userexit-dialog.md)     |
| msiDoActionStatusFailure  | -3    | Termina l'uscita irreversibile. Utilizzato con le [finestre di dialogo FatalError.](fatalerror-dialog.md) |
| msiDoActionStatusSuspend  | -4    | L'installazione viene sospesa.                                                                |



 

Zero, tutti gli altri numeri negativi o un valore Null indicano che l'azione non viene mai eseguita.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il testo localizzato associato per la visualizzazione o la registrazione dello stato di avanzamento viene specificato nella [tabella ActionText](actiontext-table.md).

Per un esempio di tabella di sequenza, vedere [Uso di una tabella di sequenza](using-a-sequence-table.md).

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

 

 



