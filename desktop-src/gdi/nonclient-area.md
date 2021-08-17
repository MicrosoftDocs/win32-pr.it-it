---
description: Il sistema invia un messaggio WM NCPAINT alla finestra ogni volta che è necessario aggiornare una parte dell'area non client della finestra, ad esempio la barra del titolo, la barra dei menu o la cornice \_ della finestra.
ms.assetid: e4dc61f3-6a9f-4ed4-8685-62eb4ceb85f1
title: Area non client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a20593063af4382e79697b249324ba0fd6fe2782d903b645a2b80c25c63c436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698740"
---
# <a name="nonclient-area"></a>Area non client

Il sistema invia un messaggio [**WM \_ NCPAINT**](wm-ncpaint.md) alla finestra ogni volta che è necessario aggiornare una parte dell'area non client della finestra, ad esempio la barra del titolo, la barra dei menu o la cornice della finestra. Il sistema può anche inviare altri messaggi per indirizzare una finestra per aggiornare una parte della relativa area client. Ad esempio, quando una finestra diventa attiva o inattiva, invia il [**messaggio WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) per aggiornare la barra del titolo. In generale, l'elaborazione di questi messaggi per le finestre standard non è consigliata, perché l'applicazione deve essere in grado di disegnare tutte le parti necessarie dell'area non client per la finestra. Per questo motivo, la maggior parte delle applicazioni passa questi messaggi a [**DefWindowProc per l'elaborazione**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) predefinita.

Un'applicazione che crea aree non client personalizzate per le finestre deve elaborare questi messaggi. In questo caso, l'applicazione deve usare un contesto di dispositivo della finestra per eseguire il disegno nella finestra. Il *contesto di dispositivo della* finestra consente all'applicazione di disegnare in tutte le parti della finestra, inclusa l'area non client. Un'applicazione recupera un contesto di dispositivo della finestra usando la [**funzione GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) e, al termine del disegno, deve rilasciare il contesto di dispositivo della finestra usando la [**funzione ReleaseDC.**](/windows/desktop/api/Winuser/nf-winuser-releasedc)

Il sistema gestisce un'area di aggiornamento per l'area non client. Quando un'applicazione riceve un [**messaggio WM \_ NCPAINT,**](wm-ncpaint.md) il *parametro wParam* contiene un handle per un'area che definisce le dimensioni dell'area di aggiornamento. L'applicazione può usare l'handle per combinare l'area di aggiornamento con l'area di ritaglio per il contesto di dispositivo della finestra. Il sistema non combina automaticamente l'area di aggiornamento durante il recupero del contesto di dispositivo della finestra, a meno che l'applicazione non usi [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) e non specifichi sia l'handle di area che il flag DCX \_ INTERSECTRGN. Se l'applicazione non combina l'area di aggiornamento, vengono ritagliate solo le operazioni di disegno che altrimenti si estenderebbero all'esterno della finestra. L'applicazione non è responsabile della cancellazione dell'area di aggiornamento, indipendentemente dal fatto che usi l'area.

Se un'applicazione elabora il [**messaggio WM \_ NCACTIVATE,**](../winmsg/wm-ncactivate.md) dopo l'elaborazione deve restituire **TRUE** per indirizzare il sistema a completare la modifica della finestra attiva. Se la finestra è ridotta a icona quando l'applicazione riceve il messaggio **WM \_ NCACTIVATE,** deve passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). In questi casi, la funzione predefinita ridisegna l'etichetta per l'icona.

 

 
