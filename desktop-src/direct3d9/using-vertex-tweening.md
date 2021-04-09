---
description: Per determinare se Direct3D supporta l'interpolazione dei vertici, verificare la presenza del \_ flag di interpolazione D3DVTXPCAPS nel membro VertexProcessingCaps della struttura D3DCAPS9.
ms.assetid: b60c7f96-3752-4703-9059-486d9906c508
title: Uso dell'interpolazione di vertici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ca56cc521b5bff01a5d6af5c2d4ab6b02cd49e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876394"
---
# <a name="using-vertex-tweening-direct3d-9"></a><span data-ttu-id="88c17-103">Uso dell'interpolazione di vertici (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="88c17-103">Using Vertex Tweening (Direct3D 9)</span></span>

<span data-ttu-id="88c17-104">Per determinare se Direct3D supporta l'interpolazione dei vertici, verificare la presenza del \_ flag di interpolazione D3DVTXPCAPS nel membro VertexProcessingCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="88c17-104">To determine if Direct3D supports vertex tweening, check for the D3DVTXPCAPS\_TWEENING flag in the VertexProcessingCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="88c17-105">Nell'esempio di codice seguente viene usato il metodo [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) per determinare se l'interpolazione è supportata.</span><span class="sxs-lookup"><span data-stu-id="88c17-105">The following code example uses the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method to determine if tweening is supported.</span></span>


```
// This example assumes that m_pD3DDevice is 
// a valid pointer to a IDirect3DDevice9 interface.
//
D3DCAPS9 d3dCaps;

m_pD3DDevice->GetDeviceCaps( &d3dCaps );
if( 0 != (d3dCaps.VertexProcessingCaps & D3DVTXPCAPS_TWEENING) )
    // Vertex tweening is supported.
```



<span data-ttu-id="88c17-106">Per usare l'interpolazione vettoriale, è necessario innanzitutto configurare un tipo di vertice personalizzato che usa una seconda posizione normale o una seconda.</span><span class="sxs-lookup"><span data-stu-id="88c17-106">To use vector tweening, you must first set up a custom vertex type that uses a second normal or a second position.</span></span> <span data-ttu-id="88c17-107">Nell'esempio di codice seguente viene illustrata una dichiarazione di esempio che include sia un secondo punto che una seconda posizione.</span><span class="sxs-lookup"><span data-stu-id="88c17-107">The following code example shows a sample declaration that includes both a second point and a second position.</span></span>


```
struct TEX_VERTEX
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DVECTOR position2;
    D3DVECTOR normal2;
};

//Create a vertex buffer with the type TEX_VERTEX.
```



<span data-ttu-id="88c17-108">Il passaggio successivo consiste nell'impostare la dichiarazione corrente.</span><span class="sxs-lookup"><span data-stu-id="88c17-108">The next step is to set the current declaration.</span></span> <span data-ttu-id="88c17-109">Nell'esempio di codice seguente viene illustrato come eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="88c17-109">The code example below shows how to do this.</span></span>


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    { 0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 1 },
    { 0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 1 },
    D3DDECL_END()
};
```



<span data-ttu-id="88c17-110">Per ulteriori informazioni sulla creazione di un tipo di vertice personalizzato e di un buffer di vertice, vedere [creazione di un buffer vertex (Direct3D 9)](creating-a-vertex-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="88c17-110">For more information about creating a custom vertex type and a vertex buffer, see [Creating a Vertex Buffer (Direct3D 9)](creating-a-vertex-buffer.md).</span></span>

> [!Note]  
> <span data-ttu-id="88c17-111">Quando è abilitata l'interpolazione dei vertici, nella dichiarazione corrente deve essere presente una seconda posizione o una seconda normale.</span><span class="sxs-lookup"><span data-stu-id="88c17-111">When vertex tweening is enabled, a second position or a second normal must be present in the current declaration.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="88c17-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88c17-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88c17-113">Interpolazione di vertici</span><span class="sxs-lookup"><span data-stu-id="88c17-113">Vertex Tweening</span></span>](vertex-tweening.md)
</dt> </dl>

 

 
