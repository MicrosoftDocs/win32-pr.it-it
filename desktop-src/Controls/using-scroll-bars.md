---
title: Uso delle barre di scorrimento
description: Questa sezione contiene argomenti che illustrano come creare barre di scorrimento.
ms.assetid: 45ffb56f-f567-40d7-8172-e64e26744ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d602426bd5f716a380d43104046f330d3240d516
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047454"
---
# <a name="using-scroll-bars"></a>Uso delle barre di scorrimento

Questa sezione contiene argomenti che illustrano come creare barre di scorrimento.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Come creare barre di scorrimento](create-scroll-bars.md)<br/>                                                                     | Quando si crea una finestra sovrapposta, popup o figlio, è possibile aggiungere barre di scorrimento standard usando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificando WS \_ HSCROLL, WS \_ VSCROLL o entrambi gli stili. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Come scorrere il testo](scroll-text-in-scroll-bars.md)<br/>                                                                    | In questa sezione vengono descritte le modifiche che è possibile apportare alla routine della finestra principale di un'applicazione per consentire a un utente di scorrere il testo. L'esempio in questa sezione Crea e visualizza una matrice di stringhe di testo ed elabora i messaggi della barra di scorrimento [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) in modo che l'utente possa scorrere il testo in senso verticale e orizzontale. <br/>                                                                                                                                                                                                                                                                 |
| [Come scorrere una bitmap](scroll-a-bitmap-in-scroll-bars.md)<br/>                                                            | In questa sezione vengono descritte le modifiche che è possibile apportare alla routine della finestra principale di un'applicazione per consentire all'utente di scorrere una bitmap. <br/> Nell'esempio è inclusa una voce di menu che copia il contenuto della schermata in una bitmap e visualizza la bitmap nell'area client. Nell'esempio vengono inoltre elaborati i messaggi [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md) generati dalle barre di scorrimento in modo che l'utente possa scorrere la bitmap orizzontalmente e verticalmente. A differenza dell'esempio relativo al testo a scorrimento, l'esempio bitmap usa la funzione [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) per creare la parte non valida dell'area client. <br/> |
| [Come creare un'interfaccia della tastiera per le barre di scorrimento standard](create-a-keyboard-interface-for-standard-scroll-bars.md)<br/> | Anche se un controllo barra di scorrimento fornisce un'interfaccia di tastiera incorporata, non è presente una barra di scorrimento standard. Per implementare un'interfaccia della tastiera per una barra di scorrimento standard, una routine della finestra deve elaborare il messaggio di [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) ed esaminare il codice della chiave virtuale specificato dal parametro *wParam* . Se il codice della chiave virtuale corrisponde a un tasto di direzione, la routine della finestra Invia a se stessa un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con la parola meno ordinata del parametro *wParam* impostato sul codice di richiesta della barra di scorrimento appropriato. <br/>                                              |



 

 

