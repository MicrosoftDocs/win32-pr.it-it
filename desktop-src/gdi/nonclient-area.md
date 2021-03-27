---
description: Il sistema invia un \_ messaggio WM NCPAINT alla finestra ogni volta che è necessario aggiornare una parte dell'area non client della finestra, ad esempio la barra del titolo, la barra dei menu o la cornice della finestra.
ms.assetid: e4dc61f3-6a9f-4ed4-8685-62eb4ceb85f1
title: Area non client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51da31709f5bd9326cc0d05a9e37e2df78bfbb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226680"
---
# <a name="nonclient-area"></a>Area non client

Il sistema invia un messaggio [**WM \_ NCPAINT**](wm-ncpaint.md) alla finestra ogni volta che è necessario aggiornare una parte dell'area non client della finestra, ad esempio la barra del titolo, la barra dei menu o la cornice della finestra. Il sistema può anche inviare altri messaggi per indicare a una finestra di aggiornare una parte della relativa area client; ad esempio, quando una finestra diventa attiva o inattiva, invia il messaggio [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) per aggiornare la relativa barra del titolo. In generale, non è consigliabile elaborare questi messaggi per le finestre standard, perché l'applicazione deve essere in grado di creare tutte le parti necessarie dell'area non client per la finestra. Per questo motivo, la maggior parte delle applicazioni passa questi messaggi a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per l'elaborazione predefinita.

Un'applicazione che crea aree non client personalizzate per le finestre deve elaborare questi messaggi. Quando si esegue questa operazione, l'applicazione deve usare un contesto di dispositivo della finestra per eseguire il disegno nella finestra. Il *contesto di dispositivo della finestra* consente all'applicazione di creare tutte le parti della finestra, inclusa l'area non client. Un'applicazione recupera un contesto di dispositivo della finestra usando la funzione [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) e, al termine del disegno, deve rilasciare il contesto di dispositivo della finestra usando la funzione [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) .

Il sistema mantiene un'area di aggiornamento per l'area non client. Quando un'applicazione riceve un messaggio [**WM \_ NCPAINT**](wm-ncpaint.md) , il parametro *wParam* contiene un handle per un'area che definisce le dimensioni dell'area di aggiornamento. L'applicazione può usare l'handle per combinare l'area di aggiornamento con l'area di ridimensionamento per il contesto di dispositivo della finestra. Il sistema non combina automaticamente l'area di aggiornamento durante il recupero del contesto di dispositivo della finestra, a meno che l'applicazione non usi [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) e specifichi sia l'handle dell'area sia il \_ flag DCX INTERSECTRGN. Se l'applicazione non combina l'area di aggiornamento, verranno ritagliate solo le operazioni di disegno che altrimenti si estendono all'esterno della finestra. L'applicazione non è responsabile della cancellazione dell'area di aggiornamento, indipendentemente dal fatto che usi l'area.

Se un'applicazione elabora il messaggio [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) , dopo l'elaborazione deve restituire **true** per indicare al sistema di completare la modifica della finestra attiva. Se la finestra è ridotta a icona quando l'applicazione riceve il messaggio **WM \_ NCACTIVATE** , deve passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). In questi casi, la funzione predefinita ridisegnato l'etichetta per l'icona.

 

 
