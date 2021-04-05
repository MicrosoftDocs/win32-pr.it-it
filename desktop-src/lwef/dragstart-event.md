---
title: Evento DragStart
description: Evento DragStart
ms.assetid: fef0ae05-1958-45c6-8260-107c47b5fa92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e382e77c87848226568755c06d2541ebb4db14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044691"
---
# <a name="dragstart-event"></a>Evento DragStart

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando l'utente inizia a trascinare un carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

 *Agente secondario * * * \_ DragStart* *  **(ByVal** *CharacterID*, **(** *pulsante* ByVal, **(ByVal** *Shift*, **(** ByVal *X*, **(ByVal** *Y * * *)**



| Parte          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere selezionato sotto forma di stringa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Button*      | Restituisce un intero che identifica il pulsante che è stato premuto e rilasciato per generare l'evento. L'argomento del pulsante è un bit con bit corrispondente al pulsante sinistro (bit 0), pulsante destro (bit 1) e pulsante centrale (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. Viene impostato solo uno dei bit, che indica il pulsante che ha causato l'evento.                                                                                                                                                                                                                                                                                |
| *MAIUSC*       | Restituisce un intero che corrisponde allo stato dei tasti MAIUSC, CTRL e ALT quando il pulsante specificato nell'argomento del pulsante viene premuto o rilasciato. Se la chiave è inattiva, viene impostato un bit. L'argomento Shift è un bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), il tasto CTRL (bit 1) e il tasto ALT (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. L'argomento Shift indica lo stato di queste chiavi. È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti. Se, ad esempio, sono stati premuti sia CTRL che ALT, il valore di Shift sarà 6. |
| *X, Y*         | Restituisce un Integer che specifica la posizione corrente del puntatore del mouse. I valori X e Y sono sempre espressi in pixel, in relazione all'angolo superiore sinistro dello schermo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento viene inviato solo al client attivo di input di un carattere. Quando l'utente trascina un carattere senza client attivo di input, il server imposta l'ultimo client attivo di input come il client attivo di input corrente, inviando l'evento [**ActivateInput**](activateinput-event.md) al client e quindi inviando l'evento **DragStart** .

### <a name="see-also"></a>Vedere anche

[**Evento DragComplete**](dragcomplete-event.md)


 

 




