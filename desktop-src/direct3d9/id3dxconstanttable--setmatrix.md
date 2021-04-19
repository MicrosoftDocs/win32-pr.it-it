---
description: Imposta una matrice nontransposed.
ms.assetid: 30369e34-6e9d-4480-a142-e38f46fd38b0
title: 'Metodo ID3DXConstantTable:: sematrix (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ae227663a61087fae309d1954b8f0dc438f6df2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322810"
---
# <a name="id3dxconstanttablesetmatrix-method"></a><span data-ttu-id="a9f2a-103">Metodo ID3DXConstantTable:: sematrix</span><span class="sxs-lookup"><span data-stu-id="a9f2a-103">ID3DXConstantTable::SetMatrix method</span></span>

<span data-ttu-id="a9f2a-104">Imposta una matrice nontransposed.</span><span class="sxs-lookup"><span data-stu-id="a9f2a-104">Sets a nontransposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9f2a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9f2a-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="a9f2a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9f2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9f2a-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9f2a-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f2a-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a9f2a-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a9f2a-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="a9f2a-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="a9f2a-110">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9f2a-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f2a-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a9f2a-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a9f2a-112">Identificatore univoco della matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="a9f2a-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="a9f2a-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a9f2a-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9f2a-114">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9f2a-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f2a-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a9f2a-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a9f2a-116">Puntatore a una matrice nontransposed.</span><span class="sxs-lookup"><span data-stu-id="a9f2a-116">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="a9f2a-117">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="a9f2a-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9f2a-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9f2a-118">Return value</span></span>

<span data-ttu-id="a9f2a-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a9f2a-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a9f2a-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a9f2a-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a9f2a-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a9f2a-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9f2a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9f2a-122">Requirements</span></span>



| <span data-ttu-id="a9f2a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9f2a-123">Requirement</span></span> | <span data-ttu-id="a9f2a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a9f2a-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f2a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9f2a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a9f2a-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9f2a-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a9f2a-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="a9f2a-127">Library</span></span><br/> | <dl> <span data-ttu-id="a9f2a-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9f2a-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a9f2a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9f2a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9f2a-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="a9f2a-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
