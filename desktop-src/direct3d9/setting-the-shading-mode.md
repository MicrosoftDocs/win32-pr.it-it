---
description: Direct3D consente di selezionare una modalità di ombreggiatura alla volta.
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: Impostazione della modalità di ombreggiatura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f93d79e4507d9e9d08569e5cbd75bb8b42aa4f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482084"
---
# <a name="setting-the-shading-mode-direct3d-9"></a><span data-ttu-id="4408e-103">Impostazione della modalità di ombreggiatura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4408e-103">Setting the Shading Mode (Direct3D 9)</span></span>

<span data-ttu-id="4408e-104">Direct3D consente di selezionare una modalità di ombreggiatura alla volta.</span><span class="sxs-lookup"><span data-stu-id="4408e-104">Direct3D enables one shading mode to be selected at a time.</span></span> <span data-ttu-id="4408e-105">Per impostazione predefinita, è selezionata l'ombreggiatura Gouraud.</span><span class="sxs-lookup"><span data-stu-id="4408e-105">By default, Gouraud shading is selected.</span></span> <span data-ttu-id="4408e-106">In C++ è possibile modificare la modalità di ombreggiatura chiamando il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="4408e-106">In C++, you can change the shading mode by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="4408e-107">Impostare il parametro *state* su D3DRS \_ MODOOMBRA.</span><span class="sxs-lookup"><span data-stu-id="4408e-107">Set the *State* parameter to D3DRS\_SHADEMODE.</span></span> <span data-ttu-id="4408e-108">Il parametro *state* deve essere impostato su un membro dell'enumerazione [**D3DSHADEMODE**](./d3dshademode.md) .</span><span class="sxs-lookup"><span data-stu-id="4408e-108">The *State* parameter must be set to a member of the [**D3DSHADEMODE**](./d3dshademode.md) enumeration.</span></span> <span data-ttu-id="4408e-109">Gli esempi di codice di esempio seguenti illustrano come è possibile impostare la modalità di ombreggiatura corrente di un'applicazione Direct3D sulla modalità di ombreggiatura flat o Gouraud.</span><span class="sxs-lookup"><span data-stu-id="4408e-109">The following sample code examples illustrate how the current shading mode of a Direct3D application can be set to flat or Gouraud shading mode.</span></span>


```
// Set to flat shading.
// This code example assumes that pDev is a valid pointer to 
// an IDirect3DDevice9 interface.
hr = pDev->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}

// Set to Gouraud shading. This is the default for Direct3D.
hr = pDev->SetRenderState(D3DRS_SHADEMODE,
                            D3DSHADE_GOURAUD);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



## <a name="related-topics"></a><span data-ttu-id="4408e-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4408e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4408e-111">Ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="4408e-111">Shading</span></span>](shading.md)
</dt> </dl>

 

 
