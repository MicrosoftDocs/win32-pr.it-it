---
title: Definizione dell'ambito di riproduzione
description: Definizione dell'ambito di riproduzione
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- MCIWndPlayFrom (macro)
- MCIWndPlayTo (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518fc80588147c4ccbbca619452b714333a8a34d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955443"
---
# <a name="defining-playback-scope"></a><span data-ttu-id="3b38b-105">Definizione dell'ambito di riproduzione</span><span class="sxs-lookup"><span data-stu-id="3b38b-105">Defining Playback Scope</span></span>

<span data-ttu-id="3b38b-106">MCIWnd fornisce macro che consentono di definire l' *ambito* di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="3b38b-106">MCIWnd provides macros that allow you to define the playback *scope*.</span></span> <span data-ttu-id="3b38b-107">L'ambito è la parte della riproduzione che si desidera riprodurre.</span><span class="sxs-lookup"><span data-stu-id="3b38b-107">The scope is the portion of the playback you want to play.</span></span> <span data-ttu-id="3b38b-108">Ad esempio, è possibile riprodurre il contenuto da una posizione diversa dalla posizione iniziale usando la macro [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) .</span><span class="sxs-lookup"><span data-stu-id="3b38b-108">For example, you can play the content from a position other than the beginning position by using the [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) macro.</span></span> <span data-ttu-id="3b38b-109">Questa macro viene spostata nella posizione specificata, inizia la riproduzione e continua fino alla fine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="3b38b-109">This macro moves to the specified position, begins playback, and continues to the end of the content.</span></span> <span data-ttu-id="3b38b-110">Analogamente, è possibile riprodurre il contenuto in un endpoint specificato utilizzando la macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) .</span><span class="sxs-lookup"><span data-stu-id="3b38b-110">Similarly, you can play the content to a specified end point by using the [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macro.</span></span> <span data-ttu-id="3b38b-111">Questa macro inizia in corrispondenza della posizione di riproduzione corrente e viene riprodotta fino a quando non raggiunge la posizione specificata o viene raggiunta la fine del contenuto, a seconda di quale si verifica per primo.</span><span class="sxs-lookup"><span data-stu-id="3b38b-111">This macro starts at the current playback position and plays until it reaches the specified position or the end of the content is reached, whichever comes first.</span></span>

<span data-ttu-id="3b38b-112">Inoltre, è possibile definire le posizioni iniziale e finale usando la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .</span><span class="sxs-lookup"><span data-stu-id="3b38b-112">Also, you can define both the beginning and ending positions by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span> <span data-ttu-id="3b38b-113">Questa macro viene spostata nella posizione iniziale specificata e viene riprodotta fino a quando non viene raggiunta la posizione finale specificata o la fine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="3b38b-113">This macro moves to the specified starting position and plays until the specified ending position or the end of the content is reached.</span></span>

 

 




