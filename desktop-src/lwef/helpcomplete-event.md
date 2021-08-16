---
title: Evento HelpComplete
description: Evento HelpComplete
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a41b4dc0b1b6767b113220f2a922d1a512132a2cd7754891acb9c99b92d0039
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478996"
---
# <a name="helpcomplete-event"></a>Evento HelpComplete

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Indica che la modalità della Guida sensibile al contesto è stata chiusa.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent.***(ByVal* *  *CharacterID***, ByVal* *  *Name***, ByVal* *  *Cause***)**



| Parte          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere su cui è stato fatto clic come stringa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *Nome*        | Restituisce un valore stringa che identifica il nome (ID) del comando.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| *Causa*       | Restituisce un valore che indica la causa del completamento della modalità Guida. 1 L'utente ha selezionato un comando fornito dall'applicazione.<br/> 2 L'utente ha selezionato [**l'oggetto Commands**](/windows/desktop/lwef/the-commands-collection-object) di un altro client.<br/> 3 L'utente ha selezionato il comando Apri comandi vocali.<br/> 4 L'utente ha selezionato il comando Chiudi comandi vocali.<br/> 5 L'utente ha selezionato il comando *Show CharacterName.*<br/> 6 L'utente ha selezionato il *comando Nascondi CharacterName.*<br/> 7 L'utente ha selezionato (selezionato) il carattere.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

In genere, la modalità Guida viene completata quando l'utente fa clic o trascina il carattere o seleziona un comando dal menu a comparsa del carattere. Facendo clic su un altro carattere o altrove sullo schermo non viene annullata la modalità Guida. Il client che imposta la modalità Guida per il carattere può annullare la modalità Guida impostando [**HelpModeOn**](helpmodeon-property.md) su **False.** Questa operazione non attiva **l'evento HelpComplete.**

Quando l'utente seleziona un comando dal menu a comparsa del carattere in modalità Guida, il server rimuove il menu, chiama la Guida con il [**valore HelpContextID**](helpcontextid-property.md)specificato dal comando e invia questo evento. Sensibile al contesto (noto anche come What's This?) La finestra della Guida viene visualizzata nella posizione del puntatore. Se l'utente seleziona il comando tramite input vocale, viene visualizzata la finestra della Guida sul carattere. Se il carattere è fuori schermo, la finestra viene visualizzata sullo schermo più vicina alla posizione corrente del carattere.

Se il server restituisce Name come stringa vuota (""), indica che l'utente ha selezionato un comando fornito dal server.

Questo evento viene inviato solo all'applicazione client che imposta il carattere in modalità Guida.

### <a name="see-also"></a>Vedere anche

[**Proprietà HelpModeOn**](helpmodeon-property.md), [ **proprietà HelpContextID**](helpcontextid-property.md)


 

