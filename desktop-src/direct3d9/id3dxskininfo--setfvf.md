---
description: Imposta il tipo FVF (Flexible Vertex Format).
ms.assetid: e581dcd4-7e17-4c36-aac9-c2942924cf51
title: 'Metodo ID3DXSkinInfo:: SetFVF (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 010385597442ba1546c20122f6551fca0cfcf81c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322051"
---
# <a name="id3dxskininfosetfvf-method"></a><span data-ttu-id="67cc6-103">Metodo ID3DXSkinInfo:: SetFVF</span><span class="sxs-lookup"><span data-stu-id="67cc6-103">ID3DXSkinInfo::SetFVF method</span></span>

<span data-ttu-id="67cc6-104">Imposta il tipo FVF (Flexible Vertex Format).</span><span class="sxs-lookup"><span data-stu-id="67cc6-104">Sets the flexible vertex format (FVF) type.</span></span>

## <a name="syntax"></a><span data-ttu-id="67cc6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67cc6-105">Syntax</span></span>


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="67cc6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="67cc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67cc6-107">*FVF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67cc6-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67cc6-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67cc6-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67cc6-109">Formato vertice flessibile.</span><span class="sxs-lookup"><span data-stu-id="67cc6-109">Flexible vertex format.</span></span> <span data-ttu-id="67cc6-110">Vedere [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="67cc6-110">See [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67cc6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67cc6-111">Return value</span></span>

<span data-ttu-id="67cc6-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="67cc6-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="67cc6-113">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="67cc6-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="67cc6-114">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="67cc6-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="67cc6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67cc6-115">Requirements</span></span>



| <span data-ttu-id="67cc6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="67cc6-116">Requirement</span></span> | <span data-ttu-id="67cc6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="67cc6-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67cc6-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67cc6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="67cc6-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="67cc6-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="67cc6-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="67cc6-120">Library</span></span><br/> | <dl> <span data-ttu-id="67cc6-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67cc6-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="67cc6-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67cc6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67cc6-123">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="67cc6-123">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
