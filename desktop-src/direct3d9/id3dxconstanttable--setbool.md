---
description: Imposta un valore booleano.
ms.assetid: 652e5b68-88f3-4b05-959b-38bb530c546a
title: 'Metodo ID3DXConstantTable:: SetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetBool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49fb38407aeaaf042d8d606c90e075a1891b9557
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762076"
---
# <a name="id3dxconstanttablesetbool-method"></a><span data-ttu-id="c33c6-103">Metodo ID3DXConstantTable:: SetValue</span><span class="sxs-lookup"><span data-stu-id="c33c6-103">ID3DXConstantTable::SetBool method</span></span>

<span data-ttu-id="c33c6-104">Imposta un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="c33c6-104">Sets a Boolean value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c33c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c33c6-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] BOOL              b
);
```



## <a name="parameters"></a><span data-ttu-id="c33c6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c33c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c33c6-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c33c6-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c33c6-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c33c6-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c33c6-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="c33c6-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="c33c6-110">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c33c6-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c33c6-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c33c6-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c33c6-112">Identificatore univoco della costante.</span><span class="sxs-lookup"><span data-stu-id="c33c6-112">Unique identifier to the constant.</span></span> <span data-ttu-id="c33c6-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c33c6-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c33c6-114">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c33c6-114">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c33c6-115">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c33c6-115">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c33c6-116">.</span><span class="sxs-lookup"><span data-stu-id="c33c6-116">Boolean value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c33c6-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c33c6-117">Return value</span></span>

<span data-ttu-id="c33c6-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c33c6-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c33c6-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c33c6-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c33c6-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c33c6-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c33c6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c33c6-121">Requirements</span></span>



| <span data-ttu-id="c33c6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c33c6-122">Requirement</span></span> | <span data-ttu-id="c33c6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c33c6-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c33c6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c33c6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c33c6-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c33c6-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c33c6-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="c33c6-126">Library</span></span><br/> | <dl> <span data-ttu-id="c33c6-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c33c6-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c33c6-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c33c6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c33c6-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="c33c6-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
