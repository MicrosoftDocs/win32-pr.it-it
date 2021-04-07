---
description: Nella tabella AdvtExecuteSequence sono elencate le azioni che il programma di installazione chiama quando viene eseguita l'azione di annuncio di primo livello.
ms.assetid: 8873c161-a709-48b8-a66f-fe2ee9be859f
title: Tabella AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b68a3f69cc7473b2364f169545743941d752f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881149"
---
# <a name="advtexecutesequence-table"></a>Tabella AdvtExecuteSequence

Nella tabella AdvtExecuteSequence sono elencate le azioni che il programma di installazione chiama quando viene eseguita l' [azione di annuncio](advertise-action.md) di primo livello.

Nella tabella AdvtExecuteSequence è possibile utilizzare solo le azioni seguenti. Non è possibile usare azioni personalizzate in questa tabella.

[CostFinalize secondo](costfinalize-action.md)

[CostInitialize](costinitialize-action.md)

[CreateShortcuts](createshortcuts-action.md)

[InstallFinalize](installfinalize-action.md)

[InstallInitialize](installinitialize-action.md)

[InstallValidate](installvalidate-action.md)

[MsiPublishAssemblies](msipublishassemblies-action.md)

[PublishComponents](publishcomponents-action.md)

[PublishFeatures](publishfeatures-action.md)

[PublishProduct](publishproduct-action.md)

[RegisterClassInfo](registerclassinfo-action.md)

[RegisterExtensionInfo](registerextensioninfo-action.md)

[RegisterMIMEInfo](registermimeinfo-action.md)

[RegisterProgIdInfo](registerprogidinfo-action.md)

Le colonne sono identiche a quelle della [tabella InstallExecuteSequence](installexecutesequence-table.md). La tabella AdvtExecuteSequence include le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Azione    | [Identificatore](identifier.md) | S   | N        |
| Condizione | [Condition](condition.md)   | N   | S        |
| Sequenza  | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Nome dell' [azione standard](standard-actions.md) che deve essere eseguita dal programma di installazione. Si tratta della chiave primaria della tabella.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Espressione logica. Se l'espressione restituisce false, l'azione viene ignorata. Se la sintassi dell'espressione non è valida, la sequenza termina, restituendo iesBadActionData. Per informazioni sulla sintassi delle istruzioni condizionali, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).

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
[ICE27](ice27.md)  
[ICE46](ice46.md)  
[ICE72](ice72.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE83](ice83.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICEM04](icem04.md)  
</dl>

 

 



