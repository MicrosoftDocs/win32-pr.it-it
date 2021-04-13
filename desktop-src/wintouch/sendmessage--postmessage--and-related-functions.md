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
# <a name="sendmessage-postmessage-and-related-functions"></a><span data-ttu-id="2d5c4-103">SendMessage, PostMessage e funzioni correlate</span><span class="sxs-lookup"><span data-stu-id="2d5c4-103">SendMessage, PostMessage, and Related Functions</span></span>

<span data-ttu-id="2d5c4-104">In questa sezione vengono descritte le considerazioni sull'invio di messaggi tramite [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)e funzioni correlate con i messaggi touch.</span><span class="sxs-lookup"><span data-stu-id="2d5c4-104">This section describes considerations about forwarding messages using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), and related functions with touch messages.</span></span>

<span data-ttu-id="2d5c4-105">Se un messaggio tocco viene inviato utilizzando [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)o un'altra funzione correlata, l'handle di input tocco viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="2d5c4-105">If a touch message is forwarded using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), or some other related function, the touch input handle is closed.</span></span> <span data-ttu-id="2d5c4-106">Se sono state recuperate le informazioni contenute a cui fa riferimento un handle di input tocco tramite una chiamata a [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), i dati rimarranno validi fino a quando non si libera la memoria.</span><span class="sxs-lookup"><span data-stu-id="2d5c4-106">If you have retrieved the information contained referenced by a touch input handle through a call to [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), that data will remain valid until you free the memory.</span></span>

<span data-ttu-id="2d5c4-107">Un'applicazione che riceve i messaggi di tocco inoltrati tramite uno di questi meccanismi è proprietaria dell'handle di input tocco che riceve nel messaggio *lParam* ed è responsabile della chiusura.</span><span class="sxs-lookup"><span data-stu-id="2d5c4-107">An application that receives touch messages forwarded through one of these mechanisms owns the touch input handle it receives in the message *LPARAM* and is responsible for closing it.</span></span> <span data-ttu-id="2d5c4-108">Se non si chiude l'handle con una chiamata a [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), si passa il messaggio a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)o si inoltra il messaggio usando [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)o una funzione correlata, si disporrà di una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="2d5c4-108">If you don't close the handle with a call to [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), pass the message to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), or forward the message using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), or some related function, you will have a memory leak.</span></span>

> [!Note]  
> <span data-ttu-id="2d5c4-109">I messaggi di tocco sono soggetti alle normali regole di isolamento dei privilegi di interfaccia utente (UIPI) al momento dell'invio.</span><span class="sxs-lookup"><span data-stu-id="2d5c4-109">Touch messages are subject to normal User Interface Privilege Isolation (UIPI) rules when they are forwarded.</span></span>

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a><span data-ttu-id="2d5c4-110">Funzioni correlate a SendMessage e PostMessage</span><span class="sxs-lookup"><span data-stu-id="2d5c4-110">Functions related to SendMessage and PostMessage</span></span>

<span data-ttu-id="2d5c4-111">Le funzioni seguenti che possono influire sullo stato dell'handle di input tocco.</span><span class="sxs-lookup"><span data-stu-id="2d5c4-111">The following functions that can affect the state of the touch input handle.</span></span>

-   [<span data-ttu-id="2d5c4-112">SendMessage</span><span class="sxs-lookup"><span data-stu-id="2d5c4-112">SendMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
-   [<span data-ttu-id="2d5c4-113">PostMessage</span><span class="sxs-lookup"><span data-stu-id="2d5c4-113">PostMessage</span></span>](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   <span data-ttu-id="2d5c4-114">SendNotifyMessage</span><span class="sxs-lookup"><span data-stu-id="2d5c4-114">SendNotifyMessage</span></span>
-   <span data-ttu-id="2d5c4-115">SendMessageCallback</span><span class="sxs-lookup"><span data-stu-id="2d5c4-115">SendMessageCallback</span></span>
-   <span data-ttu-id="2d5c4-116">SendMessageTimeout</span><span class="sxs-lookup"><span data-stu-id="2d5c4-116">SendMessageTimeout</span></span>
-   <span data-ttu-id="2d5c4-117">PostThreadMessage</span><span class="sxs-lookup"><span data-stu-id="2d5c4-117">PostThreadMessage</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d5c4-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d5c4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d5c4-119">Funzioni</span><span class="sxs-lookup"><span data-stu-id="2d5c4-119">Functions</span></span>](mtfunctions.md)
</dt> <dt>

[<span data-ttu-id="2d5c4-120">DefWindowProc</span><span class="sxs-lookup"><span data-stu-id="2d5c4-120">DefWindowProc</span></span>](/windows/win32/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

 