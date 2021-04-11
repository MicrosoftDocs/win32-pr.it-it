---
description: Imposta la trasformazione sprite.
ms.assetid: 87dfc169-b647-4a96-897d-abbe765ea9e2
title: 'Metodo ID3DXSprite:: setransform (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 316e7e2c68dfa8f25a712c2077ece03d09455050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235081"
---
# <a name="id3dxspritesettransform-method"></a><span data-ttu-id="cd53f-103">Metodo ID3DXSprite:: setransform</span><span class="sxs-lookup"><span data-stu-id="cd53f-103">ID3DXSprite::SetTransform method</span></span>

<span data-ttu-id="cd53f-104">Imposta la trasformazione sprite.</span><span class="sxs-lookup"><span data-stu-id="cd53f-104">Sets the sprite transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd53f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd53f-105">Syntax</span></span>


```C++
HRESULT SetTransform(
  [in] const D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a><span data-ttu-id="cd53f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd53f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd53f-107">*pTransform* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd53f-107">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd53f-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd53f-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cd53f-109">Puntatore a un [**D3DXMATRIX**](d3dxmatrix.md) che contiene una trasformazione dello sprite dallo spazio globale originale.</span><span class="sxs-lookup"><span data-stu-id="cd53f-109">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a transform of the sprite from the original world space.</span></span> <span data-ttu-id="cd53f-110">Usare questa trasformazione per ridimensionare, ruotare o trasformare lo sprite.</span><span class="sxs-lookup"><span data-stu-id="cd53f-110">Use this transform to scale, rotate, or transform the sprite.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd53f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd53f-111">Return value</span></span>

<span data-ttu-id="cd53f-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cd53f-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cd53f-113">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cd53f-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="cd53f-114">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="cd53f-114">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="cd53f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd53f-115">Requirements</span></span>



| <span data-ttu-id="cd53f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd53f-116">Requirement</span></span> | <span data-ttu-id="cd53f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cd53f-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd53f-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd53f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cd53f-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd53f-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="cd53f-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="cd53f-120">Library</span></span><br/> | <dl> <span data-ttu-id="cd53f-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd53f-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cd53f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd53f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd53f-123">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="cd53f-123">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="cd53f-124">Trasformazioni (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cd53f-124">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




