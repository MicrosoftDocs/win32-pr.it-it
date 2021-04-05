---
description: Le applicazioni che usano le funzioni API Unicode e set di caratteri usano in genere la stessa classe di finestra. Il sistema operativo converte in modo trasparente i messaggi tra le finestre di classi diverse.
ms.assetid: 68e9839b-39f8-411a-8ae4-4a627c667cae
title: Traduzione automatica di messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b02a5c5a4951189333608aa448f09ba9c6866d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751167"
---
# <a name="automatic-message-translation"></a><span data-ttu-id="73d1e-104">Traduzione automatica di messaggi</span><span class="sxs-lookup"><span data-stu-id="73d1e-104">Automatic Message Translation</span></span>

<span data-ttu-id="73d1e-105">Le applicazioni che usano le funzioni API Unicode e set di caratteri usano in genere la stessa classe di finestra.</span><span class="sxs-lookup"><span data-stu-id="73d1e-105">Applications using the Unicode and character set API functions generally use the same window class.</span></span> <span data-ttu-id="73d1e-106">Il sistema operativo converte in modo trasparente i messaggi tra le finestre di classi diverse.</span><span class="sxs-lookup"><span data-stu-id="73d1e-106">The operating system transparently translates messages between windows of different classes.</span></span>

<span data-ttu-id="73d1e-107">Una funzione finestra viene implementata per ricevere messaggi in formato Unicode o tabella codici di Windows.</span><span class="sxs-lookup"><span data-stu-id="73d1e-107">A window function is implemented to receive messages in Unicode or Windows code page format.</span></span> <span data-ttu-id="73d1e-108">La funzione finestra può inviare messaggi o chiamare funzioni di entrambi i tipi.</span><span class="sxs-lookup"><span data-stu-id="73d1e-108">The window function can send messages or call functions of either type.</span></span>

<span data-ttu-id="73d1e-109">I messaggi seguenti contengono argomenti di testo e sono soggetti alla traduzione automatica del testo.</span><span class="sxs-lookup"><span data-stu-id="73d1e-109">The following messages have text arguments and are subject to automatic text translation.</span></span> <span data-ttu-id="73d1e-110">Per informazioni sulla traduzione automatica, vedere la pagina relativa alla [sottoclasse e alla conversione automatica dei messaggi](subclassing-and-automatic-message-translation.md).</span><span class="sxs-lookup"><span data-stu-id="73d1e-110">For information about automatic translation, see [Subclassing and Automatic Message Translation](subclassing-and-automatic-message-translation.md).</span></span>

<dl>

