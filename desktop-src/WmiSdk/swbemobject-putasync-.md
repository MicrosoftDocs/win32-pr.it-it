---
description: Il \_ Metodo PutAsync di SWbemObject crea o aggiorna in modo asincrono un'istanza o un oggetto classe per Strumentazione gestione Windows (WMI).
ms.assetid: ff738412-fcca-4e4a-a178-0d1d391ec99b
ms.tgt_platform: multiple
title: Metodo SWbemObject.PutAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.PutAsync_
- ISWbemObject.PutAsync_
- ISWbemObject.PutAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3530c3883763773f53bec81aeee8b0d199170133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233808"
---
# <a name="swbemobjectputasync_-method"></a><span data-ttu-id="74366-103">SWbemObject. PutAsync, \_ Metodo</span><span class="sxs-lookup"><span data-stu-id="74366-103">SWbemObject.PutAsync\_ method</span></span>

<span data-ttu-id="74366-104">Il **metodo \_ PutAsync** di [**SWbemObject**](swbemobject.md) crea o aggiorna in modo asincrono un'istanza o un oggetto classe per Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="74366-104">The **PutAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously creates or updates an instance or class object to Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="74366-105">È possibile utilizzare questo metodo dopo aver modificato le proprietà o i metodi in **SWbemObject** e le modifiche vengono scritte in WMI.</span><span class="sxs-lookup"><span data-stu-id="74366-105">You can use this method after you modify any properties or methods in **SWbemObject**, and your changes are written to WMI.</span></span>

<span data-ttu-id="74366-106">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="74366-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="74366-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74366-107">Syntax</span></span>


