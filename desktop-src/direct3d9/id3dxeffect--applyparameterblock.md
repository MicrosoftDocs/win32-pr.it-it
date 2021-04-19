---
description: Applicare i valori in un blocco di stato allo stato del sistema con effetto corrente.
ms.assetid: f228e2a2-64fa-4354-9f49-42d1d3b12d50
title: 'Metodo ID3DXEffect:: ApplyParameterBlock (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ApplyParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 12af672b929822180c4dba681ca333692a9174ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322794"
---
# <a name="id3dxeffectapplyparameterblock-method"></a><span data-ttu-id="72459-103">Metodo ID3DXEffect:: ApplyParameterBlock</span><span class="sxs-lookup"><span data-stu-id="72459-103">ID3DXEffect::ApplyParameterBlock method</span></span>

<span data-ttu-id="72459-104">Applicare i valori in un blocco di stato allo stato del sistema con effetto corrente.</span><span class="sxs-lookup"><span data-stu-id="72459-104">Apply the values in a state block to the current effect system state.</span></span>

## <a name="syntax"></a><span data-ttu-id="72459-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72459-105">Syntax</span></span>


```C++
HRESULT ApplyParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a><span data-ttu-id="72459-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="72459-106">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="72459-107">*hParameterBlock* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72459-107">*hParameterBlock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72459-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="72459-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="72459-109">Handle per il blocco di parametri.</span><span class="sxs-lookup"><span data-stu-id="72459-109">A handle to the parameter block.</span></span> <span data-ttu-id="72459-110">Si tratta dell'handle restituito da [**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md).</span><span class="sxs-lookup"><span data-stu-id="72459-110">This is the handle returned by [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72459-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72459-111">Return value</span></span>

<span data-ttu-id="72459-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="72459-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="72459-113">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="72459-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="72459-114">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="72459-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="72459-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="72459-115">Remarks</span></span>

<span data-ttu-id="72459-116">Modificare lo stato del parametro dell'effetto di acquisizione in un blocco di parametri chiamando BeginParameterBlock; arrestare l'acquisizione delle modifiche di stato chiamando EndParameterBlock.</span><span class="sxs-lookup"><span data-stu-id="72459-116">Capture effect parameter state changes in a parameter block by calling BeginParameterBlock; stop capturing state changes by calling EndParameterBlock.</span></span> <span data-ttu-id="72459-117">Queste modifiche di stato includono eventuali modifiche ai parametri dell'effetto che si verificano all'interno di una tecnica, incluse quelle all'esterno di un passaggio.</span><span class="sxs-lookup"><span data-stu-id="72459-117">These state changes include any effect parameter changes that occur inside of a technique (including those outside of a pass).</span></span> <span data-ttu-id="72459-118">Al termine del blocco dei parametri, chiamare DeleteParameterBlock per recuperare la memoria.</span><span class="sxs-lookup"><span data-stu-id="72459-118">Once you are done with the parameter block, call DeleteParameterBlock to recover memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="72459-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72459-119">Requirements</span></span>



| <span data-ttu-id="72459-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="72459-120">Requirement</span></span> | <span data-ttu-id="72459-121">Valore</span><span class="sxs-lookup"><span data-stu-id="72459-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="72459-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72459-122">Header</span></span><br/>  | <dl> <span data-ttu-id="72459-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="72459-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="72459-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="72459-124">Library</span></span><br/> | <dl> <span data-ttu-id="72459-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72459-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="72459-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72459-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72459-127">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="72459-127">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="72459-128">**ID3DXEffect::BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="72459-128">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="72459-129">**ID3DXEffect::EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="72459-129">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> <dt>

[<span data-ttu-id="72459-130">**ID3DXEffect::D eleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="72459-130">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




