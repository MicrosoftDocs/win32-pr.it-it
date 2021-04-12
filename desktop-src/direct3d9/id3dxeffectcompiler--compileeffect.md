---
description: Compilare un effetto.
ms.assetid: be6f862a-5091-4a06-a27a-308e81360129
title: 'Metodo ID3DXEffectCompiler:: CompileEffect (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6552d0216cd05c40c122657270c02e0886438da1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354349"
---
# <a name="id3dxeffectcompilercompileeffect-method"></a><span data-ttu-id="bba23-103">Metodo ID3DXEffectCompiler:: CompileEffect</span><span class="sxs-lookup"><span data-stu-id="bba23-103">ID3DXEffectCompiler::CompileEffect method</span></span>

<span data-ttu-id="bba23-104">Compilare un effetto.</span><span class="sxs-lookup"><span data-stu-id="bba23-104">Compile an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba23-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bba23-105">Syntax</span></span>


```C++
HRESULT CompileEffect(
  [in]          DWORD        Flags,
  [out, retval] LPD3DXBUFFER *ppEffect,
  [out, retval] LPD3DXBUFFER *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="bba23-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bba23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bba23-107">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bba23-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba23-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bba23-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bba23-109">Opzioni di compilazione identificate da diversi flag.</span><span class="sxs-lookup"><span data-stu-id="bba23-109">Compile options identified by various flags.</span></span> <span data-ttu-id="bba23-110">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="bba23-110">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="bba23-111">Per informazioni dettagliate, vedere [flag D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="bba23-111">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="bba23-112">*ppEffect* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bba23-112">*ppEffect* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bba23-113">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bba23-113">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="bba23-114">Buffer contenente l'effetto compilato.</span><span class="sxs-lookup"><span data-stu-id="bba23-114">Buffer containing the compiled effect.</span></span> <span data-ttu-id="bba23-115">Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="bba23-115">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba23-116">*ppErrorMsgs* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bba23-116">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bba23-117">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bba23-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="bba23-118">Buffer contenente almeno il primo messaggio di errore di compilazione che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="bba23-118">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="bba23-119">Sono inclusi gli errori del compilatore degli effetti e gli errori di compilazione del linguaggio di alto livello.</span><span class="sxs-lookup"><span data-stu-id="bba23-119">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="bba23-120">Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="bba23-120">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bba23-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bba23-121">Return value</span></span>

<span data-ttu-id="bba23-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bba23-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bba23-123">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bba23-123">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="bba23-124">Se gli argomenti non sono validi, il metodo restituirà D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bba23-124">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="bba23-125">Se il metodo ha esito negativo, il valore restituito sarà E avrà \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="bba23-125">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bba23-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bba23-126">Requirements</span></span>



| <span data-ttu-id="bba23-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bba23-127">Requirement</span></span> | <span data-ttu-id="bba23-128">Valore</span><span class="sxs-lookup"><span data-stu-id="bba23-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bba23-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bba23-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bba23-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bba23-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="bba23-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="bba23-131">Library</span></span><br/> | <dl> <span data-ttu-id="bba23-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bba23-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bba23-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bba23-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba23-134">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="bba23-134">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> </dl>

 

 
