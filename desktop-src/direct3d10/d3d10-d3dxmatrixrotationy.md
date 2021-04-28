---
description: "Funzione D3DXMatrixRotationY (D3DX10Math.h): compila una matrice che ruota intorno all'asse y."
ms.assetid: b58def9b-29dc-4c7d-89a3-188ef9b9f94f
title: Funzione D3DXMatrixRotationY (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationY
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 570179fadc9008c5f919acf657541e53ab399ac8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108969"
---
# <a name="d3dxmatrixrotationy-function-d3dx10mathh"></a><span data-ttu-id="17f62-103">Funzione D3DXMatrixRotationY (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="17f62-103">D3DXMatrixRotationY function (D3DX10Math.h)</span></span>

<span data-ttu-id="17f62-104">Compila una matrice che ruota intorno all'asse y.</span><span class="sxs-lookup"><span data-stu-id="17f62-104">Builds a matrix that rotates around the y-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="17f62-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17f62-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationY(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="17f62-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="17f62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17f62-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="17f62-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="17f62-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="17f62-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="17f62-109">Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="17f62-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="17f62-110">*Angolo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="17f62-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17f62-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="17f62-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="17f62-112">Angolo di rotazione in radianti.</span><span class="sxs-lookup"><span data-stu-id="17f62-112">Angle of rotation in radians.</span></span> <span data-ttu-id="17f62-113">Gli angoli vengono misurati in senso orario quando si guarda lungo l'asse di rotazione verso l'origine.</span><span class="sxs-lookup"><span data-stu-id="17f62-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17f62-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17f62-114">Return value</span></span>

<span data-ttu-id="17f62-115">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="17f62-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="17f62-116">Puntatore a una struttura D3DXMATRIX ruotata intorno all'asse y.</span><span class="sxs-lookup"><span data-stu-id="17f62-116">Pointer to a D3DXMATRIX structure rotated around the y-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="17f62-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="17f62-117">Remarks</span></span>

<span data-ttu-id="17f62-118">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="17f62-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="17f62-119">In questo modo, la funzione D3DXMatrixRotationY può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="17f62-119">In this way, the D3DXMatrixRotationY function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="17f62-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17f62-120">Requirements</span></span>



| <span data-ttu-id="17f62-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="17f62-121">Requirement</span></span> | <span data-ttu-id="17f62-122">Valore</span><span class="sxs-lookup"><span data-stu-id="17f62-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17f62-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17f62-123">Header</span></span><br/>  | <dl> <span data-ttu-id="17f62-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="17f62-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="17f62-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="17f62-125">Library</span></span><br/> | <dl> <span data-ttu-id="17f62-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="17f62-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="17f62-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17f62-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f62-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="17f62-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
