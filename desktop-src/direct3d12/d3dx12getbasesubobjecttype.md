---
title: Funzione D3DX12GetBaseSubobjectType (D3dx12. h)
description: Restituisce il tipo di sottooggetto che corrisponde alla classe di base del tipo di sottooggetto passato.
ms.assetid: 3744B042-094C-4EA4-8185-A018B728D843
keywords:
- D3DX12GetBaseSubobjectType (funzione)
topic_type:
- apiref
api_name:
- D3DX12GetBaseSubobjectType
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b39f1c61be682d55512772bef1258aecdb009a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322176"
---
# <a name="d3dx12getbasesubobjecttype-function"></a><span data-ttu-id="47bd2-104">D3DX12GetBaseSubobjectType (funzione)</span><span class="sxs-lookup"><span data-stu-id="47bd2-104">D3DX12GetBaseSubobjectType function</span></span>

<span data-ttu-id="47bd2-105">Restituisce il tipo di sottooggetto che corrisponde alla classe di base del tipo di sottooggetto passato.</span><span class="sxs-lookup"><span data-stu-id="47bd2-105">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span>

## <a name="syntax"></a><span data-ttu-id="47bd2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47bd2-106">Syntax</span></span>


```C++
D3D12_PIPELINE_STATE_SUBOBJECT_TYPE inline D3DX12GetBaseSubobjectType(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE SubobjectType
);
```



## <a name="parameters"></a><span data-ttu-id="47bd2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="47bd2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47bd2-108">*Sottoobjecttype*</span><span class="sxs-lookup"><span data-stu-id="47bd2-108">*SubobjectType*</span></span> 
</dt> <dd>

<span data-ttu-id="47bd2-109">Tipo: **\_ \_ \_ \_ tipo di sottooggetto stato della pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="47bd2-109">Type: **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>

<span data-ttu-id="47bd2-110">Valore di enumerazione che specifica il tipo di sottooggetto a cui si è interessati.</span><span class="sxs-lookup"><span data-stu-id="47bd2-110">An enumeration value that specifies the subobject type that you're interested in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47bd2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47bd2-111">Return value</span></span>

<span data-ttu-id="47bd2-112">Tipo: **\_ \_ \_ \_ tipo di sottooggetto stato della pipeline D3D12**</span><span class="sxs-lookup"><span data-stu-id="47bd2-112">Type: **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>

<span data-ttu-id="47bd2-113">Se *subobjecttype* corrisponde a un tipo di dati SubObject derivato da un altro tipo di dati SubObject, viene restituito il tipo di oggetto SubObject del tipo di dati SubObject di base. in caso contrario, viene restituito il tipo di sottooggetto passato.</span><span class="sxs-lookup"><span data-stu-id="47bd2-113">If *SubobjectType* corresponds to a subobject data type that is derived from another subobject data type, the subobject type of the base subobject data type is returned; otherwise, the passed-in subobject type is returned.</span></span> <span data-ttu-id="47bd2-114">Se, ad esempio, viene passato il STENCIL1 di profondità del **\_ \_ \_ \_ tipo \_ \_ di sottooggetto stato della pipeline D3D12** , viene restituito **\_ \_ lo \_ stencil di profondità del \_ tipo \_ \_ di sottooggetto stato** della pipeline D3D12.</span><span class="sxs-lookup"><span data-stu-id="47bd2-114">For example, if **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL1** is passed in, then **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="47bd2-115">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="47bd2-115">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="47bd2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47bd2-116">Requirements</span></span>



| <span data-ttu-id="47bd2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="47bd2-117">Requirement</span></span> | <span data-ttu-id="47bd2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="47bd2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="47bd2-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47bd2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="47bd2-120"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="47bd2-120"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="47bd2-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="47bd2-121">Library</span></span><br/> | <dl> <span data-ttu-id="47bd2-122"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47bd2-122"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="47bd2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="47bd2-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="47bd2-124"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47bd2-124"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47bd2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47bd2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47bd2-126">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="47bd2-126">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





