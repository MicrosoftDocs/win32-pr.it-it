---
title: Metodo ID3DX11EffectConstantBuffer UndoSetConstantBuffer (D3dx11effect. h)
description: Ripristina un buffer costante impostato in precedenza.
ms.assetid: 6c5e1256-3a92-4bfe-8614-f09d627bc3db
keywords:
- Metodo UndoSetConstantBuffer Direct3D 11
- Metodo UndoSetConstantBuffer Direct3D 11, interfaccia ID3DX11EffectConstantBuffer
- Interfaccia ID3DX11EffectConstantBuffer Direct3D 11, metodo UndoSetConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.UndoSetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c95a26f1ea92d5bfe1975e3fe4dc1961046e5535
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104402010"
---
# <a name="id3dx11effectconstantbufferundosetconstantbuffer-method"></a><span data-ttu-id="61068-106">Metodo ID3DX11EffectConstantBuffer:: UndoSetConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="61068-106">ID3DX11EffectConstantBuffer::UndoSetConstantBuffer method</span></span>

<span data-ttu-id="61068-107">Ripristina un buffer costante impostato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="61068-107">Reverts a previously set constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="61068-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61068-108">Syntax</span></span>


```C++
HRESULT UndoSetConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="61068-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="61068-109">Parameters</span></span>

<span data-ttu-id="61068-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="61068-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="61068-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61068-111">Return value</span></span>

<span data-ttu-id="61068-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="61068-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="61068-113">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="61068-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="61068-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="61068-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="61068-115">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="61068-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="61068-116">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="61068-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="61068-117">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="61068-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="61068-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61068-118">Requirements</span></span>



| <span data-ttu-id="61068-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="61068-119">Requirement</span></span> | <span data-ttu-id="61068-120">Valore</span><span class="sxs-lookup"><span data-stu-id="61068-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61068-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61068-121">Header</span></span><br/>  | <dl> <span data-ttu-id="61068-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="61068-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="61068-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="61068-123">Library</span></span><br/> | <dl> <span data-ttu-id="61068-124"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="61068-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61068-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61068-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61068-126">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="61068-126">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





