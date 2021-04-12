---
description: Il \_ metodo ExecMethodAsync di SWbemObject esegue in modo asincrono un metodo esportato da un provider di metodi.
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: Metodo SWbemObject.ExecMethodAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8af1b7c10eed427423afea8b40a1df5bc237f99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233673"
---
# <a name="swbemobjectexecmethodasync_-method"></a><span data-ttu-id="2c895-103">Metodo cMethodAsync SWbemObject.Exe\_</span><span class="sxs-lookup"><span data-stu-id="2c895-103">SWbemObject.ExecMethodAsync\_ method</span></span>

<span data-ttu-id="2c895-104">Il **metodo \_ ExecMethodAsync** di [**SWbemObject**](swbemobject.md) esegue in modo asincrono un metodo esportato da un provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="2c895-104">The **ExecMethodAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously executes a method that a method provider exports.</span></span> <span data-ttu-id="2c895-105">Questo metodo è simile a [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), ma opera direttamente sull'oggetto del metodo da eseguire.</span><span class="sxs-lookup"><span data-stu-id="2c895-105">This method is similar to [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), but operates directly on the object of the method to be executed.</span></span> <span data-ttu-id="2c895-106">Strumentazione gestione Windows (WMI) non implementa questo metodo.</span><span class="sxs-lookup"><span data-stu-id="2c895-106">Windows Management Instrumentation (WMI) does not implement this method.</span></span> <span data-ttu-id="2c895-107">Il provider implementa questo metodo.</span><span class="sxs-lookup"><span data-stu-id="2c895-107">The provider implements this method.</span></span>

<span data-ttu-id="2c895-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2c895-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c895-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c895-109">Syntax</span></span>


