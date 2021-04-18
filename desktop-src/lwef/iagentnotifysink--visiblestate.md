---
title: IAgentNotifySink VisibleState
description: IAgentNotifySink VisibleState
ms.assetid: b0346296-74e9-448f-aa6d-a9fb1e645f05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3525c079ecd1b566ac2230f06e3effa1ceb7a694
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298733"
---
# <a name="iagentnotifysinkvisiblestate"></a>IAgentNotifySink::VisibleState

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT VisibleState(
   long dwCharID,  // character ID
   long bVisible,  // visibility flag
   long dwCause,   // cause of visible state
);                          
```

Notifica a un'applicazione client quando viene modificato lo stato di visibilità del carattere.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificatore del carattere il cui stato di visibilità viene modificato.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Flag di visibilità. Questo valore booleano è **true** quando il carattere diventa visibile e **false** quando il carattere viene nascosto.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

Motivo dell'Ultima modifica apportata allo stato di visibilità del carattere. Il parametro può essere uno dei seguenti:



| Valore                                                                   | Descrizione                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **const unsigned short** **NeverShown = 0;**<br/>                 | Il carattere non è stato visualizzato.                                                               |
| **const unsigned short** **UserHid = 1;**<br/>                    | L'utente ha nascosto il carattere con il menu di scelta rapida dell'icona della barra delle applicazioni del carattere o con input vocale. |
| UserShowed **short const senza segno** **= 2;**<br/>                 | L'utente ha mostrato il carattere.                                                                  |
| **const unsigned short** **ProgramHid = 3;**<br/>                 | L'applicazione ha nascosto il carattere.                                                         |
| ProgramShowed **short const senza segno** **= 4;**<br/>              | L'applicazione ha mostrato il carattere.                                                      |
| **const unsigned short** **OtherProgramHid = 5;**<br/>            | Il carattere è stato nascosto da un'altra applicazione.                                                      |
| OtherProgramShowed **short senza segno const** **= 6;**<br/>         | Un'altra applicazione ha mostrato il carattere.                                                   |
| UserHidViaCharacterMenu **short const senza segno** **= 7**<br/>     | L'utente ha nascosto il carattere con il menu di scelta rapida del carattere.                                    |
| **const unsigned short** **UserHidViaTaskbarIcon = UserHid**<br/> | L'utente ha nascosto il carattere con il menu di scelta rapida dell'icona della barra delle applicazioni del carattere o usando l'input vocale. |



 

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: getVisible**](iagentcharacter--getvisible.md), [ **IAgentCharacter:: GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)


 

 





