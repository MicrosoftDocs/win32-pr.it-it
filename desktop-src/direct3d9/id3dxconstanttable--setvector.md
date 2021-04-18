---
description: Imposta un vettore 4D.
ms.assetid: d5849a8b-b372-4ad0-8773-8c9c4bac3799
title: 'Metodo ID3DXConstantTable:: sevector (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ace1e7b12b67173eb5b9d9a5fc5e56a8b360f2b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322798"
---
# <a name="id3dxconstanttablesetvector-method"></a><span data-ttu-id="29282-103">Metodo ID3DXConstantTable:: sevector</span><span class="sxs-lookup"><span data-stu-id="29282-103">ID3DXConstantTable::SetVector method</span></span>

<span data-ttu-id="29282-104">Imposta un vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="29282-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="29282-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29282-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="29282-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="29282-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29282-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29282-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29282-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="29282-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="29282-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="29282-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="29282-110">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29282-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29282-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="29282-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="29282-112">Identificatore univoco della costante Vector.</span><span class="sxs-lookup"><span data-stu-id="29282-112">Unique identifier to the vector constant.</span></span> <span data-ttu-id="29282-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="29282-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="29282-114">*pVector* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29282-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29282-115">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="29282-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="29282-116">Puntatore a un vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="29282-116">Pointer to a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29282-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29282-117">Return value</span></span>

<span data-ttu-id="29282-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="29282-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="29282-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="29282-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="29282-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="29282-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="29282-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29282-121">Requirements</span></span>



| <span data-ttu-id="29282-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="29282-122">Requirement</span></span> | <span data-ttu-id="29282-123">Valore</span><span class="sxs-lookup"><span data-stu-id="29282-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="29282-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29282-124">Header</span></span><br/>  | <dl> <span data-ttu-id="29282-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="29282-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="29282-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="29282-126">Library</span></span><br/> | <dl> <span data-ttu-id="29282-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29282-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="29282-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29282-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29282-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="29282-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
