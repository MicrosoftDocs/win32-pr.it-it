---
title: IAgentCharacterEx GetHelpModeOn
description: IAgentCharacterEx GetHelpModeOn
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072f657ba5ac93d057474f062f73101f2559aed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221940"
---
# <a name="iagentcharacterexgethelpmodeon"></a>IAgentCharacterEx::GetHelpModeOn

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

Recupera un valore che indica se la modalità della Guida sensibile al contesto è attiva per il carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*
</dt> <dd>

Indirizzo di una variabile che riceve **true** se la modalità della guida è impostata su on per il carattere e **false** in caso contrario.

</dd> </dl>

Quando questa proprietà è impostata su **true**, il puntatore del mouse assume la forma dell'immagine della Guida sensibile al contesto quando viene spostato sul carattere o sul menu di scelta rapida per il carattere. Quando l'utente fa clic o trascina il carattere o fa clic su un elemento nel menu popup del carattere, il server attiva l'evento [**IAgentNotifySinkEx:: HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) e chiude la modalità della guida.

In modalità guida, il server non invia gli eventi [**IAgentNotifySink:: click**](iagentnotifysink--click.md), [**IAgentNotifySink::D ragstart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink::D Ragcomplete**](iagentnotifysink--dragcomplete.md)e [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) , a meno che la proprietà [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) non restituisca **true**. In tal caso, il server invierà l'evento **IAgentNotifySink:: click** (non esce dalla modalità guida), ma solo per il pulsante destro del mouse per consentire la visualizzazione del menu a comparsa.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)


 

 




