---
description: Un'applicazione esegue l'hit test sulle aree per determinare le coordinate della posizione corrente del cursore.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Aree di hit testing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe136c3ba9ab4babfc1150ae4c3eee878cb42327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226691"
---
# <a name="hit-testing-regions"></a><span data-ttu-id="e4186-103">Aree di hit testing</span><span class="sxs-lookup"><span data-stu-id="e4186-103">Hit Testing Regions</span></span>

<span data-ttu-id="e4186-104">Un'applicazione esegue l'hit test sulle aree per determinare le coordinate della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="e4186-104">An application performs hit testing on regions to determine the coordinates of the current cursor position.</span></span> <span data-ttu-id="e4186-105">Passa quindi queste coordinate e un handle che identifica l'area alla funzione [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) .</span><span class="sxs-lookup"><span data-stu-id="e4186-105">Then it passes these coordinates as well as a handle identifying the region to the [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) function.</span></span> <span data-ttu-id="e4186-106">Le coordinate del cursore possono essere recuperate elaborando i vari messaggi del mouse, ad esempio [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) , [**WM \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) , [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) e [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md).</span><span class="sxs-lookup"><span data-stu-id="e4186-106">The cursor coordinates can be retrieved by processing the various mouse messages, such as [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) , [**WM\_LBUTTONUP**](../inputdev/wm-lbuttonup.md) , [**WM\_RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) , and [**WM\_RBUTTONUP**](../inputdev/wm-rbuttonup.md).</span></span> <span data-ttu-id="e4186-107">Il valore restituito per PtInRegion indica se la posizione del cursore si trova all'interno dell'area specificata.</span><span class="sxs-lookup"><span data-stu-id="e4186-107">The return value for PtInRegion indicates whether the cursor position is within the given region.</span></span>

 

 
