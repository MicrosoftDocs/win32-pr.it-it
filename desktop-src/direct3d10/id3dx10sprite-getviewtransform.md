---
description: Ottenere la trasformazione visualizzazione che si applica a tutti gli sprite.
ms.assetid: eba45c08-64cc-4119-83d4-50351fe21bea
title: 'Metodo ID3DX10Sprite:: GetViewTransform (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 699a46e48545d58058fb1f2db2955b4a4f403a53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323742"
---
# <a name="id3dx10spritegetviewtransform-method"></a><span data-ttu-id="fab95-103">Metodo ID3DX10Sprite:: GetViewTransform</span><span class="sxs-lookup"><span data-stu-id="fab95-103">ID3DX10Sprite::GetViewTransform method</span></span>

<span data-ttu-id="fab95-104">Ottenere la trasformazione visualizzazione che si applica a tutti gli sprite.</span><span class="sxs-lookup"><span data-stu-id="fab95-104">Get the view transform that applies to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab95-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fab95-105">Syntax</span></span>


```C++
HRESULT GetViewTransform(
  [out] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a><span data-ttu-id="fab95-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fab95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fab95-107">*pViewTransform* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fab95-107">*pViewTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fab95-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fab95-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fab95-109">Puntatore a un [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) che verrà impostato sulla trasformazione dello sprite dallo spazio globale originale.</span><span class="sxs-lookup"><span data-stu-id="fab95-109">Pointer to a [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) that will be set to the transform of the sprite from the original world space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fab95-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fab95-110">Return value</span></span>

<span data-ttu-id="fab95-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fab95-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fab95-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fab95-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fab95-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fab95-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fab95-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fab95-114">Requirements</span></span>



| <span data-ttu-id="fab95-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fab95-115">Requirement</span></span> | <span data-ttu-id="fab95-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fab95-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fab95-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fab95-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fab95-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="fab95-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="fab95-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="fab95-119">Library</span></span><br/> | <dl> <span data-ttu-id="fab95-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fab95-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fab95-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fab95-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab95-122">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="fab95-122">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="fab95-123">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="fab95-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
