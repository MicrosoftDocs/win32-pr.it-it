---
description: Imposta una matrice di numeri a virgola mobile.
ms.assetid: 7a622dd5-47ed-4166-a6df-f484b03e0b5a
title: 'Metodo ID3DXConstantTable:: SetFloatArray (D3DX9Shader. h)'
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
ms.openlocfilehash: d75d4171ab51859e4095acbe5d3e86d704b1f437
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235053"
---
# <a name="id3dxconstanttablesetfloatarray-method"></a><span data-ttu-id="b1033-103">Metodo ID3DXConstantTable:: SetFloatArray</span><span class="sxs-lookup"><span data-stu-id="b1033-103">ID3DXConstantTable::SetFloatArray method</span></span>

<span data-ttu-id="b1033-104">Imposta una matrice di numeri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="b1033-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1033-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1033-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const FLOAT             *pf,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="b1033-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1033-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1033-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1033-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1033-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b1033-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b1033-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="b1033-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="b1033-110">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1033-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1033-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b1033-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b1033-112">Identificatore univoco della matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="b1033-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="b1033-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b1033-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1033-114">*PF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1033-114">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1033-115">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b1033-115">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b1033-116">Matrice di numeri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="b1033-116">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="b1033-117">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b1033-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1033-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1033-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1033-119">Numero di valori a virgola mobile nella matrice.</span><span class="sxs-lookup"><span data-stu-id="b1033-119">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1033-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1033-120">Return value</span></span>

<span data-ttu-id="b1033-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1033-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1033-122">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b1033-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b1033-123">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b1033-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1033-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1033-124">Requirements</span></span>



| <span data-ttu-id="b1033-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1033-125">Requirement</span></span> | <span data-ttu-id="b1033-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b1033-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1033-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1033-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b1033-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1033-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b1033-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="b1033-129">Library</span></span><br/> | <dl> <span data-ttu-id="b1033-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1033-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b1033-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1033-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1033-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="b1033-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
