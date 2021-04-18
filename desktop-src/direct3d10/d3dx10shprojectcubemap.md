---
description: Proietta una funzione rappresentata in una mappa cubo in armoniche sferiche.
ms.assetid: de8bc4bd-cb29-44ab-8806-33d3ffd10a7b
title: Funzione D3DX10SHProjectCubeMap (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SHProjectCubeMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fd991e2207f1ad556d9f9b5e648e296b857e884b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322766"
---
# <a name="d3dx10shprojectcubemap-function"></a><span data-ttu-id="83667-103">D3DX10SHProjectCubeMap (funzione)</span><span class="sxs-lookup"><span data-stu-id="83667-103">D3DX10SHProjectCubeMap function</span></span>

<span data-ttu-id="83667-104">Proietta una funzione rappresentata in una mappa cubo in armoniche sferiche.</span><span class="sxs-lookup"><span data-stu-id="83667-104">Projects a function represented in a cube map into spherical harmonics.</span></span>

## <a name="syntax"></a><span data-ttu-id="83667-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83667-105">Syntax</span></span>


```C++
HRESULT D3DX10SHProjectCubeMap(
   UINT            Order,
   ID3D10Texture2D *pCubeMap,
   FLOAT           *pROut,
   FLOAT           *pGOut,
   FLOAT           *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="83667-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="83667-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83667-107">*Ordine*</span><span class="sxs-lookup"><span data-stu-id="83667-107">*Order*</span></span> 
</dt> <dd>

<span data-ttu-id="83667-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83667-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83667-109">Ordine della valutazione SH, genera l'ordine ^ 2 coefs, Degree è Order-1.</span><span class="sxs-lookup"><span data-stu-id="83667-109">Order of the SH evaluation, generates Order^2 coefs, degree is Order-1.</span></span>

</dd> <dt>

<span data-ttu-id="83667-110">*pCubeMap*</span><span class="sxs-lookup"><span data-stu-id="83667-110">*pCubeMap*</span></span> 
</dt> <dd>

<span data-ttu-id="83667-111">Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="83667-111">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="83667-112">Mappa cubi che verrà proiettato in armoniche sferiche.</span><span class="sxs-lookup"><span data-stu-id="83667-112">Cubemap that is going to be projected into spherical harmonics.</span></span> <span data-ttu-id="83667-113">Vedere [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).</span><span class="sxs-lookup"><span data-stu-id="83667-113">See [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).</span></span>

</dd> <dt>

<span data-ttu-id="83667-114">*pROut*</span><span class="sxs-lookup"><span data-stu-id="83667-114">*pROut*</span></span> 
</dt> <dd>

<span data-ttu-id="83667-115">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="83667-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="83667-116">Output SH Vector per rosso.</span><span class="sxs-lookup"><span data-stu-id="83667-116">Output SH vector for red.</span></span>

</dd> <dt>

<span data-ttu-id="83667-117">*pGOut*</span><span class="sxs-lookup"><span data-stu-id="83667-117">*pGOut*</span></span> 
</dt> <dd>

<span data-ttu-id="83667-118">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="83667-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="83667-119">Output SH Vector per verde.</span><span class="sxs-lookup"><span data-stu-id="83667-119">Output SH vector for green.</span></span>

</dd> <dt>

<span data-ttu-id="83667-120">*pBOut*</span><span class="sxs-lookup"><span data-stu-id="83667-120">*pBOut*</span></span> 
</dt> <dd>

<span data-ttu-id="83667-121">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="83667-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="83667-122">Output SH Vector per Blue.</span><span class="sxs-lookup"><span data-stu-id="83667-122">Output SH vector for blue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83667-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83667-123">Return value</span></span>

<span data-ttu-id="83667-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83667-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83667-125">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="83667-125">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83667-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83667-126">Requirements</span></span>



| <span data-ttu-id="83667-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="83667-127">Requirement</span></span> | <span data-ttu-id="83667-128">Valore</span><span class="sxs-lookup"><span data-stu-id="83667-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83667-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83667-129">Header</span></span><br/>  | <dl> <span data-ttu-id="83667-130"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="83667-130"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="83667-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="83667-131">Library</span></span><br/> | <dl> <span data-ttu-id="83667-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83667-132"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="83667-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83667-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83667-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="83667-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
