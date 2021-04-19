---
description: Creare uno sprite per il disegno di una trama 2D. Nota invece di utilizzare questa funzione, è consigliabile utilizzare Direct2D e la libreria DirectXTK, SpriteBatch Class.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: Funzione D3DX10CreateSprite (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSprite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cf40e303cb616f35ea5cd3526c263e3bd12ae428
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322414"
---
# <a name="d3dx10createsprite-function"></a><span data-ttu-id="eeb9c-103">D3DX10CreateSprite (funzione)</span><span class="sxs-lookup"><span data-stu-id="eeb9c-103">D3DX10CreateSprite function</span></span>

<span data-ttu-id="eeb9c-104">Creare uno sprite per il disegno di una trama 2D.</span><span class="sxs-lookup"><span data-stu-id="eeb9c-104">Create a sprite for drawing a 2D texture.</span></span>

> [!Note]  
> <span data-ttu-id="eeb9c-105">Anziché utilizzare questa funzione, è consigliabile utilizzare [Direct2D](../direct2d/direct2d-portal.md) e la libreria [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SpriteBatch** Class.</span><span class="sxs-lookup"><span data-stu-id="eeb9c-105">Instead of using this function, we recommend that you use [Direct2D](../direct2d/direct2d-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteBatch** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="eeb9c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eeb9c-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateSprite(
  _In_  ID3D10Device   *pDevice,
  _In_  UINT           cDeviceBufferSize,
  _Out_ LPD3DX10SPRITE *ppSprite
);
```



## <a name="parameters"></a><span data-ttu-id="eeb9c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="eeb9c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeb9c-108">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eeb9c-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeb9c-109">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="eeb9c-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="eeb9c-110">Un puntatore al dispositivo (vedere [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) che trarrà lo sprite.</span><span class="sxs-lookup"><span data-stu-id="eeb9c-110">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will draw the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="eeb9c-111">*cDeviceBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eeb9c-111">*cDeviceBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeb9c-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eeb9c-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eeb9c-113">Dimensioni del buffer dei vertici, in numero di sprite, che verranno inviate al dispositivo quando viene chiamato [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) o [**ID3DX10Sprite::D rawspritesimmediate**](id3dx10sprite-drawspritesimmediate.md) .</span><span class="sxs-lookup"><span data-stu-id="eeb9c-113">The size of the vertex buffer, in number of sprites, that will be sent to the device when [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) or [**ID3DX10Sprite::DrawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md) is called.</span></span> <span data-ttu-id="eeb9c-114">Si tratta di un numero ridotto se si è certi che verrà eseguito il rendering di un numero ridotto di sprite alla volta (per risparmiare memoria) e un numero elevato se si è certi che verrà eseguito il rendering di un numero elevato di sprite alla volta.</span><span class="sxs-lookup"><span data-stu-id="eeb9c-114">This should be a small number if you know you will be rendering a small number of sprites at a time (to save memory) and a large number if you know you will be rendering a large number of sprites at a time.</span></span> <span data-ttu-id="eeb9c-115">Il valore massimo è 4096.</span><span class="sxs-lookup"><span data-stu-id="eeb9c-115">The maximum value is 4096.</span></span> <span data-ttu-id="eeb9c-116">Se si specifica 0, le dimensioni del buffer vertici verranno impostate automaticamente su 4096.</span><span class="sxs-lookup"><span data-stu-id="eeb9c-116">If 0 is specified, the vertex buffer size will automatically be set to 4096.</span></span>

</dd> <dt>

<span data-ttu-id="eeb9c-117">*ppSprite* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="eeb9c-117">*ppSprite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eeb9c-118">Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="eeb9c-118">Type: **[**LPD3DX10SPRITE**](id3dx10sprite.md)\***</span></span>

<span data-ttu-id="eeb9c-119">Indirizzo di un puntatore a un'interfaccia sprite (vedere [**interfaccia ID3DX10Sprite**](id3dx10sprite.md)).</span><span class="sxs-lookup"><span data-stu-id="eeb9c-119">The address of a pointer to a sprite interface (see [**ID3DX10Sprite Interface**](id3dx10sprite.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeb9c-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eeb9c-120">Return value</span></span>

<span data-ttu-id="eeb9c-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eeb9c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eeb9c-122">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eeb9c-122">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="eeb9c-123">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="eeb9c-123">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeb9c-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eeb9c-124">Requirements</span></span>



| <span data-ttu-id="eeb9c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeb9c-125">Requirement</span></span> | <span data-ttu-id="eeb9c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="eeb9c-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb9c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eeb9c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="eeb9c-128"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeb9c-128"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="eeb9c-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="eeb9c-129">Library</span></span><br/> | <dl> <span data-ttu-id="eeb9c-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eeb9c-130"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeb9c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eeb9c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeb9c-132">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="eeb9c-132">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
