---
description: Preparare un dispositivo per il disegno degli sprite.
ms.assetid: cffe5ac3-eeee-4ece-afcc-04a476b75863
title: 'Metodo ID3DX10Sprite:: begin (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Begin
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ede2995f72eb1200e68f035119643a362e15701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235110"
---
# <a name="id3dx10spritebegin-method"></a><span data-ttu-id="dda42-103">Metodo ID3DX10Sprite:: Begin</span><span class="sxs-lookup"><span data-stu-id="dda42-103">ID3DX10Sprite::Begin method</span></span>

<span data-ttu-id="dda42-104">Preparare un dispositivo per il disegno degli sprite.</span><span class="sxs-lookup"><span data-stu-id="dda42-104">Prepare a device for drawing sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="dda42-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dda42-105">Syntax</span></span>


```C++
HRESULT Begin(
  [in] UINT flags
);
```



## <a name="parameters"></a><span data-ttu-id="dda42-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dda42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dda42-107">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dda42-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dda42-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dda42-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dda42-109">Flag che controllano il modo in cui verranno disegnati gli sprite.</span><span class="sxs-lookup"><span data-stu-id="dda42-109">Flags that control how the sprites will be drawn.</span></span> <span data-ttu-id="dda42-110">Vedere [**d3dx10 \_ sprite \_ flag**](d3dx10-sprite-flag.md).</span><span class="sxs-lookup"><span data-stu-id="dda42-110">See [**D3DX10\_SPRITE\_FLAG**](d3dx10-sprite-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dda42-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dda42-111">Return value</span></span>

<span data-ttu-id="dda42-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dda42-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dda42-113">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dda42-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="dda42-114">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="dda42-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="dda42-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="dda42-115">Remarks</span></span>

<span data-ttu-id="dda42-116">Ogni chiamata a Begin deve corrispondere a una chiamata a [**ID3DX10Sprite:: end**](id3dx10sprite-end.md).</span><span class="sxs-lookup"><span data-stu-id="dda42-116">Every call to Begin must be matched with a call to [**ID3DX10Sprite::End**](id3dx10sprite-end.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dda42-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dda42-117">Requirements</span></span>



| <span data-ttu-id="dda42-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dda42-118">Requirement</span></span> | <span data-ttu-id="dda42-119">Valore</span><span class="sxs-lookup"><span data-stu-id="dda42-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dda42-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dda42-120">Header</span></span><br/>  | <dl> <span data-ttu-id="dda42-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="dda42-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="dda42-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="dda42-122">Library</span></span><br/> | <dl> <span data-ttu-id="dda42-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dda42-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dda42-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dda42-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dda42-125">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="dda42-125">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="dda42-126">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="dda42-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
