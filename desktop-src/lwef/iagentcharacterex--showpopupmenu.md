---
title: IAgentCharacterEx ShowPopupMenu
description: IAgentCharacterEx ShowPopupMenu
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67d01edae103bad10eb085c4bfd1f5ce559bf26ab030816d241367ec3c13763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105459"
---
# <a name="iagentcharacterexshowpopupmenu"></a>IAgentCharacterEx::ShowPopupMenu

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

Visualizza il menu a comparsa per il carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordinata x del menu a comparsa del carattere in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Coordinata y del menu a comparsa del carattere in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> </dl>

Quando si imposta [**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) su **False,** il server non visualizza più automaticamente il menu quando si fa clic con il pulsante destro del mouse sul carattere o sull'icona della barra delle applicazioni. È possibile usare questo metodo per visualizzare il menu.

Il menu viene visualizzato fino a quando l'utente non seleziona un comando o visualizza un altro menu. È possibile visualizzare un solo menu a comparsa alla volta. Pertanto, le chiamate a questo metodo annullano (rimuovono) il menu precedente.

Questo metodo deve essere chiamato solo quando l'applicazione client è il client attivo del carattere. in caso contrario, ha esito negativo.

[**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md)

 

 




