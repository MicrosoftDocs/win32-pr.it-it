---
description: Creare uno stack di matrici.
ms.assetid: df0f3564-0226-44b8-b22b-4dd27905c44c
title: Funzione D3DXCreateMatrixStack (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b5799632f171d1b80f95f0f684bb22d24f741f6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104402001"
---
# <a name="d3dxcreatematrixstack-function-d3dx10mathh"></a><span data-ttu-id="edc21-103">Funzione D3DXCreateMatrixStack (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="edc21-103">D3DXCreateMatrixStack function (D3DX10Math.h)</span></span>

<span data-ttu-id="edc21-104">Creare uno stack di matrici.</span><span class="sxs-lookup"><span data-stu-id="edc21-104">Create a matrix stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="edc21-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="edc21-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  UINT              Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a><span data-ttu-id="edc21-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="edc21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edc21-107">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edc21-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edc21-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="edc21-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="edc21-109">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="edc21-109">Not implemented.</span></span> <span data-ttu-id="edc21-110">Specificare zero.</span><span class="sxs-lookup"><span data-stu-id="edc21-110">Specify zero.</span></span>

</dd> <dt>

<span data-ttu-id="edc21-111">*ppStack* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="edc21-111">*ppStack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edc21-112">Tipo: **LPD3DXMATRIXSTACK \***</span><span class="sxs-lookup"><span data-stu-id="edc21-112">Type: **LPD3DXMATRIXSTACK\***</span></span>

<span data-ttu-id="edc21-113">Indirizzo di un puntatore a uno stack di matrici (vedere [**interfaccia ID3DXMatrixStack**](d3d10-id3dxmatrixstack.md)).</span><span class="sxs-lookup"><span data-stu-id="edc21-113">The address of a pointer to a matrix stack (see [**ID3DXMatrixStack Interface**](d3d10-id3dxmatrixstack.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edc21-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="edc21-114">Return value</span></span>

<span data-ttu-id="edc21-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="edc21-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="edc21-116">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="edc21-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="edc21-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edc21-117">Requirements</span></span>



| <span data-ttu-id="edc21-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="edc21-118">Requirement</span></span> | <span data-ttu-id="edc21-119">Valore</span><span class="sxs-lookup"><span data-stu-id="edc21-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="edc21-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="edc21-120">Header</span></span><br/>  | <dl> <span data-ttu-id="edc21-121"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="edc21-121"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="edc21-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="edc21-122">Library</span></span><br/> | <dl> <span data-ttu-id="edc21-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="edc21-123"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="edc21-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="edc21-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edc21-125">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="edc21-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
