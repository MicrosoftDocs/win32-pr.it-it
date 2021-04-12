---
description: Termina una tecnica attiva.
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: 'Metodo ID3DXEffect:: end (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.End
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: baaccd7710845296497dcc7f16d3d71c7ceeb9bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355014"
---
# <a name="id3dxeffectend-method"></a><span data-ttu-id="2748f-103">Metodo ID3DXEffect:: end</span><span class="sxs-lookup"><span data-stu-id="2748f-103">ID3DXEffect::End method</span></span>

<span data-ttu-id="2748f-104">Termina una tecnica attiva.</span><span class="sxs-lookup"><span data-stu-id="2748f-104">Ends an active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="2748f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2748f-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="2748f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2748f-106">Parameters</span></span>

<span data-ttu-id="2748f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2748f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2748f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2748f-108">Return value</span></span>

<span data-ttu-id="2748f-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2748f-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2748f-110">Questo metodo restituisce sempre il valore S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2748f-110">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2748f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2748f-111">Remarks</span></span>

<span data-ttu-id="2748f-112">Tutto il rendering in un effetto viene eseguito all'interno di una coppia corrispondente di chiamate [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) e **ID3DXEffect:: end** .</span><span class="sxs-lookup"><span data-stu-id="2748f-112">All rendering in an effect is done within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and **ID3DXEffect::End** calls.</span></span> <span data-ttu-id="2748f-113">Una volta eseguito il rendering di tutti i passaggi, è necessario chiamare **ID3DXEffect:: end** per terminare la tecnica attiva.</span><span class="sxs-lookup"><span data-stu-id="2748f-113">After all passes are rendered, **ID3DXEffect::End** must be called to end the active technique.</span></span> <span data-ttu-id="2748f-114">Il sistema di effetto risponde usando il blocco di stato creato quando è stato chiamato **ID3DXEffect:: Begin** , per ripristinare automaticamente lo stato della pipeline prima di **ID3DXEffect:: Begin**.</span><span class="sxs-lookup"><span data-stu-id="2748f-114">The effect system responds by using the state block created when **ID3DXEffect::Begin** was called, to automatically restore the pipeline state before **ID3DXEffect::Begin**.</span></span>

<span data-ttu-id="2748f-115">Per impostazione predefinita, il sistema degli effetti gestisce il salvataggio dello stato prima di una tecnica e il ripristino dello stato dopo una tecnica.</span><span class="sxs-lookup"><span data-stu-id="2748f-115">By default, the effect system takes care of saving state prior to a technique, and restoring state after a technique.</span></span> <span data-ttu-id="2748f-116">Se si sceglie di disabilitare questa funzionalità di salvataggio e ripristino, vedere [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="2748f-116">If you choose to disable this save and restore functionality, see [D3DXFX\_DONOTSAVESAMPLERSTATE](d3dxfx.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2748f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2748f-117">Requirements</span></span>



| <span data-ttu-id="2748f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2748f-118">Requirement</span></span> | <span data-ttu-id="2748f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2748f-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2748f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2748f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2748f-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2748f-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2748f-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="2748f-122">Library</span></span><br/> | <dl> <span data-ttu-id="2748f-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2748f-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2748f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2748f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2748f-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="2748f-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




