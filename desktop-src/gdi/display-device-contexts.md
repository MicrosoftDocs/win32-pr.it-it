---
description: Un'applicazione ottiene un controller di dominio di visualizzazione chiamando la funzione BeginPaint, GetDC o GetDCEx e identificando la finestra in cui verrà visualizzato l'output corrispondente.
ms.assetid: 8f952d68-ee52-4e63-9f09-80a14c755d31
title: Visualizzare i contesti di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d0eeb3055209ad99a6a50fd129f9f9c064bf52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754447"
---
# <a name="display-device-contexts"></a>Visualizzare i contesti di dispositivo

Un'applicazione ottiene un controller di dominio di visualizzazione chiamando la funzione [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) e identificando la finestra in cui verrà visualizzato l'output corrispondente. In genere, un'applicazione ottiene un controller di dominio di visualizzazione solo quando deve essere disegnato nell'area client. Tuttavia, è possibile ottenere un [contesto di dispositivo della finestra](#window-device-contexts) chiamando la funzione [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) . Al termine del disegno, l'applicazione deve rilasciare il controller di dominio chiamando la funzione [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) o [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) .

Sono disponibili cinque tipi di controller di dominio per le visualizzazioni video:

-   Classe
-   Comuni
-   Privato
-   Finestra
-   Padre

## <a name="class-device-contexts"></a>Contesti di dispositivo di classe

I *contesti di dispositivo di classe* sono supportati rigorosamente per la compatibilità con le versioni di Windows a 16 bit. Quando si scrive l'applicazione, evitare di usare il contesto di dispositivo della classe; usare invece un contesto di dispositivo privato.

## <a name="common-device-contexts"></a>Contesti di dispositivo comuni

Per i *contesti di dispositivo comuni* vengono visualizzati i controller di dominio gestiti in una cache speciale dal sistema. I contesti di dispositivo comuni vengono usati nelle applicazioni che eseguono operazioni di disegno non frequenti. Prima che il sistema restituisca l'handle del controller di dominio, Inizializza il contesto di dispositivo comune con gli oggetti, gli attributi e le modalità predefiniti. Tutte le operazioni di disegno eseguite dall'applicazione utilizzano queste impostazioni predefinite a meno che non venga chiamata una delle funzioni GDI per selezionare un nuovo oggetto, modificare gli attributi di un oggetto esistente o selezionare una nuova modalità.

Poiché esiste solo un numero limitato di contesti di dispositivo comuni, un'applicazione deve rilasciarli dopo aver completato il disegno. Quando l'applicazione rilascia un contesto di dispositivo comune, tutte le modifiche apportate ai dati predefiniti vengono perse.

## <a name="private-device-contexts"></a>Contesti di dispositivi privati

I *contesti di dispositivi privati* sono i controller di dominio che, a differenza dei contesti di dispositivo comuni, conservano le modifiche ai dati predefiniti anche dopo che sono stati rilasciati da un'applicazione. I contesti di dispositivi privati vengono utilizzati nelle applicazioni che eseguono numerose operazioni di disegno, ad esempio applicazioni CAD (computer-aided design), applicazioni di pubblicazione desktop, applicazioni di disegno e disegno e così via. I contesti di dispositivo privati non fanno parte della cache di sistema e pertanto non devono essere rilasciati dopo l'utilizzo. Il sistema rimuove automaticamente un contesto di dispositivo privato dopo che l'ultima finestra di tale classe è stata eliminata definitivamente.

Un'applicazione crea un contesto di dispositivo privato specificando prima di \_ tutto lo stile della classe della finestra CS OWNDC Quando Inizializza il membro dello **stile** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) e chiama la funzione [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . Per ulteriori informazioni sulle classi della finestra, vedere [classi di finestra](../winmsg/window-classes.md).

Dopo la creazione di una finestra con lo \_ stile cs OWNDC, un'applicazione può chiamare la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc), [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)o [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) una volta per ottenere un handle che identifica un contesto di dispositivo privato. L'applicazione può continuare a usare questo handle (e il controller di dominio associato) finché non elimina la finestra creata con questa classe. Tutte le modifiche apportate agli oggetti grafici e ai relativi attributi, o modalità grafica, vengono conservate dal sistema fino a quando la finestra non viene eliminata.

## <a name="window-device-contexts"></a>Contesti di dispositivo finestra

Un *contesto di dispositivo finestra* consente a un'applicazione di creare qualsiasi punto in una finestra, inclusa l'area non client. I contesti di dispositivo Windows vengono in genere usati da applicazioni che elaborano i messaggi [**WM \_ NCPAINT**](wm-ncpaint.md) e [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) per Windows con aree non client personalizzate. L'uso di un contesto di dispositivo Windows non è consigliato per altri scopi. Per ulteriori informazioni, vedere [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc).

## <a name="parent-device-contexts"></a>Contesti di dispositivo padre

Un *contesto di dispositivo padre* consente a un'applicazione di ridurre al minimo il tempo necessario per configurare l'area di visualizzazione per una finestra. Un'applicazione usa in genere i contesti di dispositivo padre per velocizzare il disegno per le finestre di controllo senza richiedere un contesto di dispositivo privato o di classe. Ad esempio, il sistema usa i contesti di dispositivo padre per i pulsanti di comando e di modifica. I contesti di dispositivo padre sono destinati all'uso solo con le finestre figlio, mai con finestre popup o di primo livello. Per ulteriori informazioni, vedere [contesti di dispositivo di visualizzazione padre](parent-display-device-contexts.md).

 

 
