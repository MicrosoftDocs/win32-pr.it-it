---
description: Un contesto di dispositivo privato consente a un'applicazione di evitare di recuperare e inizializzare un contesto di dispositivo di visualizzazione ogni volta che l'applicazione deve disegnare in una finestra.
ms.assetid: 8de5a14b-a8b3-42a5-81f3-bf3c357052cb
title: Contesti di dispositivo di visualizzazione privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce63fddbc2e351b166308c9ca3ce674be1a0026851af7bb1192c49cc961cdee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092881"
---
# <a name="private-display-device-contexts"></a>Contesti di dispositivo di visualizzazione privati

Un *contesto di dispositivo privato* consente a un'applicazione di evitare di recuperare e inizializzare un contesto di dispositivo di visualizzazione ogni volta che l'applicazione deve disegnare in una finestra. I contesti di dispositivo privati sono utili per le finestre che richiedono molte modifiche ai valori degli attributi del contesto di dispositivo per prepararlo per il disegno. I contesti di dispositivo privati riducono il tempo necessario per preparare il contesto di dispositivo e quindi il tempo necessario per eseguire il disegno nella finestra.

Un'applicazione indica al sistema di creare un contesto di dispositivo privato per una finestra specificando lo stile CS \_ OWNDC nella classe della finestra. Il sistema crea un contesto di dispositivo privato univoco ogni volta che crea una nuova finestra appartenente alla classe . Inizialmente, il contesto di dispositivo privato ha gli stessi valori predefiniti per gli attributi di un contesto di dispositivo comune, ma l'applicazione può modificarli in qualsiasi momento. Il sistema mantiene le modifiche al contesto di dispositivo per tutta la durata della finestra o fino a quando l'applicazione non apporta altre modifiche.

Un'applicazione può recuperare un handle per il contesto di dispositivo privato usando la [**funzione GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) in qualsiasi momento dopo la creazione della finestra. L'applicazione deve recuperare l'handle una sola volta. Successivamente, può mantenere e usare l'handle per un numero qualsiasi di volte. Poiché un contesto di dispositivo privato non fa parte della cache del contesto di dispositivo di visualizzazione, un'applicazione non deve mai rilasciare il contesto di dispositivo usando la [**funzione ReleaseDC.**](/windows/desktop/api/Winuser/nf-winuser-releasedc)

Il sistema regola automaticamente il contesto di dispositivo per riflettere le modifiche apportate alla finestra, ad esempio lo spostamento o il ridimensionamento. Ciò garantisce che tutte le finestre sovrapposte siano sempre ritagliate correttamente; ciò significa che l'applicazione non richiede alcuna azione per garantire il ritaglio. Tuttavia, il sistema non modifica il contesto di dispositivo per includere l'area di aggiornamento. Pertanto, quando si elabora un messaggio [**WM \_ PAINT,**](wm-paint.md) l'applicazione deve incorporare l'area di aggiornamento chiamando [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) o recuperando l'area di aggiornamento e intersecarla con l'area di ritaglio corrente. Se l'applicazione non chiama **BeginPaint,** deve convalidare in modo esplicito l'area di aggiornamento usando la [**funzione ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) [**o ValidateRgn.**](/windows/desktop/api/Winuser/nf-winuser-validatergn) Se l'applicazione non convalida l'area di aggiornamento, la finestra riceve una serie infinita di **messaggi WM \_ PAINT.**

Poiché [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) nasconde il punto di ingresso se viene visualizzato in una finestra, un'applicazione che chiama **BeginPaint** deve chiamare anche la [**funzione EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) per ripristinare il punto di controllo. **EndPaint** non ha altri effetti su un contesto di dispositivo privato.

Anche se un contesto di dispositivo privato è pratico da usare, è a elevato utilizzo di memoria in termini di risorse di sistema e richiede 800 o più byte da archiviare. I contesti di dispositivo privati sono consigliati quando le considerazioni sulle prestazioni superano i costi di archiviazione.

Il sistema include il contesto di dispositivo privato quando si invia il [**messaggio WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) all'applicazione. Le selezioni correnti del contesto di dispositivo privato, inclusa la modalità di mapping, sono effettive quando l'applicazione o il sistema elabora questi messaggi. Per evitare effetti indesiderati, il sistema usa coordinate logiche durante la cancellazione dello sfondo; Ad esempio, usa la [**funzione GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox) per recuperare le coordinate logiche dell'area da cancellare e passa queste coordinate alla [**funzione FillRect.**](/windows/desktop/api/Winuser/nf-winuser-fillrect) Le applicazioni che elaborano questi messaggi possono usare tecniche simili.

Un'applicazione può usare [**la funzione GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) per forzare il sistema a restituire un contesto di dispositivo comune per la finestra con un contesto di dispositivo privato. Ciò è utile per eseguire rapidi touch up in una finestra senza modificare i valori correnti degli attributi del contesto di dispositivo privato.

 

 
