---
title: Metodo seresource ID3DX11EffectShaderResourceVariable (D3dx11effect. h)
description: Impostare una risorsa shader.
ms.assetid: f85c33ff-dc00-4421-939c-74f9317faadc
keywords:
- Metodo seresource Direct3D 11
- Metodo seresource Direct3D 11, interfaccia ID3DX11EffectShaderResourceVariable
- Interfaccia ID3DX11EffectShaderResourceVariable Direct3D 11, metodo seresource
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.SetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec6c7daa2db552d6b5befee02bf57c6047dc5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356099"
---
# <a name="id3dx11effectshaderresourcevariablesetresource-method"></a><span data-ttu-id="49a83-106">Metodo ID3DX11EffectShaderResourceVariable:: seresource</span><span class="sxs-lookup"><span data-stu-id="49a83-106">ID3DX11EffectShaderResourceVariable::SetResource method</span></span>

<span data-ttu-id="49a83-107">Impostare una risorsa shader.</span><span class="sxs-lookup"><span data-stu-id="49a83-107">Set a shader resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="49a83-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49a83-108">Syntax</span></span>


```C++
HRESULT SetResource(
   ID3D11ShaderResourceView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="49a83-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="49a83-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49a83-110">*pResource*</span><span class="sxs-lookup"><span data-stu-id="49a83-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="49a83-111">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="49a83-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span></span>

<span data-ttu-id="49a83-112">Indirizzo di un puntatore a un'interfaccia shader-Resource-View.</span><span class="sxs-lookup"><span data-stu-id="49a83-112">The address of a pointer to a shader-resource-view interface.</span></span> <span data-ttu-id="49a83-113">Vedere [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="49a83-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49a83-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49a83-114">Return value</span></span>

<span data-ttu-id="49a83-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49a83-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49a83-116">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="49a83-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="49a83-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="49a83-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="49a83-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="49a83-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="49a83-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="49a83-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="49a83-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="49a83-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="49a83-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49a83-121">Requirements</span></span>



| <span data-ttu-id="49a83-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="49a83-122">Requirement</span></span> | <span data-ttu-id="49a83-123">Valore</span><span class="sxs-lookup"><span data-stu-id="49a83-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49a83-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49a83-124">Header</span></span><br/>  | <dl> <span data-ttu-id="49a83-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="49a83-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="49a83-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="49a83-126">Library</span></span><br/> | <dl> <span data-ttu-id="49a83-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="49a83-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49a83-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49a83-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49a83-129">ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="49a83-129">ID3DX11EffectShaderResourceVariable</span></span>](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 





