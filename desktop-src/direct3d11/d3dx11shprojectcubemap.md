---
title: Funzione D3DX11SHProjectCubeMap (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Si noti invece di usare questa funzione, è consigliabile usare la libreria matematica delle armoniche sferiche SHProjectCubeMap.
ms.assetid: 58c741a3-dd5d-4b18-b257-5e85a9b799fd
keywords:
- Funzione D3DX11SHProjectCubeMap Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SHProjectCubeMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf773c00a649e6ace065fcf552358fbf5eeb19c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995981"
---
# <a name="d3dx11shprojectcubemap-function"></a><span data-ttu-id="9eec4-105">D3DX11SHProjectCubeMap (funzione)</span><span class="sxs-lookup"><span data-stu-id="9eec4-105">D3DX11SHProjectCubeMap function</span></span>

> [!Note]  
> <span data-ttu-id="9eec4-106">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9eec4-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="9eec4-107">Invece di usare questa funzione, è consigliabile usare la libreria [matematica delle armoniche sferiche](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) **SHProjectCubeMap**.</span><span class="sxs-lookup"><span data-stu-id="9eec4-107">Instead of using this function, we recommend that you use the [Spherical Harmonics Math](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) library, **SHProjectCubeMap**.</span></span>

 

<span data-ttu-id="9eec4-108">Proietta una funzione rappresentata in una mappa cubo in armoniche sferiche.</span><span class="sxs-lookup"><span data-stu-id="9eec4-108">Projects a function represented in a cube map into spherical harmonics.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eec4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9eec4-109">Syntax</span></span>


```C++
HRESULT D3DX11SHProjectCubeMap(
   ID3D11DeviceContext *pContext,
   UINT                Order,
   ID3D11Texture2D     *pCubeMap,
   FLOAT               *pROut,
   FLOAT               *pGOut,
   FLOAT               *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="9eec4-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="9eec4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eec4-111">*pContext*</span><span class="sxs-lookup"><span data-stu-id="9eec4-111">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="9eec4-112">Tipo: **[ **sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="9eec4-112">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="9eec4-113">Puntatore a un oggetto [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="9eec4-113">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="9eec4-114">*Ordine*</span><span class="sxs-lookup"><span data-stu-id="9eec4-114">*Order*</span></span> 
</dt> <dd>

<span data-ttu-id="9eec4-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9eec4-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9eec4-116">Ordine della valutazione SH, genera coefficienti Order ^ 2 il cui grado è Order-1.</span><span class="sxs-lookup"><span data-stu-id="9eec4-116">Order of the SH evaluation, generates Order^2 coefficients whose degree is Order-1.</span></span> <span data-ttu-id="9eec4-117">L'intervallo valido è compreso tra 2 e 6.</span><span class="sxs-lookup"><span data-stu-id="9eec4-117">Valid range is between 2 and 6.</span></span>

</dd> <dt>

<span data-ttu-id="9eec4-118">*pCubeMap*</span><span class="sxs-lookup"><span data-stu-id="9eec4-118">*pCubeMap*</span></span> 
</dt> <dd>

<span data-ttu-id="9eec4-119">Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="9eec4-119">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="9eec4-120">Puntatore a un [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) che rappresenta un mappa cubi che verrà proiettato in armoniche sferiche.</span><span class="sxs-lookup"><span data-stu-id="9eec4-120">A pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) that represents a cubemap that is going to be projected into spherical harmonics.</span></span>

</dd> <dt>

<span data-ttu-id="9eec4-121">*pROut*</span><span class="sxs-lookup"><span data-stu-id="9eec4-121">*pROut*</span></span> 
</dt> <dd>

<span data-ttu-id="9eec4-122">Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="9eec4-122">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="9eec4-123">Output SH Vector per rosso.</span><span class="sxs-lookup"><span data-stu-id="9eec4-123">Output SH vector for red.</span></span>

</dd> <dt>

<span data-ttu-id="9eec4-124">*pGOut*</span><span class="sxs-lookup"><span data-stu-id="9eec4-124">*pGOut*</span></span> 
</dt> <dd>

<span data-ttu-id="9eec4-125">Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="9eec4-125">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="9eec4-126">Output SH Vector per verde.</span><span class="sxs-lookup"><span data-stu-id="9eec4-126">Output SH vector for green.</span></span>

</dd> <dt>

<span data-ttu-id="9eec4-127">*pBOut*</span><span class="sxs-lookup"><span data-stu-id="9eec4-127">*pBOut*</span></span> 
</dt> <dd>

<span data-ttu-id="9eec4-128">Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="9eec4-128">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="9eec4-129">Output SH Vector per Blue.</span><span class="sxs-lookup"><span data-stu-id="9eec4-129">Output SH vector for blue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eec4-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9eec4-130">Return value</span></span>

<span data-ttu-id="9eec4-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9eec4-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9eec4-132">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9eec4-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9eec4-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9eec4-133">Requirements</span></span>



| <span data-ttu-id="9eec4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eec4-134">Requirement</span></span> | <span data-ttu-id="9eec4-135">Valore</span><span class="sxs-lookup"><span data-stu-id="9eec4-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9eec4-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9eec4-136">Header</span></span><br/>  | <dl> <span data-ttu-id="9eec4-137"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eec4-137"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="9eec4-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="9eec4-138">Library</span></span><br/> | <dl> <span data-ttu-id="9eec4-139"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9eec4-139"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9eec4-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9eec4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eec4-141">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="9eec4-141">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

