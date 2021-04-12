---
title: Porting di funzioni di anti-aliasing
description: Porting di funzioni di anti-aliasing
ms.assetid: 7f79f0fa-4a08-4678-bc73-8611e8d9e91a
keywords:
- Porting di IRIS GL, anti-aliasing
- porting da IRIS GL, anti-aliasing
- porting in OpenGL da IRIS GL, anti-aliasing
- Porting OpenGL da IRIS GL, anti-aliasing
- anti-aliasing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec2fcae4fe7b6909e00efb0fb892821a5c12765
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396827"
---
# <a name="porting-antialiasing-functions"></a><span data-ttu-id="29be4-108">Porting di funzioni di anti-aliasing</span><span class="sxs-lookup"><span data-stu-id="29be4-108">Porting Antialiasing Functions</span></span>

<span data-ttu-id="29be4-109">In OpenGL la modalità subpixel è sempre attiva, di conseguenza la funzione di IRIS GL **subpixel**(**true**) non è necessaria e non ha un equivalente OpenGL.</span><span class="sxs-lookup"><span data-stu-id="29be4-109">In OpenGL the subpixel mode is always on, consequently the IRIS GL function **subpixel**(**TRUE**) is not necessary and has no OpenGL equivalent.</span></span> <span data-ttu-id="29be4-110">Negli argomenti seguenti vengono descritti gli aspetti della portabilità del codice di anti-aliasing IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="29be4-110">The following topics describe aspects of porting IRIS GL antialiasing code.</span></span>

-   [<span data-ttu-id="29be4-111">Porting del codice di fusione</span><span class="sxs-lookup"><span data-stu-id="29be4-111">Porting Blending Code</span></span>](porting-blending-code.md)
-   [<span data-ttu-id="29be4-112">Porting di funzioni di test AFunction</span><span class="sxs-lookup"><span data-stu-id="29be4-112">Porting afunction Test Functions</span></span>](porting-afunction-test-functions.md)
-   [<span data-ttu-id="29be4-113">Uso di funzioni di anti-aliasing</span><span class="sxs-lookup"><span data-stu-id="29be4-113">Using Antialiasing Functions</span></span>](using-antialiasing-functions.md)

 

 




