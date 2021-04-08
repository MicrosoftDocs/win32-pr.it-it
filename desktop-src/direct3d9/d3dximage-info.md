---
description: Restituisce una descrizione del contenuto originale di un file di immagine.
ms.assetid: d6cbd5b7-642e-43ce-a2ed-11a400c5bdc1
title: Struttura D3DXIMAGE_INFO (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_INFO
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: 6ec152dc56dcea3a718cf5cd42fb351d4fddf852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762035"
---
# <a name="d3dximage_info-structure"></a><span data-ttu-id="43b69-103">Struttura delle informazioni di D3DXIMAGE \_</span><span class="sxs-lookup"><span data-stu-id="43b69-103">D3DXIMAGE\_INFO structure</span></span>

<span data-ttu-id="43b69-104">Restituisce una descrizione del contenuto originale di un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="43b69-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="43b69-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43b69-105">Syntax</span></span>


```C++
typedef struct D3DXIMAGE_INFO {
  UINT                 Width;
  UINT                 Height;
  UINT                 Depth;
  UINT                 MipLevels;
  D3DFORMAT            Format;
  D3DRESOURCETYPE      ResourceType;
  D3DXIMAGE_FILEFORMAT ImageFileFormat;
} D3DXIMAGE_INFO, *LPD3DXIMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="43b69-106">Members</span><span class="sxs-lookup"><span data-stu-id="43b69-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="43b69-107">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="43b69-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="43b69-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43b69-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43b69-109">Larghezza dell'immagine originale in pixel.</span><span class="sxs-lookup"><span data-stu-id="43b69-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="43b69-110">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="43b69-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="43b69-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43b69-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43b69-112">Altezza dell'immagine originale in pixel.</span><span class="sxs-lookup"><span data-stu-id="43b69-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="43b69-113">**Livello nidificazione**</span><span class="sxs-lookup"><span data-stu-id="43b69-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="43b69-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43b69-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43b69-115">Profondità dell'immagine originale in pixel.</span><span class="sxs-lookup"><span data-stu-id="43b69-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="43b69-116">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="43b69-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="43b69-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43b69-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43b69-118">Numero di livelli MIP nell'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="43b69-118">Number of mip levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="43b69-119">**Formato**</span><span class="sxs-lookup"><span data-stu-id="43b69-119">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="43b69-120">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="43b69-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43b69-121">Valore del tipo enumerato [D3DFORMAT](d3dformat.md) che descrive più accuratamente i dati nell'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="43b69-121">A value from the [D3DFORMAT](d3dformat.md) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="43b69-122">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="43b69-122">**ResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="43b69-123">Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="43b69-123">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43b69-124">Rappresenta il tipo di trama archiviato nel file.</span><span class="sxs-lookup"><span data-stu-id="43b69-124">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="43b69-125">Si tratta di una \_ trama D3DRTYPE, D3DRTYPE \_ VOLUMETEXTURE o D3DRTYPE \_ CubeTexture.</span><span class="sxs-lookup"><span data-stu-id="43b69-125">It is either D3DRTYPE\_TEXTURE, D3DRTYPE\_VOLUMETEXTURE, or D3DRTYPE\_CubeTexture.</span></span>

</dd> <dt>

<span data-ttu-id="43b69-126">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="43b69-126">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="43b69-127">Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="43b69-127">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43b69-128">Rappresenta il formato del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="43b69-128">Represents the format of the image file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43b69-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43b69-129">Requirements</span></span>



| <span data-ttu-id="43b69-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="43b69-130">Requirement</span></span> | <span data-ttu-id="43b69-131">Valore</span><span class="sxs-lookup"><span data-stu-id="43b69-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43b69-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43b69-132">Header</span></span><br/> | <dl> <span data-ttu-id="43b69-133"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="43b69-133"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43b69-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43b69-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43b69-135">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="43b69-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
