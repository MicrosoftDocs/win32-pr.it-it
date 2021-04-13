---
description: Limitare il numero di ossa che possono influenzare un vertice e/o limitare la quantità di influenza che può avere un osso su un vertice.
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: 'Metodo ID3DX10SkinInfo:: Compact (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.Compact
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 379343688a1fd2ffe5ebd968dc984fa09faada7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401944"
---
# <a name="id3dx10skininfocompact-method"></a><span data-ttu-id="9ce31-103">Metodo ID3DX10SkinInfo:: Compact</span><span class="sxs-lookup"><span data-stu-id="9ce31-103">ID3DX10SkinInfo::Compact method</span></span>

<span data-ttu-id="9ce31-104">Limitare il numero di ossa che possono influenzare un vertice e/o limitare la quantità di influenza che può avere un osso su un vertice.</span><span class="sxs-lookup"><span data-stu-id="9ce31-104">Limit the number of bones that can influence a vertex and/or limit the amount of influence a bone can have on a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ce31-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ce31-105">Syntax</span></span>


```C++
HRESULT Compact(
  [in] UINT  MaxPerVertexInfluences,
  [in] UINT  ScaleMode,
  [in] float MinWeight
);
```



## <a name="parameters"></a><span data-ttu-id="9ce31-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ce31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ce31-107">*MaxPerVertexInfluences* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ce31-107">*MaxPerVertexInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ce31-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ce31-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ce31-109">Numero massimo di ossa che possono influenzare qualsiasi vertice specificato.</span><span class="sxs-lookup"><span data-stu-id="9ce31-109">The maximum number of bones that can influence any given vertex.</span></span> <span data-ttu-id="9ce31-110">Questo valore viene ignorato se è maggiore del valore restituito da [**ID3DX10SkinInfo:: GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md).</span><span class="sxs-lookup"><span data-stu-id="9ce31-110">This value is ignored if it is greater than the value returned by [**ID3DX10SkinInfo::GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ce31-111">*ScaleMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ce31-111">*ScaleMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ce31-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ce31-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ce31-113">Flag che descrive come ridimensionare i pesi rimanenti su un determinato vertice dopo che alcuni sono stati tagliati da MinWeight.</span><span class="sxs-lookup"><span data-stu-id="9ce31-113">A flag describing how to scale the remaining weights on a given vertex after some have been chopped off by MinWeight.</span></span> <span data-ttu-id="9ce31-114">Se D3DX10 \_ SKININFO \_ non \_ viene specificato alcun ridimensionamento, i pesi non verranno ridimensionati.</span><span class="sxs-lookup"><span data-stu-id="9ce31-114">If D3DX10\_SKININFO\_NO\_SCALING is specified, the weights will not be scaled at all.</span></span> <span data-ttu-id="9ce31-115">Se \_ \_ si specifica d3dx10 SKININFO scale \_ a \_ 1, i pesi maggiori di MinWeight verranno scalati in modo da aggiungerli fino a 1,0.</span><span class="sxs-lookup"><span data-stu-id="9ce31-115">If D3DX10\_SKININFO\_SCALE\_TO\_1 is specified, the weights greater than MinWeight will be scaled up so that they add up to 1.0.</span></span> <span data-ttu-id="9ce31-116">Se \_ \_ si specifica d3dx10 SKININFO scale \_ to \_ Total, i pesi maggiori di MinWeight verranno ridimensionati in modo da aggiungerli al totale originale.</span><span class="sxs-lookup"><span data-stu-id="9ce31-116">If D3DX10\_SKININFO\_SCALE\_TO\_TOTAL is specified, the weights greater than MinWeight will be scaled up so that they add up to the original total.</span></span>

</dd> <dt>

<span data-ttu-id="9ce31-117">*MinWeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ce31-117">*MinWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ce31-118">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="9ce31-118">Type: **float**</span></span>

<span data-ttu-id="9ce31-119">Percentuale minima di influenza, o peso, che qualsiasi osso può avere su qualsiasi vertice.</span><span class="sxs-lookup"><span data-stu-id="9ce31-119">The minimum percentage of influence, or weight, that any bone can have on any vertex.</span></span> <span data-ttu-id="9ce31-120">Questo valore deve essere compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="9ce31-120">This value must be between 0 and 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ce31-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ce31-121">Return value</span></span>

<span data-ttu-id="9ce31-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9ce31-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9ce31-123">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9ce31-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9ce31-124">Se il metodo ha esito negativo, il valore restituito può essere: E \_ OutOfMemory o e \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="9ce31-124">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ce31-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ce31-125">Requirements</span></span>



| <span data-ttu-id="9ce31-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ce31-126">Requirement</span></span> | <span data-ttu-id="9ce31-127">Valore</span><span class="sxs-lookup"><span data-stu-id="9ce31-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce31-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ce31-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9ce31-129"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ce31-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ce31-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="9ce31-130">Library</span></span><br/> | <dl> <span data-ttu-id="9ce31-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ce31-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ce31-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ce31-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ce31-133">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="9ce31-133">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="9ce31-134">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="9ce31-134">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
