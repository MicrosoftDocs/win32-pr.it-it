---
description: 'Metodo ID3DXConstantTable::SetFloatArray: imposta una matrice di numeri a virgola mobile.'
ms.assetid: 7a622dd5-47ed-4166-a6df-f484b03e0b5a
title: Metodo ID3DXConstantTable::SetFloatArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 23c96cb2bfc8113fd167c8b57a21a46285b691a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115169"
---
# <a name="id3dxconstanttablesetfloatarray-method"></a><span data-ttu-id="b4de3-103">Metodo ID3DXConstantTable::SetFloatArray</span><span class="sxs-lookup"><span data-stu-id="b4de3-103">ID3DXConstantTable::SetFloatArray method</span></span>

<span data-ttu-id="b4de3-104">Imposta una matrice di numeri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="b4de3-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4de3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4de3-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const FLOAT             *pf,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="b4de3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4de3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4de3-107">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b4de3-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4de3-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b4de3-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b4de3-109">Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo associato alla tabella costante.</span><span class="sxs-lookup"><span data-stu-id="b4de3-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="b4de3-110">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b4de3-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4de3-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b4de3-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b4de3-112">Identificatore univoco della matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="b4de3-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="b4de3-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b4de3-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4de3-114">*pf* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b4de3-114">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4de3-115">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b4de3-115">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b4de3-116">Matrice di numeri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="b4de3-116">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="b4de3-117">*Conteggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b4de3-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4de3-118">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4de3-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4de3-119">Numero di valori a virgola mobile nella matrice.</span><span class="sxs-lookup"><span data-stu-id="b4de3-119">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4de3-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4de3-120">Return value</span></span>

<span data-ttu-id="b4de3-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b4de3-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b4de3-122">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b4de3-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b4de3-123">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b4de3-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4de3-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4de3-124">Requirements</span></span>



| <span data-ttu-id="b4de3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4de3-125">Requirement</span></span> | <span data-ttu-id="b4de3-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b4de3-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4de3-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4de3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b4de3-128"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="b4de3-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b4de3-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="b4de3-129">Library</span></span><br/> | <dl> <span data-ttu-id="b4de3-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4de3-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b4de3-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4de3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4de3-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="b4de3-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
