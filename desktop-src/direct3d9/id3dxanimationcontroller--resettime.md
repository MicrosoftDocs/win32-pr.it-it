---
description: Reimposta il tempo di animazione globale su zero. Tutti gli eventi in sospeso manterranno le pianificazioni originali, ma nel nuovo intervallo di tempo.
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: 'Metodo ID3DXAnimationController:: ResetTime (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ResetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1206cc8514f3e7eb235f1072bf2a66c4b5bf1e7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762209"
---
# <a name="id3dxanimationcontrollerresettime-method"></a><span data-ttu-id="c1dc1-104">Metodo ID3DXAnimationController:: ResetTime</span><span class="sxs-lookup"><span data-stu-id="c1dc1-104">ID3DXAnimationController::ResetTime method</span></span>

<span data-ttu-id="c1dc1-105">Reimposta il tempo di animazione globale su zero.</span><span class="sxs-lookup"><span data-stu-id="c1dc1-105">Resets the global animation time to zero.</span></span> <span data-ttu-id="c1dc1-106">Tutti gli eventi in sospeso manterranno le pianificazioni originali, ma nel nuovo intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="c1dc1-106">Any pending events will retain their original schedules, but in the new timeframe.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1dc1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1dc1-107">Syntax</span></span>


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a><span data-ttu-id="c1dc1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1dc1-108">Parameters</span></span>

<span data-ttu-id="c1dc1-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c1dc1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1dc1-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1dc1-110">Return value</span></span>

<span data-ttu-id="c1dc1-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c1dc1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c1dc1-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c1dc1-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c1dc1-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c1dc1-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1dc1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1dc1-114">Remarks</span></span>

<span data-ttu-id="c1dc1-115">Questo metodo viene in genere utilizzato quando il valore del tempo di animazione globale è prossimo alla precisione massima della doppia archiviazione o 2 ⁶ ⁴-1.</span><span class="sxs-lookup"><span data-stu-id="c1dc1-115">This method is typically used when the global animation time value is nearing the maximum precision of DOUBLE storage, or 2⁶⁴ - 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1dc1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1dc1-116">Requirements</span></span>



| <span data-ttu-id="c1dc1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1dc1-117">Requirement</span></span> | <span data-ttu-id="c1dc1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c1dc1-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1dc1-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1dc1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c1dc1-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1dc1-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c1dc1-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="c1dc1-121">Library</span></span><br/> | <dl> <span data-ttu-id="c1dc1-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1dc1-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c1dc1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1dc1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1dc1-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="c1dc1-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




