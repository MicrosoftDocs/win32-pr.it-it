---
description: Imposta un valore integer.
ms.assetid: b57d30b5-c2b5-469e-a267-24e6e712d645
title: 'Metodo ID3DXConstantTable:: setInt (D3DX9Shader. h)'
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
ms.openlocfilehash: a0aa0a213f9f4704a5d557db66aaf360f8baa727
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322814"
---
# <a name="id3dxconstanttablesetint-method"></a><span data-ttu-id="a8ec2-103">Metodo ID3DXConstantTable:: setInt</span><span class="sxs-lookup"><span data-stu-id="a8ec2-103">ID3DXConstantTable::SetInt method</span></span>

<span data-ttu-id="a8ec2-104">Imposta un valore integer.</span><span class="sxs-lookup"><span data-stu-id="a8ec2-104">Sets an integer value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8ec2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8ec2-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] INT               n
);
```



## <a name="parameters"></a><span data-ttu-id="a8ec2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8ec2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8ec2-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8ec2-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8ec2-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a8ec2-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a8ec2-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="a8ec2-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="a8ec2-110">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8ec2-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8ec2-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a8ec2-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a8ec2-112">Identificatore univoco della costante.</span><span class="sxs-lookup"><span data-stu-id="a8ec2-112">Unique identifier to the constant.</span></span> <span data-ttu-id="a8ec2-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a8ec2-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8ec2-114">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8ec2-114">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8ec2-115">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8ec2-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8ec2-116">Integer.</span><span class="sxs-lookup"><span data-stu-id="a8ec2-116">Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8ec2-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8ec2-117">Return value</span></span>

<span data-ttu-id="a8ec2-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8ec2-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8ec2-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a8ec2-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a8ec2-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a8ec2-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8ec2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8ec2-121">Requirements</span></span>



| <span data-ttu-id="a8ec2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8ec2-122">Requirement</span></span> | <span data-ttu-id="a8ec2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a8ec2-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ec2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8ec2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a8ec2-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8ec2-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a8ec2-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="a8ec2-126">Library</span></span><br/> | <dl> <span data-ttu-id="a8ec2-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8ec2-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a8ec2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8ec2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8ec2-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="a8ec2-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
