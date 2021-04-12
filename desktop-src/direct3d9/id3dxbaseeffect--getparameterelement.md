---
description: Ottiene l'handle di un parametro dell'elemento della matrice.
ms.assetid: fe8edbc5-dc1d-4386-8149-489541d55bde
title: 'Metodo ID3DXBaseEffect:: getparameterelement (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterElement
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5130ccf57634f9b1a569a1dd70833fe2014e1a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355874"
---
# <a name="id3dxbaseeffectgetparameterelement-method"></a><span data-ttu-id="92694-103">Metodo ID3DXBaseEffect:: getparameterelement</span><span class="sxs-lookup"><span data-stu-id="92694-103">ID3DXBaseEffect::GetParameterElement method</span></span>

<span data-ttu-id="92694-104">Ottiene l'handle di un parametro dell'elemento della matrice.</span><span class="sxs-lookup"><span data-stu-id="92694-104">Get the handle of an array element parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="92694-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92694-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterElement(
  [in] D3DXHANDLE hParameter,
  [in] UINT       ElementIndex
);
```



## <a name="parameters"></a><span data-ttu-id="92694-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="92694-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92694-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92694-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92694-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="92694-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="92694-109">Handle della matrice.</span><span class="sxs-lookup"><span data-stu-id="92694-109">Handle of the array.</span></span> <span data-ttu-id="92694-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="92694-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="92694-111">*ElementIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92694-111">*ElementIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92694-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92694-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92694-113">Indice dell'elemento della matrice.</span><span class="sxs-lookup"><span data-stu-id="92694-113">Array element index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92694-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92694-114">Return value</span></span>

<span data-ttu-id="92694-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="92694-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="92694-116">Restituisce l'handle del parametro specificato oppure **null** se HParameter o ElementIndex non è valido.</span><span class="sxs-lookup"><span data-stu-id="92694-116">Returns the handle of the specified parameter, or **NULL** if either hParameter or ElementIndex is invalid.</span></span> <span data-ttu-id="92694-117">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="92694-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="92694-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="92694-118">Remarks</span></span>

<span data-ttu-id="92694-119">Questo metodo viene usato per ottenere un elemento di un parametro che è una matrice.</span><span class="sxs-lookup"><span data-stu-id="92694-119">This method is used to get an element of a parameter that is an array.</span></span>

## <a name="requirements"></a><span data-ttu-id="92694-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92694-120">Requirements</span></span>



| <span data-ttu-id="92694-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="92694-121">Requirement</span></span> | <span data-ttu-id="92694-122">Valore</span><span class="sxs-lookup"><span data-stu-id="92694-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="92694-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92694-123">Header</span></span><br/>  | <dl> <span data-ttu-id="92694-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="92694-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="92694-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="92694-125">Library</span></span><br/> | <dl> <span data-ttu-id="92694-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92694-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="92694-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92694-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92694-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="92694-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
