---
title: DblClick IAgentNotifySink
description: DblClick IAgentNotifySink
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ec7372d524027588dae5a0a3aafaf07146556e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395991"
---
# <a name="iagentnotifysinkdblclick"></a>IAgentNotifySink::D blClick

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

Notifica a un'applicazione client quando l'utente fa doppio clic su un carattere.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificatore del carattere a doppio clic.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Parametro che indica il pulsante del mouse e lo stato del tasto di modifica. Il parametro può restituire qualsiasi combinazione dei seguenti elementi:



|        |                                                |
|--------|------------------------------------------------|
| 0x0001 | Pulsante sinistro                                    |
| 0x0010 | Pulsante centrale                                  |
| 0x0002 | Pulsante destro                                   |
| 0x0004 | Tasto MAIUSC giù                                 |
| 0x0008 | Chiave di controllo in basso                               |
| 0x0020 | Tasto ALT premuto                                   |
| 0x1000 | Si è verificato l'evento sull'icona della barra delle applicazioni del carattere |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordinata x del puntatore del mouse, in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordinata y del puntatore del mouse, in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> </dl>

Questo evento viene inviato al client attivo di input del carattere. Se nessuno dei client del carattere è attivo per l'input, il server invia una notifica al client attivo del carattere. Se il carattere è visibile, il server rende anche attivo l'input del client e invia [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md). Se il carattere è nascosto, viene visualizzato automaticamente anche il carattere.

 

 




