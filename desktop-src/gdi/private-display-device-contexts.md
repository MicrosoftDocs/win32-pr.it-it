---
description: Un contesto di dispositivo privato consente a un'applicazione di evitare il recupero e l'inizializzazione di un contesto di dispositivo di visualizzazione ogni volta che l'applicazione deve creare in una finestra.
ms.assetid: 8de5a14b-a8b3-42a5-81f3-bf3c357052cb
title: Contesti di dispositivo di visualizzazione privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451dbd3c0a232610026740d0ea0fa817ea2034b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528285"
---
# <a name="private-display-device-contexts"></a>Contesti di dispositivo di visualizzazione privati

Un *contesto di dispositivo privato* consente a un'applicazione di evitare il recupero e l'inizializzazione di un contesto di dispositivo di visualizzazione ogni volta che l'applicazione deve creare in una finestra. I contesti di dispositivi privati sono utili per Windows che richiedono molte modifiche ai valori degli attributi del contesto di dispositivo per prepararlo per il disegno. I contesti di dispositivi privati riducono il tempo necessario per preparare il contesto di dispositivo e quindi il tempo necessario per eseguire il disegno nella finestra.

Un'applicazione indica al sistema di creare un contesto di dispositivo privato per una finestra specificando lo \_ stile cs OWNDC nella classe Window. Il sistema crea un contesto di dispositivo privato univoco ogni volta che viene creata una nuova finestra appartenente alla classe. Inizialmente, il contesto di dispositivo privato ha gli stessi valori predefiniti per gli attributi di un contesto di dispositivo comune, ma l'applicazione può modificarli in qualsiasi momento. Il sistema conserva le modifiche apportate al contesto di dispositivo per la durata della finestra o fino a quando l'applicazione non apporta modifiche aggiuntive.

Un'applicazione può recuperare un handle per il contesto di dispositivo privato utilizzando la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) in qualsiasi momento dopo la creazione della finestra. L'applicazione deve recuperare l'handle una sola volta. In seguito, può contenere e utilizzare l'handle per un numero qualsiasi di volte. Poiché un contesto di dispositivo privato non fa parte della cache del contesto del dispositivo di visualizzazione, un'applicazione non deve mai rilasciare il contesto di dispositivo tramite la funzione [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) .

Il sistema regola automaticamente il contesto di dispositivo in modo da riflettere le modifiche apportate alla finestra, ad esempio lo spostare o il ridimensionamento. In questo modo si garantisce che tutte le finestre sovrapposte vengano sempre ritagliate correttamente; ovvero non è richiesta alcuna azione da parte dell'applicazione per garantire il ritaglio. Tuttavia, il sistema non modifica il contesto di dispositivo per includere l'area di aggiornamento. Pertanto, quando si elabora un messaggio di [**\_ disegno WM**](wm-paint.md) , l'applicazione deve incorporare l'area di aggiornamento chiamando [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) o recuperando l'area di aggiornamento e intersecando l'area di visualizzazione corrente. Se l'applicazione non chiama **BeginPaint**, deve convalidare in modo esplicito l'area di aggiornamento utilizzando la funzione [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) o [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) . Se l'applicazione non convalida l'area di aggiornamento, la finestra riceve una serie infinita di messaggi di **\_ disegno WM** .

Poiché [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) nasconde il punto di inserimento se viene visualizzato in una finestra, un'applicazione che chiama **BeginPaint** deve chiamare anche la funzione [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) per ripristinare il punto di inserimento. **EndPaint** non ha alcun effetto su un contesto di dispositivo privato.

Anche se un contesto di dispositivo privato è pratico da usare, è un utilizzo intensivo della memoria in termini di risorse di sistema, che richiedono 800 o più byte da archiviare. Quando considerazioni sulle prestazioni superano i costi di archiviazione, è consigliabile usare contesti di dispositivo privati.

Il sistema include il contesto di dispositivo privato durante l'invio del messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) all'applicazione. Le selezioni correnti del contesto di dispositivo privato, inclusa la modalità di mapping, sono attive quando l'applicazione o il sistema elabora questi messaggi. Per evitare effetti indesiderati, il sistema utilizza coordinate logiche quando si cancella lo sfondo; ad esempio, usa la funzione [**GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox) per recuperare le coordinate logiche dell'area da cancellare e passa queste coordinate alla funzione [**fillRect**](/windows/desktop/api/Winuser/nf-winuser-fillrect) . Le applicazioni che elaborano questi messaggi possono utilizzare tecniche simili.

Un'applicazione può usare la funzione [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) per forzare il sistema a restituire un contesto di dispositivo comune per la finestra con un contesto di dispositivo privato. Questa operazione è utile per eseguire rapidi ritocchi a una finestra senza modificare i valori correnti degli attributi del contesto di dispositivo privato.

 

 
