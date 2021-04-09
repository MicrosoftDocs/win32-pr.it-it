---
title: Effetto dei metadati di opacità
description: È possibile utilizzare questo effetto per contrassegnare un'area di un'immagine di input come opaca, in modo che sia possibile ottimizzare il rendering interno del grafico.
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84d90ba1c4b1186e3e682ec94a0c9c17bdfc73e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120950"
---
# <a name="opacity-metadata-effect"></a><span data-ttu-id="1dc27-103">Effetto dei metadati di opacità</span><span class="sxs-lookup"><span data-stu-id="1dc27-103">Opacity metadata effect</span></span>

<span data-ttu-id="1dc27-104">È possibile utilizzare questo effetto per contrassegnare un'area di un'immagine di input come opaca, in modo che sia possibile ottimizzare il rendering interno del grafico.</span><span class="sxs-lookup"><span data-stu-id="1dc27-104">You can use this effect to mark an area of an input image as opaque, so internal rendering optimizations to the graph are possible.</span></span>

> [!Note]  
> <span data-ttu-id="1dc27-105">Questo effetto non modifica l'immagine in modo che sia opaca.</span><span class="sxs-lookup"><span data-stu-id="1dc27-105">This effect doesn't modify the image itself to be opaque.</span></span> <span data-ttu-id="1dc27-106">Modifica i dati associati all'immagine in modo che il renderer presupponga che l'area specificata sia opaca.</span><span class="sxs-lookup"><span data-stu-id="1dc27-106">It modifies data associated with the image so the renderer assumes the specified region is opaque.</span></span>

 

<span data-ttu-id="1dc27-107">Il CLSID per questo effetto è CLSID \_ D2D1OpacityMetadata.</span><span class="sxs-lookup"><span data-stu-id="1dc27-107">The CLSID for this effect is CLSID\_D2D1OpacityMetadata.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="1dc27-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="1dc27-108">Effect properties</span></span>



| <span data-ttu-id="1dc27-109">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="1dc27-109">Display name and index enumeration</span></span>                                                 | <span data-ttu-id="1dc27-110">Tipo e valore predefinito</span><span class="sxs-lookup"><span data-stu-id="1dc27-110">Type and default value</span></span>                                                             | <span data-ttu-id="1dc27-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dc27-111">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc27-112">OutputRect</span><span class="sxs-lookup"><span data-stu-id="1dc27-112">OutputRect</span></span><br/> <span data-ttu-id="1dc27-113">D2D1 \_ OPACITYMETADATA \_ - \_ input \_ opaco \_ Rect</span><span class="sxs-lookup"><span data-stu-id="1dc27-113">D2D1\_OPACITYMETADATA\_PROP\_INPUT\_OPAQUE\_RECT</span></span> <br/> | <span data-ttu-id="1dc27-114">D2D1 \_ vector \_ 4F</span><span class="sxs-lookup"><span data-stu-id="1dc27-114">D2D1\_VECTOR\_4F</span></span><br/> <span data-ttu-id="1dc27-115">(-FLT \_ MAX,-FLT \_ Max, flt \_ Max, flt \_ max)</span><span class="sxs-lookup"><span data-stu-id="1dc27-115">(-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX)</span></span> <br/> | <span data-ttu-id="1dc27-116">Parte dell'immagine di origine opaca.</span><span class="sxs-lookup"><span data-stu-id="1dc27-116">The portion of the source image that is opaque.</span></span> <span data-ttu-id="1dc27-117">Il valore predefinito è l'intera immagine di input.</span><span class="sxs-lookup"><span data-stu-id="1dc27-117">The default is the entire input image.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1dc27-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dc27-118">Requirements</span></span>



| <span data-ttu-id="1dc27-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dc27-119">Requirement</span></span> | <span data-ttu-id="1dc27-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1dc27-120">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc27-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dc27-121">Minimum supported client</span></span> | <span data-ttu-id="1dc27-122">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="1dc27-122">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="1dc27-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dc27-123">Minimum supported server</span></span> | <span data-ttu-id="1dc27-124">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="1dc27-124">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="1dc27-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1dc27-125">Header</span></span>                   | <span data-ttu-id="1dc27-126">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="1dc27-126">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="1dc27-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="1dc27-127">Library</span></span>                  | <span data-ttu-id="1dc27-128">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="1dc27-128">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="1dc27-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1dc27-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dc27-130">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="1dc27-130">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

