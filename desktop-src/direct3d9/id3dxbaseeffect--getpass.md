---
description: Ottiene l'handle di un passaggio.
ms.assetid: 71332f6a-18fe-4702-8620-6d16b835ba8f
title: 'Metodo ID3DXBaseEffect:: GETPASS (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5db5c5da16a65b53b6e266886ee6ab8472dc3246
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104402024"
---
# <a name="id3dxbaseeffectgetpass-method"></a><span data-ttu-id="bcf06-103">Metodo ID3DXBaseEffect:: GETPASS</span><span class="sxs-lookup"><span data-stu-id="bcf06-103">ID3DXBaseEffect::GetPass method</span></span>

<span data-ttu-id="bcf06-104">Ottiene l'handle di un passaggio.</span><span class="sxs-lookup"><span data-stu-id="bcf06-104">Gets the handle of a pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf06-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcf06-105">Syntax</span></span>


```C++
D3DXHANDLE GetPass(
  [in] D3DXHANDLE hTechnique,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="bcf06-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bcf06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcf06-107">*hTechnique* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bcf06-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf06-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="bcf06-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="bcf06-109">Handle della tecnica padre.</span><span class="sxs-lookup"><span data-stu-id="bcf06-109">Handle of the parent technique.</span></span> <span data-ttu-id="bcf06-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="bcf06-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="bcf06-111">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="bcf06-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf06-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bcf06-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bcf06-113">Indice per il passaggio.</span><span class="sxs-lookup"><span data-stu-id="bcf06-113">Index for the pass.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcf06-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bcf06-114">Return value</span></span>

<span data-ttu-id="bcf06-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="bcf06-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="bcf06-116">Restituisce l'handle del passaggio specificato all'interno della tecnica specificata o **null** se l'indice non è valido.</span><span class="sxs-lookup"><span data-stu-id="bcf06-116">Returns the handle of the specified pass inside the specified technique, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="bcf06-117">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="bcf06-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf06-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcf06-118">Requirements</span></span>



| <span data-ttu-id="bcf06-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcf06-119">Requirement</span></span> | <span data-ttu-id="bcf06-120">Valore</span><span class="sxs-lookup"><span data-stu-id="bcf06-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf06-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bcf06-121">Header</span></span><br/>  | <dl> <span data-ttu-id="bcf06-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcf06-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="bcf06-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="bcf06-123">Library</span></span><br/> | <dl> <span data-ttu-id="bcf06-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bcf06-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bcf06-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcf06-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf06-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="bcf06-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
