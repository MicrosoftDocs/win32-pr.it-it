---
description: Ottiene il numero massimo di influenze per qualsiasi vertice nella mesh.
ms.assetid: 012168e8-30e5-4571-b793-647ab23df068
title: 'Metodo ID3DXSkinInfo:: GetMaxVertexInfluences (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxVertexInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2acae5cc119df25989e6bf22692ec1609ffa9408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969296"
---
# <a name="id3dxskininfogetmaxvertexinfluences-method"></a><span data-ttu-id="d508e-103">Metodo ID3DXSkinInfo:: GetMaxVertexInfluences</span><span class="sxs-lookup"><span data-stu-id="d508e-103">ID3DXSkinInfo::GetMaxVertexInfluences method</span></span>

<span data-ttu-id="d508e-104">Ottiene il numero massimo di influenze per qualsiasi vertice nella mesh.</span><span class="sxs-lookup"><span data-stu-id="d508e-104">Gets the maximum number of influences for any vertex in the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="d508e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d508e-105">Syntax</span></span>


```C++
HRESULT GetMaxVertexInfluences(
  [in] DWORD *maxVertexInfluences
);
```



## <a name="parameters"></a><span data-ttu-id="d508e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d508e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d508e-107">*maxVertexInfluences* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d508e-107">*maxVertexInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d508e-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d508e-108">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d508e-109">Puntatore all'influenza massima del vertice.</span><span class="sxs-lookup"><span data-stu-id="d508e-109">Pointer to the maximum vertex influence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d508e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d508e-110">Return value</span></span>

<span data-ttu-id="d508e-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d508e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d508e-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d508e-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d508e-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d508e-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d508e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d508e-114">Requirements</span></span>



| <span data-ttu-id="d508e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d508e-115">Requirement</span></span> | <span data-ttu-id="d508e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d508e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d508e-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d508e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d508e-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d508e-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d508e-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="d508e-119">Library</span></span><br/> | <dl> <span data-ttu-id="d508e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d508e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d508e-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d508e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d508e-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="d508e-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
