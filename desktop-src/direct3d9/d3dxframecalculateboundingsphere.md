---
description: Calcola l'ambito di delimitazione di tutti i mesh nella gerarchia dei frame.
ms.assetid: 8c3f5a9e-73ff-4d83-8f85-a3fc2a9a53f7
title: Funzione D3DXFrameCalculateBoundingSphere (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameCalculateBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f10043d2c897bf6ab24c442b8e134f31221c498e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322685"
---
# <a name="d3dxframecalculateboundingsphere-function"></a><span data-ttu-id="86c5e-103">D3DXFrameCalculateBoundingSphere (funzione)</span><span class="sxs-lookup"><span data-stu-id="86c5e-103">D3DXFrameCalculateBoundingSphere function</span></span>

<span data-ttu-id="86c5e-104">Calcola l'ambito di delimitazione di tutti i mesh nella gerarchia dei frame.</span><span class="sxs-lookup"><span data-stu-id="86c5e-104">Computes the bounding sphere of all the meshes in the frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="86c5e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86c5e-105">Syntax</span></span>


```C++
HRESULT D3DXFrameCalculateBoundingSphere(
  _In_  const D3DXFRAME     *pFrameRoot,
  _Out_       LPD3DXVECTOR3 pObjectCenter,
  _Out_       FLOAT         *pObjectRadius
);
```



## <a name="parameters"></a><span data-ttu-id="86c5e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="86c5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86c5e-107">*pFrameRoot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86c5e-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c5e-108">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="86c5e-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="86c5e-109">Puntatore al nodo radice.</span><span class="sxs-lookup"><span data-stu-id="86c5e-109">Pointer to the root node.</span></span>

</dd> <dt>

<span data-ttu-id="86c5e-110">*pObjectCenter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="86c5e-110">*pObjectCenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86c5e-111">Tipo: **[ **LPD3DXVECTOR3**](d3dxvector3.md)**</span><span class="sxs-lookup"><span data-stu-id="86c5e-111">Type: **[**LPD3DXVECTOR3**](d3dxvector3.md)**</span></span>

<span data-ttu-id="86c5e-112">Restituisce il centro della sfera di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="86c5e-112">Returns the center of the bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="86c5e-113">*pObjectRadius* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="86c5e-113">*pObjectRadius* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86c5e-114">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="86c5e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="86c5e-115">Restituisce il raggio della sfera di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="86c5e-115">Returns the radius of the bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86c5e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86c5e-116">Return value</span></span>

<span data-ttu-id="86c5e-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="86c5e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="86c5e-118">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="86c5e-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="86c5e-119">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="86c5e-119">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="86c5e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86c5e-120">Requirements</span></span>



| <span data-ttu-id="86c5e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="86c5e-121">Requirement</span></span> | <span data-ttu-id="86c5e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="86c5e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86c5e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86c5e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="86c5e-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="86c5e-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="86c5e-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="86c5e-125">Library</span></span><br/> | <dl> <span data-ttu-id="86c5e-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86c5e-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="86c5e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86c5e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c5e-128">Funzioni di animazione</span><span class="sxs-lookup"><span data-stu-id="86c5e-128">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
