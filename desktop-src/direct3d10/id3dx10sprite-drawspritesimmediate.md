---
description: Creare una matrice di sprite.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: Metodo ID3DX10Sprite::D rawSpritesImmediate (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesImmediate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7fa4012f5f589c7bc0d1f789599da142194f6e08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356119"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a><span data-ttu-id="0cb9e-103">ID3DX10Sprite::D Metodo rawSpritesImmediate</span><span class="sxs-lookup"><span data-stu-id="0cb9e-103">ID3DX10Sprite::DrawSpritesImmediate method</span></span>

<span data-ttu-id="0cb9e-104">Creare una matrice di sprite.</span><span class="sxs-lookup"><span data-stu-id="0cb9e-104">Draw an array of sprites.</span></span> <span data-ttu-id="0cb9e-105">Questa operazione invierà immediatamente gli sprite al dispositivo per il rendering, che è diverso da [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) che aggiunge una matrice di sprite a un batch di sprite di cui eseguire il rendering quando viene chiamato [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) .</span><span class="sxs-lookup"><span data-stu-id="0cb9e-105">This will immediately send the sprites to the device for rendering, which is different from [**ID3DX10Sprite::DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md) which only adds an array of sprites to a batch of sprites to be rendered when [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) is called.</span></span> <span data-ttu-id="0cb9e-106">Questo metodo di disegno è particolarmente utile quando si disegna un numero elevato di sprite che sono già stati ordinati sulla CPU (o che non devono essere ordinati), ad esempio in un sistema particellare.</span><span class="sxs-lookup"><span data-stu-id="0cb9e-106">This draw method is most useful when drawing a large number of sprites that have already been sorted on the CPU (or do not need to be sorted), such as in a particle system.</span></span> <span data-ttu-id="0cb9e-107">Questo deve essere chiamato tra le chiamate a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite:: end**](id3dx10sprite-end.md).</span><span class="sxs-lookup"><span data-stu-id="0cb9e-107">This must be called in between calls to [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) and [**ID3DX10Sprite::End**](id3dx10sprite-end.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb9e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0cb9e-108">Syntax</span></span>


```C++
HRESULT DrawSpritesImmediate(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites,
  [in] UINT          cbSprite,
  [in] UINT          flags
);
```



## <a name="parameters"></a><span data-ttu-id="0cb9e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0cb9e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cb9e-110">*pSprites* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cb9e-110">*pSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb9e-111">Tipo: **[ **d3dx10 \_ sprite**](d3dx10-sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="0cb9e-111">Type: **[**D3DX10\_SPRITE**](d3dx10-sprite.md)\***</span></span>

<span data-ttu-id="0cb9e-112">Matrice di sprite da creare.</span><span class="sxs-lookup"><span data-stu-id="0cb9e-112">The array of sprites to draw.</span></span> <span data-ttu-id="0cb9e-113">Vedere [**d3dx10 \_ sprite**](d3dx10-sprite.md).</span><span class="sxs-lookup"><span data-stu-id="0cb9e-113">See [**D3DX10\_SPRITE**](d3dx10-sprite.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cb9e-114">*cSprites* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cb9e-114">*cSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb9e-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cb9e-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cb9e-116">Numero di sprite in pSprites.</span><span class="sxs-lookup"><span data-stu-id="0cb9e-116">The number of sprites in pSprites.</span></span>

</dd> <dt>

<span data-ttu-id="0cb9e-117">*cbSprite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cb9e-117">*cbSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb9e-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cb9e-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cb9e-119">Dimensione della struttura sprite che si passa a pSprites.</span><span class="sxs-lookup"><span data-stu-id="0cb9e-119">The size of the sprite structure you are passing into pSprites.</span></span> <span data-ttu-id="0cb9e-120">Il passaggio di 0 equivale al passaggio di sizeof (D3DX10 \_ sprite).</span><span class="sxs-lookup"><span data-stu-id="0cb9e-120">Passing in 0 is the equivalent of passing in sizeof(D3DX10\_SPRITE).</span></span>

</dd> <dt>

<span data-ttu-id="0cb9e-121">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cb9e-121">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb9e-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0cb9e-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0cb9e-123">Riservato.</span><span class="sxs-lookup"><span data-stu-id="0cb9e-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cb9e-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0cb9e-124">Return value</span></span>

<span data-ttu-id="0cb9e-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0cb9e-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0cb9e-126">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0cb9e-126">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0cb9e-127">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="0cb9e-127">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb9e-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cb9e-128">Requirements</span></span>



| <span data-ttu-id="0cb9e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb9e-129">Requirement</span></span> | <span data-ttu-id="0cb9e-130">Valore</span><span class="sxs-lookup"><span data-stu-id="0cb9e-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb9e-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0cb9e-131">Header</span></span><br/>  | <dl> <span data-ttu-id="0cb9e-132"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cb9e-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0cb9e-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="0cb9e-133">Library</span></span><br/> | <dl> <span data-ttu-id="0cb9e-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cb9e-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cb9e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0cb9e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb9e-136">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="0cb9e-136">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="0cb9e-137">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="0cb9e-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
