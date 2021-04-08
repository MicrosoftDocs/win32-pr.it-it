---
description: Salva un oggetto in modo asincrono in uno spazio dei nomi. Quando ha esito positivo, questo metodo invia un evento OnCompleted all'oggetto SWbemSink specificato come parametro di input.
ms.assetid: 27da0c60-6dae-482d-a9bf-1aab016d3ae8
ms.tgt_platform: multiple
title: Metodo SWbemServicesEx. PutAsync (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 06f470ed6f8cbd497ba3d3a3a77c5a8b4e5748c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057856"
---
# <a name="swbemservicesexputasync-method"></a><span data-ttu-id="634fb-104">SWbemServicesEx. PutAsync, metodo</span><span class="sxs-lookup"><span data-stu-id="634fb-104">SWbemServicesEx.PutAsync method</span></span>

<span data-ttu-id="634fb-105">Il metodo **PutAsync** dell'oggetto [**SWbemServicesEx**](swbemservicesex.md) Salva in modo asincrono un oggetto in uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="634fb-105">The **PutAsync** method of the [**SWbemServicesEx**](swbemservicesex.md) object saves an object asynchronously to a namespace.</span></span> <span data-ttu-id="634fb-106">Quando ha esito positivo, questo metodo invia un evento [**OnCompleted**](swbemsink-oncompleted.md) all'oggetto [**SWbemSink**](swbemsink.md) specificato come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="634fb-106">When successful, this method sends an [**OnCompleted**](swbemsink-oncompleted.md) event to the [**SWbemSink**](swbemsink.md) object that is specified as an input parameter.</span></span>

<span data-ttu-id="634fb-107">Questo metodo viene chiamato in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="634fb-107">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="634fb-108">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="634fb-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="634fb-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="634fb-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="634fb-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="634fb-110">Syntax</span></span>


```VB
SWbemServicesEx.PutAsync( _
  ByVal objWbemSink, _
  ByVal ojbWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="634fb-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="634fb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="634fb-112">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="634fb-112">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="634fb-113">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="634fb-113">Required.</span></span> <span data-ttu-id="634fb-114">Sink di oggetto che riceve gli oggetti in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="634fb-114">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="634fb-115">Creare un oggetto [**SWbemSink**](swbemsink.md) per ricevere gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="634fb-115">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="634fb-116">*ojbWbemObject*</span><span class="sxs-lookup"><span data-stu-id="634fb-116">*ojbWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="634fb-117">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="634fb-117">Required.</span></span> <span data-ttu-id="634fb-118">Nuovo oggetto da inserire nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="634fb-118">The new object to be put in the namespace.</span></span> <span data-ttu-id="634fb-119">Potrebbe trattarsi di un oggetto appena creato o di un oggetto modificato.</span><span class="sxs-lookup"><span data-stu-id="634fb-119">This may be a newly created object or a modified object.</span></span>

</dd> <dt>

<span data-ttu-id="634fb-120">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="634fb-120">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="634fb-121">Questo parametro determina se la chiamata crea o aggiorna l'oggetto e se la chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="634fb-121">This parameter determines whether the call creates or updates the object and whether the call returns immediately.</span></span> <span data-ttu-id="634fb-122">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="634fb-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="634fb-123"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="634fb-123"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="634fb-124">Consente di aggiornare una classe quando non sono presenti classi derivate e nessuna istanza per la classe.</span><span class="sxs-lookup"><span data-stu-id="634fb-124">Allows a class to be updated when there are no derived classes and no instances for the class.</span></span> <span data-ttu-id="634fb-125">Consente inoltre gli aggiornamenti in tutti i casi in cui la modifica riguarda solo i qualificatori non importanti, ad esempio il qualificatore della **Descrizione** .</span><span class="sxs-lookup"><span data-stu-id="634fb-125">It also allows updates in all cases when the change is only to unimportant qualifiers, for example, the **Description** qualifier.</span></span> <span data-ttu-id="634fb-126">Questo è il comportamento predefinito per questa chiamata e viene usato per la compatibilità con le versioni precedenti di WMI.</span><span class="sxs-lookup"><span data-stu-id="634fb-126">This is the default behavior for this call, and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="634fb-127">Se la classe dispone di istanze, l'aggiornamento avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="634fb-127">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="634fb-128"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="634fb-128"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="634fb-129">Consente di aggiornare le classi anche quando sono presenti classi figlio e la modifica non provoca conflitti con le classi figlio.</span><span class="sxs-lookup"><span data-stu-id="634fb-129">Allows updates of classes even when there are child classes and the change does not cause conflicts with the child classes.</span></span> <span data-ttu-id="634fb-130">Utilizzare questo flag quando si aggiunge una nuova proprietà a una classe di base non citata in precedenza in nessuna delle classi figlio.</span><span class="sxs-lookup"><span data-stu-id="634fb-130">Use this flag when adding a new property to a base class that is not mentioned previously in any of the child classes.</span></span> <span data-ttu-id="634fb-131">Se la classe dispone di istanze, l'aggiornamento avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="634fb-131">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="634fb-132"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="634fb-132"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="634fb-133">Questo flag forza gli aggiornamenti delle classi quando esistono classi figlio in conflitto.</span><span class="sxs-lookup"><span data-stu-id="634fb-133">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="634fb-134">Questo flag, ad esempio, impone un aggiornamento quando viene definito un qualificatore di classe in una classe figlio e la classe di base tenta di aggiungere lo stesso qualificatore in conflitto con quello esistente.</span><span class="sxs-lookup"><span data-stu-id="634fb-134">For example, this flag forces an update when a class qualifier is defined in a child class, and the base class tries to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="634fb-135">In modalità Force questo conflitto viene risolto eliminando il qualificatore in conflitto nella classe figlio.</span><span class="sxs-lookup"><span data-stu-id="634fb-135">In the force mode, this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="634fb-136">Se la classe dispone di istanze, l'aggiornamento avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="634fb-136">If the class has instances, the update fails.</span></span>

<span data-ttu-id="634fb-137">L'uso della modalità Force per aggiornare una classe statica comporta l'eliminazione di tutte le istanze di tale classe.</span><span class="sxs-lookup"><span data-stu-id="634fb-137">The use of the force mode to update a static class causes the deletion of all instances of that class.</span></span> <span data-ttu-id="634fb-138">Un aggiornamento forzato in una classe provider non elimina le istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="634fb-138">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="634fb-139"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="634fb-139"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="634fb-140">Determina la creazione della classe o dell'istanza, se non esiste, oppure sovrascritta se esiste già.</span><span class="sxs-lookup"><span data-stu-id="634fb-140">Causes the class or instance to be created if it does not exist, or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="634fb-141"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="634fb-141"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="634fb-142">Utilizzato solo per la creazione.</span><span class="sxs-lookup"><span data-stu-id="634fb-142">Used for creation only.</span></span> <span data-ttu-id="634fb-143">La chiamata ha esito negativo se la classe o l'istanza esiste già.</span><span class="sxs-lookup"><span data-stu-id="634fb-143">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="634fb-144"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="634fb-144"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="634fb-145">Causa l'aggiornamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="634fb-145">Causes this call to update.</span></span> <span data-ttu-id="634fb-146">La classe o l'istanza deve esistere affinché la chiamata abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="634fb-146">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="634fb-147"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="634fb-147"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="634fb-148">Causa la restituzione immediata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="634fb-148">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="634fb-149"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="634fb-149"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="634fb-150">Causa il blocco della chiamata fino al completamento della query.</span><span class="sxs-lookup"><span data-stu-id="634fb-150">Causes this call to block until the query is complete.</span></span> <span data-ttu-id="634fb-151">Questo flag chiama il metodo in modalità sincrona.</span><span class="sxs-lookup"><span data-stu-id="634fb-151">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="634fb-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="634fb-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="634fb-153">Fa in modo che WMI scriva i dati di modifica della classe e la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="634fb-153">Causes WMI to write class amendment data and the base class definition.</span></span> <span data-ttu-id="634fb-154">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="634fb-154">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="634fb-155">*objWbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="634fb-155">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="634fb-156">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="634fb-156">Typically, this is undefined.</span></span> <span data-ttu-id="634fb-157">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che servizi la richiesta.</span><span class="sxs-lookup"><span data-stu-id="634fb-157">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="634fb-158">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="634fb-158">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="634fb-159">*objWbemAsyncContext* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="634fb-159">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="634fb-160">Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="634fb-160">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="634fb-161">Utilizzare questo parametro per effettuare più chiamate asincrone utilizzando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="634fb-161">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="634fb-162">Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando.</span><span class="sxs-lookup"><span data-stu-id="634fb-162">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="634fb-163">Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="634fb-163">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="634fb-164">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="634fb-164">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="634fb-165">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="634fb-165">Return value</span></span>

<span data-ttu-id="634fb-166">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="634fb-166">This method does not return a value.</span></span> <span data-ttu-id="634fb-167">Se la chiamata ha esito positivo, l'evento [**OnObjectPut**](swbemsink-onobjectput.md) del sink di oggetto fornito riceve un oggetto [**SWbemObjectPath**](swbemobjectpath.md) che contiene il percorso dell'oggetto dell'istanza o della classe di cui è stato eseguito correttamente il commit in WMI.</span><span class="sxs-lookup"><span data-stu-id="634fb-167">If the call is successful, the [**OnObjectPut**](swbemsink-onobjectput.md) event of the supplied object sink receives an [**SWbemObjectPath**](swbemobjectpath.md) object, which contains the object path of the instance or class that is successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="634fb-168">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="634fb-168">Error codes</span></span>

<span data-ttu-id="634fb-169">Dopo il completamento del metodo **PutAsync** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="634fb-169">After the completion of the **PutAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="634fb-170">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="634fb-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="634fb-171">L'utente corrente non dispone dell'autorizzazione per l'aggiornamento di un'istanza della classe specificata.</span><span class="sxs-lookup"><span data-stu-id="634fb-171">Current user does not have the permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="634fb-172">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="634fb-172">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="634fb-173">È stato specificato il flag **wbemChangeFlagCreateOnly** , ma l'istanza esiste già.</span><span class="sxs-lookup"><span data-stu-id="634fb-173">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="634fb-174">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="634fb-174">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="634fb-175">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="634fb-175">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="634fb-176">**wbemErrIllegalNull** -2147749898 (0x8004100a)</span><span class="sxs-lookup"><span data-stu-id="634fb-176">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="634fb-177">È stato specificato un valore null per una proprietà che non può essere null.</span><span class="sxs-lookup"><span data-stu-id="634fb-177">A value of Null was specified for a property that cannot be Null.</span></span> <span data-ttu-id="634fb-178">Un esempio di tale proprietà è quello contrassegnato da un qualificatore di **chiave**, **indicizzato** o **Not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="634fb-178">An example of such a property is one marked by a **Key**, **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="634fb-179">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="634fb-179">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="634fb-180">L'istanza specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="634fb-180">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="634fb-181">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="634fb-181">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="634fb-182">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="634fb-182">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="634fb-183">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="634fb-183">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="634fb-184">È stato specificato il flag **wbemChangeFlagUpdateOnly** , ma l'istanza o la classe non esiste.</span><span class="sxs-lookup"><span data-stu-id="634fb-184">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="634fb-185">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="634fb-185">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="634fb-186">Le proprietà obbligatorie per le classi non sono state impostate.</span><span class="sxs-lookup"><span data-stu-id="634fb-186">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="634fb-187">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="634fb-187">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="634fb-188">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="634fb-188">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="634fb-189">Commenti</span><span class="sxs-lookup"><span data-stu-id="634fb-189">Remarks</span></span>

<span data-ttu-id="634fb-190">Questa chiamata restituisce immediatamente un risultato e i risultati e lo stato vengono restituiti al chiamante tramite gli eventi recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="634fb-190">This call returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="634fb-191">Per gestire ogni oggetto all'arrivo, creare un *objWbemSink*. Subroutine dell'evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="634fb-191">To handle each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="634fb-192">Qualsiasi elaborazione eseguita dopo l'arrivo di tutti gli oggetti viene eseguita in una subroutine per *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="634fb-192">Any processing done after all the objects arrive is done in a subroutine for the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="634fb-193">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="634fb-193">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="634fb-194">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="634fb-194">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="634fb-195">Per eliminare i rischi, vedere [impostazione della sicurezza per una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="634fb-195">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="634fb-196">Requisiti</span><span class="sxs-lookup"><span data-stu-id="634fb-196">Requirements</span></span>



| <span data-ttu-id="634fb-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="634fb-197">Requirement</span></span> | <span data-ttu-id="634fb-198">Valore</span><span class="sxs-lookup"><span data-stu-id="634fb-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="634fb-199">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="634fb-199">Minimum supported client</span></span><br/> | <span data-ttu-id="634fb-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="634fb-200">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="634fb-201">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="634fb-201">Minimum supported server</span></span><br/> | <span data-ttu-id="634fb-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="634fb-202">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="634fb-203">Intestazione</span><span class="sxs-lookup"><span data-stu-id="634fb-203">Header</span></span><br/>                   | <dl> <span data-ttu-id="634fb-204"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="634fb-204"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="634fb-205">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="634fb-205">Type library</span></span><br/>             | <dl> <span data-ttu-id="634fb-206"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="634fb-206"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="634fb-207">DLL</span><span class="sxs-lookup"><span data-stu-id="634fb-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="634fb-208"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="634fb-208"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="634fb-209">CLSID</span><span class="sxs-lookup"><span data-stu-id="634fb-209">CLSID</span></span><br/>                    | <span data-ttu-id="634fb-210">\_ISWBEMSERVICESEX CLSID</span><span class="sxs-lookup"><span data-stu-id="634fb-210">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="634fb-211">IID</span><span class="sxs-lookup"><span data-stu-id="634fb-211">IID</span></span><br/>                      | <span data-ttu-id="634fb-212">\_ISWBEMSERVICESEX IID</span><span class="sxs-lookup"><span data-stu-id="634fb-212">IID\_ISWbemServicesEx</span></span><br/>                                                        |



 

