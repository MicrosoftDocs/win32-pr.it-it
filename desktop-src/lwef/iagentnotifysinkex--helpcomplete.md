---
title: IAgentNotifySinkEx HelpComplete
description: IAgentNotifySinkEx HelpComplete
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6ad0cc7212a7e7bedbcb968f9b9d2a658f520f1a3593595ff03091b03ba32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749563"
---
# <a name="iagentnotifysinkexhelpcomplete"></a>IAgentNotifySinkEx::HelpComplete

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT HelpComplete(
   long dwCharID,     // character ID
   long dwCommandID,  // command ID
   long dwCause       // cause 
);
```

Notifica a un'applicazione client quando l'utente seleziona un comando o un carattere per completare la modalità Guida.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificatore del carattere per il quale è stata completata la modalità Guida.

</dd> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

Identificatore del comando selezionato dall'utente.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

Causa dell'evento, che possono essere i valori seguenti:



| Valore                                                                         | Descrizione                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **CSHELPCAUSE \_ COMMAND = 1;**<br/>             | L'utente ha selezionato un comando fornito dall'applicazione.                            |
| **const unsigned short** **CSHELPCAUSE \_ OTHERPROGRAM = 2;**<br/>        | L'utente ha selezionato [**l'oggetto Commands**](/windows/desktop/lwef/the-commands-collection-object) di un altro client. |
| **const unsigned short** **CSHELPCAUSE \_ OPENCOMMANDSWINDOW = 3;**<br/>  | L'utente ha selezionato il comando Apri comandi vocali.                                   |
| **const unsigned short** **CSHELPCAUSE \_ CLOSECOMMANDSWINDOW = 4;**<br/> | L'utente ha selezionato il comando Chiudi comandi vocali.                                  |
| **const unsigned short** **CSHELPCAUSE \_ SHOWCHARACTER = 5;**<br/>       | L'utente ha selezionato il comando *Show CharacterName.*                                  |
| **const unsigned short** **CSHELPCAUSE \_ HIDECHARACTER = 6;**<br/>       | L'utente ha selezionato il comando *Nascondi CharacterName.*                                  |
| **const unsigned short** **CSHELPCAUSE \_ CHARACTER = 7;**<br/>           | L'utente ha selezionato (selezionato) il carattere.                                           |



 

</dd> </dl>

In genere la modalità Guida viene completata quando l'utente fa clic o trascina il carattere o seleziona un comando dal menu a comparsa del carattere. Facendo clic su un altro carattere o altrove sullo schermo non viene annullata la modalità Guida. Il client che imposta la modalità Guida per il carattere può annullare la modalità Guida impostando [**IAgentCharacter::HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) su **False**. Questa operazione non attiva l'evento **IAgentNotifySinkEx::HelpComplete.**

Quando l'utente seleziona un comando dal menu a comparsa del carattere in modalità Guida, il server rimuove il menu, chiama la Guida con [**helpContextID**](helpcontextid-property.md)specificato del comando e invia questo evento. Sensibile al contesto (noto anche come What's This?) La finestra della Guida viene visualizzata nella posizione del puntatore. Se l'utente seleziona il comando tramite input vocale, viene visualizzata la finestra della Guida sul carattere. Se il carattere è fuori schermo, la finestra viene visualizzata sullo schermo più vicina alla posizione corrente del carattere.

Se il server restituisce *dwCommandID* come stringa vuota (""), indica che l'utente ha selezionato un comando fornito dal server.

Questo evento viene inviato solo all'applicazione client che posiziona il carattere in modalità Guida.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx::SetHelpModeOn,**](iagentcharacterex--sethelpmodeon.md) [**IAgentCharacterEx::SetHelpFileName,**](iagentcharacterex--sethelpfilename.md) [**IAgentCharacterEx::SetHelpContextID,**](iagentcharacterex--sethelpcontextid.md) [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)


 

