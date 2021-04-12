---
description: Allocare spazio per più ossa.
ms.assetid: f2acd338-f2c2-4340-a673-f36940cf31d9
title: 'Metodo ID3DX10SkinInfo:: AddBones (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4bf9667bd25dd717c4da96c2150e7bd7c45964f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354939"
---
# <a name="id3dx10skininfoaddbones-method"></a><span data-ttu-id="5c7c0-103">Metodo ID3DX10SkinInfo:: AddBones</span><span class="sxs-lookup"><span data-stu-id="5c7c0-103">ID3DX10SkinInfo::AddBones method</span></span>

<span data-ttu-id="5c7c0-104">Allocare spazio per più ossa.</span><span class="sxs-lookup"><span data-stu-id="5c7c0-104">Allocate space for more bones.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c7c0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c7c0-105">Syntax</span></span>


```C++
HRESULT AddBones(
  [in] UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="5c7c0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c7c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c7c0-107">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5c7c0-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c7c0-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c7c0-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c7c0-109">Numero di ossa da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="5c7c0-109">The number of bones to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c7c0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c7c0-110">Return value</span></span>

<span data-ttu-id="5c7c0-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5c7c0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5c7c0-112">Se questo metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5c7c0-112">If this method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5c7c0-113">Se il metodo ha esito negativo, il valore restituito può essere: E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="5c7c0-113">If the method fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c7c0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c7c0-114">Requirements</span></span>



| <span data-ttu-id="5c7c0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c7c0-115">Requirement</span></span> | <span data-ttu-id="5c7c0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5c7c0-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c7c0-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c7c0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5c7c0-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c7c0-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c7c0-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c7c0-119">Library</span></span><br/> | <dl> <span data-ttu-id="5c7c0-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c7c0-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c7c0-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c7c0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c7c0-122">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="5c7c0-122">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="5c7c0-123">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="5c7c0-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
