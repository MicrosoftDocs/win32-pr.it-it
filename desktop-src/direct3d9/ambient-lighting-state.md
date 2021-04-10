---
description: La luce ambientale è la luce che si irradia da tutte le direzioni. Per informazioni sul modo in cui Direct3D usa la luce di ambiente, vedere matematica dell'illuminazione (Direct3D 9).
ms.assetid: c5aa493e-09b8-433c-a21c-e39af795b3c9
title: Stato illuminazione ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bd604941961f5b4abdb301d5c23efba9980791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127235"
---
# <a name="ambient-lighting-state-direct3d-9"></a><span data-ttu-id="3c8c0-104">Stato illuminazione ambiente (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3c8c0-104">Ambient Lighting State (Direct3D 9)</span></span>

<span data-ttu-id="3c8c0-105">La luce ambientale è la luce che si irradia da tutte le direzioni.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-105">Ambient light is surrounding light that radiates from all directions.</span></span> <span data-ttu-id="3c8c0-106">Per informazioni sul modo in cui Direct3D usa la luce di ambiente, vedere [matematica dell'illuminazione (Direct3D 9)](mathematics-of-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="3c8c0-106">For information about how Direct3D uses ambient light, see [Mathematics of Lighting (Direct3D 9)](mathematics-of-lighting.md).</span></span>

<span data-ttu-id="3c8c0-107">Un'applicazione C++ imposta il colore dell'illuminazione ambientale richiamando il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e passando il valore enumerato D3DRS \_ ambiente come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-107">A C++ application sets the color of ambient lighting by invoking the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method and passing the enumerated value D3DRS\_AMBIENT as the first parameter.</span></span> <span data-ttu-id="3c8c0-108">Il secondo parametro è un valore di colore.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-108">The second parameter is a color value.</span></span> <span data-ttu-id="3c8c0-109">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-109">The default value is zero.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the ambient light.

d3dDevice->SetRenderState(D3DRS_AMBIENT, 0x00202020);
```



## <a name="related-topics"></a><span data-ttu-id="3c8c0-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c8c0-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c8c0-111">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="3c8c0-111">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
