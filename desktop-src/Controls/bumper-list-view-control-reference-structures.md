---
title: Strutture di visualizzazione elenco
description: Strutture di visualizzazione elenco
ms.assetid: 12d77514-7281-4873-b456-252ff80ed7f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b603e9acd65448b3c4970aa9552f4d2b91ebccd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761716"
---
# <a name="list-view-structures"></a><span data-ttu-id="03ccc-103">Strutture di visualizzazione elenco</span><span class="sxs-lookup"><span data-stu-id="03ccc-103">List View Structures</span></span>

## <a name="in-this-section"></a><span data-ttu-id="03ccc-104">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="03ccc-104">In This Section</span></span>

-   [<span data-ttu-id="03ccc-105">**LVBKIMAGE**</span><span class="sxs-lookup"><span data-stu-id="03ccc-105">**LVBKIMAGE**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea)
-   [<span data-ttu-id="03ccc-106">**LVCOLUMN**</span><span class="sxs-lookup"><span data-stu-id="03ccc-106">**LVCOLUMN**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvcolumna)
-   [<span data-ttu-id="03ccc-107">**LVFINDINFO**</span><span class="sxs-lookup"><span data-stu-id="03ccc-107">**LVFINDINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa)
-   [<span data-ttu-id="03ccc-108">**LVFOOTERINFO**</span><span class="sxs-lookup"><span data-stu-id="03ccc-108">**LVFOOTERINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo)
-   [<span data-ttu-id="03ccc-109">**LVFOOTERITEM**</span><span class="sxs-lookup"><span data-stu-id="03ccc-109">**LVFOOTERITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem)
-   [<span data-ttu-id="03ccc-110">**LVGROUP**</span><span class="sxs-lookup"><span data-stu-id="03ccc-110">**LVGROUP**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvgroup)
-   [<span data-ttu-id="03ccc-111">**LVGROUPMETRICS**</span><span class="sxs-lookup"><span data-stu-id="03ccc-111">**LVGROUPMETRICS**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics)
-   [<span data-ttu-id="03ccc-112">**LVHITTESTINFO**</span><span class="sxs-lookup"><span data-stu-id="03ccc-112">**LVHITTESTINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo)
-   [<span data-ttu-id="03ccc-113">**LVINSERTGROUPSORTED**</span><span class="sxs-lookup"><span data-stu-id="03ccc-113">**LVINSERTGROUPSORTED**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)
-   [<span data-ttu-id="03ccc-114">**LVINSERTMARK**</span><span class="sxs-lookup"><span data-stu-id="03ccc-114">**LVINSERTMARK**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark)
-   [<span data-ttu-id="03ccc-115">**LVITEM**</span><span class="sxs-lookup"><span data-stu-id="03ccc-115">**LVITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvitema)
-   [<span data-ttu-id="03ccc-116">**LVITEMINDEX**</span><span class="sxs-lookup"><span data-stu-id="03ccc-116">**LVITEMINDEX**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvitemindex)
-   [<span data-ttu-id="03ccc-117">**LVSETINFOTIP**</span><span class="sxs-lookup"><span data-stu-id="03ccc-117">**LVSETINFOTIP**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip)
-   [<span data-ttu-id="03ccc-118">**LVTILEINFO**</span><span class="sxs-lookup"><span data-stu-id="03ccc-118">**LVTILEINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo)
-   [<span data-ttu-id="03ccc-119">**LVTILEVIEWINFO**</span><span class="sxs-lookup"><span data-stu-id="03ccc-119">**LVTILEVIEWINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo)
-   [<span data-ttu-id="03ccc-120">**NMITEMACTIVATE**</span><span class="sxs-lookup"><span data-stu-id="03ccc-120">**NMITEMACTIVATE**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate)
-   [<span data-ttu-id="03ccc-121">**NMLISTVIEW**</span><span class="sxs-lookup"><span data-stu-id="03ccc-121">**NMLISTVIEW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlistview)
-   [<span data-ttu-id="03ccc-122">**NMLVCACHEHINT**</span><span class="sxs-lookup"><span data-stu-id="03ccc-122">**NMLVCACHEHINT**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint)
-   [<span data-ttu-id="03ccc-123">**NMLVCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="03ccc-123">**NMLVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw)
-   [<span data-ttu-id="03ccc-124">**NMLVDISPINFO**</span><span class="sxs-lookup"><span data-stu-id="03ccc-124">**NMLVDISPINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa)
-   [<span data-ttu-id="03ccc-125">**NMLVEMPTYMARKUP**</span><span class="sxs-lookup"><span data-stu-id="03ccc-125">**NMLVEMPTYMARKUP**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup)
-   [<span data-ttu-id="03ccc-126">**NMLVFINDITEM**</span><span class="sxs-lookup"><span data-stu-id="03ccc-126">**NMLVFINDITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema)
-   [<span data-ttu-id="03ccc-127">**NMLVGETINFOTIP**</span><span class="sxs-lookup"><span data-stu-id="03ccc-127">**NMLVGETINFOTIP**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa)
-   [<span data-ttu-id="03ccc-128">**NMLVKEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="03ccc-128">**NMLVKEYDOWN**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown)
-   [<span data-ttu-id="03ccc-129">**NMLVLINK**</span><span class="sxs-lookup"><span data-stu-id="03ccc-129">**NMLVLINK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvlink)
-   [<span data-ttu-id="03ccc-130">**NMLVODSTATECHANGE**</span><span class="sxs-lookup"><span data-stu-id="03ccc-130">**NMLVODSTATECHANGE**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange)
-   [<span data-ttu-id="03ccc-131">**NMLVSCROLL**</span><span class="sxs-lookup"><span data-stu-id="03ccc-131">**NMLVSCROLL**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll)

 

 




