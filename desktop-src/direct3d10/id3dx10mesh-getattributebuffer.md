---
description: Accedere al buffer dell'attributo della mesh.
ms.assetid: 01ebb592-1e0d-4d93-b3f5-ad5f1e0225d0
title: 'Metodo ID3DX10Mesh:: GetAttributeBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 161711cd28dae790fd25ff8dd192945a366e9dd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323152"
---
# <a name="id3dx10meshgetattributebuffer-method"></a><span data-ttu-id="eeac4-103">Metodo ID3DX10Mesh:: GetAttributeBuffer</span><span class="sxs-lookup"><span data-stu-id="eeac4-103">ID3DX10Mesh::GetAttributeBuffer method</span></span>

<span data-ttu-id="eeac4-104">Accedere al buffer dell'attributo della mesh.</span><span class="sxs-lookup"><span data-stu-id="eeac4-104">Access the mesh's attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeac4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eeac4-105">Syntax</span></span>


```C++
HRESULT GetAttributeBuffer(
  [out] ID3DX10MeshBuffer **ppAttributeBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="eeac4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eeac4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeac4-107">*ppAttributeBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="eeac4-107">*ppAttributeBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eeac4-108">Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="eeac4-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="eeac4-109">Buffer dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="eeac4-109">The attribute buffer.</span></span> <span data-ttu-id="eeac4-110">Vedere [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="eeac4-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeac4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eeac4-111">Return value</span></span>

<span data-ttu-id="eeac4-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eeac4-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eeac4-113">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="eeac4-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eeac4-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eeac4-114">Requirements</span></span>



| <span data-ttu-id="eeac4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeac4-115">Requirement</span></span> | <span data-ttu-id="eeac4-116">Valore</span><span class="sxs-lookup"><span data-stu-id="eeac4-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eeac4-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eeac4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="eeac4-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeac4-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="eeac4-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="eeac4-119">Library</span></span><br/> | <dl> <span data-ttu-id="eeac4-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eeac4-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeac4-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eeac4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeac4-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="eeac4-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="eeac4-123">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="eeac4-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




