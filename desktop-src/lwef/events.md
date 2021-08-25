---
title: IAgentNotifySink
description: IAgentNotifySink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43a092ddd9c50ff7aacb0254c4773a43005759ab23b6682aaf6484d5aef4839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725781"
---
# <a name="iagentnotifysink"></a>IAgentNotifySink

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

IAgentNotifySink notifica ai client quando si verificano determinate modifiche di stato. Queste funzioni sono disponibili anche da [IAgentNotifySinkEx.](iagentnotifysinkex.md)

**Metodi nell'ordine Vtable**



| IAgentNotifySink                                                      | Descrizione                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**Comando**](command-method.md)                                     | Si verifica quando il server elabora un comando definito dal client.                               |
| [**ActivateInputState**](iagentnotifysink--activateinputstate.md)    | Si verifica quando un carattere diventa o smette di essere attivo per l'input.                            |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Si verifica quando cambia lo **stato Visible** del carattere.                                   |
| [**Evento Click**](click-event.md)                                    | Si verifica quando si fa clic su un carattere.                                                      |
| [**Evento DblClick**](dblclick-event.md)                              | Si verifica quando si fa doppio clic su un carattere.                                               |
| [**DragStart**](/windows/desktop/lwef/dragstart-event)                                | Si verifica quando un utente inizia a trascinare un carattere.                                          |
| [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)                          | Si verifica quando un utente smette di trascinare un carattere.                                           |
| [**RequestStart**](iagentnotifysink--requeststart.md)                | Si verifica quando il server avvia l'elaborazione [**di un oggetto**](/windows/desktop/lwef/the-request-object) Request.    |
| [**RequestComplete**](iagentnotifysink--requestcomplete.md)          | Si verifica quando il server completa l'elaborazione [**di un oggetto Request.**](/windows/desktop/lwef/the-request-object) |
| [**Segnalibro**](iagentnotifysink--bookmark.md)                        | Si verifica quando il server elabora un segnalibro.                                             |
| [**Inattivo**](iagentnotifysink--idle.md)                                | Si verifica quando il server avvia o termina l'elaborazione inattiva.                                   |
| [**Sposta**](iagentnotifysink--move.md)                                | Si verifica quando un carattere è stato spostato.                                                  |
| [**Dimensione**](iagentnotifysink---size.md)                               | Si verifica quando un carattere è stato ridimensionato.                                                |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Si verifica quando lo stato di visibilità del fumetto di un carattere cambia.                  |



 

Gli eventi IAgentNotifySink::Restart e IAgentNotifySink::Shutdown, supportati nelle versioni precedenti di Microsoft Agent, sono ora obsoleti. Sebbene sia supportato per la compatibilità con le versioni precedenti, il server non invia più questi eventi.

 

 