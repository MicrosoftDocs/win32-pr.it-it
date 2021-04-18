---
title: Evento Click
description: Evento Click
ms.assetid: 772029d5-97b6-49d8-a989-04f0fc429aca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3956d19e833a3e0a5f71192b2846ef9cb270ad10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396526"
---
# <a name="click-event"></a>Evento Click

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando l'utente fa clic su un carattere o sull'icona del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *Agent * * * \_ fare clic su* *  **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y * * *)**



| Parte          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere selezionato sotto forma di stringa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Button*      | Restituisce un intero che identifica il pulsante che è stato premuto e rilasciato per generare l'evento. L'argomento del pulsante è un bit con bit corrispondente al pulsante sinistro (bit 0), pulsante destro (bit 1) e pulsante centrale (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. Viene impostato solo uno dei bit, che indica il pulsante che ha causato l'evento. Se il carattere include un'icona della barra delle applicazioni e viene impostato anche il bit 13, il clic si è verificato sull'icona della barra delle applicazioni.                                                                                                                                                                      |
| *MAIUSC*       | Restituisce un intero che corrisponde allo stato dei tasti MAIUSC, CTRL e ALT quando il pulsante specificato nell'argomento del pulsante viene premuto o rilasciato. Se la chiave è inattiva, viene impostato un bit. L'argomento Shift è un bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), il tasto CTRL (bit 1) e il tasto ALT (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. L'argomento Shift indica lo stato di queste chiavi. È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti. Se, ad esempio, sono stati premuti sia CTRL che ALT, il valore di Shift sarà 6. |
| *X, Y*         | Restituisce un Integer che specifica la posizione corrente del puntatore del mouse. I valori X e Y sono sempre espressi in pixel, in relazione all'angolo superiore sinistro dello schermo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento viene inviato solo al client attivo di input di un carattere. Quando l'utente fa clic su un carattere o sull'icona della barra delle applicazioni senza client attivo di input, il server invia l'evento al client attivo. Se il carattere è visibile ([**visibile**](visible-property.md)  =  **true**), l'azione dell'utente imposta anche l'ultimo client attivo di input del carattere come il client di input attivo corrente, inviando l'evento [**ActivateInput**](activateinput-event.md) al client e quindi inviando l'evento **Click** . Se il carattere è nascosto (**visibile**  =  **false**) e l'utente fa clic sull'icona della barra delle applicazioni del carattere usando il pulsante 1, viene visualizzato automaticamente anche il carattere.

> [!Note]  
> Se si fa clic su un carattere, non viene disabilitato l'output di tutti gli altri caratteri. Tuttavia, premendo il tasto ascolto viene scaricato l'output del carattere attivo input e viene attivato l'evento [**RequestComplete**](requestcomplete-event.md) , passando una [richiesta. status](status-property.md) che indica che la coda del client è stata interrotta.

 

 

 




