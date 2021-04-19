---
description: 'Rimuove i dati mesh dal dispositivo di cui è stato eseguito il commit nel dispositivo (con ID3DX10Mesh:: CommitToDevice).'
ms.assetid: 60eee1f8-f04b-4f33-8f86-0564d0334f97
title: 'ID3DX10Mesh: metodo:D la scheda (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Discard
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f861de8eefff603954e896a1b6684afc8806764f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322753"
---
# <a name="id3dx10meshdiscard-method"></a><span data-ttu-id="6dd5e-103">ID3DX10Mesh::D metodo di scheda</span><span class="sxs-lookup"><span data-stu-id="6dd5e-103">ID3DX10Mesh::Discard method</span></span>

<span data-ttu-id="6dd5e-104">Rimuove i dati mesh dal dispositivo di cui è stato eseguito il commit nel dispositivo (con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md)).</span><span class="sxs-lookup"><span data-stu-id="6dd5e-104">Removes mesh data from the device that has been committed to the device (with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="6dd5e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6dd5e-105">Syntax</span></span>


```C++
HRESULT Discard(
  [in] D3DX10_MESH_DISCARD_FLAGS dwDiscard
);
```



## <a name="parameters"></a><span data-ttu-id="6dd5e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6dd5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dd5e-107">*dwDiscard* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6dd5e-107">*dwDiscard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dd5e-108">Tipo: **[ **d3dx10 \_ mesh \_ scarto \_ flag**](d3dx10-mesh-discard-flags.md)**</span><span class="sxs-lookup"><span data-stu-id="6dd5e-108">Type: **[**D3DX10\_MESH\_DISCARD\_FLAGS**](d3dx10-mesh-discard-flags.md)**</span></span>

<span data-ttu-id="6dd5e-109">Specifica le parti di dati mesh da eliminare dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6dd5e-109">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="6dd5e-110">Vedere [**d3dx10 \_ mesh \_ scarto \_ flag**](d3dx10-mesh-discard-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6dd5e-110">See [**D3DX10\_MESH\_DISCARD\_FLAGS**](d3dx10-mesh-discard-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dd5e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6dd5e-111">Return value</span></span>

<span data-ttu-id="6dd5e-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6dd5e-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6dd5e-113">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6dd5e-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6dd5e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6dd5e-114">Requirements</span></span>



| <span data-ttu-id="6dd5e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dd5e-115">Requirement</span></span> | <span data-ttu-id="6dd5e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6dd5e-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6dd5e-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6dd5e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6dd5e-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6dd5e-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6dd5e-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="6dd5e-119">Library</span></span><br/> | <dl> <span data-ttu-id="6dd5e-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6dd5e-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dd5e-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6dd5e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dd5e-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="6dd5e-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="6dd5e-123">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="6dd5e-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




