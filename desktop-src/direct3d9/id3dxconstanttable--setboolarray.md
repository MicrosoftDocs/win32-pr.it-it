---
description: 'Metodo ID3DXConstantTable::SetBoolArray : imposta una matrice di valori booleani.'
ms.assetid: 323ad654-81e3-4986-a667-8333dd44a2d1
title: Metodo ID3DXConstantTable::SetBoolArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetBoolArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c967ffd1a6601144787621628ed1b019e775eddd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115209"
---
# <a name="id3dxconstanttablesetboolarray-method"></a><span data-ttu-id="673a0-103">Metodo ID3DXConstantTable::SetBoolArray</span><span class="sxs-lookup"><span data-stu-id="673a0-103">ID3DXConstantTable::SetBoolArray method</span></span>

<span data-ttu-id="673a0-104">Imposta una matrice di valori booleani.</span><span class="sxs-lookup"><span data-stu-id="673a0-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="673a0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="673a0-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const BOOL              *pB,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="673a0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="673a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="673a0-107">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="673a0-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="673a0-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="673a0-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="673a0-109">Puntatore a [**un'interfaccia IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo associato alla tabella costante.</span><span class="sxs-lookup"><span data-stu-id="673a0-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="673a0-110">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="673a0-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="673a0-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="673a0-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="673a0-112">Identificatore univoco della matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="673a0-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="673a0-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="673a0-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="673a0-114">*pB* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="673a0-114">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="673a0-115">Tipo: **const [**BOOL**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="673a0-115">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="673a0-116">Matrice di valori booleani.</span><span class="sxs-lookup"><span data-stu-id="673a0-116">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="673a0-117">*Conteggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="673a0-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="673a0-118">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="673a0-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="673a0-119">Numero di valori booleani nella matrice.</span><span class="sxs-lookup"><span data-stu-id="673a0-119">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="673a0-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="673a0-120">Return value</span></span>

<span data-ttu-id="673a0-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="673a0-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="673a0-122">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="673a0-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="673a0-123">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="673a0-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="673a0-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="673a0-124">Requirements</span></span>



| <span data-ttu-id="673a0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="673a0-125">Requirement</span></span> | <span data-ttu-id="673a0-126">Valore</span><span class="sxs-lookup"><span data-stu-id="673a0-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="673a0-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="673a0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="673a0-128"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="673a0-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="673a0-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="673a0-129">Library</span></span><br/> | <dl> <span data-ttu-id="673a0-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="673a0-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="673a0-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="673a0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="673a0-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="673a0-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
