---
description: Restituisce una mesh con modifiche derivanti dal campionamento spaziale adattivo. La mesh restituita contiene solo posizioni, normali e coordinate di trama (se definito).
ms.assetid: 21447733-b27b-4906-8c0e-7089dec71b5b
title: 'Metodo ID3DXPRTEngine:: GetAdaptedMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetAdaptedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d012344a5dfbc1bc17780cb4ab9a53820fe34f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355694"
---
# <a name="id3dxprtenginegetadaptedmesh-method"></a><span data-ttu-id="317e8-104">Metodo ID3DXPRTEngine:: GetAdaptedMesh</span><span class="sxs-lookup"><span data-stu-id="317e8-104">ID3DXPRTEngine::GetAdaptedMesh method</span></span>

<span data-ttu-id="317e8-105">Restituisce una mesh con modifiche derivanti dal campionamento spaziale adattivo.</span><span class="sxs-lookup"><span data-stu-id="317e8-105">Returns a mesh with modifications resulting from adaptive spatial sampling.</span></span> <span data-ttu-id="317e8-106">La mesh restituita contiene solo posizioni, normali e coordinate di trama (se definito).</span><span class="sxs-lookup"><span data-stu-id="317e8-106">The returned mesh contains only positions, normals, and texture coordinates (if defined).</span></span>

## <a name="syntax"></a><span data-ttu-id="317e8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="317e8-107">Syntax</span></span>


```C++
HRESULT GetAdaptedMesh(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in, out] UINT              *pFaceRemap,
  [in, out] UINT              *pVertRemap,
  [in, out] FLOAT             *pfVertWeights,
  [out]     LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="317e8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="317e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="317e8-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="317e8-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="317e8-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="317e8-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="317e8-111">Puntatore a un dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) usato per creare la mesh di output.</span><span class="sxs-lookup"><span data-stu-id="317e8-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device that is used to create the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="317e8-112">*pFaceRemap* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="317e8-112">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="317e8-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="317e8-113">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="317e8-114">Puntatore al quadrante mesh originale diviso per generare la faccia corrente.</span><span class="sxs-lookup"><span data-stu-id="317e8-114">Pointer to the original mesh face that was split to generate the current face.</span></span>

</dd> <dt>

<span data-ttu-id="317e8-115">*pVertRemap* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="317e8-115">*pVertRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="317e8-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="317e8-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="317e8-117">Puntatore a una matrice di destinazione contenente i tre vertici mesh originali che sono gli elementi padre del vertice corrente.</span><span class="sxs-lookup"><span data-stu-id="317e8-117">Pointer to a destination array containing the three original mesh vertices that are the parents of the current vertex.</span></span>

</dd> <dt>

<span data-ttu-id="317e8-118">*pfVertWeights* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="317e8-118">*pfVertWeights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="317e8-119">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="317e8-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="317e8-120">Puntatore a una matrice di destinazione contenente i fattori di fusione per i vertici pVertRemap.</span><span class="sxs-lookup"><span data-stu-id="317e8-120">Pointer to a destination array containing blending factors for the pVertRemap vertices.</span></span>

</dd> <dt>

<span data-ttu-id="317e8-121">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="317e8-121">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="317e8-122">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="317e8-122">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="317e8-123">Puntatore all'oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di output.</span><span class="sxs-lookup"><span data-stu-id="317e8-123">Pointer to the output [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="317e8-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="317e8-124">Return value</span></span>

<span data-ttu-id="317e8-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="317e8-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="317e8-126">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="317e8-126">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="317e8-127">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="317e8-127">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="317e8-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="317e8-128">Remarks</span></span>

<span data-ttu-id="317e8-129">pVertRemap e pfVertWeights possono essere usati per interpolare qualsiasi valore per vertice sulla rete.</span><span class="sxs-lookup"><span data-stu-id="317e8-129">pVertRemap and pfVertWeights can be used to interpolate any per-vertex value over the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="317e8-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="317e8-130">Requirements</span></span>



| <span data-ttu-id="317e8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="317e8-131">Requirement</span></span> | <span data-ttu-id="317e8-132">Valore</span><span class="sxs-lookup"><span data-stu-id="317e8-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="317e8-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="317e8-133">Header</span></span><br/>  | <dl> <span data-ttu-id="317e8-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="317e8-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="317e8-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="317e8-135">Library</span></span><br/> | <dl> <span data-ttu-id="317e8-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="317e8-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="317e8-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="317e8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="317e8-138">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="317e8-138">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
