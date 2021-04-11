---
description: Creare un pool di effetti. Un pool viene usato per condividere parametri tra effetti.
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: Funzione D3DXCreateEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectPool
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 14753500ac15fb0ed30d46b1121431af78e1fe93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235172"
---
# <a name="d3dxcreateeffectpool-function"></a><span data-ttu-id="7063c-104">D3DXCreateEffectPool (funzione)</span><span class="sxs-lookup"><span data-stu-id="7063c-104">D3DXCreateEffectPool function</span></span>

<span data-ttu-id="7063c-105">Creare un pool di effetti.</span><span class="sxs-lookup"><span data-stu-id="7063c-105">Create an effect pool.</span></span> <span data-ttu-id="7063c-106">Un pool viene usato per condividere parametri tra effetti.</span><span class="sxs-lookup"><span data-stu-id="7063c-106">A pool is used to share parameters between effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="7063c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7063c-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a><span data-ttu-id="7063c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7063c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7063c-109">*ppPool* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7063c-109">*ppPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7063c-110">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span><span class="sxs-lookup"><span data-stu-id="7063c-110">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span></span>

<span data-ttu-id="7063c-111">Restituisce un puntatore al pool creato.</span><span class="sxs-lookup"><span data-stu-id="7063c-111">Returns a pointer to the created pool.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7063c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7063c-112">Return value</span></span>

<span data-ttu-id="7063c-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7063c-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7063c-114">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7063c-114">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="7063c-115">Se gli argomenti non sono validi, il metodo restituirà D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7063c-115">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="7063c-116">Se il metodo ha esito negativo, il valore restituito sarà E avrà \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7063c-116">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7063c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7063c-117">Remarks</span></span>

<span data-ttu-id="7063c-118">Per gli effetti all'interno di un pool, i parametri condivisi con lo stesso nome condividono i valori.</span><span class="sxs-lookup"><span data-stu-id="7063c-118">For effects within a pool, shared parameters with the same name share values.</span></span>

## <a name="requirements"></a><span data-ttu-id="7063c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7063c-119">Requirements</span></span>



| <span data-ttu-id="7063c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7063c-120">Requirement</span></span> | <span data-ttu-id="7063c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7063c-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7063c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7063c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7063c-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7063c-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7063c-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="7063c-124">Library</span></span><br/> | <dl> <span data-ttu-id="7063c-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7063c-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7063c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7063c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7063c-127">Funzioni effetto</span><span class="sxs-lookup"><span data-stu-id="7063c-127">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 




