---
description: Imposta la tabella delle costanti con i dati nel buffer.
ms.assetid: 55cf5456-8f23-405d-9329-8ff737c5c139
title: 'Metodo ID3DXTextureShader:: SetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2f18902c73f44bc4294e5152f8da5ea3e37f27ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322431"
---
# <a name="id3dxtextureshadersetvalue-method"></a><span data-ttu-id="9c0af-103">Metodo ID3DXTextureShader:: SetValue</span><span class="sxs-lookup"><span data-stu-id="9c0af-103">ID3DXTextureShader::SetValue method</span></span>

<span data-ttu-id="9c0af-104">Imposta la tabella delle costanti con i dati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="9c0af-104">Sets the constant table with the data in the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c0af-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c0af-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hConstant,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="9c0af-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c0af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c0af-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c0af-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c0af-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9c0af-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9c0af-109">Identificatore univoco di una costante.</span><span class="sxs-lookup"><span data-stu-id="9c0af-109">Unique identifier to a constant.</span></span> <span data-ttu-id="9c0af-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="9c0af-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c0af-111">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c0af-111">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c0af-112">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c0af-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c0af-113">Puntatore a un buffer contenente i dati costanti.</span><span class="sxs-lookup"><span data-stu-id="9c0af-113">A pointer to a buffer containing the constant data.</span></span>

</dd> <dt>

<span data-ttu-id="9c0af-114">*Byte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c0af-114">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c0af-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c0af-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c0af-116">Dimensioni del buffer, in byte.</span><span class="sxs-lookup"><span data-stu-id="9c0af-116">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c0af-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c0af-117">Return value</span></span>

<span data-ttu-id="9c0af-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9c0af-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9c0af-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9c0af-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9c0af-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9c0af-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c0af-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c0af-121">Requirements</span></span>



| <span data-ttu-id="9c0af-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c0af-122">Requirement</span></span> | <span data-ttu-id="9c0af-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9c0af-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c0af-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c0af-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9c0af-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c0af-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9c0af-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="9c0af-126">Library</span></span><br/> | <dl> <span data-ttu-id="9c0af-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c0af-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9c0af-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c0af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c0af-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="9c0af-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
