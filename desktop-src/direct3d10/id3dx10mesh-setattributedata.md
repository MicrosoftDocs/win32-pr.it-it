---
description: Imposta i dati dell'attributo della mesh.
ms.assetid: bcf7b1b3-b923-400a-8d12-5094f3844d8f
title: 'Metodo ID3DX10Mesh:: SetAttributeData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 19d69f8747196d7b25c85cb04fb173adef193098
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235114"
---
# <a name="id3dx10meshsetattributedata-method"></a><span data-ttu-id="b086a-103">Metodo ID3DX10Mesh:: SetAttributeData</span><span class="sxs-lookup"><span data-stu-id="b086a-103">ID3DX10Mesh::SetAttributeData method</span></span>

<span data-ttu-id="b086a-104">Imposta i dati dell'attributo della mesh.</span><span class="sxs-lookup"><span data-stu-id="b086a-104">Set the mesh's attribute data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b086a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b086a-105">Syntax</span></span>


```C++
HRESULT SetAttributeData(
  [in] const UINT *pData
);
```



## <a name="parameters"></a><span data-ttu-id="b086a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b086a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b086a-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b086a-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b086a-108">Tipo: **const [**uint**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b086a-108">Type: **const [**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b086a-109">Dati dell'attributo da impostare.</span><span class="sxs-lookup"><span data-stu-id="b086a-109">The attribute data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b086a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b086a-110">Return value</span></span>

<span data-ttu-id="b086a-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b086a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b086a-112">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b086a-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b086a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b086a-113">Requirements</span></span>



| <span data-ttu-id="b086a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b086a-114">Requirement</span></span> | <span data-ttu-id="b086a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b086a-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b086a-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b086a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b086a-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b086a-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b086a-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="b086a-118">Library</span></span><br/> | <dl> <span data-ttu-id="b086a-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b086a-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b086a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b086a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b086a-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="b086a-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="b086a-122">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="b086a-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
