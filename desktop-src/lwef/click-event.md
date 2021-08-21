---
title: Evento Click
description: Evento Click
ms.assetid: 772029d5-97b6-49d8-a989-04f0fc429aca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc10726c91612a6d43c4b7f8ceb0509fc347904f1328c9b99a3ec05d8e2eb0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480187"
---
# <a name="click-event"></a>Evento Click

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando l'utente fa clic su un carattere o sull'icona del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent*** \_ Click* *  **(ByVal** *CharacterID,* **ByVal** Button , **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y***)* *



| Parte          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere su cui è stato fatto clic come stringa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Button*      | Restituisce un intero che identifica il pulsante che è stato premuto e rilasciato per generare l'evento. L'argomento button è un campo di bit con bit corrispondenti al pulsante sinistro (bit 0), al pulsante destro (bit 1) e al pulsante centrale (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. Viene impostato solo uno dei bit , che indica il pulsante che ha causato l'evento. Se il carattere include un'icona della barra delle applicazioni ed è impostato anche il bit 13, il clic si è verificato sull'icona della barra delle applicazioni.                                                                                                                                                                      |
| *Maiusc*       | Restituisce un intero che corrisponde allo stato dei tasti MAIUSC, CTRL e ALT quando il pulsante specificato nell'argomento del pulsante viene premuto o rilasciato. Se la chiave non è disponibile, viene impostato un bit . L'argomento shift è un campo di bit con i bit meno significativi corrispondenti al tasto MAIUSC (bit 0), al tasto CTRL (bit 1) e al tasto ALT (bit 2). Questi bit corrispondono rispettivamente ai valori 1, 2 e 4. L'argomento shift indica lo stato di queste chiavi. È possibile impostare alcuni, tutti o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti. Ad esempio, se vengono premuti sia CTRL che ALT, il valore di MAIUSC sarà 6. |
| *X,Y*         | Restituisce un intero che specifica la posizione corrente del puntatore del mouse. I valori X e Y sono sempre espressi in pixel, rispetto all'angolo superiore sinistro dello schermo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento viene inviato solo al client attivo di input di un carattere. Quando l'utente fa clic su un carattere o sull'icona della barra delle applicazioni senza client attivo per l'input, il server invia l'evento al client attivo. Se il carattere è visibile [**(Visible**](visible-property.md)  =  **True),** l'azione dell'utente imposta anche l'ultimo client attivo di input del carattere come client attivo di input corrente, inviando l'evento [**ActivateInput**](activateinput-event.md) a tale client e quindi inviando l'evento **Click.** Se il carattere è nascosto **(Visible** False) e l'utente fa clic sull'icona della barra delle applicazioni del carattere usando il pulsante 1, viene visualizzato  =  automaticamente anche il carattere.

> [!Note]  
> Facendo clic su un carattere non vengono disabilitati tutti gli altri caratteri (tutti i caratteri). Tuttavia, premendo il tasto Listening viene scaricato l'output del carattere attivo di input e viene attivato l'evento [**RequestComplete,**](requestcomplete-event.md) passando un oggetto [Request.Status](status-property.md) che indica che la coda del client è stata interrotta.

 

 

 




