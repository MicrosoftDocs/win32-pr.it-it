---
title: IAgentCharacterEx GetHelpModeOn
description: IAgentCharacterEx GetHelpModeOn
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb78cf535fbfd7e28ab797c887c8e1548d3fd18dce03fb6b64d888c7e304c0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750786"
---
# <a name="iagentcharacterexgethelpmodeon"></a>IAgentCharacterEx::GetHelpModeOn

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

Recupera un valore che indica se la modalità guida sensibile al contesto è attivata per il carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*
</dt> <dd>

Indirizzo di una variabile che riceve **True se** la modalità Guida è attiva per il carattere e **False in** caso contrario.

</dd> </dl>

Quando questa proprietà è impostata su **True,** il puntatore del mouse passa all'immagine della Guida sensibile al contesto quando viene spostato sul carattere o sul menu a comparsa del carattere. Quando l'utente fa clic o trascina il carattere o fa clic su un elemento nel menu a comparsa del carattere, il server attiva l'evento [**IAgentNotifySinkEx::HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) e esce dalla modalità Guida.

In modalità Guida il server non invia gli eventi [**IAgentNotifySink::Click**](iagentnotifysink--click.md), [**IAgentNotifySink::D ragStart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink::D ragComplete**](iagentnotifysink--dragcomplete.md)e [**IAgentNotifySink::Command,**](iagentnotifysink--command.md) a meno che la proprietà [**GetAutoPopupMenu non**](https://www.bing.com/search?q=**GetAutoPopupMenu**) restituisca **True**. In tal caso, il server invierà l'evento **IAgentNotifySink::Click** (non esce dalla modalità Guida), ma solo per il pulsante destro del mouse per consentire la visualizzazione del menu a comparsa.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce su altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)


 

 




