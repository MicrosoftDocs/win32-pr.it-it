---
title: Metodo IWMPDVD back
description: Il metodo back modifica la visualizzazione da un sottomenu al relativo menu padre.
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- Back metodo Windows Media Player
- Metodo back Media Player Windows, interfaccia IWMPDVD
- Interfaccia IWMPDVD Windows Media Player, metodo back
topic_type:
- apiref
api_name:
- IWMPDVD.back
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cd31cd6365843a6905760c4447ea679e15e70ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332450"
---
# <a name="iwmpdvdback-method"></a><span data-ttu-id="72b0c-106">Metodo IWMPDVD:: back</span><span class="sxs-lookup"><span data-stu-id="72b0c-106">IWMPDVD::back method</span></span>

<span data-ttu-id="72b0c-107">Il metodo **back** modifica la visualizzazione da un sottomenu al relativo menu padre.</span><span class="sxs-lookup"><span data-stu-id="72b0c-107">The **back** method changes the display from a submenu to its parent menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="72b0c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72b0c-108">Syntax</span></span>


```CSharp
public void back();
```


```VB

Public Sub back()
Implements IWMPDVD.back
```





## <a name="parameters"></a><span data-ttu-id="72b0c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="72b0c-109">Parameters</span></span>

<span data-ttu-id="72b0c-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="72b0c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72b0c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72b0c-111">Return value</span></span>

<span data-ttu-id="72b0c-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="72b0c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72b0c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="72b0c-113">Remarks</span></span>

<span data-ttu-id="72b0c-114">Ogni DVD viene creato in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="72b0c-114">Every DVD is authored differently.</span></span> <span data-ttu-id="72b0c-115">Alcuni DVD vengono creati in modo che il `back` metodo sia disponibile dal menu radice, ma quando viene richiamato, non eseguirà alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="72b0c-115">Some DVDs are authored so that the `back` method is available from the root menu, but when invoked, it will do nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="72b0c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72b0c-116">Requirements</span></span>



| <span data-ttu-id="72b0c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="72b0c-117">Requirement</span></span> | <span data-ttu-id="72b0c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="72b0c-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72b0c-119">Versione</span><span class="sxs-lookup"><span data-stu-id="72b0c-119">Version</span></span><br/>   | <span data-ttu-id="72b0c-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="72b0c-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="72b0c-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="72b0c-121">Namespace</span></span><br/> | <span data-ttu-id="72b0c-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="72b0c-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="72b0c-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="72b0c-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="72b0c-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="72b0c-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72b0c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72b0c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b0c-126">**Interfaccia IWMPDVD (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="72b0c-126">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





