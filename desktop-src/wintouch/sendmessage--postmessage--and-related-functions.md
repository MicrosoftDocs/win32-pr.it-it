---
title: SendMessage, PostMessage e funzioni correlate
description: In questa sezione vengono descritte le considerazioni sull'invio di messaggi tramite SendMessage, PostMessage e funzioni correlate con i messaggi touch.
ms.assetid: 9fba2013-17a3-499c-80dc-627e89c0edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fc42e31f3c971c704d18f04a961fb6bd40eb91d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399346"
---
# <a name="sendmessage-postmessage-and-related-functions"></a>SendMessage, PostMessage e funzioni correlate

In questa sezione vengono descritte le considerazioni sull'invio di messaggi tramite [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)e funzioni correlate con i messaggi touch.

Se un messaggio tocco viene inviato utilizzando [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)o un'altra funzione correlata, l'handle di input tocco viene chiuso. Se sono state recuperate le informazioni contenute a cui fa riferimento un handle di input tocco tramite una chiamata a [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), i dati rimarranno validi fino a quando non si libera la memoria.

Un'applicazione che riceve i messaggi di tocco inoltrati tramite uno di questi meccanismi è proprietaria dell'handle di input tocco che riceve nel messaggio *lParam* ed è responsabile della chiusura. Se non si chiude l'handle con una chiamata a [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), si passa il messaggio a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)o si inoltra il messaggio usando [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)o una funzione correlata, si disporrà di una perdita di memoria.

> [!Note]  
> I messaggi di tocco sono soggetti alle normali regole di isolamento dei privilegi di interfaccia utente (UIPI) al momento dell'invio.

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a>Funzioni correlate a SendMessage e PostMessage

Le funzioni seguenti che possono influire sullo stato dell'handle di input tocco.

-   [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)
-   [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   SendNotifyMessage
-   SendMessageCallback
-   SendMessageTimeout
-   PostThreadMessage

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni](mtfunctions.md)
</dt> <dt>

[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

 