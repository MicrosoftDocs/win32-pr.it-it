---
description: Restituisce una descrizione del contenuto originale di un file di immagine.
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: Struttura D3DX10_IMAGE_INFO (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: bf240296610c083e0d042d187ae29054461193a8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354439"
---
# <a name="d3dx10_image_info-structure"></a><span data-ttu-id="9d7d6-103">Struttura delle informazioni sull' \_ immagine d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="9d7d6-103">D3DX10\_IMAGE\_INFO structure</span></span>

<span data-ttu-id="9d7d6-104">Restituisce una descrizione del contenuto originale di un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="9d7d6-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d7d6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d7d6-105">Syntax</span></span>


```C++
typedef struct D3DX10_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D10_RESOURCE_DIMENSION ResourceDimension;
  D3DX10_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX10_IMAGE_INFO, *LPD3DX10_IMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="9d7d6-106">Members</span><span class="sxs-lookup"><span data-stu-id="9d7d6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d7d6-107">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="9d7d6-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d7d6-109">Larghezza dell'immagine originale in pixel.</span><span class="sxs-lookup"><span data-stu-id="9d7d6-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9d7d6-110">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="9d7d6-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d7d6-112">Altezza dell'immagine originale in pixel.</span><span class="sxs-lookup"><span data-stu-id="9d7d6-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9d7d6-113">**Livello nidificazione**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="9d7d6-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d7d6-115">Profondità dell'immagine originale in pixel.</span><span class="sxs-lookup"><span data-stu-id="9d7d6-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9d7d6-116">**ArraySize**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-116">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="9d7d6-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d7d6-118">Dimensioni della matrice di trama.</span><span class="sxs-lookup"><span data-stu-id="9d7d6-118">Size of the texture array.</span></span> <span data-ttu-id="9d7d6-119">*ArraySize* sarà 1 per una singola immagine.</span><span class="sxs-lookup"><span data-stu-id="9d7d6-119">*ArraySize* will be 1 for a single image.</span></span>

</dd> <dt>

<span data-ttu-id="9d7d6-120">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-120">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="9d7d6-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d7d6-122">Numero di livelli di mipmap nell'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="9d7d6-122">Number of mipmap levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="9d7d6-123">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-123">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="9d7d6-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d7d6-125">Proprietà delle risorse varie ( [**vedere \_ \_ \_ flag varie della risorsa D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="9d7d6-125">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="9d7d6-126">**Formato**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-126">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="9d7d6-127">Tipo: **[ **DXGI \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-127">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="9d7d6-128">Valore del tipo enumerato del [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) che descrive più accuratamente i dati nell'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="9d7d6-128">A value from the [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="9d7d6-129">**ResourceDimension**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-129">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="9d7d6-130">Tipo: **[ **\_ \_ dimensione della risorsa D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-130">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="9d7d6-131">Rappresenta il tipo di trama archiviato nel file.</span><span class="sxs-lookup"><span data-stu-id="9d7d6-131">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="9d7d6-132">Vedere [**\_ \_ dimensione della risorsa D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span><span class="sxs-lookup"><span data-stu-id="9d7d6-132">See [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span></span>

</dd> <dt>

<span data-ttu-id="9d7d6-133">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-133">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="9d7d6-134">Tipo: **[ **d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="9d7d6-134">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d7d6-135">Rappresenta il formato del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="9d7d6-135">Represents the format of the image file.</span></span> <span data-ttu-id="9d7d6-136">Vedere [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="9d7d6-136">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d7d6-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d7d6-137">Requirements</span></span>



| <span data-ttu-id="9d7d6-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d7d6-138">Requirement</span></span> | <span data-ttu-id="9d7d6-139">Valore</span><span class="sxs-lookup"><span data-stu-id="9d7d6-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9d7d6-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9d7d6-140">Header</span></span><br/> | <dl> <span data-ttu-id="9d7d6-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d7d6-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d7d6-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d7d6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d7d6-143">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="9d7d6-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
