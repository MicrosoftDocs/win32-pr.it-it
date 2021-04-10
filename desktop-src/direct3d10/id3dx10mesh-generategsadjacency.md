---
description: Aggiunge i dati di adiacenza al buffer di indice della mesh. Quando la mesh deve essere inviata a un geometry shader che accetta i dati di adiacenza, è necessario che il buffer di indice della mesh contenga i dati adiacenza.
ms.assetid: 8e587620-a4b6-4415-8fe7-9ec22f253b16
title: 'Metodo ID3DX10Mesh:: GenerateGSAdjacency (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateGSAdjacency
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d47747acfa97fbe843dabf527c8f94742db78d6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058642"
---
# <a name="id3dx10meshgenerategsadjacency-method"></a><span data-ttu-id="7aeee-104">Metodo ID3DX10Mesh:: GenerateGSAdjacency</span><span class="sxs-lookup"><span data-stu-id="7aeee-104">ID3DX10Mesh::GenerateGSAdjacency method</span></span>

<span data-ttu-id="7aeee-105">Aggiunge i dati di adiacenza al buffer di indice della mesh.</span><span class="sxs-lookup"><span data-stu-id="7aeee-105">Adds adjacency data to the mesh's index buffer.</span></span> <span data-ttu-id="7aeee-106">Quando la mesh deve essere inviata a un geometry shader che accetta i dati di adiacenza, è necessario che il buffer di indice della mesh contenga i dati adiacenza.</span><span class="sxs-lookup"><span data-stu-id="7aeee-106">When the mesh is to be sent to a geometry shader that takes adjacency data, it is neccessary for the mesh's index buffer to contain adjacency data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aeee-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7aeee-107">Syntax</span></span>


```C++
HRESULT GenerateGSAdjacency();
```



## <a name="parameters"></a><span data-ttu-id="7aeee-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7aeee-108">Parameters</span></span>

<span data-ttu-id="7aeee-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7aeee-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7aeee-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7aeee-110">Return value</span></span>

<span data-ttu-id="7aeee-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7aeee-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7aeee-112">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7aeee-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7aeee-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7aeee-113">Requirements</span></span>



| <span data-ttu-id="7aeee-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7aeee-114">Requirement</span></span> | <span data-ttu-id="7aeee-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7aeee-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7aeee-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7aeee-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7aeee-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7aeee-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7aeee-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="7aeee-118">Library</span></span><br/> | <dl> <span data-ttu-id="7aeee-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7aeee-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7aeee-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7aeee-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aeee-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="7aeee-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="7aeee-122">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="7aeee-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




