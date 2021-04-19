---
description: Aggiungere una matrice di sprite al batch di sprite di cui eseguire il rendering.
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: Metodo ID3DX10Sprite::D rawSpritesBuffered (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesBuffered
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72893f6a8c3cf82c67f014b4bdbb9a92453de319
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323746"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a><span data-ttu-id="13674-103">ID3DX10Sprite::D Metodo rawSpritesBuffered</span><span class="sxs-lookup"><span data-stu-id="13674-103">ID3DX10Sprite::DrawSpritesBuffered method</span></span>

<span data-ttu-id="13674-104">Aggiungere una matrice di sprite al batch di sprite di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="13674-104">Add an array of sprites to the batch of sprites to be rendered.</span></span> <span data-ttu-id="13674-105">Questo deve essere chiamato tra le chiamate a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite:: end**](id3dx10sprite-end.md)e [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) deve essere chiamato prima di end per inviare tutti gli sprite in batch al dispositivo per il rendering.</span><span class="sxs-lookup"><span data-stu-id="13674-105">This must be called in between calls to [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) and [**ID3DX10Sprite::End**](id3dx10sprite-end.md), and [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) must be called before End to send all of the batched sprites to the device for rendering.</span></span> <span data-ttu-id="13674-106">Questo metodo di disegno è particolarmente utile quando si disegna un numero ridotto di sprite che si desidera memorizzare nel buffer in un batch di grandi dimensioni, ad esempio i tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="13674-106">This draw method is most useful when drawing a small number of sprites that you want buffered into a large batch, such as fonts.</span></span>

## <a name="syntax"></a><span data-ttu-id="13674-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13674-107">Syntax</span></span>


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
);
```



## <a name="parameters"></a><span data-ttu-id="13674-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="13674-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13674-109">*pSprites* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13674-109">*pSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13674-110">Tipo: **[ **d3dx10 \_ sprite**](d3dx10-sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="13674-110">Type: **[**D3DX10\_SPRITE**](d3dx10-sprite.md)\***</span></span>

<span data-ttu-id="13674-111">Matrice di sprite da creare.</span><span class="sxs-lookup"><span data-stu-id="13674-111">The array of sprites to draw.</span></span> <span data-ttu-id="13674-112">Vedere [**d3dx10 \_ sprite**](d3dx10-sprite.md).</span><span class="sxs-lookup"><span data-stu-id="13674-112">See [**D3DX10\_SPRITE**](d3dx10-sprite.md).</span></span>

</dd> <dt>

<span data-ttu-id="13674-113">*cSprites* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13674-113">*cSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13674-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13674-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13674-115">Numero di sprite in pSprites.</span><span class="sxs-lookup"><span data-stu-id="13674-115">The number of sprites in pSprites.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13674-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13674-116">Return value</span></span>

<span data-ttu-id="13674-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="13674-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="13674-118">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="13674-118">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="13674-119">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="13674-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="13674-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13674-120">Requirements</span></span>



| <span data-ttu-id="13674-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="13674-121">Requirement</span></span> | <span data-ttu-id="13674-122">Valore</span><span class="sxs-lookup"><span data-stu-id="13674-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13674-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13674-123">Header</span></span><br/>  | <dl> <span data-ttu-id="13674-124"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="13674-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="13674-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="13674-125">Library</span></span><br/> | <dl> <span data-ttu-id="13674-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13674-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13674-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13674-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13674-128">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="13674-128">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="13674-129">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="13674-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
