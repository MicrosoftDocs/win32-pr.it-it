---
description: "Flag sprite che indicano all'API di disegno sprite come si comportano. Questi vengono passati in ID3DX10Sprite:: Begin."
ms.assetid: 734096e6-1482-479c-b287-a77a4695487c
title: Enumerazione D3DX10_SPRITE_FLAG (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 21ba4f035b43b1a002b014909fb4d0a02a64d1e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323383"
---
# <a name="d3dx10_sprite_flag-enumeration"></a><span data-ttu-id="515f7-104">\_ \_ Enumerazione flag d3dx10 sprite</span><span class="sxs-lookup"><span data-stu-id="515f7-104">D3DX10\_SPRITE\_FLAG enumeration</span></span>

<span data-ttu-id="515f7-105">Flag sprite che indicano all'API di disegno sprite come si comportano.</span><span class="sxs-lookup"><span data-stu-id="515f7-105">Sprite flags that tell the sprite drawing API how to behave.</span></span> <span data-ttu-id="515f7-106">Questi vengono passati in [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md).</span><span class="sxs-lookup"><span data-stu-id="515f7-106">These are passed into [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="515f7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="515f7-107">Syntax</span></span>


```C++
typedef enum D3DX10_SPRITE_FLAG { 
  D3DX10_SPRITE_SORT_TEXTURE              = 0x01,
  D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT  = 0x02,
  D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK  = 0x04,
  D3DX10_SPRITE_SAVE_STATE                = 0x08,
  D3DX10_SPRITE_ADDREF_TEXTURES           = 0x10
} D3DX10_SPRITE_FLAG, *LPD3DX10_SPRITE_FLAG;
```



## <a name="constants"></a><span data-ttu-id="515f7-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="515f7-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="515f7-109"><span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**\_Trama di \_ ordinamento \_ sprite d3dx10**</span><span class="sxs-lookup"><span data-stu-id="515f7-109"><span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**D3DX10\_SPRITE\_SORT\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="515f7-110">Ordinare gli sprite in base alla trama prima del rendering in modo che, quando ci sono molti sprite con la stessa trama che verrà eseguito il rendering di tutti gli sprite, in modo da migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="515f7-110">Sort the sprites by texture before rendering so that when there are many sprites with the same texture that texture all of those sprites will be rendered at the same time, thereby improving performance.</span></span>

</dd> <dt>

<span data-ttu-id="515f7-111"><span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**\_ \_ \_ Profondità di ordinamento sprite \_ di d3dx10 \_ di nuovo in \_ primo piano**</span><span class="sxs-lookup"><span data-stu-id="515f7-111"><span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10\_SPRITE\_SORT\_DEPTH\_BACK\_TO\_FRONT**</span></span>
</dt> <dd>

<span data-ttu-id="515f7-112">Ordinare gli sprite da un inizio all'altra per fare in modo che quelli più lontani dalla fotocamera vengano disegnati per primi.</span><span class="sxs-lookup"><span data-stu-id="515f7-112">Sort the sprites from back to front to that those farther away from the camera will be drawn first.</span></span>

</dd> <dt>

<span data-ttu-id="515f7-113"><span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**\_ \_ Profondità di ordinamento dello sprite d3dx10 \_ \_ \_ da fronte a \_ sfondo**</span><span class="sxs-lookup"><span data-stu-id="515f7-113"><span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3DX10\_SPRITE\_SORT\_DEPTH\_FRONT\_TO\_BACK**</span></span>
</dt> <dd>

<span data-ttu-id="515f7-114">Ordinare gli sprite dalla parte anteriore a quella posteriore in modo da disegnare prima quelli più vicini alla fotocamera.</span><span class="sxs-lookup"><span data-stu-id="515f7-114">Sort the sprites from front to back so that those closer to the camera will be drawn first.</span></span>

</dd> <dt>

<span data-ttu-id="515f7-115"><span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**\_ \_ Stato salvataggio sprite \_ d3dx10**</span><span class="sxs-lookup"><span data-stu-id="515f7-115"><span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10\_SPRITE\_SAVE\_STATE**</span></span>
</dt> <dd>

<span data-ttu-id="515f7-116">Salva lo stato in modo che quando viene chiamato [**ID3DX10Sprite:: end**](id3dx10sprite-end.md) , lo stato viene ripristinato come prima della chiamata a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="515f7-116">Saves the state so that when [**ID3DX10Sprite::End**](id3dx10sprite-end.md) is called, it will restore the state to the way it was before [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) was called.</span></span>

</dd> <dt>

<span data-ttu-id="515f7-117"><span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**\_ \_ Trame d3dx10 sprite ADDREF \_**</span><span class="sxs-lookup"><span data-stu-id="515f7-117"><span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**D3DX10\_SPRITE\_ADDREF\_TEXTURES**</span></span>
</dt> <dd>

<span data-ttu-id="515f7-118">Chiama AddRef su tutte le trame quando vengono passate in [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md).</span><span class="sxs-lookup"><span data-stu-id="515f7-118">Calls AddRef on all of the textures when they are passed into [**ID3DX10Sprite::DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="515f7-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="515f7-119">Remarks</span></span>

<span data-ttu-id="515f7-120">Dopo l'esecuzione di un ordinamento front-to-back o back-to-front, viene eseguito automaticamente un ordinamento secondario per trama.</span><span class="sxs-lookup"><span data-stu-id="515f7-120">After a front-to-back or back-to-front sort is done, it will automatically do a secondary sort by texture.</span></span> <span data-ttu-id="515f7-121">Questa operazione è utile quando sono presenti molti sprite con la stessa trama nello stesso piano, ad esempio quando si disegna l'interfaccia utente in un gioco.</span><span class="sxs-lookup"><span data-stu-id="515f7-121">This is helpful for when there are many sprites with the same texture all on the same plane, such as when drawing the user interface in a game.</span></span>

## <a name="requirements"></a><span data-ttu-id="515f7-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="515f7-122">Requirements</span></span>



| <span data-ttu-id="515f7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="515f7-123">Requirement</span></span> | <span data-ttu-id="515f7-124">Valore</span><span class="sxs-lookup"><span data-stu-id="515f7-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="515f7-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="515f7-125">Header</span></span><br/> | <dl> <span data-ttu-id="515f7-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="515f7-126"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="515f7-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="515f7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="515f7-128">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="515f7-128">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




