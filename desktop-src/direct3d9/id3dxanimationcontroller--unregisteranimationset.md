---
description: Rimuove un set di animazioni dal controller animazione.
ms.assetid: 2ca99651-8249-44c2-9560-b3cfaa930862
title: 'Metodo ID3DXAnimationController:: UnregisterAnimationSet (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnregisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35c70552f16daac6d2cfed5cbccf268179526ae1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323635"
---
# <a name="id3dxanimationcontrollerunregisteranimationset-method"></a><span data-ttu-id="42c08-103">Metodo ID3DXAnimationController:: UnregisterAnimationSet</span><span class="sxs-lookup"><span data-stu-id="42c08-103">ID3DXAnimationController::UnregisterAnimationSet method</span></span>

<span data-ttu-id="42c08-104">Rimuove un set di animazioni dal controller animazione.</span><span class="sxs-lookup"><span data-stu-id="42c08-104">Removes an animation set from the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="42c08-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42c08-105">Syntax</span></span>


```C++
HRESULT UnregisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="42c08-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="42c08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42c08-107">*pAnimSet* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42c08-107">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42c08-108">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="42c08-108">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="42c08-109">Puntatore al set di animazioni [**ID3DXAnimationSet**](id3dxanimationset.md) da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="42c08-109">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42c08-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42c08-110">Return value</span></span>

<span data-ttu-id="42c08-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="42c08-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="42c08-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="42c08-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="42c08-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="42c08-113">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="42c08-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42c08-114">Requirements</span></span>



| <span data-ttu-id="42c08-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="42c08-115">Requirement</span></span> | <span data-ttu-id="42c08-116">Valore</span><span class="sxs-lookup"><span data-stu-id="42c08-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42c08-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42c08-117">Header</span></span><br/>  | <dl> <span data-ttu-id="42c08-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="42c08-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="42c08-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="42c08-119">Library</span></span><br/> | <dl> <span data-ttu-id="42c08-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42c08-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="42c08-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42c08-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42c08-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="42c08-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




