---
title: Metodo ID3DX11EffectPass GetGeometryShaderDesc (D3dx11effect. h)
description: Ottenere una descrizione dello shader di geometria.
ms.assetid: 03298ec3-6b85-40bf-8920-a82c7606d326
keywords:
- Metodo GetGeometryShaderDesc Direct3D 11
- Metodo GetGeometryShaderDesc Direct3D 11, interfaccia ID3DX11EffectPass
- Interfaccia ID3DX11EffectPass Direct3D 11, metodo GetGeometryShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetGeometryShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c3b84ed9e8c245611c1442987b68a94e7b10ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995954"
---
# <a name="id3dx11effectpassgetgeometryshaderdesc-method"></a><span data-ttu-id="6d327-106">Metodo ID3DX11EffectPass:: GetGeometryShaderDesc</span><span class="sxs-lookup"><span data-stu-id="6d327-106">ID3DX11EffectPass::GetGeometryShaderDesc method</span></span>

<span data-ttu-id="6d327-107">Ottenere una descrizione dello shader di geometria.</span><span class="sxs-lookup"><span data-stu-id="6d327-107">Get a geometry-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d327-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d327-108">Syntax</span></span>


```C++
HRESULT GetGeometryShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="6d327-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d327-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d327-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="6d327-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="6d327-111">Tipo: **[ **D3DX11 \_ pass \_ shader \_ desc**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="6d327-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="6d327-112">Puntatore a una descrizione dello shader di geometria (vedere [**D3DX11 \_ pass \_ shader \_ desc**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="6d327-112">A pointer to a geometry-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d327-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d327-113">Return value</span></span>

<span data-ttu-id="6d327-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d327-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d327-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6d327-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6d327-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d327-116">Remarks</span></span>

<span data-ttu-id="6d327-117">Un passaggio di effetto può contenere le assegnazioni dello stato di rendering e le assegnazioni degli oggetti shader.</span><span class="sxs-lookup"><span data-stu-id="6d327-117">An effect pass can contain render state assignments and shader object assignments.</span></span>

> [!Note]  
> <span data-ttu-id="6d327-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="6d327-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6d327-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="6d327-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6d327-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6d327-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d327-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d327-121">Requirements</span></span>



| <span data-ttu-id="6d327-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d327-122">Requirement</span></span> | <span data-ttu-id="6d327-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6d327-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d327-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d327-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6d327-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d327-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6d327-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="6d327-126">Library</span></span><br/> | <dl> <span data-ttu-id="6d327-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="6d327-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d327-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d327-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d327-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="6d327-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





