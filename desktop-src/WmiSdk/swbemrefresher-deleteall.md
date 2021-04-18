---
description: Il metodo SWbemRefresher. DeleteAll rimuove tutti gli elementi dalla raccolta nell'oggetto SWbemRefresher. Oggetto SWbemRefresher.
ms.assetid: c6e462d3-52b3-40c0-9a9c-fa268415a5f0
ms.tgt_platform: multiple
title: Metodo SWbemRefresher. DeleteAll (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ddeb1c5fc8e7fb1f9c5682a2da0d9a1d6f53ba5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320584"
---
# <a name="swbemrefresherdeleteall-method"></a><span data-ttu-id="39114-103">SWbemRefresher. DeleteAll, metodo</span><span class="sxs-lookup"><span data-stu-id="39114-103">SWbemRefresher.DeleteAll method</span></span>

<span data-ttu-id="39114-104">Il metodo **SWbemRefresher. DeleteAll** rimuove tutti gli elementi dalla raccolta nell'oggetto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="39114-104">The **SWbemRefresher.DeleteAll** method removes all the items from the collection in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="39114-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="39114-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="39114-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39114-106">Syntax</span></span>


```VB
SWbemRefresher.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="39114-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="39114-107">Parameters</span></span>

<span data-ttu-id="39114-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="39114-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39114-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39114-109">Return value</span></span>

<span data-ttu-id="39114-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="39114-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39114-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="39114-111">Remarks</span></span>

<span data-ttu-id="39114-112">Il valore di [**SWbemRefreshableItem**](swbemrefreshableitem.md) corrispondente per ogni elemento rimosso ha la proprietà di [**aggiornamento**](swbemrefreshableitem-refresher.md) impostata su **null**, a indicare che non è più disponibile un aggiornamento padre.</span><span class="sxs-lookup"><span data-stu-id="39114-112">The corresponding [**SWbemRefreshableItem**](swbemrefreshableitem.md) for each removed item has its [**Refresher**](swbemrefreshableitem-refresher.md) property set to **NULL**, which indicates that it no longer has a parent refresher.</span></span>

## <a name="requirements"></a><span data-ttu-id="39114-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39114-113">Requirements</span></span>



| <span data-ttu-id="39114-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="39114-114">Requirement</span></span> | <span data-ttu-id="39114-115">Valore</span><span class="sxs-lookup"><span data-stu-id="39114-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39114-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39114-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39114-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39114-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39114-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39114-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39114-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39114-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39114-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39114-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="39114-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="39114-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="39114-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="39114-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="39114-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="39114-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="39114-124">DLL</span><span class="sxs-lookup"><span data-stu-id="39114-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39114-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39114-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="39114-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="39114-126">CLSID</span></span><br/>                    | <span data-ttu-id="39114-127">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="39114-127">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="39114-128">IID</span><span class="sxs-lookup"><span data-stu-id="39114-128">IID</span></span><br/>                      | <span data-ttu-id="39114-129">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="39114-129">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="39114-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39114-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39114-131">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="39114-131">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




