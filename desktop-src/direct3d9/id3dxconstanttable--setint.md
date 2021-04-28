---
description: 'Metodo ID3DXConstantTable::SetInt : imposta un valore intero.'
ms.assetid: b57d30b5-c2b5-469e-a267-24e6e712d645
title: Metodo ID3DXConstantTable::SetInt (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetInt
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f218a0cd1a0e1858f24ec8cbccb4848c37121086
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115129"
---
# <a name="id3dxconstanttablesetint-method"></a><span data-ttu-id="d120b-103">Metodo ID3DXConstantTable::SetInt</span><span class="sxs-lookup"><span data-stu-id="d120b-103">ID3DXConstantTable::SetInt method</span></span>

<span data-ttu-id="d120b-104">Imposta un valore intero.</span><span class="sxs-lookup"><span data-stu-id="d120b-104">Sets an integer value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d120b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d120b-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] INT               n
);
```



## <a name="parameters"></a><span data-ttu-id="d120b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d120b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d120b-107">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d120b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d120b-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d120b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d120b-109">Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo associato alla tabella costante.</span><span class="sxs-lookup"><span data-stu-id="d120b-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="d120b-110">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d120b-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d120b-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d120b-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d120b-112">Identificatore univoco della costante.</span><span class="sxs-lookup"><span data-stu-id="d120b-112">Unique identifier to the constant.</span></span> <span data-ttu-id="d120b-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d120b-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d120b-114">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d120b-114">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d120b-115">Tipo: **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d120b-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d120b-116">Integer.</span><span class="sxs-lookup"><span data-stu-id="d120b-116">Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d120b-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d120b-117">Return value</span></span>

<span data-ttu-id="d120b-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d120b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d120b-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d120b-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d120b-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d120b-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d120b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d120b-121">Requirements</span></span>



| <span data-ttu-id="d120b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d120b-122">Requirement</span></span> | <span data-ttu-id="d120b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d120b-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d120b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d120b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d120b-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="d120b-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d120b-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="d120b-126">Library</span></span><br/> | <dl> <span data-ttu-id="d120b-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d120b-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d120b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d120b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d120b-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="d120b-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
