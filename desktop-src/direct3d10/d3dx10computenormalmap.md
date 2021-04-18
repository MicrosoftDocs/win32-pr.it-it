---
description: Converte una mappa di altezza in una mappa normale. Ai componenti (x, y, z) di ogni normale viene eseguito il mapping ai canali (r, g, b) della trama di output.
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: Funzione D3DX10ComputeNormalMap (D3DX10Tex. h)
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
ms.openlocfilehash: 1d7318e6d00d921ba0d573eb6fb696eed6c6a58d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322951"
---
# <a name="d3dx10computenormalmap-function"></a><span data-ttu-id="3a304-104">D3DX10ComputeNormalMap (funzione)</span><span class="sxs-lookup"><span data-stu-id="3a304-104">D3DX10ComputeNormalMap function</span></span>

<span data-ttu-id="3a304-105">Converte una mappa di altezza in una mappa normale.</span><span class="sxs-lookup"><span data-stu-id="3a304-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="3a304-106">Ai componenti (x, y, z) di ogni normale viene eseguito il mapping ai canali (r, g, b) della trama di output.</span><span class="sxs-lookup"><span data-stu-id="3a304-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a304-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a304-107">Syntax</span></span>


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="3a304-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a304-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a304-109">*pSrcTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a304-109">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a304-110">Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="3a304-110">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="3a304-111">Puntatore a un'interfaccia ID3D10Texture2D, che rappresenta la trama della mappa dell'altezza di origine.</span><span class="sxs-lookup"><span data-stu-id="3a304-111">Pointer to an ID3D10Texture2D interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="3a304-112">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a304-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a304-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a304-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a304-114">Uno o più \_ flag normalmap D3DX che controllano la generazione di mappe normali.</span><span class="sxs-lookup"><span data-stu-id="3a304-114">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="3a304-115">*Canale* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3a304-115">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a304-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a304-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a304-117">Un \_ flag del canale D3DX che specifica l'origine delle informazioni sull'altezza.</span><span class="sxs-lookup"><span data-stu-id="3a304-117">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="3a304-118">*Ampiezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a304-118">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a304-119">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a304-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a304-120">Valore costante moltiplicatore che aumenta (o diminuisce) i valori nella mappa normale.</span><span class="sxs-lookup"><span data-stu-id="3a304-120">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="3a304-121">I valori più elevati in genere rendono più visibili i riscontri, mentre i valori più bassi rendono meno visibili i riscontri.</span><span class="sxs-lookup"><span data-stu-id="3a304-121">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="3a304-122">*pDestTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a304-122">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a304-123">Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="3a304-123">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="3a304-124">Puntatore a un'interfaccia ID3D10Texture2D, che rappresenta la trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3a304-124">Pointer to an ID3D10Texture2D interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a304-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a304-125">Return value</span></span>

<span data-ttu-id="3a304-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a304-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a304-127">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3a304-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3a304-128">Se la funzione ha esito negativo, il valore restituito può essere il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3a304-128">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a304-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a304-129">Remarks</span></span>

<span data-ttu-id="3a304-130">Questo metodo calcola la normalità usando la differenza centrale con una dimensione del kernel di 3x3.</span><span class="sxs-lookup"><span data-stu-id="3a304-130">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="3a304-131">I canali RGB nella destinazione contengono i componenti parziali (x, y, z) del normale.</span><span class="sxs-lookup"><span data-stu-id="3a304-131">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="3a304-132">Il denominatore differenze centrale è hardcoded in 2,0.</span><span class="sxs-lookup"><span data-stu-id="3a304-132">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a304-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a304-133">Requirements</span></span>



| <span data-ttu-id="3a304-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a304-134">Requirement</span></span> | <span data-ttu-id="3a304-135">Valore</span><span class="sxs-lookup"><span data-stu-id="3a304-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a304-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a304-136">Header</span></span><br/>  | <dl> <span data-ttu-id="3a304-137"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a304-137"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="3a304-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="3a304-138">Library</span></span><br/> | <dl> <span data-ttu-id="3a304-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a304-139"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3a304-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a304-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a304-141">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="3a304-141">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
