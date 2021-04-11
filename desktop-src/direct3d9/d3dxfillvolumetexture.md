---
description: Usa una funzione fornita dall'utente per riempire ogni Texel di ogni livello MIP di una determinata trama del volume.
ms.assetid: cc9eb051-8a62-4e35-87df-c255f10e94d8
title: Funzione D3DXFillVolumeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d817470f0f0617001fd83054e24e8881ac9a3a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354859"
---
# <a name="d3dxfillvolumetexture-function"></a><span data-ttu-id="35a69-103">D3DXFillVolumeTexture (funzione)</span><span class="sxs-lookup"><span data-stu-id="35a69-103">D3DXFillVolumeTexture function</span></span>

<span data-ttu-id="35a69-104">Usa una funzione fornita dall'utente per riempire ogni Texel di ogni livello MIP di una determinata trama del volume.</span><span class="sxs-lookup"><span data-stu-id="35a69-104">Uses a user-provided function to fill each texel of each mip level of a given volume texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a69-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35a69-105">Syntax</span></span>


```C++
HRESULT D3DXFillVolumeTexture(
  _Out_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D             pFunction,
  _In_  LPVOID                   pData
);
```



## <a name="parameters"></a><span data-ttu-id="35a69-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35a69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35a69-107">*pTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="35a69-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35a69-108">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="35a69-108">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="35a69-109">Puntatore a un'interfaccia [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , che rappresenta la trama compilata.</span><span class="sxs-lookup"><span data-stu-id="35a69-109">Pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="35a69-110">*pFunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35a69-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a69-111">Tipo: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span><span class="sxs-lookup"><span data-stu-id="35a69-111">Type: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span></span>

<span data-ttu-id="35a69-112">Puntatore a una funzione dell'analizzatore fornita dall'utente, che verrà usata per calcolare il valore di ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="35a69-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="35a69-113">La funzione segue il prototipo di [LPD3DXFILL3D](lpd3dxfill3d.md).</span><span class="sxs-lookup"><span data-stu-id="35a69-113">The function follows the prototype of [LPD3DXFILL3D](lpd3dxfill3d.md).</span></span>

</dd> <dt>

<span data-ttu-id="35a69-114">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35a69-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a69-115">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35a69-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35a69-116">Puntatore a un blocco arbitrario di dati definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="35a69-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="35a69-117">Questo puntatore verrà passato alla funzione fornita in *pFunction*.</span><span class="sxs-lookup"><span data-stu-id="35a69-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35a69-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35a69-118">Return value</span></span>

<span data-ttu-id="35a69-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35a69-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35a69-120">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="35a69-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="35a69-121">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="35a69-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="35a69-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="35a69-122">Remarks</span></span>

<span data-ttu-id="35a69-123">Se il volume non è dinamico (poiché Usage è impostato su 0 quando viene creato) e situato nella memoria video (il pool di memoria impostato su D3DPOOL \_ default), **D3DXFillVolumeTexture** avrà esito negativo perché il volume non può essere bloccato.</span><span class="sxs-lookup"><span data-stu-id="35a69-123">If the volume is non-dynamic (because usage is set to 0 when it is created), and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), **D3DXFillVolumeTexture** will fail because the volume cannot be locked.</span></span>

<span data-ttu-id="35a69-124">Questo esempio crea una funzione denominata ColorVolumeFill, che si basa su D3DXFillVolumeTexture.</span><span class="sxs-lookup"><span data-stu-id="35a69-124">This example creates a function called ColorVolumeFill, which relies on D3DXFillVolumeTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorVolumeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
   *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill volume texture
if (FAILED (hr = D3DXFillVolumeTexture (m_pTexture, ColorVolumeFill, NULL)))
{
       return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="35a69-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35a69-125">Requirements</span></span>



| <span data-ttu-id="35a69-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="35a69-126">Requirement</span></span> | <span data-ttu-id="35a69-127">Valore</span><span class="sxs-lookup"><span data-stu-id="35a69-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35a69-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35a69-128">Header</span></span><br/>  | <dl> <span data-ttu-id="35a69-129"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="35a69-129"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="35a69-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="35a69-130">Library</span></span><br/> | <dl> <span data-ttu-id="35a69-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35a69-131"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="35a69-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35a69-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a69-133">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="35a69-133">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
