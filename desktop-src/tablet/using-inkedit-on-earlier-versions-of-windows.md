---
description: A causa della mancanza di riconoscitori nelle edizioni non Tablet PC di Microsoft Windows XP, non è possibile utilizzare InkEdit per eseguire il rendering dell'input penna nelle edizioni di Windows XP, Windows 2000, Windows Server 2003 e non Tablet PC e non è possibile utilizzare il controllo per inserire input penna in questi sistemi operativi.
ms.assetid: eb80ff91-5c09-43d1-afd4-6391097000c1
title: Utilizzo di InkEdit nelle versioni precedenti di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08343b3d379a3f45985b1f586254e7a370998f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306716"
---
# <a name="using-inkedit-on-earlier-versions-of-windows"></a><span data-ttu-id="f9322-103">Utilizzo di InkEdit nelle versioni precedenti di Windows</span><span class="sxs-lookup"><span data-stu-id="f9322-103">Using InkEdit on Earlier Versions of Windows</span></span>

<span data-ttu-id="f9322-104">A causa della mancanza di riconoscitori nelle edizioni non Tablet PC di Microsoft Windows XP, non è possibile utilizzare [InkEdit](inkedit-control.md) per eseguire il rendering dell'input penna nelle edizioni di Windows XP, Windows 2000, windows Server 2003 e non Tablet PC e non è possibile utilizzare il controllo per inserire input penna in questi sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="f9322-104">Because of the lack of recognizers on non-Tablet PC editions of Microsoft Windows XP, you cannot use [InkEdit](inkedit-control.md) to render ink on Windows 2000, Windows Server 2003, and non-Tablet PC editions of Windows XP, and you cannot use the control to input ink on these operating systems.</span></span>

<span data-ttu-id="f9322-105">La proprietà [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) del controllo è impostata su **disabled** (**IEM \_ disabled** per C++) e il tentativo di modificare la proprietà non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="f9322-105">The control's [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property is set to **Disabled** (**IEM\_Disabled** for C++), and attempting to change the property has no effect.</span></span> <span data-ttu-id="f9322-106">È possibile assegnare valori ad altre proprietà e copiare e incollare l'input penna in altre applicazioni, ma non è possibile utilizzare il controllo per accettare movimenti o raccogliere input penna.</span><span class="sxs-lookup"><span data-stu-id="f9322-106">You can assign values to other properties and copy and paste ink to other applications, but you cannot use the control to accept gestures or collect ink.</span></span>

 

 



