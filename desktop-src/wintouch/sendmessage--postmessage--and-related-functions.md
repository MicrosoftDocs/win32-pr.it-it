---
title: Funzioni sendMessage, PostMessage e correlate
description: Questa sezione descrive le considerazioni sull'inoltro dei messaggi usando SendMessage, PostMessage e le funzioni correlate con i messaggi tramite tocco.
ms.assetid: 9fba2013-17a3-499c-80dc-627e89c0edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1274327b53630058779bc3913ce4466394c4c4fa37ba78528d122b8d68e376e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435299"
---
# <a name="sendmessage-postmessage-and-related-functions"></a>Funzioni sendMessage, PostMessage e correlate

In questa sezione vengono descritte alcune considerazioni sull'inoltro dei messaggi tramite [SendMessage,](/windows/desktop/api/winuser/nf-winuser-sendmessage) [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)e le funzioni correlate con i messaggi tramite tocco.

Se un messaggio tocco viene inoltrato usando [SendMessage,](/windows/desktop/api/winuser/nf-winuser-sendmessage) [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)o un'altra funzione correlata, l'handle di input tocco viene chiuso. Se sono state recuperate le informazioni contenute a cui fa riferimento un handle di input tocco tramite una chiamata a [**GetTouchInputInfo,**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)i dati rimarranno validi fino a quando non si libera la memoria.

Un'applicazione che riceve messaggi di tocco inoltrati tramite uno di questi meccanismi è proprietaria dell'handle di input tocco ricevuto nel messaggio *LPARAM* ed è responsabile della chiusura. Se non si chiude l'handle con una chiamata a [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), si passa il messaggio a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)o si inoltra il messaggio usando [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)o una funzione correlata, si avrà una perdita di memoria.

> [!Note]  
> I messaggi touch sono soggetti alle normali regole di isolamento dei Interfaccia utente (UIPI) quando vengono inoltrati.

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a>Funzioni correlate a SendMessage e PostMessage

Le funzioni seguenti possono influire sullo stato dell'handle di input tocco.

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

 

 