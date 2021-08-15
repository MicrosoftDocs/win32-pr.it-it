---
description: La tabella AdminUISequence elenca le azioni che il programma di installazione chiama in sequenza quando viene eseguita l'azione ADMIN di primo livello e il livello dell'interfaccia utente interna è impostato su interfaccia utente completa o interfaccia utente ridotta.
ms.assetid: 7227846d-b755-4af9-acc3-e27742a5097a
title: Tabella AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12feb7080d6d97ee86456bee694cdad57eee9873c9c7f64aecf0f4bd05817cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381699"
---
# <a name="adminuisequence-table"></a>Tabella AdminUISequence

La tabella AdminUISequence elenca le azioni che il programma di installazione chiama in sequenza quando viene eseguita l'azione [ADMIN](admin-action.md) di primo livello e il livello dell'interfaccia utente interna è impostato su interfaccia utente completa o interfaccia utente ridotta. Il programma di installazione ignora le azioni in questa tabella se il livello dell'interfaccia utente è impostato sull'interfaccia utente di base o nessuna interfaccia utente. Vedere [Informazioni sul Interfaccia utente](about-the-user-interface.md).

Le azioni ADMIN nella sequenza di installazione fino all'azione [InstallValidate](installvalidate-action.md)e alle finestre di dialogo di uscita si trovano nella tabella AdminUISequence. Tutte le azioni da InstallValidate fino alla fine della sequenza di installazione sono nella [tabella AdminExecuteSequence](adminexecutesequence-table.md). Poiché la tabella AdminExecuteSequence deve essere autonoma, contiene anche tutte le azioni di inizializzazione necessarie, ad esempio [LaunchConditions,](launchconditions-action.md) [CostInitialize,](costinitialize-action.md) [FileCost](filecost-action.md)e [CostFinalize.](costfinalize-action.md) Include anche [l'azione ExecuteAction](executeaction-action.md).

Le colonne sono identiche a quelle della [tabella InstallUISequence](installuisequence-table.md). La tabella AdminUISequence contiene le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Azione    | [Identificatore](identifier.md) | S   | N        |
| Condition | [Condition](condition.md)   | N   | S        |
| Sequenza  | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Nome dell'azione da eseguire. Si tratta di un'azione standard, di una procedura guidata dell'interfaccia utente o di un'azione personalizzata elencata nella [tabella CustomAction](customaction-table.md).

Chiave della tabella primaria.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Espressione logica. Se l'espressione restituisce false, l'azione viene ignorata. Se la sintassi dell'espressione non è valida, la sequenza termina e restituisce iesBadActionData. Per informazioni sulla sintassi delle istruzioni condizionali, vedere [Sintassi delle istruzioni condizionali.](conditional-statement-syntax.md)

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Un valore positivo indica la posizione della sequenza dell'azione. I valori negativi seguenti indicano che l'azione viene chiamata se il programma di installazione restituisce il flag di terminazione. Ogni flag di terminazione (valore negativo) può essere usato senza più di un'azione. Più azioni possono avere flag di terminazione, ma devono essere flag diversi. I flag di terminazione (valori negativi) vengono in genere usati con [le finestre di dialogo](dialog-boxes.md).



| Flag di terminazione          | Valore | Descrizione                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Completamento. Utilizzato con [le finestre di](exit-dialog.md) dialogo Di uscita.               |
| msiDoActionStatusUserExit | -2    | L'utente termina l'installazione. Usato con [le finestre di dialogo UserExit.](userexit-dialog.md)     |
| msiDoActionStatusFailure  | -3    | Termina l'uscita irreversibile. Utilizzato con una finestra [di dialogo FatalError.](fatalerror-dialog.md) |
| msiDoActionStatusSuspend  | -4    | L'installazione è sospesa.                                                                |



 

Zero, tutti gli altri numeri negativi o un valore Null indicano che l'azione non viene mai chiamata.

</dd> </dl>

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
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICE96](ice96.md)  
[ICEM04](icem04.md)  
</dl>

 

 



