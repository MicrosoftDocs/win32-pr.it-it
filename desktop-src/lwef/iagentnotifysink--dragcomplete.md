---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53215591e3d2797c5b57e5586ccb13fc91f5902
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045232"
---
# <a name="iagentnotifysinkdragcomplete"></a>IAgentNotifySink::D ragComplete

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

Notifica a un'applicazione client quando l'utente smette di trascinare un carattere.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificatore del carattere trascinato.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Parametro che indica il pulsante del mouse e lo stato del tasto di modifica. Il parametro può restituire qualsiasi combinazione dei seguenti elementi:



|        |                  |
|--------|------------------|
| 0x0001 | Pulsante sinistro      |
| 0x0010 | Pulsante centrale    |
| 0x0002 | Pulsante destro     |
| 0x0004 | Tasto MAIUSC giù   |
| 0x0008 | Chiave di controllo in basso |
| 0x0020 | Tasto ALT premuto     |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordinata x del puntatore del mouse, in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordinata y del puntatore del mouse, in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> </dl>

 

 




