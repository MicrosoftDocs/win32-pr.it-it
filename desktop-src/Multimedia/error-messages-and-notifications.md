---
title: Messaggi di errore e notifiche
description: Messaggi di errore e notifiche
ms.assetid: 7f804364-d8be-4e52-ab0e-fba05bcf76ce
keywords:
- MCIWndGetError (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e40e78c72dc378baa37b56dbb2d5718ae2d85b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046640"
---
# <a name="error-messages-and-notifications"></a>Messaggi di errore e notifiche

MCIWnd USA MCI per controllare i dispositivi che riproducono e registrano i dati multimediali. In generale, MCIWnd Visualizza gli errori di MCI in una finestra di dialogo di errore. Un errore MCI viene generato ogni volta che un comando MCI ha esito negativo. Ad esempio, se l'applicazione tenta di riprendere la riproduzione sospesa usando la macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) e il dispositivo corrente non supporta la ripresa, viene restituito un errore all'utente.

MCIWnd consente due opzioni per la gestione dei messaggi di errore:

-   È possibile impedire che i messaggi di errore raggiungano l'utente. Per evitare la visualizzazione di messaggi di errore MCI, specificare lo \_ stile della finestra MCIWNDF NOERRORDLG quando si crea un'istanza di una finestra MCIWnd usando la funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) o [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) .
-   È possibile reindirizzarli all'applicazione per la visualizzazione. Per reindirizzare i messaggi di errore di MCI all'applicazione, specificare lo \_ stile della finestra MCIWNDF NOTIFYERROR quando si crea un'istanza di una finestra MCIWnd usando **MCIWndCreate** o **CreateWindowEx**.

Quando è abilitata la notifica degli errori, MCIWnd invia ogni messaggio di notifica ([**MCIWNDM \_ NOTIFYERROR**](mciwndm-notifyerror.md)) al gestore di messaggi principale dell'elemento padre della finestra MCIWnd. Per elaborare i messaggi di notifica ricevuti, l'applicazione deve disporre di un gestore di messaggi.

È possibile ottenere una descrizione testuale del messaggio di errore MCI più recente utilizzando la macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) . Questa macro restituisce il testo in un buffer definito dall'applicazione. Se la stringa di errore è più lunga del buffer, MCIWnd tronca la stringa.

È possibile instradare tutte le notifiche a un'altra finestra usando la macro [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .

 

 