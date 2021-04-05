---
description: Ottiene un puntatore al pool di parametri condivisi.
ms.assetid: 1e999fd5-76ef-43fa-8a77-ae6f2821f46d
title: 'Metodo ID3DXEffect:: getpool (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetPool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 18a35e9bc0a596cb88da6d4c1faf10941fbce8a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969316"
---
# <a name="id3dxeffectgetpool-method"></a><span data-ttu-id="e699c-103">Metodo ID3DXEffect:: getpool</span><span class="sxs-lookup"><span data-stu-id="e699c-103">ID3DXEffect::GetPool method</span></span>

<span data-ttu-id="e699c-104">Ottiene un puntatore al pool di parametri condivisi.</span><span class="sxs-lookup"><span data-stu-id="e699c-104">Gets a pointer to the pool of shared parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="e699c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e699c-105">Syntax</span></span>


```C++
HRESULT GetPool(
  [out] LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a><span data-ttu-id="e699c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e699c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e699c-107">*ppPool* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e699c-107">*ppPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e699c-108">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span><span class="sxs-lookup"><span data-stu-id="e699c-108">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span></span>

<span data-ttu-id="e699c-109">Puntatore a un oggetto [**ID3DXEffectPool**](id3dxeffectpool.md) .</span><span class="sxs-lookup"><span data-stu-id="e699c-109">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e699c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e699c-110">Return value</span></span>

<span data-ttu-id="e699c-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e699c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e699c-112">Questo metodo restituisce sempre il valore S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e699c-112">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e699c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e699c-113">Remarks</span></span>

<span data-ttu-id="e699c-114">I pool contengono parametri condivisi tra gli effetti.</span><span class="sxs-lookup"><span data-stu-id="e699c-114">Pools contain shared parameters between effects.</span></span> <span data-ttu-id="e699c-115">Vedere [clonazione e condivisione (Direct3D 9)](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="e699c-115">See [Cloning and Sharing (Direct3D 9)](cloning-and-sharing.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e699c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e699c-116">Requirements</span></span>



| <span data-ttu-id="e699c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e699c-117">Requirement</span></span> | <span data-ttu-id="e699c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e699c-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e699c-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e699c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e699c-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e699c-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e699c-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="e699c-121">Library</span></span><br/> | <dl> <span data-ttu-id="e699c-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e699c-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e699c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e699c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e699c-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="e699c-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




