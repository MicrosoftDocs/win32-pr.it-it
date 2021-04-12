---
description: "Le risorse di trama sono implementate nell'interfaccia IDirect3DTexture9. Per ottenere un puntatore a un'interfaccia di trama, chiamare il metodo IDirect3DDevice9:: CreateTexture o una delle funzioni D3DX seguenti."
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: Risorse di trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14134ca53b7735426e3f01340308282858da5516
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225469"
---
# <a name="texture-resources-direct3d-9"></a><span data-ttu-id="a9244-104">Risorse di trama (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a9244-104">Texture Resources (Direct3D 9)</span></span>

<span data-ttu-id="a9244-105">Le risorse di trama sono implementate nell'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="a9244-105">Texture resources are implemented in the [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface.</span></span> <span data-ttu-id="a9244-106">Per ottenere un puntatore a un'interfaccia di trama, chiamare il metodo [**IDirect3DDevice9:: createTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) o una delle funzioni D3DX seguenti.</span><span class="sxs-lookup"><span data-stu-id="a9244-106">To obtain a pointer to a texture interface, call the [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) method or any of the following D3DX functions.</span></span>

-   [<span data-ttu-id="a9244-107">**D3DXCreateTexture**</span><span class="sxs-lookup"><span data-stu-id="a9244-107">**D3DXCreateTexture**</span></span>](d3dxcreatetexture.md)
-   [<span data-ttu-id="a9244-108">**D3DXCreateTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="a9244-108">**D3DXCreateTextureFromFile**</span></span>](d3dxcreatetexturefromfile.md)
-   [<span data-ttu-id="a9244-109">**D3DXCreateTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="a9244-109">**D3DXCreateTextureFromFileEx**</span></span>](d3dxcreatetexturefromfileex.md)
-   [<span data-ttu-id="a9244-110">**D3DXCreateTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="a9244-110">**D3DXCreateTextureFromFileInMemory**</span></span>](d3dxcreatetexturefromfileinmemory.md)
-   [<span data-ttu-id="a9244-111">**D3DXCreateTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="a9244-111">**D3DXCreateTextureFromFileInMemoryEx**</span></span>](d3dxcreatetexturefromfileinmemoryex.md)
-   [<span data-ttu-id="a9244-112">**D3DXCreateTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="a9244-112">**D3DXCreateTextureFromResource**</span></span>](d3dxcreatetexturefromresource.md)
-   [<span data-ttu-id="a9244-113">**D3DXCreateTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="a9244-113">**D3DXCreateTextureFromResourceEx**</span></span>](d3dxcreatetexturefromresourceex.md)

<span data-ttu-id="a9244-114">Nell'esempio di codice seguente viene usato [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) per caricare una trama da Tiger.bmp.</span><span class="sxs-lookup"><span data-stu-id="a9244-114">The following code example uses [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) to load a texture from Tiger.bmp.</span></span>


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



<span data-ttu-id="a9244-115">Il primo parametro accettato da [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) è un puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="a9244-115">The first parameter that [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) accepts is a pointer to an [**IDirect3DDevice9**](/windows/desktop/api) interface.</span></span> <span data-ttu-id="a9244-116">Il secondo parametro indica a Direct3D il nome del file da cui caricare la trama.</span><span class="sxs-lookup"><span data-stu-id="a9244-116">The second parameter tells Direct3D the name of the file from which to load the texture.</span></span> <span data-ttu-id="a9244-117">Il terzo parametro accetta l'indirizzo di un puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta l'oggetto trama creato.</span><span class="sxs-lookup"><span data-stu-id="a9244-117">The third parameter takes the address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

## <a name="rendering-with-texture-resources"></a><span data-ttu-id="a9244-118">Rendering con risorse di trama</span><span class="sxs-lookup"><span data-stu-id="a9244-118">Rendering with Texture Resources</span></span>

