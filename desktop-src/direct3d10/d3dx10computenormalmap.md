---
description: 'Funzione D3DX10ComputeNormalMap: converte una mappa di altezza in una mappa normale. I componenti (x,y,z) di ogni normale vengono mappati ai canali (r,g,b) della trama di output.'
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: Funzione D3DX10ComputeNormalMap (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ComputeNormalMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 173a8e0c1b3130a399152187eb52288a0306051c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105319"
---
# <a name="d3dx10computenormalmap-function"></a><span data-ttu-id="48ec9-104">Funzione D3DX10ComputeNormalMap</span><span class="sxs-lookup"><span data-stu-id="48ec9-104">D3DX10ComputeNormalMap function</span></span>

<span data-ttu-id="48ec9-105">Converte una mappa di altezza in una mappa normale.</span><span class="sxs-lookup"><span data-stu-id="48ec9-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="48ec9-106">I componenti (x,y,z) di ogni normale vengono mappati ai canali (r,g,b) della trama di output.</span><span class="sxs-lookup"><span data-stu-id="48ec9-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="48ec9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48ec9-107">Syntax</span></span>


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="48ec9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="48ec9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48ec9-109">*pSrcTexture* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="48ec9-109">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48ec9-110">Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="48ec9-110">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="48ec9-111">Puntatore a un'interfaccia ID3D10Texture2D, che rappresenta la trama della mappa dell'altezza di origine.</span><span class="sxs-lookup"><span data-stu-id="48ec9-111">Pointer to an ID3D10Texture2D interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="48ec9-112">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="48ec9-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48ec9-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48ec9-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48ec9-114">Uno o più flag D3DX \_ NORMALMAP che controllano la generazione di mappe normali.</span><span class="sxs-lookup"><span data-stu-id="48ec9-114">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="48ec9-115">*Canale* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="48ec9-115">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48ec9-116">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48ec9-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48ec9-117">Un flag CHANNEL D3DX \_ che specifica l'origine delle informazioni sull'altezza.</span><span class="sxs-lookup"><span data-stu-id="48ec9-117">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="48ec9-118">*Ampiezza* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="48ec9-118">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48ec9-119">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48ec9-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48ec9-120">Moltiplicatore di valori costante che aumenta (o diminuisce) i valori nella mappa normale.</span><span class="sxs-lookup"><span data-stu-id="48ec9-120">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="48ec9-121">I valori più elevati in genere rendono le dossi più visibili, i valori più bassi in genere rendono le dossi meno visibili.</span><span class="sxs-lookup"><span data-stu-id="48ec9-121">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="48ec9-122">*pDestTexture* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="48ec9-122">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48ec9-123">Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="48ec9-123">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="48ec9-124">Puntatore a un'interfaccia ID3D10Texture2D, che rappresenta la trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="48ec9-124">Pointer to an ID3D10Texture2D interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48ec9-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="48ec9-125">Return value</span></span>

<span data-ttu-id="48ec9-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="48ec9-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="48ec9-127">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="48ec9-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="48ec9-128">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="48ec9-128">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="48ec9-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="48ec9-129">Remarks</span></span>

<span data-ttu-id="48ec9-130">Questo metodo calcola la normale usando la differenza centrale con una dimensione del kernel di 3x3.</span><span class="sxs-lookup"><span data-stu-id="48ec9-130">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="48ec9-131">I canali RGB nella destinazione contengono componenti distorti (x,y,z) della normale.</span><span class="sxs-lookup"><span data-stu-id="48ec9-131">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="48ec9-132">Il denominatore differenze centrale è hardcoded a 2.0.</span><span class="sxs-lookup"><span data-stu-id="48ec9-132">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="48ec9-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48ec9-133">Requirements</span></span>



| <span data-ttu-id="48ec9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="48ec9-134">Requirement</span></span> | <span data-ttu-id="48ec9-135">Valore</span><span class="sxs-lookup"><span data-stu-id="48ec9-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48ec9-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48ec9-136">Header</span></span><br/>  | <dl> <span data-ttu-id="48ec9-137"><dt>D3DX10Tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="48ec9-137"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="48ec9-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="48ec9-138">Library</span></span><br/> | <dl> <span data-ttu-id="48ec9-139"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="48ec9-139"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="48ec9-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48ec9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48ec9-141">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="48ec9-141">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
