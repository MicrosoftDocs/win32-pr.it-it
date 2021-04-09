---
title: IAgentCharacterEx SetAutoPopupMenu
description: IAgentCharacterEx SetAutoPopupMenu
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcfd1bd7ea0b02f226ed6f0365b466577807a193
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955528"
---
# <a name="iagentcharacterexsetautopopupmenu"></a>IAgentCharacterEx::SetAutoPopupMenu

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetAutoPopupMenu(
   long bAutoPopupMenu,  // auto pop-up menu display setting
);
```

Imposta un valore che indica se il server Visualizza automaticamente il menu di scelta rapida del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*
</dt> <dd>

Flag di visualizzazione del menu a comparsa automatico. Se questo parametro è **true**, Microsoft Agent visualizzerà automaticamente il menu popup del carattere quando l'utente fa clic con il pulsante destro del mouse sull'icona della barra delle applicazioni del carattere o del carattere.

</dd> </dl>

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

Impostando questa proprietà su **false**, è possibile creare un comportamento personalizzato per la gestione dei menu. Per visualizzare il menu dopo l'impostazione di questa proprietà su **false**, usare il metodo [**IAgentCharacterEx:: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) .

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx:: GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [ **IAgentCharacterEx:: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)


 

 




