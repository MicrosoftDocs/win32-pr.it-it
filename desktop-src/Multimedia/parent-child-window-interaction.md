---
title: Interazione della finestra Parent-Child
description: Interazione della finestra Parent-Child
ms.assetid: de10bf12-4ba4-4c6b-be56-489e4e2b26b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da43ab5ebe1aa24d8d67b8c901cd3302d8db48ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725863"
---
# <a name="parent-child-window-interaction"></a><span data-ttu-id="3f4bf-103">Interazione della finestra Parent-Child</span><span class="sxs-lookup"><span data-stu-id="3f4bf-103">Parent-Child Window Interaction</span></span>

<span data-ttu-id="3f4bf-104">Alcuni messaggi a livello di sistema, ad esempio [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) e [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), vengono inviati solo alle finestre di primo livello e sovrapposte.</span><span class="sxs-lookup"><span data-stu-id="3f4bf-104">Some system-level messages, such as [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), are sent only to top-level and overlapped windows.</span></span> <span data-ttu-id="3f4bf-105">Se una finestra di acquisizione è una finestra figlio, è necessario che l'elemento padre inoltri questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="3f4bf-105">If a capture window is a child window, its parent must forward these messages.</span></span>

<span data-ttu-id="3f4bf-106">Analogamente, se la finestra padre cambia dimensione, potrebbe essere necessario inviare messaggi di notifica alla finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="3f4bf-106">Similarly, if the parent window changes size, it might need to send notification messages to the capture window.</span></span> <span data-ttu-id="3f4bf-107">Viceversa, se le dimensioni del video acquisito cambiano, la finestra di acquisizione potrebbe dover inviare messaggi di notifica alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="3f4bf-107">Conversely, if the dimensions of the captured video change, the capture window might need to send notification messages to the parent window.</span></span> <span data-ttu-id="3f4bf-108">Il modo più semplice per gestire questo problema consiste nel lasciare sempre le dimensioni della finestra di acquisizione uguali alle dimensioni del flusso video acquisito, inviando una notifica all'elemento padre ogni volta che queste dimensioni cambiano.</span><span class="sxs-lookup"><span data-stu-id="3f4bf-108">The simplest way to manage this is to always keep the capture window dimensions equal to the size of the captured video stream, notifying the parent whenever these dimensions change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f4bf-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f4bf-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f4bf-110">Acquisisci Windows</span><span class="sxs-lookup"><span data-stu-id="3f4bf-110">Capture Windows</span></span>](capture-windows.md)
</dt> </dl>

 

 