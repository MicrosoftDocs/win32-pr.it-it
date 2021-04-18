---
description: È possibile utilizzare il controllo InkPicture per eseguire il rendering dell'input penna nelle edizioni di Windows XP per Microsoft Windows 2000, Windows Server 2003 e non Tablet PC. Tuttavia, non è possibile usare il controllo per inserire input penna in questi sistemi operativi.
ms.assetid: e5d00b0f-0a4f-4ea2-ae63-dfb6bc8c2caf
title: Uso di InkPicture nelle versioni precedenti di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbd2bf8545524787c9e37f70c43d954ab440910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306715"
---
# <a name="using-inkpicture-on-earlier-versions-of-windows"></a><span data-ttu-id="ae62d-104">Uso di InkPicture nelle versioni precedenti di Windows</span><span class="sxs-lookup"><span data-stu-id="ae62d-104">Using InkPicture on Earlier Versions of Windows</span></span>

<span data-ttu-id="ae62d-105">È possibile utilizzare il [controllo InkPicture](inkpicture-control.md) per eseguire il rendering dell'input penna nelle edizioni di Windows XP per Microsoft Windows 2000, windows Server 2003 e non Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="ae62d-105">You can use the [InkPicture Control](inkpicture-control.md) to render ink on Microsoft Windows 2000, Windows Server 2003, and non-Tablet PC editions of Windows XP.</span></span> <span data-ttu-id="ae62d-106">Tuttavia, non è possibile usare il controllo per inserire input penna in questi sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="ae62d-106">However, you cannot use the control to input ink on these operating systems.</span></span>

<span data-ttu-id="ae62d-107">La proprietà [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) del controllo è impostata su **false** e il tentativo di modificare la proprietà non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="ae62d-107">The control's [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) property is set to **FALSE**, and attempting to change the property has no effect.</span></span> <span data-ttu-id="ae62d-108">È possibile assegnare valori ad altre proprietà e modificare l'input penna a livello di codice, ma non è possibile usare il controllo per raccogliere input penna.</span><span class="sxs-lookup"><span data-stu-id="ae62d-108">You can assign values to other properties and programmatically manipulate ink, but you cannot use the control to collect ink.</span></span>

 

 



