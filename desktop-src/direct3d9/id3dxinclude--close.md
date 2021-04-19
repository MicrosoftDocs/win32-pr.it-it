---
description: Metodo implementato dall'utente per la chiusura di un \# file di inclusione dello shader.
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: 'Metodo ID3DXInclude:: Close (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Close
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b60d01d59a4e54fa0d50c16a3fc845ea4e316792
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323537"
---
# <a name="id3dxincludeclose-method"></a><span data-ttu-id="fac3e-103">Metodo ID3DXInclude:: Close</span><span class="sxs-lookup"><span data-stu-id="fac3e-103">ID3DXInclude::Close method</span></span>

<span data-ttu-id="fac3e-104">Metodo implementato dall'utente per la chiusura di un \# file di inclusione dello shader.</span><span class="sxs-lookup"><span data-stu-id="fac3e-104">A user-implemented method for closing a shader \#include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac3e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fac3e-105">Syntax</span></span>


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a><span data-ttu-id="fac3e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fac3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac3e-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fac3e-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fac3e-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fac3e-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fac3e-109">Puntatore al buffer restituito che contiene le direttive include.</span><span class="sxs-lookup"><span data-stu-id="fac3e-109">Pointer to the returned buffer that contains the include directives.</span></span> <span data-ttu-id="fac3e-110">Si tratta del puntatore restituito dalla chiamata [**ID3DXInclude:: Open**](id3dxinclude--open.md) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="fac3e-110">This is the pointer that was returned by the corresponding [**ID3DXInclude::Open**](id3dxinclude--open.md) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fac3e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fac3e-111">Return value</span></span>

<span data-ttu-id="fac3e-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fac3e-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fac3e-113">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fac3e-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="fac3e-114">Se il callback ha esito negativo durante la lettura del \# file di inclusione, l'API che ha causato la chiamata al callback avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="fac3e-114">If the callback fails when reading the \#include file, the API that caused the callback to be called will fail.</span></span> <span data-ttu-id="fac3e-115">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fac3e-115">This is one of the following:</span></span>

-   <span data-ttu-id="fac3e-116">Lo shader HLSL non riuscirà a eseguire una delle \* \* \* funzioni D3DXCompileShader.</span><span class="sxs-lookup"><span data-stu-id="fac3e-116">The HLSL shader will fail one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="fac3e-117">L'assembly shader non riuscirà a eseguire una delle \* \* \* funzioni D3DXAssembleShader.</span><span class="sxs-lookup"><span data-stu-id="fac3e-117">The assembly shader will fail one of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="fac3e-118">L'effetto avrà esito negativo per una delle \* \* \* funzioni D3DXCreateEffect o D3DXCreateEffectCompiler \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="fac3e-118">The effect will fail one of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="remarks"></a><span data-ttu-id="fac3e-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="fac3e-119">Remarks</span></span>

<span data-ttu-id="fac3e-120">Se [**ID3DXInclude:: Open**](id3dxinclude--open.md) ha avuto esito positivo, viene garantita la chiamata a **ID3DXInclude:: Close** prima che l'API che usa questa interfaccia restituisca.</span><span class="sxs-lookup"><span data-stu-id="fac3e-120">If [**ID3DXInclude::Open**](id3dxinclude--open.md) was successful, **ID3DXInclude::Close** is guaranteed to be called before the API using this interface returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="fac3e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fac3e-121">Requirements</span></span>



| <span data-ttu-id="fac3e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fac3e-122">Requirement</span></span> | <span data-ttu-id="fac3e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="fac3e-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fac3e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fac3e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fac3e-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fac3e-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fac3e-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="fac3e-126">Library</span></span><br/> | <dl> <span data-ttu-id="fac3e-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fac3e-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fac3e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fac3e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac3e-129">ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="fac3e-129">ID3DXInclude</span></span>](id3dxinclude.md)
</dt> <dt>

[<span data-ttu-id="fac3e-130">**ID3DXInclude:: Open**</span><span class="sxs-lookup"><span data-stu-id="fac3e-130">**ID3DXInclude::Open**</span></span>](id3dxinclude--open.md)
</dt> </dl>

 

 
