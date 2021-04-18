---
title: IAgentCharacter GetVisibilityCause
description: IAgentCharacter GetVisibilityCause
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6013385144b82b79a0f17ae6443b094a9d9c8a4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396983"
---
# <a name="iagentcharactergetvisibilitycause"></a>IAgentCharacter::GetVisibilityCause

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

Recupera la motivo dello stato visibile del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

Indirizzo di una variabile che riceve la modifica dello stato dell'ultima visibilità del carattere e sarà uno dei seguenti:



| Valore                                                                   | Descrizione                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **const unsigned short** **NeverShown = 0;**<br/>                 | Il carattere non è stato visualizzato.                                                               |
| **const unsigned short** **UserHid = 1;**<br/>                    | L'utente ha nascosto il carattere con il menu di scelta rapida dell'icona della barra delle applicazioni del carattere o usando l'input vocale. |
| UserShowed **short const senza segno** **= 2;**<br/>                 | L'utente ha mostrato il carattere.                                                                  |
| **const unsigned short** **ProgramHid = 3;**<br/>                 | L'applicazione ha nascosto il carattere.                                                         |
| ProgramShowed **short const senza segno** **= 4;**<br/>              | L'applicazione ha mostrato il carattere.                                                      |
| **const unsigned short** **OtherProgramHid = 5;**<br/>            | Il carattere è stato nascosto da un'altra applicazione.                                                      |
| OtherProgramShowed **short senza segno const** **= 6;**<br/>         | Un'altra applicazione ha mostrato il carattere.                                                   |
| UserHidViaCharacterMenu **short const senza segno** **= 7**<br/>     | L'utente ha nascosto il carattere con il menu di scelta rapida del carattere.                                    |
| **const unsigned short** **UserHidViaTaskbarIcon = UserHid**<br/> | L'utente ha nascosto il carattere con il menu di scelta rapida dell'icona della barra delle applicazioni del carattere o usando l'input vocale. |



 

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentNotifySink::VisibleState**](iagentnotifysink--visiblestate.md)


 

 





