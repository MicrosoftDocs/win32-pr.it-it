---
title: Metodo ID3DX11DataLoader Destroy (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Elimina il caricatore dopo il completamento di un elemento di lavoro.
ms.assetid: 5d86c4ad-3eb6-421f-bb77-c88e8f5b42bb
keywords:
- Distruggi il metodo Direct3D 11
- Distruggi il metodo Direct3D 11, interfaccia ID3DX11DataLoader
- Interfaccia ID3DX11DataLoader Direct3D 11, metodo Destroy
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Destroy
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c3a1c6511a00d66704c104b3b69150a8509e41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982611"
---
# <a name="id3dx11dataloaderdestroy-method"></a><span data-ttu-id="d8516-107">ID3DX11DataLoader::D Metodo estroy</span><span class="sxs-lookup"><span data-stu-id="d8516-107">ID3DX11DataLoader::Destroy method</span></span>

> [!Note]  
> <span data-ttu-id="d8516-108">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="d8516-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="d8516-109">Elimina il caricatore dopo il completamento di un elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d8516-109">Destroys the loader after a work item completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8516-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8516-110">Syntax</span></span>


```C++
HRESULT Destroy();
```



## <a name="parameters"></a><span data-ttu-id="d8516-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8516-111">Parameters</span></span>

<span data-ttu-id="d8516-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d8516-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8516-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8516-113">Return value</span></span>

<span data-ttu-id="d8516-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d8516-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d8516-115">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d8516-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8516-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8516-116">Remarks</span></span>

<span data-ttu-id="d8516-117">Questo metodo viene utilizzato da un' [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="d8516-117">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8516-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8516-118">Requirements</span></span>



| <span data-ttu-id="d8516-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8516-119">Requirement</span></span> | <span data-ttu-id="d8516-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d8516-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8516-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8516-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d8516-122"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8516-122"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="d8516-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="d8516-123">Library</span></span><br/> | <dl> <span data-ttu-id="d8516-124"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8516-124"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d8516-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8516-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8516-126">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="d8516-126">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="d8516-127">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="d8516-127">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





