---
description: Il \_ Metodo DeleteAsync di SWbemObject Elimina in modo asincrono la classe corrente o l'istanza corrente.
ms.assetid: b8d67fa5-5217-422b-acbe-5eea6028deeb
ms.tgt_platform: multiple
title: Metodo SWbemObject.DeleteAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7951b84a2b5d9f06061f4cefb04c797ccfea3ecd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309829"
---
# <a name="swbemobjectdeleteasync_-method"></a><span data-ttu-id="ca06e-103">SWbemObject. DeleteAsync, \_ Metodo</span><span class="sxs-lookup"><span data-stu-id="ca06e-103">SWbemObject.DeleteAsync\_ method</span></span>

<span data-ttu-id="ca06e-104">Il **metodo \_ DeleteAsync** di [**SWbemObject**](swbemobject.md) Elimina in modo asincrono la classe corrente o l'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="ca06e-104">The **DeleteAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously deletes either the current class or the current instance.</span></span> <span data-ttu-id="ca06e-105">Se un provider dinamico fornisce la classe o l'istanza, a volte non è possibile eliminare questo oggetto a meno che il provider non supporti l'eliminazione di classi o istanze.</span><span class="sxs-lookup"><span data-stu-id="ca06e-105">If a dynamic provider supplies the class or instance, sometimes it is not possible to delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="ca06e-106">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ca06e-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca06e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca06e-107">Syntax</span></span>


```VB
SWbemObject.DeleteAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ca06e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca06e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca06e-109">*objWbemSink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca06e-109">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca06e-110">Sink di oggetto che restituisce il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="ca06e-110">Object sink that returns the outcome of the delete operation.</span></span>

</dd> <dt>

<span data-ttu-id="ca06e-111">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ca06e-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca06e-112">Integer che determina il comportamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="ca06e-112">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="ca06e-113">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ca06e-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="ca06e-114"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="ca06e-114"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="ca06e-115">Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**SWbemSink. OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ca06e-115">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="ca06e-116"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="ca06e-116"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* ( 0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="ca06e-117">Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ca06e-117">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ca06e-118">*objwbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ca06e-118">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca06e-119">Questo parametro non è in genere definito.</span><span class="sxs-lookup"><span data-stu-id="ca06e-119">This parameter is typically undefined.</span></span> <span data-ttu-id="ca06e-120">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ca06e-120">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="ca06e-121">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="ca06e-121">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="ca06e-122">*objWbemAsyncContext* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ca06e-122">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca06e-123">Si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="ca06e-123">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="ca06e-124">Utilizzare questo parametro se si eseguono più chiamate asincrone utilizzando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="ca06e-124">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="ca06e-125">Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando.</span><span class="sxs-lookup"><span data-stu-id="ca06e-125">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="ca06e-126">Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="ca06e-126">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="ca06e-127">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ca06e-127">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca06e-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca06e-128">Return value</span></span>

<span data-ttu-id="ca06e-129">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ca06e-129">This method does not return a value.</span></span> <span data-ttu-id="ca06e-130">Se la chiamata ha esito positivo, il risultato dell'operazione di eliminazione viene fornito tramite il sink di oggetto fornito.</span><span class="sxs-lookup"><span data-stu-id="ca06e-130">If this call is successful, the result of the delete operation is provided through the supplied object sink.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ca06e-131">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ca06e-131">Error codes</span></span>

<span data-ttu-id="ca06e-132">Dopo il completamento del metodo **DeleteAsync \_** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="ca06e-132">After the completion of the **DeleteAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ca06e-133">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="ca06e-133">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="ca06e-134">Il contesto corrente non dispone dei privilegi di protezione appropriati per eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ca06e-134">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="ca06e-135">**wbemErrFailed** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="ca06e-135">**wbemErrFailed** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="ca06e-136">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ca06e-136">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ca06e-137">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="ca06e-137">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="ca06e-138">La classe specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="ca06e-138">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="ca06e-139">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="ca06e-139">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="ca06e-140">Impossibile eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ca06e-140">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="ca06e-141">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="ca06e-141">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="ca06e-142">Oggetto inesistente.</span><span class="sxs-lookup"><span data-stu-id="ca06e-142">Object did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="ca06e-143">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="ca06e-143">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="ca06e-144">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ca06e-144">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca06e-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca06e-145">Remarks</span></span>

<span data-ttu-id="ca06e-146">Questa chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="ca06e-146">This call returns immediately.</span></span> <span data-ttu-id="ca06e-147">Lo stato viene restituito al chiamante tramite un callback recapitato al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="ca06e-147">The status is returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span>

<span data-ttu-id="ca06e-148">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="ca06e-148">An asynchronous callback allows a nonauthenticated user to provide data to the sink.</span></span> <span data-ttu-id="ca06e-149">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ca06e-149">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="ca06e-150">Per eliminare i rischi, usare la comunicazione semisincrono o la comunicazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="ca06e-150">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="ca06e-151">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ca06e-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca06e-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca06e-152">Requirements</span></span>



| <span data-ttu-id="ca06e-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca06e-153">Requirement</span></span> | <span data-ttu-id="ca06e-154">Valore</span><span class="sxs-lookup"><span data-stu-id="ca06e-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca06e-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca06e-155">Minimum supported client</span></span><br/> | <span data-ttu-id="ca06e-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca06e-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca06e-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca06e-157">Minimum supported server</span></span><br/> | <span data-ttu-id="ca06e-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca06e-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca06e-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca06e-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca06e-160"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca06e-160"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca06e-161">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ca06e-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="ca06e-162"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ca06e-162"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ca06e-163">DLL</span><span class="sxs-lookup"><span data-stu-id="ca06e-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca06e-164"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca06e-164"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ca06e-165">CLSID</span><span class="sxs-lookup"><span data-stu-id="ca06e-165">CLSID</span></span><br/>                    | <span data-ttu-id="ca06e-166">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="ca06e-166">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="ca06e-167">IID</span><span class="sxs-lookup"><span data-stu-id="ca06e-167">IID</span></span><br/>                      | <span data-ttu-id="ca06e-168">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="ca06e-168">IID\_ISWbemObject</span></span><br/>                                                            |



 

