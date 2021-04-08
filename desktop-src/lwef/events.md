---
title: IAgentNotifySink
description: IAgentNotifySink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2ccfd4acf4a64c229379aeea5847fbe044b7d5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046666"
---
# <a name="iagentnotifysink"></a>IAgentNotifySink

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

IAgentNotifySink notifica ai client quando si verificano determinate modifiche di stato. Queste funzioni sono disponibili anche da [IAgentNotifySinkEx](iagentnotifysinkex.md).

**Metodi nell'ordine Vtable**



| IAgentNotifySink                                                      | Descrizione                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**Comando**](command-method.md)                                     | Si verifica quando il server elabora un comando definito dal client.                               |
| [**ActivateInputState**](iagentnotifysink--activateinputstate.md)    | Si verifica quando un carattere diventa o smette di essere input-Active.                            |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Si verifica quando cambia lo stato **visibile** del carattere.                                   |
| [**Evento Click**](click-event.md)                                    | Si verifica quando si fa clic su un carattere.                                                      |
| [**Evento DblClick**](dblclick-event.md)                              | Si verifica quando si fa doppio clic su un carattere.                                               |
| [**DragStart**](/windows/desktop/lwef/dragstart-event)                                | Si verifica quando un utente inizia a trascinare un carattere.                                          |
| [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)                          | Si verifica quando un utente smette di trascinare un carattere.                                           |
| [**RequestStart**](iagentnotifysink--requeststart.md)                | Si verifica quando il server inizia a elaborare un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .    |
| [**RequestComplete**](iagentnotifysink--requestcomplete.md)          | Si verifica quando il server completa l'elaborazione di un oggetto [**Request**](/windows/desktop/lwef/the-request-object) . |
| [**Segnalibro**](iagentnotifysink--bookmark.md)                        | Si verifica quando il server elabora un segnalibro.                                             |
| [**Inattivo**](iagentnotifysink--idle.md)                                | Si verifica all'avvio o alla fine dell'elaborazione inattiva del server.                                   |
| [**Spostare**](iagentnotifysink--move.md)                                | Si verifica quando un carattere è stato spostato.                                                  |
| [**Dimensione**](iagentnotifysink---size.md)                               | Si verifica quando un carattere è stato ridimensionato.                                                |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Si verifica quando cambia lo stato di visibilità del fumetto di parole di un carattere.                  |



 

Gli eventi IAgentNotifySink:: Restart e IAgentNotifySink:: Shutdown, supportati nelle versioni precedenti di Microsoft Agent, sono ora obsoleti. Sebbene supportato per la compatibilità con le versioni precedenti, il server non invia più questi eventi.

 

 