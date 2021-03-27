---
title: Metodo ID3DX11DataProcessor Destroy (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Elimina il processore dopo il completamento di un elemento di lavoro.
ms.assetid: 759641c0-ef86-42ee-88b9-3fcb7a171d86
keywords:
- Distruggi il metodo Direct3D 11
- Distruggi il metodo Direct3D 11, interfaccia ID3DX11DataProcessor
- Interfaccia ID3DX11DataProcessor Direct3D 11, metodo Destroy
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Destroy
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af92f8b3a22ba9a62258e8b24589a662eda22592
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886326"
---
# <a name="id3dx11dataprocessordestroy-method"></a><span data-ttu-id="537c1-107">ID3DX11DataProcessor::D Metodo estroy</span><span class="sxs-lookup"><span data-stu-id="537c1-107">ID3DX11DataProcessor::Destroy method</span></span>

> [!Note]  
> <span data-ttu-id="537c1-108">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="537c1-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="537c1-109">Elimina il processore dopo il completamento di un elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="537c1-109">Destroys the processor after a work item completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="537c1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="537c1-110">Syntax</span></span>


```C++
HRESULT Destroy();
```



## <a name="parameters"></a><span data-ttu-id="537c1-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="537c1-111">Parameters</span></span>

<span data-ttu-id="537c1-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="537c1-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="537c1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="537c1-113">Return value</span></span>

<span data-ttu-id="537c1-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="537c1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="537c1-115">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="537c1-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="537c1-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="537c1-116">Remarks</span></span>

<span data-ttu-id="537c1-117">Questo metodo viene utilizzato da un' [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="537c1-117">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="537c1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="537c1-118">Requirements</span></span>



| <span data-ttu-id="537c1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="537c1-119">Requirement</span></span> | <span data-ttu-id="537c1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="537c1-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="537c1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="537c1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="537c1-122"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="537c1-122"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="537c1-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="537c1-123">Library</span></span><br/> | <dl> <span data-ttu-id="537c1-124"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="537c1-124"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="537c1-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="537c1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="537c1-126">ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="537c1-126">ID3DX11DataProcessor</span></span>](id3dx11dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="537c1-127">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="537c1-127">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