```VB
SWbemObject.PutAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="74366-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="74366-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74366-109">*objWbemSink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74366-109">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74366-110">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="74366-110">Required.</span></span> <span data-ttu-id="74366-111">Sink di oggetto che riceve in modo asincrono il risultato dell'operazione **put** .</span><span class="sxs-lookup"><span data-stu-id="74366-111">Object sink that asynchronously receives the result of the **put** operation.</span></span>

</dd> <dt>

<span data-ttu-id="74366-112">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="74366-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="74366-113">Determina se la chiamata crea o aggiorna la classe o l'istanza e se la chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="74366-113">Determines if the call creates or updates the class or instance and if the call returns immediately.</span></span> <span data-ttu-id="74366-114">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="74366-114">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="74366-115"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="74366-115"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>\*\*\*\*wbemChangeFlagUpdateCompatible\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="74366-116">Consente di aggiornare una classe se non sono presenti classi derivate e non sono presenti istanze per tale classe.</span><span class="sxs-lookup"><span data-stu-id="74366-116">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="74366-117">Consente inoltre gli aggiornamenti in tutti i casi in cui la modifica riguarda solo i qualificatori non importanti, ad esempio il qualificatore della **Descrizione** .</span><span class="sxs-lookup"><span data-stu-id="74366-117">It also allows updates in all cases if the change is just to unimportant qualifiers (for example the **Description** qualifier).</span></span> <span data-ttu-id="74366-118">Questo è il comportamento predefinito per questa chiamata e viene utilizzato per la compatibilità con le versioni precedenti di WMI.</span><span class="sxs-lookup"><span data-stu-id="74366-118">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="74366-119">Se la classe dispone di istanze, l'aggiornamento ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="74366-119">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="74366-120"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="74366-120"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>\*\*\*\*wbemChangeFlagUpdateSafeMode\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="74366-121">Consente di aggiornare le classi, anche se sono presenti classi figlio, se la modifica non provoca conflitti con le classi figlio.</span><span class="sxs-lookup"><span data-stu-id="74366-121">Allows updates of classes, even if there are child classes, if the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="74366-122">È possibile utilizzare questo flag quando si aggiunge una nuova proprietà a una classe di base non indicata in precedenza in nessuna delle classi figlio.</span><span class="sxs-lookup"><span data-stu-id="74366-122">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="74366-123">Se la classe dispone di istanze, l'aggiornamento ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="74366-123">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="74366-124"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode \* \* \* \* (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="74366-124"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>\*\*\*\*WbemChangeFlagUpdateForceMode\*\*\*\* (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="74366-125">Forza gli aggiornamenti delle classi quando esistono classi figlio in conflitto.</span><span class="sxs-lookup"><span data-stu-id="74366-125">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="74366-126">Questo flag, ad esempio, impone un aggiornamento se è stato definito un qualificatore di classe in una classe figlio e la classe di base tenta di aggiungere lo stesso qualificatore in conflitto con quello esistente.</span><span class="sxs-lookup"><span data-stu-id="74366-126">For example, this flag forces an update if a class qualifier was defined in a child class, and the base class attempts to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="74366-127">In modalità Force questo conflitto viene risolto eliminando il qualificatore in conflitto nella classe figlio.</span><span class="sxs-lookup"><span data-stu-id="74366-127">In force mode this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="74366-128">Se la classe dispone di istanze, l'aggiornamento ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="74366-128">If the class has instances the update fails.</span></span>

<span data-ttu-id="74366-129">L'uso della modalità Force per aggiornare una classe statica comporta l'eliminazione di tutte le istanze di tale classe.</span><span class="sxs-lookup"><span data-stu-id="74366-129">Using force mode to update a static class results in the deletion of all instances of that class.</span></span> <span data-ttu-id="74366-130">Un aggiornamento forzato in una classe provider non elimina le istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="74366-130">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="74366-131"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="74366-131"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>\*\*\*\*wbemChangeFlagCreateOrUpdate\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="74366-132">Determina la creazione della classe o dell'istanza se non esiste o sovrascritta se esiste già.</span><span class="sxs-lookup"><span data-stu-id="74366-132">Causes the class or instance to be created if it does not exist or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="74366-133"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="74366-133"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>\*\*\*\*wbemChangeFlagCreateOnly\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="74366-134">Utilizzato solo per la creazione.</span><span class="sxs-lookup"><span data-stu-id="74366-134">Used for creation only.</span></span> <span data-ttu-id="74366-135">La chiamata ha esito negativo se la classe o l'istanza esiste già.</span><span class="sxs-lookup"><span data-stu-id="74366-135">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="74366-136"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="74366-136"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>\*\*\*\*wbemChangeFlagUpdateOnly\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="74366-137">Causa l'aggiornamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="74366-137">Causes this call to update.</span></span> <span data-ttu-id="74366-138">La classe o l'istanza deve esistere affinché la chiamata abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="74366-138">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="74366-139"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="74366-139"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="74366-140">Causa la restituzione immediata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="74366-140">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="74366-141"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="74366-141"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="74366-142">Causa il blocco della chiamata fino al completamento della query.</span><span class="sxs-lookup"><span data-stu-id="74366-142">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="74366-143"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="74366-143"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="74366-144">Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**SWbemSink. OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="74366-144">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="74366-145"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="74366-145"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="74366-146">Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="74366-146">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="74366-147"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="74366-147"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="74366-148">Fa in modo che WMI scriva i dati di modifica della classe insieme alla definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="74366-148">Causes WMI to write class amendment data along with the base class definition.</span></span> <span data-ttu-id="74366-149">Per ulteriori informazioni sui qualificatori modificati, vedere [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="74366-149">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="74366-150">*objWbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="74366-150">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="74366-151">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="74366-151">Typically, this is undefined.</span></span> <span data-ttu-id="74366-152">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="74366-152">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="74366-153">Un provider che supporta o richiede queste informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="74366-153">A provider that supports or requires this information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="74366-154">*objWbemAsyncContext* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="74366-154">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="74366-155">Si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale.</span><span class="sxs-lookup"><span data-stu-id="74366-155">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="74366-156">Utilizzare questo parametro se si eseguono più chiamate asincrone utilizzando lo stesso sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="74366-156">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="74366-157">Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando.</span><span class="sxs-lookup"><span data-stu-id="74366-157">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="74366-158">Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="74366-158">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="74366-159">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="74366-159">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74366-160">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74366-160">Return value</span></span>

<span data-ttu-id="74366-161">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="74366-161">This method does not return a value.</span></span> <span data-ttu-id="74366-162">Se la chiamata ha esito positivo, l'evento [**OnObjectPut**](swbemsink-onobjectput.md) del sink di oggetto fornito riceve un oggetto [**SWbemObjectPath**](swbemobjectpath.md) che contiene il percorso dell'oggetto dell'istanza o della classe di cui è stato eseguito correttamente il commit in WMI.</span><span class="sxs-lookup"><span data-stu-id="74366-162">If the call is successful, the [**OnObjectPut**](swbemsink-onobjectput.md) event of the supplied object sink receives an [**SWbemObjectPath**](swbemobjectpath.md) object, containing the object path of the instance or class that is successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="74366-163">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="74366-163">Error codes</span></span>

<span data-ttu-id="74366-164">Dopo il completamento del metodo **PutAsync \_** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="74366-164">After the completion of the **PutAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="74366-165">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="74366-165">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="74366-166">L'utente corrente non dispone delle autorizzazioni necessarie per aggiornare un'istanza della classe specificata.</span><span class="sxs-lookup"><span data-stu-id="74366-166">Current user does not have permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="74366-167">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="74366-167">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="74366-168">È stato specificato il flag **wbemChangeFlagCreateOnly** , ma l'istanza esiste già.</span><span class="sxs-lookup"><span data-stu-id="74366-168">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="74366-169">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="74366-169">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="74366-170">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="74366-170">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="74366-171">**wbemErrIllegalNull** -2147749898 (0x8004100a)</span><span class="sxs-lookup"><span data-stu-id="74366-171">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="74366-172">Non è stato specificato **alcun** valore per una proprietà che non può essere **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="74366-172">A value of **Nothing** was specified for a property that may not be **Nothing**.</span></span> <span data-ttu-id="74366-173">Un esempio di tale proprietà è quello contrassegnato da un qualificatore di **chiave**, **indicizzato** o **Not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="74366-173">An example of such a property is one that is marked by a **Key**, **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="74366-174">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="74366-174">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="74366-175">L'istanza specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="74366-175">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="74366-176">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="74366-176">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="74366-177">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="74366-177">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="74366-178">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="74366-178">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="74366-179">È stato specificato il flag **wbemChangeFlagUpdateOnly** , ma l'istanza o la classe non esiste.</span><span class="sxs-lookup"><span data-stu-id="74366-179">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="74366-180">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="74366-180">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="74366-181">Le proprietà obbligatorie per le classi non sono state impostate.</span><span class="sxs-lookup"><span data-stu-id="74366-181">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="74366-182">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="74366-182">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="74366-183">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="74366-183">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74366-184">Commenti</span><span class="sxs-lookup"><span data-stu-id="74366-184">Remarks</span></span>

<span data-ttu-id="74366-185">Questa chiamata viene restituita immediatamente e il risultato dell'operazione **put** viene restituito al chiamante tramite callback recapitati al sink specificato in *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="74366-185">This call returns immediately, and the result of the **put** operation is returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="74366-186">Implementare *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="74366-186">Implement the *objWbemSink*.</span></span> <span data-ttu-id="74366-187">Metodo [**OnObjectPut**](swbemsink-onobjectput.md) per ottenere il percorso dell'oggetto dell'istanza o della classe che viene scritta nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="74366-187">[**OnObjectPut**](swbemsink-onobjectput.md) method to obtain the object path of the instance or class that is written to the WMI repository.</span></span> <span data-ttu-id="74366-188">Per ulteriori informazioni sui metodi sink, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="74366-188">For more information about sink methods, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="74366-189">Un callback asincrono consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="74366-189">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="74366-190">Questo comporta rischi per la sicurezza per gli script e le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="74366-190">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="74366-191">Per eliminare i rischi, utilizzare semisincrono o la comunicazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="74366-191">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="74366-192">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="74366-192">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74366-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74366-193">Requirements</span></span>



| <span data-ttu-id="74366-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="74366-194">Requirement</span></span> | <span data-ttu-id="74366-195">Valore</span><span class="sxs-lookup"><span data-stu-id="74366-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74366-196">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74366-196">Minimum supported client</span></span><br/> | <span data-ttu-id="74366-197">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74366-197">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="74366-198">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74366-198">Minimum supported server</span></span><br/> | <span data-ttu-id="74366-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74366-199">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="74366-200">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74366-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="74366-201"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="74366-201"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="74366-202">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="74366-202">Type library</span></span><br/>             | <dl> <span data-ttu-id="74366-203"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="74366-203"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="74366-204">DLL</span><span class="sxs-lookup"><span data-stu-id="74366-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74366-205"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74366-205"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="74366-206">CLSID</span><span class="sxs-lookup"><span data-stu-id="74366-206">CLSID</span></span><br/>                    | <span data-ttu-id="74366-207">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="74366-207">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="74366-208">IID</span><span class="sxs-lookup"><span data-stu-id="74366-208">IID</span></span><br/>                      | <span data-ttu-id="74366-209">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="74366-209">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="74366-210">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74366-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74366-211">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="74366-211">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="74366-212">**SWbemObjectPath. Class**</span><span class="sxs-lookup"><span data-stu-id="74366-212">**SWbemObjectPath.Class**</span></span>](swbemobjectpath-class.md)
</dt> <dt>

[<span data-ttu-id="74366-213">**SWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="74366-213">**SWbemProperty**</span></span>](swbemproperty.md)
</dt> <dt>

[<span data-ttu-id="74366-214">**Oggetto SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="74366-214">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

