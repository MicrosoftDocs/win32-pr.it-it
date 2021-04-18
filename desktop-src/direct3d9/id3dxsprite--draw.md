---
description: Aggiunge uno sprite all'elenco di sprite in batch.
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: 'ID3DXSprite: Metodo Raw:D (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cba7b12c55e7ab9f5f939347a8b500ec4965f75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323519"
---
# <a name="id3dxspritedraw-method"></a><span data-ttu-id="eba49-103">ID3DXSprite::D Metodo Raw</span><span class="sxs-lookup"><span data-stu-id="eba49-103">ID3DXSprite::Draw method</span></span>

<span data-ttu-id="eba49-104">Aggiunge uno sprite all'elenco di sprite in batch.</span><span class="sxs-lookup"><span data-stu-id="eba49-104">Adds a sprite to the list of batched sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="eba49-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eba49-105">Syntax</span></span>


```C++
HRESULT Draw(
  [in]       LPDIRECT3DTEXTURE9 pTexture,
  [in] const RECT               *pSrcRect,
  [in] const D3DXVECTOR3        *pCenter,
  [in] const D3DXVECTOR3        *pPosition,
  [in]       D3DCOLOR           Color
);
```



## <a name="parameters"></a><span data-ttu-id="eba49-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eba49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eba49-107">*pTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eba49-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba49-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="eba49-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="eba49-109">Puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta la trama sprite.</span><span class="sxs-lookup"><span data-stu-id="eba49-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the sprite texture.</span></span>

</dd> <dt>

<span data-ttu-id="eba49-110">*pSrcRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eba49-110">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba49-111">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="eba49-111">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="eba49-112">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che indica la parte della trama di origine da usare per lo sprite.</span><span class="sxs-lookup"><span data-stu-id="eba49-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that indicates the portion of the source texture to use for the sprite.</span></span> <span data-ttu-id="eba49-113">Se questo parametro è **null**, viene usata l'intera immagine di origine per lo sprite.</span><span class="sxs-lookup"><span data-stu-id="eba49-113">If this parameter is **NULL**, then the entire source image is used for the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="eba49-114">*pCenter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eba49-114">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba49-115">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="eba49-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="eba49-116">Puntatore a un vettore [**D3DXVECTOR3**](d3dxvector3.md) che identifica il centro dello sprite.</span><span class="sxs-lookup"><span data-stu-id="eba49-116">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the center of the sprite.</span></span> <span data-ttu-id="eba49-117">Se questo argomento è **null**, viene utilizzato il punto (0, 0, 0), ovvero l'angolo superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="eba49-117">If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.</span></span>

</dd> <dt>

<span data-ttu-id="eba49-118">*pPosition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eba49-118">*pPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba49-119">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="eba49-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="eba49-120">Puntatore a un vettore [**D3DXVECTOR3**](d3dxvector3.md) che identifica la posizione dello sprite.</span><span class="sxs-lookup"><span data-stu-id="eba49-120">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the position of the sprite.</span></span> <span data-ttu-id="eba49-121">Se questo argomento è **null**, viene utilizzato il punto (0, 0, 0), ovvero l'angolo superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="eba49-121">If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.</span></span>

</dd> <dt>

<span data-ttu-id="eba49-122">*Colore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eba49-122">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba49-123">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="eba49-123">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="eba49-124">Tipo [**D3DCOLOR**](d3dcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="eba49-124">[**D3DCOLOR**](d3dcolor.md) type.</span></span> <span data-ttu-id="eba49-125">Il colore e i canali alfa vengono modulati in base a questo valore.</span><span class="sxs-lookup"><span data-stu-id="eba49-125">The color and alpha channels are modulated by this value.</span></span> <span data-ttu-id="eba49-126">Il valore 0xFFFFFFFF mantiene il colore di origine e i dati alfa originali.</span><span class="sxs-lookup"><span data-stu-id="eba49-126">A value of 0xFFFFFFFF maintains the original source color and alpha data.</span></span> <span data-ttu-id="eba49-127">Usare la macro [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) per generare questo colore.</span><span class="sxs-lookup"><span data-stu-id="eba49-127">Use the [**D3DCOLOR\_RGBA**](d3dcolor-rgba.md) macro to help generate this color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eba49-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eba49-128">Return value</span></span>

<span data-ttu-id="eba49-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eba49-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eba49-130">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eba49-130">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="eba49-131">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="eba49-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="eba49-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="eba49-132">Remarks</span></span>

<span data-ttu-id="eba49-133">Per ridimensionare, ruotare o tradurre uno sprite, chiamare [**ID3DXSprite:: setransform**](id3dxsprite--settransform.md) con una matrice che contiene i valori scale, Rotate e translate (SRT), prima di chiamare ID3DXSprite::D RAW.</span><span class="sxs-lookup"><span data-stu-id="eba49-133">To scale, rotate, or translate a sprite, call [**ID3DXSprite::SetTransform**](id3dxsprite--settransform.md) with a matrix that contains the scale, rotate, and translate (SRT) values, before calling ID3DXSprite::Draw.</span></span> <span data-ttu-id="eba49-134">Per informazioni sull'impostazione di valori SRT in una matrice, vedere [trasformazioni matrici](transforms.md).</span><span class="sxs-lookup"><span data-stu-id="eba49-134">For information about setting SRT values in a matrix, see [Matrix Transforms](transforms.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eba49-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eba49-135">Requirements</span></span>



| <span data-ttu-id="eba49-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="eba49-136">Requirement</span></span> | <span data-ttu-id="eba49-137">Valore</span><span class="sxs-lookup"><span data-stu-id="eba49-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eba49-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eba49-138">Header</span></span><br/>  | <dl> <span data-ttu-id="eba49-139"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="eba49-139"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="eba49-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="eba49-140">Library</span></span><br/> | <dl> <span data-ttu-id="eba49-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eba49-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eba49-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eba49-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eba49-143">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="eba49-143">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="eba49-144">**ID3DXSprite:: GetTransform**</span><span class="sxs-lookup"><span data-stu-id="eba49-144">**ID3DXSprite::GetTransform**</span></span>](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
