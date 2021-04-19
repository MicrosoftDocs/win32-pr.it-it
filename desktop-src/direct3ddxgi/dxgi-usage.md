---
description: Flag per le opzioni di creazione di superfici e risorse.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55e99d86201c76fbe2ec229b13b5831d767ff34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322511"
---
# <a name="dxgi_usage"></a><span data-ttu-id="0d75a-103">utilizzo di DXGI \_</span><span class="sxs-lookup"><span data-stu-id="0d75a-103">DXGI\_USAGE</span></span>

<span data-ttu-id="0d75a-104">Flag per le opzioni di creazione di superfici e risorse.</span><span class="sxs-lookup"><span data-stu-id="0d75a-104">Flags for surface and resource creation options.</span></span>



| <span data-ttu-id="0d75a-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="0d75a-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                  | <span data-ttu-id="0d75a-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d75a-106">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <span data-ttu-id="0d75a-107"><dt>**DXGI \_ \_ \_ Buffer back di utilizzo**</dt> <dt> <<  1L (2 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="0d75a-107"><dt>**DXGI\_USAGE\_BACK\_BUFFER**</dt> <dt>1L << (2 + 4)</dt></span></span> </dl>                             | <span data-ttu-id="0d75a-108">La superficie o la risorsa viene utilizzata come buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="0d75a-108">The surface or resource is used as a back buffer.</span></span> <span data-ttu-id="0d75a-109">Non è necessario passare il **\_ \_ \_ buffer di utilizzo di DXGI** quando si crea una catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="0d75a-109">You don’t need to pass **DXGI\_USAGE\_BACK\_BUFFER** when you create a swap chain.</span></span> <span data-ttu-id="0d75a-110">È tuttavia possibile determinare se una risorsa appartiene a una catena di scambio quando si chiama [**IDXGIResource:: getusage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) e si ottiene il **\_ \_ \_ buffer di utilizzo di DXGI**.</span><span class="sxs-lookup"><span data-stu-id="0d75a-110">But you can determine whether a resource belongs to a swap chain when you call [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) and get **DXGI\_USAGE\_BACK\_BUFFER**.</span></span><br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <span data-ttu-id="0d75a-111"><dt>**DXGI \_ Eliminazione dell'utilizzo \_ \_ nel \_**</dt> <dt> <<  1L corrente (5 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="0d75a-111"><dt>**DXGI\_USAGE\_DISCARD\_ON\_PRESENT**</dt> <dt>1L << (5 + 4)</dt></span></span> </dl>       | <span data-ttu-id="0d75a-112">Questo flag è solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="0d75a-112">This flag is for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <span data-ttu-id="0d75a-113"><dt>**DXGI \_ UTILIZZO \_ di \_ sola lettura**</dt> <dt>1L <<  (4 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="0d75a-113"><dt>**DXGI\_USAGE\_READ\_ONLY**</dt> <dt>1L << (4 + 4)</dt></span></span> </dl>                                   | <span data-ttu-id="0d75a-114">Utilizzare la superficie o la risorsa solo per la lettura.</span><span class="sxs-lookup"><span data-stu-id="0d75a-114">Use the surface or resource for reading only.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <span data-ttu-id="0d75a-115"><dt>**DXGI \_ \_Output della \_ destinazione \_ di rendering di utilizzo**</dt> <dt> <<  1L (1 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="0d75a-115"><dt>**DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT**</dt> <dt>1L << (1 + 4)</dt></span></span> </dl> | <span data-ttu-id="0d75a-116">Usare la superficie o la risorsa come destinazione di rendering dell'output.</span><span class="sxs-lookup"><span data-stu-id="0d75a-116">Use the surface or resource as an output render target.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <span data-ttu-id="0d75a-117"><dt>**DXGI \_ <<  \_ \_ input shader di utilizzo**</dt> <dt>(0 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="0d75a-117"><dt>**DXGI\_USAGE\_SHADER\_INPUT**</dt> <dt>1L << (0 + 4)</dt></span></span> </dl>                          | <span data-ttu-id="0d75a-118">Utilizzare la superficie o la risorsa come input per uno shader.</span><span class="sxs-lookup"><span data-stu-id="0d75a-118">Use the surface or resource as an input to a shader.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <span data-ttu-id="0d75a-119"><dt>**DXGI \_ UTILIZZO \_**</dt> <dt> <<  1L condiviso (3 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="0d75a-119"><dt>**DXGI\_USAGE\_SHARED**</dt> <dt>1L << (3 + 4)</dt></span></span> </dl>                                             | <span data-ttu-id="0d75a-120">Condividere la superficie o la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0d75a-120">Share the surface or resource.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <span data-ttu-id="0d75a-121"><dt>**DXGI \_ UTILIZZO di \_ \_ accesso non ordinato**</dt> <dt>1L <<  (6 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="0d75a-121"><dt>**DXGI\_USAGE\_UNORDERED\_ACCESS**</dt> <dt>1L << (6 + 4)</dt></span></span> </dl>              | <span data-ttu-id="0d75a-122">Utilizzare la superficie o la risorsa per l'accesso non ordinato.</span><span class="sxs-lookup"><span data-stu-id="0d75a-122">Use the surface or resource for unordered access.</span></span><br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="0d75a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d75a-123">Remarks</span></span>

<span data-ttu-id="0d75a-124">Ogni flag viene definito come Unsigned Integer.</span><span class="sxs-lookup"><span data-stu-id="0d75a-124">Each flag is defined as an unsigned integer.</span></span>

``` syntax
#define DXGI_CPU_ACCESS_NONE    ( 0 )
#define DXGI_CPU_ACCESS_DYNAMIC    ( 1 )
#define DXGI_CPU_ACCESS_READ_WRITE    ( 2 )
#define DXGI_CPU_ACCESS_SCRATCH    ( 3 )
#define DXGI_CPU_ACCESS_FIELD        15
#define DXGI_USAGE_SHADER_INPUT             ( 1L << (0 + 4) )
#define DXGI_USAGE_RENDER_TARGET_OUTPUT     ( 1L << (1 + 4) )
#define DXGI_USAGE_BACK_BUFFER              ( 1L << (2 + 4) )
#define DXGI_USAGE_SHARED                   ( 1L << (3 + 4) )
#define DXGI_USAGE_READ_ONLY                ( 1L << (4 + 4) )
#define DXGI_USAGE_DISCARD_ON_PRESENT       ( 1L << (5 + 4) )
#define DXGI_USAGE_UNORDERED_ACCESS         ( 1L << (6 + 4) )
typedef UINT DXGI_USAGE;
```

<span data-ttu-id="0d75a-125">Queste opzioni dei flag vengono usate in una chiamata al metodo [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2:: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2:: CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)o [**IDXGIFactory2:: CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) per descrivere le opzioni di utilizzo della superficie e di accesso alla CPU per il buffer nascosto di una catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="0d75a-125">These flag options are used in a call to the [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow), or [**IDXGIFactory2::CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) method to describe the surface usage and CPU access options for the back buffer of a swap chain.</span></span> <span data-ttu-id="0d75a-126">Non è possibile usare **la \_ \_ condivisione di utilizzo di DXGI**, l' **\_ utilizzo di DXGI \_ scartare \_ sul \_ presente** e i valori di **\_ \_ sola lettura \_** per l'utilizzo di DXGI come input per creare una catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="0d75a-126">You can't use the **DXGI\_USAGE\_SHARED**, **DXGI\_USAGE\_DISCARD\_ON\_PRESENT**, and **DXGI\_USAGE\_READ\_ONLY** values as input to create a swap chain.</span></span> <span data-ttu-id="0d75a-127">Tuttavia, DXGI può impostare **gli \_ \_ scarti di utilizzo di DXGI \_ in \_** caso di utilizzo di DXGI e in **\_ \_ sola lettura \_** per alcuni dei buffer back della catena di scambio per conto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0d75a-127">However, DXGI can set **DXGI\_USAGE\_DISCARD\_ON\_PRESENT** and **DXGI\_USAGE\_READ\_ONLY** for some of the swap chain's back buffers on the application's behalf.</span></span> <span data-ttu-id="0d75a-128">È possibile chiamare il metodo [**IDXGIResource:: getusage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) per recuperare l'utilizzo di questi buffer back.</span><span class="sxs-lookup"><span data-stu-id="0d75a-128">You can call the [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) method to retrieve the usage of these back buffers.</span></span> <span data-ttu-id="0d75a-129">La catena di scambio supporta solo il valore **\_ None di \_ accesso \_ alla CPU DXGI** nel **campo di \_ accesso alla CPU \_ \_ DXGI** parte di **DXGI \_ Usage**.</span><span class="sxs-lookup"><span data-stu-id="0d75a-129">Swap chain's only support the **DXGI\_CPU\_ACCESS\_NONE** value in the **DXGI\_CPU\_ACCESS\_FIELD** part of **DXGI\_USAGE**.</span></span>

<span data-ttu-id="0d75a-130">Queste opzioni dei flag vengono usate anche dal metodo [**IDXGIDevice:: CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) .</span><span class="sxs-lookup"><span data-stu-id="0d75a-130">These flag options are also used by the [**IDXGIDevice::CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d75a-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d75a-131">Requirements</span></span>



| <span data-ttu-id="0d75a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d75a-132">Requirement</span></span> | <span data-ttu-id="0d75a-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0d75a-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0d75a-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d75a-134">Header</span></span><br/> | <dl> <span data-ttu-id="0d75a-135"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d75a-135"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d75a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d75a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d75a-137">Costanti DXGI</span><span class="sxs-lookup"><span data-stu-id="0d75a-137">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




