---
description: Imposta i dati adiacenza della mesh.
ms.assetid: 67d51ce0-7fe2-484d-9874-f1fa59632d59
title: 'Metodo ID3DX10Mesh:: SetAdjacencyData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAdjacencyData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6fabced002caf424fa1fcbcefcb3b326b0c71f7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323140"
---
# <a name="id3dx10meshsetadjacencydata-method"></a><span data-ttu-id="2844a-103">Metodo ID3DX10Mesh:: SetAdjacencyData</span><span class="sxs-lookup"><span data-stu-id="2844a-103">ID3DX10Mesh::SetAdjacencyData method</span></span>

<span data-ttu-id="2844a-104">Imposta i dati adiacenza della mesh.</span><span class="sxs-lookup"><span data-stu-id="2844a-104">Set the mesh's adjacency data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2844a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2844a-105">Syntax</span></span>


```C++
HRESULT SetAdjacencyData(
  [in] const UINT *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="2844a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2844a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2844a-107">*pAdjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2844a-107">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2844a-108">Tipo: **const [**uint**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2844a-108">Type: **const [**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2844a-109">Dati adiacenza da impostare.</span><span class="sxs-lookup"><span data-stu-id="2844a-109">The adjacency data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2844a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2844a-110">Return value</span></span>

<span data-ttu-id="2844a-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2844a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2844a-112">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2844a-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2844a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2844a-113">Requirements</span></span>



| <span data-ttu-id="2844a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2844a-114">Requirement</span></span> | <span data-ttu-id="2844a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2844a-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2844a-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2844a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2844a-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2844a-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2844a-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="2844a-118">Library</span></span><br/> | <dl> <span data-ttu-id="2844a-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2844a-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2844a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2844a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2844a-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="2844a-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="2844a-122">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="2844a-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
