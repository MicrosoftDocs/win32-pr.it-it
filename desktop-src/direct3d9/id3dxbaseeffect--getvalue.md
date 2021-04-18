---
description: Ottenere il valore di un parametro o di un'annotazione arbitraria, inclusi tipi semplici, struct, matrici, stringhe, shader e trame. Questo metodo può essere utilizzato al posto di quasi tutte le chiamate GetXXX in ID3DXBaseEffect.
ms.assetid: 41343922-99a7-486f-b4b0-1aa07f339664
title: 'Metodo ID3DXBaseEffect:: GetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 166635b22875692da0396f1c7c2145f13ca08df3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322087"
---
# <a name="id3dxbaseeffectgetvalue-method"></a><span data-ttu-id="23188-104">Metodo ID3DXBaseEffect:: GetValue</span><span class="sxs-lookup"><span data-stu-id="23188-104">ID3DXBaseEffect::GetValue method</span></span>

<span data-ttu-id="23188-105">Ottenere il valore di un parametro o di un'annotazione arbitraria, inclusi tipi semplici, struct, matrici, stringhe, shader e trame.</span><span class="sxs-lookup"><span data-stu-id="23188-105">Get the value of an arbitrary parameter or annotation, including simple types, structs, arrays, strings, shaders and textures.</span></span> <span data-ttu-id="23188-106">Questo metodo può essere utilizzato al posto di quasi tutte le chiamate GetXXX in [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="23188-106">This method can be used in place of nearly all the Getxxx calls in [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="23188-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23188-107">Syntax</span></span>


```C++
HRESULT GetValue(
  [in]  D3DXHANDLE hParameter,
  [out] LPVOID     pData,
  [in]  UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="23188-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="23188-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23188-109">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23188-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23188-110">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="23188-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="23188-111">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="23188-111">Unique identifier.</span></span> <span data-ttu-id="23188-112">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="23188-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="23188-113">*pData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="23188-113">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23188-114">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23188-114">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23188-115">Restituisce un buffer che contiene il valore.</span><span class="sxs-lookup"><span data-stu-id="23188-115">Returns a buffer containing the value.</span></span>

</dd> <dt>

<span data-ttu-id="23188-116">*Byte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23188-116">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23188-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23188-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23188-118">\[\]numero di byte nel buffer.</span><span class="sxs-lookup"><span data-stu-id="23188-118">\[in\] Number of bytes in the buffer.</span></span> <span data-ttu-id="23188-119">Passare \_ il valore predefinito D3DX se si è certi che il buffer è sufficientemente grande da contenere l'intero parametro e si vuole ignorare la convalida delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="23188-119">Pass in D3DX\_DEFAULT if you know your buffer is large enough to contain the entire parameter, and you want to skip size validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23188-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23188-120">Return value</span></span>

<span data-ttu-id="23188-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="23188-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="23188-122">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="23188-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="23188-123">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="23188-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="23188-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23188-124">Requirements</span></span>



| <span data-ttu-id="23188-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="23188-125">Requirement</span></span> | <span data-ttu-id="23188-126">Valore</span><span class="sxs-lookup"><span data-stu-id="23188-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="23188-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23188-127">Header</span></span><br/>  | <dl> <span data-ttu-id="23188-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="23188-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="23188-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="23188-129">Library</span></span><br/> | <dl> <span data-ttu-id="23188-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23188-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="23188-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23188-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23188-132">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="23188-132">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="23188-133">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="23188-133">**SetValue**</span></span>](id3dxbaseeffect--setvalue.md)
</dt> </dl>

 

 
