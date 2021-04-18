---
description: Imposta una matrice di valori booleani.
ms.assetid: 920b3482-cc30-4ab2-bfce-59f03afe11da
title: 'Metodo ID3DXBaseEffect:: SetBoolArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 813259fc9fcca954c4d7a992c7542387be33bb6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322081"
---
# <a name="id3dxbaseeffectsetboolarray-method"></a><span data-ttu-id="ce685-103">Metodo ID3DXBaseEffect:: SetBoolArray</span><span class="sxs-lookup"><span data-stu-id="ce685-103">ID3DXBaseEffect::SetBoolArray method</span></span>

<span data-ttu-id="ce685-104">Imposta una matrice di valori booleani.</span><span class="sxs-lookup"><span data-stu-id="ce685-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce685-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce685-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hParameter,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="ce685-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce685-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce685-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce685-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce685-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ce685-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ce685-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="ce685-109">Unique identifier.</span></span> <span data-ttu-id="ce685-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="ce685-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce685-111">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce685-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce685-112">Tipo: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ce685-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ce685-113">Matrice di valori booleani.</span><span class="sxs-lookup"><span data-stu-id="ce685-113">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="ce685-114">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ce685-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce685-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce685-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce685-116">Numero di valori booleani nella matrice.</span><span class="sxs-lookup"><span data-stu-id="ce685-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce685-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce685-117">Return value</span></span>

<span data-ttu-id="ce685-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce685-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce685-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ce685-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ce685-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ce685-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce685-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce685-121">Requirements</span></span>



| <span data-ttu-id="ce685-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce685-122">Requirement</span></span> | <span data-ttu-id="ce685-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ce685-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce685-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce685-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ce685-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce685-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ce685-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="ce685-126">Library</span></span><br/> | <dl> <span data-ttu-id="ce685-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce685-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ce685-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce685-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce685-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="ce685-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="ce685-130">**GetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="ce685-130">**GetBoolArray**</span></span>](id3dxbaseeffect--getboolarray.md)
</dt> </dl>

 

 
