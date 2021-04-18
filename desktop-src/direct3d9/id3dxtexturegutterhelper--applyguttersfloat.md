---
description: Applica le grondature a un buffer di trama FLOAT.
ms.assetid: 822483d7-ae62-498a-bce7-3a925ab21c04
title: 'Metodo ID3DXTextureGutterHelper:: ApplyGuttersFloat (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00ee6eac7328ee5f6adceb5b3966c222509237b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322965"
---
# <a name="id3dxtexturegutterhelperapplyguttersfloat-method"></a><span data-ttu-id="2e08f-103">Metodo ID3DXTextureGutterHelper:: ApplyGuttersFloat</span><span class="sxs-lookup"><span data-stu-id="2e08f-103">ID3DXTextureGutterHelper::ApplyGuttersFloat method</span></span>

<span data-ttu-id="2e08f-104">Applica le grondature a un buffer di trama FLOAT.</span><span class="sxs-lookup"><span data-stu-id="2e08f-104">Applies gutters to a FLOAT texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e08f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e08f-105">Syntax</span></span>


```C++
HRESULT ApplyGuttersFloat(
  [in] FLOAT *pDataIn,
  [in] UINT  *NumCoeffs,
  [in] UINT  *Width,
  [in] UINT  *Height
);
```



## <a name="parameters"></a><span data-ttu-id="2e08f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e08f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e08f-107">*pDataIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e08f-107">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e08f-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e08f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2e08f-109">Puntatore a un buffer di dati di trama FLOAT.</span><span class="sxs-lookup"><span data-stu-id="2e08f-109">Pointer to a buffer of FLOAT texture data.</span></span>

</dd> <dt>

<span data-ttu-id="2e08f-110">*NumCoeffs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e08f-110">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e08f-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e08f-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2e08f-112">Numero di scalari per canale di colore utilizzato in memoria per archiviare esempi.</span><span class="sxs-lookup"><span data-stu-id="2e08f-112">Number of scalars per color channel used in memory to store samples.</span></span> <span data-ttu-id="2e08f-113">Ogni Texel contiene valori FLOAT NumCoeffs.</span><span class="sxs-lookup"><span data-stu-id="2e08f-113">Each texel contains NumCoeffs FLOAT values.</span></span>

</dd> <dt>

<span data-ttu-id="2e08f-114">*Larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e08f-114">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e08f-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e08f-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2e08f-116">Larghezza della trama, in pixel, ottenuta da [**ID3DXTextureGutterHelper:: GetWidth**](id3dxtexturegutterhelper--getwidth.md).</span><span class="sxs-lookup"><span data-stu-id="2e08f-116">Width of the texture, in pixels, obtained from [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e08f-117">*Altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e08f-117">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e08f-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e08f-118">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2e08f-119">Altezza della trama, in pixel, ottenuta da [**ID3DXTextureGutterHelper:: GetHeight**](id3dxtexturegutterhelper--getheight.md).</span><span class="sxs-lookup"><span data-stu-id="2e08f-119">Height of the texture, in pixels, obtained from [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e08f-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e08f-120">Return value</span></span>

<span data-ttu-id="2e08f-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2e08f-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2e08f-122">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2e08f-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2e08f-123">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="2e08f-123">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="2e08f-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e08f-124">Remarks</span></span>

<span data-ttu-id="2e08f-125">I [**Texel della classe 2**](id3dxtexturegutterhelper.md) vengono generati ricampionando la classe 1 e 4 Texel.</span><span class="sxs-lookup"><span data-stu-id="2e08f-125">[**Class 2 texels**](id3dxtexturegutterhelper.md) are generated by resampling class 1 and 4 texels.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e08f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e08f-126">Requirements</span></span>



| <span data-ttu-id="2e08f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e08f-127">Requirement</span></span> | <span data-ttu-id="2e08f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2e08f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e08f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e08f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2e08f-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e08f-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2e08f-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="2e08f-131">Library</span></span><br/> | <dl> <span data-ttu-id="2e08f-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e08f-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2e08f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e08f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e08f-134">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="2e08f-134">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
