---
title: IAgentCharacterEx SetHelpModeOn
description: IAgentCharacterEx SetHelpModeOn
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aacbdf9c0ea9737bb73ba7a99e0839e1435379e42536a82aa30c2ca034a28860
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062031"
---
# <a name="iagentcharacterexsethelpmodeon"></a>IAgentCharacterEx::SetHelpModeOn

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

Imposta la modalità Guida sensibile al contesto attivata per il carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*
</dt> <dd>

Flag della modalità Guida. Se questo parametro è **True,** Microsoft Agent attiva la modalità Guida per il carattere.

</dd> </dl>

Quando si imposta questa proprietà su **True,** il puntatore del mouse passa all'immagine della Guida sensibile al contesto quando viene spostato sul carattere o sul menu a comparsa per il carattere. Quando l'utente fa clic o trascina il carattere o fa clic su un elemento nel menu a comparsa del carattere, il server attiva l'evento [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md) e esce dalla modalità Guida.

In modalità Guida il server non invia gli eventi [**Click**](click-event.md), [**DragStart**](/windows/desktop/lwef/dragstart-event), [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)e [**Command,**](command-event.md) a meno che la proprietà [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) non restituisca **True**. In tal caso, il server invierà l'evento **Click** (non esce dalla modalità Guida), ma solo per il pulsante destro del mouse in modo da poter visualizzare il menu a comparsa.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx::GetHelpModeOn,**](iagentcharacterex--gethelpmodeon.md) [ **IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md)


 

 