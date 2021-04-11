---
title: Supporto Unicode per i controlli comuni
description: In questo argomento viene descritto come supportare Unicode per le notifiche di controllo comuni.
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb029d6e1c018f1793c749aefb2f88104559cae
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963580"
---
# <a name="unicode-support-for-common-controls"></a><span data-ttu-id="0a11b-103">Supporto Unicode per i controlli comuni</span><span class="sxs-lookup"><span data-stu-id="0a11b-103">Unicode Support for Common Controls</span></span>

<span data-ttu-id="0a11b-104">In questo argomento viene descritto come supportare Unicode per le notifiche di controllo comuni.</span><span class="sxs-lookup"><span data-stu-id="0a11b-104">This topic describes how to support Unicode for common control notifications.</span></span>


<span data-ttu-id="0a11b-105">Per le versioni 5,80 e successive di comctl32.dll, le notifiche dei controlli comuni supportano i formati ANSI e Unicode nei sistemi Windows 95 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0a11b-105">For versions 5.80 and later of comctl32.dll, common controls notifications support both ANSI and Unicode formats on Windows 95 systems or later.</span></span> <span data-ttu-id="0a11b-106">Il sistema determina il formato da usare inviando alla finestra un messaggio [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) .</span><span class="sxs-lookup"><span data-stu-id="0a11b-106">The system determines which format to use by sending your window a [**WM\_NOTIFYFORMAT**](wm-notifyformat.md) message.</span></span> <span data-ttu-id="0a11b-107">Per specificare un formato, restituire NFR \_ ANSI per le notifiche ANSI o NFR \_ Unicode per le notifiche Unicode.</span><span class="sxs-lookup"><span data-stu-id="0a11b-107">To specify a format, return NFR\_ANSI for ANSI notifications or NFR\_UNICODE for Unicode notifications.</span></span> <span data-ttu-id="0a11b-108">Se non si gestisce questo messaggio, il sistema chiama [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) per determinare il formato.</span><span class="sxs-lookup"><span data-stu-id="0a11b-108">If you do not handle this message, the system calls [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) to determine the format.</span></span> <span data-ttu-id="0a11b-109">Poiché Windows 95 e Windows 98 restituiscono sempre **false** a questa chiamata di funzione, usano le notifiche ANSI per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0a11b-109">Since Windows 95 and Windows 98 always return **FALSE** to this function call, they use ANSI notifications by default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a11b-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a11b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a11b-111">Informazioni sui controlli comuni</span><span class="sxs-lookup"><span data-stu-id="0a11b-111">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 