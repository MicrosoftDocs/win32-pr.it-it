---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63c24abd41f0509293ba2fafeb055f195a4d13ad354662e8d32d0fb1715e1fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477029"
---
# <a name="iagentnotifysinkdragcomplete"></a>IAgentNotifySink::D ragComplete

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

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

Parametro che indica lo stato del pulsante del mouse e del tasto di modifica. Il parametro può restituire qualsiasi combinazione degli elementi seguenti:



| Valore  | Descrizione      |
|--------|------------------|
| 0x0001 | Pulsante sinistro      |
| 0x0010 | Pulsante centrale    |
| 0x0002 | Pulsante destro     |
| 0x0004 | MAIUSC+FRECCIA GIÙ   |
| 0x0008 | CTRL+FRECCIA GIÙ |
| 0x0020 | ALT+FRECCIA GIÙ     |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordinata x del puntatore del mouse in pixel rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Coordinata y del puntatore del mouse in pixel rispetto all'origine dello schermo (in alto a sinistra).

</dd> </dl>

 

 




