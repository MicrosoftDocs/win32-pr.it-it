---
description: Queste opzioni identificano i tipi di risorse di query.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eac450ed722da26fe4885d41707483adf401f89
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994108"
---
# <a name="d3dusage_query"></a><span data-ttu-id="9e910-103">D3DUSAGE \_ QUERY</span><span class="sxs-lookup"><span data-stu-id="9e910-103">D3DUSAGE\_QUERY</span></span>

<span data-ttu-id="9e910-104">Queste opzioni identificano i tipi di risorse di query.</span><span class="sxs-lookup"><span data-stu-id="9e910-104">These options identify query resource types.</span></span>



| <span data-ttu-id="9e910-105">\#Definire</span><span class="sxs-lookup"><span data-stu-id="9e910-105">\#define</span></span>                                   | <span data-ttu-id="9e910-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e910-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e910-107">FILTRO QUERY D3DUSAGE \_ \_</span><span class="sxs-lookup"><span data-stu-id="9e910-107">D3DUSAGE\_QUERY\_FILTER</span></span>                    | <span data-ttu-id="9e910-108">Eseguire una query sul formato della risorsa per verificare se supporta tipi di filtro trame diversi da D3DTEXF \_ POINT (che è sempre supportato).</span><span class="sxs-lookup"><span data-stu-id="9e910-108">Query the resource format to see if it supports texture filter types other than D3DTEXF\_POINT (which is always supported).</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="9e910-109">D3DUSAGE \_ QUERY \_ LEGACYBUMPMAP</span><span class="sxs-lookup"><span data-stu-id="9e910-109">D3DUSAGE\_QUERY\_LEGACYBUMPMAP</span></span>             | <span data-ttu-id="9e910-110">Eseguire una query sulla risorsa su una mappa di rilievo legacy.</span><span class="sxs-lookup"><span data-stu-id="9e910-110">Query the resource about a legacy bump map.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="9e910-111">D3DUSAGE \_ QUERY \_ POSTPIXELSHADER \_ BLENDING</span><span class="sxs-lookup"><span data-stu-id="9e910-111">D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING</span></span> | <span data-ttu-id="9e910-112">Eseguire una query sulla risorsa per verificare il supporto per il supporto pixel shader blending.</span><span class="sxs-lookup"><span data-stu-id="9e910-112">Query the resource to verify support for post pixel shader blending support.</span></span> <span data-ttu-id="9e910-113">Se [**CheckDeviceFormat ha**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) esito negativo con D3DUSAGE \_ QUERY \_ POSTPIXELSHADER \_ BLENDING, le operazioni di fusione post-pixel non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="9e910-113">If [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) fails with D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING, post pixel blending operations are not supported.</span></span> <span data-ttu-id="9e910-114">Sono inclusi il test alfa, la nebbia dei pixel, la fusione della destinazione di rendering, l'abilitazione della scrittura dei colori e il dithering.</span><span class="sxs-lookup"><span data-stu-id="9e910-114">These include alpha test, pixel fog, render-target blending, color write enable, and dithering.</span></span> |
| <span data-ttu-id="9e910-115">D3DUSAGE \_ QUERY \_ SRGBREAD</span><span class="sxs-lookup"><span data-stu-id="9e910-115">D3DUSAGE\_QUERY\_SRGBREAD</span></span>                  | <span data-ttu-id="9e910-116">Eseguire una query sulla risorsa per verificare se una trama supporta la correzione gamma durante un'operazione di lettura.</span><span class="sxs-lookup"><span data-stu-id="9e910-116">Query the resource to verify if a texture supports gamma correction during a read operation.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9e910-117">D3DUSAGE \_ QUERY \_ SRGBWRITE</span><span class="sxs-lookup"><span data-stu-id="9e910-117">D3DUSAGE\_QUERY\_SRGBWRITE</span></span>                 | <span data-ttu-id="9e910-118">Eseguire una query sulla risorsa per verificare se una trama supporta la correzione gamma durante un'operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="9e910-118">Query the resource to verify if a texture supports gamma correction during a write operation.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9e910-119">D3DUSAGE \_ QUERY \_ VERTEXTEXTURE</span><span class="sxs-lookup"><span data-stu-id="9e910-119">D3DUSAGE\_QUERY\_VERTEXTEXTURE</span></span>             | <span data-ttu-id="9e910-120">Eseguire una query sulla risorsa per verificare il supporto per il campionamento delle trame dei vertex shader.</span><span class="sxs-lookup"><span data-stu-id="9e910-120">Query the resource to verify support for vertex shader texture sampling.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="9e910-121">D3DUSAGE \_ QUERY \_ WRAPANDMIP</span><span class="sxs-lookup"><span data-stu-id="9e910-121">D3DUSAGE\_QUERY\_WRAPANDMIP</span></span>                | <span data-ttu-id="9e910-122">Eseguire una query sulla risorsa per verificare il supporto per il wrapping delle trame e il mapping mip.</span><span class="sxs-lookup"><span data-stu-id="9e910-122">Query the resource to verify support for texture wrapping and mip-mapping.</span></span>                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="9e910-123">Usare [**CheckDeviceFormat per**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) eseguire query sul supporto hardware per questi utilizzi e su altri utilizzi elencati in [D3DUSAGE](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="9e910-123">Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) to query hardware support for these usages, and some other usages listed in [D3DUSAGE](d3dusage.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="9e910-124">Informazioni costanti</span><span class="sxs-lookup"><span data-stu-id="9e910-124">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="9e910-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e910-125">Header</span></span>                   | <span data-ttu-id="9e910-126">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="9e910-126">d3d9types.h</span></span> |
| <span data-ttu-id="9e910-127">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="9e910-127">Minimum operating system</span></span> | <span data-ttu-id="9e910-128">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9e910-128">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="9e910-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9e910-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e910-130">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="9e910-130">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
