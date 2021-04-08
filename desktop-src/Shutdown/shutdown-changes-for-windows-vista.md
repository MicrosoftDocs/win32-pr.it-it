---
description: Nella tabella seguente sono riepilogate le differenze tra l'arresto di Windows Vista e Windows XP.
ms.assetid: da7985d2-85c8-47e1-a172-c9e92f450e24
title: Modifiche di arresto per Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e04bb20099349ce378384cf01c39e53ca03a896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050069"
---
# <a name="shutdown-changes-for-windows-vista"></a>Modifiche di arresto per Windows Vista

Nella tabella seguente sono riepilogate le differenze tra l'arresto di Windows Vista e Windows XP.



| Funzionalità                 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                | Windows Vista                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Arresto blocco       | Le applicazioni possono ritardare la risposta a [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) per 5 secondi, quindi il sistema consente all'utente di terminare l'applicazione. Le applicazioni che restituiscono **true** in risposta a **WM \_ QUERYENDSESSION** possono ritardare la risposta a [**WM \_ ENDSESSION**](wm-endsession.md) per 5 secondi, quindi il sistema consente all'utente di terminare l'applicazione. | Le applicazioni possono ritardare la risposta a [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) per 5 secondi, quindi il sistema consente all'utente di continuare o annullare l'arresto. Le applicazioni che restituiscono **true** in risposta a **WM \_ QUERYENDSESSION** possono ritardare la risposta a [**WM \_ ENDSESSION**](wm-endsession.md) per 5 secondi, quindi il sistema consente all'utente di continuare o annullare l'arresto.                                                                                                      |
| Annullamento dell'arresto      | Se un'applicazione restituisce **false** in risposta a [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), nella maggior parte dei casi l'arresto viene annullato. Tuttavia, non viene visualizzata alcuna interfaccia utente, pertanto l'utente potrebbe non essere in grado di tenere presente che l'arresto è stato annullato.                                                                                                                                                      | Se un'applicazione restituisce **false** in risposta a [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), viene comunque visualizzata nell'interfaccia utente di arresto. Si noti che il sistema non consente le applicazioni console o le applicazioni senza una finestra visibile per annullare l'arresto. Queste applicazioni vengono terminate automaticamente se non rispondono a **WM \_ QUERYENDSESSION** o [**WM \_ ENDSESSION**](wm-endsession.md) entro 5 secondi o se restituiscono **false** in risposta a **WM \_ QUERYENDSESSION**. |
| Interfaccia utente shutdown | Il sistema Visualizza una finestra di dialogo per l'arresto del blocco dell'applicazione. Se l'utente fa clic sul pulsante **Termina ora** , l'applicazione viene terminata. Se l'utente fa clic sul pulsante **Annulla** , l'arresto viene annullato e l'applicazione continua a essere eseguita.                                                                                                                                    | Il sistema Visualizza un'interfaccia utente a schermo intero che identifica tutte le applicazioni che bloccano l'arresto e i motivi per farlo (se hanno registrato un motivo con [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)).                                                                                                                                                                                                                                                                    |



 

## <a name="best-practices"></a>Procedure consigliate

-   Le applicazioni non devono bloccare l'arresto. Rispondere a [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) il più rapidamente possibile e posticipare le attività di pulizia fino all'elaborazione del messaggio [**WM \_ ENDSESSION**](wm-endsession.md) .
-   Le applicazioni che devono bloccare la chiusura devono usare la nuova funzione [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) per registrare una stringa che ne spiega il motivo. L'utente può decidere se continuare o annullare l'arresto.
-   Le applicazioni non possono basarsi sulla possibilità di bloccare l'arresto.

 

 



