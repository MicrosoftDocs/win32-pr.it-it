---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612fcbfd4470d17e2365373458a8ded899a8180a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396991"
---
# <a name="iagentcharactergetmovecause"></a>IAgentCharacter::GetMoveCause

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

Recupera la motivo dell'ultima spostamento del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

Indirizzo di una variabile che riceve la motivo dell'ultimo spostamento del carattere e sarà uno dei seguenti:



|                                                                |                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **NeverMoved = 0;**<br/>        | Il carattere non è stato spostato.                                                        |
| **const unsigned short** **UserMoved = 1;**<br/>         | Il carattere è stato trascinato dall'utente.                                                          |
| ProgramMoved **short const senza segno** **= 2;**<br/>      | L'applicazione ha spostato il carattere.                                                |
| **const unsigned short** **OtherProgramMoved = 3;**<br/> | Il carattere è stato spostato da un'altra applicazione.                                             |
| SystemMoved **short const senza segno** **= 4**<br/>        | Il server ha spostato il carattere per mantenerlo sullo schermo dopo una modifica della risoluzione dello schermo. |



 

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentNotifySink:: Move**](iagentnotifysink--move.md)


 

 





