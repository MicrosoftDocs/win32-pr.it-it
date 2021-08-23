---
title: Evento DragComplete
description: Evento DragComplete
ms.assetid: b48e7097-9d9d-4eab-9dfc-68dbc9793382
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df5ec931a8d5f303dbc1eff5c2f97c018486c4b2fa7326de3e70fbf47a949aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976671"
---
# <a name="dragcomplete-event"></a>Evento DragComplete

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando l'utente completa il trascinamento di un carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent*** \_ DragComplete* *  **(ByVal** *CharacterID,* **ByVal** Button , **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y***)* *



| Parte          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere trascinato come stringa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Button*      | Restituisce un intero che identifica il pulsante che è stato premuto e rilasciato per generare l'evento. L'argomento button è un campo di bit con bit corrispondenti al pulsante sinistro (bit 0), al pulsante destro (bit 1) e al pulsante centrale (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. Viene impostato solo uno dei bit , che indica il pulsante che ha causato l'evento.                                                                                                                                                                                                                                                                                |
| *Maiusc*       | Restituisce un intero che corrisponde allo stato dei tasti MAIUSC, CTRL e ALT quando il pulsante specificato nell'argomento del pulsante viene premuto o rilasciato. Se la chiave non è disponibile, viene impostato un bit . L'argomento shift è un campo di bit con i bit meno significativi corrispondenti al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. L'argomento shift indica lo stato di queste chiavi. È possibile impostare alcuni, tutti o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti. Ad esempio, se vengono premuti sia CTRL che ALT, il valore di MAIUSC sarà 6. |
| *X,Y*         | Restituisce un intero che specifica la posizione corrente del puntatore del mouse. I valori X e Y sono sempre espressi in pixel, rispetto all'angolo superiore sinistro dello schermo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento viene inviato solo al client attivo di input di un carattere. Quando l'utente trascina un carattere senza client attivo per l'input, il server imposta l'ultimo client di input attivo come client attivo per l'input corrente, inviando l'evento [**ActivateInput**](activateinput-event.md) a tale client e quindi inviando gli eventi [**DragStart**](dragstart-event.md) **e DragComplete.**

### <a name="see-also"></a>Vedere anche

[**Evento DragStart**](dragstart-event.md)


 

 




