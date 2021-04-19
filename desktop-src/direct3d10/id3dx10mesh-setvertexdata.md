---
description: Impostare i dati dei vertici in uno dei buffer dei vertici della mesh.
ms.assetid: 930cbc49-4202-431f-ac72-386c31acd87e
title: 'Metodo ID3DX10Mesh:: SetVertexData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetVertexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 68d54c6868e44517d42e0b53159f7a23ef45a05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323135"
---
# <a name="id3dx10meshsetvertexdata-method"></a><span data-ttu-id="0d095-103">Metodo ID3DX10Mesh:: SetVertexData</span><span class="sxs-lookup"><span data-stu-id="0d095-103">ID3DX10Mesh::SetVertexData method</span></span>

<span data-ttu-id="0d095-104">Impostare i dati dei vertici in uno dei buffer dei vertici della mesh.</span><span class="sxs-lookup"><span data-stu-id="0d095-104">Set vertex data into one of the mesh's vertex buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d095-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d095-105">Syntax</span></span>


```C++
HRESULT SetVertexData(
  [in]       UINT iBuffer,
  [in] const void *pData
);
```



## <a name="parameters"></a><span data-ttu-id="0d095-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d095-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d095-107">*IBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d095-107">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d095-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d095-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d095-109">Buffer dei vertici da riempire con pData.</span><span class="sxs-lookup"><span data-stu-id="0d095-109">The vertex buffer to be filled with pData.</span></span>

</dd> <dt>

<span data-ttu-id="0d095-110">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d095-110">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d095-111">Tipo: **const \* void**</span><span class="sxs-lookup"><span data-stu-id="0d095-111">Type: **const void\***</span></span>

<span data-ttu-id="0d095-112">Dati dei vertici da impostare.</span><span class="sxs-lookup"><span data-stu-id="0d095-112">The vertex data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d095-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d095-113">Return value</span></span>

<span data-ttu-id="0d095-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0d095-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0d095-115">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0d095-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d095-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d095-116">Requirements</span></span>



| <span data-ttu-id="0d095-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d095-117">Requirement</span></span> | <span data-ttu-id="0d095-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0d095-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d095-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d095-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0d095-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d095-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d095-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="0d095-121">Library</span></span><br/> | <dl> <span data-ttu-id="0d095-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d095-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d095-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d095-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d095-124">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="0d095-124">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="0d095-125">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="0d095-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
