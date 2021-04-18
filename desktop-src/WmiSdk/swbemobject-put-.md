---
description: Il \_ metodo Put di SWbemObject crea o aggiorna un'istanza o un oggetto classe per Strumentazione gestione Windows (WMI). È possibile utilizzare questo metodo dopo aver modificato le proprietà o i metodi in un SWbemObject e le modifiche vengono scritte in WMI.
ms.assetid: c636ff95-9f3e-4ba9-adf3-30b981be02a4
ms.tgt_platform: multiple
title: Metodo SWbemObject.Put_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Put_
- ISWbemObject.Put_
- ISWbemObject.Put_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9f5ca9b79c9def8f209da37e0ef1cfddefa0dbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309822"
---
# <a name="swbemobjectput_-method"></a><span data-ttu-id="2fe36-104">Metodo SWbemObject. put \_</span><span class="sxs-lookup"><span data-stu-id="2fe36-104">SWbemObject.Put\_ method</span></span>

<span data-ttu-id="2fe36-105">Il **metodo \_ put** di [**SWbemObject**](swbemobject.md) crea o aggiorna un'istanza o un oggetto classe per Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2fe36-105">The **Put\_** method of [**SWbemObject**](swbemobject.md) creates or updates an instance or a class object to Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="2fe36-106">È possibile utilizzare questo metodo dopo aver modificato le proprietà o i metodi in un **SWbemObject** e le modifiche vengono scritte in WMI.</span><span class="sxs-lookup"><span data-stu-id="2fe36-106">You can use this method after you modify any properties or methods in an **SWbemObject**, and your changes are written to WMI.</span></span>

<span data-ttu-id="2fe36-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2fe36-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2fe36-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fe36-108">Syntax</span></span>


