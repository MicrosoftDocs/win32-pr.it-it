---
description: Ottiene il dispositivo che ha creato la mesh.
ms.assetid: b03dadda-ca54-4a55-a0a5-cf5ccdb55a72
title: 'Metodo ID3DXPatchMesh:: GetDevice (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a026398b719bf3ba9a9c02082105cbc7dd299013
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969490"
---
# <a name="id3dxpatchmeshgetdevice-method"></a><span data-ttu-id="d6170-103">Metodo ID3DXPatchMesh:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="d6170-103">ID3DXPatchMesh::GetDevice method</span></span>

<span data-ttu-id="d6170-104">Ottiene il dispositivo che ha creato la mesh.</span><span class="sxs-lookup"><span data-stu-id="d6170-104">Gets the device that created the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6170-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6170-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="d6170-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6170-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6170-107">*ppDevice* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d6170-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6170-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="d6170-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="d6170-109">Puntatore al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6170-109">Pointer to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6170-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d6170-110">Return value</span></span>

<span data-ttu-id="d6170-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d6170-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d6170-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d6170-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d6170-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="d6170-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6170-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6170-114">Requirements</span></span>



| <span data-ttu-id="d6170-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6170-115">Requirement</span></span> | <span data-ttu-id="d6170-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d6170-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6170-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d6170-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d6170-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6170-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d6170-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="d6170-119">Library</span></span><br/> | <dl> <span data-ttu-id="d6170-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6170-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d6170-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6170-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6170-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="d6170-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
