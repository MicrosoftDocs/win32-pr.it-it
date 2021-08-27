---
description: La tabella AdminExecuteSequence elenca le azioni che il programma di installazione chiama in sequenza quando viene eseguita l'azione ADMIN di primo livello.
ms.assetid: 33a2ef50-519b-424e-b510-55c21c5706a3
title: Tabella AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eed182f5a27b357ecd546003cbfd7c68728d41c4018442b23bbf834ac8a796a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046001"
---
# <a name="adminexecutesequence-table"></a>Tabella AdminExecuteSequence

La tabella AdminExecuteSequence elenca le azioni che il programma di installazione chiama in sequenza quando viene eseguita l'azione [ADMIN](admin-action.md) di primo livello.

Le azioni ADMIN nella sequenza di installazione, fino all'azione [InstallValidate](installvalidate-action.md) e alle finestre di dialogo di uscita, si trovano nella [tabella AdminUISequence](adminuisequence-table.md).

Le azioni admin dall'azione InstallValidate fino alla fine della sequenza di installazione sono nella tabella AdminExecuteSequence. Poiché la tabella AdminExecuteSequence deve essere autonoma, contiene anche tutte le azioni di inizializzazione necessarie, ad esempio [LaunchConditions,](launchconditions-action.md) [CostInitialize,](costinitialize-action.md) [FileCost](filecost-action.md)e [CostFinalize.](costfinalize-action.md)

[Le azioni personalizzate](custom-actions.md) che richiedono un'interfaccia utente devono [**usare MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) anziché le finestre di dialogo create usando la [tabella Dialog](dialog-table.md).

Le colonne sono identiche a quelle della [tabella InstallExecuteSequence](installexecutesequence-table.md). La tabella AdminExecuteSequence contiene le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Azione    | [Identificatore](identifier.md) | S   | N        |
| Condition | [Condition](condition.md)   | N   | S        |
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

 

 



