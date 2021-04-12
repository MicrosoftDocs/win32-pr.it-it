---
description: Queste opzioni identificano i tipi di risorse della query.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f5dda7f84dfa36e4f3b7ece1b359a4841bbbf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126878"
---
# <a name="d3dusage_query"></a><span data-ttu-id="6eac4-103">\_Query D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="6eac4-103">D3DUSAGE\_QUERY</span></span>

<span data-ttu-id="6eac4-104">Queste opzioni identificano i tipi di risorse della query.</span><span class="sxs-lookup"><span data-stu-id="6eac4-104">These options identify query resource types.</span></span>



|                                            |                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eac4-105">\#definire</span><span class="sxs-lookup"><span data-stu-id="6eac4-105">\#define</span></span>                                   | <span data-ttu-id="6eac4-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6eac4-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="6eac4-107">\_Filtro query \_ D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="6eac4-107">D3DUSAGE\_QUERY\_FILTER</span></span>                    | <span data-ttu-id="6eac4-108">Eseguire una query sul formato di risorsa per verificare se supporta i tipi di filtro di trama diversi dal punto di D3DTEXF, \_ che è sempre supportato.</span><span class="sxs-lookup"><span data-stu-id="6eac4-108">Query the resource format to see if it supports texture filter types other than D3DTEXF\_POINT (which is always supported).</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="6eac4-109">\_LEGACYBUMPMAP query \_ D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="6eac4-109">D3DUSAGE\_QUERY\_LEGACYBUMPMAP</span></span>             | <span data-ttu-id="6eac4-110">Eseguire una query sulla risorsa relativa a una mappa Bump legacy.</span><span class="sxs-lookup"><span data-stu-id="6eac4-110">Query the resource about a legacy bump map.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="6eac4-111">D3DUSAGE \_ query \_ POSTPIXELSHADER \_ blending</span><span class="sxs-lookup"><span data-stu-id="6eac4-111">D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING</span></span> | <span data-ttu-id="6eac4-112">Eseguire una query sulla risorsa per verificare il supporto per il supporto di post pixel shader blending.</span><span class="sxs-lookup"><span data-stu-id="6eac4-112">Query the resource to verify support for post pixel shader blending support.</span></span> <span data-ttu-id="6eac4-113">Se [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) ha esito negativo con D3DUSAGE \_ query \_ POSTPIXELSHADER \_ blending, le operazioni successive alla fusione dei pixel non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="6eac4-113">If [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) fails with D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING, post pixel blending operations are not supported.</span></span> <span data-ttu-id="6eac4-114">Sono inclusi test alfa, nebbia pixel, Blend di destinazione di rendering, abilitazione della scrittura di colori e dithering.</span><span class="sxs-lookup"><span data-stu-id="6eac4-114">These include alpha test, pixel fog, render-target blending, color write enable, and dithering.</span></span> |
| <span data-ttu-id="6eac4-115">\_SRGBREAD query \_ D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="6eac4-115">D3DUSAGE\_QUERY\_SRGBREAD</span></span>                  | <span data-ttu-id="6eac4-116">Eseguire una query sulla risorsa per verificare se una trama supporta la correzione gamma durante un'operazione di lettura.</span><span class="sxs-lookup"><span data-stu-id="6eac4-116">Query the resource to verify if a texture supports gamma correction during a read operation.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="6eac4-117">\_SRGBWRITE query \_ D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="6eac4-117">D3DUSAGE\_QUERY\_SRGBWRITE</span></span>                 | <span data-ttu-id="6eac4-118">Eseguire una query sulla risorsa per verificare se una trama supporta la correzione gamma durante un'operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="6eac4-118">Query the resource to verify if a texture supports gamma correction during a write operation.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="6eac4-119">\_VERTEXTEXTURE query \_ D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="6eac4-119">D3DUSAGE\_QUERY\_VERTEXTEXTURE</span></span>             | <span data-ttu-id="6eac4-120">Eseguire una query sulla risorsa per verificare il supporto per il campionamento di trama vertex shader.</span><span class="sxs-lookup"><span data-stu-id="6eac4-120">Query the resource to verify support for vertex shader texture sampling.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="6eac4-121">\_WRAPANDMIP query \_ D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="6eac4-121">D3DUSAGE\_QUERY\_WRAPANDMIP</span></span>                | <span data-ttu-id="6eac4-122">Eseguire una query sulla risorsa per verificare il supporto per il wrapping della trama e il mapping MIP.</span><span class="sxs-lookup"><span data-stu-id="6eac4-122">Query the resource to verify support for texture wrapping and mip-mapping.</span></span>                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="6eac4-123">Usare [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) per eseguire query sul supporto hardware per questi usi e altri utilizzi elencati in [D3DUSAGE](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="6eac4-123">Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) to query hardware support for these usages, and some other usages listed in [D3DUSAGE](d3dusage.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="6eac4-124">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="6eac4-124">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="6eac4-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6eac4-125">Header</span></span>                   | <span data-ttu-id="6eac4-126">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="6eac4-126">d3d9types.h</span></span> |
| <span data-ttu-id="6eac4-127">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="6eac4-127">Minimum operating system</span></span> | <span data-ttu-id="6eac4-128">Windows 98</span><span class="sxs-lookup"><span data-stu-id="6eac4-128">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="6eac4-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6eac4-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6eac4-130">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="6eac4-130">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
