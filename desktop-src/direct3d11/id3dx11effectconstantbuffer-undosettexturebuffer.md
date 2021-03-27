---
title: Metodo ID3DX11EffectConstantBuffer UndoSetTextureBuffer (D3dx11effect. h)
description: Ripristina un buffer di trama impostato in precedenza.
ms.assetid: 982e7899-9569-4611-9fe0-b78624acba2c
keywords:
- Metodo UndoSetTextureBuffer Direct3D 11
- Metodo UndoSetTextureBuffer Direct3D 11, interfaccia ID3DX11EffectConstantBuffer
- Interfaccia ID3DX11EffectConstantBuffer Direct3D 11, metodo UndoSetTextureBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.UndoSetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5e1e1b2be167466da5a4d92999646bb7c8f225
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355259"
---
# <a name="id3dx11effectconstantbufferundosettexturebuffer-method"></a><span data-ttu-id="029a9-106">Metodo ID3DX11EffectConstantBuffer:: UndoSetTextureBuffer</span><span class="sxs-lookup"><span data-stu-id="029a9-106">ID3DX11EffectConstantBuffer::UndoSetTextureBuffer method</span></span>

<span data-ttu-id="029a9-107">Ripristina un buffer di trama impostato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="029a9-107">Reverts a previously set texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="029a9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="029a9-108">Syntax</span></span>


```C++
HRESULT UndoSetTextureBuffer();
```



## <a name="parameters"></a><span data-ttu-id="029a9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="029a9-109">Parameters</span></span>

<span data-ttu-id="029a9-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="029a9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="029a9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="029a9-111">Return value</span></span>

<span data-ttu-id="029a9-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="029a9-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="029a9-113">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="029a9-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="029a9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="029a9-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="029a9-115">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="029a9-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="029a9-116">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="029a9-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="029a9-117">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="029a9-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="029a9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="029a9-118">Requirements</span></span>



| <span data-ttu-id="029a9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="029a9-119">Requirement</span></span> | <span data-ttu-id="029a9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="029a9-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="029a9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="029a9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="029a9-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="029a9-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="029a9-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="029a9-123">Library</span></span><br/> | <dl> <span data-ttu-id="029a9-124"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="029a9-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="029a9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="029a9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="029a9-126">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="029a9-126">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





