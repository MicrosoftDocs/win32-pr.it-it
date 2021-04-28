---
description: 'Funzione D3DXGetShaderConstantTableEx: ottiene la tabella costante shader incorporata in uno shader.'
ms.assetid: f7e846e4-9cb4-4634-95e3-4b2a752978a8
title: Funzione D3DXGetShaderConstantTableEx (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTableEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cac525f6f6fc4f4e3b6e5900aa9b655e7c7f60d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114430"
---
# <a name="d3dxgetshaderconstanttableex-function"></a><span data-ttu-id="b4acb-103">Funzione D3DXGetShaderConstantTableEx</span><span class="sxs-lookup"><span data-stu-id="b4acb-103">D3DXGetShaderConstantTableEx function</span></span>

<span data-ttu-id="b4acb-104">Ottiene la tabella costante shader incorporata all'interno di uno shader.</span><span class="sxs-lookup"><span data-stu-id="b4acb-104">Gets the shader-constant table embedded inside a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4acb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4acb-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderConstantTableEx(
  _In_  const DWORD               *pFunction,
  _In_        DWORD               Flags,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="b4acb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4acb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4acb-107">*pFunction* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b4acb-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4acb-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b4acb-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b4acb-109">Puntatore al flusso DWORD della funzione.</span><span class="sxs-lookup"><span data-stu-id="b4acb-109">Pointer to the function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="b4acb-110">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b4acb-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4acb-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4acb-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4acb-112">Usare il flag D3DXCONSTTABLE LARGEADDRESSAWARE per accedere a un massimo di 4 GB di spazio degli indirizzi virtuali (anziché il valore predefinito \_ di 2 GB).</span><span class="sxs-lookup"><span data-stu-id="b4acb-112">Use the D3DXCONSTTABLE\_LARGEADDRESSAWARE flag to access up to 4 GB of virtual address space (instead of the default of 2 GB).</span></span> <span data-ttu-id="b4acb-113">Se non è necessario lo spazio indirizzi virtuali aggiuntivo, usare [**D3DXGetShaderConstantTable.**](d3dxgetshaderconstanttable.md)</span><span class="sxs-lookup"><span data-stu-id="b4acb-113">If you do not need the additional virtual address space, use [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).</span></span>

</dd> <dt>

 <span data-ttu-id="b4acb-114">*ppConstantTable* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="b4acb-114">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4acb-115">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="b4acb-115">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="b4acb-116">Restituisce l'interfaccia di tabella costante (vedere [**ID3DXConstantTable)**](id3dxconstanttable.md)che gestisce la tabella costante.</span><span class="sxs-lookup"><span data-stu-id="b4acb-116">Returns the constant table interface (see [**ID3DXConstantTable**](id3dxconstanttable.md)) that manages the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4acb-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4acb-117">Return value</span></span>

<span data-ttu-id="b4acb-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b4acb-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b4acb-119">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b4acb-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b4acb-120">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b4acb-120">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4acb-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4acb-121">Remarks</span></span>

<span data-ttu-id="b4acb-122">Una tabella costante viene generata da [**D3DXCompileShader**](d3dxcompileshader.md) e incorporata nel corpo dello shader.</span><span class="sxs-lookup"><span data-stu-id="b4acb-122">A constant table is generated by [**D3DXCompileShader**](d3dxcompileshader.md) and embedded in the shader body.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4acb-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4acb-123">Requirements</span></span>



| <span data-ttu-id="b4acb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4acb-124">Requirement</span></span> | <span data-ttu-id="b4acb-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b4acb-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4acb-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4acb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b4acb-127"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="b4acb-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b4acb-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="b4acb-128">Library</span></span><br/> | <dl> <span data-ttu-id="b4acb-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4acb-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b4acb-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4acb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4acb-131">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="b4acb-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
