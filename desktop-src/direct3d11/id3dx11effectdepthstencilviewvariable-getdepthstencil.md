---
title: Metodo ID3DX11EffectDepthStencilViewVariable GetDepthStencil (D3dx11effect. h)
description: Ottenere una risorsa di visualizzazione stencil profondità.
ms.assetid: 7d94d98b-7070-41ee-9a9d-fe848f8914f2
keywords:
- Metodo GetDepthStencil Direct3D 11
- Metodo GetDepthStencil Direct3D 11, interfaccia ID3DX11EffectDepthStencilViewVariable
- Interfaccia ID3DX11EffectDepthStencilViewVariable Direct3D 11, metodo GetDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49206f051922982ac77265e68fa3d7b7397d1348
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982448"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencil-method"></a><span data-ttu-id="4c026-106">Metodo ID3DX11EffectDepthStencilViewVariable:: GetDepthStencil</span><span class="sxs-lookup"><span data-stu-id="4c026-106">ID3DX11EffectDepthStencilViewVariable::GetDepthStencil method</span></span>

<span data-ttu-id="4c026-107">Ottenere una risorsa di visualizzazione stencil profondità.</span><span class="sxs-lookup"><span data-stu-id="4c026-107">Get a depth-stencil-view resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c026-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c026-108">Syntax</span></span>


```C++
HRESULT GetDepthStencil(
   ID3D11DepthStencilView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="4c026-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c026-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c026-110">*ppResource*</span><span class="sxs-lookup"><span data-stu-id="4c026-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="4c026-111">Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span><span class="sxs-lookup"><span data-stu-id="4c026-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span></span>

<span data-ttu-id="4c026-112">Indirizzo di un puntatore a un'interfaccia di visualizzazione stencil profondità.</span><span class="sxs-lookup"><span data-stu-id="4c026-112">The address of a pointer to a depth-stencil-view interface.</span></span> <span data-ttu-id="4c026-113">Vedere [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="4c026-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c026-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c026-114">Return value</span></span>

<span data-ttu-id="4c026-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4c026-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4c026-116">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4c026-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4c026-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c026-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4c026-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="4c026-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4c026-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="4c026-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4c026-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4c026-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4c026-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c026-121">Requirements</span></span>



| <span data-ttu-id="4c026-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c026-122">Requirement</span></span> | <span data-ttu-id="4c026-123">Valore</span><span class="sxs-lookup"><span data-stu-id="4c026-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c026-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c026-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4c026-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c026-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4c026-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="4c026-126">Library</span></span><br/> | <dl> <span data-ttu-id="4c026-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="4c026-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c026-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c026-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c026-129">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="4c026-129">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





