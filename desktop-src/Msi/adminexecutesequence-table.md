---
description: La tabella AdminExecuteSequence elenca le azioni che il programma di installazione chiama in sequenza quando viene eseguita l'azione di amministrazione di primo livello.
ms.assetid: 33a2ef50-519b-424e-b510-55c21c5706a3
title: Tabella AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c62ae43f8436ab210765e5402751c5722b78b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311071"
---
# <a name="adminexecutesequence-table"></a>Tabella AdminExecuteSequence

La tabella AdminExecuteSequence elenca le azioni che il programma di installazione chiama in sequenza quando viene eseguita l' [azione di amministrazione](admin-action.md) di primo livello.

Le azioni amministrative nella sequenza di installazione, fino all' [azione InstallValidate](installvalidate-action.md) e alle finestre di dialogo di uscita, si trovano nella [tabella AdminUISequence](adminuisequence-table.md).

Le azioni amministrative dall'azione InstallValidate fino alla fine della sequenza di installazione si trovano nella tabella AdminExecuteSequence. Poiché la tabella AdminExecuteSequence deve essere autonoma, contiene anche tutte le azioni di inizializzazione necessarie, ad esempio [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [filecost](filecost-action.md)e [CostFinalize secondo](costfinalize-action.md).

Le [azioni personalizzate](custom-actions.md) che richiedono un'interfaccia utente devono usare [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) anziché le finestre di dialogo Create con la [tabella della finestra di dialogo](dialog-table.md).

Le colonne sono identiche a quelle della [tabella InstallExecuteSequence](installexecutesequence-table.md). La tabella AdminExecuteSequence include le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Azione    | [Identificatore](identifier.md) | S   | N        |
| Condizione | [Condition](condition.md)   | N   | S        |
| Sequenza  | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Nome dell'azione da eseguire. Si tratta di un'azione standard o di un'azione personalizzata elencata nella [tabella CustomAction](customaction-table.md).

Chiave della tabella primaria.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Espressione logica. Se l'espressione restituisce false, l'azione viene ignorata. Se la sintassi dell'espressione non è valida, la sequenza termina, restituendo iesBadActionData. Per informazioni sulla sintassi delle istruzioni condizionali, vedere Sintassi delle istruzioni [condizionali](conditional-statement-syntax.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Un valore positivo indica la posizione della sequenza dell'azione. I valori negativi seguenti indicano che l'azione viene chiamata se il programma di installazione restituisce il flag di terminazione. Ogni flag di terminazione (valore negativo) può essere utilizzato senza più di un'azione. Più azioni possono avere flag di terminazione, ma devono essere flag diversi. I flag di terminazione (valori negativi) vengono in genere utilizzati con le [finestre di dialogo](dialog-boxes.md).



| Flag di terminazione          | Valore | Descrizione                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Operazione completata. Utilizzato con le finestre di dialogo di [uscita](exit-dialog.md) .               |
| msiDoActionStatusUserExit | -2    | L'utente termina l'installazione. Utilizzato con le finestre di dialogo [UserExit](userexit-dialog.md) .     |
| msiDoActionStatusFailure  | -3    | Terminazione irreversibile. Utilizzato con le finestre di dialogo [FatalError](fatalerror-dialog.md) . |
| msiDoActionStatusSuspend  | -4    | L'installazione è stata sospesa.                                                                |



 

Zero, tutti gli altri numeri negativi o un valore null indicano che l'azione non viene mai chiamata.

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICEM04](icem04.md)  
</dl>

 

 



