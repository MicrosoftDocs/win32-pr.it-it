---
title: Metodo ID3DX11EffectConstantBuffer SetTextureBuffer (D3dx11effect. h)
description: Impostare un buffer di trama.
ms.assetid: b8c327e4-52ff-498e-81e9-187e58bbe5d2
keywords:
- Metodo SetTextureBuffer Direct3D 11
- Metodo SetTextureBuffer Direct3D 11, interfaccia ID3DX11EffectConstantBuffer
- Interfaccia ID3DX11EffectConstantBuffer Direct3D 11, metodo SetTextureBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736ec4c5f0125dfc37925d67875cf97c5441117c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982160"
---
# <a name="id3dx11effectconstantbuffersettexturebuffer-method"></a><span data-ttu-id="ce5a1-106">Metodo ID3DX11EffectConstantBuffer:: SetTextureBuffer</span><span class="sxs-lookup"><span data-stu-id="ce5a1-106">ID3DX11EffectConstantBuffer::SetTextureBuffer method</span></span>

<span data-ttu-id="ce5a1-107">Impostare un buffer di trama.</span><span class="sxs-lookup"><span data-stu-id="ce5a1-107">Set a texture-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce5a1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce5a1-108">Syntax</span></span>


```C++
HRESULT SetTextureBuffer(
   ID3D11ShaderResourceView *pTextureBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="ce5a1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce5a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce5a1-110">*pTextureBuffer*</span><span class="sxs-lookup"><span data-stu-id="ce5a1-110">*pTextureBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="ce5a1-111">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="ce5a1-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span></span>

<span data-ttu-id="ce5a1-112">Puntatore a un'interfaccia di visualizzazione delle risorse shader per accedere a un buffer di trama.</span><span class="sxs-lookup"><span data-stu-id="ce5a1-112">A pointer to a shader-resource-view interface for accessing a texture buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce5a1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce5a1-113">Return value</span></span>

<span data-ttu-id="ce5a1-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce5a1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce5a1-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ce5a1-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ce5a1-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce5a1-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ce5a1-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="ce5a1-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ce5a1-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="ce5a1-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ce5a1-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ce5a1-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ce5a1-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce5a1-120">Requirements</span></span>



| <span data-ttu-id="ce5a1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce5a1-121">Requirement</span></span> | <span data-ttu-id="ce5a1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ce5a1-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce5a1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce5a1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ce5a1-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce5a1-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ce5a1-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="ce5a1-125">Library</span></span><br/> | <dl> <span data-ttu-id="ce5a1-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="ce5a1-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce5a1-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce5a1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce5a1-128">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="ce5a1-128">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





