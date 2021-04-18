---
description: Imposta una matrice di valori BOOL.
ms.assetid: d168d362-86b3-4db4-bc52-748a640ebc18
title: 'Metodo ID3DXTextureShader:: SetBoolArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBoolArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0799e4ef9d35a886e59fae44c37a841bcda3aed6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323353"
---
# <a name="id3dxtextureshadersetboolarray-method"></a><span data-ttu-id="ea66c-103">Metodo ID3DXTextureShader:: SetBoolArray</span><span class="sxs-lookup"><span data-stu-id="ea66c-103">ID3DXTextureShader::SetBoolArray method</span></span>

<span data-ttu-id="ea66c-104">Imposta una matrice di valori BOOL.</span><span class="sxs-lookup"><span data-stu-id="ea66c-104">Sets an array of BOOL values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea66c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea66c-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hConstant,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="ea66c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea66c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea66c-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea66c-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea66c-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ea66c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ea66c-109">Identificatore univoco della matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="ea66c-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="ea66c-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="ea66c-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea66c-111">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea66c-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea66c-112">Tipo: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea66c-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ea66c-113">Matrice di valori BOOL.</span><span class="sxs-lookup"><span data-stu-id="ea66c-113">Array of BOOL values.</span></span>

</dd> <dt>

<span data-ttu-id="ea66c-114">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ea66c-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea66c-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea66c-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea66c-116">Numero di valori BOOL nella matrice.</span><span class="sxs-lookup"><span data-stu-id="ea66c-116">Number of BOOL values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea66c-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea66c-117">Return value</span></span>

<span data-ttu-id="ea66c-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ea66c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ea66c-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea66c-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ea66c-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ea66c-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea66c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea66c-121">Requirements</span></span>



| <span data-ttu-id="ea66c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea66c-122">Requirement</span></span> | <span data-ttu-id="ea66c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ea66c-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea66c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea66c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ea66c-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea66c-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ea66c-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="ea66c-126">Library</span></span><br/> | <dl> <span data-ttu-id="ea66c-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea66c-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ea66c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea66c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea66c-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="ea66c-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
