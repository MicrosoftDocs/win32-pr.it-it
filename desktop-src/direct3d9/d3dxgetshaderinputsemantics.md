---
description: Ottiene la semantica per gli input dello shader. Utilizzare questo metodo per determinare il formato del vertice di input.
ms.assetid: e94b2b14-3830-4a13-8c23-7841a56d6730
title: Funzione D3DXGetShaderInputSemantics (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderInputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2032f241d6ca5c22506c0875a21f9d5b431920df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322659"
---
# <a name="d3dxgetshaderinputsemantics-function"></a><span data-ttu-id="9b9c8-104">D3DXGetShaderInputSemantics (funzione)</span><span class="sxs-lookup"><span data-stu-id="9b9c8-104">D3DXGetShaderInputSemantics function</span></span>

<span data-ttu-id="9b9c8-105">Ottiene la semantica per gli input dello shader.</span><span class="sxs-lookup"><span data-stu-id="9b9c8-105">Gets the semantics for the shader inputs.</span></span> <span data-ttu-id="9b9c8-106">Utilizzare questo metodo per determinare il formato del vertice di input.</span><span class="sxs-lookup"><span data-stu-id="9b9c8-106">Use this method to determine the input vertex format.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b9c8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b9c8-107">Syntax</span></span>


```C++
HRESULT D3DXGetShaderInputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="9b9c8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b9c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b9c8-109">*pFunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b9c8-109">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b9c8-110">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9b9c8-110">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9b9c8-111">Puntatore al flusso DWORD della funzione shader.</span><span class="sxs-lookup"><span data-stu-id="9b9c8-111">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="9b9c8-112">*pSemantics* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b9c8-112">*pSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b9c8-113">Tipo: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b9c8-113">Type: **[**D3DXSEMANTIC**](d3dxsemantic.md)\***</span></span>

<span data-ttu-id="9b9c8-114">Puntatore a una matrice di strutture [**D3DXSEMANTIC**](d3dxsemantic.md) .</span><span class="sxs-lookup"><span data-stu-id="9b9c8-114">Pointer to an array of [**D3DXSEMANTIC**](d3dxsemantic.md) structures.</span></span> <span data-ttu-id="9b9c8-115">La funzione riempirà questa matrice con la semantica per ogni elemento di input a cui fa riferimento lo shader.</span><span class="sxs-lookup"><span data-stu-id="9b9c8-115">The function will fill this array with the semantics for each input element referenced by the shader.</span></span> <span data-ttu-id="9b9c8-116">Si presuppone che questa matrice contenga almeno gli elementi MAXD3DDECLLENGTH.</span><span class="sxs-lookup"><span data-stu-id="9b9c8-116">This array is assumed to contain at least MAXD3DDECLLENGTH elements.</span></span> <span data-ttu-id="9b9c8-117">Tuttavia, la chiamata a **D3DXGetShaderInputSemantics** con PSemantics = **null** restituirà il numero di elementi necessari per pcount.</span><span class="sxs-lookup"><span data-stu-id="9b9c8-117">However, calling **D3DXGetShaderInputSemantics** with pSemantics = **NULL** will return the number of elements needed for pCount.</span></span>

</dd> <dt>

<span data-ttu-id="9b9c8-118">*pcount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9b9c8-118">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b9c8-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b9c8-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9b9c8-120">Restituisce il numero di elementi in pSemantics.</span><span class="sxs-lookup"><span data-stu-id="9b9c8-120">Returns the number of elements in pSemantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b9c8-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9b9c8-121">Return value</span></span>

<span data-ttu-id="9b9c8-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9b9c8-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9b9c8-123">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9b9c8-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9b9c8-124">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="9b9c8-124">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b9c8-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b9c8-125">Remarks</span></span>

<span data-ttu-id="9b9c8-126">Usare **D3DXGetShaderInputSemantics** per restituire un elenco di semantica di input richiesto dallo shader.</span><span class="sxs-lookup"><span data-stu-id="9b9c8-126">Use **D3DXGetShaderInputSemantics** to return a list of input semantics required by the shader.</span></span> <span data-ttu-id="9b9c8-127">Questo è il modo per individuare il formato del vertice di input per un shader HLSL (High-Level Shader Language).</span><span class="sxs-lookup"><span data-stu-id="9b9c8-127">This is the way to find out what the input vertex format is for a high-level shader language (HLSL) shader.</span></span> <span data-ttu-id="9b9c8-128">Se lo shader contiene input aggiuntivi che la dichiarazione del vertice non è presente, è possibile creare un flusso di vertici aggiuntivo con uno stride pari a 0 con i componenti mancanti con i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="9b9c8-128">If the shader has additional inputs that your vertex declaration is missing, you could create an extra vertex stream that has a stride of 0 that has the missing components with default values.</span></span> <span data-ttu-id="9b9c8-129">È ad esempio possibile usare questa tecnica per fornire il colore del vertice predefinito per i modelli che non lo specificano.</span><span class="sxs-lookup"><span data-stu-id="9b9c8-129">For instance, this technique could be used to provide default vertex color for models that do not specify it.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b9c8-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b9c8-130">Requirements</span></span>



| <span data-ttu-id="9b9c8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b9c8-131">Requirement</span></span> | <span data-ttu-id="9b9c8-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9b9c8-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b9c8-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b9c8-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9b9c8-134"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b9c8-134"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9b9c8-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="9b9c8-135">Library</span></span><br/> | <dl> <span data-ttu-id="9b9c8-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b9c8-136"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9b9c8-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b9c8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b9c8-138">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="9b9c8-138">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
