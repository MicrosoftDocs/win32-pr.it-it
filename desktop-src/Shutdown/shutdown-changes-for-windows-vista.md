---
description: La tabella seguente riepiloga le differenze tra l'arresto in Windows Vista e Windows XP.
ms.assetid: da7985d2-85c8-47e1-a172-c9e92f450e24
title: Modifiche di arresto per Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd510e800de23c2304dbc8c61b6547f9f3e846002b234401d0b8e3d0bbaa820d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117963558"
---
# <a name="shutdown-changes-for-windows-vista"></a>Modifiche di arresto per Windows Vista

La tabella seguente riepiloga le differenze tra l'arresto in Windows Vista e Windows XP.



| Funzionalità                 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                | Windows Vista                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Blocco dell'arresto       | Le applicazioni possono ritardare la [**risposta a WM \_ QUERYENDSESSION**](wm-queryendsession.md) per 5 secondi, quindi il sistema consente all'utente di terminare l'applicazione. Le applicazioni che restituiscono **TRUE** in risposta a **WM \_ QUERYENDSESSION** possono ritardare la risposta a [**WM \_ ENDSESSION**](wm-endsession.md) per 5 secondi, quindi il sistema consente all'utente di terminare l'applicazione. | Le applicazioni possono ritardare la risposta [**a WM \_ QUERYENDSESSION**](wm-queryendsession.md) per 5 secondi, quindi il sistema consente all'utente di continuare o annullare l'arresto. Le applicazioni che restituiscono **TRUE** in risposta a **WM \_ QUERYENDSESSION** possono ritardare la risposta a [**WM \_ ENDSESSION**](wm-endsession.md) per 5 secondi, quindi il sistema consente all'utente di continuare o annullare l'arresto.                                                                                                      |
| Annullamento dell'arresto      | Se un'applicazione restituisce **FALSE** in risposta a [**WM \_ QUERYENDSESSION,**](wm-queryendsession.md)l'arresto viene annullato nella maggior parte dei casi. Tuttavia, non viene visualizzata alcuna interfaccia utente, pertanto l'utente potrebbe non essere a conoscenza del fatto che l'arresto è stato annullato.                                                                                                                                                      | Se un'applicazione restituisce **FALSE** in risposta a [**WM \_ QUERYENDSESSION,**](wm-queryendsession.md)viene comunque visualizzata nell'interfaccia utente di arresto. Si noti che il sistema non consente alle applicazioni console o alle applicazioni senza una finestra visibile di annullare l'arresto. Queste applicazioni vengono terminate automaticamente se non rispondono a **WM \_ QUERYENDSESSION** o [**WM \_ ENDSESSION**](wm-endsession.md) entro 5 secondi o se restituiscono **FALSE** in risposta a **WM \_ QUERYENDSESSION.** |
| Arrestare l'interfaccia utente | Il sistema visualizza una finestra di dialogo per ogni arresto di blocco dell'applicazione. Se l'utente fa clic **sul pulsante Termina** ora, l'applicazione viene terminata. Se l'utente fa clic sul **pulsante Annulla,** l'arresto viene annullato e l'applicazione continua a essere eseguita.                                                                                                                                    | Il sistema visualizza un'interfaccia utente a schermo intero che identifica tutte le applicazioni che bloccano l'arresto e i relativi motivi (se hanno registrato un motivo [**usando ShutdownBlockReasonCreate).**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)                                                                                                                                                                                                                                                                    |



 

## <a name="best-practices"></a>Procedure consigliate

-   Le applicazioni non devono bloccare l'arresto. Rispondere a [**WM \_ QUERYENDSESSION il**](wm-queryendsession.md) più rapidamente possibile e posticipare le attività di pulizia fino all'elaborazione del messaggio [**\_ ENDSESSION WM.**](wm-endsession.md)
-   Le applicazioni che devono bloccare l'arresto devono usare la nuova [**funzione ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) per registrare una stringa che spiega il motivo all'utente. L'utente può decidere se continuare o annullare l'arresto.
-   Le applicazioni non possono basarsi sulla possibilità di bloccare l'arresto.

 

 



