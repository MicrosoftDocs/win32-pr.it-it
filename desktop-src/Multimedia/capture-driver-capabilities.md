---
title: Acquisisci funzionalità driver
description: Acquisisci funzionalità driver
ms.assetid: 6e74635e-9dac-419d-a264-08fee04ae7b7
keywords:
- Messaggio WM_CAP_DRIVER_GET_CAPS
- capDriverGetCaps (macro)
- Struttura CAPDRIVERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87fb4f9cb439229721b6c10aa6207af601f9ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044314"
---
# <a name="capture-driver-capabilities"></a><span data-ttu-id="25f88-106">Acquisisci funzionalità driver</span><span class="sxs-lookup"><span data-stu-id="25f88-106">Capture Driver Capabilities</span></span>

<span data-ttu-id="25f88-107">È possibile recuperare le funzionalità hardware del driver di acquisizione attualmente connesso usando il [**driver WM \_ Cap \_ \_ get \_ Caps**](wm-cap-driver-get-caps.md) Message (o la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) ).</span><span class="sxs-lookup"><span data-stu-id="25f88-107">You can retrieve the hardware capabilities of the currently connected capture driver by using the [**WM\_CAP\_DRIVER\_GET\_CAPS**](wm-cap-driver-get-caps.md) message (or the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro).</span></span> <span data-ttu-id="25f88-108">Questo messaggio restituisce le funzionalità del driver di acquisizione e dell'hardware sottostante nella struttura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="25f88-108">This message returns the capabilities of the capture driver and underlying hardware in the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

 

 




