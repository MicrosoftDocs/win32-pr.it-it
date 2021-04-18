---
description: Elimina un blocco di parametri.
ms.assetid: 5502dabc-1703-481b-a69d-f6bd8fd01d20
title: Metodo ID3DXEffect::D eleteParameterBlock (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.DeleteParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 483b09ebf308b8cdfa14d714bc74786e5fcb1f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322789"
---
# <a name="id3dxeffectdeleteparameterblock-method"></a><span data-ttu-id="0b445-103">ID3DXEffect::D Metodo eleteParameterBlock</span><span class="sxs-lookup"><span data-stu-id="0b445-103">ID3DXEffect::DeleteParameterBlock method</span></span>

<span data-ttu-id="0b445-104">Elimina un blocco di parametri.</span><span class="sxs-lookup"><span data-stu-id="0b445-104">Delete a parameter block.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b445-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b445-105">Syntax</span></span>


```C++
HRESULT DeleteParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a><span data-ttu-id="0b445-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b445-106">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="0b445-107">*hParameterBlock* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b445-107">*hParameterBlock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b445-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0b445-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0b445-109">Handle per il blocco di parametri.</span><span class="sxs-lookup"><span data-stu-id="0b445-109">A handle to the parameter block.</span></span> <span data-ttu-id="0b445-110">Si tratta dell'handle restituito da [**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md).</span><span class="sxs-lookup"><span data-stu-id="0b445-110">This is the handle returned by [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b445-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b445-111">Return value</span></span>

<span data-ttu-id="0b445-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b445-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b445-113">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0b445-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0b445-114">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="0b445-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b445-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b445-115">Remarks</span></span>

<span data-ttu-id="0b445-116">I blocchi di parametri sono blocchi di Stati effettivi.</span><span class="sxs-lookup"><span data-stu-id="0b445-116">Parameter blocks are blocks of effect states.</span></span> <span data-ttu-id="0b445-117">Usare un blocco di parametri per registrare le modifiche di stato in modo che possano essere applicate in un secondo momento con una singola chiamata API.</span><span class="sxs-lookup"><span data-stu-id="0b445-117">Use a parameter block to record state changes so that they can be applied later on with a single API call.</span></span> <span data-ttu-id="0b445-118">Quando non è più necessario, eliminare il blocco di parametri per ridurre l'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="0b445-118">When no longer needed, delete the parameter block to reduce memory usage.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b445-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b445-119">Requirements</span></span>



| <span data-ttu-id="0b445-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b445-120">Requirement</span></span> | <span data-ttu-id="0b445-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0b445-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b445-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b445-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0b445-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b445-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="0b445-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="0b445-124">Library</span></span><br/> | <dl> <span data-ttu-id="0b445-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b445-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0b445-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b445-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b445-127">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="0b445-127">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="0b445-128">**ID3DXEffect::BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="0b445-128">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="0b445-129">**ID3DXEffect::EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="0b445-129">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> </dl>

 

 




