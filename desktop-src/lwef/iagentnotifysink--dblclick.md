---
title: IAgentNotifySink DblClick
description: IAgentNotifySink DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88193f228f94d24384e6bf2b874e9208d67f3e9c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120924"
---
# <a name="iagentnotifysinkdblclick"></a>IAgentNotifySink::D blClick

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

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

Identificatore del carattere su cui si è fatto doppio clic.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Parametro che indica lo stato del pulsante del mouse e del tasto di modifica. Il parametro può restituire qualsiasi combinazione degli elementi seguenti:



| Valore  | Descrizione                               |
|--------|------------------------------------------------|
| 0x0001 | Pulsante sinistro                                    |
| 0x0010 | Pulsante centrale                                  |
| 0x0002 | Pulsante destro                                   |
| 0x0004 | MAIUSC+FRECCIA GIÙ                                 |
| 0x0008 | CTRL+FRECCIA GIÙ                               |
| 0x0020 | ALT+FRECCIA GIÙ                                   |
| 0x1000 | Evento che si è verificato sull'icona della barra delle applicazioni del carattere |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordinata x del puntatore del mouse in pixel rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Coordinata y del puntatore del mouse in pixel rispetto all'origine dello schermo (in alto a sinistra).

</dd> </dl>

Questo evento viene inviato al client attivo di input del carattere. Se nessuno dei client del carattere è attivo per l'input, il server invia una notifica al client attivo del carattere. Se il carattere è visibile, il server rende attivo anche l'input del client e invia [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md). Se il carattere è nascosto, viene visualizzato automaticamente anche il carattere.

 

 




