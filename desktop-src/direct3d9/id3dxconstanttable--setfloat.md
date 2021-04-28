---
description: 'Metodo ID3DXConstantTable::SetFloat: imposta un numero a virgola mobile.'
ms.assetid: 920cbcf2-ccb9-4533-abbc-6bab8b159ebe
title: Metodo ID3DXConstantTable::SetFloat (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6589d56e0b9dcf8debe14a7c81f86a4972a73405
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115219"
---
# <a name="id3dxconstanttablesetfloat-method"></a><span data-ttu-id="bb67c-103">Metodo ID3DXConstantTable::SetFloat</span><span class="sxs-lookup"><span data-stu-id="bb67c-103">ID3DXConstantTable::SetFloat method</span></span>

<span data-ttu-id="bb67c-104">Imposta un numero a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="bb67c-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb67c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb67c-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] FLOAT             f
);
```



## <a name="parameters"></a><span data-ttu-id="bb67c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb67c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb67c-107">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="bb67c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb67c-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="bb67c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="bb67c-109">Puntatore a [**un'interfaccia IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo associato alla tabella costante.</span><span class="sxs-lookup"><span data-stu-id="bb67c-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="bb67c-110">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="bb67c-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb67c-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="bb67c-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="bb67c-112">Identificatore univoco della costante.</span><span class="sxs-lookup"><span data-stu-id="bb67c-112">Unique identifier to the constant.</span></span> <span data-ttu-id="bb67c-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="bb67c-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb67c-114">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb67c-114">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb67c-115">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb67c-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb67c-116">Numero a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="bb67c-116">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb67c-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb67c-117">Return value</span></span>

<span data-ttu-id="bb67c-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb67c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb67c-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bb67c-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bb67c-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bb67c-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb67c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb67c-121">Requirements</span></span>



| <span data-ttu-id="bb67c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb67c-122">Requirement</span></span> | <span data-ttu-id="bb67c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bb67c-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb67c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb67c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bb67c-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="bb67c-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="bb67c-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="bb67c-126">Library</span></span><br/> | <dl> <span data-ttu-id="bb67c-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb67c-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bb67c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb67c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb67c-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="bb67c-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
