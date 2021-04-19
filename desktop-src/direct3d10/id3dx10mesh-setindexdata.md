---
description: Imposta i dati dell'indice della mesh.
ms.assetid: f3e7e166-94b5-45f6-9d43-8d7e32b7b523
title: 'Metodo ID3DX10Mesh:: SetIndexData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetIndexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f561a4109fbab2163b2ec51e95b45a618da5b6d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323138"
---
# <a name="id3dx10meshsetindexdata-method"></a><span data-ttu-id="ecb3b-103">Metodo ID3DX10Mesh:: SetIndexData</span><span class="sxs-lookup"><span data-stu-id="ecb3b-103">ID3DX10Mesh::SetIndexData method</span></span>

<span data-ttu-id="ecb3b-104">Imposta i dati dell'indice della mesh.</span><span class="sxs-lookup"><span data-stu-id="ecb3b-104">Set the mesh's index data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb3b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecb3b-105">Syntax</span></span>


```C++
HRESULT SetIndexData(
  [in] const void *pData,
  [in]       UINT cIndices
);
```



## <a name="parameters"></a><span data-ttu-id="ecb3b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecb3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecb3b-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecb3b-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb3b-108">Tipo: **const \* void**</span><span class="sxs-lookup"><span data-stu-id="ecb3b-108">Type: **const void\***</span></span>

<span data-ttu-id="ecb3b-109">Dati dell'indice.</span><span class="sxs-lookup"><span data-stu-id="ecb3b-109">The index data.</span></span>

</dd> <dt>

<span data-ttu-id="ecb3b-110">*cIndices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecb3b-110">*cIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb3b-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ecb3b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ecb3b-112">Numero di indici in pData.</span><span class="sxs-lookup"><span data-stu-id="ecb3b-112">The number of indices in pData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecb3b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecb3b-113">Return value</span></span>

<span data-ttu-id="ecb3b-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ecb3b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ecb3b-115">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ecb3b-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ecb3b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecb3b-116">Requirements</span></span>



| <span data-ttu-id="ecb3b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecb3b-117">Requirement</span></span> | <span data-ttu-id="ecb3b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ecb3b-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb3b-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ecb3b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ecb3b-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecb3b-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ecb3b-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="ecb3b-121">Library</span></span><br/> | <dl> <span data-ttu-id="ecb3b-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecb3b-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecb3b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecb3b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb3b-124">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ecb3b-124">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ecb3b-125">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="ecb3b-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
