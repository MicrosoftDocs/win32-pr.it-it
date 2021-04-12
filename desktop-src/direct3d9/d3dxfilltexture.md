---
description: Usa una funzione fornita dall'utente per riempire ogni Texel di ogni livello MIP di una determinata trama.
ms.assetid: 9c822472-2bbf-4629-bdb3-6491573e8de2
title: Funzione D3DXFillTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20790a9e4c1a9ce242a5e067dd617c7871a70b7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354864"
---
# <a name="d3dxfilltexture-function"></a><span data-ttu-id="a3fb3-103">D3DXFillTexture (funzione)</span><span class="sxs-lookup"><span data-stu-id="a3fb3-103">D3DXFillTexture function</span></span>

<span data-ttu-id="a3fb3-104">Usa una funzione fornita dall'utente per riempire ogni Texel di ogni livello MIP di una determinata trama.</span><span class="sxs-lookup"><span data-stu-id="a3fb3-104">Uses a user-provided function to fill each texel of each mip level of a given texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3fb3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3fb3-105">Syntax</span></span>


```C++
HRESULT D3DXFillTexture(
  _Out_ LPDIRECT3DTEXTURE9 pTexture,
  _In_  LPD3DXFILL2D       pFunction,
  _In_  LPVOID             pData
);
```



## <a name="parameters"></a><span data-ttu-id="a3fb3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3fb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3fb3-107">*pTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a3fb3-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3fb3-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="a3fb3-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="a3fb3-109">Puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta la trama compilata.</span><span class="sxs-lookup"><span data-stu-id="a3fb3-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="a3fb3-110">*pFunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3fb3-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3fb3-111">Tipo: **[LPD3DXFILL2D](lpd3dxfill2d.md)**</span><span class="sxs-lookup"><span data-stu-id="a3fb3-111">Type: **[LPD3DXFILL2D](lpd3dxfill2d.md)**</span></span>

<span data-ttu-id="a3fb3-112">Puntatore a una funzione dell'analizzatore fornita dall'utente, che verrà usata per calcolare il valore di ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="a3fb3-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="a3fb3-113">La funzione segue il prototipo di [LPD3DXFILL2D](lpd3dxfill2d.md).</span><span class="sxs-lookup"><span data-stu-id="a3fb3-113">The function follows the prototype of [LPD3DXFILL2D](lpd3dxfill2d.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3fb3-114">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3fb3-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3fb3-115">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3fb3-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3fb3-116">Puntatore a un blocco arbitrario di dati definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a3fb3-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="a3fb3-117">Questo puntatore verrà passato alla funzione fornita in *pFunction*.</span><span class="sxs-lookup"><span data-stu-id="a3fb3-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3fb3-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3fb3-118">Return value</span></span>

<span data-ttu-id="a3fb3-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a3fb3-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a3fb3-120">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a3fb3-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a3fb3-121">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a3fb3-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3fb3-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3fb3-122">Remarks</span></span>

<span data-ttu-id="a3fb3-123">Di seguito è riportato un esempio in cui viene creata una funzione denominata ColorFill, che si basa su D3DXFillTexture.</span><span class="sxs-lookup"><span data-stu-id="a3fb3-123">Here is an example that creates a function called ColorFill, which relies on D3DXFillTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorFill (D3DXVECTOR4* pOut, const D3DXVECTOR2* pTexCoord, 
const D3DXVECTOR2* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, 0.0f, 0.0f);
}
    
    
// Fill the texture using D3DXFillTexture
if (FAILED (hr = D3DXFillTexture (m_pTexture, ColorFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="a3fb3-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3fb3-124">Requirements</span></span>



| <span data-ttu-id="a3fb3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3fb3-125">Requirement</span></span> | <span data-ttu-id="a3fb3-126">Valore</span><span class="sxs-lookup"><span data-stu-id="a3fb3-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3fb3-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3fb3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a3fb3-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3fb3-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a3fb3-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="a3fb3-129">Library</span></span><br/> | <dl> <span data-ttu-id="a3fb3-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3fb3-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a3fb3-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3fb3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3fb3-132">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="a3fb3-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
