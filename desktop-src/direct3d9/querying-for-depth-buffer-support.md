---
description: Come per qualsiasi caratteristica, il driver utilizzato dall'applicazione potrebbe non supportare tutti i tipi di buffering di profondità.
ms.assetid: 8bf022f6-fd97-43f5-ac19-6a75ddb45f5e
title: Esecuzione di query per il supporto del buffer di profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfe7555c1fa0fccddcfcb12ff8bc53f1a0f5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745522"
---
# <a name="querying-for-depth-buffer-support-direct3d-9"></a><span data-ttu-id="ab515-103">Esecuzione di query per il supporto del buffer di profondità (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ab515-103">Querying for Depth Buffer Support (Direct3D 9)</span></span>

<span data-ttu-id="ab515-104">Come per qualsiasi caratteristica, il driver utilizzato dall'applicazione potrebbe non supportare tutti i tipi di buffering di profondità.</span><span class="sxs-lookup"><span data-stu-id="ab515-104">As with any feature, the driver that your application uses might not support all types of depth buffering.</span></span> <span data-ttu-id="ab515-105">Controllare sempre le funzionalità del driver.</span><span class="sxs-lookup"><span data-stu-id="ab515-105">Always check the driver's capabilities.</span></span> <span data-ttu-id="ab515-106">Sebbene la maggior parte dei driver supporti il buffering di profondità basato su z, non tutti supporteranno il buffering basato su w.</span><span class="sxs-lookup"><span data-stu-id="ab515-106">Although most drivers support z-based depth buffering, not all will support w-based depth buffering.</span></span> <span data-ttu-id="ab515-107">I driver non hanno esito negativo se si tenta di abilitare uno schema non supportato.</span><span class="sxs-lookup"><span data-stu-id="ab515-107">Drivers do not fail if you attempt to enable an unsupported scheme.</span></span> <span data-ttu-id="ab515-108">Eseguono invece il fallback su un altro metodo di buffering di profondità, o talvolta disabilitano completamente il buffering di profondità, che può comportare il rendering di scene con artefatti di ordinamento estremamente approfonditi.</span><span class="sxs-lookup"><span data-stu-id="ab515-108">They fall back on another depth buffering method instead, or sometimes disable depth buffering altogether, which can result in scenes rendered with extreme depth-sorting artifacts.</span></span>

<span data-ttu-id="ab515-109">È possibile verificare il supporto generale per i buffer di profondità eseguendo una query su Direct3D per il dispositivo di visualizzazione che l'applicazione userà prima di creare un dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ab515-109">You can check for general support for depth buffers by querying Direct3D for the display device that your application will use before you create a Direct3D device.</span></span> <span data-ttu-id="ab515-110">Se l'oggetto Direct3D segnala che supporta il buffering di profondità, qualsiasi dispositivo hardware creato dall'oggetto Direct3D supporterà il buffer z.</span><span class="sxs-lookup"><span data-stu-id="ab515-110">If the Direct3D object reports that it supports depth buffering, any hardware devices you create from this Direct3D object will support z-buffering.</span></span>

<span data-ttu-id="ab515-111">Per eseguire una query per il supporto del buffering di profondità, è possibile usare il metodo [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) , come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="ab515-111">To query for depth buffering support, you can use the [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) method, as shown in the following code example.</span></span>


```
// The following example assumes that pCaps is a valid pointer to an 
// initialized D3DCAPS9 structure
if(FAILED(m_pD3D->CheckDeviceFormat(pCaps->AdapterOrdinal, 
                                    pCaps->DeviceType, 
                                    AdapterFormat, 
                                    D3DUSAGE_DEPTHSTENCIL, 
                                    D3DRTYPE_SURFACE,
                                    D3DFMT_D16)))
    return E_FAIL;
```



<span data-ttu-id="ab515-112">[**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) consente di scegliere un dispositivo da creare in base alle funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab515-112">[**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) allows you to choose a device to create based on the capabilities of that device.</span></span> <span data-ttu-id="ab515-113">In questo caso, i dispositivi che non supportano i buffer di profondità a 16 bit vengono rifiutati.</span><span class="sxs-lookup"><span data-stu-id="ab515-113">In this case, devices that do not support 16-bit depth buffers are rejected.</span></span>

<span data-ttu-id="ab515-114">Nell'esempio di codice seguente viene illustrato l'uso di [**IDirect3D9:: CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) per determinare la compatibilità di stencil Depth con una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="ab515-114">Using [**IDirect3D9::CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) to determine depth-stencil compatibility with a render target is illustrated in the following code example.</span></span>


```
// Reject devices that cannot create a render target of RTFormat while
// the back buffer is of RTFormat and the depth-stencil buffer is
// at least 8 bits of stencil
if(FAILED(m_pD3D->CheckDepthStencilMatch(pCaps->AdapterOrdinal,
                                        pCaps->DeviceType, 
                                        AdapterFormat, 
                                        RTFormat, 
                                        D3DFMT_D24S8)))
    return E_FAIL;
```



<span data-ttu-id="ab515-115">Quando si è certi che il driver supporta i buffer di profondità, è possibile verificare il supporto del buffer w.</span><span class="sxs-lookup"><span data-stu-id="ab515-115">When you know that the driver supports depth buffers, you can verify w-buffer support.</span></span> <span data-ttu-id="ab515-116">Sebbene i buffer di profondità siano supportati per tutti i rasterizzatori software, i buffer w sono supportati solo dall'rasterizzatore dei riferimenti, che non è adatto per l'uso da parte di applicazioni reali.</span><span class="sxs-lookup"><span data-stu-id="ab515-116">Although depth buffers are supported for all software rasterizers, w-buffers are supported only by the reference rasterizer, which is not suited for use by real-world applications.</span></span> <span data-ttu-id="ab515-117">Indipendentemente dal tipo di dispositivo usato dall'applicazione, verificare il supporto per i buffer w prima di provare ad abilitare il buffering con profondità basata su w.</span><span class="sxs-lookup"><span data-stu-id="ab515-117">Regardless of the type of device your application uses, verify support for w-buffers before you attempt to enable w-based depth buffering.</span></span>

1.  <span data-ttu-id="ab515-118">Dopo la creazione del dispositivo, chiamare il metodo [**IDirect3DDevice9:: GetDeviceCaps**](/windows/desktop/api) , passando una struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) inizializzata.</span><span class="sxs-lookup"><span data-stu-id="ab515-118">After creating your device, call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/desktop/api) method, passing an initialized [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span>
2.  <span data-ttu-id="ab515-119">Dopo la chiamata, il membro LineCaps contiene informazioni sul supporto del driver per il rendering delle primitive.</span><span class="sxs-lookup"><span data-stu-id="ab515-119">After the call, the LineCaps member contains information about the driver's support for rendering primitives.</span></span>
3.  <span data-ttu-id="ab515-120">Se il membro RasterCaps della struttura contiene il flag D3DPRASTERCAPS \_ WBUFFER, il driver supporta il buffering con profondità basata su w per quel tipo primitivo.</span><span class="sxs-lookup"><span data-stu-id="ab515-120">If the RasterCaps member of this structure contains the D3DPRASTERCAPS\_WBUFFER flag, then the driver supports w-based depth buffering for that primitive type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab515-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ab515-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab515-122">Buffer di profondità</span><span class="sxs-lookup"><span data-stu-id="ab515-122">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
