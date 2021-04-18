---
description: Ottiene i nomi dei sampler a cui si fa riferimento in uno shader.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: Funzione D3DXGetShaderSamplers (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSamplers
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2135ba36f238188c6e7817001ba89bb47e3b9998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322657"
---
# <a name="d3dxgetshadersamplers-function"></a><span data-ttu-id="a3244-103">D3DXGetShaderSamplers (funzione)</span><span class="sxs-lookup"><span data-stu-id="a3244-103">D3DXGetShaderSamplers function</span></span>

<span data-ttu-id="a3244-104">Ottiene i nomi dei sampler a cui si fa riferimento in uno shader.</span><span class="sxs-lookup"><span data-stu-id="a3244-104">Get the sampler names referenced in a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3244-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3244-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderSamplers(
  _In_    const DWORD  *pFunction,
  _Inout_       LPCSTR *pSamplers,
  _Out_         UINT   *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="a3244-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3244-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3244-107">*pFunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3244-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3244-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3244-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a3244-109">Puntatore al flusso DWORD della funzione shader.</span><span class="sxs-lookup"><span data-stu-id="a3244-109">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="a3244-110">*pSamplers* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a3244-110">*pSamplers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3244-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3244-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a3244-112">Puntatore a una matrice di LPCSTRs.</span><span class="sxs-lookup"><span data-stu-id="a3244-112">Pointer to an array of LPCSTRs.</span></span> <span data-ttu-id="a3244-113">La funzione riempirà questa matrice con i puntatori ai nomi del campionatore contenuti in *pFunction*.</span><span class="sxs-lookup"><span data-stu-id="a3244-113">The function will fill this array with pointers to the sampler names contained within *pFunction*.</span></span> <span data-ttu-id="a3244-114">La dimensione massima della matrice è il numero massimo di registri del campionatore (16 per vs \_ 3 \_ 0 e PS \_ 3 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="a3244-114">The maximum array size is the maximum number of sampler registers (16 for vs\_3\_0 and ps\_3\_0).</span></span>

<span data-ttu-id="a3244-115">Per trovare il numero di campioni utilizzati, controllare *pcount* dopo aver chiamato **D3DXGetShaderSamplers** con pSamplers = **null**.</span><span class="sxs-lookup"><span data-stu-id="a3244-115">To find the number of samplers used, check *pCount* after calling **D3DXGetShaderSamplers** with pSamplers = **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a3244-116">*pcount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a3244-116">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3244-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3244-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a3244-118">Restituisce il numero di campioni a cui fa riferimento lo shader.</span><span class="sxs-lookup"><span data-stu-id="a3244-118">Returns the number of samplers referenced by the shader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3244-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3244-119">Return value</span></span>

<span data-ttu-id="a3244-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a3244-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a3244-121">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a3244-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a3244-122">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="a3244-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3244-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3244-123">Requirements</span></span>



| <span data-ttu-id="a3244-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3244-124">Requirement</span></span> | <span data-ttu-id="a3244-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a3244-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3244-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3244-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a3244-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3244-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a3244-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="a3244-128">Library</span></span><br/> | <dl> <span data-ttu-id="a3244-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3244-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a3244-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3244-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3244-131">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="a3244-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
