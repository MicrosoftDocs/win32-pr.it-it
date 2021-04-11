---
description: Impostare il valore di un parametro o di un'annotazione arbitraria, inclusi tipi semplici, struct, matrici, stringhe, shader e trame.
ms.assetid: ab71f1a1-3e10-4883-99b4-607e0b5751c2
title: 'Metodo ID3DXBaseEffect:: SetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3281306240cefc0312ff9a2af7e056dab74a085b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132370"
---
# <a name="id3dxbaseeffectsetvalue-method"></a><span data-ttu-id="679fd-103">Metodo ID3DXBaseEffect:: SetValue</span><span class="sxs-lookup"><span data-stu-id="679fd-103">ID3DXBaseEffect::SetValue method</span></span>

<span data-ttu-id="679fd-104">Impostare il valore di un parametro o di un'annotazione arbitraria, inclusi tipi semplici, struct, matrici, stringhe, shader e trame.</span><span class="sxs-lookup"><span data-stu-id="679fd-104">Set the value of an arbitrary parameter or annotation, including simple types, structs, arrays, strings, shaders and textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="679fd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="679fd-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hParameter,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="679fd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="679fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="679fd-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="679fd-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="679fd-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="679fd-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="679fd-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="679fd-109">Unique identifier.</span></span> <span data-ttu-id="679fd-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="679fd-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="679fd-111">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="679fd-111">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="679fd-112">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="679fd-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="679fd-113">Puntatore a un buffer contenente i dati.</span><span class="sxs-lookup"><span data-stu-id="679fd-113">Pointer to a buffer containing data.</span></span>

</dd> <dt>

<span data-ttu-id="679fd-114">*Byte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="679fd-114">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="679fd-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="679fd-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="679fd-116">\[\]numero di byte nel buffer.</span><span class="sxs-lookup"><span data-stu-id="679fd-116">\[in\] Number of bytes in the buffer.</span></span> <span data-ttu-id="679fd-117">Passare \_ il valore predefinito D3DX se si è certi che il buffer è sufficientemente grande da contenere l'intero parametro e si vuole ignorare la convalida delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="679fd-117">Pass in D3DX\_DEFAULT if you know your buffer is large enough to contain the entire parameter, and you want to skip size validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="679fd-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="679fd-118">Return value</span></span>

<span data-ttu-id="679fd-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="679fd-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="679fd-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="679fd-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="679fd-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="679fd-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="679fd-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="679fd-122">Remarks</span></span>

<span data-ttu-id="679fd-123">Questo metodo può essere utilizzato al posto di quasi tutte le chiamate API dei set di effetti.</span><span class="sxs-lookup"><span data-stu-id="679fd-123">This method can be used in place of nearly all the effect set API calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="679fd-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="679fd-124">Requirements</span></span>



| <span data-ttu-id="679fd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="679fd-125">Requirement</span></span> | <span data-ttu-id="679fd-126">Valore</span><span class="sxs-lookup"><span data-stu-id="679fd-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="679fd-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="679fd-127">Header</span></span><br/>  | <dl> <span data-ttu-id="679fd-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="679fd-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="679fd-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="679fd-129">Library</span></span><br/> | <dl> <span data-ttu-id="679fd-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="679fd-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="679fd-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="679fd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="679fd-132">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="679fd-132">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="679fd-133">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="679fd-133">**GetValue**</span></span>](id3dxbaseeffect--getvalue.md)
</dt> </dl>

 

 
