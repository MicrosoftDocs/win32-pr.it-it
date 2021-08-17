---
title: IAgentNotifySink Idle
description: IAgentNotifySink Idle
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8263bd9bc62d4fccfad74b18b189c6e4bae426245dd3d4d6a46c826ebacf498d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105175"
---
# <a name="iagentnotifysinkidle"></a>IAgentNotifySink::Idle

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

Notifica a un'applicazione client quando lo stato di **idling di un** carattere è stato modificato.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificatore della richiesta avviata.

</dd> <dt>

<span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*Bstart*
</dt> <dd>

Flag di avvio. Questo valore booleano **è True** quando il carattere inizia a idling e **False** quando si arresta l'idling.

</dd> </dl>

Questo evento consente di tenere traccia dell'avvio o dell'arresto dell'elaborazione inattiva del server Microsoft Agent per un carattere.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md), [ **IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)


 

 




