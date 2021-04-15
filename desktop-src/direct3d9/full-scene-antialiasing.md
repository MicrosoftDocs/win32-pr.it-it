---
description: L'anti-aliasing della scena completa si riferisce alla sfocatura dei bordi di ogni poligono nella scena in quanto viene rasterizzato in un singolo passaggio. non è necessario alcun secondo passaggio.
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: Anti-aliasing di Full-Scene (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73d559c4b4fec060efbff7468ee29e6c83b64c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520913"
---
# <a name="full-scene-antialiasing-direct3d-9"></a><span data-ttu-id="c7136-103">Anti-aliasing di Full-Scene (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c7136-103">Full-Scene Antialiasing (Direct3D 9)</span></span>

<span data-ttu-id="c7136-104">L'anti-aliasing della scena completa si riferisce alla sfocatura dei bordi di ogni poligono nella scena in quanto viene rasterizzato in un singolo passaggio. non è necessario alcun secondo passaggio.</span><span class="sxs-lookup"><span data-stu-id="c7136-104">Full-scene antialiasing refers to blurring the edges of each polygon in the scene as it is rasterized in a single pass; no second pass is required.</span></span> <span data-ttu-id="c7136-105">L'anti-aliasing della scena completa, quando supportato, interessa solo triangoli e gruppi di triangoli.</span><span class="sxs-lookup"><span data-stu-id="c7136-105">Full-scene antialiasing, when supported, affects only triangles and groups of triangles.</span></span> <span data-ttu-id="c7136-106">Non è possibile eseguire l'anti-aliasing delle righe usando i servizi Direct3D.</span><span class="sxs-lookup"><span data-stu-id="c7136-106">Lines cannot be antialiased by using Direct3D services.</span></span> <span data-ttu-id="c7136-107">L'anti-aliasing della scena completa viene eseguito in Direct3D usando il campionamento multiplo su ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="c7136-107">Full-scene antialiasing is done in Direct3D by using multisampling on each pixel.</span></span> <span data-ttu-id="c7136-108">Quando è abilitato il campionamento multiplo, tutti i sottocampionati di un pixel vengono aggiornati in un unico passaggio, ma se usati per altri effetti che coinvolgono più passaggi di rendering, l'applicazione può specificare che solo alcuni sottocampionamenti devono essere interessati da un determinato passaggio di rendering.</span><span class="sxs-lookup"><span data-stu-id="c7136-108">When multisampling is enabled, all subsamples of a pixel are updated in one pass but when used for other effects that involve multiple rendering passes, the application can specify that only some subsamples are to be affected by a given rendering pass.</span></span> <span data-ttu-id="c7136-109">Questo secondo approccio consente di simulare la sfocatura del movimento, gli effetti sullo stato attivo della profondità dei campi, la sfocatura della reflection e così via.</span><span class="sxs-lookup"><span data-stu-id="c7136-109">This latter approach enables simulation of motion blur, depth-of-field focus effects, reflection blur, and so on.</span></span>

<span data-ttu-id="c7136-110">In entrambi i casi, i vari esempi registrati per ogni pixel vengono combinati e restituiti sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="c7136-110">In both cases, the various samples recorded for each pixel are blended together and output to the screen.</span></span> <span data-ttu-id="c7136-111">Ciò consente di migliorare la qualità dell'immagine dell'anti-aliasing o di altri effetti.</span><span class="sxs-lookup"><span data-stu-id="c7136-111">This enables the improved image quality of antialiasing or other effects.</span></span>

<span data-ttu-id="c7136-112">Prima di creare un dispositivo con il metodo [**IDirect3D9:: CreateDevice**](/windows/desktop/api) , è necessario determinare se l'anti-aliasing a scena completa è supportato.</span><span class="sxs-lookup"><span data-stu-id="c7136-112">Before creating a device with the [**IDirect3D9::CreateDevice**](/windows/desktop/api) method, you need to determine if full-scene antialiasing is supported.</span></span> <span data-ttu-id="c7136-113">A tale scopo, chiamare il metodo [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) , come illustrato nell'esempio di codice riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c7136-113">Do this by calling the [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) method as shown in the code example below.</span></span>


```
/*
* The code below assumes that pD3D is a valid pointer 
*   to a IDirect3D9 interface.
*/

if( SUCCEEDED(pD3D->CheckDeviceMultiSampleType( D3DADAPTER_DEFAULT, 
                    D3DDEVTYPE_HAL , D3DFMT_R8G8B8, FALSE, 
                    D3DMULTISAMPLE_2_SAMPLES, NULL ) ) )
// Full-scene antialiasing is supported. Enable it here.
```



<span data-ttu-id="c7136-114">Il primo parametro che [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) accetta è un numero ordinale che indica l'adattatore di visualizzazione su cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="c7136-114">The first parameter that [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) accepts is an ordinal number that denotes the display adapter to query.</span></span> <span data-ttu-id="c7136-115">Questo esempio USA D3DADAPTER \_ default per specificare la scheda di visualizzazione principale.</span><span class="sxs-lookup"><span data-stu-id="c7136-115">This sample uses D3DADAPTER\_DEFAULT to specify the primary display adapter.</span></span> <span data-ttu-id="c7136-116">Il secondo parametro è un valore del tipo enumerato [**D3DDEVTYPE**](./d3ddevtype.md) , che specifica il tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7136-116">The second parameter is a value from the [**D3DDEVTYPE**](./d3ddevtype.md) enumerated type, specifying the device type.</span></span> <span data-ttu-id="c7136-117">Il terzo parametro specifica il formato della superficie.</span><span class="sxs-lookup"><span data-stu-id="c7136-117">The third parameter specifies the format of the surface.</span></span> <span data-ttu-id="c7136-118">Il quarto parametro indica a Direct3D se richiedere informazioni sul multisampling a finestra completa (**true**) o sull'anti-aliasing della scena completa (**false**).</span><span class="sxs-lookup"><span data-stu-id="c7136-118">The fourth parameter tells Direct3D whether to inquire about full-windowed multisampling (**TRUE**) or full-scene antialiasing (**FALSE**).</span></span> <span data-ttu-id="c7136-119">Questo esempio usa **false** per indicare a Direct3D che è in grado di richiedere l'anti-aliasing della scena completa.</span><span class="sxs-lookup"><span data-stu-id="c7136-119">This sample uses **FALSE** to tell Direct3D that it is inquiring about full-scene antialiasing.</span></span> <span data-ttu-id="c7136-120">L'ultimo parametro specifica la tecnica di campionamento multiplo che si desidera testare.</span><span class="sxs-lookup"><span data-stu-id="c7136-120">The last parameter specifies the multisampling technique that you want to test.</span></span> <span data-ttu-id="c7136-121">Usare un valore del tipo enumerato di [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) .</span><span class="sxs-lookup"><span data-stu-id="c7136-121">Use a value from the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="c7136-122">In questo esempio viene testato per verificare se sono supportati due livelli di multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="c7136-122">This sample tests to see if two levels of multisampling are supported.</span></span>

<span data-ttu-id="c7136-123">Se il dispositivo supporta il livello di multicampionamento che si vuole usare, il passaggio successivo consiste nell'impostare i parametri di presentazione compilando i membri appropriati della struttura dei [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md) per creare una superficie di rendering multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="c7136-123">If the device supports the level of multisampling that you want to use, the next step is to set the presentation parameters by filling in the appropriate members of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to create a multisample rendering surface.</span></span> <span data-ttu-id="c7136-124">Successivamente, è possibile creare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7136-124">After that, you can create the device.</span></span> <span data-ttu-id="c7136-125">Il codice di esempio seguente illustra come configurare un dispositivo con una superficie di rendering multicampionamento.</span><span class="sxs-lookup"><span data-stu-id="c7136-125">The sample code below shows how to set up a device with a multisampling render surface.</span></span>


```
/*
* The example below assumes that pD3D is a valid pointer 
* to a IDirect3D9 interface, d3dDevice is a pointer to a 
* IDirect3DDevice9 interface, and hWnd is a valid handle
* to a window.
*/

D3DPRESENT_PARAMETER d3dPP
ZeroMemory( &d3dPP, sizeof( d3dPP ) );
d3dPP.Windowed        = FALSE
d3dPP.SwapEffect      = D3DSWAPEFFECT_DISCARD;
d3dPP.MultiSampleType = D3DMULTISAMPLE_2_SAMPLES;
pD3D->CreateDevice(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                    &d3dpp, &d3dDevice)
```



<span data-ttu-id="c7136-126">Per usare il campionamento multiplo, il membro SwapEffect del \_ parametro D3DPRESENT deve essere impostato su D3DSWAPEFFECT \_ Ignora.</span><span class="sxs-lookup"><span data-stu-id="c7136-126">To use multisampling, the SwapEffect member of D3DPRESENT\_PARAMETER must be set to D3DSWAPEFFECT\_DISCARD.</span></span>

<span data-ttu-id="c7136-127">L'ultimo passaggio consiste nell'abilitare l'anti-aliasing multicampionamento chiamando il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e impostando D3DRS \_ MULTISAMPLEANTIALIAS su **true**.</span><span class="sxs-lookup"><span data-stu-id="c7136-127">The last step is to enable multisampling antialiasing by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method and setting the D3DRS\_MULTISAMPLEANTIALIAS to **TRUE**.</span></span> <span data-ttu-id="c7136-128">Dopo aver impostato questo valore su **true**, a tutti i rendering a cui è applicato il campionamento multiplo.</span><span class="sxs-lookup"><span data-stu-id="c7136-128">After setting this value to **TRUE**, any rendering that you do will have multisampling applied to it.</span></span> <span data-ttu-id="c7136-129">Potrebbe essere necessario abilitare e disabilitare il campionamento multiplo, a seconda di ciò che si sta eseguendo il rendering.</span><span class="sxs-lookup"><span data-stu-id="c7136-129">You might want to enable and disable multisampling, depending on what you are rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7136-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c7136-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7136-131">Anti-aliasing</span><span class="sxs-lookup"><span data-stu-id="c7136-131">Antialiasing</span></span>](antialiasing.md)
</dt> </dl>

 

 
