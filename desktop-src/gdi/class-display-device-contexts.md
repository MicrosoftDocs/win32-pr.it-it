---
description: Usando un contesto di dispositivo di classe, un'applicazione può usare un singolo contesto di dispositivo di visualizzazione per ogni finestra appartenente a una classe specificata.
ms.assetid: fc76abbf-68da-47f2-8145-4fad806297b4
title: Contesti di dispositivo di visualizzazione delle classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8e4ca7f7d51f3dd50f50a07ab44496d56e4a78effb78f33e9eed6f5ffc3745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062481"
---
# <a name="class-display-device-contexts"></a>Contesti di dispositivo di visualizzazione delle classi

Usando un contesto *di dispositivo della* classe , un'applicazione può usare un singolo contesto di dispositivo di visualizzazione per ogni finestra appartenente a una classe specificata. I contesti di dispositivo della classe vengono spesso usati con le finestre di controllo disegnate usando gli stessi valori di attributo. Analogamente ai contesti di dispositivo privati, i contesti di dispositivo della classe riducono al minimo il tempo necessario per preparare un contesto di dispositivo per il disegno.

Il sistema fornisce un contesto di dispositivo della classe per una finestra se appartiene a una classe finestra con lo stile CS \_ CLASSDC. Il sistema crea il contesto di dispositivo quando crea la prima finestra appartenente alla classe e quindi usa lo stesso contesto di dispositivo per tutte le finestre create successivamente nella classe . Inizialmente, il contesto di dispositivo della classe ha gli stessi valori predefiniti per gli attributi di un contesto di dispositivo comune, ma l'applicazione può modificarli in qualsiasi momento. Il sistema mantiene tutte le modifiche, ad eccezione dell'area di ritaglio e dell'origine del dispositivo, fino a quando l'ultima finestra della classe non è stata distrutta. Una modifica apportata per una finestra si applica a tutte le finestre in tale classe.

Un'applicazione può recuperare l'handle per il contesto di dispositivo della classe usando la [**funzione GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) in qualsiasi momento dopo la creazione della prima finestra. L'applicazione può mantenere e usare l'handle senza rilasciarlo perché il contesto di dispositivo della classe non fa parte della cache del contesto di dispositivo di visualizzazione. Se l'applicazione crea un'altra finestra nella stessa classe finestra, l'applicazione deve recuperare nuovamente il contesto di dispositivo della classe. Il recupero del contesto di dispositivo imposta l'origine del dispositivo e l'area di ritaglio corrette per la nuova finestra. Dopo che l'applicazione ha recuperato il contesto di dispositivo della classe per una nuova finestra nella classe , il contesto di dispositivo non può più essere usato per disegnare nella finestra originale senza recuperarlo di nuovo per tale finestra. In generale, ogni volta che deve disegnare in una finestra, un'applicazione deve recuperare in modo esplicito il contesto di dispositivo della classe per la finestra.

Le applicazioni che usano contesti di dispositivo della classe devono sempre chiamare [**BeginPaint durante**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) l'elaborazione di [**un messaggio WM \_ PAINT.**](wm-paint.md) La funzione imposta l'origine del dispositivo e l'area di ritaglio corrette per la finestra e incorpora l'area di aggiornamento. L'applicazione deve chiamare [**anche EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) per ripristinare il punto di sospensione se **BeginPaint** lo nasconde. **EndPaint** non ha altri effetti su un contesto di dispositivo della classe.

Il sistema passa il contesto di dispositivo della classe quando invia il messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) all'applicazione, permettendo ai valori dell'attributo corrente di influire su qualsiasi disegno eseguito dall'applicazione o dal sistema durante l'elaborazione del messaggio. Come nel caso di una finestra con un contesto di dispositivo privato, un'applicazione può usare [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) per forzare il sistema a restituire un contesto di dispositivo comune per la finestra con un contesto di dispositivo di classe.

Non è consigliabile usare contesti di dispositivo della classe.

 

 
