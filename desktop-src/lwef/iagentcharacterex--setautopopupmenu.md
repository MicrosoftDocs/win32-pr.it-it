---
title: IAgentCharacterEx SetAutoPopupMenu
description: IAgentCharacterEx SetAutoPopupMenu
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a616bd95836d8f8131aaccabe0bb6db4f35a5caf22c480c17908935d80f2b12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477959"
---
# <a name="iagentcharacterexsetautopopupmenu"></a>IAgentCharacterEx::SetAutoPopupMenu

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetAutoPopupMenu(
   long bAutoPopupMenu,  // auto pop-up menu display setting
);
```

Imposta se il server visualizza automaticamente il menu a comparsa del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*
</dt> <dd>

Flag di visualizzazione del menu a comparsa automatico. Se questo parametro è **True,** Microsoft Agent visualizza automaticamente il menu a comparsa del carattere quando l'utente fa clic con il pulsante destro del mouse sull'icona della barra delle applicazioni del carattere o del carattere.

</dd> </dl>

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

Impostando questa proprietà su **False**, è possibile creare un comportamento di gestione dei menu personalizzato. Per visualizzare il menu dopo aver impostato questa proprietà su **False,** usare il [**metodo IAgentCharacterEx::ShowPopupMenu.**](iagentcharacterex--showpopupmenu.md)

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx::GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [ **IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)


 

 




