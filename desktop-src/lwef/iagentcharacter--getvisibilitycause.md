---
title: IAgentCharacter GetVisibilityCause
description: IAgentCharacter GetVisibilityCause
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdae2465ccc9e7153a0e9cc8202027137e2a7c0f07fdfb5da2a83a7c0d1ed1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962241"
---
# <a name="iagentcharactergetvisibilitycause"></a>IAgentCharacter::GetVisibilityCause

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

Recupera la causa dello stato visibile del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

Indirizzo di una variabile che riceve la causa dell'ultima modifica dello stato di visibilità del carattere e sarà una delle seguenti:



| Valore                                                                   | Descrizione                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **const unsigned short** **NeverShown = 0;**<br/>                 | Il carattere non è stato visualizzato.                                                               |
| **const unsigned short** **UserHid = 1;**<br/>                    | L'utente ha nascosto il carattere con il menu a comparsa dell'icona della barra delle applicazioni del carattere o usando l'input vocale. |
| **const unsigned short** **UserShowed = 2;**<br/>                 | L'utente ha mostrato il carattere.                                                                  |
| **const unsigned short** **ProgramHid = 3;**<br/>                 | L'applicazione ha nascosto il carattere.                                                         |
| **const unsigned short** **ProgramShowed = 4;**<br/>              | L'applicazione ha mostrato il carattere.                                                      |
| **const unsigned short** **OtherProgramHid = 5;**<br/>            | Un'altra applicazione ha nascosto il carattere.                                                      |
| **const unsigned short** **OtherProgramShowed = 6;**<br/>         | Un'altra applicazione ha mostrato il carattere.                                                   |
| **const unsigned short** **UserHidViaCharacterMenu = 7**<br/>     | L'utente ha nascosto il carattere con il menu a comparsa del carattere.                                    |
| **const unsigned short** **UserHidViaTaskbarIcon = UserHid**<br/> | L'utente ha nascosto il carattere con il menu a comparsa dell'icona della barra delle applicazioni del carattere o usando l'input vocale. |



 

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentNotifySink::VisibleState**](iagentnotifysink--visiblestate.md)


 

 





