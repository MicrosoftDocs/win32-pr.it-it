---
description: Crea un'istanza dell'interfaccia ID3DXMATRIXStack.
ms.assetid: bb067b38-efc6-4ed8-9eef-14b3cc70660f
title: Funzione D3DXCreateMatrixStack (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMatrixStack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 08e1ac23d5f6bcd874b1d5bd7f60313a232b0563
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323252"
---
# <a name="d3dxcreatematrixstack-function-d3dx9mathh"></a><span data-ttu-id="764cf-103">Funzione D3DXCreateMatrixStack (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="764cf-103">D3DXCreateMatrixStack function (D3dx9math.h)</span></span>

<span data-ttu-id="764cf-104">Crea un'istanza dell'interfaccia [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="764cf-104">Creates an instance of the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="764cf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="764cf-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  DWORD             Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a><span data-ttu-id="764cf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="764cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="764cf-107">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="764cf-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="764cf-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="764cf-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="764cf-109">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="764cf-109">Not implemented.</span></span> <span data-ttu-id="764cf-110">Specificare zero.</span><span class="sxs-lookup"><span data-stu-id="764cf-110">Specify zero.</span></span>

</dd> <dt>

<span data-ttu-id="764cf-111">*ppStack* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="764cf-111">*ppStack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="764cf-112">Tipo: **LPD3DXMATRIXSTACK \***</span><span class="sxs-lookup"><span data-stu-id="764cf-112">Type: **LPD3DXMATRIXSTACK\***</span></span>

<span data-ttu-id="764cf-113">Indirizzo di un puntatore riempito con un puntatore a interfaccia [**ID3DXMATRIXStack**](id3dxmatrixstack.md) se la funzione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="764cf-113">Address of a pointer filled with an [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface pointer if the function succeeds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="764cf-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="764cf-114">Return value</span></span>

<span data-ttu-id="764cf-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="764cf-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="764cf-116">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="764cf-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="764cf-117">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="764cf-117">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="764cf-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="764cf-118">Requirements</span></span>



| <span data-ttu-id="764cf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="764cf-119">Requirement</span></span> | <span data-ttu-id="764cf-120">Valore</span><span class="sxs-lookup"><span data-stu-id="764cf-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="764cf-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="764cf-121">Header</span></span><br/>  | <dl> <span data-ttu-id="764cf-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="764cf-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="764cf-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="764cf-123">Library</span></span><br/> | <dl> <span data-ttu-id="764cf-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="764cf-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="764cf-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="764cf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="764cf-126">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="764cf-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
