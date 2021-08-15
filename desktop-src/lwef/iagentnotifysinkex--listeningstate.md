---
title: IAgentNotifySinkEx ListeningState
description: IAgentNotifySinkEx ListeningState
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21d3926741f83f66ab6133874ec47783976c0ddb6d3fbd2ee91c6e584813147a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692607"
---
# <a name="iagentnotifysinkexlisteningstate"></a>IAgentNotifySinkEx::ListeningState

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

Notifica a un'applicazione client quando cambia la modalità di ascolto.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*
</dt> <dd>

Carattere per il quale è stato modificato lo stato di ascolto.

</dd> <dt>

<span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bElenciazione*
</dt> <dd>

Stato della modalità di ascolto. **True** indica che la modalità di ascolto è stata avviata. **False**, che la modalità di ascolto è terminata.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

Causa dell'evento, che può essere uno dei valori seguenti.



| Valore                                                                             | Descrizione                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ PROGRAMDISABLED = 1;**<br/>    | La modalità di ascolto è stata disattivata dal codice programma.                                 |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ PROGRAMTIMEDOUT = 2;**<br/>    | Timeout della modalità di ascolto (attivata dal codice programma).                          |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERTIMEDOUT = 3;**<br/>       | Timeout della modalità di ascolto (attivata dalla chiave di ascolto).                     |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERRELEASEDKEY = 4;**<br/>    | La modalità di ascolto è stata disattivata perché l'utente ha rilasciato il tasto di ascolto.     |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERUTTERANCEENDED = 5;**<br/> | La modalità di ascolto è stata disattivata perché l'utente ha terminato di parlare.              |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ CLIENTDEACTIVATED = 6;**<br/>  | La modalità di ascolto è stata disattivata perché il client attivo di input è stato disattivato. |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ DEFAULTCHARCHANGE = 7**<br/>   | La modalità di ascolto è stata disattivata perché il carattere predefinito è stato modificato.       |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERDISABLED = 8**<br/>        | La modalità di ascolto è stata disattivata perché l'utente ha disabilitato l'input vocale.          |



 

</dd> </dl>

Questo evento viene inviato a tutti i client quando la modalità di ascolto inizia dopo che l'utente preme il tasto listening o quando termina il timeout oppure quando il client attivo per l'input chiama il metodo [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) con **True** o **False.**

L'evento restituisce valori ai client in cui è attualmente caricato questo carattere. Tutti gli altri client ricevono un carattere Null (stringa vuota).

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md)


 

 





