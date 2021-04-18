---
description: Ottiene l'handle di una funzione.
ms.assetid: 97c82c28-4402-4605-8247-44d6f38bfa20
title: 'Metodo ID3DXBaseEffect:: GetFunction (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunction
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: de0567b605f4a892c1f8274a346a74acfbbc0442
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323604"
---
# <a name="id3dxbaseeffectgetfunction-method"></a><span data-ttu-id="22331-103">Metodo ID3DXBaseEffect:: GetFunction</span><span class="sxs-lookup"><span data-stu-id="22331-103">ID3DXBaseEffect::GetFunction method</span></span>

<span data-ttu-id="22331-104">Ottiene l'handle di una funzione.</span><span class="sxs-lookup"><span data-stu-id="22331-104">Gets the handle of a function.</span></span>

## <a name="syntax"></a><span data-ttu-id="22331-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22331-105">Syntax</span></span>


```C++
D3DXHANDLE GetFunction(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="22331-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="22331-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22331-107">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="22331-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22331-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22331-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="22331-109">Indice di funzione.</span><span class="sxs-lookup"><span data-stu-id="22331-109">Function index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22331-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22331-110">Return value</span></span>

<span data-ttu-id="22331-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="22331-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="22331-112">Restituisce l'handle della funzione specificata o **null** se l'indice non è valido.</span><span class="sxs-lookup"><span data-stu-id="22331-112">Returns the handle of the specified function, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="22331-113">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="22331-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22331-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22331-114">Requirements</span></span>



| <span data-ttu-id="22331-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="22331-115">Requirement</span></span> | <span data-ttu-id="22331-116">Valore</span><span class="sxs-lookup"><span data-stu-id="22331-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="22331-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22331-117">Header</span></span><br/>  | <dl> <span data-ttu-id="22331-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="22331-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="22331-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="22331-119">Library</span></span><br/> | <dl> <span data-ttu-id="22331-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22331-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="22331-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22331-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22331-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="22331-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
