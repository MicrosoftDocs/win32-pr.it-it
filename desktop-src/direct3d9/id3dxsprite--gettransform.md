---
description: Ottiene la trasformazione sprite.
ms.assetid: d91f2776-ee87-42b3-998b-fccea178cee2
title: 'Metodo ID3DXSprite:: GetTransform (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 646fa3574c3b9be788ad32ef402a7ca2051d04de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058628"
---
# <a name="id3dxspritegettransform-method"></a><span data-ttu-id="d4332-103">Metodo ID3DXSprite:: GetTransform</span><span class="sxs-lookup"><span data-stu-id="d4332-103">ID3DXSprite::GetTransform method</span></span>

<span data-ttu-id="d4332-104">Ottiene la trasformazione sprite.</span><span class="sxs-lookup"><span data-stu-id="d4332-104">Gets the sprite transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4332-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4332-105">Syntax</span></span>


```C++
HRESULT GetTransform(
  [in] D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a><span data-ttu-id="d4332-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4332-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4332-107">*pTransform* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4332-107">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4332-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4332-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d4332-109">Puntatore a un [**D3DXMATRIX**](d3dxmatrix.md) che contiene una trasformazione dello sprite dallo spazio globale originale.</span><span class="sxs-lookup"><span data-stu-id="d4332-109">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a transform of the sprite from the original world space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4332-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4332-110">Return value</span></span>

<span data-ttu-id="d4332-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4332-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4332-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d4332-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d4332-113">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="d4332-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="d4332-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4332-114">Requirements</span></span>



| <span data-ttu-id="d4332-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4332-115">Requirement</span></span> | <span data-ttu-id="d4332-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d4332-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4332-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4332-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d4332-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4332-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d4332-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="d4332-119">Library</span></span><br/> | <dl> <span data-ttu-id="d4332-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4332-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4332-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4332-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4332-122">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="d4332-122">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




