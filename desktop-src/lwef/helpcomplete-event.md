---
title: Evento HelpComplete
description: Evento HelpComplete
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3984f4b67eaed6bc9226685e927c35e151c11e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299705"
---
# <a name="helpcomplete-event"></a>Evento HelpComplete

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Indica che la modalità della Guida sensibile al contesto è stata chiusa.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

Agente **secondario** *. * * * (ByVal* *  *CharacterID * * *, ByVal* *  *Name * * *, ByVal* *  *causare * * *)**



| Parte          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere selezionato sotto forma di stringa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *Nome*        | Restituisce un valore stringa che identifica il nome (ID) del comando.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| *Causa*       | Restituisce un valore che indica la causa del completamento della modalità della guida. 1 l'utente ha selezionato un comando fornito dall'applicazione.<br/> 2 l'utente ha selezionato l'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) di un altro client.<br/> 3 l'utente ha selezionato il comando Open Voice Commands.<br/> 4 l'utente ha selezionato il comando Chiudi voce comandi.<br/> 5 l'utente ha selezionato il comando Mostra *caratteriname* .<br/> 6 l'utente ha selezionato il comando Nascondi *caratterename* .<br/> 7 l'utente ha selezionato (selezionato) il carattere.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

In genere, la modalità della guida viene completata quando l'utente fa clic o trascina il carattere o seleziona un comando dal menu di scelta rapida del carattere. Se si fa clic su un altro carattere o altrove sullo schermo, la modalità della guida non viene annullata. Il client che imposta la modalità della Guida per il carattere può annullare la modalità della Guida impostando [**HelpModeOn**](helpmodeon-property.md) su **false**. (L'evento **HelpComplete** non viene attivato).

Quando l'utente seleziona un comando dal menu popup del carattere in modalità guida, il server rimuove il menu, chiama la guida con il [**HelpContextID**](helpcontextid-property.md)specificato del comando e invia questo evento. L'oggetto sensibile al contesto (noto anche come?) La finestra della guida viene visualizzata nella posizione del puntatore. Se l'utente seleziona il comando in base all'input vocale, la finestra della guida viene visualizzata sopra il carattere. Se il carattere è esterno allo schermo, la finestra viene visualizzata sullo schermo più vicino alla posizione corrente del carattere.

Se il server restituisce un nome come stringa vuota (""), indica che l'utente ha selezionato un comando fornito dal server.

Questo evento viene inviato solo all'applicazione client che inserisce il carattere in modalità guida.

### <a name="see-also"></a>Vedere anche

[**Proprietà HelpModeOn**](helpmodeon-property.md), [ **proprietà HelpContextID**](helpcontextid-property.md)


 

