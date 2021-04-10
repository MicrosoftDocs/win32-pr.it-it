---
title: IAgentNotifySinkEx HelpComplete
description: IAgentNotifySinkEx HelpComplete
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3b7dbbdf272844242943d49ed86b303d220185
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046616"
---
# <a name="iagentnotifysinkexhelpcomplete"></a>IAgentNotifySinkEx::HelpComplete

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT HelpComplete(
   long dwCharID,     // character ID
   long dwCommandID,  // command ID
   long dwCause       // cause 
);
```

Notifica a un'applicazione client quando l'utente seleziona un comando o un carattere per completare la modalità della guida.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificatore del carattere per il quale è stata completata la modalità della guida.

</dd> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

Identificatore del comando selezionato dall'utente.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

La motivo dell'evento, che può corrispondere ai valori seguenti:



| Valore                                                                         | Descrizione                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| comando CSHELPCAUSE **short senza segno const** **\_ = 1;**<br/>             | L'utente ha selezionato un comando fornito dall'applicazione.                            |
| **const unsigned short** **CSHELPCAUSE \_ OTHERPROGRAM = 2;**<br/>        | L'utente ha selezionato l'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) di un altro client. |
| **const unsigned short** **CSHELPCAUSE \_ OPENCOMMANDSWINDOW = 3;**<br/>  | L'utente ha selezionato il comando Open Voice Commands.                                   |
| **const unsigned short** **CSHELPCAUSE \_ CLOSECOMMANDSWINDOW = 4;**<br/> | L'utente ha selezionato il comando Chiudi voce comandi.                                  |
| **const unsigned short** **CSHELPCAUSE \_ SHOWCHARACTER = 5;**<br/>       | L'utente ha selezionato il comando Mostra *caratteriname* .                                  |
| **const unsigned short** **CSHELPCAUSE \_ HIDECHARACTER = 6;**<br/>       | L'utente ha selezionato il comando Nascondi *caratterename* .                                  |
| carattere CSHELPCAUSE **short const senza segno** **\_ = 7;**<br/>           | L'utente ha selezionato (selezionato) il carattere.                                           |



 

</dd> </dl>

In genere, la modalità Guida viene completata quando l'utente fa clic o trascina il carattere o seleziona un comando dal menu a comparsa del carattere. Se si fa clic su un altro carattere o altrove sullo schermo, la modalità della guida non viene annullata. Il client che imposta la modalità della Guida per il carattere può annullare la modalità della Guida impostando [**IAgentCharacter:: HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) su **false**. Questa operazione non attiva l'evento **IAgentNotifySinkEx:: HelpComplete** .

Quando l'utente seleziona un comando dal menu popup del carattere in modalità guida, il server rimuove il menu, chiama la guida con il [**HelpContextID**](helpcontextid-property.md)specificato del comando e invia questo evento. L'oggetto sensibile al contesto (noto anche come?) La finestra della guida viene visualizzata nella posizione del puntatore. Se l'utente seleziona il comando in base all'input vocale, la finestra della guida viene visualizzata sopra il carattere. Se il carattere è esterno allo schermo, la finestra viene visualizzata sullo schermo più vicino alla posizione corrente del carattere.

Se il server restituisce *dwCommandID* come stringa vuota (""), significa che l'utente ha selezionato un comando fornito dal server.

Questo evento viene inviato solo all'applicazione client che inserisce il carattere in modalità guida.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx:: SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)


 

