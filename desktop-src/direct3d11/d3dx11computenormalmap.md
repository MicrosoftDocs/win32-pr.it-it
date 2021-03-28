---
title: Funzione D3DX11ComputeNormalMap (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTex, ComputeNormalMap.
ms.assetid: 3ccdbd9a-669e-48ff-97d5-e5a6c7d2fb26
keywords:
- Funzione D3DX11ComputeNormalMap Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11ComputeNormalMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4399282c325fde0ea46679da9e9b84331b8c125b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235134"
---
# <a name="d3dx11computenormalmap-function"></a><span data-ttu-id="dcaf1-105">D3DX11ComputeNormalMap (funzione)</span><span class="sxs-lookup"><span data-stu-id="dcaf1-105">D3DX11ComputeNormalMap function</span></span>

> [!Note]  
> <span data-ttu-id="dcaf1-106">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="dcaf1-107">Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) , **ComputeNormalMap**.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-107">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **ComputeNormalMap**.</span></span>

 

<span data-ttu-id="dcaf1-108">Converte una mappa di altezza in una mappa normale.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-108">Converts a height map into a normal map.</span></span> <span data-ttu-id="dcaf1-109">Ai componenti (x, y, z) di ogni normale viene eseguito il mapping ai canali (r, g, b) della trama di output.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-109">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcaf1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcaf1-110">Syntax</span></span>


```C++
HRESULT D3DX11ComputeNormalMap(
  _In_ ID3D11DeviceContext *pContext,
  _In_ ID3D11Texture2D     *pSrcTexture,
  _In_ UINT                Flags,
  _In_ UINT                Channel,
  _In_ FLOAT               Amplitude,
  _In_ ID3D11Texture2D     *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="dcaf1-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcaf1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcaf1-112">*pContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcaf1-112">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcaf1-113">Tipo: **[ **sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="dcaf1-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="dcaf1-114">Puntatore a un'interfaccia [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) , che rappresenta la trama della mappa dell'altezza di origine.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-114">Pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="dcaf1-115">*pSrcTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcaf1-115">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcaf1-116">Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="dcaf1-116">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="dcaf1-117">Puntatore a un'interfaccia [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , che rappresenta la trama della mappa dell'altezza di origine.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-117">Pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="dcaf1-118">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcaf1-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcaf1-119">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dcaf1-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dcaf1-120">Uno o più \_ flag normalmap D3DX che controllano la generazione di mappe normali.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-120">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="dcaf1-121">*Canale* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="dcaf1-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcaf1-122">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dcaf1-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dcaf1-123">Un \_ flag del canale D3DX che specifica l'origine delle informazioni sull'altezza.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-123">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="dcaf1-124">*Ampiezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcaf1-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcaf1-125">Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dcaf1-125">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dcaf1-126">Valore costante moltiplicatore che aumenta (o diminuisce) i valori nella mappa normale.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="dcaf1-127">I valori più elevati in genere rendono più visibili i riscontri, mentre i valori più bassi rendono meno visibili i riscontri.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="dcaf1-128">*pDestTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcaf1-128">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcaf1-129">Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="dcaf1-129">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="dcaf1-130">Puntatore a un'interfaccia [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , che rappresenta la trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-130">Pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcaf1-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcaf1-131">Return value</span></span>

<span data-ttu-id="dcaf1-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dcaf1-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dcaf1-133">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-133">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dcaf1-134">Se la funzione ha esito negativo, il valore restituito può essere il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-134">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcaf1-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="dcaf1-135">Remarks</span></span>

<span data-ttu-id="dcaf1-136">Questo metodo calcola la normalità usando la differenza centrale con una dimensione del kernel di 3x3.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-136">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="dcaf1-137">I canali RGB nella destinazione contengono i componenti parziali (x, y, z) del normale.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-137">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="dcaf1-138">Il denominatore differenze centrale è hardcoded in 2,0.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-138">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcaf1-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcaf1-139">Requirements</span></span>



| <span data-ttu-id="dcaf1-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcaf1-140">Requirement</span></span> | <span data-ttu-id="dcaf1-141">Valore</span><span class="sxs-lookup"><span data-stu-id="dcaf1-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcaf1-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dcaf1-142">Header</span></span><br/>  | <dl> <span data-ttu-id="dcaf1-143"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcaf1-143"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="dcaf1-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="dcaf1-144">Library</span></span><br/> | <dl> <span data-ttu-id="dcaf1-145"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcaf1-145"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="dcaf1-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcaf1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcaf1-147">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="dcaf1-147">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

