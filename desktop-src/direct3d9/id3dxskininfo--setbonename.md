---
description: Imposta il nome dell'osso.
ms.assetid: 2eecddb8-4efa-41a3-be83-7404047a9857
title: 'Metodo ID3DXSkinInfo:: sebonename (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c9190c12eac21963d116f60d5a7aa09f97db796
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234931"
---
# <a name="id3dxskininfosetbonename-method"></a><span data-ttu-id="3ef18-103">Metodo ID3DXSkinInfo:: sebonename</span><span class="sxs-lookup"><span data-stu-id="3ef18-103">ID3DXSkinInfo::SetBoneName method</span></span>

<span data-ttu-id="3ef18-104">Imposta il nome dell'osso.</span><span class="sxs-lookup"><span data-stu-id="3ef18-104">Sets the bone name.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ef18-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ef18-105">Syntax</span></span>


```C++
HRESULT SetBoneName(
  [in] DWORD  Bone,
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="3ef18-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ef18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ef18-107">*Osso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ef18-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ef18-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ef18-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ef18-109">Numero osso</span><span class="sxs-lookup"><span data-stu-id="3ef18-109">Bone number</span></span>

</dd> <dt>

<span data-ttu-id="3ef18-110">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ef18-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ef18-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ef18-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ef18-112">Nome dell'osso</span><span class="sxs-lookup"><span data-stu-id="3ef18-112">Bone name</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ef18-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ef18-113">Return value</span></span>

<span data-ttu-id="3ef18-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3ef18-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3ef18-115">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3ef18-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3ef18-116">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3ef18-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ef18-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ef18-117">Remarks</span></span>

<span data-ttu-id="3ef18-118">I nomi di osso vengono restituiti da [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span><span class="sxs-lookup"><span data-stu-id="3ef18-118">Bone names are returned by [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ef18-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ef18-119">Requirements</span></span>



| <span data-ttu-id="3ef18-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ef18-120">Requirement</span></span> | <span data-ttu-id="3ef18-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3ef18-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef18-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ef18-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3ef18-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ef18-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3ef18-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="3ef18-124">Library</span></span><br/> | <dl> <span data-ttu-id="3ef18-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ef18-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3ef18-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ef18-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef18-127">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="3ef18-127">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="3ef18-128">**ID3DXSkinInfo:: getbonename**</span><span class="sxs-lookup"><span data-stu-id="3ef18-128">**ID3DXSkinInfo::GetBoneName**</span></span>](id3dxskininfo--getbonename.md)
</dt> </dl>

 

 
