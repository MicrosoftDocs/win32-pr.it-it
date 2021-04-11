---
description: Un buffer di profondità è una proprietà del dispositivo. Per creare un buffer di profondità gestito da Direct3D, impostare i membri appropriati della struttura dei parametri D3DPRESENT, \_ come illustrato nell'esempio di codice seguente.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Creazione di un buffer di profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa30ccba6c44d3582201ea96017a16cc903fecce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126159"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a><span data-ttu-id="65bb8-104">Creazione di un buffer di profondità (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="65bb8-104">Creating a Depth Buffer (Direct3D 9)</span></span>

<span data-ttu-id="65bb8-105">Un buffer di profondità è una proprietà del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="65bb8-105">A depth buffer is a property of the device.</span></span> <span data-ttu-id="65bb8-106">Per creare un buffer di profondità gestito da Direct3D, impostare i membri appropriati della struttura dei [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md) , come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="65bb8-106">To create a depth buffer that is managed by Direct3D, set the appropriate members of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure as shown in the following code example.</span></span>


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



<span data-ttu-id="65bb8-107">Impostando il membro EnableAutoDepthStencil su **true**, si indica a Direct3D di gestire i buffer di profondità per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="65bb8-107">By setting the EnableAutoDepthStencil member to **TRUE**, you instruct Direct3D to manage depth buffers for the application.</span></span> <span data-ttu-id="65bb8-108">Si noti che AutoDepthStencilFormat deve essere impostato su un formato di buffer di profondità valido.</span><span class="sxs-lookup"><span data-stu-id="65bb8-108">Note that AutoDepthStencilFormat must be set to a valid depth buffer format.</span></span> <span data-ttu-id="65bb8-109">Il \_ flag D3DFMT D16 specifica un buffer di profondità a 16 bit, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="65bb8-109">The D3DFMT\_D16 flag specifies a 16-bit depth buffer, if one is available.</span></span>

<span data-ttu-id="65bb8-110">La chiamata seguente al metodo [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) crea un dispositivo che quindi crea un buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="65bb8-110">The following call to the [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) method creates a device that then creates a depth buffer.</span></span>


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



<span data-ttu-id="65bb8-111">Il buffer di profondità viene impostato automaticamente come destinazione di rendering del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="65bb8-111">The depth buffer is automatically set as the render target of the device.</span></span> <span data-ttu-id="65bb8-112">Quando il dispositivo viene reimpostato, il buffer di profondità viene eliminato e ricreato automaticamente nelle nuove dimensioni.</span><span class="sxs-lookup"><span data-stu-id="65bb8-112">When the device is reset, the depth buffer is automatically destroyed and re-created in the new size.</span></span>

<span data-ttu-id="65bb8-113">Per creare una nuova superficie del buffer di profondità, usare il metodo [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) .</span><span class="sxs-lookup"><span data-stu-id="65bb8-113">To create a new depth buffer surface, use the [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) method.</span></span>

<span data-ttu-id="65bb8-114">Per impostare una nuova superficie del buffer di profondità per il dispositivo, usare il metodo [**IDirect3DDevice9:: SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) .</span><span class="sxs-lookup"><span data-stu-id="65bb8-114">To set a new depth-buffer surface for the device, use the [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) method.</span></span>

<span data-ttu-id="65bb8-115">Per usare il buffer di profondità nell'applicazione, è necessario abilitare il buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="65bb8-115">To use the depth buffer in your application, you need to enable the depth buffer.</span></span> <span data-ttu-id="65bb8-116">Per informazioni dettagliate, vedere [Abilitazione del buffer di profondità (Direct3D 9)](enabling-depth-buffering.md).</span><span class="sxs-lookup"><span data-stu-id="65bb8-116">For details, see [Enabling Depth Buffering (Direct3D 9)](enabling-depth-buffering.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="65bb8-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65bb8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65bb8-118">Buffer di profondità</span><span class="sxs-lookup"><span data-stu-id="65bb8-118">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