```VB
objObjectPath = .Put_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2fe36-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2fe36-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fe36-110">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2fe36-110">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2fe36-111">Questo parametro determina se la chiamata crea o aggiorna la classe o l'istanza e se la chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="2fe36-111">This parameter determines if the call creates or updates the class or instance and if the call returns immediately.</span></span> <span data-ttu-id="2fe36-112">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2fe36-112">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="2fe36-113"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="2fe36-113"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>\*\*\*\*wbemChangeFlagUpdateCompatible\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2fe36-114">Consente di aggiornare una classe se non sono presenti classi derivate e non sono presenti istanze per tale classe.</span><span class="sxs-lookup"><span data-stu-id="2fe36-114">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="2fe36-115">Consente inoltre gli aggiornamenti in tutti i casi in cui la modifica riguarda solo i qualificatori non importanti (ad esempio, il qualificatore della **Descrizione** ).</span><span class="sxs-lookup"><span data-stu-id="2fe36-115">It also allows updates in all cases if the change is just to unimportant qualifiers (for example, the **Description** qualifier).</span></span> <span data-ttu-id="2fe36-116">Questo è il comportamento predefinito per questa chiamata e viene utilizzato per la compatibilità con le versioni precedenti di WMI.</span><span class="sxs-lookup"><span data-stu-id="2fe36-116">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="2fe36-117">Se la classe dispone di istanze, l'aggiornamento ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2fe36-117">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="2fe36-118"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="2fe36-118"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>\*\*\*\*wbemChangeFlagUpdateSafeMode\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="2fe36-119">Consente di aggiornare le classi anche se sono presenti classi figlio se la modifica non provoca conflitti con le classi figlio.</span><span class="sxs-lookup"><span data-stu-id="2fe36-119">Allows updates of classes even if there are child classes if the change does not cause any conflicts with child classes.</span></span> <span data-ttu-id="2fe36-120">È possibile utilizzare questo flag quando si aggiunge una nuova proprietà a una classe di base non indicata in precedenza in nessuna delle classi figlio.</span><span class="sxs-lookup"><span data-stu-id="2fe36-120">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="2fe36-121">Se la classe dispone di istanze, l'aggiornamento ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2fe36-121">If the class has instances the update fails.</span></span> <span data-ttu-id="2fe36-122">Se la classe dispone di istanze, l'aggiornamento ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2fe36-122">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="2fe36-123"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode \* \* \* \* (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="2fe36-123"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>\*\*\*\*WbemChangeFlagUpdateForceMode\*\*\*\* (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="2fe36-124">Questo flag forza gli aggiornamenti delle classi quando esistono classi figlio in conflitto.</span><span class="sxs-lookup"><span data-stu-id="2fe36-124">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="2fe36-125">Questo flag, ad esempio, forza un aggiornamento se è stato definito un qualificatore di classe in una classe figlio e la classe di base tenta di aggiungere lo stesso qualificatore e in conflitto con quello esistente.</span><span class="sxs-lookup"><span data-stu-id="2fe36-125">For example, this flag will force an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier and in conflict with the existing one.</span></span> <span data-ttu-id="2fe36-126">In modalità Force questo conflitto verrebbe risolto eliminando il qualificatore in conflitto nella classe figlio.</span><span class="sxs-lookup"><span data-stu-id="2fe36-126">In force mode this conflict would be resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="2fe36-127">Se la classe dispone di istanze, l'aggiornamento avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2fe36-127">If the class has instances the update will fail.</span></span>

<span data-ttu-id="2fe36-128">L'uso della modalità Force per aggiornare una classe statica comporta l'eliminazione di tutte le istanze di tale classe.</span><span class="sxs-lookup"><span data-stu-id="2fe36-128">Using force mode to update a static class results in the deletion of all instances of that class.</span></span> <span data-ttu-id="2fe36-129">Un aggiornamento forzato in una classe provider non elimina le istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="2fe36-129">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="2fe36-130"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="2fe36-130"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>\*\*\*\*wbemChangeFlagCreateOrUpdate\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2fe36-131">Determina la creazione della classe o dell'istanza se non esiste o sovrascritta se esiste già.</span><span class="sxs-lookup"><span data-stu-id="2fe36-131">Causes the class or instance to be created if it does not exist or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="2fe36-132"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="2fe36-132"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>\*\*\*\*wbemChangeFlagCreateOnly\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="2fe36-133">Utilizzato solo per la creazione.</span><span class="sxs-lookup"><span data-stu-id="2fe36-133">Used for creation only.</span></span> <span data-ttu-id="2fe36-134">La chiamata ha esito negativo se la classe o l'istanza esiste già.</span><span class="sxs-lookup"><span data-stu-id="2fe36-134">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="2fe36-135"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="2fe36-135"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>\*\*\*\*wbemChangeFlagUpdateOnly\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="2fe36-136">Causa l'aggiornamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="2fe36-136">Causes this call to update.</span></span> <span data-ttu-id="2fe36-137">La classe o l'istanza deve esistere affinché la chiamata abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2fe36-137">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="2fe36-138"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="2fe36-138"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="2fe36-139">Causa la restituzione immediata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="2fe36-139">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="2fe36-140"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="2fe36-140"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2fe36-141">Causa il blocco della chiamata fino al completamento della query.</span><span class="sxs-lookup"><span data-stu-id="2fe36-141">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="2fe36-142"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="2fe36-142"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="2fe36-143">Fa in modo che WMI scriva i dati di modifica della classe e la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="2fe36-143">Causes WMI to write class amendment data as well as the base class definition.</span></span> <span data-ttu-id="2fe36-144">Per ulteriori informazioni sui qualificatori modificati, vedere [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="2fe36-144">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2fe36-145">*objwbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2fe36-145">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2fe36-146">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="2fe36-146">Typically, this is undefined.</span></span> <span data-ttu-id="2fe36-147">In caso contrario, si tratta di un oggetto [**SWbemObjectPath**](swbemobjectpath.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="2fe36-147">Otherwise, this is an [**SWbemObjectPath**](swbemobjectpath.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="2fe36-148">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="2fe36-148">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fe36-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2fe36-149">Return value</span></span>

<span data-ttu-id="2fe36-150">Se la chiamata ha esito positivo, viene restituito un oggetto [**SWbemObjectPath**](swbemobjectpath.md) .</span><span class="sxs-lookup"><span data-stu-id="2fe36-150">If the call is successful, an [**SWbemObjectPath**](swbemobjectpath.md) object is returned.</span></span> <span data-ttu-id="2fe36-151">Questo oggetto contiene il percorso dell'oggetto dell'istanza o della classe di cui è stato eseguito correttamente il commit in WMI.</span><span class="sxs-lookup"><span data-stu-id="2fe36-151">This object contains the object path of the instance or class that has been successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2fe36-152">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2fe36-152">Error codes</span></span>

<span data-ttu-id="2fe36-153">Dopo il completamento del metodo **put \_** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="2fe36-153">After the completion of the **Put\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="2fe36-154">**wbemErrAccessDenied** -2147749891</span><span class="sxs-lookup"><span data-stu-id="2fe36-154">**wbemErrAccessDenied** - 2147749891</span></span>
</dt> <dd>

<span data-ttu-id="2fe36-155">L'utente corrente non dispone delle autorizzazioni necessarie per aggiornare un'istanza della classe specificata.</span><span class="sxs-lookup"><span data-stu-id="2fe36-155">Current user does not have permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="2fe36-156">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="2fe36-156">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="2fe36-157">È stato specificato il flag **wbemChangeFlagCreateOnly** , ma l'istanza esiste già.</span><span class="sxs-lookup"><span data-stu-id="2fe36-157">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2fe36-158">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="2fe36-158">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2fe36-159">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="2fe36-159">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="2fe36-160">**wbemErrIllegalNull** -2147749898 (0x8004100a)</span><span class="sxs-lookup"><span data-stu-id="2fe36-160">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="2fe36-161">Non è stato specificato **alcun** valore per una proprietà che non può essere **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="2fe36-161">A value of **Nothing** was specified for a property that may not be **Nothing**.</span></span> <span data-ttu-id="2fe36-162">Un esempio di tale proprietà è quello contrassegnato da un qualificatore di **chiave,** **indicizzato** o **Not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="2fe36-162">An example of such a property is one marked by a **Key,** **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="2fe36-163">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="2fe36-163">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="2fe36-164">L'istanza specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="2fe36-164">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2fe36-165">**wbemErrInvalidParameter** -0x80041008</span><span class="sxs-lookup"><span data-stu-id="2fe36-165">**wbemErrInvalidParameter** - 0x80041008</span></span>
</dt> <dd>

<span data-ttu-id="2fe36-166">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="2fe36-166">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2fe36-167">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="2fe36-167">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="2fe36-168">È stato specificato il flag **wbemChangeFlagUpdateOnly** , ma l'istanza o la classe non esiste.</span><span class="sxs-lookup"><span data-stu-id="2fe36-168">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="2fe36-169">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="2fe36-169">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="2fe36-170">Le proprietà obbligatorie per le classi non sono state impostate.</span><span class="sxs-lookup"><span data-stu-id="2fe36-170">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="2fe36-171">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="2fe36-171">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="2fe36-172">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="2fe36-172">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2fe36-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fe36-173">Requirements</span></span>



| <span data-ttu-id="2fe36-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fe36-174">Requirement</span></span> | <span data-ttu-id="2fe36-175">Valore</span><span class="sxs-lookup"><span data-stu-id="2fe36-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fe36-176">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fe36-176">Minimum supported client</span></span><br/> | <span data-ttu-id="2fe36-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fe36-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2fe36-178">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fe36-178">Minimum supported server</span></span><br/> | <span data-ttu-id="2fe36-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fe36-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2fe36-180">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2fe36-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fe36-181"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fe36-181"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2fe36-182">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2fe36-182">Type library</span></span><br/>             | <dl> <span data-ttu-id="2fe36-183"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2fe36-183"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2fe36-184">DLL</span><span class="sxs-lookup"><span data-stu-id="2fe36-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fe36-185"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fe36-185"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2fe36-186">CLSID</span><span class="sxs-lookup"><span data-stu-id="2fe36-186">CLSID</span></span><br/>                    | <span data-ttu-id="2fe36-187">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="2fe36-187">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="2fe36-188">IID</span><span class="sxs-lookup"><span data-stu-id="2fe36-188">IID</span></span><br/>                      | <span data-ttu-id="2fe36-189">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="2fe36-189">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="2fe36-190">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fe36-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fe36-191">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="2fe36-191">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="2fe36-192">**SWbemObjectPath. Class**</span><span class="sxs-lookup"><span data-stu-id="2fe36-192">**SWbemObjectPath.Class**</span></span>](swbemobjectpath-class.md)
</dt> <dt>

[<span data-ttu-id="2fe36-193">**SWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="2fe36-193">**SWbemProperty**</span></span>](swbemproperty.md)
</dt> <dt>

[<span data-ttu-id="2fe36-194">**Oggetto SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="2fe36-194">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

