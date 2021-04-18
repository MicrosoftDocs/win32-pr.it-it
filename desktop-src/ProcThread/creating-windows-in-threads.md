---
description: Qualsiasi thread può creare una finestra.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: Creazione di finestre nei thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebcde45ca37696b6dbc90e639f630a689498b04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311990"
---
# <a name="creating-windows-in-threads"></a><span data-ttu-id="74230-103">Creazione di finestre nei thread</span><span class="sxs-lookup"><span data-stu-id="74230-103">Creating Windows in Threads</span></span>

<span data-ttu-id="74230-104">Qualsiasi thread può creare una finestra.</span><span class="sxs-lookup"><span data-stu-id="74230-104">Any thread can create a window.</span></span> <span data-ttu-id="74230-105">Il thread che crea la finestra è proprietario della finestra e della coda di messaggi associata.</span><span class="sxs-lookup"><span data-stu-id="74230-105">The thread that creates the window owns the window and its associated message queue.</span></span> <span data-ttu-id="74230-106">Pertanto, il thread deve fornire un ciclo di messaggi per elaborare i messaggi nella coda di messaggi.</span><span class="sxs-lookup"><span data-stu-id="74230-106">Therefore, the thread must provide a message loop to process the messages in its message queue.</span></span> <span data-ttu-id="74230-107">Inoltre, è necessario utilizzare [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) o [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) in tale thread, anziché le altre funzioni di [attesa](/windows/desktop/Sync/wait-functions), in modo che sia in grado di elaborare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="74230-107">In addition, you must use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) or [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) in that thread, rather than the other [wait functions](/windows/desktop/Sync/wait-functions), so that it can process messages.</span></span> <span data-ttu-id="74230-108">In caso contrario, il sistema può diventare un deadlock quando il thread riceve un messaggio mentre è in attesa.</span><span class="sxs-lookup"><span data-stu-id="74230-108">Otherwise, the system can become deadlocked when the thread is sent a message while it is waiting.</span></span>

<span data-ttu-id="74230-109">La funzione [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) può essere usata per consentire a un set di thread di condividere lo stesso stato di input.</span><span class="sxs-lookup"><span data-stu-id="74230-109">The [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) function can be used to allow a set of threads to share the same input state.</span></span> <span data-ttu-id="74230-110">Condividendo lo stato di input, i thread condividono il concetto della finestra attiva.</span><span class="sxs-lookup"><span data-stu-id="74230-110">By sharing input state, the threads share their concept of the active window.</span></span> <span data-ttu-id="74230-111">In questo, un thread può sempre attivare la finestra di un altro thread.</span><span class="sxs-lookup"><span data-stu-id="74230-111">By doing this, one thread can always activate another thread's window.</span></span> <span data-ttu-id="74230-112">Questa funzione è utile anche per condividere lo stato attivo, lo stato di acquisizione del mouse, lo stato della tastiera e lo stato dell'ordine Z della finestra tra le finestre create da thread diversi il cui stato di input è condiviso.</span><span class="sxs-lookup"><span data-stu-id="74230-112">This function is also useful for sharing focus state, mouse capture state, keyboard state, and window Z-order state among windows created by different threads whose input state is shared.</span></span>

<span data-ttu-id="74230-113">Per informazioni sulla creazione di Windows, vedere [classi di Windows](../winmsg/window-classes.md).</span><span class="sxs-lookup"><span data-stu-id="74230-113">For information about creating windows, see [Windows Classes](../winmsg/window-classes.md).</span></span>

 

 