```VB
objOutParams = .ExecMethodAsync_( _
  ByVal objWbemSink, _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2c895-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c895-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c895-111">*objWbemSink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c895-111">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c895-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c895-112">Required.</span></span> <span data-ttu-id="2c895-113">Si tratta del sink di oggetto che riceve i risultati della chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="2c895-113">This is the object sink that receives the results of the method call.</span></span> <span data-ttu-id="2c895-114">I parametri in uscita vengono inviati all'evento [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) del sink di oggetto fornito.</span><span class="sxs-lookup"><span data-stu-id="2c895-114">The outbound parameters are sent to the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event of the supplied object sink.</span></span> <span data-ttu-id="2c895-115">I risultati del meccanismo di chiamata vengono inviati all'evento [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) del sink di oggetto fornito.</span><span class="sxs-lookup"><span data-stu-id="2c895-115">The results of the call mechanism are sent to the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the supplied object sink.</span></span> <span data-ttu-id="2c895-116">Si noti che **SWbemSink. OnCompleted** non riceve il codice restituito del metodo.</span><span class="sxs-lookup"><span data-stu-id="2c895-116">Notice that **SWbemSink.OnCompleted** does not receive the return code of the method.</span></span> <span data-ttu-id="2c895-117">Tuttavia, riceve il codice restituito del meccanismo effettivo di restituzione della chiamata ed è utile solo per verificare se la chiamata è stata eseguita o che non è riuscita per motivi meccanici.</span><span class="sxs-lookup"><span data-stu-id="2c895-117">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred, or that it failed for mechanical reasons.</span></span> <span data-ttu-id="2c895-118">Il codice risultato restituito dal metodo viene restituito nell'oggetto parametro in uscita fornito a **SWbemSink. OnObjectReady**.</span><span class="sxs-lookup"><span data-stu-id="2c895-118">The result code returned from the method is returned in the outbound parameter object supplied to **SWbemSink.OnObjectReady**.</span></span> <span data-ttu-id="2c895-119">Se viene restituito un codice di errore, l'oggetto [**IWbemObjectSink**](iwbemobjectsink.md) specificato non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="2c895-119">If any error code returns, then the supplied [**IWbemObjectSink**](iwbemobjectsink.md) object is not used.</span></span> <span data-ttu-id="2c895-120">Se la chiamata ha esito positivo, viene chiamata l'implementazione **IWbemObjectSink** dell'utente per indicare il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2c895-120">If the call is successful, then the user's **IWbemObjectSink** implementation is called to indicate the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2c895-121">*strMethodName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c895-121">*strMethodName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c895-122">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c895-122">Required.</span></span> <span data-ttu-id="2c895-123">Si tratta del nome del metodo per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2c895-123">This is the name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="2c895-124">*objwbemInParams* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2c895-124">*objwbemInParams* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2c895-125">Si tratta di un oggetto [**SWbemObject**](swbemobject.md) che contiene i parametri di input per il metodo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2c895-125">This is an [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="2c895-126">Per impostazione predefinita, questo parametro non è definito.</span><span class="sxs-lookup"><span data-stu-id="2c895-126">By default, this parameter is undefined.</span></span> <span data-ttu-id="2c895-127">Per altre informazioni, vedere [creazione di oggetti InParameters](constructing-inparameters-objects.md) e [analisi di oggetti OutParameters](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2c895-127">For more information, see [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c895-128">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2c895-128">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2c895-129">Integer che determina il comportamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="2c895-129">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="2c895-130">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2c895-130">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="2c895-131"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="2c895-131"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="2c895-132">Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**SWbemSink. OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2c895-132">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="2c895-133"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="2c895-133"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2c895-134">Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2c895-134">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2c895-135">*objwbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2c895-135">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2c895-136">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="2c895-136">Typically, it is undefined.</span></span> <span data-ttu-id="2c895-137">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="2c895-137">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="2c895-138">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="2c895-138">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="2c895-139">*objWbemAsyncContext* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2c895-139">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2c895-140">Si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="2c895-140">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="2c895-141">Utilizzare questo parametro se si eseguono più chiamate asincrone utilizzando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="2c895-141">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="2c895-142">Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando.</span><span class="sxs-lookup"><span data-stu-id="2c895-142">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="2c895-143">Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="2c895-143">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="2c895-144">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="2c895-144">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c895-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c895-145">Return value</span></span>

<span data-ttu-id="2c895-146">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2c895-146">This method has no return values.</span></span> <span data-ttu-id="2c895-147">Se la chiamata ha esito positivo, viene fornito un oggetto [**OutParameters**](swbemmethod-outparameters.md) , che è anche un oggetto [**SWbemObject**](swbemobject.md) , al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="2c895-147">If the call is successful, an [**OutParameters**](swbemmethod-outparameters.md) object, which is also an [**SWbemObject**](swbemobject.md) object, is supplied to the sink specified in *objWbemSink*.</span></span> <span data-ttu-id="2c895-148">L'oggetto **OutParameters** restituito contiene i parametri di output e il valore restituito per il metodo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2c895-148">The returned **OutParameters** object contains the output parameters and return value for the method being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2c895-149">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2c895-149">Error codes</span></span>

<span data-ttu-id="2c895-150">Dopo il completamento del **metodo \_ ExecMethodAsync** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="2c895-150">After completion of the **ExecMethodAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="2c895-151">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="2c895-151">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2c895-152">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="2c895-152">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="2c895-153">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="2c895-153">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="2c895-154">La classe specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="2c895-154">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2c895-155">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="2c895-155">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="2c895-156">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="2c895-156">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2c895-157">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="2c895-157">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="2c895-158">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="2c895-158">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2c895-159">**wbemErrInvalidMethod** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="2c895-159">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="2c895-160">Il metodo richiesto non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="2c895-160">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="2c895-161">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="2c895-161">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="2c895-162">L'utente corrente non è autorizzato a eseguire il metodo.</span><span class="sxs-lookup"><span data-stu-id="2c895-162">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c895-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c895-163">Remarks</span></span>

<span data-ttu-id="2c895-164">Usare il metodo **SWbemObject.Exe\_ cMethodAsync** come alternativa all'accesso diretto per l'esecuzione di un [*metodo del provider*](gloss-p.md) quando non è possibile eseguire direttamente un metodo.</span><span class="sxs-lookup"><span data-stu-id="2c895-164">Use the **SWbemObject.ExecMethodAsync\_** method as an alternative to direct access for executing a [*provider method*](gloss-p.md) when you cannot execute a method directly.</span></span> <span data-ttu-id="2c895-165">Se, ad esempio, il metodo presenta parametri out, utilizzare il metodo **SWbemObject.ExecMethodAsync \_** con un linguaggio di scripting che non supporta i parametri di output.</span><span class="sxs-lookup"><span data-stu-id="2c895-165">For example, if your method has out parameters, use the **SWbemObject.ExecMethodAsync\_** method with a scripting language that does not support output parameters.</span></span> <span data-ttu-id="2c895-166">In caso contrario, è consigliabile richiamare un metodo utilizzando l'accesso diretto.</span><span class="sxs-lookup"><span data-stu-id="2c895-166">Otherwise, it is recommended that you invoke a method using direct access.</span></span> <span data-ttu-id="2c895-167">Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="2c895-167">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="2c895-168">Questa chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="2c895-168">This call returns immediately.</span></span> <span data-ttu-id="2c895-169">Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="2c895-169">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="2c895-170">Per elaborare ogni oggetto all'arrivo, creare un *objWbemSink*. Subroutine dell'evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="2c895-170">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="2c895-171">Dopo la restituzione di tutti gli oggetti, è possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="2c895-171">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="2c895-172">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="2c895-172">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="2c895-173">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2c895-173">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="2c895-174">Per eliminare i rischi, usare la comunicazione semisincrono o la comunicazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="2c895-174">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="2c895-175">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="2c895-175">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="2c895-176">Se il metodo in esecuzione dispone di parametri di input, è necessario costruire l'oggetto [**InParameters**](swbemmethod-inparameters.md) e il parametro *objWbemInParam* come descritto in [creazione di oggetti InParameters](constructing-inparameters-objects.md) e [analisi degli oggetti OutParameters](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2c895-176">If the method being executed has input parameters, the [**InParameters**](swbemmethod-inparameters.md) object and *objWbemInParam* parameter must be constructed as described in [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="2c895-177">Il **SWbemObject.Exemetodo \_ cMethodAsync** presuppone che l'oggetto rappresentato da [**SWbemObject**](swbemobject.md) contenga il metodo da eseguire.</span><span class="sxs-lookup"><span data-stu-id="2c895-177">The **SWbemObject.ExecMethodAsync\_** method assumes the object represented by [**SWbemObject**](swbemobject.md) contains the method to execute.</span></span> <span data-ttu-id="2c895-178">Il [**SWbemServices.Exemetodo cMethodAsync**](swbemservices-execmethodasync.md) richiede un percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2c895-178">The [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) method requires an object path.</span></span>

## <a name="examples"></a><span data-ttu-id="2c895-179">Esempio</span><span class="sxs-lookup"><span data-stu-id="2c895-179">Examples</span></span>

<span data-ttu-id="2c895-180">Nell'esempio seguente viene illustrato il metodo [**ExecMethodAsync**](swbemservices-execmethodasync.md) .</span><span class="sxs-lookup"><span data-stu-id="2c895-180">The following example shows the [**ExecMethodAsync**](swbemservices-execmethodasync.md) method.</span></span> <span data-ttu-id="2c895-181">Lo script crea un [**oggetto \_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) che rappresenta un processo che esegue blocco note.</span><span class="sxs-lookup"><span data-stu-id="2c895-181">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="2c895-182">Viene illustrata la configurazione dell'oggetto [**InParameters**](swbemmethod-inparameters.md) e come ottenere risultati da un oggetto [**OutParameters**](swbemmethod-outparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="2c895-182">It shows setting up of [**InParameters**](swbemmethod-inparameters.md) object, and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span>

<span data-ttu-id="2c895-183">Per uno script che mostra le stesse operazioni eseguite in modo sincrono, vedere [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="2c895-183">For a script that shows the same operations performed synchronously, see [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span> <span data-ttu-id="2c895-184">Per un esempio di utilizzo dell'accesso diretto, vedere [**creare un metodo nella classe \_ processo Win32**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="2c895-184">For an example using direct access, see [**Create Method in Class Win32\_Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="2c895-185">Per un esempio della stessa operazione usando un oggetto [**SWbemServices**](swbemservices.md) , vedere [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span><span class="sxs-lookup"><span data-stu-id="2c895-185">For an example of the same operation using an [**SWbemServices**](swbemservices.md) object, see [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span></span>


```VB
On Error Resume Next

