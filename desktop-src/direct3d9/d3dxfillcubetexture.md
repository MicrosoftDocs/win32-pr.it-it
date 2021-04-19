---
description: Usa una funzione fornita dall'utente per riempire ogni Texel di ogni livello MIP di una determinata trama del cubo.
ms.assetid: 0390a1b6-6675-42e1-bc45-65dd7b2d83c5
title: Funzione D3DXFillCubeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9fda70aa42d6982c40eb1ec926b6823e7ac7d997
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322702"
---
# <a name="d3dxfillcubetexture-function"></a><span data-ttu-id="e77d2-103">D3DXFillCubeTexture (funzione)</span><span class="sxs-lookup"><span data-stu-id="e77d2-103">D3DXFillCubeTexture function</span></span>

<span data-ttu-id="e77d2-104">Usa una funzione fornita dall'utente per riempire ogni Texel di ogni livello MIP di una determinata trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="e77d2-104">Uses a user-provided function to fill each texel of each mip level of a given cube texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e77d2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e77d2-105">Syntax</span></span>


```C++
HRESULT D3DXFillCubeTexture(
  _Out_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D           pFunction,
  _In_  LPVOID                 pData
);
```



## <a name="parameters"></a><span data-ttu-id="e77d2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e77d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e77d2-107">*pTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e77d2-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e77d2-108">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="e77d2-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="e77d2-109">Puntatore a un'interfaccia [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , che rappresenta la trama compilata.</span><span class="sxs-lookup"><span data-stu-id="e77d2-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="e77d2-110">*pFunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e77d2-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e77d2-111">Tipo: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span><span class="sxs-lookup"><span data-stu-id="e77d2-111">Type: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span></span>

<span data-ttu-id="e77d2-112">Puntatore a una funzione dell'analizzatore fornita dall'utente, che verrà usata per calcolare il valore di ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="e77d2-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="e77d2-113">La funzione segue il prototipo di [LPD3DXFILL3D](lpd3dxfill3d.md).</span><span class="sxs-lookup"><span data-stu-id="e77d2-113">The function follows the prototype of [LPD3DXFILL3D](lpd3dxfill3d.md).</span></span>

</dd> <dt>

<span data-ttu-id="e77d2-114">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e77d2-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e77d2-115">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e77d2-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e77d2-116">Puntatore a un blocco arbitrario di dati definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e77d2-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="e77d2-117">Questo puntatore verrà passato alla funzione fornita in *pFunction*.</span><span class="sxs-lookup"><span data-stu-id="e77d2-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e77d2-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e77d2-118">Return value</span></span>

<span data-ttu-id="e77d2-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e77d2-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e77d2-120">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e77d2-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e77d2-121">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e77d2-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e77d2-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="e77d2-122">Remarks</span></span>

<span data-ttu-id="e77d2-123">Di seguito è riportato un esempio in cui viene creata una funzione denominata ColorCubeFill, che si basa su D3DXFillCubeTexture.</span><span class="sxs-lookup"><span data-stu-id="e77d2-123">Here is an example that creates a function called ColorCubeFill, which relies on D3DXFillCubeTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorCubeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill the texture using D3DXFillCubeTexture
if (FAILED (hr = D3DXFillCubeTexture (m_pTexture, ColorCubeFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="e77d2-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e77d2-124">Requirements</span></span>



| <span data-ttu-id="e77d2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e77d2-125">Requirement</span></span> | <span data-ttu-id="e77d2-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e77d2-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e77d2-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e77d2-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e77d2-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e77d2-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e77d2-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="e77d2-129">Library</span></span><br/> | <dl> <span data-ttu-id="e77d2-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e77d2-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e77d2-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e77d2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e77d2-132">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e77d2-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
