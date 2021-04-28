---
description: 'Metodo ID3DXConstantTable::GetDesc: ottiene una descrizione della tabella costante.'
ms.assetid: 3a7396c6-3a3e-44c2-96b7-60339015b376
title: Metodo ID3DXConstantTable::GetDesc (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81b64f1a01af8909aa820e772214a1f11c6099b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115239"
---
# <a name="id3dxconstanttablegetdesc-method"></a><span data-ttu-id="09c4b-103">Metodo ID3DXConstantTable::GetDesc</span><span class="sxs-lookup"><span data-stu-id="09c4b-103">ID3DXConstantTable::GetDesc method</span></span>

<span data-ttu-id="09c4b-104">Ottiene una descrizione della tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="09c4b-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="09c4b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09c4b-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="09c4b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="09c4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09c4b-107">*pDesc* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="09c4b-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09c4b-108">Tipo: **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="09c4b-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="09c4b-109">Descrizione della tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="09c4b-109">Description of the constant table.</span></span> <span data-ttu-id="09c4b-110">Vedere [**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md).</span><span class="sxs-lookup"><span data-stu-id="09c4b-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09c4b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09c4b-111">Return value</span></span>

<span data-ttu-id="09c4b-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="09c4b-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="09c4b-113">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="09c4b-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="09c4b-114">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="09c4b-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="09c4b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09c4b-115">Requirements</span></span>



| <span data-ttu-id="09c4b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="09c4b-116">Requirement</span></span> | <span data-ttu-id="09c4b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="09c4b-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="09c4b-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09c4b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="09c4b-119"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="09c4b-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="09c4b-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="09c4b-120">Library</span></span><br/> | <dl> <span data-ttu-id="09c4b-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="09c4b-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="09c4b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09c4b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09c4b-123">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="09c4b-123">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> <dt>

[<span data-ttu-id="09c4b-124">**ID3DXConstantTable::GetConstantDesc**</span><span class="sxs-lookup"><span data-stu-id="09c4b-124">**ID3DXConstantTable::GetConstantDesc**</span></span>](id3dxconstanttable--getconstantdesc.md)
</dt> </dl>

 

 