[<span data-ttu-id="73d1e-111">CB \_ ADDSTRING</span><span class="sxs-lookup"><span data-stu-id="73d1e-111">CB\_ADDSTRING</span></span>](../controls/cb-addstring.md)  
[<span data-ttu-id="73d1e-112">DIR della CB \_</span><span class="sxs-lookup"><span data-stu-id="73d1e-112">CB\_DIR</span></span>](../controls/cb-dir.md)  
[<span data-ttu-id="73d1e-113">CB \_ FindString</span><span class="sxs-lookup"><span data-stu-id="73d1e-113">CB\_FINDSTRING</span></span>](../controls/cb-findstring.md)  
[<span data-ttu-id="73d1e-114">CB \_ GETLBTEXT</span><span class="sxs-lookup"><span data-stu-id="73d1e-114">CB\_GETLBTEXT</span></span>](../controls/cb-getlbtext.md)  
[<span data-ttu-id="73d1e-115">CB \_ INSERTSTRING</span><span class="sxs-lookup"><span data-stu-id="73d1e-115">CB\_INSERTSTRING</span></span>](../controls/cb-insertstring.md)  
[<span data-ttu-id="73d1e-116">CB \_ SELECTSTRING</span><span class="sxs-lookup"><span data-stu-id="73d1e-116">CB\_SELECTSTRING</span></span>](../controls/cb-selectstring.md)  
[<span data-ttu-id="73d1e-117">\_riga em</span><span class="sxs-lookup"><span data-stu-id="73d1e-117">EM\_GETLINE</span></span>](../controls/em-getline.md)  
[<span data-ttu-id="73d1e-118">\_REPLACESEL em</span><span class="sxs-lookup"><span data-stu-id="73d1e-118">EM\_REPLACESEL</span></span>](../controls/em-replacesel.md)  
[<span data-ttu-id="73d1e-119">\_SETPASSWORDCHAR em</span><span class="sxs-lookup"><span data-stu-id="73d1e-119">EM\_SETPASSWORDCHAR</span></span>](../controls/em-setpasswordchar.md)  
[<span data-ttu-id="73d1e-120">\_AddFile lb</span><span class="sxs-lookup"><span data-stu-id="73d1e-120">LB\_ADDFILE</span></span>](../controls/lb-addfile.md)  
[<span data-ttu-id="73d1e-121">\_ADDSTRING lb</span><span class="sxs-lookup"><span data-stu-id="73d1e-121">LB\_ADDSTRING</span></span>](../controls/lb-addstring.md)  
[<span data-ttu-id="73d1e-122">\_dir lb</span><span class="sxs-lookup"><span data-stu-id="73d1e-122">LB\_DIR</span></span>](../controls/lb-dir.md)  
[<span data-ttu-id="73d1e-123">\_FindString lb</span><span class="sxs-lookup"><span data-stu-id="73d1e-123">LB\_FINDSTRING</span></span>](../controls/lb-findstring.md)  
[<span data-ttu-id="73d1e-124">GetText LB \_</span><span class="sxs-lookup"><span data-stu-id="73d1e-124">LB\_GETTEXT</span></span>](../controls/lb-gettext.md)  
[<span data-ttu-id="73d1e-125">\_INSERTSTRING lb</span><span class="sxs-lookup"><span data-stu-id="73d1e-125">LB\_INSERTSTRING</span></span>](../controls/lb-insertstring.md)  
[<span data-ttu-id="73d1e-126">\_SELECTSTRING lb</span><span class="sxs-lookup"><span data-stu-id="73d1e-126">LB\_SELECTSTRING</span></span>](../controls/lb-selectstring.md)  
[<span data-ttu-id="73d1e-127">\_ASKCBFORMATNAME WM</span><span class="sxs-lookup"><span data-stu-id="73d1e-127">WM\_ASKCBFORMATNAME</span></span>](../dataxchg/wm-askcbformatname.md)  
[<span data-ttu-id="73d1e-128">\_carattere WM</span><span class="sxs-lookup"><span data-stu-id="73d1e-128">WM\_CHAR</span></span>](../inputdev/wm-char.md)  
[<span data-ttu-id="73d1e-129">\_CHARTOITEM WM</span><span class="sxs-lookup"><span data-stu-id="73d1e-129">WM\_CHARTOITEM</span></span>](../controls/wm-chartoitem.md)  
[<span data-ttu-id="73d1e-130">creazione di WM \_</span><span class="sxs-lookup"><span data-stu-id="73d1e-130">WM\_CREATE</span></span>](../winmsg/wm-create.md)  
[<span data-ttu-id="73d1e-131">\_DEADCHAR WM</span><span class="sxs-lookup"><span data-stu-id="73d1e-131">WM\_DEADCHAR</span></span>](../inputdev/wm-deadchar.md)  
[<span data-ttu-id="73d1e-132">\_DEVMODECHANGE WM</span><span class="sxs-lookup"><span data-stu-id="73d1e-132">WM\_DEVMODECHANGE</span></span>](../gdi/wm-devmodechange.md)  
[<span data-ttu-id="73d1e-133">WM \_ GETtext</span><span class="sxs-lookup"><span data-stu-id="73d1e-133">WM\_GETTEXT</span></span>](../winmsg/wm-gettext.md)  
[<span data-ttu-id="73d1e-134">\_MDICREATE WM</span><span class="sxs-lookup"><span data-stu-id="73d1e-134">WM\_MDICREATE</span></span>](../winmsg/wm-mdicreate.md)  
[<span data-ttu-id="73d1e-135">\_MENUCHAR WM</span><span class="sxs-lookup"><span data-stu-id="73d1e-135">WM\_MENUCHAR</span></span>](../menurc/wm-menuchar.md)  
[<span data-ttu-id="73d1e-136">\_NCCREATE WM</span><span class="sxs-lookup"><span data-stu-id="73d1e-136">WM\_NCCREATE</span></span>](../winmsg/wm-nccreate.md)  
[<span data-ttu-id="73d1e-137">\_testo WM</span><span class="sxs-lookup"><span data-stu-id="73d1e-137">WM\_SETTEXT</span></span>](../winmsg/wm-settext.md)  
[<span data-ttu-id="73d1e-138">\_SYSCHAR WM</span><span class="sxs-lookup"><span data-stu-id="73d1e-138">WM\_SYSCHAR</span></span>](../menurc/wm-syschar.md)  
[<span data-ttu-id="73d1e-139">\_SYSDEADCHAR WM</span><span class="sxs-lookup"><span data-stu-id="73d1e-139">WM\_SYSDEADCHAR</span></span>](../inputdev/wm-sysdeadchar.md)  
[<span data-ttu-id="73d1e-140">\_WININICHANGE WM</span><span class="sxs-lookup"><span data-stu-id="73d1e-140">WM\_WININICHANGE</span></span>](../winmsg/wm-wininichange.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="73d1e-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="73d1e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73d1e-142">Unicode nell'API Windows</span><span class="sxs-lookup"><span data-stu-id="73d1e-142">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
