---
description: Imposta un valore della classe Texel che indica la classe Texel in base alla posizione di ogni Texel.
ms.assetid: cb2e6afb-4b6a-4b01-aaa8-1fd2d1f2bfa1
title: 'Metodo ID3DXTextureGutterHelper:: SetGutterMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d3c0b7c7e33664f3e078eca82a6f39b1294992a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323365"
---
# <a name="id3dxtexturegutterhelpersetguttermap-method"></a><span data-ttu-id="8b994-103">Metodo ID3DXTextureGutterHelper:: SetGutterMap</span><span class="sxs-lookup"><span data-stu-id="8b994-103">ID3DXTextureGutterHelper::SetGutterMap method</span></span>

<span data-ttu-id="8b994-104">Imposta un valore della classe Texel che indica la classe Texel in base alla posizione di ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="8b994-104">Sets a texel class value that indicates texel class according to each texel's location.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b994-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b994-105">Syntax</span></span>


```C++
HRESULT SetGutterMap(
  [in] BYTE *pGutterData
);
```



## <a name="parameters"></a><span data-ttu-id="8b994-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b994-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b994-107">*pGutterData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b994-107">*pGutterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b994-108">Tipo: **[ **byte**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8b994-108">Type: **[**BYTE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8b994-109">Puntatore alla classe Texel.</span><span class="sxs-lookup"><span data-stu-id="8b994-109">Pointer to the texel class.</span></span> <span data-ttu-id="8b994-110">Di seguito sono riportate le classi Texel possibili.</span><span class="sxs-lookup"><span data-stu-id="8b994-110">Possible texel classes are as follows.</span></span> <span data-ttu-id="8b994-111">Nessuna classe Texel 3.</span><span class="sxs-lookup"><span data-stu-id="8b994-111">There is no texel class 3.</span></span>



| <span data-ttu-id="8b994-112">Classe Texel</span><span class="sxs-lookup"><span data-stu-id="8b994-112">Texel Class</span></span> | <span data-ttu-id="8b994-113">Percorso Texel</span><span class="sxs-lookup"><span data-stu-id="8b994-113">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b994-114">0</span><span class="sxs-lookup"><span data-stu-id="8b994-114">0</span></span>           | <span data-ttu-id="8b994-115">Punto non valido; Texel non verrà usato.</span><span class="sxs-lookup"><span data-stu-id="8b994-115">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8b994-116">1</span><span class="sxs-lookup"><span data-stu-id="8b994-116">1</span></span>           | <span data-ttu-id="8b994-117">Triangolo interno.</span><span class="sxs-lookup"><span data-stu-id="8b994-117">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8b994-118">2</span><span class="sxs-lookup"><span data-stu-id="8b994-118">2</span></span>           | <span data-ttu-id="8b994-119">Barra interna.</span><span class="sxs-lookup"><span data-stu-id="8b994-119">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="8b994-120">4</span><span class="sxs-lookup"><span data-stu-id="8b994-120">4</span></span>           | <span data-ttu-id="8b994-121">Barra interna; Texel verrà valutato come un esempio completo nei metodi [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)o [**ID3DXTextureGutterHelper:: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) .</span><span class="sxs-lookup"><span data-stu-id="8b994-121">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b994-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b994-122">Return value</span></span>

<span data-ttu-id="8b994-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8b994-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8b994-124">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8b994-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8b994-125">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="8b994-125">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="8b994-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b994-126">Requirements</span></span>



| <span data-ttu-id="8b994-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b994-127">Requirement</span></span> | <span data-ttu-id="8b994-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8b994-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b994-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b994-129">Header</span></span><br/>  | <dl> <span data-ttu-id="8b994-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b994-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8b994-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="8b994-131">Library</span></span><br/> | <dl> <span data-ttu-id="8b994-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b994-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8b994-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b994-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b994-134">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="8b994-134">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
