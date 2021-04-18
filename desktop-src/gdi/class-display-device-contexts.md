---
description: Utilizzando un contesto di dispositivo della classe, un'applicazione può utilizzare un unico contesto di dispositivo di visualizzazione per ogni finestra appartenente a una classe specificata.
ms.assetid: fc76abbf-68da-47f2-8145-4fad806297b4
title: Classe Visualizza contesti di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5a4cc0268d948e1a6f95050409698217e3f13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978783"
---
# <a name="class-display-device-contexts"></a>Classe Visualizza contesti di dispositivo

Utilizzando un *contesto di dispositivo della classe*, un'applicazione può utilizzare un unico contesto di dispositivo di visualizzazione per ogni finestra appartenente a una classe specificata. I contesti di dispositivo di classe vengono spesso usati con le finestre di controllo disegnate usando gli stessi valori di attributo. Analogamente ai contesti di dispositivi privati, i contesti di dispositivo di classe riducono al minimo il tempo necessario per preparare un contesto di dispositivo per il disegno.

Il sistema fornisce un contesto di dispositivo della classe per una finestra se appartiene a una classe di finestra con lo \_ stile cs CLASSDC. Il sistema crea il contesto di dispositivo quando crea la prima finestra appartenente alla classe e quindi usa lo stesso contesto di dispositivo per tutte le finestre create successivamente nella classe. Inizialmente, il contesto di dispositivo della classe ha gli stessi valori predefiniti per gli attributi di un contesto di dispositivo comune, ma l'applicazione può modificarli in qualsiasi momento. Il sistema conserva tutte le modifiche, ad eccezione dell'area di ridimensionamento e dell'origine del dispositivo, fino a quando l'ultima finestra della classe non viene eliminata definitivamente. Una modifica apportata a una finestra viene applicata a tutte le finestre di tale classe.

Un'applicazione può recuperare l'handle per il contesto di dispositivo della classe usando la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) in qualsiasi momento dopo la creazione della prima finestra. L'applicazione può rimanere e usare l'handle senza rilasciarlo perché il contesto di dispositivo della classe non fa parte della cache del contesto del dispositivo di visualizzazione. Se l'applicazione crea un'altra finestra nella stessa classe di finestra, l'applicazione deve recuperare di nuovo il contesto di dispositivo della classe. Il recupero del contesto di dispositivo imposta l'origine del dispositivo e l'area di ritaglio corrette per la nuova finestra. Dopo che l'applicazione recupera il contesto di dispositivo della classe per una nuova finestra nella classe, il contesto di dispositivo non può più essere usato per creare la finestra originale senza recuperarlo di nuovo per tale finestra. In generale, ogni volta che deve essere disegnato in una finestra, un'applicazione deve recuperare in modo esplicito il contesto di dispositivo della classe per la finestra.

Le applicazioni che usano i contesti di dispositivo della classe devono sempre chiamare [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) durante l'elaborazione di un messaggio di [**\_ disegno WM**](wm-paint.md) . La funzione imposta l'origine del dispositivo e l'area di ritaglio corrette per la finestra e incorpora l'area di aggiornamento. L'applicazione deve anche chiamare [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) per ripristinare il punto di inserimento se **BeginPaint** lo nasconde. **EndPaint** non ha alcun effetto su un contesto di dispositivo di classe.

Il sistema passa il contesto di dispositivo della classe quando invia il messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) all'applicazione, consentendo ai valori degli attributi correnti di influenzare qualsiasi disegno eseguito dall'applicazione o dal sistema durante l'elaborazione di questo messaggio. Come con una finestra con un contesto di dispositivo privato, un'applicazione può usare [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) per forzare il sistema a restituire un contesto di dispositivo comune per la finestra con un contesto di dispositivo di classe.

Non è consigliabile usare contesti di dispositivo di classe.

 

 
