---
description: Imposta il contenuto del buffer sulla tabella delle costanti.
ms.assetid: 6058795c-fa32-42aa-9a36-af0b7f6eed1d
title: 'Metodo ID3DXConstantTable:: SetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5e02c43e0d0ad84615650bc0b1c0d5fd5654e38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322799"
---
# <a name="id3dxconstanttablesetvalue-method"></a><span data-ttu-id="0f88c-103">Metodo ID3DXConstantTable:: SetValue</span><span class="sxs-lookup"><span data-stu-id="0f88c-103">ID3DXConstantTable::SetValue method</span></span>

<span data-ttu-id="0f88c-104">Imposta il contenuto del buffer sulla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="0f88c-104">Sets the contents of the buffer to the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f88c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f88c-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] LPCVOID           pData,
  [in] UINT              Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="0f88c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f88c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f88c-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f88c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f88c-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0f88c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0f88c-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="0f88c-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="0f88c-110">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f88c-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f88c-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0f88c-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0f88c-112">Identificatore univoco di una costante.</span><span class="sxs-lookup"><span data-stu-id="0f88c-112">Unique identifier to a constant.</span></span> <span data-ttu-id="0f88c-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0f88c-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f88c-114">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f88c-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f88c-115">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f88c-115">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0f88c-116">Buffer contenente i dati.</span><span class="sxs-lookup"><span data-stu-id="0f88c-116">Buffer containing data.</span></span>

</dd> <dt>

<span data-ttu-id="0f88c-117">*Byte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f88c-117">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f88c-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f88c-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0f88c-119">Dimensioni del buffer, in byte.</span><span class="sxs-lookup"><span data-stu-id="0f88c-119">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f88c-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f88c-120">Return value</span></span>

<span data-ttu-id="0f88c-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0f88c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0f88c-122">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0f88c-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0f88c-123">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0f88c-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f88c-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f88c-124">Requirements</span></span>



| <span data-ttu-id="0f88c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f88c-125">Requirement</span></span> | <span data-ttu-id="0f88c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0f88c-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f88c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f88c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0f88c-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f88c-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0f88c-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="0f88c-129">Library</span></span><br/> | <dl> <span data-ttu-id="0f88c-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f88c-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0f88c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f88c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f88c-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="0f88c-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
