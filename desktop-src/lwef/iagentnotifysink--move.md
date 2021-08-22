---
title: Spostamento di IAgentNotifySink
description: Spostamento di IAgentNotifySink
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16f32df3058a5b5c8e0a4e02a98f9a97afdbff56f349a63fceb5d70a9001391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105176"
---
# <a name="iagentnotifysinkmove"></a>IAgentNotifySink::Move

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

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

Identificatore del carattere spostato.

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordinata x della nuova posizione in pixel rispetto all'origine dello schermo (in alto a sinistra). La posizione di un carattere è basata sull'angolo superiore sinistro del frame di animazione.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Coordinata y della nuova posizione in pixel rispetto all'origine dello schermo (in alto a sinistra). La posizione di un carattere è basata sull'angolo superiore sinistro del frame di animazione.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

Causa dello spostamento del carattere. Il parametro può essere uno dei seguenti:



| Valore                                                          | Descrizione                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **NeverMoved = 0;**<br/>        | Il carattere non è stato spostato.                                                        |
| **const unsigned short** **UserMoved = 1;**<br/>         | L'utente ha trascinato il carattere.                                                          |
| **const unsigned short** **ProgramMoved = 2;**<br/>      | L'applicazione ha spostato il carattere.                                                |
| **const unsigned short** **OtherProgramMoved = 3;**<br/> | Un'altra applicazione ha spostato il carattere.                                             |
| **const unsigned short** **SystemMoved = 4**<br/>        | Il server ha spostato il carattere per mantenerlo sullo schermo dopo una modifica della risoluzione dello schermo. |



 

</dd> </dl>

Questo evento viene inviato a tutti i client del carattere.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::GetMoveCause**](iagentcharacter--getmovecause.md), [ **IAgentCharacter::MoveTo**](iagentcharacter--moveto.md)


 

 





