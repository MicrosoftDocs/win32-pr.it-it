---
description: Imposta una matrice di valori booleani.
ms.assetid: 323ad654-81e3-4986-a667-8333dd44a2d1
title: 'Metodo ID3DXConstantTable:: SetBoolArray (D3DX9Shader. h)'
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
ms.openlocfilehash: d573a2c44b54809ec259a0ceb5abab02ef37df34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322818"
---
# <a name="id3dxconstanttablesetboolarray-method"></a><span data-ttu-id="a49e2-103">Metodo ID3DXConstantTable:: SetBoolArray</span><span class="sxs-lookup"><span data-stu-id="a49e2-103">ID3DXConstantTable::SetBoolArray method</span></span>

<span data-ttu-id="a49e2-104">Imposta una matrice di valori booleani.</span><span class="sxs-lookup"><span data-stu-id="a49e2-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a49e2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a49e2-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const BOOL              *pB,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="a49e2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a49e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a49e2-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a49e2-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a49e2-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a49e2-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a49e2-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="a49e2-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="a49e2-110">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a49e2-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a49e2-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a49e2-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a49e2-112">Identificatore univoco della matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="a49e2-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="a49e2-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a49e2-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a49e2-114">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a49e2-114">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a49e2-115">Tipo: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a49e2-115">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a49e2-116">Matrice di valori booleani.</span><span class="sxs-lookup"><span data-stu-id="a49e2-116">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="a49e2-117">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a49e2-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a49e2-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a49e2-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a49e2-119">Numero di valori booleani nella matrice.</span><span class="sxs-lookup"><span data-stu-id="a49e2-119">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a49e2-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a49e2-120">Return value</span></span>

<span data-ttu-id="a49e2-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a49e2-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a49e2-122">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a49e2-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a49e2-123">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a49e2-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a49e2-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a49e2-124">Requirements</span></span>



| <span data-ttu-id="a49e2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a49e2-125">Requirement</span></span> | <span data-ttu-id="a49e2-126">Valore</span><span class="sxs-lookup"><span data-stu-id="a49e2-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a49e2-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a49e2-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a49e2-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a49e2-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a49e2-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="a49e2-129">Library</span></span><br/> | <dl> <span data-ttu-id="a49e2-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a49e2-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a49e2-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a49e2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a49e2-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="a49e2-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
