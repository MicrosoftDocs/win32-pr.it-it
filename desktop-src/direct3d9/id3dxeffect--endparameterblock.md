---
description: Arresta l'acquisizione delle modifiche allo stato del parametro dell'effetto.
ms.assetid: b6ca2917-2df0-4f3a-9ee3-23e9d2501ff4
title: 'Metodo ID3DXEffect:: EndParameterBlock (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3359e3b923d05e003ffbda18791e497d18ba627e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969374"
---
# <a name="id3dxeffectendparameterblock-method"></a><span data-ttu-id="3b14b-103">Metodo ID3DXEffect:: EndParameterBlock</span><span class="sxs-lookup"><span data-stu-id="3b14b-103">ID3DXEffect::EndParameterBlock method</span></span>

<span data-ttu-id="3b14b-104">Arresta l'acquisizione delle modifiche allo stato del parametro dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="3b14b-104">Stop capturing effect parameter state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b14b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b14b-105">Syntax</span></span>


```C++
D3DXHANDLE EndParameterBlock();
```



## <a name="parameters"></a><span data-ttu-id="3b14b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b14b-106">Parameters</span></span>

<span data-ttu-id="3b14b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3b14b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3b14b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b14b-108">Return value</span></span>

<span data-ttu-id="3b14b-109">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="3b14b-109">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="3b14b-110">Restituisce un handle per il blocco di stato del parametro.</span><span class="sxs-lookup"><span data-stu-id="3b14b-110">Returns a handle to the parameter state block.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b14b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b14b-111">Remarks</span></span>

<span data-ttu-id="3b14b-112">Tutti i parametri degli effetti che modificano lo stato (dopo la chiamata a BeginParameterBlock e prima di chiamare EndParameterBlock) verranno salvati in un blocco di stato del parametro Effect.</span><span class="sxs-lookup"><span data-stu-id="3b14b-112">All effect parameters that change state (after calling BeginParameterBlock and before calling EndParameterBlock) will be saved in an effect parameter state block.</span></span> <span data-ttu-id="3b14b-113">Usare ApplyParameterBlock per applicare questo blocco di modifiche di stato al sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="3b14b-113">Use ApplyParameterBlock to apply this block of state changes to the effect system.</span></span> <span data-ttu-id="3b14b-114">Al termine di un blocco di stato, usare DeleteParameterBlock per liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="3b14b-114">Once you are finished with a state block use DeleteParameterBlock to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b14b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b14b-115">Requirements</span></span>



| <span data-ttu-id="3b14b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b14b-116">Requirement</span></span> | <span data-ttu-id="3b14b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3b14b-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b14b-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b14b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3b14b-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b14b-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="3b14b-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="3b14b-120">Library</span></span><br/> | <dl> <span data-ttu-id="3b14b-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b14b-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3b14b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b14b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b14b-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="3b14b-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="3b14b-124">**ID3DXEffect::BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="3b14b-124">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="3b14b-125">**ID3DXEffect::ApplyParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="3b14b-125">**ID3DXEffect::ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[<span data-ttu-id="3b14b-126">**ID3DXEffect::D eleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="3b14b-126">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




