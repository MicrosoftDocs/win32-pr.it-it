---
description: "Forzare l'invio di tutti gli sprite in batch al dispositivo. Gli Stati del dispositivo rimangono invariati dopo l'ultima chiamata a ID3DX10Sprite:: Begin. L'elenco degli sprite in batch viene quindi cancellato."
ms.assetid: ae03e17c-1a14-4a41-a9a9-8757d2f7a81d
title: 'Metodo ID3DX10Sprite:: Flush (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Flush
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 748be56a7b89223db1957b9c0144143edd90ee4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323744"
---
# <a name="id3dx10spriteflush-method"></a><span data-ttu-id="e827d-105">Metodo ID3DX10Sprite:: Flush</span><span class="sxs-lookup"><span data-stu-id="e827d-105">ID3DX10Sprite::Flush method</span></span>

<span data-ttu-id="e827d-106">Forzare l'invio di tutti gli sprite in batch al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e827d-106">Force all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="e827d-107">Gli Stati del dispositivo rimangono invariati dopo l'ultima chiamata a ID3DX10Sprite:: Begin.</span><span class="sxs-lookup"><span data-stu-id="e827d-107">Device states remain as they were after the last call to ID3DX10Sprite::Begin.</span></span> <span data-ttu-id="e827d-108">L'elenco degli sprite in batch viene quindi cancellato.</span><span class="sxs-lookup"><span data-stu-id="e827d-108">The list of batched sprites is then cleared.</span></span>

## <a name="syntax"></a><span data-ttu-id="e827d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e827d-109">Syntax</span></span>


```C++
HRESULT Flush();
```



## <a name="parameters"></a><span data-ttu-id="e827d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e827d-110">Parameters</span></span>

<span data-ttu-id="e827d-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e827d-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e827d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e827d-112">Return value</span></span>

<span data-ttu-id="e827d-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e827d-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e827d-114">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e827d-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e827d-115">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e827d-115">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e827d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e827d-116">Requirements</span></span>



| <span data-ttu-id="e827d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e827d-117">Requirement</span></span> | <span data-ttu-id="e827d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e827d-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e827d-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e827d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e827d-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e827d-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e827d-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="e827d-121">Library</span></span><br/> | <dl> <span data-ttu-id="e827d-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e827d-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e827d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e827d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e827d-124">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="e827d-124">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="e827d-125">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="e827d-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




