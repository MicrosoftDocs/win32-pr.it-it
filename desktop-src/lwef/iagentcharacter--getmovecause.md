---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 381d0f695fb1d183cced20609fc70abc0bfca0e51ddf2f904ae320a6c4844f06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962277"
---
# <a name="iagentcharactergetmovecause"></a>IAgentCharacter::GetMoveCause

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

Recupera la causa dell'ultimo spostamento del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

Indirizzo di una variabile che riceve la causa dell'ultimo spostamento del carattere e sarà uno dei seguenti:



| Valore                                                               | Descrizione                                                                                     |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **NeverMoved = 0;**<br/>        | Il carattere non è stato spostato.                                                        |
| **const unsigned short** **UserMoved = 1;**<br/>         | L'utente ha trascinato il carattere.                                                          |
| **const unsigned short** **ProgramMoved = 2;**<br/>      | L'applicazione ha spostato il carattere.                                                |
| **const unsigned short** **OtherProgramMoved = 3;**<br/> | Un'altra applicazione ha spostato il carattere.                                             |
| **const unsigned short** **SystemMoved = 4**<br/>        | Il server ha spostato il carattere per mantenerlo sullo schermo dopo una modifica della risoluzione dello schermo. |



 

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentNotifySink::Move**](iagentnotifysink--move.md)


 

 





