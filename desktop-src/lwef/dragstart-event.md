---
title: Evento DragStart
description: Evento DragStart
ms.assetid: fef0ae05-1958-45c6-8260-107c47b5fa92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 835ffc22e23643d306b361977a4bbe8b04e6481f8a577c3c2cef959b4be46ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963091"
---
# <a name="dragstart-event"></a>Evento DragStart

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando l'utente inizia a trascinare un carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent*** \_ DragStart* *  **(ByVal** *CharacterID*, **(ByVal** *Button*, **(ByVal** *Shift*, **(ByVal** *X*, **(ByVal** *Y****)**



| Parte          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere su cui si è fatto clic come stringa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Button*      | Restituisce un numero intero che identifica il pulsante premuto e rilasciato per causare l'evento. L'argomento button è un campo di bit con bit corrispondenti al pulsante sinistro (bit 0), al pulsante destro (bit 1) e al pulsante centrale (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. Viene impostato solo uno dei bit, che indica il pulsante che ha causato l'evento.                                                                                                                                                                                                                                                                                |
| *Maiusc*       | Restituisce un numero intero che corrisponde allo stato dei tasti MAIUSC, CTRL e ALT quando il pulsante specificato nell'argomento del pulsante viene premuto o rilasciato. Un bit viene impostato se la chiave non è disponibile. L'argomento shift è un campo di bit con i bit meno significativi corrispondenti al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. L'argomento shift indica lo stato di queste chiavi. Alcuni, tutti o nessuno dei bit possono essere impostati, a indicare che alcuni, tutti o nessuno dei tasti vengono premuti. Ad esempio, se si preme CTRL e ALT, il valore di MAIUSC sarà 6. |
| *X,Y*         | Restituisce un intero che specifica la posizione corrente del puntatore del mouse. I valori X e Y sono sempre espressi in pixel, rispetto all'angolo superiore sinistro dello schermo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento viene inviato solo al client attivo di input di un carattere. Quando l'utente trascina un carattere senza client attivo per l'input, il server imposta l'ultimo client attivo di input come client attivo per l'input corrente, inviando l'evento [**ActivateInput**](activateinput-event.md) a tale client e quindi inviando **l'evento DragStart.**

### <a name="see-also"></a>Vedere anche

[**Evento DragComplete**](dragcomplete-event.md)


 

 




