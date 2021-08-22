---
description: Un'applicazione ottiene un controller di dominio di visualizzazione chiamando la funzione BeginPaint, GetDC o GetDCEx e identificando la finestra in cui verrà visualizzato l'output corrispondente.
ms.assetid: 8f952d68-ee52-4e63-9f09-80a14c755d31
title: Visualizzare i contesti di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2e2bbd847d1a473ff08de7db52da7513b91377e8a891b2c6fdde04a82bf1d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761326"
---
# <a name="display-device-contexts"></a>Visualizzare i contesti di dispositivo

Un'applicazione ottiene un controller di dominio di visualizzazione chiamando la funzione [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) e identificando la finestra in cui verrà visualizzato l'output corrispondente. In genere, un'applicazione ottiene un controller di dominio di visualizzazione solo quando deve disegnare nell'area client. Tuttavia, è possibile ottenere un [contesto di dispositivo della](#window-device-contexts) finestra chiamando la funzione [**GetWindowDC.**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) Al termine del disegno, l'applicazione deve rilasciare il controller di dominio chiamando la [**funzione EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) [**o ReleaseDC.**](/windows/desktop/api/Winuser/nf-winuser-releasedc)

Esistono cinque tipi di controller di dominio per gli schermi video:

-   Classe
-   Comuni
-   Privato
-   Finestra
-   Padre

## <a name="class-device-contexts"></a>Contesti di dispositivo della classe

*I contesti di dispositivo* delle classi sono supportati esclusivamente per la compatibilità con le versioni a 16 bit di Windows. Quando si scrive l'applicazione, evitare di usare il contesto di dispositivo della classe . usare invece un contesto di dispositivo privato.

## <a name="common-device-contexts"></a>Contesti di dispositivo comuni

*I contesti di dispositivo* comuni sono controller di dominio visualizzati gestiti in una cache speciale dal sistema. I contesti di dispositivo comuni vengono usati nelle applicazioni che eseguono operazioni di disegno poco frequenti. Prima che il sistema restituisca l'handle del controller di dominio, inizializza il contesto di dispositivo comune con oggetti, attributi e modalità predefiniti. Tutte le operazioni di disegno eseguite dall'applicazione usano queste impostazioni predefinite, a meno che non venga chiamata una delle funzioni GDI per selezionare un nuovo oggetto, modificare gli attributi di un oggetto esistente o selezionare una nuova modalità.

Poiché esiste solo un numero limitato di contesti di dispositivo comuni, un'applicazione deve rilasciarli al termine del disegno. Quando l'applicazione rilascia un contesto di dispositivo comune, tutte le modifiche ai dati predefiniti vengono perse.

## <a name="private-device-contexts"></a>Contesti di dispositivo privati

*I contesti di dispositivo* privati sono controller di dominio di visualizzazione che, a differenza dei contesti di dispositivo comuni, mantengono le modifiche ai dati predefiniti anche dopo il rilascio da parte di un'applicazione. I contesti di dispositivo privati vengono usati nelle applicazioni che eseguono numerose operazioni di disegno, ad esempio applicazioni CAD (Computer-Aided Design), applicazioni di pubblicazione desktop, applicazioni di disegno e disegno e così via. I contesti di dispositivo privati non fanno parte della cache di sistema e pertanto non devono essere rilasciati dopo l'uso. Il sistema rimuove automaticamente un contesto di dispositivo privato dopo l'eliminazione dell'ultima finestra della classe.

Un'applicazione crea un contesto di dispositivo privato specificando prima di tutto lo stile della classe di finestra CS OWNDC quando inizializza il membro di stile della struttura WNDCLASS e chiama la \_ [**funzione RegisterClass.**](/windows/win32/api/winuser/nf-winuser-registerclassa)  [](/windows/win32/api/winuser/ns-winuser-wndclassa) Per altre informazioni sulle classi di finestra, vedere [Classi di finestre.](../winmsg/window-classes.md)

Dopo aver creato una finestra con lo stile CS OWNDC, un'applicazione può chiamare una volta la funzione \_ [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc), [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)o [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) per ottenere un handle che identifica un contesto di dispositivo privato. L'applicazione può continuare a usare questo handle (e il controller di dominio associato) fino a quando non elimina la finestra creata con questa classe. Tutte le modifiche apportate agli oggetti grafici e ai relativi attributi o modalità grafica vengono mantenute dal sistema fino a quando la finestra non viene eliminata.

## <a name="window-device-contexts"></a>Contesti di dispositivo della finestra

Un *contesto di dispositivo della* finestra consente a un'applicazione di disegnare in qualsiasi punto di una finestra, inclusa l'area non client. I contesti di dispositivo della finestra vengono in genere usati dalle applicazioni che elaborano i messaggi [**WM \_ NCPAINT**](wm-ncpaint.md) e [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) per le finestre con aree non client personalizzate. L'uso di un contesto di dispositivo finestra non è consigliato per altri scopi. Per altre informazioni, vedere vedere [**GetWindowDC.**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)

## <a name="parent-device-contexts"></a>Contesti di dispositivo padre

Un *contesto di dispositivo padre* consente a un'applicazione di ridurre al minimo il tempo necessario per configurare l'area di ritaglio per una finestra. Un'applicazione usa in genere contesti di dispositivo padre per velocizzare il disegno per le finestre di controllo senza richiedere un contesto di dispositivo privato o di classe. Ad esempio, il sistema usa contesti di dispositivo padre per il pulsante di comando e i controlli di modifica. I contesti di dispositivo padre sono destinati all'uso solo con le finestre figlio, mai con finestre di primo livello o popup. Per altre informazioni, vedere Vedere [Parent Display Device Contexts (Contesti di dispositivo di visualizzazione padre).](parent-display-device-contexts.md)

 

 
