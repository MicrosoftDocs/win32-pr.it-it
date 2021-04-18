---
description: Disassemblare un effetto.
ms.assetid: d95d6e97-2e79-4cd2-965e-483aa1a1ddbc
title: Funzione D3DXDisassembleEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 945c30319d16264a2b7489d1dc0849a4678cbede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322712"
---
# <a name="d3dxdisassembleeffect-function"></a><span data-ttu-id="b6ff2-103">D3DXDisassembleEffect (funzione)</span><span class="sxs-lookup"><span data-stu-id="b6ff2-103">D3DXDisassembleEffect function</span></span>

<span data-ttu-id="b6ff2-104">Disassemblare un effetto.</span><span class="sxs-lookup"><span data-stu-id="b6ff2-104">Disassemble an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6ff2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6ff2-105">Syntax</span></span>


```C++
HRESULT D3DXDisassembleEffect(
  _In_  LPD3DXEFFECT pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="b6ff2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6ff2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6ff2-107">*pEffect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6ff2-107">*pEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6ff2-108">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="b6ff2-108">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)**</span></span>

<span data-ttu-id="b6ff2-109">Puntatore a un'interfaccia [**ID3DXEffect**](id3dxeffect.md) che contiene l'effetto.</span><span class="sxs-lookup"><span data-stu-id="b6ff2-109">Pointer to an [**ID3DXEffect**](id3dxeffect.md) interface that contains the effect.</span></span>

</dd> <dt>

<span data-ttu-id="b6ff2-110">*EnableColorCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6ff2-110">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6ff2-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6ff2-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6ff2-112">Abilitare la codifica a colori per semplificare la lettura del Disassembly.</span><span class="sxs-lookup"><span data-stu-id="b6ff2-112">Enable color coding to make the disassembly easier to read.</span></span>

</dd> <dt>

<span data-ttu-id="b6ff2-113">*ppDisassembly* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b6ff2-113">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6ff2-114">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b6ff2-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b6ff2-115">Restituisce un buffer contenente lo shader disassemblato.</span><span class="sxs-lookup"><span data-stu-id="b6ff2-115">Returns a buffer containing the disassembled shader.</span></span> <span data-ttu-id="b6ff2-116">Vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="b6ff2-116">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6ff2-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6ff2-117">Return value</span></span>

<span data-ttu-id="b6ff2-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b6ff2-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b6ff2-119">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b6ff2-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b6ff2-120">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b6ff2-120">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6ff2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6ff2-121">Requirements</span></span>



| <span data-ttu-id="b6ff2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6ff2-122">Requirement</span></span> | <span data-ttu-id="b6ff2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b6ff2-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ff2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6ff2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b6ff2-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6ff2-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b6ff2-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="b6ff2-126">Library</span></span><br/> | <dl> <span data-ttu-id="b6ff2-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6ff2-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b6ff2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6ff2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ff2-129">Funzioni effetto</span><span class="sxs-lookup"><span data-stu-id="b6ff2-129">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 
