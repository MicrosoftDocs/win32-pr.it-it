---
description: Riceve un valore della classe Texel che indica la classe Texel in base alla posizione di ogni Texel.
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: 'Metodo ID3DXTextureGutterHelper:: GetGutterMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d973e716c598eaceaf7f75e6694a35691df4266
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322961"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a><span data-ttu-id="81b11-103">Metodo ID3DXTextureGutterHelper:: GetGutterMap</span><span class="sxs-lookup"><span data-stu-id="81b11-103">ID3DXTextureGutterHelper::GetGutterMap method</span></span>

<span data-ttu-id="81b11-104">Riceve un valore della classe Texel che indica la classe Texel in base alla posizione di ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="81b11-104">Receives a texel class value that indicates texel class according to each texel's location.</span></span>

## <a name="syntax"></a><span data-ttu-id="81b11-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81b11-105">Syntax</span></span>


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a><span data-ttu-id="81b11-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="81b11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81b11-107">*pGutterData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="81b11-107">*pGutterData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="81b11-108">Tipo: **[ **byte**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="81b11-108">Type: **[**BYTE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="81b11-109">Puntatore alla classe Texel.</span><span class="sxs-lookup"><span data-stu-id="81b11-109">Pointer to the texel class.</span></span> <span data-ttu-id="81b11-110">Di seguito sono riportate le classi Texel possibili.</span><span class="sxs-lookup"><span data-stu-id="81b11-110">Possible texel classes are as follows.</span></span> <span data-ttu-id="81b11-111">Nessuna classe Texel 3.</span><span class="sxs-lookup"><span data-stu-id="81b11-111">There is no texel class 3.</span></span>



| <span data-ttu-id="81b11-112">Classe Texel</span><span class="sxs-lookup"><span data-stu-id="81b11-112">Texel Class</span></span> | <span data-ttu-id="81b11-113">Percorso Texel</span><span class="sxs-lookup"><span data-stu-id="81b11-113">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81b11-114">0</span><span class="sxs-lookup"><span data-stu-id="81b11-114">0</span></span>           | <span data-ttu-id="81b11-115">Punto non valido; Texel non verrà usato.</span><span class="sxs-lookup"><span data-stu-id="81b11-115">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="81b11-116">1</span><span class="sxs-lookup"><span data-stu-id="81b11-116">1</span></span>           | <span data-ttu-id="81b11-117">Triangolo interno.</span><span class="sxs-lookup"><span data-stu-id="81b11-117">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="81b11-118">2</span><span class="sxs-lookup"><span data-stu-id="81b11-118">2</span></span>           | <span data-ttu-id="81b11-119">Barra interna.</span><span class="sxs-lookup"><span data-stu-id="81b11-119">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="81b11-120">4</span><span class="sxs-lookup"><span data-stu-id="81b11-120">4</span></span>           | <span data-ttu-id="81b11-121">Barra interna; Texel verrà valutato come un esempio completo nei metodi [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)o [**ID3DXTextureGutterHelper:: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) .</span><span class="sxs-lookup"><span data-stu-id="81b11-121">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81b11-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81b11-122">Return value</span></span>

<span data-ttu-id="81b11-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81b11-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81b11-124">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="81b11-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="81b11-125">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="81b11-125">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="81b11-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="81b11-126">Remarks</span></span>

<span data-ttu-id="81b11-127">L'applicazione deve allocare e gestire pGutterData, con le dimensioni fornite da:</span><span class="sxs-lookup"><span data-stu-id="81b11-127">The application must allocate and manage pGutterData, with size given by:</span></span>


```
texture width * texture height * sizeof(BYTE)
```



<span data-ttu-id="81b11-128">La larghezza e l'altezza della trama vengono restituite da [**ID3DXTextureGutterHelper:: GetWidth**](id3dxtexturegutterhelper--getwidth.md) e [**ID3DXTextureGutterHelper:: GetHeight**](id3dxtexturegutterhelper--getheight.md).</span><span class="sxs-lookup"><span data-stu-id="81b11-128">Texture width and height are returned by [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md) and [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81b11-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81b11-129">Requirements</span></span>



| <span data-ttu-id="81b11-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="81b11-130">Requirement</span></span> | <span data-ttu-id="81b11-131">Valore</span><span class="sxs-lookup"><span data-stu-id="81b11-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81b11-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81b11-132">Header</span></span><br/>  | <dl> <span data-ttu-id="81b11-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="81b11-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="81b11-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="81b11-134">Library</span></span><br/> | <dl> <span data-ttu-id="81b11-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81b11-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="81b11-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81b11-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81b11-137">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="81b11-137">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
