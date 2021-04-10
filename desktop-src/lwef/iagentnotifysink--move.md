---
title: Spostamento IAgentNotifySink
description: Spostamento IAgentNotifySink
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52563ff3838348b7bf8e6a2bcdfdf20a51c79723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955774"
---
# <a name="iagentnotifysinkmove"></a>IAgentNotifySink:: Move

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Move(
   long dwCharID,  // character ID
   long x,         // x-coordinate of new location
   long y,         // y-coordinate of new location
   long dwCause    // cause of move state
);                          
```

Notifica a un'applicazione client quando il carattere è stato spostato.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificatore del carattere che è stato spostato.

</dd> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordinata x della nuova posizione, espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra). La posizione di un carattere è basata sull'angolo superiore sinistro del frame di animazione.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordinata y della nuova posizione, espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra). La posizione di un carattere è basata sull'angolo superiore sinistro del frame di animazione.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

Motivo dello spostamento dei caratteri. Il parametro può essere uno dei seguenti:



| Valore                                                          | Descrizione                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **NeverMoved = 0;**<br/>        | Il carattere non è stato spostato.                                                        |
| **const unsigned short** **UserMoved = 1;**<br/>         | Il carattere è stato trascinato dall'utente.                                                          |
| ProgramMoved **short const senza segno** **= 2;**<br/>      | L'applicazione ha spostato il carattere.                                                |
| **const unsigned short** **OtherProgramMoved = 3;**<br/> | Il carattere è stato spostato da un'altra applicazione.                                             |
| SystemMoved **short const senza segno** **= 4**<br/>        | Il server ha spostato il carattere per mantenerlo sullo schermo dopo una modifica della risoluzione dello schermo. |



 

</dd> </dl>

Questo evento viene inviato a tutti i client del carattere.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: GetMoveCause**](iagentcharacter--getmovecause.md), [ **IAgentCharacter:: MoveTo**](iagentcharacter--moveto.md)


 

 





