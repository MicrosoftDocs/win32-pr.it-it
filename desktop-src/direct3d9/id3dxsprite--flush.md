---
description: "Impone l'invio di tutti gli sprite in batch al dispositivo. Gli Stati del dispositivo rimangono invariati dopo l'ultima chiamata a ID3DXSprite:: Begin. L'elenco degli sprite in batch viene quindi cancellato."
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: 'Metodo ID3DXSprite:: Flush (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Flush
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3bcd89984672f0dcfa2df120ede1abdfee23d171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322972"
---
# <a name="id3dxspriteflush-method"></a><span data-ttu-id="e0b98-105">Metodo ID3DXSprite:: Flush</span><span class="sxs-lookup"><span data-stu-id="e0b98-105">ID3DXSprite::Flush method</span></span>

<span data-ttu-id="e0b98-106">Impone l'invio di tutti gli sprite in batch al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e0b98-106">Forces all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="e0b98-107">Gli Stati del dispositivo rimangono invariati dopo l'ultima chiamata a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="e0b98-107">Device states remain as they were after the last call to [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span> <span data-ttu-id="e0b98-108">L'elenco degli sprite in batch viene quindi cancellato.</span><span class="sxs-lookup"><span data-stu-id="e0b98-108">The list of batched sprites is then cleared.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b98-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0b98-109">Syntax</span></span>


```C++
HRESULT Flush();
```



## <a name="parameters"></a><span data-ttu-id="e0b98-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0b98-110">Parameters</span></span>

<span data-ttu-id="e0b98-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e0b98-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0b98-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0b98-112">Return value</span></span>

<span data-ttu-id="e0b98-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0b98-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0b98-114">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e0b98-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e0b98-115">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="e0b98-115">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b98-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0b98-116">Requirements</span></span>



| <span data-ttu-id="e0b98-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0b98-117">Requirement</span></span> | <span data-ttu-id="e0b98-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e0b98-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b98-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0b98-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e0b98-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0b98-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e0b98-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="e0b98-121">Library</span></span><br/> | <dl> <span data-ttu-id="e0b98-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0b98-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e0b98-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0b98-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b98-124">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="e0b98-124">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="e0b98-125">**ID3DXSprite:: end**</span><span class="sxs-lookup"><span data-stu-id="e0b98-125">**ID3DXSprite::End**</span></span>](id3dxsprite--end.md)
</dt> </dl>

 

 




