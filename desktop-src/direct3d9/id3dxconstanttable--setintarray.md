---
description: Imposta una matrice di numeri interi.
ms.assetid: 15add9df-966d-45aa-b29c-d4bed2a125f4
title: 'Metodo ID3DXConstantTable:: SetIntArray (D3DX9Shader. h)'
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
ms.openlocfilehash: 9f89de7d784ce355570d369606bfa67ddd6f5acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322811"
---
# <a name="id3dxconstanttablesetintarray-method"></a><span data-ttu-id="54502-103">Metodo ID3DXConstantTable:: SetIntArray</span><span class="sxs-lookup"><span data-stu-id="54502-103">ID3DXConstantTable::SetIntArray method</span></span>

<span data-ttu-id="54502-104">Imposta una matrice di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="54502-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="54502-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54502-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const INT               *pn,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="54502-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="54502-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54502-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54502-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54502-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="54502-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="54502-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="54502-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="54502-110">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54502-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54502-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="54502-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="54502-112">Identificatore univoco della matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="54502-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="54502-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="54502-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="54502-114">*PN* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54502-114">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54502-115">Tipo: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="54502-115">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="54502-116">Matrice di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="54502-116">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="54502-117">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="54502-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54502-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54502-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54502-119">Numero di numeri interi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="54502-119">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54502-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54502-120">Return value</span></span>

<span data-ttu-id="54502-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54502-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54502-122">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54502-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="54502-123">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="54502-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="54502-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54502-124">Requirements</span></span>



| <span data-ttu-id="54502-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="54502-125">Requirement</span></span> | <span data-ttu-id="54502-126">Valore</span><span class="sxs-lookup"><span data-stu-id="54502-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="54502-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54502-127">Header</span></span><br/>  | <dl> <span data-ttu-id="54502-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="54502-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="54502-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="54502-129">Library</span></span><br/> | <dl> <span data-ttu-id="54502-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54502-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="54502-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54502-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54502-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="54502-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
