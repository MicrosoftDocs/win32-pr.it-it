---
title: Evento DblClick
description: Evento DblClick
ms.assetid: 81ed5396-a2dc-49fe-820f-61ca0935fe85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48e5b4574f8378930001e1cea3916d12904fcc317b3b00ff14c436fb4912574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693775"
---
# <a name="dblclick-event"></a>Evento DblClick

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando l'utente fa doppio clic su un carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent*** \_ DblClick* *  **(ByVal** *CharacterID,* **ByVal** *Button,* **ByVal** *Shift,* **ByVal** *X,* **ByVal** *Y****)**



| Parte          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere su cui si è fatto doppio clic come stringa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| *Button*      | Restituisce un numero intero che identifica il pulsante premuto e rilasciato per causare l'evento. L'argomento button è un campo di bit con bit corrispondenti al pulsante sinistro (bit 0), al pulsante destro (bit 1) e al pulsante centrale (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. Viene impostato solo uno dei bit, che indica il pulsante che ha causato l'evento. Se il carattere include un'icona della barra delle applicazioni, se è impostato anche il bit 13, si è fatto clic sull'icona della barra delle applicazioni.                                                                                                                                                                       |
| *Maiusc*       | Restituisce un numero intero che corrisponde allo stato dei tasti MAIUSC, CTRL e ALT quando il pulsante specificato nell'argomento del pulsante viene premuto o rilasciato. Un bit viene impostato se la chiave non è disponibile. L'argomento shift è un campo di bit con i bit meno significativi corrispondenti al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. L'argomento shift indica lo stato di queste chiavi. Alcuni, tutti o nessuno dei bit possono essere impostati, a indicare che alcuni, tutti o nessuno dei tasti vengono premuti. Ad esempio, se si preme CTRL e ALT, il valore di MAIUSC sarà 6. |
| *X,Y*         | Restituisce un intero che specifica la posizione corrente del puntatore del mouse. I valori X e Y sono sempre espressi in pixel, rispetto all'angolo superiore sinistro dello schermo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento viene inviato solo al client attivo di input di un carattere. Quando l'utente fa doppio clic su un carattere o sull'icona della barra delle applicazioni senza client attivo per l'input, il server invia l'evento all'ultimo client attivo per l'input. Se il carattere è visibile [(Visible](visible-property.md)True), imposta anche il client attivo come client attivo di input corrente, inviando l'evento ActivateInput a tale client e quindi inviando l'evento  =   **DblClick.** [](activateinput-event.md) Se il carattere è nascosto (Visible = **False)** e l'utente fa doppio clic sull'icona della barra delle applicazioni del carattere usando il pulsante 1, visualizza automaticamente anche il carattere.

 

 




