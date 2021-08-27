---
description: La tabella ControlCondition consente a un autore di specificare azioni speciali da applicare ai controlli in base al risultato di un'istruzione condizionale. Ad esempio, usando questa tabella, l'autore può scegliere di nascondere un controllo basato sulla proprietà VersionNT.
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: Tabella ControlCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637d9470af21ad1f8a15c2697ba34a6c9866c822c21c6f3a85241bac1309f76b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105251"
---
# <a name="controlcondition-table"></a>Tabella ControlCondition

La tabella ControlCondition consente a un autore di specificare azioni speciali da applicare ai controlli in base al risultato di un'istruzione condizionale. Ad esempio, usando questa tabella, l'autore può scegliere di nascondere un controllo basato sulla [**proprietà VersionNT.**](versionnt.md)

La tabella ControlCondition include le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Finestra di dialogo\_  | [Identificatore](identifier.md) | S   | N        |
| controllo\_ | [Identificatore](identifier.md) | S   | N        |
| Azione    | [Text](text.md)             | S   | N        |
| Condition | [Condition](condition.md)   | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogo\_
</dt> <dd>

Chiave esterna alla prima colonna della tabella [Dialog](dialog-table.md). La combinazione di questo campo con il \_ campo Controllo identifica un controllo univoco.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controllo\_
</dt> <dd>

Chiave esterna alla seconda colonna della tabella [Control](control-table.md). Combinando questo campo, il campo \_ Dialog identifica un controllo univoco.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Azione da eseguire sul controllo. Le azioni possibili sono illustrate nella tabella seguente.



| Valore   | Significato                     |
|---------|-----------------------------|
| Predefinito | Impostare il controllo come predefinito. |
| Disabilita | Disabilitare il controllo.        |
| Abilita  | Abilitare il controllo .         |
| Nascondi    | Nascondere il controllo.           |
| Mostra    | Visualizzare il controllo .        |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Istruzione condizionale che specifica in quali condizioni deve essere attivata l'azione. Questa colonna non può essere lasciata vuota. Se questa istruzione non restituisce TRUE, l'azione non viene eseguita. Se è impostato su 1, l'azione viene sempre applicata. Per informazioni sulla sintassi delle istruzioni condizionali, vedere [Sintassi delle istruzioni condizionali.](conditional-statement-syntax.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Se vuoi nascondere e disabilitare un controllo [PushButton](pushbutton-control.md) o [CheckBox](checkbox-control.md) in base a un'istruzione condizionale nel campo Condizione della tabella ControlCondition, devi usare quattro record per ogni controllo per disabilitare e nascondere il controllo. I tasti di scelta rapida possono comunque accedere ai controlli PushButton o CheckBox che sono stati nascosti.

Ad esempio, i record seguenti nascondono e disabilitano ControlA nella finestra di dialogoA quando il prodotto è installato. Il controllo sarà visibile e abilitato quando il prodotto non è installato.



| Finestra di dialogo  | Control  | Azione  | Condition                      |
|---------|----------|---------|--------------------------------|
| Finestra di dialogo | Controllo A | Nascondi    | [**Installato**](installed.md) |
| Finestra di dialogo | Controllo A | Disabilita | Installato                      |
| Finestra di dialogo | Controllo A | Mostra    | NON installato                  |
| Finestra di dialogo | Controllo A | Abilita  | NON installato                  |



 

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

 

 



