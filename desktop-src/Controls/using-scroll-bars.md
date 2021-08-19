---
title: Uso delle barre di scorrimento
description: Questa sezione contiene argomenti che illustrano come creare barre di scorrimento.
ms.assetid: 45ffb56f-f567-40d7-8172-e64e26744ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96b1341e76b80e4ba5bf45df3dcfee03db87bb82adb4ba50273edbac6db4ac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957590"
---
# <a name="using-scroll-bars"></a>Uso delle barre di scorrimento

Questa sezione contiene argomenti che illustrano come creare barre di scorrimento.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Come creare barre di scorrimento](create-scroll-bars.md)<br/>                                                                     | Quando si crea una finestra sovrapposta, popup o figlio, è possibile aggiungere barre di scorrimento standard usando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificando WS \_ HSCROLL, WS VSCROLL o entrambi gli \_ stili. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Come scorrere il testo](scroll-text-in-scroll-bars.md)<br/>                                                                    | Questa sezione descrive le modifiche che è possibile apportare alla procedura della finestra principale di un'applicazione per consentire a un utente di scorrere il testo. L'esempio in questa sezione crea e visualizza una matrice di stringhe di testo ed elabora i messaggi della barra di scorrimento [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) in modo che l'utente possa scorrere il testo sia verticalmente che orizzontalmente. <br/>                                                                                                                                                                                                                                                                 |
| [Come scorrere una bitmap](scroll-a-bitmap-in-scroll-bars.md)<br/>                                                            | Questa sezione descrive le modifiche che è possibile apportare alla procedura della finestra principale di un'applicazione per consentire all'utente di scorrere una bitmap. <br/> L'esempio include una voce di menu che copia il contenuto dello schermo in una bitmap e visualizza la bitmap nell'area client. L'esempio elabora anche i messaggi [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) generati dalle barre di scorrimento in modo che l'utente possa scorrere la bitmap orizzontalmente e verticalmente. A differenza dell'esempio di testo scorretto, l'esempio bitmap usa la [**funzione BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) per disegnare la parte non valida dell'area client. <br/> |
| [Come creare un'interfaccia della tastiera per le barre di scorrimento standard](create-a-keyboard-interface-for-standard-scroll-bars.md)<br/> | Anche se un controllo barra di scorrimento fornisce un'interfaccia della tastiera predefinita, una barra di scorrimento standard non lo fornisce. Per implementare un'interfaccia della tastiera per una barra di scorrimento standard, una routine della finestra deve elaborare il messaggio [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) ed esaminare il codice del tasto virtuale specificato dal *parametro wParam.* Se il codice del tasto virtuale corrisponde a un tasto di direzione, la routine della finestra invia a se stessa un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con la parola di ordine inferiore del parametro *wParam* impostata sul codice di richiesta della barra di scorrimento appropriato. <br/>                                              |



 

 

