---
description: Definisce le informazioni sulla posizione, sulla trama e sul colore di uno sprite.
ms.assetid: 4b8d1ed1-75d5-418c-b809-410c6a44d425
title: Struttura D3DX10_SPRITE (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: b896b8158e84caa841addbac7abae8c972c06acd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323382"
---
# <a name="d3dx10_sprite-structure"></a><span data-ttu-id="f91fd-103">\_Struttura d3dx10 sprite</span><span class="sxs-lookup"><span data-stu-id="f91fd-103">D3DX10\_SPRITE structure</span></span>

<span data-ttu-id="f91fd-104">Definisce le informazioni sulla posizione, sulla trama e sul colore di uno sprite.</span><span class="sxs-lookup"><span data-stu-id="f91fd-104">Defines position, texture, and color information about a sprite.</span></span>

## <a name="syntax"></a><span data-ttu-id="f91fd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f91fd-105">Syntax</span></span>


```C++
typedef struct D3DX10_SPRITE {
  D3DXMATRIX               matWorld;
  D3DXVECTOR2              TexCoord;
  D3DXVECTOR2              TexSize;
  D3DXCOLOR                ColorModulate;
  ID3D10ShaderResourceView *pTexture;
  UINT                     TextureIndex;
} D3DX10_SPRITE;
```



## <a name="members"></a><span data-ttu-id="f91fd-106">Members</span><span class="sxs-lookup"><span data-stu-id="f91fd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f91fd-107">**matWorld**</span><span class="sxs-lookup"><span data-stu-id="f91fd-107">**matWorld**</span></span>
</dt> <dd>

<span data-ttu-id="f91fd-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="f91fd-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f91fd-109">Trasformazione del mondo del modello dello sprite.</span><span class="sxs-lookup"><span data-stu-id="f91fd-109">The sprite's model-world transformation.</span></span> <span data-ttu-id="f91fd-110">Definisce la posizione e l'orientamento dello sprite nello spazio globale.</span><span class="sxs-lookup"><span data-stu-id="f91fd-110">This defines the position and orientation of the sprite in world space.</span></span>

</dd> <dt>

<span data-ttu-id="f91fd-111">**TexCoord**</span><span class="sxs-lookup"><span data-stu-id="f91fd-111">**TexCoord**</span></span>
</dt> <dd>

<span data-ttu-id="f91fd-112">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span><span class="sxs-lookup"><span data-stu-id="f91fd-112">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f91fd-113">Offset dall'angolo superiore sinistro della trama che indica dove deve essere avviata l'immagine sprite nella trama.</span><span class="sxs-lookup"><span data-stu-id="f91fd-113">Offset from the upper-left corner of the texture indicating where the sprite image should start in the texture.</span></span> <span data-ttu-id="f91fd-114">**TexCoord** è nelle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="f91fd-114">**TexCoord** is in texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="f91fd-115">**TexSize**</span><span class="sxs-lookup"><span data-stu-id="f91fd-115">**TexSize**</span></span>
</dt> <dd>

<span data-ttu-id="f91fd-116">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span><span class="sxs-lookup"><span data-stu-id="f91fd-116">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f91fd-117">Vettore che contiene la larghezza e l'altezza dello sprite nelle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="f91fd-117">A vector containing the width and height of the sprite in texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="f91fd-118">**ColorModulate**</span><span class="sxs-lookup"><span data-stu-id="f91fd-118">**ColorModulate**</span></span>
</dt> <dd>

<span data-ttu-id="f91fd-119">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="f91fd-119">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f91fd-120">Colore che verrà moltiplicato con il colore del pixel prima del rendering.</span><span class="sxs-lookup"><span data-stu-id="f91fd-120">A color that will be multiplied with the pixel color before rendering.</span></span>

</dd> <dt>

<span data-ttu-id="f91fd-121">**pTexture**</span><span class="sxs-lookup"><span data-stu-id="f91fd-121">**pTexture**</span></span>
</dt> <dd>

<span data-ttu-id="f91fd-122">Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="f91fd-122">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***</span></span>

</dd> <dd>

<span data-ttu-id="f91fd-123">Puntatore a una visualizzazione risorse dello shader che rappresenta la trama dello sprite.</span><span class="sxs-lookup"><span data-stu-id="f91fd-123">Pointer to a shader-resource view representing the sprite's texture.</span></span> <span data-ttu-id="f91fd-124">Vedere [**interfaccia ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="f91fd-124">See [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="f91fd-125">**TextureIndex**</span><span class="sxs-lookup"><span data-stu-id="f91fd-125">**TextureIndex**</span></span>
</dt> <dd>

<span data-ttu-id="f91fd-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f91fd-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f91fd-127">Indice della trama.</span><span class="sxs-lookup"><span data-stu-id="f91fd-127">The index of the texture.</span></span> <span data-ttu-id="f91fd-128">Se pTexture non rappresenta una matrice di trama, deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="f91fd-128">If pTexture does not represent a texture array, then this should be 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f91fd-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f91fd-129">Requirements</span></span>



| <span data-ttu-id="f91fd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f91fd-130">Requirement</span></span> | <span data-ttu-id="f91fd-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f91fd-131">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f91fd-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f91fd-132">Header</span></span><br/> | <dl> <span data-ttu-id="f91fd-133"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f91fd-133"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f91fd-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f91fd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f91fd-135">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="f91fd-135">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
