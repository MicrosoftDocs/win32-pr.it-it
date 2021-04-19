---
title: IAgentNotifySink inattivo
description: IAgentNotifySink inattivo
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43e060f361499b02bc0a83db697938975c76291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298794"
---
# <a name="iagentnotifysinkidle"></a>IAgentNotifySink:: Idle

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

Notifica a un'applicazione client quando è stato modificato lo stato di **minimo** di un carattere.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificatore della richiesta avviata.

</dd> <dt>

<span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*
</dt> <dd>

Flag di avvio. Questo valore booleano è **true** quando il carattere inizia al minimo e **false** quando si arresta al minimo.

</dd> </dl>

Questo evento consente di tenere traccia del momento in cui il server Microsoft Agent avvia o interrompe l'elaborazione inattiva per un carattere.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: GetIdleOn**](iagentcharacter--getidleon.md), [ **IAgentCharacter:: SetIdleOn**](iagentcharacter--setidleon.md)


 

 




