---
description: Imposta una matrice trasposta.
ms.assetid: 1c4d64ce-64bd-47d4-9912-879f4834c0e8
title: 'Metodo ID3DXConstantTable:: SetMatrixTranspose (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTranspose
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa84f9e483be0c6c2ddae37c52ef6df2c43fda90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322803"
---
# <a name="id3dxconstanttablesetmatrixtranspose-method"></a><span data-ttu-id="4adcf-103">Metodo ID3DXConstantTable:: SetMatrixTranspose</span><span class="sxs-lookup"><span data-stu-id="4adcf-103">ID3DXConstantTable::SetMatrixTranspose method</span></span>

<span data-ttu-id="4adcf-104">Imposta una matrice trasposta.</span><span class="sxs-lookup"><span data-stu-id="4adcf-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4adcf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4adcf-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="4adcf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4adcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4adcf-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4adcf-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4adcf-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="4adcf-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="4adcf-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="4adcf-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="4adcf-110">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4adcf-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4adcf-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="4adcf-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="4adcf-112">Identificatore univoco della matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="4adcf-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="4adcf-113">Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4adcf-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="4adcf-114">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4adcf-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4adcf-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4adcf-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4adcf-116">Puntatore a una matrice trasposta.</span><span class="sxs-lookup"><span data-stu-id="4adcf-116">Pointer to a transposed matrix.</span></span> <span data-ttu-id="4adcf-117">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="4adcf-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4adcf-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4adcf-118">Return value</span></span>

<span data-ttu-id="4adcf-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4adcf-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4adcf-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4adcf-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4adcf-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4adcf-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4adcf-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4adcf-122">Requirements</span></span>



| <span data-ttu-id="4adcf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4adcf-123">Requirement</span></span> | <span data-ttu-id="4adcf-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4adcf-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4adcf-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4adcf-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4adcf-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="4adcf-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="4adcf-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="4adcf-127">Library</span></span><br/> | <dl> <span data-ttu-id="4adcf-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4adcf-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4adcf-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4adcf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4adcf-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="4adcf-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
