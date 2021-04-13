---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 031e78319beb0f62ddb0ea340fca0cd7ed88c0a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330076"
---
# <a name="iagentnotifysinkdragstart"></a>IAgentNotifySink::D ragStart

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

Notifica a un'applicazione client quando l'utente inizia a trascinare un carattere.

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

 

 