'Get a Win32_Process class description
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"

' Create a sink to receive event resulting
' from the ExecMethodAsync call.
Set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink", "Sink_")

' Call the Win32_Process.Create method asynchronously. Set up a 
' wait so the results of the method execution can be returned to 
' the sink subroutines.
bDone = false

' Call SWbemObject.ExecMethodAsync on the oProcess object.
oProcess.ExecMethodAsync_ Sink, "Create", oInParams, 0 
' 
while not bDone
    wscript.sleep 1000
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _
    & VBNewLine & "ReturnValue = " _
    & oOutParams.ReturnValue & VBNewLine & _
    "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
    & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a><span data-ttu-id="2c895-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c895-186">Requirements</span></span>



| <span data-ttu-id="2c895-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c895-187">Requirement</span></span> | <span data-ttu-id="2c895-188">Valore</span><span class="sxs-lookup"><span data-stu-id="2c895-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c895-189">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c895-189">Minimum supported client</span></span><br/> | <span data-ttu-id="2c895-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c895-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c895-191">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c895-191">Minimum supported server</span></span><br/> | <span data-ttu-id="2c895-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c895-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c895-193">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c895-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c895-194"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c895-194"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c895-195">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2c895-195">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c895-196"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2c895-196"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2c895-197">DLL</span><span class="sxs-lookup"><span data-stu-id="2c895-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c895-198"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c895-198"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2c895-199">CLSID</span><span class="sxs-lookup"><span data-stu-id="2c895-199">CLSID</span></span><br/>                    | <span data-ttu-id="2c895-200">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="2c895-200">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="2c895-201">IID</span><span class="sxs-lookup"><span data-stu-id="2c895-201">IID</span></span><br/>                      | <span data-ttu-id="2c895-202">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="2c895-202">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="2c895-203">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c895-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c895-204">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="2c895-204">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="2c895-205">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="2c895-205">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

