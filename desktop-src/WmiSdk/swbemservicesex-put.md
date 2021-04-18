---
description: Restituisce un oggetto SWbemObjectPath che contiene il percorso dell'oggetto in cui sono stati scritti i dati.
ms.assetid: 1a9a718d-875d-4102-9d9d-3d10be162f58
ms.tgt_platform: multiple
title: Metodo SWbemServicesEx. Put (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.Put
- ISWbemServicesEx.Put
- ISWbemServicesEx.Put
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e495a38262e6b6f7dd8b67424b74db74c025be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309772"
---
# <a name="swbemservicesexput-method"></a><span data-ttu-id="13eaa-103">Metodo SWbemServicesEx. Put</span><span class="sxs-lookup"><span data-stu-id="13eaa-103">SWbemServicesEx.Put method</span></span>

<span data-ttu-id="13eaa-104">Il metodo **put** dell'oggetto [**SWbemServicesEx**](swbemservicesex.md) Salva l'oggetto nello spazio dei nomi associato all'oggetto e restituisce un oggetto [**SWbemObjectPath**](swbemobjectpath.md) che contiene il percorso dell'oggetto in cui sono stati scritti i dati.</span><span class="sxs-lookup"><span data-stu-id="13eaa-104">The **Put** method of the [**SWbemServicesEx**](swbemservicesex.md) object saves the object to the namespace bound to the object and returns an [**SWbemObjectPath**](swbemobjectpath.md) object that contains the path of the object to which the data was written.</span></span>

<span data-ttu-id="13eaa-105">Questo metodo viene chiamato in modalità semisincrono.</span><span class="sxs-lookup"><span data-stu-id="13eaa-105">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="13eaa-106">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="13eaa-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="13eaa-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="13eaa-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="13eaa-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13eaa-108">Syntax</span></span>


```VB
objObjectPath = .Put( _
  ByVal objWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="13eaa-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="13eaa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13eaa-110">*objWbemObject*</span><span class="sxs-lookup"><span data-stu-id="13eaa-110">*objWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="13eaa-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="13eaa-111">Required.</span></span> <span data-ttu-id="13eaa-112">Nuovo oggetto da inserire nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="13eaa-112">The new object to be put in the namespace.</span></span> <span data-ttu-id="13eaa-113">Può trattarsi di un oggetto appena creato o di un oggetto modificato.</span><span class="sxs-lookup"><span data-stu-id="13eaa-113">This can be either a newly created object or a modified object.</span></span>

</dd> <dt>

<span data-ttu-id="13eaa-114">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="13eaa-114">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="13eaa-115">Questo parametro determina se la chiamata crea o aggiorna l'oggetto e se la chiamata restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="13eaa-115">This parameter determines if the call creates or updates the object and if the call returns immediately.</span></span> <span data-ttu-id="13eaa-116">Questo parametro può accettare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="13eaa-116">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="13eaa-117"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="13eaa-117"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="13eaa-118">Consente di aggiornare una classe se non sono presenti classi derivate e non sono presenti istanze per tale classe.</span><span class="sxs-lookup"><span data-stu-id="13eaa-118">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="13eaa-119">Consente inoltre gli aggiornamenti in tutti i casi in cui la modifica riguarda solo i qualificatori non importanti (ad esempio, il qualificatore della **Descrizione** ).</span><span class="sxs-lookup"><span data-stu-id="13eaa-119">It also allows updates in all cases if the change is only to unimportant qualifiers (for example, the **Description** qualifier).</span></span> <span data-ttu-id="13eaa-120">Questo è il comportamento predefinito per questa chiamata e viene utilizzato per la compatibilità con le versioni precedenti di WMI.</span><span class="sxs-lookup"><span data-stu-id="13eaa-120">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="13eaa-121">Se la classe dispone di istanze, l'aggiornamento avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="13eaa-121">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="13eaa-122"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="13eaa-122"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="13eaa-123">Consente di aggiornare le classi anche se sono presenti classi figlio, quando la modifica non provoca conflitti con le classi figlio.</span><span class="sxs-lookup"><span data-stu-id="13eaa-123">Allows updates of classes even if there are child classes, when the change does not cause any conflicts with child classes.</span></span> <span data-ttu-id="13eaa-124">È possibile utilizzare questo flag quando si aggiunge una nuova proprietà a una classe di base non indicata in precedenza in nessuna delle classi figlio.</span><span class="sxs-lookup"><span data-stu-id="13eaa-124">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="13eaa-125">Se la classe dispone di istanze, l'aggiornamento avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="13eaa-125">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="13eaa-126"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="13eaa-126"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="13eaa-127">Questo flag forza gli aggiornamenti delle classi quando esistono classi figlio in conflitto.</span><span class="sxs-lookup"><span data-stu-id="13eaa-127">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="13eaa-128">Questo flag, ad esempio, impone un aggiornamento se è stato definito un qualificatore di classe in una classe figlio e la classe di base tenta di aggiungere lo stesso qualificatore in conflitto con quello esistente.</span><span class="sxs-lookup"><span data-stu-id="13eaa-128">For example, this flag forces an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="13eaa-129">In modalità Force questo conflitto viene risolto eliminando il qualificatore in conflitto nella classe figlio.</span><span class="sxs-lookup"><span data-stu-id="13eaa-129">In the force mode, this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="13eaa-130">Se la classe dispone di istanze, l'aggiornamento avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="13eaa-130">If the class has instances, the update fails.</span></span>

<span data-ttu-id="13eaa-131">L'uso della modalità Force per aggiornare una classe statica comporta l'eliminazione di tutte le istanze di tale classe.</span><span class="sxs-lookup"><span data-stu-id="13eaa-131">The use of the force mode to update a static class causes the deletion of all instances of that class.</span></span> <span data-ttu-id="13eaa-132">Un aggiornamento forzato in una classe provider non elimina le istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="13eaa-132">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="13eaa-133"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="13eaa-133"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="13eaa-134">Determina la creazione della classe o dell'istanza, se non esiste, oppure sovrascritta se esiste già.</span><span class="sxs-lookup"><span data-stu-id="13eaa-134">Causes the class or instance to be created if it does not exist, or overwritten if it already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="13eaa-135"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="13eaa-135"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="13eaa-136">Utilizzato solo per la creazione.</span><span class="sxs-lookup"><span data-stu-id="13eaa-136">Used for creation only.</span></span> <span data-ttu-id="13eaa-137">La chiamata ha esito negativo se la classe o l'istanza esiste già.</span><span class="sxs-lookup"><span data-stu-id="13eaa-137">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="13eaa-138"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="13eaa-138"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="13eaa-139">Fa in modo che la chiamata esegua solo un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="13eaa-139">Causes this call to only do an update.</span></span> <span data-ttu-id="13eaa-140">La classe o l'istanza deve esistere affinché la chiamata abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="13eaa-140">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="13eaa-141"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="13eaa-141"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="13eaa-142">Causa la restituzione immediata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="13eaa-142">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="13eaa-143"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="13eaa-143"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="13eaa-144">Causa il blocco della chiamata fino al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="13eaa-144">Causes this call to block until the operation has completed.</span></span> <span data-ttu-id="13eaa-145">Questo flag chiama il metodo in modalità sincrona.</span><span class="sxs-lookup"><span data-stu-id="13eaa-145">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="13eaa-146"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="13eaa-146"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="13eaa-147">Fa in modo che WMI scriva i dati di modifica della classe e la definizione della classe base.</span><span class="sxs-lookup"><span data-stu-id="13eaa-147">Causes WMI to write class amendment data as well as the base class definition.</span></span> <span data-ttu-id="13eaa-148">Per ulteriori informazioni, vedere la pagina relativa alla [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="13eaa-148">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="13eaa-149">*objWbemNamedValueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="13eaa-149">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="13eaa-150">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="13eaa-150">Typically, this is undefined.</span></span> <span data-ttu-id="13eaa-151">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che servizi la richiesta.</span><span class="sxs-lookup"><span data-stu-id="13eaa-151">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="13eaa-152">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="13eaa-152">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13eaa-153">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13eaa-153">Return value</span></span>

<span data-ttu-id="13eaa-154">Se la chiamata ha esito positivo, viene restituito un oggetto [**SWbemObjectPath**](swbemobjectpath.md) .</span><span class="sxs-lookup"><span data-stu-id="13eaa-154">If the call is successful, an [**SWbemObjectPath**](swbemobjectpath.md) object is returned.</span></span> <span data-ttu-id="13eaa-155">Questo oggetto contiene il percorso dell'oggetto dell'istanza o della classe di cui è stato eseguito correttamente il commit in WMI.</span><span class="sxs-lookup"><span data-stu-id="13eaa-155">This object contains the object path of the instance or class that has been successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="13eaa-156">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="13eaa-156">Error codes</span></span>

<span data-ttu-id="13eaa-157">Dopo il completamento del metodo **put** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="13eaa-157">After the completion of the **Put** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="13eaa-158">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="13eaa-158">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="13eaa-159">L'utente corrente non dispone dell'autorizzazione per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="13eaa-159">Current user does not have the permission for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="13eaa-160">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="13eaa-160">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="13eaa-161">È stato specificato il flag **wbemChangeFlagCreateOnly** , ma l'istanza esiste già.</span><span class="sxs-lookup"><span data-stu-id="13eaa-161">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="13eaa-162">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="13eaa-162">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="13eaa-163">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="13eaa-163">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="13eaa-164">**wbemErrIllegalNull** -2147749898 (0x8004100a)</span><span class="sxs-lookup"><span data-stu-id="13eaa-164">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="13eaa-165">È stato specificato un valore **null** per una proprietà che non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="13eaa-165">A value of **NULL** was specified for a property that cannot be **NULL**.</span></span> <span data-ttu-id="13eaa-166">Un esempio di tale proprietà è quello contrassegnato da un qualificatore di [**chiave**](standard-qualifiers.md), **indicizzato** o **Not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="13eaa-166">An example of such a property is one marked by a [**Key**](standard-qualifiers.md), **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="13eaa-167">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="13eaa-167">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="13eaa-168">L'oggetto specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="13eaa-168">The specified object is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="13eaa-169">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="13eaa-169">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="13eaa-170">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="13eaa-170">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="13eaa-171">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="13eaa-171">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="13eaa-172">È stato specificato il flag **wbemChangeFlagUpdateOnly** , ma l'istanza o la classe non esiste.</span><span class="sxs-lookup"><span data-stu-id="13eaa-172">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="13eaa-173">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="13eaa-173">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="13eaa-174">Le proprietà obbligatorie per le classi non sono state impostate.</span><span class="sxs-lookup"><span data-stu-id="13eaa-174">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="13eaa-175">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="13eaa-175">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="13eaa-176">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="13eaa-176">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13eaa-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13eaa-177">Requirements</span></span>



| <span data-ttu-id="13eaa-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="13eaa-178">Requirement</span></span> | <span data-ttu-id="13eaa-179">Valore</span><span class="sxs-lookup"><span data-stu-id="13eaa-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13eaa-180">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13eaa-180">Minimum supported client</span></span><br/> | <span data-ttu-id="13eaa-181">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13eaa-181">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13eaa-182">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13eaa-182">Minimum supported server</span></span><br/> | <span data-ttu-id="13eaa-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13eaa-183">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13eaa-184">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13eaa-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="13eaa-185"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="13eaa-185"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="13eaa-186">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="13eaa-186">Type library</span></span><br/>             | <dl> <span data-ttu-id="13eaa-187"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="13eaa-187"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="13eaa-188">DLL</span><span class="sxs-lookup"><span data-stu-id="13eaa-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13eaa-189"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13eaa-189"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="13eaa-190">CLSID</span><span class="sxs-lookup"><span data-stu-id="13eaa-190">CLSID</span></span><br/>                    | <span data-ttu-id="13eaa-191">\_ISWBEMSERVICESEX CLSID</span><span class="sxs-lookup"><span data-stu-id="13eaa-191">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="13eaa-192">IID</span><span class="sxs-lookup"><span data-stu-id="13eaa-192">IID</span></span><br/>                      | <span data-ttu-id="13eaa-193">\_ISWBEMSERVICESEX IID</span><span class="sxs-lookup"><span data-stu-id="13eaa-193">IID\_ISWbemServicesEx</span></span><br/>                                                        |



 

 