<span data-ttu-id="a9244-119">Direct3D supporta la fusione di più trame attraverso il concetto di fasi della trama.</span><span class="sxs-lookup"><span data-stu-id="a9244-119">Direct3D supports multiple texture blending through the concept of texture stages.</span></span> <span data-ttu-id="a9244-120">Ogni fase della trama contiene una trama e le operazioni che possono essere eseguite sulla trama.</span><span class="sxs-lookup"><span data-stu-id="a9244-120">Each texture stage contains a texture and operations that can be performed on the texture.</span></span> <span data-ttu-id="a9244-121">Le trame nelle fasi della trama formano il set di trame correnti.</span><span class="sxs-lookup"><span data-stu-id="a9244-121">The textures in the texture stages form the set of current textures.</span></span> <span data-ttu-id="a9244-122">Per altre informazioni, vedere [blending di trame (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="a9244-122">For more information, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span> <span data-ttu-id="a9244-123">Lo stato di ogni trama viene incapsulato nella fase della trama.</span><span class="sxs-lookup"><span data-stu-id="a9244-123">The state of each texture is encapsulated in its texture stage.</span></span>

<span data-ttu-id="a9244-124">In un'applicazione C++ lo stato di ogni trama deve essere impostato con il metodo [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="a9244-124">In a C++ application, the state of each texture must be set with the [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="a9244-125">Passare il numero di fase (0-7) come valore del primo parametro.</span><span class="sxs-lookup"><span data-stu-id="a9244-125">Pass the stage number (0-7) as the value of the first parameter.</span></span> <span data-ttu-id="a9244-126">Impostare il valore del secondo parametro su un membro del tipo enumerato [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) .</span><span class="sxs-lookup"><span data-stu-id="a9244-126">Set the value of the second parameter to a member of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type.</span></span> <span data-ttu-id="a9244-127">Il parametro finale è il valore dello stato per lo stato della trama particolare.</span><span class="sxs-lookup"><span data-stu-id="a9244-127">The final parameter is the state value for the particular texture state.</span></span>

<span data-ttu-id="a9244-128">Usando i puntatori dell'interfaccia di trama, l'applicazione può eseguire il rendering di una blend di un massimo di otto trame.</span><span class="sxs-lookup"><span data-stu-id="a9244-128">Using texture interface pointers, your application can render a blend of up to eight textures.</span></span> <span data-ttu-id="a9244-129">Impostare le trame correnti richiamando il metodo [**IDirect3DDevice9:: setexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .</span><span class="sxs-lookup"><span data-stu-id="a9244-129">Set the current textures by invoking the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span> <span data-ttu-id="a9244-130">Direct3D combina tutte le trame correnti sulle primitive di cui esegue il rendering.</span><span class="sxs-lookup"><span data-stu-id="a9244-130">Direct3D blends all current textures onto the primitives that it renders.</span></span>

> [!Note]  
> <span data-ttu-id="a9244-131">Il metodo [**IDirect3DDevice9:: setexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) incrementa il conteggio dei riferimenti della superficie della trama da assegnare.</span><span class="sxs-lookup"><span data-stu-id="a9244-131">The [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method increments the reference count of the texture surface being assigned.</span></span> <span data-ttu-id="a9244-132">Quando la trama non è più necessaria, è necessario impostare la trama nella fase appropriata su **null**.</span><span class="sxs-lookup"><span data-stu-id="a9244-132">When the texture is no longer needed, you should set the texture at the appropriate stage to **NULL**.</span></span> <span data-ttu-id="a9244-133">Se non si riesce a eseguire questa operazione, la superficie non verrà rilasciata, causando una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="a9244-133">If you fail to do this, the surface will not be released, resulting in a memory leak.</span></span>

 

<span data-ttu-id="a9244-134">L'applicazione può impostare lo stato di wrapping della trama per le trame correnti chiamando il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) .</span><span class="sxs-lookup"><span data-stu-id="a9244-134">Your application can set the texture wrapping state for the current textures by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method.</span></span> <span data-ttu-id="a9244-135">Passare un valore da D3DRS \_ WRAP0 a D3DRS \_ WRAP7 come valore del primo parametro e usare una combinazione dei \_ flag D3DWRAPCOORD 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD \_ 2 e D3DWRAPCOORD \_ 3 per abilitare il ritorno a capo nelle direzioni u, v o w.</span><span class="sxs-lookup"><span data-stu-id="a9244-135">Pass a value from D3DRS\_WRAP0 through D3DRS\_WRAP7 as the value of the first parameter, and use a combination of the D3DWRAPCOORD\_0, D3DWRAPCOORD\_1, D3DWRAPCOORD\_2, and D3DWRAPCOORD\_3 flags to enable wrapping in the u, v, or w directions.</span></span>

<span data-ttu-id="a9244-136">L'applicazione può anche impostare la prospettiva della trama e gli Stati di filtro della trama.</span><span class="sxs-lookup"><span data-stu-id="a9244-136">Your application can also set the texture perspective and texture filtering states.</span></span> <span data-ttu-id="a9244-137">Vedere [filtro delle trame (Direct3D 9)](texture-filtering.md).</span><span class="sxs-lookup"><span data-stu-id="a9244-137">See [Texture Filtering (Direct3D 9)](texture-filtering.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9244-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9244-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9244-139">Trame Direct3D</span><span class="sxs-lookup"><span data-stu-id="a9244-139">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
