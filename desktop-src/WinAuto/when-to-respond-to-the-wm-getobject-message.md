---
title: Quando rispondere al messaggio WM_GETOBJECT messaggio
description: Se un'applicazione supporta Microsoft Active Accessibility o Automazione interfaccia utente per un elemento dell'interfaccia utente, l'applicazione non deve rispondere al messaggio WM GETOBJECT prima che l'oggetto che rappresenta l'elemento dell'interfaccia utente sia completamente inizializzato o dopo l'inizio della chiusura \_ dell'applicazione.
ms.assetid: cc99f7ef-1eb6-40c4-9ec0-8fb18cb4a3e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdb12edde21b7906fdda91d1bc5d46e453696214b93a331e26034527e163a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114616"
---
# <a name="when-to-respond-to-the-wm_getobject-message"></a>Quando rispondere al messaggio WM \_ GETOBJECT

Se un'applicazione supporta Microsoft Active Accessibility o Automazione interfaccia utente per un elemento dell'interfaccia utente, l'applicazione non deve rispondere al messaggio [**WM \_ GETOBJECT**](wm-getobject.md) prima che l'oggetto che rappresenta l'elemento dell'interfaccia utente sia completamente inizializzato o dopo l'inizio della chiusura dell'applicazione. Quando un'applicazione crea una nuova finestra, il sistema genera l'evento [**EVENT \_ OBJECT \_ CREATE**](event-constants.md) WinEvent per inviare una notifica ai client prima di inviare il messaggio [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) alla routine della finestra dell'applicazione. Poiché molte applicazioni usano **WM \_ CREATE** per avviare il processo di inizializzazione, qualsiasi implementazione di accessibilità di un elemento dell'interfaccia utente non risponde al messaggio [**WM \_ GETOBJECT**](wm-getobject.md) fino al termine dell'elaborazione del messaggio **WM \_ CREATE** da parte dell'applicazione.

 

 