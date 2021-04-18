---
description: Proietta una funzione rappresentata su una mappa del cubo in armonica sferica (SH).
ms.assetid: da5a3195-801e-4f1c-b52c-9eafc6e2e7b4
title: Funzione D3DXSHProjectCubeMap (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHProjectCubeMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0e3e45b42907c47d8c7f1b9e5294738b8997cd6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323299"
---
# <a name="d3dxshprojectcubemap-function"></a><span data-ttu-id="b05b2-103">D3DXSHProjectCubeMap (funzione)</span><span class="sxs-lookup"><span data-stu-id="b05b2-103">D3DXSHProjectCubeMap function</span></span>

<span data-ttu-id="b05b2-104">Proietta una funzione rappresentata su una mappa del cubo in armonica sferica (SH).</span><span class="sxs-lookup"><span data-stu-id="b05b2-104">Projects a function represented on a cube map into spherical harmonics (SH).</span></span>

## <a name="syntax"></a><span data-ttu-id="b05b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b05b2-105">Syntax</span></span>


```C++
HRESULT D3DXSHProjectCubeMap(
  _In_ UINT                   Order,
  _In_ LPDIRECT3DCUBETEXTURE9 pCubeMap,
  _In_ FLOAT                  *pROut,
  _In_ FLOAT                  *pGOut,
  _In_ FLOAT                  *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="b05b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b05b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b05b2-107">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b05b2-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b05b2-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b05b2-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b05b2-109">Ordine della valutazione dell'armonica sferica (SH).</span><span class="sxs-lookup"><span data-stu-id="b05b2-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="b05b2-110">Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="b05b2-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="b05b2-111">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="b05b2-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="b05b2-112">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="b05b2-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="b05b2-113">*pCubeMap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b05b2-113">*pCubeMap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b05b2-114">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="b05b2-114">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="b05b2-115">Puntatore a una trama del cubo di origine.</span><span class="sxs-lookup"><span data-stu-id="b05b2-115">Pointer to a source cube texture.</span></span> <span data-ttu-id="b05b2-116">Vedere [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9).</span><span class="sxs-lookup"><span data-stu-id="b05b2-116">See [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9).</span></span>

</dd> <dt>

<span data-ttu-id="b05b2-117">*pROut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b05b2-117">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b05b2-118">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b05b2-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b05b2-119">Puntatore al vettore SH di output per il componente rosso.</span><span class="sxs-lookup"><span data-stu-id="b05b2-119">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="b05b2-120">*pGOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b05b2-120">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b05b2-121">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b05b2-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b05b2-122">Puntatore al vettore SH di output per il componente verde.</span><span class="sxs-lookup"><span data-stu-id="b05b2-122">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="b05b2-123">*pBOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b05b2-123">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b05b2-124">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b05b2-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b05b2-125">Puntatore al vettore SH di output per il componente blu.</span><span class="sxs-lookup"><span data-stu-id="b05b2-125">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b05b2-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b05b2-126">Return value</span></span>

<span data-ttu-id="b05b2-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b05b2-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b05b2-128">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b05b2-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b05b2-129">Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b05b2-129">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b05b2-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b05b2-130">Requirements</span></span>



| <span data-ttu-id="b05b2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b05b2-131">Requirement</span></span> | <span data-ttu-id="b05b2-132">Valore</span><span class="sxs-lookup"><span data-stu-id="b05b2-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b05b2-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b05b2-133">Header</span></span><br/>  | <dl> <span data-ttu-id="b05b2-134"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b05b2-134"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b05b2-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="b05b2-135">Library</span></span><br/> | <dl> <span data-ttu-id="b05b2-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b05b2-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b05b2-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b05b2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b05b2-138">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="b05b2-138">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b05b2-139">Trasferimento Radiance pre-calcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b05b2-139">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
