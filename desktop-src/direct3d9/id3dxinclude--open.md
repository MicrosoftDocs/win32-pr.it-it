---
description: Metodo implementato dall'utente per l'apertura e la lettura del contenuto di un \# file di inclusione dello shader.
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: 'Metodo ID3DXInclude:: Open (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Open
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 313b3f4845f9a46f758a40b6b315cc5b5eeecb29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323532"
---
# <a name="id3dxincludeopen-method"></a><span data-ttu-id="30efa-103">Metodo ID3DXInclude:: Open</span><span class="sxs-lookup"><span data-stu-id="30efa-103">ID3DXInclude::Open method</span></span>

<span data-ttu-id="30efa-104">Metodo implementato dall'utente per l'apertura e la lettura del contenuto di un \# file di inclusione dello shader.</span><span class="sxs-lookup"><span data-stu-id="30efa-104">A user-implemented method for opening and reading the contents of a shader \#include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="30efa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30efa-105">Syntax</span></span>


```C++
HRESULT Open(
  [in]  D3DXINCLUDE_TYPE IncludeType,
  [in]  LPCSTR           pFileName,
  [in]  LPCVOID          pParentData,
  [out] LPCVOID          *ppData,
  [out] UINT             *pBytes
);
```



## <a name="parameters"></a><span data-ttu-id="30efa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="30efa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30efa-107">*IncludeType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30efa-107">*IncludeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30efa-108">Tipo: **[ **D3DXINCLUDE \_**](./d3dxinclude-type.md)**</span><span class="sxs-lookup"><span data-stu-id="30efa-108">Type: **[**D3DXINCLUDE\_TYPE**](./d3dxinclude-type.md)**</span></span>

<span data-ttu-id="30efa-109">Percorso del file di \# inclusione.</span><span class="sxs-lookup"><span data-stu-id="30efa-109">The location of the \#include file.</span></span> <span data-ttu-id="30efa-110">Vedere [**D3DXINCLUDE \_ Type**](./d3dxinclude-type.md).</span><span class="sxs-lookup"><span data-stu-id="30efa-110">See [**D3DXINCLUDE\_TYPE**](./d3dxinclude-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="30efa-111">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30efa-111">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30efa-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30efa-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30efa-113">Nome del \# file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="30efa-113">Name of the \#include file.</span></span>

</dd> <dt>

<span data-ttu-id="30efa-114">*pParentData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30efa-114">*pParentData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30efa-115">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30efa-115">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30efa-116">Puntatore al contenitore che include il \# file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="30efa-116">Pointer to the container that includes the \#include file.</span></span> <span data-ttu-id="30efa-117">Il compilatore potrebbe passare NULL in *pParentData*.</span><span class="sxs-lookup"><span data-stu-id="30efa-117">The compiler might pass NULL in *pParentData*.</span></span> <span data-ttu-id="30efa-118">Per ulteriori informazioni, vedere la sezione "ricerca di file di inclusione" in [compilare un effetto (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).</span><span class="sxs-lookup"><span data-stu-id="30efa-118">For more information, see the "Searching for Include Files" section in [Compile an Effect (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).</span></span>

</dd> <dt>

<span data-ttu-id="30efa-119">*ppData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="30efa-119">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30efa-120">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="30efa-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="30efa-121">Puntatore al buffer restituito che contiene le direttive include.</span><span class="sxs-lookup"><span data-stu-id="30efa-121">Pointer to the returned buffer that contains the include directives.</span></span> <span data-ttu-id="30efa-122">Questo puntatore rimane valido fino a quando non viene chiamato [**ID3DXInclude:: Close**](id3dxinclude--close.md) .</span><span class="sxs-lookup"><span data-stu-id="30efa-122">This pointer remains valid until [**ID3DXInclude::Close**](id3dxinclude--close.md) is called.</span></span>

</dd> <dt>

<span data-ttu-id="30efa-123">*pBytes* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="30efa-123">*pBytes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30efa-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="30efa-124">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="30efa-125">Numero di byte restituiti in ppData.</span><span class="sxs-lookup"><span data-stu-id="30efa-125">Number of bytes returned in ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30efa-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30efa-126">Return value</span></span>

<span data-ttu-id="30efa-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30efa-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30efa-128">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="30efa-128">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="30efa-129">Se il callback ha esito negativo durante la lettura del \# file di inclusione, l'API che ha causato la chiamata al callback avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="30efa-129">If the callback fails when reading the \#include file, the API that caused the callback to be called will fail.</span></span> <span data-ttu-id="30efa-130">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="30efa-130">This is one of the following:</span></span>

-   <span data-ttu-id="30efa-131">Lo shader HLSL non riuscirà a eseguire una delle \* \* \* funzioni D3DXCompileShader.</span><span class="sxs-lookup"><span data-stu-id="30efa-131">The HLSL shader will fail one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="30efa-132">L'assembly shader non riuscirà a eseguire una delle \* \* \* funzioni D3DXAssembleShader.</span><span class="sxs-lookup"><span data-stu-id="30efa-132">The assembly shader will fail one of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="30efa-133">L'effetto avrà esito negativo per una delle \* \* \* funzioni D3DXCreateEffect o D3DXCreateEffectCompiler \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="30efa-133">The effect will fail one of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="30efa-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30efa-134">Requirements</span></span>



| <span data-ttu-id="30efa-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="30efa-135">Requirement</span></span> | <span data-ttu-id="30efa-136">Valore</span><span class="sxs-lookup"><span data-stu-id="30efa-136">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="30efa-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30efa-137">Header</span></span><br/>  | <dl> <span data-ttu-id="30efa-138"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="30efa-138"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="30efa-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="30efa-139">Library</span></span><br/> | <dl> <span data-ttu-id="30efa-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30efa-140"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="30efa-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30efa-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30efa-142">ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="30efa-142">ID3DXInclude</span></span>](id3dxinclude.md)
</dt> <dt>

[<span data-ttu-id="30efa-143">**ID3DXInclude:: Close**</span><span class="sxs-lookup"><span data-stu-id="30efa-143">**ID3DXInclude::Close**</span></span>](id3dxinclude--close.md)
</dt> </dl>

 

 
