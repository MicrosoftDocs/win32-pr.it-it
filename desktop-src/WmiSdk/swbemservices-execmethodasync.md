---
description: 'SWbemServices.Exemetodo cMethodAsync: esegue un metodo esportato da un provider di metodi.'
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: SWbemServices.Exemetodo cMethodAsync (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fcdcd70b567a737cb8686ac841dc1ce0b55d3996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105589"
---
# <a name="swbemservicesexecmethodasync-method"></a><span data-ttu-id="bf891-103">SWbemServices.Exemetodo cMethodAsync</span><span class="sxs-lookup"><span data-stu-id="bf891-103">SWbemServices.ExecMethodAsync method</span></span>

<span data-ttu-id="bf891-104">Il **metodo ExecMethodAsync** dell'oggetto [**SWbemServices**](swbemservices.md) esegue un metodo esportato da un provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="bf891-104">The **ExecMethodAsync** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="bf891-105">La chiamata viene restituita immediatamente al client mentre i parametri in ingresso vengono inoltrati al provider appropriato in cui viene eseguito il metodo.</span><span class="sxs-lookup"><span data-stu-id="bf891-105">The call immediately returns to the client while the inbound parameters are forwarded to the appropriate provider where the method executes.</span></span> <span data-ttu-id="bf891-106">Le informazioni e lo stato vengono restituiti al chiamante tramite eventi recapitati al sink specificato in *objWbemSink.*</span><span class="sxs-lookup"><span data-stu-id="bf891-106">Information and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="bf891-107">Il provider, anziché Strumentazione gestione Windows (WMI), implementa il metodo .</span><span class="sxs-lookup"><span data-stu-id="bf891-107">The provider, rather than Windows Management Instrumentation (WMI), implements the method.</span></span>

<span data-ttu-id="bf891-108">Il metodo viene chiamato in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="bf891-108">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="bf891-109">Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="bf891-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="bf891-110">Per altre informazioni e una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bf891-110">For more information and an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf891-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf891-111">Syntax</span></span>


```VB
SWbemServices.ExecMethodAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="bf891-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf891-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf891-113">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="bf891-113">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="bf891-114">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf891-114">Required.</span></span> <span data-ttu-id="bf891-115">Creare un [**oggetto SWbemSink**](swbemsink.md) per ricevere gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="bf891-115">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span> <span data-ttu-id="bf891-116">Sink dell'oggetto che riceve il risultato della chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="bf891-116">Object sink that receives the result of the method call.</span></span> <span data-ttu-id="bf891-117">I parametri in uscita vengono inviati [**all'evento SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) del sink di oggetto fornito.</span><span class="sxs-lookup"><span data-stu-id="bf891-117">The outbound parameters are sent to the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event of the supplied object sink.</span></span> <span data-ttu-id="bf891-118">I risultati del meccanismo di chiamata vengono inviati all'evento [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) del sink di oggetto fornito.</span><span class="sxs-lookup"><span data-stu-id="bf891-118">The results of the call mechanism are sent to the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the supplied object sink.</span></span> <span data-ttu-id="bf891-119">Tenere presente che **SWbemSink.OnCompleted** non riceve il codice restituito del metodo WMI.</span><span class="sxs-lookup"><span data-stu-id="bf891-119">Be aware that **SWbemSink.OnCompleted** does not receive the return code of the WMI method.</span></span> <span data-ttu-id="bf891-120">Riceve tuttavia il codice restituito del meccanismo di chiamata-restituzione effettivo ed è utile solo per verificare che la chiamata si sia verificata o che non sia riuscita per motivi meccanici.</span><span class="sxs-lookup"><span data-stu-id="bf891-120">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons.</span></span> <span data-ttu-id="bf891-121">Il codice del risultato restituito dal metodo WMI viene restituito nell'oggetto parametro in uscita fornito a **SWbemSink.OnObjectReady.**</span><span class="sxs-lookup"><span data-stu-id="bf891-121">The result code that is returned from the WMI method is returned in the outbound parameter object supplied to **SWbemSink.OnObjectReady**.</span></span> <span data-ttu-id="bf891-122">Se viene restituito un codice di errore, l'oggetto [**IWbemObjectSink**](iwbemobjectsink.md) fornito non viene usato.</span><span class="sxs-lookup"><span data-stu-id="bf891-122">If any error code is returned, then the supplied [**IWbemObjectSink**](iwbemobjectsink.md) object is not used.</span></span> <span data-ttu-id="bf891-123">Se la chiamata ha esito positivo, viene chiamata l'implementazione **IWbemObjectSink** dell'utente per indicare il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bf891-123">If the call is successful, then the user's **IWbemObjectSink** implementation is called to indicate the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bf891-124">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="bf891-124">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="bf891-125">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf891-125">Required.</span></span> <span data-ttu-id="bf891-126">Stringa contenente il percorso dell'oggetto per cui viene eseguito il metodo.</span><span class="sxs-lookup"><span data-stu-id="bf891-126">A string that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="bf891-127">Per altre informazioni, vedere [Descrizione del percorso di un oggetto WMI.](describing-the-location-of-a-wmi-object.md)</span><span class="sxs-lookup"><span data-stu-id="bf891-127">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf891-128">*strMethodName*</span><span class="sxs-lookup"><span data-stu-id="bf891-128">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="bf891-129">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf891-129">Required.</span></span> <span data-ttu-id="bf891-130">Nome del metodo da eseguire.</span><span class="sxs-lookup"><span data-stu-id="bf891-130">The name of the method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="bf891-131">*objWbemInParams* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="bf891-131">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bf891-132">Oggetto [**SWbemObject**](swbemobject.md) che contiene i parametri di input per il metodo eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf891-132">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method that is executed.</span></span> <span data-ttu-id="bf891-133">Per impostazione predefinita, questo parametro non è definito.</span><span class="sxs-lookup"><span data-stu-id="bf891-133">By default, this parameter is undefined.</span></span> <span data-ttu-id="bf891-134">Per altre informazioni, vedere [Costruzione di oggetti InParameters e Analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bf891-134">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf891-135">*iFlags* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="bf891-135">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bf891-136">Numero intero che determina il comportamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="bf891-136">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="bf891-137">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bf891-137">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="bf891-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus\*\*\*\* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="bf891-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="bf891-139">Fa sì che le chiamate asincrone inviino aggiornamenti dello stato al [**gestore dell'evento OnProgress**](swbemsink-onprogress.md) per il sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="bf891-139">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="bf891-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="bf891-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="bf891-141">Impedisce alle chiamate asincrone di inviare aggiornamenti dello stato al [**gestore eventi OnProgress**](swbemsink-onprogress.md) per il sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="bf891-141">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bf891-142">*objWbemNamedValueSet* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="bf891-142">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bf891-143">In genere, questa operazione non è definita.</span><span class="sxs-lookup"><span data-stu-id="bf891-143">Typically, this is undefined.</span></span> <span data-ttu-id="bf891-144">In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere usate dal provider che sta servo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="bf891-144">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="bf891-145">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="bf891-145">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="bf891-146">*objWbemAsyncContext* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="bf891-146">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bf891-147">Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink dell'oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="bf891-147">A [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="bf891-148">Usare questo parametro se si effettuano più chiamate asincrone usando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="bf891-148">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="bf891-149">Per usare questo parametro, creare un **oggetto SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bf891-149">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="bf891-150">Questo **oggetto SWbemNamedValueSet** viene restituito al sink dell'oggetto e l'origine della chiamata può essere estratta usando il metodo [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md)</span><span class="sxs-lookup"><span data-stu-id="bf891-150">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="bf891-151">Per altre informazioni, vedere [Esecuzione di una chiamata asincrona con VBScript.](making-an-asynchronous-call-with-vbscript.md)</span><span class="sxs-lookup"><span data-stu-id="bf891-151">For more information, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf891-152">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf891-152">Return value</span></span>

<span data-ttu-id="bf891-153">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bf891-153">This method does not return a value.</span></span> <span data-ttu-id="bf891-154">Se la chiamata ha esito positivo, al sink specificato in *objWbemSink* viene fornito un oggetto [**OutParameters,**](swbemmethod-outparameters.md) che è anche un [**oggetto SWbemObject.**](swbemobject.md)</span><span class="sxs-lookup"><span data-stu-id="bf891-154">If the call is successful, an [**OutParameters**](swbemmethod-outparameters.md) object, which is also an [**SWbemObject**](swbemobject.md) is supplied to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="bf891-155">**L'oggetto OutParameters** restituito contiene i parametri di output e il valore restituito per il metodo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bf891-155">The returned **OutParameters** object contains the output parameters and return value for the method being executed.</span></span> <span data-ttu-id="bf891-156">Per altre informazioni, vedere [Costruzione di oggetti InParameters e Analisi di oggetti OutParameters.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)</span><span class="sxs-lookup"><span data-stu-id="bf891-156">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="bf891-157">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="bf891-157">Error codes</span></span>

<span data-ttu-id="bf891-158">Dopo il completamento del **metodo ExecMethodAsync,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="bf891-158">After the completion of the **ExecMethodAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes listed in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="bf891-159">**wbemErrFailed** - 2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="bf891-159">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="bf891-160">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="bf891-160">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="bf891-161">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="bf891-161">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="bf891-162">Classe specificata non valida.</span><span class="sxs-lookup"><span data-stu-id="bf891-162">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="bf891-163">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="bf891-163">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="bf891-164">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="bf891-164">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="bf891-165">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="bf891-165">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="bf891-166">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="bf891-166">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bf891-167">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="bf891-167">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="bf891-168">Metodo richiesto non disponibile.</span><span class="sxs-lookup"><span data-stu-id="bf891-168">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="bf891-169">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="bf891-169">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="bf891-170">L'utente corrente non è stato autorizzato a eseguire il metodo.</span><span class="sxs-lookup"><span data-stu-id="bf891-170">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf891-171">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf891-171">Remarks</span></span>

<span data-ttu-id="bf891-172">Se il metodo eseguito ha parametri di input, l'oggetto [**InParameters**](swbemmethod-inparameters.md) nel *parametro objWbemInParam* deve corrispondere alla descrizione negli argomenti Costruzione di oggetti InParameters e Analisi di oggetti [OutParameters.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)</span><span class="sxs-lookup"><span data-stu-id="bf891-172">If the method executed has input parameters, the [**InParameters**](swbemmethod-inparameters.md) object in the *objWbemInParam* parameter must be the same as the description in the [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md) topics.</span></span>

<span data-ttu-id="bf891-173">Usare **SWbemServices.ExecMethodAsync** come alternativa all'accesso diretto per l'esecuzione di un metodo [*provider*](gloss-p.md) quando non è possibile eseguire direttamente un metodo.</span><span class="sxs-lookup"><span data-stu-id="bf891-173">Use **SWbemServices.ExecMethodAsync** as an alternative to direct access for executing a [*provider method*](gloss-p.md) when it is not possible to execute a method directly.</span></span> <span data-ttu-id="bf891-174">Ad esempio, usarlo con un linguaggio di scripting che non supporta i parametri di output, ad esempio se il metodo dispone di parametri OUT.</span><span class="sxs-lookup"><span data-stu-id="bf891-174">For example, use it with a scripting language that does not support output parameters, that is, if your method has OUT parameters.</span></span> <span data-ttu-id="bf891-175">In caso contrario, è consigliabile usare l'accesso diretto per richiamare un metodo.</span><span class="sxs-lookup"><span data-stu-id="bf891-175">Otherwise, it is recommended that you use direct access to invoke a method.</span></span> <span data-ttu-id="bf891-176">Per altre informazioni, vedere [Modifica delle informazioni su classi e istanze](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="bf891-176">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="bf891-177">Il **SWbemServices.ExecMethodAsync** richiede un percorso di oggetto.</span><span class="sxs-lookup"><span data-stu-id="bf891-177">The **SWbemServices.ExecMethodAsync** method requires an object path.</span></span> <span data-ttu-id="bf891-178">Se lo script contiene già un [**oggetto SWbemObject,**](swbemobject.md) è possibile chiamareSWbemObject.Exe [**cMethodAsync**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="bf891-178">If the script already contains an [**SWbemObject**](swbemobject.md) object, you can call [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>

<span data-ttu-id="bf891-179">Questa chiamata restituisce immediatamente .</span><span class="sxs-lookup"><span data-stu-id="bf891-179">This call returns immediately.</span></span> <span data-ttu-id="bf891-180">Le informazioni sullo stato vengono restituite al chiamante tramite i call-back recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="bf891-180">The status information is returned to the caller through call-backs delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="bf891-181">Per continuare l'elaborazione al termine della chiamata, implementare una subroutine per *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md)</span><span class="sxs-lookup"><span data-stu-id="bf891-181">To continue processing when the call is completed, implement a subroutine for the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="bf891-182">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="bf891-182">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="bf891-183">Ciò comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="bf891-183">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="bf891-184">Per altre informazioni su come eliminare i rischi, vedere [Impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="bf891-184">For more information about how to eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="bf891-185">Usare il *parametro objWbemAsyncContext* per verificare l'origine di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="bf891-185">Use the *objWbemAsyncContext* parameter to verify the source of a call.</span></span>

## <a name="examples"></a><span data-ttu-id="bf891-186">Esempio</span><span class="sxs-lookup"><span data-stu-id="bf891-186">Examples</span></span>

<span data-ttu-id="bf891-187">L'esempio di codice seguente mostra il **metodo ExecMethodAsync.**</span><span class="sxs-lookup"><span data-stu-id="bf891-187">The following code example shows the **ExecMethodAsync** method.</span></span> <span data-ttu-id="bf891-188">Lo script crea un [**oggetto Processo \_ Win32**](/windows/desktop/CIMWin32Prov/win32-process) che rappresenta un processo che esegue Blocco note.</span><span class="sxs-lookup"><span data-stu-id="bf891-188">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="bf891-189">Mostra la configurazione di un [**oggetto InParameters**](swbemmethod-inparameters.md) e come ottenere i risultati da un [**oggetto OutParameters.**](swbemmethod-outparameters.md)</span><span class="sxs-lookup"><span data-stu-id="bf891-189">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="bf891-190">Per uno script che mostra le stesse operazioni eseguite in modo sincrono, vedereSWbemServices.Exe [**cMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="bf891-190">For a script that shows the same operations performed synchronously, see [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span> <span data-ttu-id="bf891-191">Per un esempio dell'uso dell'accesso diretto, vedere [Create Method in Class Win32 \_ Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="bf891-191">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="bf891-192">Per un esempio della stessa operazione che usa [**SWbemObject,**](swbemobject.md) [**SWbemObject.ExecMethodAsync.**](swbemobject-execmethodasync-.md)</span><span class="sxs-lookup"><span data-stu-id="bf891-192">For an example of the same operation using [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>


```VB
' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &VBCR & "ReturnValue = " _
        & oOutParams.ReturnValue &VBCR & _
        "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
        & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a><span data-ttu-id="bf891-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf891-193">Requirements</span></span>



| <span data-ttu-id="bf891-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf891-194">Requirement</span></span> | <span data-ttu-id="bf891-195">Valore</span><span class="sxs-lookup"><span data-stu-id="bf891-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf891-196">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf891-196">Minimum supported client</span></span><br/> | <span data-ttu-id="bf891-197">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf891-197">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bf891-198">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf891-198">Minimum supported server</span></span><br/> | <span data-ttu-id="bf891-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf891-199">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf891-200">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf891-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf891-201"><dt>Wbemdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="bf891-201"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf891-202">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bf891-202">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf891-203"><dt>Wbemdisp.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bf891-203"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bf891-204">DLL</span><span class="sxs-lookup"><span data-stu-id="bf891-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf891-205"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf891-205"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf891-206">CLSID</span><span class="sxs-lookup"><span data-stu-id="bf891-206">CLSID</span></span><br/>                    | <span data-ttu-id="bf891-207">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="bf891-207">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="bf891-208">IID</span><span class="sxs-lookup"><span data-stu-id="bf891-208">IID</span></span><br/>                      | <span data-ttu-id="bf891-209">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="bf891-209">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="bf891-210">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf891-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf891-211">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="bf891-211">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="bf891-212">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="bf891-212">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="bf891-213">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="bf891-213">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="bf891-214">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="bf891-214">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="bf891-215">Chiamata di un metodo del provider</span><span class="sxs-lookup"><span data-stu-id="bf891-215">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="bf891-216">Modifica delle informazioni su classi e istanze</span><span class="sxs-lookup"><span data-stu-id="bf891-216">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

