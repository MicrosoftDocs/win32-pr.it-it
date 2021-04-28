---
description: 'Metodo ID3DXConstantTable::SetIntArray: imposta una matrice di numeri interi.'
ms.assetid: 15add9df-966d-45aa-b29c-d4bed2a125f4
title: Metodo ID3DXConstantTable::SetIntArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f674bc730398c386856314a7e7305f33f3e7fa1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115109"
---
# <a name="id3dxconstanttablesetintarray-method"></a><span data-ttu-id="959d8-103">Metodo ID3DXConstantTable::SetIntArray</span><span class="sxs-lookup"><span data-stu-id="959d8-103">ID3DXConstantTable::SetIntArray method</span></span>

<span data-ttu-id="959d8-104">Imposta una matrice di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="959d8-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="959d8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="959d8-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const INT               *pn,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="959d8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="959d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="959d8-107">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="959d8-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="959d8-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="959d8-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="959d8-109">Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo associato alla tabella costante.</span><span class="sxs-lookup"><span data-stu-id="959d8-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="959d8-110">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="959d8-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="959d8-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="959d8-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="959d8-112">Identificatore univoco della matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="959d8-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="959d8-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="959d8-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="959d8-114">*pn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="959d8-114">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="959d8-115">Tipo: **const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="959d8-115">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="959d8-116">Matrice di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="959d8-116">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="959d8-117">*Conteggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="959d8-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="959d8-118">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="959d8-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="959d8-119">Numero di numeri interi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="959d8-119">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="959d8-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="959d8-120">Return value</span></span>

<span data-ttu-id="959d8-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="959d8-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="959d8-122">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="959d8-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="959d8-123">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="959d8-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="959d8-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="959d8-124">Requirements</span></span>



| <span data-ttu-id="959d8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="959d8-125">Requirement</span></span> | <span data-ttu-id="959d8-126">Valore</span><span class="sxs-lookup"><span data-stu-id="959d8-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="959d8-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="959d8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="959d8-128"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="959d8-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="959d8-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="959d8-129">Library</span></span><br/> | <dl> <span data-ttu-id="959d8-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="959d8-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="959d8-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="959d8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="959d8-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="959d8-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
