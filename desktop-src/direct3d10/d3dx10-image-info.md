---
description: 'D3DX10_IMAGE_INFO struttura : restituisce una descrizione del contenuto originale di un file di immagine.'
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: D3DX10_IMAGE_INFO struttura (D3DX10.h)
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
ms.openlocfilehash: 228ddf777217e9e61369b0a7fc3b3eb1ca012b1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105479"
---
# <a name="d3dx10_image_info-structure"></a><span data-ttu-id="8ff6b-103">Struttura D3DX10 \_ IMAGE \_ INFO</span><span class="sxs-lookup"><span data-stu-id="8ff6b-103">D3DX10\_IMAGE\_INFO structure</span></span>

<span data-ttu-id="8ff6b-104">Restituisce una descrizione del contenuto originale di un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="8ff6b-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ff6b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ff6b-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="8ff6b-106">Members</span><span class="sxs-lookup"><span data-stu-id="8ff6b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8ff6b-107">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="8ff6b-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ff6b-109">Larghezza dell'immagine originale in pixel.</span><span class="sxs-lookup"><span data-stu-id="8ff6b-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8ff6b-110">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="8ff6b-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ff6b-112">Altezza dell'immagine originale in pixel.</span><span class="sxs-lookup"><span data-stu-id="8ff6b-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8ff6b-113">**Livello nidificazione**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="8ff6b-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ff6b-115">Profondità dell'immagine originale in pixel.</span><span class="sxs-lookup"><span data-stu-id="8ff6b-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8ff6b-116">**ArraySize**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-116">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="8ff6b-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ff6b-118">Dimensioni della matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="8ff6b-118">Size of the texture array.</span></span> <span data-ttu-id="8ff6b-119">*ArraySize* sarà 1 per una singola immagine.</span><span class="sxs-lookup"><span data-stu-id="8ff6b-119">*ArraySize* will be 1 for a single image.</span></span>

</dd> <dt>

<span data-ttu-id="8ff6b-120">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-120">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="8ff6b-121">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ff6b-122">Numero di livelli mipmap nell'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="8ff6b-122">Number of mipmap levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="8ff6b-123">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-123">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8ff6b-124">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ff6b-125">Proprietà delle risorse varie (vedere [**D3D10 \_ RESOURCE \_ MISC \_ FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="8ff6b-125">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="8ff6b-126">**Formato**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-126">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="8ff6b-127">Tipo: **[ **FORMATO \_ DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-127">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="8ff6b-128">Valore del tipo [**enumerato DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) che descrive più da vicino i dati nell'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="8ff6b-128">A value from the [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="8ff6b-129">**ResourceDimension**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-129">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="8ff6b-130">Tipo: **[ **DIMENSIONE RISORSA \_ \_ D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-130">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="8ff6b-131">Rappresenta il tipo della trama archiviata nel file.</span><span class="sxs-lookup"><span data-stu-id="8ff6b-131">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="8ff6b-132">Vedere [**D3D10 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span><span class="sxs-lookup"><span data-stu-id="8ff6b-132">See [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span></span>

</dd> <dt>

<span data-ttu-id="8ff6b-133">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-133">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="8ff6b-134">Tipo: **[ **D3DX10 \_ IMAGE \_ FILE \_ FORMAT**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="8ff6b-134">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ff6b-135">Rappresenta il formato del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="8ff6b-135">Represents the format of the image file.</span></span> <span data-ttu-id="8ff6b-136">Vedere [**D3DX10 \_ IMAGE FILE \_ \_ FORMAT**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="8ff6b-136">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ff6b-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ff6b-137">Requirements</span></span>



| <span data-ttu-id="8ff6b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ff6b-138">Requirement</span></span> | <span data-ttu-id="8ff6b-139">Valore</span><span class="sxs-lookup"><span data-stu-id="8ff6b-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff6b-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ff6b-140">Header</span></span><br/> | <dl> <span data-ttu-id="8ff6b-141"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="8ff6b-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ff6b-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ff6b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ff6b-143">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="8ff6b-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
