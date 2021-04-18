---
description: L'evento OnProgress di SWbemSink viene attivato quando una chiamata asincrona restituisce lo stato di una chiamata in corso.
ms.assetid: abb43916-f952-41fe-a5ba-0428864c0685
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnProgress (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnProgress
- ISWbemSinkEvents.OnProgress
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d322309adcfad33b1c303d7efd6af28db1cac80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318858"
---
# <a name="iswbemsinkeventsonprogress-event"></a><span data-ttu-id="a6b53-103">Evento ISWbemSinkEvents:: OnProgress</span><span class="sxs-lookup"><span data-stu-id="a6b53-103">ISWbemSinkEvents::OnProgress event</span></span>

<span data-ttu-id="a6b53-104">L'evento **OnProgress** di [**SWbemSink**](swbemsink.md) viene attivato quando una chiamata asincrona restituisce lo stato di una chiamata in corso.</span><span class="sxs-lookup"><span data-stu-id="a6b53-104">The **OnProgress** event of [**SWbemSink**](swbemsink.md) is triggered when an asynchronous call returns the status of a call that is in progress.</span></span> <span data-ttu-id="a6b53-105">Se gli eventi, le istanze o le classi vengono prodotti da un provider che supporta gli aggiornamenti di stato, è possibile inserire il codice in questo evento per fornire agli utenti feedback sullo stato di un'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="a6b53-105">If the events, instances, or classes are produced from a provider that supports status updates, you can place code in this event to provide users with feedback about the status of an asynchronous operation.</span></span> <span data-ttu-id="a6b53-106">Se si desidera ricevere gli aggiornamenti di stato, è necessario impostare il parametro *iFlags* della chiamata asincrona su **wbemFlagSendStatus** (128/0x80). in caso contrario, questo evento non viene attivato.</span><span class="sxs-lookup"><span data-stu-id="a6b53-106">You must set the *iFlags* parameter of the asynchronous call to **wbemFlagSendStatus** (128/0x80) if you want to receive status updates, otherwise this event is not triggered.</span></span>

<span data-ttu-id="a6b53-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a6b53-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a6b53-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6b53-108">Syntax</span></span>


```VB
SWbemSink.OnProgress( _
  ByVal iUpperBound, _
  ByVal iCurrent, _
  ByVal strMessage, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="a6b53-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6b53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6b53-110">*iUpperBound*</span><span class="sxs-lookup"><span data-stu-id="a6b53-110">*iUpperBound*</span></span> 
</dt> <dd>

<span data-ttu-id="a6b53-111">Intero che descrive il numero totale di attività da completare.</span><span class="sxs-lookup"><span data-stu-id="a6b53-111">Integer that describes the total number of tasks to complete.</span></span>

</dd> <dt>

<span data-ttu-id="a6b53-112">*iCurrent*</span><span class="sxs-lookup"><span data-stu-id="a6b53-112">*iCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="a6b53-113">Elemento corrente in fase di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="a6b53-113">Current item that is being processed.</span></span>

</dd> <dt>

<span data-ttu-id="a6b53-114">*strMessage*</span><span class="sxs-lookup"><span data-stu-id="a6b53-114">*strMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="a6b53-115">Messaggio che descrive lo stato dell'attività corrente.</span><span class="sxs-lookup"><span data-stu-id="a6b53-115">Message that describes the status of the current task.</span></span>

</dd> <dt>

<span data-ttu-id="a6b53-116">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="a6b53-116">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="a6b53-117">Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) passato alla chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="a6b53-117">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="a6b53-118">Utilizzare questo parametro per identificare l'origine della chiamata asincrona che attiva questo evento quando vengono effettuate più chiamate asincrone utilizzando questo sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="a6b53-118">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6b53-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a6b53-119">Return value</span></span>

<span data-ttu-id="a6b53-120">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a6b53-120">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a6b53-121">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a6b53-121">Error codes</span></span>

<span data-ttu-id="a6b53-122">Al termine dell'evento **OnProgress** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="a6b53-122">After the completion of the **OnProgress** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="a6b53-123">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a6b53-123">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a6b53-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="a6b53-124">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="a6b53-125">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="a6b53-125">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="a6b53-126">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="a6b53-126">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a6b53-127">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="a6b53-127">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="a6b53-128">Si è verificato un errore di rete, che impedisce il normale funzionamento.</span><span class="sxs-lookup"><span data-stu-id="a6b53-128">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6b53-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="a6b53-129">Remarks</span></span>

<span data-ttu-id="a6b53-130">L'evento **OnProgress** viene attivato quando una chiamata asincrona restituisce lo stato di una chiamata in corso.</span><span class="sxs-lookup"><span data-stu-id="a6b53-130">The **OnProgress** event is triggered when an asynchronous call returns the status of a call that is in progress.</span></span> <span data-ttu-id="a6b53-131">Se gli eventi, le istanze o le classi vengono prodotti da un provider che supporta gli aggiornamenti di stato, è possibile inserire il codice in questo evento per fornire agli utenti il feedback sullo stato di un'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="a6b53-131">If the events, instances, or classes are produced from a provider that supports status updates, you can place code in this event to give users feedback about the status of an asynchronous operation.</span></span>

> [!Note]  
> <span data-ttu-id="a6b53-132">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="a6b53-132">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="a6b53-133">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="a6b53-133">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="a6b53-134">Per eliminare i rischi, usare la comunicazione semi-sincrona o sincrona.</span><span class="sxs-lookup"><span data-stu-id="a6b53-134">To eliminate the risks, use semi-synchronous or synchronous communication.</span></span> <span data-ttu-id="a6b53-135">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="a6b53-135">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a6b53-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6b53-136">Requirements</span></span>



| <span data-ttu-id="a6b53-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6b53-137">Requirement</span></span> | <span data-ttu-id="a6b53-138">Valore</span><span class="sxs-lookup"><span data-stu-id="a6b53-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6b53-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6b53-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a6b53-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6b53-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a6b53-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6b53-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a6b53-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6b53-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a6b53-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6b53-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6b53-144"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6b53-144"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6b53-145">IDL</span><span class="sxs-lookup"><span data-stu-id="a6b53-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a6b53-146"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6b53-146"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="a6b53-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a6b53-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6b53-148"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6b53-148"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a6b53-149">CLSID</span><span class="sxs-lookup"><span data-stu-id="a6b53-149">CLSID</span></span><br/>                    | <span data-ttu-id="a6b53-150">\_SWBEMSINK CLSID</span><span class="sxs-lookup"><span data-stu-id="a6b53-150">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="a6b53-151">IID</span><span class="sxs-lookup"><span data-stu-id="a6b53-151">IID</span></span><br/>                      | <span data-ttu-id="a6b53-152">\_ISWBEMSINKEVENTS IID</span><span class="sxs-lookup"><span data-stu-id="a6b53-152">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="a6b53-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6b53-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6b53-154">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="a6b53-154">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

