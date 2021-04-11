---
description: L'evento OnObjectReady di un oggetto SWbemSink viene attivato quando un'operazione asincrona restituisce un oggetto.
ms.assetid: 14110ee7-a808-4786-b695-2ce54189d826
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnObjectReady (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectReady
- ISWbemSinkEvents.OnObjectReady
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1fa803339e7007a030881c3d5b47d67f354b5661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130962"
---
# <a name="iswbemsinkeventsonobjectready-event"></a><span data-ttu-id="42d0e-103">Evento ISWbemSinkEvents:: OnObjectReady</span><span class="sxs-lookup"><span data-stu-id="42d0e-103">ISWbemSinkEvents::OnObjectReady event</span></span>

<span data-ttu-id="42d0e-104">L'evento **OnObjectReady** di un oggetto [**SWbemSink**](swbemsink.md) viene attivato quando un'operazione asincrona restituisce un oggetto.</span><span class="sxs-lookup"><span data-stu-id="42d0e-104">The **OnObjectReady** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous operation returns an object.</span></span> <span data-ttu-id="42d0e-105">Utilizzare questo evento per elaborare oggetti da chiamate asincrone, ad esempio [**SWbemObject. \_ InstancesAsync**](swbemobject-instancesasync-.md) o [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="42d0e-105">Use this event to process objects from asynchronous calls such as [**SWbemObject.InstancesAsync\_**](swbemobject-instancesasync-.md) or [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md).</span></span> <span data-ttu-id="42d0e-106">**OnObjectReady** restituisce un [**SWbemObject**](swbemobject.md) ogni volta fino al completamento dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="42d0e-106">**OnObjectReady** returns one [**SWbemObject**](swbemobject.md) each time until the enumeration is complete.</span></span>

<span data-ttu-id="42d0e-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="42d0e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="42d0e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42d0e-108">Syntax</span></span>


```VB
SWbemSink.OnObjectReady( _
  ByVal objWbemObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="42d0e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="42d0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42d0e-110">*objWbemObject*</span><span class="sxs-lookup"><span data-stu-id="42d0e-110">*objWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="42d0e-111">Oggetto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="42d0e-111">An [**SWbemObject**](swbemobject.md) object.</span></span> <span data-ttu-id="42d0e-112">Questa operazione è simile a quella restituita dall'equivalente sincrono della chiamata asincrona che attiva questo evento.</span><span class="sxs-lookup"><span data-stu-id="42d0e-112">This is similar to what is returned by the synchronous equivalent of the asynchronous call that triggers this event.</span></span> <span data-ttu-id="42d0e-113">Ad esempio, una chiamata al metodo [**SWbemServices. GetAsync**](swbemservices-getasync.md) restituisce un **SWbemObject** nel parametro *objWbemObject* dell'evento **OnObjectReady** dell'oggetto [**SWbemSink**](swbemsink.md) , che viene passato come parametro *objWbemObject* della chiamata originale.</span><span class="sxs-lookup"><span data-stu-id="42d0e-113">For example, a call to the [**SWbemServices.GetAsync**](swbemservices-getasync.md) method returns an **SWbemObject** in the *objWbemObject* parameter of the **OnObjectReady** event of the [**SWbemSink**](swbemsink.md) object, which is passed as the *objWbemObject* parameter of the original call.</span></span> <span data-ttu-id="42d0e-114">È possibile ottenere lo stesso oggetto **SWbemObject** utilizzando una chiamata sincrona equivalente a [**SWbemServices. Get**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="42d0e-114">The same **SWbemObject** object can be obtained by using an equivalent synchronous call to [**SWbemServices.Get**](swbemservices-get.md).</span></span>

</dd> <dt>

<span data-ttu-id="42d0e-115">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="42d0e-115">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="42d0e-116">Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) passato alla chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="42d0e-116">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="42d0e-117">Utilizzare questo parametro per identificare l'origine della chiamata asincrona che attiva questo evento quando vengono effettuate più chiamate asincrone utilizzando questo sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="42d0e-117">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42d0e-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42d0e-118">Return value</span></span>

<span data-ttu-id="42d0e-119">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="42d0e-119">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="42d0e-120">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="42d0e-120">Error codes</span></span>

<span data-ttu-id="42d0e-121">Al termine dell'evento **OnObjectReady** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="42d0e-121">After the completion of the **OnObjectReady** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="42d0e-122">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="42d0e-122">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="42d0e-123">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="42d0e-123">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="42d0e-124">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="42d0e-124">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="42d0e-125">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="42d0e-125">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="42d0e-126">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="42d0e-126">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="42d0e-127">Si è verificato un errore di rete, che impedisce il normale funzionamento.</span><span class="sxs-lookup"><span data-stu-id="42d0e-127">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42d0e-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="42d0e-128">Remarks</span></span>

<span data-ttu-id="42d0e-129">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="42d0e-129">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="42d0e-130">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="42d0e-130">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="42d0e-131">Per eliminare i rischi, usare la comunicazione semi-sincrona o la comunicazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="42d0e-131">To eliminate the risks, use either semi-synchronous communication or synchronous communication.</span></span> <span data-ttu-id="42d0e-132">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="42d0e-132">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42d0e-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42d0e-133">Requirements</span></span>



| <span data-ttu-id="42d0e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="42d0e-134">Requirement</span></span> | <span data-ttu-id="42d0e-135">Valore</span><span class="sxs-lookup"><span data-stu-id="42d0e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42d0e-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42d0e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="42d0e-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42d0e-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="42d0e-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42d0e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="42d0e-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42d0e-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="42d0e-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42d0e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="42d0e-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="42d0e-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="42d0e-142">IDL</span><span class="sxs-lookup"><span data-stu-id="42d0e-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42d0e-143"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42d0e-143"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="42d0e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="42d0e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42d0e-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42d0e-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="42d0e-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="42d0e-146">CLSID</span></span><br/>                    | <span data-ttu-id="42d0e-147">\_SWBEMSINK CLSID</span><span class="sxs-lookup"><span data-stu-id="42d0e-147">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="42d0e-148">IID</span><span class="sxs-lookup"><span data-stu-id="42d0e-148">IID</span></span><br/>                      | <span data-ttu-id="42d0e-149">\_ISWBEMSINKEVENTS IID</span><span class="sxs-lookup"><span data-stu-id="42d0e-149">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="42d0e-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42d0e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d0e-151">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="42d0e-151">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

