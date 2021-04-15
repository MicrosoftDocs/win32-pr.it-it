---
title: IAgentNotifySinkEx ListeningState
description: IAgentNotifySinkEx ListeningState
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee8f931030cbd68cd148fc57360d8b0ccf7624
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515829"
---
# <a name="iagentnotifysinkexlisteningstate"></a>IAgentNotifySinkEx::ListeningState

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

Notifica a un'applicazione client quando viene modificata la modalità di ascolto.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*
</dt> <dd>

Carattere per il quale è stato modificato lo stato di ascolto.

</dd> <dt>

<span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*
</dt> <dd>

Stato della modalità di ascolto. **True** indica che la modalità di ascolto è stata avviata. **False**, la modalità di ascolto è terminata.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

Motivo dell'evento, che può corrispondere a uno dei valori seguenti.



| Valore                                                                             | Descrizione                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| **const unsigned long** **LSCOMPLETE \_ cause \_ PROGRAMDISABLED = 1;**<br/>    | La modalità di ascolto è stata disattivata dal codice del programma.                                 |
| **const unsigned long** **LSCOMPLETE \_ causare \_ PROGRAMTIMEDOUT = 2;**<br/>    | Timeout della modalità di ascolto (attivata dal codice del programma).                          |
| **const unsigned long** **LSCOMPLETE \_ causare \_ USERTIMEDOUT = 3;**<br/>       | Timeout della modalità di ascolto (attivata dal tasto di attesa).                     |
| **const unsigned long** **LSCOMPLETE \_ causare \_ USERRELEASEDKEY = 4;**<br/>    | La modalità di ascolto è stata disattivata perché l'utente ha rilasciato il tasto di attesa.     |
| **const unsigned long** **LSCOMPLETE \_ causare \_ USERUTTERANCEENDED = 5;**<br/> | La modalità di ascolto è stata disattivata perché l'utente ha terminato di parlare.              |
| **const unsigned long** **LSCOMPLETE \_ causare \_ CLIENTDEACTIVATED = 6;**<br/>  | La modalità di ascolto è stata disabilitata perché il client attivo di input è stato disattivato. |
| **const unsigned long** **LSCOMPLETE \_ cause \_ DEFAULTCHARCHANGE = 7**<br/>   | La modalità di ascolto è stata disattivata perché il carattere predefinito è stato modificato.       |
| **const unsigned long** **LSCOMPLETE \_ cause \_ USERDISABLED = 8**<br/>        | La modalità di ascolto è stata disattivata perché l'utente ha disabilitato l'input vocale.          |



 

</dd> </dl>

Questo evento viene inviato a tutti i client quando la modalità di ascolto viene avviata dopo che l'utente ha premuto il tasto ascolto o quando è terminato il timeout oppure quando il client di input-attivo chiama il metodo [**IAgentCharacterEx:: Listen**](iagentcharacterex--listen.md) con **true** o **false**.

L'evento restituisce i valori ai client attualmente caricati da questo carattere. Tutti gli altri client ricevono un carattere null (stringa vuota).

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx:: Listen**](iagentcharacterex--listen.md)


 

 





