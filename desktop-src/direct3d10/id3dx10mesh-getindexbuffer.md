---
description: Recupera i dati in un buffer di indice.
ms.assetid: 7e25ad67-7f9d-4c23-a029-a2262034ef38
title: 'Metodo ID3DX10Mesh:: GetIndexBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c2777a9d530ac7217b1cc0f3c0f148998cc70ffe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401965"
---
# <a name="id3dx10meshgetindexbuffer-method"></a><span data-ttu-id="4fb00-103">Metodo ID3DX10Mesh:: GetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="4fb00-103">ID3DX10Mesh::GetIndexBuffer method</span></span>

<span data-ttu-id="4fb00-104">Recupera i dati in un buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="4fb00-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb00-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4fb00-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="4fb00-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4fb00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fb00-107">*ppIndexBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4fb00-107">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fb00-108">Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="4fb00-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="4fb00-109">Indirizzo di un puntatore a un'interfaccia ID3DX10MeshBuffer, che rappresenta il buffer di indice associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="4fb00-109">Address of a pointer to a ID3DX10MeshBuffer interface, representing the index buffer associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fb00-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4fb00-110">Return value</span></span>

<span data-ttu-id="4fb00-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4fb00-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4fb00-112">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4fb00-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4fb00-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4fb00-113">Requirements</span></span>



| <span data-ttu-id="4fb00-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fb00-114">Requirement</span></span> | <span data-ttu-id="4fb00-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4fb00-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb00-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4fb00-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4fb00-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fb00-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4fb00-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="4fb00-118">Library</span></span><br/> | <dl> <span data-ttu-id="4fb00-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fb00-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fb00-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4fb00-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb00-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="4fb00-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="4fb00-122">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="4fb00-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




