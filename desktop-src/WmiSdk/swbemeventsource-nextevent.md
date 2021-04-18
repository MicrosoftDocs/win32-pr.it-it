---
description: Se è disponibile un evento, il metodo NextEvent dell'oggetto SWbemEventSource recupera l'evento da una query di eventi.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: Metodo SWbemEventSource. NextEvent (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 02fbc32557ab29c66849a4249d26cc2ca41564e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318516"
---
# <a name="swbemeventsourcenextevent-method"></a><span data-ttu-id="ec8e8-103">SWbemEventSource. NextEvent, metodo</span><span class="sxs-lookup"><span data-stu-id="ec8e8-103">SWbemEventSource.NextEvent method</span></span>

<span data-ttu-id="ec8e8-104">Se è disponibile un evento, il metodo **NextEvent** dell'oggetto [**SWbemEventSource**](swbemeventsource.md) recupera l'evento da una query di eventi.</span><span class="sxs-lookup"><span data-stu-id="ec8e8-104">If an event is available, the **NextEvent** method of the [**SWbemEventSource**](swbemeventsource.md) object retrieves the event from an event query.</span></span>

<span data-ttu-id="ec8e8-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ec8e8-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ec8e8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec8e8-106">Syntax</span></span>


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ec8e8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec8e8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec8e8-108">*iTimeoutMs* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ec8e8-108">*iTimeoutMs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec8e8-109">Numero di millisecondi di attesa della chiamata per un evento prima che venga restituito un errore di timeout.</span><span class="sxs-lookup"><span data-stu-id="ec8e8-109">Number of milliseconds the call waits for an event before returning a time-out error.</span></span> <span data-ttu-id="ec8e8-110">Il valore predefinito per questo parametro è **wbemTimeoutInfinite** (-1), che indirizza la chiamata a un'attesa indefinita.</span><span class="sxs-lookup"><span data-stu-id="ec8e8-110">The default value for this parameter is **wbemTimeoutInfinite** (-1), which directs the call to wait indefinitely.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec8e8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec8e8-111">Return value</span></span>

<span data-ttu-id="ec8e8-112">Se il metodo **NextEvent** ha esito positivo, restituisce un oggetto [**SWbemObject**](swbemobject.md) che contiene l'evento richiesto.</span><span class="sxs-lookup"><span data-stu-id="ec8e8-112">If the **NextEvent** method is successful, it returns an [**SWbemObject**](swbemobject.md) object that contains the requested event.</span></span> <span data-ttu-id="ec8e8-113">Se si verifica il timeout della chiamata, l'oggetto restituito è **null** e viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="ec8e8-113">If the call times out, the returned object is **NULL** and an error is raised.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ec8e8-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ec8e8-114">Error codes</span></span>

<span data-ttu-id="ec8e8-115">Al termine del metodo **NextEvent** , l'oggetto **Err** può contenere il codice di errore riportato nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="ec8e8-115">Upon the completion of the **NextEvent** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ec8e8-116">**wbemErrTimedOut** -0x80043001</span><span class="sxs-lookup"><span data-stu-id="ec8e8-116">**wbemErrTimedOut** - 0x80043001</span></span>
</dt> <dd>

<span data-ttu-id="ec8e8-117">L'evento richiesto non è arrivato nell'intervallo di tempo specificato in *iTimeoutMs.*</span><span class="sxs-lookup"><span data-stu-id="ec8e8-117">Requested event did not arrive in the amount of time specified in *iTimeoutMs.*</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec8e8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec8e8-118">Requirements</span></span>



| <span data-ttu-id="ec8e8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec8e8-119">Requirement</span></span> | <span data-ttu-id="ec8e8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ec8e8-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec8e8-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec8e8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ec8e8-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec8e8-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ec8e8-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec8e8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ec8e8-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec8e8-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ec8e8-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec8e8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec8e8-126"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec8e8-126"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec8e8-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ec8e8-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec8e8-128"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ec8e8-128"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ec8e8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ec8e8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec8e8-130"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec8e8-130"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec8e8-131">CLSID</span><span class="sxs-lookup"><span data-stu-id="ec8e8-131">CLSID</span></span><br/>                    | <span data-ttu-id="ec8e8-132">\_SWBEMEVENTSOURCE CLSID</span><span class="sxs-lookup"><span data-stu-id="ec8e8-132">CLSID\_SWbemEventSource</span></span><br/>                                                      |
| <span data-ttu-id="ec8e8-133">IID</span><span class="sxs-lookup"><span data-stu-id="ec8e8-133">IID</span></span><br/>                      | <span data-ttu-id="ec8e8-134">\_ISWBEMEVENTSOURCE IID</span><span class="sxs-lookup"><span data-stu-id="ec8e8-134">IID\_ISWbemEventSource</span></span><br/>                                                       |



 

 




