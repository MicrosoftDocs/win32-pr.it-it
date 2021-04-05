---
description: La tabella ControlCondition consente a un autore di specificare azioni speciali da applicare ai controlli in base al risultato di un'istruzione condizionale. Se ad esempio si usa questa tabella, l'autore può scegliere di nascondere un controllo in base alla proprietà VersionNT.
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: Tabella ControlCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 671dcdee6e2ed1067c51a04084693c276b8db2d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967909"
---
# <a name="controlcondition-table"></a>Tabella ControlCondition

La tabella ControlCondition consente a un autore di specificare azioni speciali da applicare ai controlli in base al risultato di un'istruzione condizionale. Se ad esempio si usa questa tabella, l'autore può scegliere di nascondere un controllo in base alla proprietà [**VersionNT**](versionnt.md) .

La tabella ControlCondition include le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Finestra di dialogo\_  | [Identificatore](identifier.md) | S   | N        |
| controllo\_ | [Identificatore](identifier.md) | S   | N        |
| Azione    | [Text](text.md)             | S   | N        |
| Condizione | [Condition](condition.md)   | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogo\_
</dt> <dd>

Chiave esterna per la prima colonna della tabella della [finestra di dialogo](dialog-table.md). La combinazione di questo campo con il campo del controllo \_ identifica un controllo univoco.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controllo\_
</dt> <dd>

Chiave esterna per la seconda colonna della tabella dei [controlli](control-table.md). Combinando questo campo \_ , il campo finestra di dialogo identifica un controllo univoco.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Azione da intraprendere sul controllo. Le azioni possibili sono illustrate nella tabella seguente.



| Valore   | Significato                     |
|---------|-----------------------------|
| Predefinito | Impostare il controllo come predefinito. |
| Disabilita | Disabilitare il controllo.        |
| Abilitare  | Abilitare il controllo.         |
| Nascondi    | Nascondere il controllo.           |
| Mostra    | Visualizzare il controllo.        |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Istruzione condizionale che specifica le condizioni in base alle quali deve essere attivata l'azione. Questa colonna non può essere lasciata vuota. Se questa istruzione non restituisce TRUE, l'azione non viene eseguita. Se è impostato su 1, l'azione viene sempre applicata. Per informazioni sulla sintassi delle istruzioni condizionali, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si desidera nascondere e disabilitare un controllo [pulsante](pushbutton-control.md) o una [casella di controllo](checkbox-control.md) in base a un'istruzione condizionale nel campo condizione della tabella ControlCondition, è necessario utilizzare quattro record per ogni controllo per disabilitare e nascondere il controllo. È ancora possibile accedere ai controlli pulsante o CheckBox che sono rimasti nascosti solo tramite i tasti di scelta rapida.

Ad esempio, i record seguenti nascondono e disabilitano controla nella finestra di dialogo quando il prodotto è installato. Il controllo sarà visibile e attivato quando il prodotto non è installato.



| Finestra di dialogo  | Control  | Azione  | Condizione                      |
|---------|----------|---------|--------------------------------|
| Finestra di dialogo | ControlA | Nascondi    | [**Installato**](installed.md) |
| Finestra di dialogo | ControlA | Disabilita | Installato                      |
| Finestra di dialogo | ControlA | Mostra    | NON installato                  |
| Finestra di dialogo | ControlA | Abilitare  | NON installato                  |



 

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



