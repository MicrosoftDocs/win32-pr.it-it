---
description: Descrive i codici di errore 8200-8999 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: Codici di errore di sistema (8200-8999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7500ae4c178999de8052b0858089604652dc5237
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225652"
---
# <a name="system-error-codes-8200-8999"></a><span data-ttu-id="93ba9-103">Codici di errore di sistema (8200-8999)</span><span class="sxs-lookup"><span data-stu-id="93ba9-103">System Error Codes (8200-8999)</span></span>

> [!NOTE]
> <span data-ttu-id="93ba9-104">Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="93ba9-105">Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="93ba9-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="93ba9-106">Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) per gli errori da 8200 a 8999.</span><span class="sxs-lookup"><span data-stu-id="93ba9-106">The following list describes [system error codes](system-error-codes.md) for errors 8200 to 8999.</span></span> <span data-ttu-id="93ba9-107">Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="93ba9-108">Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="93ba9-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="93ba9-109"><span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERRORE \_ DS \_ non \_ installato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-109"><span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERROR\_DS\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-110">8200 (0x2008)</span><span class="sxs-lookup"><span data-stu-id="93ba9-110">8200 (0x2008)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-111">Si è verificato un errore durante l'installazione del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="93ba9-111">An error occurred while installing the directory service.</span></span> <span data-ttu-id="93ba9-112">Per ulteriori informazioni, vedere il registro eventi.</span><span class="sxs-lookup"><span data-stu-id="93ba9-112">For more information, see the event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-113"><span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERRORE \_ di \_ appartenenza DS \_ valutato \_ localmente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-113"><span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERROR\_DS\_MEMBERSHIP\_EVALUATED\_LOCALLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-114">8201 (0x2009)</span><span class="sxs-lookup"><span data-stu-id="93ba9-114">8201 (0x2009)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-115">Il servizio directory ha valutato le appartenenze ai gruppi localmente.</span><span class="sxs-lookup"><span data-stu-id="93ba9-115">The directory service evaluated group memberships locally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-116"><span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERRORE \_ DS \_ nessun \_ attributo \_ o \_ valore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-116"><span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERROR\_DS\_NO\_ATTRIBUTE\_OR\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-117">8202 (0x200A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-117">8202 (0x200A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-118">Il valore o l'attributo del servizio di directory specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="93ba9-118">The specified directory service attribute or value does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-119"><span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERRORE della \_ sintassi degli attributi di DS \_ non valida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-119"><span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERROR\_DS\_INVALID\_ATTRIBUTE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-120">8203 (0x200B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-120">8203 (0x200B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-121">La sintassi dell'attributo specificata per il servizio directory non è valida.</span><span class="sxs-lookup"><span data-stu-id="93ba9-121">The attribute syntax specified to the directory service is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-122"><span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**\_tipo di attributo DS per errori non \_ \_ \_ definito**</span><span class="sxs-lookup"><span data-stu-id="93ba9-122"><span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**ERROR\_DS\_ATTRIBUTE\_TYPE\_UNDEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-123">8204 (0x200C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-123">8204 (0x200C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-124">Il tipo di attributo specificato per il servizio directory non è definito.</span><span class="sxs-lookup"><span data-stu-id="93ba9-124">The attribute type specified to the directory service is not defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-125"><span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**il \_ valore o l'attributo DS dell'errore \_ \_ \_ \_ esiste**</span><span class="sxs-lookup"><span data-stu-id="93ba9-125"><span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**ERROR\_DS\_ATTRIBUTE\_OR\_VALUE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-126">8205 (0x200D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-126">8205 (0x200D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-127">Il valore o l'attributo del servizio di directory specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="93ba9-127">The specified directory service attribute or value already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-128"><span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERRORE \_ DS \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-128"><span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERROR\_DS\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-129">8206 (0x200E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-129">8206 (0x200E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-130">Il servizio directory è occupato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-130">The directory service is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-131"><span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERRORE \_ DS non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="93ba9-131"><span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERROR\_DS\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-132">8207 (0x200F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-132">8207 (0x200F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-133">Il servizio directory non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="93ba9-133">The directory service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-134"><span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERRORE \_ DS \_ nessun \_ RID \_ allocato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-134"><span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERROR\_DS\_NO\_RIDS\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-135">8208 (0x2010)</span><span class="sxs-lookup"><span data-stu-id="93ba9-135">8208 (0x2010)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-136">Il servizio directory non è in grado di allocare l'identificatore relativo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-136">The directory service was unable to allocate a relative identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-137"><span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERRORE \_ DS \_ non \_ più \_ RID**</span><span class="sxs-lookup"><span data-stu-id="93ba9-137"><span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERROR\_DS\_NO\_MORE\_RIDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-138">8209 (0x2011)</span><span class="sxs-lookup"><span data-stu-id="93ba9-138">8209 (0x2011)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-139">Il servizio directory ha esaurito il pool di identificatori relativi.</span><span class="sxs-lookup"><span data-stu-id="93ba9-139">The directory service has exhausted the pool of relative identifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-140"><span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERRORE \_ DS \_ \_ proprietario ruolo \_ errato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-140"><span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERROR\_DS\_INCORRECT\_ROLE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-141">8210 (0x2012)</span><span class="sxs-lookup"><span data-stu-id="93ba9-141">8210 (0x2012)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-142">Non è stato possibile eseguire l'operazione richiesta perché il servizio directory non è il master per quel tipo di operazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-142">The requested operation could not be performed because the directory service is not the master for that type of operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-143"><span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**errore \_ di \_ inizializzazione di DS RIDMGR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-143"><span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**ERROR\_DS\_RIDMGR\_INIT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-144">8211 (0x2013)</span><span class="sxs-lookup"><span data-stu-id="93ba9-144">8211 (0x2013)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-145">Il servizio directory non è stato in grado di inizializzare il sottosistema che alloca gli identificatori relativi.</span><span class="sxs-lookup"><span data-stu-id="93ba9-145">The directory service was unable to initialize the subsystem that allocates relative identifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-146"><span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**\_violazione della \_ \_ classe obj \_ di errore DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-146"><span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**ERROR\_DS\_OBJ\_CLASS\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-147">8212 (0x2014)</span><span class="sxs-lookup"><span data-stu-id="93ba9-147">8212 (0x2014)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-148">L'operazione richiesta non soddisfa uno o più vincoli associati alla classe dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-148">The requested operation did not satisfy one or more constraints associated with the class of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-149"><span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERRORE \_ DS \_ \_ non in \_ \_ foglia**</span><span class="sxs-lookup"><span data-stu-id="93ba9-149"><span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERROR\_DS\_CANT\_ON\_NON\_LEAF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-150">8213 (0x2015)</span><span class="sxs-lookup"><span data-stu-id="93ba9-150">8213 (0x2015)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-151">Il servizio directory è in grado di eseguire l'operazione richiesta solo su un oggetto foglia.</span><span class="sxs-lookup"><span data-stu-id="93ba9-151">The directory service can perform the requested operation only on a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-152"><span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**errore \_ DS \_ \_ di errore su \_ RDN**</span><span class="sxs-lookup"><span data-stu-id="93ba9-152"><span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**ERROR\_DS\_CANT\_ON\_RDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-153">8214 (0x2016)</span><span class="sxs-lookup"><span data-stu-id="93ba9-153">8214 (0x2016)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-154">Il servizio directory non è in grado di eseguire l'operazione richiesta sull'attributo RDN di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-154">The directory service cannot perform the requested operation on the RDN attribute of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-155"><span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERRORE \_ DS \_ \_ mod cant \_ \_ classe obj**</span><span class="sxs-lookup"><span data-stu-id="93ba9-155"><span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERROR\_DS\_CANT\_MOD\_OBJ\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-156">8215 (0x2017)</span><span class="sxs-lookup"><span data-stu-id="93ba9-156">8215 (0x2017)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-157">Il servizio directory ha rilevato un tentativo di modificare la classe di oggetti di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-157">The directory service detected an attempt to modify the object class of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-158"><span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**errore \_ di \_ \_ trasferimento Dom \_ tra \_ i DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-158"><span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**ERROR\_DS\_CROSS\_DOM\_MOVE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-159">8216 (0x2018)</span><span class="sxs-lookup"><span data-stu-id="93ba9-159">8216 (0x2018)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-160">Non è stato possibile eseguire l'operazione di spostamento tra domini richiesta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-160">The requested cross-domain move operation could not be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-161"><span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERRORE \_ \_ GC DS \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="93ba9-161"><span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERROR\_DS\_GC\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-162">8217 (0x2019)</span><span class="sxs-lookup"><span data-stu-id="93ba9-162">8217 (0x2019)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-163">Impossibile contattare il server di catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="93ba9-163">Unable to contact the global catalog server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-164"><span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**ERRORE \_ di \_ criteri condivisi**</span><span class="sxs-lookup"><span data-stu-id="93ba9-164"><span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**ERROR\_SHARED\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-165">8218 (0x201A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-165">8218 (0x201A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-166">L'oggetto criteri è condiviso e può essere modificato solo alla radice.</span><span class="sxs-lookup"><span data-stu-id="93ba9-166">The policy object is shared and can only be modified at the root.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-167"><span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**\_ \_ \_ Impossibile trovare l'oggetto Criteri di errore \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-167"><span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**ERROR\_POLICY\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-168">8219 (0x201B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-168">8219 (0x201B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-169">L'oggetto criteri non esiste.</span><span class="sxs-lookup"><span data-stu-id="93ba9-169">The policy object does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-170"><span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**\_criteri \_ di errore solo \_ in \_ DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-170"><span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**ERROR\_POLICY\_ONLY\_IN\_DS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-171">8220 (0x201C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-171">8220 (0x201C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-172">Le informazioni sui criteri richieste sono solo nel servizio directory.</span><span class="sxs-lookup"><span data-stu-id="93ba9-172">The requested policy information is only in the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-173"><span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**promozione dell'errore \_ \_ attiva**</span><span class="sxs-lookup"><span data-stu-id="93ba9-173"><span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**ERROR\_PROMOTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-174">8221 (0x201D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-174">8221 (0x201D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-175">Una promozione del controller di dominio è attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="93ba9-175">A domain controller promotion is currently active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-176"><span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERRORE \_ Nessuna \_ Promozione \_ attiva**</span><span class="sxs-lookup"><span data-stu-id="93ba9-176"><span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERROR\_NO\_PROMOTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-177">8222 (0x201E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-177">8222 (0x201E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-178">Una promozione del controller di dominio non è attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="93ba9-178">A domain controller promotion is not currently active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-179"><span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**errore \_ operazioni DS errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-179"><span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**ERROR\_DS\_OPERATIONS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-180">8224 (0x2020)</span><span class="sxs-lookup"><span data-stu-id="93ba9-180">8224 (0x2020)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-181">Si è verificato un errore operativo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-181">An operations error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-182"><span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**errore \_ del \_ protocollo DS di errore \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-182"><span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**ERROR\_DS\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-183">8225 (0x2021)</span><span class="sxs-lookup"><span data-stu-id="93ba9-183">8225 (0x2021)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-184">Si è verificato un errore di protocollo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-184">A protocol error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-185"><span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**superato il limite di timeout \_ DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-185"><span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**ERROR\_DS\_TIMELIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-186">8226 (0x2022)</span><span class="sxs-lookup"><span data-stu-id="93ba9-186">8226 (0x2022)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-187">È stato superato il limite di tempo per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-187">The time limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-188"><span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERRORE \_ DS \_ SIZELIMIT \_ superato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-188"><span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERROR\_DS\_SIZELIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-189">8227 (0x2023)</span><span class="sxs-lookup"><span data-stu-id="93ba9-189">8227 (0x2023)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-190">È stato superato il limite di dimensioni per questa richiesta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-190">The size limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-191"><span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**\_ \_ superato limite di amministrazione DS \_ per \_ errori**</span><span class="sxs-lookup"><span data-stu-id="93ba9-191"><span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**ERROR\_DS\_ADMIN\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-192">8228 (0x2024)</span><span class="sxs-lookup"><span data-stu-id="93ba9-192">8228 (0x2024)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-193">Il limite amministrativo per questa richiesta è stato superato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-193">The administrative limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-194"><span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERRORE \_ DS \_ confronto \_ false**</span><span class="sxs-lookup"><span data-stu-id="93ba9-194"><span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERROR\_DS\_COMPARE\_FALSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-195">8229 (0x2025)</span><span class="sxs-lookup"><span data-stu-id="93ba9-195">8229 (0x2025)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-196">La risposta di confronto è false.</span><span class="sxs-lookup"><span data-stu-id="93ba9-196">The compare response was false.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-197"><span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERRORE \_ DS \_ compare \_ true**</span><span class="sxs-lookup"><span data-stu-id="93ba9-197"><span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERROR\_DS\_COMPARE\_TRUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-198">8230 (0x2026)</span><span class="sxs-lookup"><span data-stu-id="93ba9-198">8230 (0x2026)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-199">La risposta di confronto è vera.</span><span class="sxs-lookup"><span data-stu-id="93ba9-199">The compare response was true.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-200"><span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**il \_ metodo di autenticazione DS con errori \_ non è \_ \_ \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-200"><span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**ERROR\_DS\_AUTH\_METHOD\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-201">8231 (0x2027)</span><span class="sxs-lookup"><span data-stu-id="93ba9-201">8231 (0x2027)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-202">Il metodo di autenticazione richiesto non è supportato dal server.</span><span class="sxs-lookup"><span data-stu-id="93ba9-202">The requested authentication method is not supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-203"><span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERRORE \_ \_ autenticazione avanzata \_ DS \_ necessaria**</span><span class="sxs-lookup"><span data-stu-id="93ba9-203"><span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERROR\_DS\_STRONG\_AUTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-204">8232 (0x2028)</span><span class="sxs-lookup"><span data-stu-id="93ba9-204">8232 (0x2028)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-205">Per questo server è necessario un metodo di autenticazione più sicuro.</span><span class="sxs-lookup"><span data-stu-id="93ba9-205">A more secure authentication method is required for this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-206"><span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**\_autenticazione non \_ appropriata di DS per gli errori \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-206"><span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**ERROR\_DS\_INAPPROPRIATE\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-207">8233 (0x2029)</span><span class="sxs-lookup"><span data-stu-id="93ba9-207">8233 (0x2029)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-208">Autenticazione non appropriata.</span><span class="sxs-lookup"><span data-stu-id="93ba9-208">Inappropriate authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-209"><span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERRORE \_ di \_ autenticazione DS non \_ noto**</span><span class="sxs-lookup"><span data-stu-id="93ba9-209"><span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERROR\_DS\_AUTH\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-210">8234 (0x202A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-210">8234 (0x202A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-211">Il meccanismo di autenticazione è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-211">The authentication mechanism is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-212"><span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**\_segnalazione errori DS \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-212"><span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**ERROR\_DS\_REFERRAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-213">8235 (0x202B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-213">8235 (0x202B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-214">Il server ha restituito un riferimento.</span><span class="sxs-lookup"><span data-stu-id="93ba9-214">A referral was returned from the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-215"><span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**ERRORE \_ DS non disponibile per l' \_ \_ estensione del critico \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-215"><span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**ERROR\_DS\_UNAVAILABLE\_CRIT\_EXTENSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-216">8236 (0x202C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-216">8236 (0x202C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-217">Il server non supporta l'estensione critica richiesta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-217">The server does not support the requested critical extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-218"><span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**ERRORE \_ \_ riservato DS \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="93ba9-218"><span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**ERROR\_DS\_CONFIDENTIALITY\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-219">8237 (0x202D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-219">8237 (0x202D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-220">Questa richiesta richiede una connessione protetta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-220">This request requires a secure connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-221"><span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERRORE \_ DS non \_ appropriato \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-221"><span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERROR\_DS\_INAPPROPRIATE\_MATCHING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-222">8238 (0x202E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-222">8238 (0x202E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-223">Corrispondenza non appropriata.</span><span class="sxs-lookup"><span data-stu-id="93ba9-223">Inappropriate matching.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-224"><span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**\_violazione del \_ vincolo \_ DS di errore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-224"><span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**ERROR\_DS\_CONSTRAINT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-225">8239 (0x202F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-225">8239 (0x202F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-226">Si è verificata una violazione del vincolo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-226">A constraint violation occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-227"><span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERRORE \_ DS \_ nessun \_ oggetto di questo tipo \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-227"><span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERROR\_DS\_NO\_SUCH\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-228">8240 (0x2030)</span><span class="sxs-lookup"><span data-stu-id="93ba9-228">8240 (0x2030)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-229">Oggetto inesistente sul server.</span><span class="sxs-lookup"><span data-stu-id="93ba9-229">There is no such object on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-230"><span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**\_ \_ problema alias DS \_ errore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-230"><span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**ERROR\_DS\_ALIAS\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-231">8241 (0x2031)</span><span class="sxs-lookup"><span data-stu-id="93ba9-231">8241 (0x2031)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-232">Si è verificato un problema di alias.</span><span class="sxs-lookup"><span data-stu-id="93ba9-232">There is an alias problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-233"><span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERRORE \_ DS \_ \_ sintassi DN non valida \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-233"><span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERROR\_DS\_INVALID\_DN\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-234">8242 (0x2032)</span><span class="sxs-lookup"><span data-stu-id="93ba9-234">8242 (0x2032)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-235">È stata specificata una sintassi DN non valida.</span><span class="sxs-lookup"><span data-stu-id="93ba9-235">An invalid dn syntax has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-236"><span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**l'errore \_ DS \_ è \_ foglia**</span><span class="sxs-lookup"><span data-stu-id="93ba9-236"><span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**ERROR\_DS\_IS\_LEAF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-237">8243 (0x2033)</span><span class="sxs-lookup"><span data-stu-id="93ba9-237">8243 (0x2033)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-238">L'oggetto è un oggetto foglia.</span><span class="sxs-lookup"><span data-stu-id="93ba9-238">The object is a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-239"><span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**ERRORE \_ \_ Deref alias \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-239"><span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**ERROR\_DS\_ALIAS\_DEREF\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-240">8244 (0x2034)</span><span class="sxs-lookup"><span data-stu-id="93ba9-240">8244 (0x2034)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-241">Si è verificato un problema di dereferenziazione dell'alias.</span><span class="sxs-lookup"><span data-stu-id="93ba9-241">There is an alias dereferencing problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-242"><span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERRORE \_ DS \_ che non verrà \_ \_ eseguito**</span><span class="sxs-lookup"><span data-stu-id="93ba9-242"><span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERROR\_DS\_UNWILLING\_TO\_PERFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-243">8245 (0x2035)</span><span class="sxs-lookup"><span data-stu-id="93ba9-243">8245 (0x2035)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-244">Il server non è in funzione di elaborare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-244">The server is unwilling to process the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-245"><span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**\_ \_ rilevamento ciclo DS \_ errore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-245"><span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**ERROR\_DS\_LOOP\_DETECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-246">8246 (0x2036)</span><span class="sxs-lookup"><span data-stu-id="93ba9-246">8246 (0x2036)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-247">È stato rilevato un ciclo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-247">A loop has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-248"><span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**\_violazione di \_ denominazione \_ DS errore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-248"><span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**ERROR\_DS\_NAMING\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-249">8247 (0x2037)</span><span class="sxs-lookup"><span data-stu-id="93ba9-249">8247 (0x2037)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-250">Si è verificata una violazione di denominazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-250">There is a naming violation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-251"><span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**ERRORE \_ \_ dei risultati di un oggetto DS \_ \_ troppo \_ grande**</span><span class="sxs-lookup"><span data-stu-id="93ba9-251"><span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**ERROR\_DS\_OBJECT\_RESULTS\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-252">8248 (0x2038)</span><span class="sxs-lookup"><span data-stu-id="93ba9-252">8248 (0x2038)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-253">Il set di risultati è troppo grande.</span><span class="sxs-lookup"><span data-stu-id="93ba9-253">The result set is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-254"><span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**ERRORE \_ DS \_ influiscono su \_ più \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="93ba9-254"><span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**ERROR\_DS\_AFFECTS\_MULTIPLE\_DSAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-255">8249 (0x2039)</span><span class="sxs-lookup"><span data-stu-id="93ba9-255">8249 (0x2039)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-256">L'operazione ha effetto su più DSA.</span><span class="sxs-lookup"><span data-stu-id="93ba9-256">The operation affects multiple DSAs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-257"><span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERRORE \_ nel \_ server \_ DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-257"><span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERROR\_DS\_SERVER\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-258">8250 (0x203A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-258">8250 (0x203A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-259">Il server non è operativo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-259">The server is not operational.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-260"><span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**errore \_ locale DS errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-260"><span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**ERROR\_DS\_LOCAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-261">8251 (0x203B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-261">8251 (0x203B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-262">Si è verificato un errore locale.</span><span class="sxs-lookup"><span data-stu-id="93ba9-262">A local error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-263"><span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**errore \_ di \_ codifica DS errore \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-263"><span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**ERROR\_DS\_ENCODING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-264">8252 (0x203C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-264">8252 (0x203C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-265">Si è verificato un errore di codifica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-265">An encoding error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-266"><span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**\_errore di \_ decodifica DS di errore \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-266"><span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**ERROR\_DS\_DECODING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-267">8253 (0x203D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-267">8253 (0x203D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-268">Si è verificato un errore di decodifica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-268">A decoding error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-269"><span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERRORE \_ \_ filtro DS \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="93ba9-269"><span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERROR\_DS\_FILTER\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-270">8254 (0x203E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-270">8254 (0x203E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-271">Impossibile riconoscere il filtro di ricerca.</span><span class="sxs-lookup"><span data-stu-id="93ba9-271">The search filter cannot be recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-272"><span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**errore \_ di \_ param DS errore \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-272"><span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**ERROR\_DS\_PARAM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-273">8255 (0x203F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-273">8255 (0x203F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-274">Uno o più parametri non sono validi.</span><span class="sxs-lookup"><span data-stu-id="93ba9-274">One or more parameters are illegal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-275"><span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERRORE \_ DS \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-275"><span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERROR\_DS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-276">8256 (0x2040)</span><span class="sxs-lookup"><span data-stu-id="93ba9-276">8256 (0x2040)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-277">Il metodo specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-277">The specified method is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-278"><span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERRORE \_ DS \_ nessun \_ risultato \_ restituito**</span><span class="sxs-lookup"><span data-stu-id="93ba9-278"><span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERROR\_DS\_NO\_RESULTS\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-279">8257 (0x2041)</span><span class="sxs-lookup"><span data-stu-id="93ba9-279">8257 (0x2041)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-280">Nessun risultato restituito.</span><span class="sxs-lookup"><span data-stu-id="93ba9-280">No results were returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-281"><span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**ERRORE \_ \_ controllo DS \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-281"><span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**ERROR\_DS\_CONTROL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-282">8258 (0x2042)</span><span class="sxs-lookup"><span data-stu-id="93ba9-282">8258 (0x2042)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-283">Il controllo specificato non è supportato dal server.</span><span class="sxs-lookup"><span data-stu-id="93ba9-283">The specified control is not supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-284"><span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERRORE \_ \_ ciclo client \_ DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-284"><span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERROR\_DS\_CLIENT\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-285">8259 (0x2043)</span><span class="sxs-lookup"><span data-stu-id="93ba9-285">8259 (0x2043)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-286">Il client ha rilevato un ciclo di riferimento.</span><span class="sxs-lookup"><span data-stu-id="93ba9-286">A referral loop was detected by the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-287"><span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**\_limite di riferimento DS per errori \_ \_ \_ superato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-287"><span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**ERROR\_DS\_REFERRAL\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-288">8260 (0x2044)</span><span class="sxs-lookup"><span data-stu-id="93ba9-288">8260 (0x2044)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-289">È stato superato il limite di riferimento del set di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="93ba9-289">The preset referral limit was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-290"><span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERRORE \_ \_ controllo ordinamento \_ DS \_ mancante**</span><span class="sxs-lookup"><span data-stu-id="93ba9-290"><span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERROR\_DS\_SORT\_CONTROL\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-291">8261 (0x2045)</span><span class="sxs-lookup"><span data-stu-id="93ba9-291">8261 (0x2045)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-292">La ricerca richiede un controllo SORT.</span><span class="sxs-lookup"><span data-stu-id="93ba9-292">The search requires a SORT control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-293"><span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**\_errore di \_ intervallo di offset DS \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-293"><span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**ERROR\_DS\_OFFSET\_RANGE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-294">8262 (0x2046)</span><span class="sxs-lookup"><span data-stu-id="93ba9-294">8262 (0x2046)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-295">I risultati della ricerca superano l'intervallo di offset specificato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-295">The search results exceed the offset range specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-296"><span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERRORE \_ DS \_ RIDMGR \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-296"><span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERROR\_DS\_RIDMGR\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-297">8263 (0x2047)</span><span class="sxs-lookup"><span data-stu-id="93ba9-297">8263 (0x2047)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-298">Il servizio directory ha rilevato che il sottosistema che alloca gli identificatori relativi è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-298">The directory service detected the subsystem that allocates relative identifiers is disabled.</span></span> <span data-ttu-id="93ba9-299">Questo può verificarsi come meccanismo di protezione quando il sistema determina che una parte significativa degli identificatori relativi (RID) è stata esaurita.</span><span class="sxs-lookup"><span data-stu-id="93ba9-299">This can occur as a protective mechanism when the system determines a significant portion of relative identifiers (RIDs) have been exhausted.</span></span> <span data-ttu-id="93ba9-300"><https://go.microsoft.com/fwlink/p/?linkid=228610>Per la procedura di riabilitazione della creazione dell'account, vedere la procedura consigliata per la procedura di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-300">Please see <https://go.microsoft.com/fwlink/p/?linkid=228610> for recommended diagnostic steps and the procedure to re-enable account creation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-301"><span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**ERRORE \_ DS \_ radice \_ deve \_ essere \_ NC**</span><span class="sxs-lookup"><span data-stu-id="93ba9-301"><span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**ERROR\_DS\_ROOT\_MUST\_BE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-302">8301 (0x206D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-302">8301 (0x206D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-303">L'oggetto radice deve essere il capo di un contesto dei nomi.</span><span class="sxs-lookup"><span data-stu-id="93ba9-303">The root object must be the head of a naming context.</span></span> <span data-ttu-id="93ba9-304">L'oggetto radice non può avere un elemento padre di cui è stata creata un'istanza.</span><span class="sxs-lookup"><span data-stu-id="93ba9-304">The root object cannot have an instantiated parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-305"><span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERRORE \_ DS \_ aggiunta \_ replica \_ inibita**</span><span class="sxs-lookup"><span data-stu-id="93ba9-305"><span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERROR\_DS\_ADD\_REPLICA\_INHIBITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-306">8302 (0x206E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-306">8302 (0x206E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-307">Impossibile eseguire l'operazione di aggiunta replica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-307">The add replica operation cannot be performed.</span></span> <span data-ttu-id="93ba9-308">Per creare la replica, il contesto dei nomi deve essere scrivibile.</span><span class="sxs-lookup"><span data-stu-id="93ba9-308">The naming context must be writeable in order to create the replica.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-309"><span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERRORE \_ DS \_ att \_ non \_ def \_ nello \_ schema**</span><span class="sxs-lookup"><span data-stu-id="93ba9-309"><span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERROR\_DS\_ATT\_NOT\_DEF\_IN\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-310">8303 (0x206F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-310">8303 (0x206F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-311">Si è verificato un riferimento a un attributo non definito nello schema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-311">A reference to an attribute that is not defined in the schema occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-312"><span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**\_ \_ dimensioni massime \_ obj errore DS \_ \_ superate**</span><span class="sxs-lookup"><span data-stu-id="93ba9-312"><span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**ERROR\_DS\_MAX\_OBJ\_SIZE\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-313">8304 (0x2070)</span><span class="sxs-lookup"><span data-stu-id="93ba9-313">8304 (0x2070)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-314">È stata superata la dimensione massima di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-314">The maximum size of an object has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-315"><span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**ERRORE \_ DS \_ \_ nome stringa \_ obj \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-315"><span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**ERROR\_DS\_OBJ\_STRING\_NAME\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-316">8305 (0x2071)</span><span class="sxs-lookup"><span data-stu-id="93ba9-316">8305 (0x2071)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-317">È stato effettuato un tentativo di aggiungere un oggetto alla directory con un nome già in uso.</span><span class="sxs-lookup"><span data-stu-id="93ba9-317">An attempt was made to add an object to the directory with a name that is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-318"><span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERRORE \_ DS \_ nessun \_ RDN \_ definito \_ nello \_ schema**</span><span class="sxs-lookup"><span data-stu-id="93ba9-318"><span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERROR\_DS\_NO\_RDN\_DEFINED\_IN\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-319">8306 (0x2072)</span><span class="sxs-lookup"><span data-stu-id="93ba9-319">8306 (0x2072)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-320">È stato effettuato un tentativo di aggiungere un oggetto di una classe che non dispone di un RDN definito nello schema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-320">An attempt was made to add an object of a class that does not have an RDN defined in the schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-321"><span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**ERRORE \_ directory \_ RDN non \_ \_ corrispondente \_ schema**</span><span class="sxs-lookup"><span data-stu-id="93ba9-321"><span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**ERROR\_DS\_RDN\_DOESNT\_MATCH\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-322">8307 (0x2073)</span><span class="sxs-lookup"><span data-stu-id="93ba9-322">8307 (0x2073)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-323">È stato effettuato un tentativo di aggiungere un oggetto utilizzando un RDN che non è il RDN definito nello schema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-323">An attempt was made to add an object using an RDN that is not the RDN defined in the schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-324"><span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERRORE \_ DS \_ nessun \_ \_ atts richiesto \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-324"><span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERROR\_DS\_NO\_REQUESTED\_ATTS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-325">8308 (0x2074)</span><span class="sxs-lookup"><span data-stu-id="93ba9-325">8308 (0x2074)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-326">Nessuno degli attributi richiesti è stato trovato negli oggetti.</span><span class="sxs-lookup"><span data-stu-id="93ba9-326">None of the requested attributes were found on the objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-327"><span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERRORE \_ del \_ buffer utente DS \_ \_ su \_ Small**</span><span class="sxs-lookup"><span data-stu-id="93ba9-327"><span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERROR\_DS\_USER\_BUFFER\_TO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-328">8309 (0x2075)</span><span class="sxs-lookup"><span data-stu-id="93ba9-328">8309 (0x2075)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-329">Il buffer utente è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-329">The user buffer is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-330"><span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**ERRORE \_ DS \_ att \_ \_ non è \_ in \_ obj**</span><span class="sxs-lookup"><span data-stu-id="93ba9-330"><span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**ERROR\_DS\_ATT\_IS\_NOT\_ON\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-331">8310 (0x2076)</span><span class="sxs-lookup"><span data-stu-id="93ba9-331">8310 (0x2076)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-332">L'attributo specificato nell'operazione non è presente nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-332">The attribute specified in the operation is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-333"><span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERRORE \_ DS \_ - \_ operazione mod non valida \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-333"><span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERROR\_DS\_ILLEGAL\_MOD\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-334">8311 (0x2077)</span><span class="sxs-lookup"><span data-stu-id="93ba9-334">8311 (0x2077)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-335">Operazione di modifica non valida.</span><span class="sxs-lookup"><span data-stu-id="93ba9-335">Illegal modify operation.</span></span> <span data-ttu-id="93ba9-336">Alcuni aspetti della modifica non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="93ba9-336">Some aspect of the modification is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-337"><span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**ERRORE \_ DS \_ obj \_ troppo \_ grande**</span><span class="sxs-lookup"><span data-stu-id="93ba9-337"><span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**ERROR\_DS\_OBJ\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-338">8312 (0x2078)</span><span class="sxs-lookup"><span data-stu-id="93ba9-338">8312 (0x2078)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-339">L'oggetto specificato è troppo grande.</span><span class="sxs-lookup"><span data-stu-id="93ba9-339">The specified object is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-340"><span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERRORE \_ DS \_ \_ tipo istanza non valida \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-340"><span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERROR\_DS\_BAD\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-341">8313 (0x2079)</span><span class="sxs-lookup"><span data-stu-id="93ba9-341">8313 (0x2079)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-342">Il tipo di istanza specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="93ba9-342">The specified instance type is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-343"><span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERRORE \_ DS \_ MASTERDSA \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="93ba9-343"><span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERROR\_DS\_MASTERDSA\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-344">8314 (0x207A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-344">8314 (0x207A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-345">L'operazione deve essere eseguita in un DSA master.</span><span class="sxs-lookup"><span data-stu-id="93ba9-345">The operation must be performed at a master DSA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-346"><span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**\_classe dell'oggetto DS di errore \_ \_ \_ obbligatoria**</span><span class="sxs-lookup"><span data-stu-id="93ba9-346"><span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**ERROR\_DS\_OBJECT\_CLASS\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-347">8315 (0x207B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-347">8315 (0x207B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-348">È necessario specificare l'attributo della classe di oggetti.</span><span class="sxs-lookup"><span data-stu-id="93ba9-348">The object class attribute must be specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-349"><span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**ERRORE \_ DS \_ manca \_ l' \_ att obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="93ba9-349"><span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**ERROR\_DS\_MISSING\_REQUIRED\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-350">8316 (0x207C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-350">8316 (0x207C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-351">Attributo obbligatorio mancante.</span><span class="sxs-lookup"><span data-stu-id="93ba9-351">A required attribute is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-352"><span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERRORE \_ DS \_ att \_ non \_ def \_ per la \_ classe**</span><span class="sxs-lookup"><span data-stu-id="93ba9-352"><span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERROR\_DS\_ATT\_NOT\_DEF\_FOR\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-353">8317 (0x207D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-353">8317 (0x207D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-354">È stato effettuato un tentativo di modificare un oggetto per includere un attributo che non è valido per la relativa classe.</span><span class="sxs-lookup"><span data-stu-id="93ba9-354">An attempt was made to modify an object to include an attribute that is not legal for its class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-355"><span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**ERRORE \_ DS \_ att \_ già \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-355"><span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**ERROR\_DS\_ATT\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-356">8318 (0x207E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-356">8318 (0x207E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-357">L'attributo specificato è già presente nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-357">The specified attribute is already present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-358"><span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERRORE non è stato \_ \_ aggiunto alcun \_ \_ \_ valore att di DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-358"><span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERROR\_DS\_CANT\_ADD\_ATT\_VALUES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-359">8320 (0x2080)</span><span class="sxs-lookup"><span data-stu-id="93ba9-359">8320 (0x2080)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-360">L'attributo specificato non è presente o non ha valori.</span><span class="sxs-lookup"><span data-stu-id="93ba9-360">The specified attribute is not present, or has no values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-361"><span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERRORE \_ DS \_ \_ valore singolo \_ vincolo**</span><span class="sxs-lookup"><span data-stu-id="93ba9-361"><span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERROR\_DS\_SINGLE\_VALUE\_CONSTRAINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-362">8321 (0x2081)</span><span class="sxs-lookup"><span data-stu-id="93ba9-362">8321 (0x2081)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-363">Sono stati specificati più valori per un attributo che può avere un solo valore.</span><span class="sxs-lookup"><span data-stu-id="93ba9-363">Multiple values were specified for an attribute that can have only one value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-364"><span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**ERRORE \_ \_ vincolo intervallo \_ DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-364"><span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**ERROR\_DS\_RANGE\_CONSTRAINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-365">8322 (0x2082)</span><span class="sxs-lookup"><span data-stu-id="93ba9-365">8322 (0x2082)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-366">Un valore per l'attributo non è compreso nell'intervallo di valori accettabile.</span><span class="sxs-lookup"><span data-stu-id="93ba9-366">A value for the attribute was not in the acceptable range of values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-367"><span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**ERRORE \_ DS \_ att \_ Val \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="93ba9-367"><span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**ERROR\_DS\_ATT\_VAL\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-368">8323 (0x2083)</span><span class="sxs-lookup"><span data-stu-id="93ba9-368">8323 (0x2083)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-369">Il valore specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="93ba9-369">The specified value already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-370"><span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERRORE \_ REM cant di DS non \_ \_ \_ presente \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-370"><span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERROR\_DS\_CANT\_REM\_MISSING\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-371">8324 (0x2084)</span><span class="sxs-lookup"><span data-stu-id="93ba9-371">8324 (0x2084)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-372">Impossibile rimuovere l'attributo perché non è presente nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-372">The attribute cannot be removed because it is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-373"><span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**ERRORE \_ \_ REM cant di DS \_ \_ mancato \_ att \_ Val**</span><span class="sxs-lookup"><span data-stu-id="93ba9-373"><span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**ERROR\_DS\_CANT\_REM\_MISSING\_ATT\_VAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-374">8325 (0x2085)</span><span class="sxs-lookup"><span data-stu-id="93ba9-374">8325 (0x2085)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-375">Impossibile rimuovere il valore dell'attributo perché non è presente nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-375">The attribute value cannot be removed because it is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-376"><span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**ERRORE \_ DS \_ root \_ cant \_ be \_ sottoriferimento**</span><span class="sxs-lookup"><span data-stu-id="93ba9-376"><span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**ERROR\_DS\_ROOT\_CANT\_BE\_SUBREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-377">8326 (0x2086)</span><span class="sxs-lookup"><span data-stu-id="93ba9-377">8326 (0x2086)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-378">L'oggetto radice specificato non può essere un sottoriferimento.</span><span class="sxs-lookup"><span data-stu-id="93ba9-378">The specified root object cannot be a subref.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-379"><span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERRORE \_ DS \_ nessun \_ concatenamento**</span><span class="sxs-lookup"><span data-stu-id="93ba9-379"><span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERROR\_DS\_NO\_CHAINING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-380">8327 (0x2087)</span><span class="sxs-lookup"><span data-stu-id="93ba9-380">8327 (0x2087)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-381">Il concatenamento non è consentito.</span><span class="sxs-lookup"><span data-stu-id="93ba9-381">Chaining is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-382"><span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERRORE \_ DS \_ non \_ concatenato \_ EVAL**</span><span class="sxs-lookup"><span data-stu-id="93ba9-382"><span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERROR\_DS\_NO\_CHAINED\_EVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-383">8328 (0x2088)</span><span class="sxs-lookup"><span data-stu-id="93ba9-383">8328 (0x2088)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-384">La valutazione concatenata non è consentita.</span><span class="sxs-lookup"><span data-stu-id="93ba9-384">Chained evaluation is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-385"><span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERRORE \_ DS \_ nessun \_ \_ oggetto padre**</span><span class="sxs-lookup"><span data-stu-id="93ba9-385"><span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERROR\_DS\_NO\_PARENT\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-386">8329 (0x2089)</span><span class="sxs-lookup"><span data-stu-id="93ba9-386">8329 (0x2089)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-387">Il padre dell'oggetto è privo di istanza o è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-387">The operation could not be performed because the object's parent is either uninstantiated or deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-388"><span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**ERRORE \_ DS \_ padre \_ è \_ un \_ alias**</span><span class="sxs-lookup"><span data-stu-id="93ba9-388"><span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**ERROR\_DS\_PARENT\_IS\_AN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-389">8330 (0x208A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-389">8330 (0x208A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-390">Non è consentito disporre di un elemento padre che è un alias.</span><span class="sxs-lookup"><span data-stu-id="93ba9-390">Having a parent that is an alias is not permitted.</span></span> <span data-ttu-id="93ba9-391">Gli alias sono oggetti foglia.</span><span class="sxs-lookup"><span data-stu-id="93ba9-391">Aliases are leaf objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-392"><span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERRORE \_ nel \_ \_ \_ master e nei \_ \_ rep di DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-392"><span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERROR\_DS\_CANT\_MIX\_MASTER\_AND\_REPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-393">8331 (0x208B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-393">8331 (0x208B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-394">L'oggetto e l'elemento padre devono essere dello stesso tipo, sia master che entrambe le repliche.</span><span class="sxs-lookup"><span data-stu-id="93ba9-394">The object and parent must be of the same type, either both masters or both replicas.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-395"><span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**gli errori \_ DS sono \_ \_ disponibili**</span><span class="sxs-lookup"><span data-stu-id="93ba9-395"><span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**ERROR\_DS\_CHILDREN\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-396">8332 (0x208C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-396">8332 (0x208C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-397">Impossibile eseguire l'operazione perché sono presenti oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="93ba9-397">The operation cannot be performed because child objects exist.</span></span> <span data-ttu-id="93ba9-398">Questa operazione può essere eseguita solo su un oggetto foglia.</span><span class="sxs-lookup"><span data-stu-id="93ba9-398">This operation can only be performed on a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-399"><span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**ERRORE \_ DS \_ obj \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-399"><span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**ERROR\_DS\_OBJ\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-400">8333 (0x208D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-400">8333 (0x208D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-401">Impossibile trovare l'oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="93ba9-401">Directory object not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-402"><span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**ERRORE \_ di \_ obj con alias DS \_ \_ mancante**</span><span class="sxs-lookup"><span data-stu-id="93ba9-402"><span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**ERROR\_DS\_ALIASED\_OBJ\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-403">8334 (0x208E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-403">8334 (0x208E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-404">Oggetto con alias mancante.</span><span class="sxs-lookup"><span data-stu-id="93ba9-404">The aliased object is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-405"><span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**sintassi per i \_ \_ nomi non validi DS \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-405"><span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**ERROR\_DS\_BAD\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-406">8335 (0x208F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-406">8335 (0x208F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-407">Il nome dell'oggetto presenta una sintassi non valida.</span><span class="sxs-lookup"><span data-stu-id="93ba9-407">The object name has bad syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-408"><span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**ERRORE \_ \_ alias DS \_ punta \_ a \_ alias**</span><span class="sxs-lookup"><span data-stu-id="93ba9-408"><span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**ERROR\_DS\_ALIAS\_POINTS\_TO\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-409">8336 (0x2090)</span><span class="sxs-lookup"><span data-stu-id="93ba9-409">8336 (0x2090)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-410">Non è consentito che un alias faccia riferimento a un altro alias.</span><span class="sxs-lookup"><span data-stu-id="93ba9-410">It is not permitted for an alias to refer to another alias.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-411"><span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERRORE \_ di \_ Deref cant di DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-411"><span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERROR\_DS\_CANT\_DEREF\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-412">8337 (0x2091)</span><span class="sxs-lookup"><span data-stu-id="93ba9-412">8337 (0x2091)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-413">Non è possibile dereferenziare l'alias.</span><span class="sxs-lookup"><span data-stu-id="93ba9-413">The alias cannot be dereferenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-414"><span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERRORE \_ DS \_ dall' \_ \_ ambito**</span><span class="sxs-lookup"><span data-stu-id="93ba9-414"><span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERROR\_DS\_OUT\_OF\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-415">8338 (0x2092)</span><span class="sxs-lookup"><span data-stu-id="93ba9-415">8338 (0x2092)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-416">L'operazione non rientra nell'ambito.</span><span class="sxs-lookup"><span data-stu-id="93ba9-416">The operation is out of scope.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-417"><span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERRORE di \_ dominio DS \_ \_ \_ rimosso**</span><span class="sxs-lookup"><span data-stu-id="93ba9-417"><span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERROR\_DS\_OBJECT\_BEING\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-418">8339 (0x2093)</span><span class="sxs-lookup"><span data-stu-id="93ba9-418">8339 (0x2093)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-419">L'operazione non può continuare perché è in corso la rimozione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-419">The operation cannot continue because the object is in the process of being removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-420"><span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERRORE \_ di \_ \_ eliminazione \_ DSA \_ obj**</span><span class="sxs-lookup"><span data-stu-id="93ba9-420"><span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERROR\_DS\_CANT\_DELETE\_DSA\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-421">8340 (0x2094)</span><span class="sxs-lookup"><span data-stu-id="93ba9-421">8340 (0x2094)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-422">Non è possibile eliminare l'oggetto DSA.</span><span class="sxs-lookup"><span data-stu-id="93ba9-422">The DSA object cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-423"><span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**errore \_ generico DS errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-423"><span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**ERROR\_DS\_GENERIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-424">8341 (0x2095)</span><span class="sxs-lookup"><span data-stu-id="93ba9-424">8341 (0x2095)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-425">Si è verificato un errore del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="93ba9-425">A directory service error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-426"><span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**ERRORE \_ DS \_ DSA \_ deve \_ essere \_ int \_ Master**</span><span class="sxs-lookup"><span data-stu-id="93ba9-426"><span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**ERROR\_DS\_DSA\_MUST\_BE\_INT\_MASTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-427">8342 (0x2096)</span><span class="sxs-lookup"><span data-stu-id="93ba9-427">8342 (0x2096)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-428">L'operazione può essere eseguita solo su un oggetto master DSA interno.</span><span class="sxs-lookup"><span data-stu-id="93ba9-428">The operation can only be performed on an internal master DSA object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-429"><span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERRORE \_ \_ classe DS \_ non \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="93ba9-429"><span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERROR\_DS\_CLASS\_NOT\_DSA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-430">8343 (0x2097)</span><span class="sxs-lookup"><span data-stu-id="93ba9-430">8343 (0x2097)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-431">L'oggetto deve essere di classe DSA.</span><span class="sxs-lookup"><span data-stu-id="93ba9-431">The object must be of class DSA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-432"><span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**\_diritti di \_ \_ accesso insuff di DS \_ errore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-432"><span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**ERROR\_DS\_INSUFF\_ACCESS\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-433">8344 (0x2098)</span><span class="sxs-lookup"><span data-stu-id="93ba9-433">8344 (0x2098)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-434">Diritti di accesso insufficienti per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-434">Insufficient access rights to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-435"><span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERRORE \_ DS \_ superiore non valido \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-435"><span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERROR\_DS\_ILLEGAL\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-436">8345 (0x2099)</span><span class="sxs-lookup"><span data-stu-id="93ba9-436">8345 (0x2099)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-437">Non è possibile aggiungere l'oggetto perché l'elemento padre non è presente nell'elenco dei migliori.</span><span class="sxs-lookup"><span data-stu-id="93ba9-437">The object cannot be added because the parent is not on the list of possible superiors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-438"><span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**\_attributo DS \_ \_ di errore \_ di proprietà di \_ Sam**</span><span class="sxs-lookup"><span data-stu-id="93ba9-438"><span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**ERROR\_DS\_ATTRIBUTE\_OWNED\_BY\_SAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-439">8346 (0x209A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-439">8346 (0x209A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-440">L'accesso all'attributo non è consentito perché l'attributo appartiene a gestione account di sicurezza (SAM).</span><span class="sxs-lookup"><span data-stu-id="93ba9-440">Access to the attribute is not permitted because the attribute is owned by the Security Accounts Manager (SAM).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-441"><span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERRORE \_ \_ nome DS \_ numero troppe \_ \_ parti**</span><span class="sxs-lookup"><span data-stu-id="93ba9-441"><span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERROR\_DS\_NAME\_TOO\_MANY\_PARTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-442">8347 (0x209B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-442">8347 (0x209B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-443">Il nome contiene troppe parti.</span><span class="sxs-lookup"><span data-stu-id="93ba9-443">The name has too many parts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-444"><span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**\_nome DS \_ errore \_ troppo \_ lungo**</span><span class="sxs-lookup"><span data-stu-id="93ba9-444"><span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**ERROR\_DS\_NAME\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-445">8348 (0x209C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-445">8348 (0x209C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-446">Nome troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-446">The name is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-447"><span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**\_ \_ valore nome DS \_ errore \_ troppo \_ lungo**</span><span class="sxs-lookup"><span data-stu-id="93ba9-447"><span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**ERROR\_DS\_NAME\_VALUE\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-448">8349 (0x209D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-448">8349 (0x209D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-449">Il valore del nome è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-449">The name value is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-450"><span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERRORE \_ nome DS non \_ \_ analizzabile**</span><span class="sxs-lookup"><span data-stu-id="93ba9-450"><span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERROR\_DS\_NAME\_UNPARSEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-451">8350 (0x209E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-451">8350 (0x209E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-452">Il servizio directory ha rilevato un errore durante l'analisi di un nome.</span><span class="sxs-lookup"><span data-stu-id="93ba9-452">The directory service encountered an error parsing a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-453"><span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERRORE \_ \_ nome DS \_ tipo \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="93ba9-453"><span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERROR\_DS\_NAME\_TYPE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-454">8351 (0x209F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-454">8351 (0x209F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-455">Il servizio directory non è in grado di ottenere il tipo di attributo per un nome.</span><span class="sxs-lookup"><span data-stu-id="93ba9-455">The directory service cannot get the attribute type for a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-456"><span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERRORE \_ DS \_ non è \_ un \_ oggetto**</span><span class="sxs-lookup"><span data-stu-id="93ba9-456"><span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERROR\_DS\_NOT\_AN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-457">8352 (0x20A0)</span><span class="sxs-lookup"><span data-stu-id="93ba9-457">8352 (0x20A0)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-458">Il nome non identifica un oggetto. il nome identifica un oggetto fantasma.</span><span class="sxs-lookup"><span data-stu-id="93ba9-458">The name does not identify an object; the name identifies a phantom.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-459"><span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERRORE di \_ DS \_ sec \_ desc \_ troppo \_ breve**</span><span class="sxs-lookup"><span data-stu-id="93ba9-459"><span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERROR\_DS\_SEC\_DESC\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-460">8353 (0x20A1)</span><span class="sxs-lookup"><span data-stu-id="93ba9-460">8353 (0x20A1)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-461">Il descrittore di sicurezza è troppo breve.</span><span class="sxs-lookup"><span data-stu-id="93ba9-461">The security descriptor is too short.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-462"><span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERRORE \_ DS \_ sec \_ desc \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="93ba9-462"><span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERROR\_DS\_SEC\_DESC\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-463">8354 (0x20A2)</span><span class="sxs-lookup"><span data-stu-id="93ba9-463">8354 (0x20A2)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-464">Il descrittore di sicurezza non è valido.</span><span class="sxs-lookup"><span data-stu-id="93ba9-464">The security descriptor is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-465"><span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERRORE \_ DS \_ nessun \_ \_ nome eliminato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-465"><span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERROR\_DS\_NO\_DELETED\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-466">8355 (0x20A3)</span><span class="sxs-lookup"><span data-stu-id="93ba9-466">8355 (0x20A3)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-467">Impossibile creare il nome per l'oggetto eliminato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-467">Failed to create name for deleted object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-468"><span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**ERRORE \_ DS \_ sottoriferimento \_ deve \_ avere \_ padre**</span><span class="sxs-lookup"><span data-stu-id="93ba9-468"><span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**ERROR\_DS\_SUBREF\_MUST\_HAVE\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-469">8356 (0x20A4)</span><span class="sxs-lookup"><span data-stu-id="93ba9-469">8356 (0x20A4)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-470">Il padre di un nuovo sottoriferimento deve esistere.</span><span class="sxs-lookup"><span data-stu-id="93ba9-470">The parent of a new subref must exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-471"><span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**ERRORE \_ DS \_ NCName \_ deve \_ essere \_ NC**</span><span class="sxs-lookup"><span data-stu-id="93ba9-471"><span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**ERROR\_DS\_NCNAME\_MUST\_BE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-472">8357 (0x20A5)</span><span class="sxs-lookup"><span data-stu-id="93ba9-472">8357 (0x20A5)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-473">L'oggetto deve essere un contesto dei nomi.</span><span class="sxs-lookup"><span data-stu-id="93ba9-473">The object must be a naming context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-474"><span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERRORE \_ DS \_ cant \_ Add \_ System \_ only**</span><span class="sxs-lookup"><span data-stu-id="93ba9-474"><span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERROR\_DS\_CANT\_ADD\_SYSTEM\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-475">8358 (0x20A6)</span><span class="sxs-lookup"><span data-stu-id="93ba9-475">8358 (0x20A6)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-476">Non è consentito aggiungere un attributo di proprietà del sistema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-476">It is not permitted to add an attribute which is owned by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-477"><span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**la \_ classe DS degli errori \_ \_ deve \_ essere \_ concreta**</span><span class="sxs-lookup"><span data-stu-id="93ba9-477"><span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**ERROR\_DS\_CLASS\_MUST\_BE\_CONCRETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-478">8359 (0x20A7)</span><span class="sxs-lookup"><span data-stu-id="93ba9-478">8359 (0x20A7)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-479">La classe dell'oggetto deve essere strutturale; non è possibile creare un'istanza di una classe astratta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-479">The class of the object must be structural; you cannot instantiate an abstract class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-480"><span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERRORE \_ DS \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-480"><span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERROR\_DS\_INVALID\_DMD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-481">8360 (0x20A8)</span><span class="sxs-lookup"><span data-stu-id="93ba9-481">8360 (0x20A8)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-482">Impossibile trovare l'oggetto dello schema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-482">The schema object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-483"><span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**ERRORE \_ DS \_ obj \_ GUID \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-483"><span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**ERROR\_DS\_OBJ\_GUID\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-484">8361 (0x20A9)</span><span class="sxs-lookup"><span data-stu-id="93ba9-484">8361 (0x20A9)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-485">Un oggetto locale con questo GUID (Dead o Alive) esiste già.</span><span class="sxs-lookup"><span data-stu-id="93ba9-485">A local object with this GUID (dead or alive) already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-486"><span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERRORE \_ DS \_ non \_ in \_ BACKLINK**</span><span class="sxs-lookup"><span data-stu-id="93ba9-486"><span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERROR\_DS\_NOT\_ON\_BACKLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-487">8362 (0x20AA)</span><span class="sxs-lookup"><span data-stu-id="93ba9-487">8362 (0x20AA)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-488">Impossibile eseguire l'operazione su un collegamento indietro.</span><span class="sxs-lookup"><span data-stu-id="93ba9-488">The operation cannot be performed on a back link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-489"><span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERRORE \_ DS \_ nessun \_ CROSSREF \_ per \_ NC**</span><span class="sxs-lookup"><span data-stu-id="93ba9-489"><span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERROR\_DS\_NO\_CROSSREF\_FOR\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-490">8363 (0x20AB)</span><span class="sxs-lookup"><span data-stu-id="93ba9-490">8363 (0x20AB)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-491">Impossibile trovare il riferimento incrociato per il contesto dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-491">The cross reference for the specified naming context could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-492"><span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERRORE \_ di \_ arresto di \_ DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-492"><span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERROR\_DS\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-493">8364 (0x20AC)</span><span class="sxs-lookup"><span data-stu-id="93ba9-493">8364 (0x20AC)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-494">Non è stato possibile eseguire l'operazione perché è in corso la chiusura del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="93ba9-494">The operation could not be performed because the directory service is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-495"><span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**\_ \_ operazione sconosciuta DS \_ errore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-495"><span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**ERROR\_DS\_UNKNOWN\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-496">8365 (0x20AD)</span><span class="sxs-lookup"><span data-stu-id="93ba9-496">8365 (0x20AD)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-497">La richiesta del servizio directory non è valida.</span><span class="sxs-lookup"><span data-stu-id="93ba9-497">The directory service request is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-498"><span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERRORE \_ DS \_ \_ proprietario ruolo non valido \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-498"><span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERROR\_DS\_INVALID\_ROLE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-499">8366 (0x20AE)</span><span class="sxs-lookup"><span data-stu-id="93ba9-499">8366 (0x20AE)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-500">Impossibile leggere l'attributo del proprietario del ruolo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-500">The role owner attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-501"><span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERRORE \_ DS \_ couldnt \_ Contact \_ FSMO**</span><span class="sxs-lookup"><span data-stu-id="93ba9-501"><span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERROR\_DS\_COULDNT\_CONTACT\_FSMO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-502">8367 (0x20AF)</span><span class="sxs-lookup"><span data-stu-id="93ba9-502">8367 (0x20AF)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-503">L'operazione FSMO richiesta non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="93ba9-503">The requested FSMO operation failed.</span></span> <span data-ttu-id="93ba9-504">Impossibile contattare il proprietario FSMO corrente.</span><span class="sxs-lookup"><span data-stu-id="93ba9-504">The current FSMO holder could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-505"><span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERRORE \_ di \_ \_ \_ ridenominazione DN Cross NC \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-505"><span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERROR\_DS\_CROSS\_NC\_DN\_RENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-506">8368 (0x20B0)</span><span class="sxs-lookup"><span data-stu-id="93ba9-506">8368 (0x20B0)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-507">Non è consentita la modifica di un DN in un contesto di denominazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-507">Modification of a DN across a naming context is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-508"><span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERRORE \_ \_ solo del sistema cant DS \_ mod \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-508"><span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERROR\_DS\_CANT\_MOD\_SYSTEM\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-509">8369 (0x20B1)</span><span class="sxs-lookup"><span data-stu-id="93ba9-509">8369 (0x20B1)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-510">L'attributo non può essere modificato perché appartiene al sistema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-510">The attribute cannot be modified because it is owned by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-511"><span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERRORE \_ \_ solo Replicator \_ DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-511"><span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERROR\_DS\_REPLICATOR\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-512">8370 (0x20B2)</span><span class="sxs-lookup"><span data-stu-id="93ba9-512">8370 (0x20B2)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-513">Questa funzione può essere eseguita solo da Replicator.</span><span class="sxs-lookup"><span data-stu-id="93ba9-513">Only the replicator can perform this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-514"><span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERRORE \_ DS \_ obj \_ classe \_ non \_ definita**</span><span class="sxs-lookup"><span data-stu-id="93ba9-514"><span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERROR\_DS\_OBJ\_CLASS\_NOT\_DEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-515">8371 (0x20B3)</span><span class="sxs-lookup"><span data-stu-id="93ba9-515">8371 (0x20B3)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-516">La classe specificata non è definita.</span><span class="sxs-lookup"><span data-stu-id="93ba9-516">The specified class is not defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-517"><span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERRORE \_ DS \_ obj \_ classe \_ non \_ sottoclasse**</span><span class="sxs-lookup"><span data-stu-id="93ba9-517"><span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERROR\_DS\_OBJ\_CLASS\_NOT\_SUBCLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-518">8372 (0x20B4)</span><span class="sxs-lookup"><span data-stu-id="93ba9-518">8372 (0x20B4)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-519">La classe specificata non è una sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="93ba9-519">The specified class is not a subclass.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-520"><span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**\_ \_ riferimento nome DS \_ errore \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="93ba9-520"><span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**ERROR\_DS\_NAME\_REFERENCE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-521">8373 (0x20B5)</span><span class="sxs-lookup"><span data-stu-id="93ba9-521">8373 (0x20B5)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-522">Il riferimento al nome non è valido.</span><span class="sxs-lookup"><span data-stu-id="93ba9-522">The name reference is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-523"><span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**ERRORE di \_ DS \_ Cross \_ ref \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-523"><span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**ERROR\_DS\_CROSS\_REF\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-524">8374 (0x20B6)</span><span class="sxs-lookup"><span data-stu-id="93ba9-524">8374 (0x20B6)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-525">Esiste già un riferimento incrociato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-525">A cross reference already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-526"><span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERRORE \_ DS \_ cant \_ del \_ master \_ CROSSREF**</span><span class="sxs-lookup"><span data-stu-id="93ba9-526"><span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERROR\_DS\_CANT\_DEL\_MASTER\_CROSSREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-527">8375 (0x20B7)</span><span class="sxs-lookup"><span data-stu-id="93ba9-527">8375 (0x20B7)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-528">Non è consentito eliminare un riferimento incrociato master.</span><span class="sxs-lookup"><span data-stu-id="93ba9-528">It is not permitted to delete a master cross reference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-529"><span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERRORE del \_ sottoalbero di DS per la \_ \_ notifica \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-529"><span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERROR\_DS\_SUBTREE\_NOTIFY\_NOT\_NC\_HEAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-530">8376 (0x20B8)</span><span class="sxs-lookup"><span data-stu-id="93ba9-530">8376 (0x20B8)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-531">Le notifiche del sottoalbero sono supportate solo nelle intestazioni NC.</span><span class="sxs-lookup"><span data-stu-id="93ba9-531">Subtree notifications are only supported on NC heads.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-532"><span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**\_ \_ filtro notifiche DS \_ errore \_ troppo \_ complesso**</span><span class="sxs-lookup"><span data-stu-id="93ba9-532"><span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**ERROR\_DS\_NOTIFY\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-533">8377 (0x20B9)</span><span class="sxs-lookup"><span data-stu-id="93ba9-533">8377 (0x20B9)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-534">Il filtro di notifica è troppo complesso.</span><span class="sxs-lookup"><span data-stu-id="93ba9-534">Notification filter is too complex.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-535"><span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERRORE \_ RDN di DS \_ DUP \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-535"><span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERROR\_DS\_DUP\_RDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-536">8378 (0x20BA)</span><span class="sxs-lookup"><span data-stu-id="93ba9-536">8378 (0x20BA)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-537">Aggiornamento dello schema non riuscito: RDN duplicato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-537">Schema update failed: duplicate RDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-538"><span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ID errore \_ DS \_ DUP \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-538"><span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ERROR\_DS\_DUP\_OID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-539">8379 (0x20BB)</span><span class="sxs-lookup"><span data-stu-id="93ba9-539">8379 (0x20BB)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-540">Aggiornamento dello schema non riuscito: OID duplicato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-540">Schema update failed: duplicate OID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-541"><span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**ERRORE \_ DS \_ DUP \_ \_ ID MAPI**</span><span class="sxs-lookup"><span data-stu-id="93ba9-541"><span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**ERROR\_DS\_DUP\_MAPI\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-542">8380 (0x20BC)</span><span class="sxs-lookup"><span data-stu-id="93ba9-542">8380 (0x20BC)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-543">Aggiornamento dello schema non riuscito: identificatore MAPI duplicato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-543">Schema update failed: duplicate MAPI identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-544"><span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**\_ \_ \_ \_ GUID ID schema duplicato errore DS \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-544"><span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**ERROR\_DS\_DUP\_SCHEMA\_ID\_GUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-545">8381 (0x20BD)</span><span class="sxs-lookup"><span data-stu-id="93ba9-545">8381 (0x20BD)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-546">Aggiornamento dello schema non riuscito: GUID ID schema duplicato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-546">Schema update failed: duplicate schema-id GUID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-547"><span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERRORE \_ DS \_ DUP \_ \_ nome visualizzato \_ LDAP**</span><span class="sxs-lookup"><span data-stu-id="93ba9-547"><span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERROR\_DS\_DUP\_LDAP\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-548">8382 (0x20BE)</span><span class="sxs-lookup"><span data-stu-id="93ba9-548">8382 (0x20BE)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-549">Aggiornamento dello schema non riuscito: nome visualizzato LDAP duplicato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-549">Schema update failed: duplicate LDAP display name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-550"><span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERRORE \_ di \_ test semantico di DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-550"><span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERROR\_DS\_SEMANTIC\_ATT\_TEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-551">8383 (0x20BF)</span><span class="sxs-lookup"><span data-stu-id="93ba9-551">8383 (0x20BF)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-552">Aggiornamento schema non riuscito: intervallo-inferiore minore di intervallo superiore.</span><span class="sxs-lookup"><span data-stu-id="93ba9-552">Schema update failed: range-lower less than range upper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-553"><span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERRORE \_ di \_ sintassi DS non \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-553"><span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERROR\_DS\_SYNTAX\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-554">8384 (0x20C0)</span><span class="sxs-lookup"><span data-stu-id="93ba9-554">8384 (0x20C0)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-555">Aggiornamento dello schema non riuscito: sintassi non corrispondente.</span><span class="sxs-lookup"><span data-stu-id="93ba9-555">Schema update failed: syntax mismatch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-556"><span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**ERRORE \_ DS \_ \_ in \_ deve \_ avere**</span><span class="sxs-lookup"><span data-stu-id="93ba9-556"><span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**ERROR\_DS\_EXISTS\_IN\_MUST\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-557">8385 (0x20C1)</span><span class="sxs-lookup"><span data-stu-id="93ba9-557">8385 (0x20C1)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-558">Eliminazione dello schema non riuscita: l'attributo viene usato in must-contain.</span><span class="sxs-lookup"><span data-stu-id="93ba9-558">Schema deletion failed: attribute is used in must-contain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-559"><span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**ERRORE \_ DS \_ presente \_ in \_ potrebbe \_ avere**</span><span class="sxs-lookup"><span data-stu-id="93ba9-559"><span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**ERROR\_DS\_EXISTS\_IN\_MAY\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-560">8386 (0x20C2)</span><span class="sxs-lookup"><span data-stu-id="93ba9-560">8386 (0x20C2)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-561">L'eliminazione dello schema non è riuscita: l'attributo viene utilizzato in può contenere.</span><span class="sxs-lookup"><span data-stu-id="93ba9-561">Schema deletion failed: attribute is used in may-contain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-562"><span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**ERRORE \_ DS non \_ esistente \_ potrebbe \_ avere**</span><span class="sxs-lookup"><span data-stu-id="93ba9-562"><span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**ERROR\_DS\_NONEXISTENT\_MAY\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-563">8387 (0x20C3)</span><span class="sxs-lookup"><span data-stu-id="93ba9-563">8387 (0x20C3)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-564">Aggiornamento dello schema non riuscito: l'attributo in può contenere non esiste.</span><span class="sxs-lookup"><span data-stu-id="93ba9-564">Schema update failed: attribute in may-contain does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-565"><span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**ERRORE \_ DS non \_ esistente \_ deve \_ contenere**</span><span class="sxs-lookup"><span data-stu-id="93ba9-565"><span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**ERROR\_DS\_NONEXISTENT\_MUST\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-566">8388 (0x20C4)</span><span class="sxs-lookup"><span data-stu-id="93ba9-566">8388 (0x20C4)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-567">Aggiornamento dello schema non riuscito: l'attributo in must-contain non esiste.</span><span class="sxs-lookup"><span data-stu-id="93ba9-567">Schema update failed: attribute in must-contain does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-568"><span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERRORE \_ del \_ \_ test CLS \_ aux \_ DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-568"><span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERROR\_DS\_AUX\_CLS\_TEST\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-569">8389 (0x20C5)</span><span class="sxs-lookup"><span data-stu-id="93ba9-569">8389 (0x20C5)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-570">Aggiornamento dello schema non riuscito: la classe nell'elenco di classi aux non esiste o non è una classe ausiliaria.</span><span class="sxs-lookup"><span data-stu-id="93ba9-570">Schema update failed: class in aux-class list does not exist or is not an auxiliary class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-571"><span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERRORE di \_ DS non \_ esistente \_ \_ sup**</span><span class="sxs-lookup"><span data-stu-id="93ba9-571"><span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERROR\_DS\_NONEXISTENT\_POSS\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-572">8390 (0x20C6)</span><span class="sxs-lookup"><span data-stu-id="93ba9-572">8390 (0x20C6)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-573">Aggiornamento dello schema non riuscito: la classe in poss-superiors non esiste.</span><span class="sxs-lookup"><span data-stu-id="93ba9-573">Schema update failed: class in poss-superiors does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-574"><span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERRORE \_ \_ \_ test sottocls \_ di \_ DS errore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-574"><span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERROR\_DS\_SUB\_CLS\_TEST\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-575">8391 (0x20C7)</span><span class="sxs-lookup"><span data-stu-id="93ba9-575">8391 (0x20C7)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-576">Aggiornamento dello schema non riuscito: la classe nell'elenco subclassOf non esiste o non soddisfa le regole della gerarchia.</span><span class="sxs-lookup"><span data-stu-id="93ba9-576">Schema update failed: class in subclassof list does not exist or does not satisfy hierarchy rules.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-577"><span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERRORE \_ DS \_ \_ \_ \_ sintassi ID RDN non \_ valida**</span><span class="sxs-lookup"><span data-stu-id="93ba9-577"><span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERROR\_DS\_BAD\_RDN\_ATT\_ID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-578">8392 (0x20C8)</span><span class="sxs-lookup"><span data-stu-id="93ba9-578">8392 (0x20C8)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-579">L'aggiornamento dello schema non è riuscito: la sintassi di RDN-att-ID non è corretta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-579">Schema update failed: Rdn-Att-Id has wrong syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-580"><span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**ERRORE \_ DS \_ presente \_ nella \_ \_ CLS aux**</span><span class="sxs-lookup"><span data-stu-id="93ba9-580"><span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**ERROR\_DS\_EXISTS\_IN\_AUX\_CLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-581">8393 (0x20C9)</span><span class="sxs-lookup"><span data-stu-id="93ba9-581">8393 (0x20C9)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-582">Eliminazione dello schema non riuscita: la classe viene usata come classe ausiliaria.</span><span class="sxs-lookup"><span data-stu-id="93ba9-582">Schema deletion failed: class is used as auxiliary class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-583"><span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**ERRORE \_ DS \_ presente \_ in \_ Sub \_ CLS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-583"><span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**ERROR\_DS\_EXISTS\_IN\_SUB\_CLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-584">8394 (0x20CA)</span><span class="sxs-lookup"><span data-stu-id="93ba9-584">8394 (0x20CA)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-585">Eliminazione dello schema non riuscita: la classe viene usata come classe secondaria.</span><span class="sxs-lookup"><span data-stu-id="93ba9-585">Schema deletion failed: class is used as sub class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-586"><span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**ERRORE \_ DS \_ presente \_ nel \_ \_ sup sup**</span><span class="sxs-lookup"><span data-stu-id="93ba9-586"><span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**ERROR\_DS\_EXISTS\_IN\_POSS\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-587">8395 (0x20CB)</span><span class="sxs-lookup"><span data-stu-id="93ba9-587">8395 (0x20CB)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-588">Eliminazione dello schema non riuscita: la classe viene utilizzata come superiore.</span><span class="sxs-lookup"><span data-stu-id="93ba9-588">Schema deletion failed: class is used as poss superior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-589"><span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**ERRORE \_ DS \_ RECALCSCHEMA \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="93ba9-589"><span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**ERROR\_DS\_RECALCSCHEMA\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-590">8396 (0x20CC)</span><span class="sxs-lookup"><span data-stu-id="93ba9-590">8396 (0x20CC)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-591">Errore di aggiornamento dello schema durante il ricalcolo della cache di convalida.</span><span class="sxs-lookup"><span data-stu-id="93ba9-591">Schema update failed in recalculating validation cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-592"><span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERRORE \_ di \_ eliminazione albero DS \_ \_ non \_ completata**</span><span class="sxs-lookup"><span data-stu-id="93ba9-592"><span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERROR\_DS\_TREE\_DELETE\_NOT\_FINISHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-593">8397 (0x20CD)</span><span class="sxs-lookup"><span data-stu-id="93ba9-593">8397 (0x20CD)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-594">L'eliminazione dell'albero non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="93ba9-594">The tree deletion is not finished.</span></span> <span data-ttu-id="93ba9-595">La richiesta deve essere eseguita di nuovo per continuare a eliminare l'albero.</span><span class="sxs-lookup"><span data-stu-id="93ba9-595">The request must be made again to continue deleting the tree.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-596"><span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERRORE \_ di \_ eliminazione del cant DS \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-596"><span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERROR\_DS\_CANT\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-597">8398 (0x20CE)</span><span class="sxs-lookup"><span data-stu-id="93ba9-597">8398 (0x20CE)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-598">Non è stato possibile eseguire l'operazione di eliminazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-598">The requested delete operation could not be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-599"><span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**\_ID richiesta \_ \_ dello schema \_ \_ di errore DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-599"><span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**ERROR\_DS\_ATT\_SCHEMA\_REQ\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-600">8399 (0x20CF)</span><span class="sxs-lookup"><span data-stu-id="93ba9-600">8399 (0x20CF)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-601">Impossibile leggere l'identificatore di classe governas per il record dello schema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-601">Cannot read the governs class identifier for the schema record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-602"><span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**\_ \_ \_ \_ sintassi dello schema \_ di errore DS non valida**</span><span class="sxs-lookup"><span data-stu-id="93ba9-602"><span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**ERROR\_DS\_BAD\_ATT\_SCHEMA\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-603">8400 (0x20D0)</span><span class="sxs-lookup"><span data-stu-id="93ba9-603">8400 (0x20D0)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-604">La sintassi dello schema dell'attributo non è valida.</span><span class="sxs-lookup"><span data-stu-id="93ba9-604">The attribute schema has bad syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-605"><span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERRORE \_ \_ nella cache del cant DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-605"><span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERROR\_DS\_CANT\_CACHE\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-606">8401 (0x20D1)</span><span class="sxs-lookup"><span data-stu-id="93ba9-606">8401 (0x20D1)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-607">Non è stato possibile memorizzare nella cache l'attributo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-607">The attribute could not be cached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-608"><span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERRORE \_ \_ \_ classe cache cant \_ DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-608"><span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERROR\_DS\_CANT\_CACHE\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-609">8402 (0x20D2)</span><span class="sxs-lookup"><span data-stu-id="93ba9-609">8402 (0x20D2)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-610">Impossibile memorizzare nella cache la classe.</span><span class="sxs-lookup"><span data-stu-id="93ba9-610">The class could not be cached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-611"><span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERRORE di DS per la \_ \_ \_ rimozione \_ \_ della cache att**</span><span class="sxs-lookup"><span data-stu-id="93ba9-611"><span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERROR\_DS\_CANT\_REMOVE\_ATT\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-612">8403 (0x20D3)</span><span class="sxs-lookup"><span data-stu-id="93ba9-612">8403 (0x20D3)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-613">Impossibile rimuovere l'attributo dalla cache.</span><span class="sxs-lookup"><span data-stu-id="93ba9-613">The attribute could not be removed from the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-614"><span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**errore durante la \_ \_ \_ rimozione \_ \_ della cache della classe di DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-614"><span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**ERROR\_DS\_CANT\_REMOVE\_CLASS\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-615">8404 (0x20D4)</span><span class="sxs-lookup"><span data-stu-id="93ba9-615">8404 (0x20D4)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-616">Non è stato possibile rimuovere la classe dalla cache.</span><span class="sxs-lookup"><span data-stu-id="93ba9-616">The class could not be removed from the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-617"><span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**errore durante il \_ \_ recupero del \_ \_ DN DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-617"><span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**ERROR\_DS\_CANT\_RETRIEVE\_DN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-618">8405 (0x20D5)</span><span class="sxs-lookup"><span data-stu-id="93ba9-618">8405 (0x20D5)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-619">Impossibile leggere l'attributo del nome distinto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-619">The distinguished name attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-620"><span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERRORE \_ DS \_ mancante \_ SUPREF**</span><span class="sxs-lookup"><span data-stu-id="93ba9-620"><span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERROR\_DS\_MISSING\_SUPREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-621">8406 (0x20D6)</span><span class="sxs-lookup"><span data-stu-id="93ba9-621">8406 (0x20D6)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-622">Non è stato configurato alcun riferimento superiore per il servizio directory.</span><span class="sxs-lookup"><span data-stu-id="93ba9-622">No superior reference has been configured for the directory service.</span></span> <span data-ttu-id="93ba9-623">Il servizio directory non è quindi in grado di emettere riferimenti a oggetti esterni a questa foresta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-623">The directory service is therefore unable to issue referrals to objects outside this forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-624"><span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**errore durante il \_ \_ recupero dell' \_ \_ istanza di DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-624"><span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**ERROR\_DS\_CANT\_RETRIEVE\_INSTANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-625">8407 (0x20D7)</span><span class="sxs-lookup"><span data-stu-id="93ba9-625">8407 (0x20D7)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-626">Impossibile recuperare l'attributo del tipo di istanza.</span><span class="sxs-lookup"><span data-stu-id="93ba9-626">The instance type attribute could not be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-627"><span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**ERRORE \_ di \_ incoerenza del codice DS \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-627"><span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**ERROR\_DS\_CODE\_INCONSISTENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-628">8408 (0x20D8)</span><span class="sxs-lookup"><span data-stu-id="93ba9-628">8408 (0x20D8)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-629">Si è verificato un errore interno.</span><span class="sxs-lookup"><span data-stu-id="93ba9-629">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-630"><span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**errore \_ database DS errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-630"><span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**ERROR\_DS\_DATABASE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-631">8409 (0x20D9)</span><span class="sxs-lookup"><span data-stu-id="93ba9-631">8409 (0x20D9)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-632">Si è verificato un errore del database.</span><span class="sxs-lookup"><span data-stu-id="93ba9-632">A database error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-633"><span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERRORE \_ DS \_ governsID \_ mancante**</span><span class="sxs-lookup"><span data-stu-id="93ba9-633"><span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERROR\_DS\_GOVERNSID\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-634">8410 (0x20DA)</span><span class="sxs-lookup"><span data-stu-id="93ba9-634">8410 (0x20DA)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-635">Attributo GOVERNSID mancante.</span><span class="sxs-lookup"><span data-stu-id="93ba9-635">The attribute GOVERNSID is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-636"><span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**ERRORE in \_ DS mancante per l' \_ \_ \_ att previsto**</span><span class="sxs-lookup"><span data-stu-id="93ba9-636"><span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**ERROR\_DS\_MISSING\_EXPECTED\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-637">8411 (0x20DB)</span><span class="sxs-lookup"><span data-stu-id="93ba9-637">8411 (0x20DB)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-638">Manca un attributo previsto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-638">An expected attribute is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-639"><span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERRORE \_ DS \_ NCName \_ mancante \_ \_ riferimento CR**</span><span class="sxs-lookup"><span data-stu-id="93ba9-639"><span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERROR\_DS\_NCNAME\_MISSING\_CR\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-640">8412 (0x20DC)</span><span class="sxs-lookup"><span data-stu-id="93ba9-640">8412 (0x20DC)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-641">Nel contesto di denominazione specificato manca un riferimento incrociato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-641">The specified naming context is missing a cross reference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-642"><span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**\_ \_ \_ errore controllo sicurezza DS \_ errore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-642"><span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**ERROR\_DS\_SECURITY\_CHECKING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-643">8413 (0x20DD)</span><span class="sxs-lookup"><span data-stu-id="93ba9-643">8413 (0x20DD)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-644">Si è verificato un errore di controllo di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="93ba9-644">A security checking error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-645"><span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**ERRORE \_ \_ schema DS \_ non \_ caricato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-645"><span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**ERROR\_DS\_SCHEMA\_NOT\_LOADED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-646">8414 (0x20DE)</span><span class="sxs-lookup"><span data-stu-id="93ba9-646">8414 (0x20DE)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-647">Lo schema non è caricato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-647">The schema is not loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-648"><span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERRORE \_ \_ \_ allocatore schema DS \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="93ba9-648"><span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERROR\_DS\_SCHEMA\_ALLOC\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-649">8415 (0x20DF)</span><span class="sxs-lookup"><span data-stu-id="93ba9-649">8415 (0x20DF)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-650">Allocazione dello schema non riuscita.</span><span class="sxs-lookup"><span data-stu-id="93ba9-650">Schema allocation failed.</span></span> <span data-ttu-id="93ba9-651">Verificare che la memoria del computer sia insufficiente.</span><span class="sxs-lookup"><span data-stu-id="93ba9-651">Please check if the machine is running low on memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-652"><span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERRORE nella sintassi della richiesta \_ \_ \_ dello schema DS att \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-652"><span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERROR\_DS\_ATT\_SCHEMA\_REQ\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-653">8416 (0x20E0)</span><span class="sxs-lookup"><span data-stu-id="93ba9-653">8416 (0x20E0)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-654">Impossibile ottenere la sintassi necessaria per lo schema dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-654">Failed to obtain the required syntax for the attribute schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-655"><span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**errore \_ \_ GCVERIFY DS \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-655"><span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**ERROR\_DS\_GCVERIFY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-656">8417 (0x20E1)</span><span class="sxs-lookup"><span data-stu-id="93ba9-656">8417 (0x20E1)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-657">Verifica del catalogo globale non riuscita.</span><span class="sxs-lookup"><span data-stu-id="93ba9-657">The global catalog verification failed.</span></span> <span data-ttu-id="93ba9-658">Il catalogo globale non è disponibile o non supporta l'operazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-658">The global catalog is not available or does not support the operation.</span></span> <span data-ttu-id="93ba9-659">Una parte della directory non è attualmente disponibile.</span><span class="sxs-lookup"><span data-stu-id="93ba9-659">Some part of the directory is currently not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-660"><span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERRORE \_ di \_ schema DRA di DS non \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-660"><span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERROR\_DS\_DRA\_SCHEMA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-661">8418 (0x20E2)</span><span class="sxs-lookup"><span data-stu-id="93ba9-661">8418 (0x20E2)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-662">L'operazione di replica non è riuscita a causa di una mancata corrispondenza dello schema tra i server necessari.</span><span class="sxs-lookup"><span data-stu-id="93ba9-662">The replication operation failed because of a schema mismatch between the servers involved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-663"><span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERRORE \_ DS \_ non \_ trovato \_ DSA \_ obj**</span><span class="sxs-lookup"><span data-stu-id="93ba9-663"><span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERROR\_DS\_CANT\_FIND\_DSA\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-664">8419 (0x20E3)</span><span class="sxs-lookup"><span data-stu-id="93ba9-664">8419 (0x20E3)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-665">Impossibile trovare l'oggetto DSA.</span><span class="sxs-lookup"><span data-stu-id="93ba9-665">The DSA object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-666"><span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**errore durante la ricerca del controller di dominio per l'errore \_ DS \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-666"><span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**ERROR\_DS\_CANT\_FIND\_EXPECTED\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-667">8420 (0x20E4)</span><span class="sxs-lookup"><span data-stu-id="93ba9-667">8420 (0x20E4)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-668">Impossibile trovare il contesto dei nomi.</span><span class="sxs-lookup"><span data-stu-id="93ba9-668">The naming context could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-669"><span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERRORE \_ DS \_ \_ trovare \_ NC \_ nella \_ cache**</span><span class="sxs-lookup"><span data-stu-id="93ba9-669"><span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERROR\_DS\_CANT\_FIND\_NC\_IN\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-670">8421 (0x20E5)</span><span class="sxs-lookup"><span data-stu-id="93ba9-670">8421 (0x20E5)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-671">Il contesto dei nomi non è stato trovato nella cache.</span><span class="sxs-lookup"><span data-stu-id="93ba9-671">The naming context could not be found in the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-672"><span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**errore durante il \_ \_ recupero dell' \_ \_ elemento figlio di DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-672"><span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**ERROR\_DS\_CANT\_RETRIEVE\_CHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-673">8422 (0x20E6)</span><span class="sxs-lookup"><span data-stu-id="93ba9-673">8422 (0x20E6)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-674">Impossibile recuperare l'oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="93ba9-674">The child object could not be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-675"><span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERRORE \_ di \_ sicurezza DS- \_ modifica non valida \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-675"><span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERROR\_DS\_SECURITY\_ILLEGAL\_MODIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-676">8423 (0x20E7)</span><span class="sxs-lookup"><span data-stu-id="93ba9-676">8423 (0x20E7)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-677">La modifica non è consentita per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="93ba9-677">The modification was not permitted for security reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-678"><span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERRORE \_ DS \_ cant \_ Replace \_ Hidden \_ REC**</span><span class="sxs-lookup"><span data-stu-id="93ba9-678"><span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERROR\_DS\_CANT\_REPLACE\_HIDDEN\_REC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-679">8424 (0x20E8)</span><span class="sxs-lookup"><span data-stu-id="93ba9-679">8424 (0x20E8)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-680">L'operazione non è in grado di sostituire il record nascosto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-680">The operation cannot replace the hidden record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-681"><span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERRORE \_ DS \_ \_ file di gerarchia non valido \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-681"><span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERROR\_DS\_BAD\_HIERARCHY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-682">8425 (0x20E9)</span><span class="sxs-lookup"><span data-stu-id="93ba9-682">8425 (0x20E9)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-683">Il file della gerarchia non è valido.</span><span class="sxs-lookup"><span data-stu-id="93ba9-683">The hierarchy file is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-684"><span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERRORE \_ nella \_ \_ tabella della gerarchia di compilazione \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-684"><span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERROR\_DS\_BUILD\_HIERARCHY\_TABLE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-685">8426 (0x20EA)</span><span class="sxs-lookup"><span data-stu-id="93ba9-685">8426 (0x20EA)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-686">Tentativo di compilazione della tabella della gerarchia non riuscito.</span><span class="sxs-lookup"><span data-stu-id="93ba9-686">The attempt to build the hierarchy table failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-687"><span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**ERRORE \_ \_ param configurazione \_ DS \_ mancante**</span><span class="sxs-lookup"><span data-stu-id="93ba9-687"><span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**ERROR\_DS\_CONFIG\_PARAM\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-688">8427 (0x20EB)</span><span class="sxs-lookup"><span data-stu-id="93ba9-688">8427 (0x20EB)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-689">Il parametro di configurazione della directory non è presente nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-689">The directory configuration parameter is missing from the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-690"><span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERRORE \_ DS durante il \_ conteggio degli \_ \_ indici AB \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="93ba9-690"><span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERROR\_DS\_COUNTING\_AB\_INDICES\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-691">8428 (0x20EC)</span><span class="sxs-lookup"><span data-stu-id="93ba9-691">8428 (0x20EC)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-692">Il tentativo di conteggio degli indici di Rubrica non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="93ba9-692">The attempt to count the address book indices failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-693"><span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERRORE \_ \_ malloc tabella della gerarchia DS \_ \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="93ba9-693"><span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERROR\_DS\_HIERARCHY\_TABLE\_MALLOC\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-694">8429 (0x20ED)</span><span class="sxs-lookup"><span data-stu-id="93ba9-694">8429 (0x20ED)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-695">Impossibile allocare la tabella della gerarchia.</span><span class="sxs-lookup"><span data-stu-id="93ba9-695">The allocation of the hierarchy table failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-696"><span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERRORE \_ interno DS errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-696"><span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERROR\_DS\_INTERNAL\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-697">8430 (0x20EE)</span><span class="sxs-lookup"><span data-stu-id="93ba9-697">8430 (0x20EE)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-698">Si è verificato un errore interno del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="93ba9-698">The directory service encountered an internal failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-699"><span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**errore di \_ DS \_ sconosciuto \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-699"><span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**ERROR\_DS\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-700">8431 (0x20EF)</span><span class="sxs-lookup"><span data-stu-id="93ba9-700">8431 (0x20EF)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-701">Il servizio directory ha rilevato un errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-701">The directory service encountered an unknown failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-702"><span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**l' \_ errore \_ radice DS \_ richiede la \_ classe \_ Top**</span><span class="sxs-lookup"><span data-stu-id="93ba9-702"><span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**ERROR\_DS\_ROOT\_REQUIRES\_CLASS\_TOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-703">8432 (0x20F0)</span><span class="sxs-lookup"><span data-stu-id="93ba9-703">8432 (0x20F0)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-704">Un oggetto radice richiede una classe di "Top".</span><span class="sxs-lookup"><span data-stu-id="93ba9-704">A root object requires a class of 'top'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-705"><span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERRORE \_ DS che \_ rifiuta \_ i \_ ruoli FSMO**</span><span class="sxs-lookup"><span data-stu-id="93ba9-705"><span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERROR\_DS\_REFUSING\_FSMO\_ROLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-706">8433 (0x20F1)</span><span class="sxs-lookup"><span data-stu-id="93ba9-706">8433 (0x20F1)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-707">Questo server di directory viene arrestato e non è in grado di assumere la proprietà di nuovi ruoli di operazione a master singolo a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="93ba9-707">This directory server is shutting down, and cannot take ownership of new floating single-master operation roles.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-708"><span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**ERRORE \_ DS \_ \_ Impostazioni FSMO \_ mancanti**</span><span class="sxs-lookup"><span data-stu-id="93ba9-708"><span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**ERROR\_DS\_MISSING\_FSMO\_SETTINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-709">8434 (0x20F2)</span><span class="sxs-lookup"><span data-stu-id="93ba9-709">8434 (0x20F2)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-710">Nel servizio directory mancano le informazioni di configurazione obbligatorie e non è in grado di determinare la proprietà dei ruoli di operazione a master singolo a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="93ba9-710">The directory service is missing mandatory configuration information, and is unable to determine the ownership of floating single-master operation roles.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-711"><span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERRORE \_ DS \_ non è \_ in grado di \_ cedere i \_ ruoli**</span><span class="sxs-lookup"><span data-stu-id="93ba9-711"><span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERROR\_DS\_UNABLE\_TO\_SURRENDER\_ROLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-712">8435 (0x20F3)</span><span class="sxs-lookup"><span data-stu-id="93ba9-712">8435 (0x20F3)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-713">Il servizio directory non è stato in grado di trasferire la proprietà di uno o più ruoli di operazione a master singolo mobili ad altri server.</span><span class="sxs-lookup"><span data-stu-id="93ba9-713">The directory service was unable to transfer ownership of one or more floating single-master operation roles to other servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-714"><span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERRORE \_ DS \_ DRA \_ generico**</span><span class="sxs-lookup"><span data-stu-id="93ba9-714"><span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERROR\_DS\_DRA\_GENERIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-715">8436 (0x20F4)</span><span class="sxs-lookup"><span data-stu-id="93ba9-715">8436 (0x20F4)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-716">Operazione di replica non riuscita.</span><span class="sxs-lookup"><span data-stu-id="93ba9-716">The replication operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-717"><span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERRORE \_ DS \_ DRA \_ - \_ parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="93ba9-717"><span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERROR\_DS\_DRA\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-718">8437 (0x20F5)</span><span class="sxs-lookup"><span data-stu-id="93ba9-718">8437 (0x20F5)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-719">Parametro non valido specificato per l'operazione di replica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-719">An invalid parameter was specified for this replication operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-720"><span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERRORE \_ DS \_ DS \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-720"><span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERROR\_DS\_DRA\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-721">8438 (0x20F6)</span><span class="sxs-lookup"><span data-stu-id="93ba9-721">8438 (0x20F6)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-722">Il servizio directory è troppo occupato per completare l'operazione di replica in questo momento.</span><span class="sxs-lookup"><span data-stu-id="93ba9-722">The directory service is too busy to complete the replication operation at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-723"><span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERRORE \_ DS \_ DRA \_ errato \_ DN**</span><span class="sxs-lookup"><span data-stu-id="93ba9-723"><span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERROR\_DS\_DRA\_BAD\_DN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-724">8439 (0x20F7)</span><span class="sxs-lookup"><span data-stu-id="93ba9-724">8439 (0x20F7)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-725">Il nome distinto specificato per l'operazione di replica non è valido.</span><span class="sxs-lookup"><span data-stu-id="93ba9-725">The distinguished name specified for this replication operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-726"><span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERRORE \_ DS \_ DRA \_ errato \_ NC**</span><span class="sxs-lookup"><span data-stu-id="93ba9-726"><span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERROR\_DS\_DRA\_BAD\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-727">8440 (0x20F8)</span><span class="sxs-lookup"><span data-stu-id="93ba9-727">8440 (0x20F8)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-728">Il contesto dei nomi specificato per l'operazione di replica non è valido.</span><span class="sxs-lookup"><span data-stu-id="93ba9-728">The naming context specified for this replication operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-729"><span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERRORE \_ del \_ DN DRA DS \_ \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-729"><span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERROR\_DS\_DRA\_DN\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-730">8441 (0x20F9)</span><span class="sxs-lookup"><span data-stu-id="93ba9-730">8441 (0x20F9)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-731">Il nome distinto specificato per questa operazione di replica esiste già.</span><span class="sxs-lookup"><span data-stu-id="93ba9-731">The distinguished name specified for this replication operation already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-732"><span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**errore \_ \_ interno DRA \_ DS \_ errore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-732"><span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**ERROR\_DS\_DRA\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-733">8442 (0x20FA)</span><span class="sxs-lookup"><span data-stu-id="93ba9-733">8442 (0x20FA)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-734">Si è verificato un errore interno del sistema di replica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-734">The replication system encountered an internal error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-735"><span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERRORE \_ DS \_ DRA \_ incoerente \_ dit**</span><span class="sxs-lookup"><span data-stu-id="93ba9-735"><span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERROR\_DS\_DRA\_INCONSISTENT\_DIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-736">8443 (0x20FB)</span><span class="sxs-lookup"><span data-stu-id="93ba9-736">8443 (0x20FB)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-737">L'operazione di replica ha rilevato un'incoerenza del database.</span><span class="sxs-lookup"><span data-stu-id="93ba9-737">The replication operation encountered a database inconsistency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-738"><span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERRORE \_ di \_ connessione DRA DS \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="93ba9-738"><span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERROR\_DS\_DRA\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-739">8444 (0x20FC)</span><span class="sxs-lookup"><span data-stu-id="93ba9-739">8444 (0x20FC)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-740">Impossibile contattare il server specificato per l'operazione di replica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-740">The server specified for this replication operation could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-741"><span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**\_tipo di \_ \_ istanza non \_ valida \_ del servizio di dominio errore DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-741"><span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERROR\_DS\_DRA\_BAD\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-742">8445 (0x20FD)</span><span class="sxs-lookup"><span data-stu-id="93ba9-742">8445 (0x20FD)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-743">L'operazione di replica ha rilevato un oggetto con un tipo di istanza non valido.</span><span class="sxs-lookup"><span data-stu-id="93ba9-743">The replication operation encountered an object with an invalid instance type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-744"><span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERRORE servizi \_ di dominio Active Directory- \_ \_ out \_ di \_ MEM**</span><span class="sxs-lookup"><span data-stu-id="93ba9-744"><span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERROR\_DS\_DRA\_OUT\_OF\_MEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-745">8446 (0x20FE)</span><span class="sxs-lookup"><span data-stu-id="93ba9-745">8446 (0x20FE)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-746">L'operazione di replica non è riuscita ad allocare memoria.</span><span class="sxs-lookup"><span data-stu-id="93ba9-746">The replication operation failed to allocate memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-747"><span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**\_problema di \_ \_ posta DRA di DS \_ errore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-747"><span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**ERROR\_DS\_DRA\_MAIL\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-748">8447 (0x20FF)</span><span class="sxs-lookup"><span data-stu-id="93ba9-748">8447 (0x20FF)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-749">L'operazione di replica ha rilevato un errore con il sistema di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-749">The replication operation encountered an error with the mail system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-750"><span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**ERRORE \_ di \_ riferimento DRA DS \_ \_ già \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-750"><span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**ERROR\_DS\_DRA\_REF\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-751">8448 (0x2100)</span><span class="sxs-lookup"><span data-stu-id="93ba9-751">8448 (0x2100)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-752">Le informazioni di riferimento per la replica per il server di destinazione esistono già.</span><span class="sxs-lookup"><span data-stu-id="93ba9-752">The replication reference information for the target server already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-753"><span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERRORE \_ di \_ riferimento DRA DS \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-753"><span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERROR\_DS\_DRA\_REF\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-754">8449 (0x2101)</span><span class="sxs-lookup"><span data-stu-id="93ba9-754">8449 (0x2101)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-755">Le informazioni di riferimento per la replica per il server di destinazione non esistono.</span><span class="sxs-lookup"><span data-stu-id="93ba9-755">The replication reference information for the target server does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-756"><span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERRORE \_ DS \_ DRA \_ obj \_ is \_ Rep \_ source**</span><span class="sxs-lookup"><span data-stu-id="93ba9-756"><span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERROR\_DS\_DRA\_OBJ\_IS\_REP\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-757">8450 (0x2102)</span><span class="sxs-lookup"><span data-stu-id="93ba9-757">8450 (0x2102)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-758">Il contesto dei nomi non può essere rimosso perché viene replicato in un altro server.</span><span class="sxs-lookup"><span data-stu-id="93ba9-758">The naming context cannot be removed because it is replicated to another server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-759"><span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**errore \_ del \_ database DRA di DS \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-759"><span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**ERROR\_DS\_DRA\_DB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-760">8451 (0x2103)</span><span class="sxs-lookup"><span data-stu-id="93ba9-760">8451 (0x2103)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-761">Si è verificato un errore di database durante l'operazione di replica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-761">The replication operation encountered a database error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-762"><span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERRORE \_ DS \_ DRA \_ Nessuna \_ replica**</span><span class="sxs-lookup"><span data-stu-id="93ba9-762"><span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERROR\_DS\_DRA\_NO\_REPLICA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-763">8452 (0x2104)</span><span class="sxs-lookup"><span data-stu-id="93ba9-763">8452 (0x2104)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-764">Il contesto dei nomi è in corso di rimozione o non viene replicato dal server specificato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-764">The naming context is in the process of being removed or is not replicated from the specified server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-765"><span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERRORE \_ \_ accesso DRA \_ DS \_ negato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-765"><span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERROR\_DS\_DRA\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-766">8453 (0x2105)</span><span class="sxs-lookup"><span data-stu-id="93ba9-766">8453 (0x2105)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-767">Accesso alla replica negato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-767">Replication access was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-768"><span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**\_ \_ DRA non è \_ \_ supportato per l'errore DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-768"><span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**ERROR\_DS\_DRA\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-769">8454 (0x2106)</span><span class="sxs-lookup"><span data-stu-id="93ba9-769">8454 (0x2106)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-770">L'operazione richiesta non è supportata da questa versione del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="93ba9-770">The requested operation is not supported by this version of the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-771"><span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERRORE \_ \_ RPC DRA \_ \_ annullato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-771"><span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERROR\_DS\_DRA\_RPC\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-772">8455 (0x2107)</span><span class="sxs-lookup"><span data-stu-id="93ba9-772">8455 (0x2107)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-773">La chiamata di procedura remota di replica è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="93ba9-773">The replication remote procedure call was cancelled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-774"><span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**ERRORE \_ \_ \_ codice sorgente DRA \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-774"><span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**ERROR\_DS\_DRA\_SOURCE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-775">8456 (0x2108)</span><span class="sxs-lookup"><span data-stu-id="93ba9-775">8456 (0x2108)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-776">Il server di origine rifiuta attualmente le richieste di replica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-776">The source server is currently rejecting replication requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-777"><span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERRORE \_ del \_ sink DRA DS \_ \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-777"><span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERROR\_DS\_DRA\_SINK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-778">8457 (0x2109)</span><span class="sxs-lookup"><span data-stu-id="93ba9-778">8457 (0x2109)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-779">Il server di destinazione rifiuta le richieste di replica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-779">The destination server is currently rejecting replication requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-780"><span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**ERRORE \_ \_ \_ : conflitto nome DRA DS \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-780"><span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**ERROR\_DS\_DRA\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-781">8458 (0x210A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-781">8458 (0x210A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-782">L'operazione di replica non è riuscita a causa di un conflitto di nomi di oggetti.</span><span class="sxs-lookup"><span data-stu-id="93ba9-782">The replication operation failed due to a collision of object names.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-783"><span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERRORE \_ \_ \_ codice sorgente DRA \_ reinstallato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-783"><span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERROR\_DS\_DRA\_SOURCE\_REINSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-784">8459 (0x210B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-784">8459 (0x210B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-785">L'origine della replica è stata reinstallata.</span><span class="sxs-lookup"><span data-stu-id="93ba9-785">The replication source has been reinstalled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-786"><span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERRORE \_ del \_ DRA DS \_ mancante \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-786"><span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERROR\_DS\_DRA\_MISSING\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-787">8460 (0x210C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-787">8460 (0x210C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-788">L'operazione di replica non è riuscita perché manca un oggetto padre obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="93ba9-788">The replication operation failed because a required parent object is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-789"><span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERRORE \_ DS \_ DRA \_ interrotto**</span><span class="sxs-lookup"><span data-stu-id="93ba9-789"><span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERROR\_DS\_DRA\_PREEMPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-790">8461 (0x210D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-790">8461 (0x210D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-791">L'operazione di replica è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-791">The replication operation was preempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-792"><span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERRORE servizi di \_ dominio Active Directory per errore \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-792"><span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERROR\_DS\_DRA\_ABANDON\_SYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-793">8462 (0x210E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-793">8462 (0x210E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-794">Il tentativo di sincronizzazione della replica è stato abbandonato a causa di una mancanza di aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="93ba9-794">The replication synchronization attempt was abandoned because of a lack of updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-795"><span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERRORE \_ di \_ arresto DRA DS \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-795"><span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERROR\_DS\_DRA\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-796">8463 (0x210F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-796">8463 (0x210F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-797">L'operazione di replica è stata interrotta perché è in corso l'arresto del sistema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-797">The replication operation was terminated because the system is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-798"><span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERRORE \_ DS \_ DRA \_ incompatibile \_ \_ set parziale**</span><span class="sxs-lookup"><span data-stu-id="93ba9-798"><span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERROR\_DS\_DRA\_INCOMPATIBLE\_PARTIAL\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-799">8464 (0x2110)</span><span class="sxs-lookup"><span data-stu-id="93ba9-799">8464 (0x2110)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-800">Tentativo di sincronizzazione non riuscito perché il controller di dominio di destinazione è attualmente in attesa di sincronizzare nuovi attributi parziali dall'origine.</span><span class="sxs-lookup"><span data-stu-id="93ba9-800">Synchronization attempt failed because the destination DC is currently waiting to synchronize new partial attributes from source.</span></span> <span data-ttu-id="93ba9-801">Questa condizione è normale se una modifica dello schema recente ha modificato il set di attributi parziali.</span><span class="sxs-lookup"><span data-stu-id="93ba9-801">This condition is normal if a recent schema change modified the partial attribute set.</span></span> <span data-ttu-id="93ba9-802">Il set di attributi parziali di destinazione non è un subset del set di attributi parziali di origine.</span><span class="sxs-lookup"><span data-stu-id="93ba9-802">The destination partial attribute set is not a subset of source partial attribute set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-803"><span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**ERRORE \_ DS \_ \_ origine DRA \_ è \_ una \_ replica parziale**</span><span class="sxs-lookup"><span data-stu-id="93ba9-803"><span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**ERROR\_DS\_DRA\_SOURCE\_IS\_PARTIAL\_REPLICA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-804">8465 (0x2111)</span><span class="sxs-lookup"><span data-stu-id="93ba9-804">8465 (0x2111)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-805">Il tentativo di sincronizzazione della replica non è riuscito perché una replica master ha tentato di eseguire la sincronizzazione da una replica parziale.</span><span class="sxs-lookup"><span data-stu-id="93ba9-805">The replication synchronization attempt failed because a master replica attempted to sync from a partial replica.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-806"><span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERRORE \_ di \_ connessione Extn DRA di DS \_ \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="93ba9-806"><span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERROR\_DS\_DRA\_EXTN\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-807">8466 (0x2112)</span><span class="sxs-lookup"><span data-stu-id="93ba9-807">8466 (0x2112)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-808">Il server specificato per l'operazione di replica è stato contattato, ma il server non è stato in grado di contattare un server aggiuntivo necessario per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-808">The server specified for this replication operation was contacted, but that server was unable to contact an additional server needed to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-809"><span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERRORE \_ schema di installazione di DS non \_ \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-809"><span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERROR\_DS\_INSTALL\_SCHEMA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-810">8467 (0x2113)</span><span class="sxs-lookup"><span data-stu-id="93ba9-810">8467 (0x2113)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-811">La versione dello schema del servizio directory della foresta di origine non è compatibile con la versione del servizio directory nel computer.</span><span class="sxs-lookup"><span data-stu-id="93ba9-811">The version of the directory service schema of the source forest is not compatible with the version of directory service on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-812"><span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**\_ \_ ID collegamento duplicato errore DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-812"><span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**ERROR\_DS\_DUP\_LINK\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-813">8468 (0x2114)</span><span class="sxs-lookup"><span data-stu-id="93ba9-813">8468 (0x2114)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-814">Aggiornamento dello schema non riuscito: esiste già un attributo con lo stesso identificatore di collegamento.</span><span class="sxs-lookup"><span data-stu-id="93ba9-814">Schema update failed: An attribute with the same link identifier already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-815"><span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**errore durante la risoluzione del \_ \_ nome DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-815"><span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**ERROR\_DS\_NAME\_ERROR\_RESOLVING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-816">8469 (0x2115)</span><span class="sxs-lookup"><span data-stu-id="93ba9-816">8469 (0x2115)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-817">Traduzione del nome: errore di elaborazione generica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-817">Name translation: Generic processing error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-818"><span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**\_errore di nome DS per errori \_ \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-818"><span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**ERROR\_DS\_NAME\_ERROR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-819">8470 (0x2116)</span><span class="sxs-lookup"><span data-stu-id="93ba9-819">8470 (0x2116)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-820">Traduzione del nome: non è stato possibile trovare il nome o il diritto insufficiente per visualizzare il nome.</span><span class="sxs-lookup"><span data-stu-id="93ba9-820">Name translation: Could not find the name or insufficient right to see name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-821"><span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**errore \_ \_ nome DS \_ \_ non \_ univoco**</span><span class="sxs-lookup"><span data-stu-id="93ba9-821"><span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**ERROR\_DS\_NAME\_ERROR\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-822">8471 (0x2117)</span><span class="sxs-lookup"><span data-stu-id="93ba9-822">8471 (0x2117)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-823">Traduzione del nome: nome di input mappato a più di un nome di output.</span><span class="sxs-lookup"><span data-stu-id="93ba9-823">Name translation: Input name mapped to more than one output name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-824"><span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**errore \_ \_ nome DS \_ errore \_ nessun \_ mapping**</span><span class="sxs-lookup"><span data-stu-id="93ba9-824"><span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**ERROR\_DS\_NAME\_ERROR\_NO\_MAPPING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-825">8472 (0x2118)</span><span class="sxs-lookup"><span data-stu-id="93ba9-825">8472 (0x2118)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-826">Traduzione del nome: il nome di input è stato trovato, ma non il formato di output associato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-826">Name translation: Input name found, but not the associated output format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-827"><span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERRORE \_ DS \_ nome \_ \_ dominio \_ solo errore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-827"><span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERROR\_DS\_NAME\_ERROR\_DOMAIN\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-828">8473 (0x2119)</span><span class="sxs-lookup"><span data-stu-id="93ba9-828">8473 (0x2119)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-829">Traduzione del nome: Impossibile risolvere completamente, è stato trovato solo il dominio.</span><span class="sxs-lookup"><span data-stu-id="93ba9-829">Name translation: Unable to resolve completely, only the domain was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-830"><span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**errore \_ \_ nome DS \_ errore \_ nessun \_ mapping sintattico \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-830"><span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**ERROR\_DS\_NAME\_ERROR\_NO\_SYNTACTICAL\_MAPPING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-831">8474 (0x211A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-831">8474 (0x211A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-832">Traduzione del nome: non è possibile eseguire il mapping puramente sintattico al client senza passare alla rete.</span><span class="sxs-lookup"><span data-stu-id="93ba9-832">Name translation: Unable to perform purely syntactical mapping at the client without going out to the wire.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-833"><span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERRORE \_ \_ mod di \_ att \_ costruito DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-833"><span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERROR\_DS\_CONSTRUCTED\_ATT\_MOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-834">8475 (0x211B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-834">8475 (0x211B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-835">La modifica di un attributo costruito non è consentita.</span><span class="sxs-lookup"><span data-stu-id="93ba9-835">Modification of a constructed attribute is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-836"><span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**ERRORE \_ DS \_ - \_ \_ classe om obj \_ non corretta**</span><span class="sxs-lookup"><span data-stu-id="93ba9-836"><span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**ERROR\_DS\_WRONG\_OM\_OBJ\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-837">8476 (0x211C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-837">8476 (0x211C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-838">La classe OM-Object-Object specificata non è corretta per un attributo con la sintassi specificata.</span><span class="sxs-lookup"><span data-stu-id="93ba9-838">The OM-Object-Class specified is incorrect for an attribute with the specified syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-839"><span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERRORE \_ \_ REPL DRA \_ \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="93ba9-839"><span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERROR\_DS\_DRA\_REPL\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-840">8477 (0x211D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-840">8477 (0x211D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-841">La richiesta di replica è stata inviata. in attesa di risposta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-841">The replication request has been posted; waiting for reply.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-842"><span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERRORE \_ DS \_ DS \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="93ba9-842"><span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERROR\_DS\_DS\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-843">8478 (0x211E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-843">8478 (0x211E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-844">L'operazione richiesta richiede un servizio directory e nessuno è disponibile.</span><span class="sxs-lookup"><span data-stu-id="93ba9-844">The requested operation requires a directory service, and none was available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-845"><span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERRORE \_ DS \_ \_ \_ nome visualizzato LDAP non valido \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-845"><span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERROR\_DS\_INVALID\_LDAP\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-846">8479 (0x211F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-846">8479 (0x211F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-847">Il nome visualizzato LDAP della classe o dell'attributo contiene caratteri non ASCII.</span><span class="sxs-lookup"><span data-stu-id="93ba9-847">The LDAP display name of the class or attribute contains non-ASCII characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-848"><span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERRORE \_ DS \_ - \_ ricerca non di base \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-848"><span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERROR\_DS\_NON\_BASE\_SEARCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-849">8480 (0x2120)</span><span class="sxs-lookup"><span data-stu-id="93ba9-849">8480 (0x2120)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-850">L'operazione di ricerca richiesta è supportata solo per le ricerche di base.</span><span class="sxs-lookup"><span data-stu-id="93ba9-850">The requested search operation is only supported for base searches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-851"><span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERRORE \_ di \_ \_ recupero \_ atts di DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-851"><span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERROR\_DS\_CANT\_RETRIEVE\_ATTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-852">8481 (0x2121)</span><span class="sxs-lookup"><span data-stu-id="93ba9-852">8481 (0x2121)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-853">La ricerca non è riuscita a recuperare gli attributi dal database.</span><span class="sxs-lookup"><span data-stu-id="93ba9-853">The search failed to retrieve attributes from the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-854"><span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERRORE \_ DS \_ BACKLINK \_ senza \_ collegamento**</span><span class="sxs-lookup"><span data-stu-id="93ba9-854"><span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERROR\_DS\_BACKLINK\_WITHOUT\_LINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-855">8482 (0x2122)</span><span class="sxs-lookup"><span data-stu-id="93ba9-855">8482 (0x2122)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-856">L'operazione di aggiornamento dello schema ha tentato di aggiungere un attributo di collegamento a ritroso che non dispone di un collegamento in avanti corrispondente.</span><span class="sxs-lookup"><span data-stu-id="93ba9-856">The schema update operation tried to add a backward link attribute that has no corresponding forward link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-857"><span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERRORE \_ DS \_ Epoch non \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-857"><span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERROR\_DS\_EPOCH\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-858">8483 (0x2123)</span><span class="sxs-lookup"><span data-stu-id="93ba9-858">8483 (0x2123)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-859">L'origine e la destinazione di uno spostamento tra domini non concordano sul numero di Epoch dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-859">Source and destination of a cross-domain move do not agree on the object's epoch number.</span></span> <span data-ttu-id="93ba9-860">L'origine o la destinazione non dispone della versione più recente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-860">Either source or destination does not have the latest version of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-861"><span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERRORE \_ \_ nome src DS non \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-861"><span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERROR\_DS\_SRC\_NAME\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-862">8484 (0x2124)</span><span class="sxs-lookup"><span data-stu-id="93ba9-862">8484 (0x2124)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-863">L'origine e la destinazione di uno spostamento tra domini non concordano sul nome corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-863">Source and destination of a cross-domain move do not agree on the object's current name.</span></span> <span data-ttu-id="93ba9-864">L'origine o la destinazione non dispone della versione più recente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-864">Either source or destination does not have the latest version of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-865"><span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERRORE \_ DS \_ src \_ ed \_ DST \_ NC \_ identico**</span><span class="sxs-lookup"><span data-stu-id="93ba9-865"><span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERROR\_DS\_SRC\_AND\_DST\_NC\_IDENTICAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-866">8485 (0x2125)</span><span class="sxs-lookup"><span data-stu-id="93ba9-866">8485 (0x2125)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-867">L'origine e la destinazione per l'operazione di spostamento tra domini sono identiche.</span><span class="sxs-lookup"><span data-stu-id="93ba9-867">Source and destination for the cross-domain move operation are identical.</span></span> <span data-ttu-id="93ba9-868">Il chiamante deve usare un'operazione di spostamento locale anziché un'operazione di spostamento tra domini.</span><span class="sxs-lookup"><span data-stu-id="93ba9-868">Caller should use local move operation instead of cross-domain move operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-869"><span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERRORE \_ \_ NC DS DST non \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-869"><span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERROR\_DS\_DST\_NC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-870">8486 (0x2126)</span><span class="sxs-lookup"><span data-stu-id="93ba9-870">8486 (0x2126)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-871">L'origine e la destinazione di uno spostamento tra domini non sono concordate sui contesti di denominazione della foresta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-871">Source and destination for a cross-domain move are not in agreement on the naming contexts in the forest.</span></span> <span data-ttu-id="93ba9-872">L'origine o la destinazione non dispone della versione più recente del contenitore di partizioni.</span><span class="sxs-lookup"><span data-stu-id="93ba9-872">Either source or destination does not have the latest version of the Partitions container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-873"><span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERRORE \_ DS \_ non \_ autorevole \_ per \_ \_ NC DST**</span><span class="sxs-lookup"><span data-stu-id="93ba9-873"><span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERROR\_DS\_NOT\_AUTHORITIVE\_FOR\_DST\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-874">8487 (0x2127)</span><span class="sxs-lookup"><span data-stu-id="93ba9-874">8487 (0x2127)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-875">La destinazione di uno spostamento tra domini non è autorevole per il contesto dei nomi di destinazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-875">Destination of a cross-domain move is not authoritative for the destination naming context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-876"><span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERRORE \_ DS \_ src \_ GUID non \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-876"><span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERROR\_DS\_SRC\_GUID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-877">8488 (0x2128)</span><span class="sxs-lookup"><span data-stu-id="93ba9-877">8488 (0x2128)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-878">L'origine e la destinazione di uno spostamento tra domini non concordano sull'identità dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="93ba9-878">Source and destination of a cross-domain move do not agree on the identity of the source object.</span></span> <span data-ttu-id="93ba9-879">L'origine o la destinazione non dispone della versione più recente dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="93ba9-879">Either source or destination does not have the latest version of the source object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-880"><span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERRORE \_ di \_ spostamento del cant DS \_ \_ \_ oggetto eliminato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-880"><span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERROR\_DS\_CANT\_MOVE\_DELETED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-881">8489 (0x2129)</span><span class="sxs-lookup"><span data-stu-id="93ba9-881">8489 (0x2129)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-882">L'oggetto spostato tra domini è già noto per essere eliminato dal server di destinazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-882">Object being moved across-domains is already known to be deleted by the destination server.</span></span> <span data-ttu-id="93ba9-883">Il server di origine non dispone della versione più recente dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="93ba9-883">The source server does not have the latest version of the source object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-884"><span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**\_ \_ operazione PDC errore \_ DS \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="93ba9-884"><span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**ERROR\_DS\_PDC\_OPERATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-885">8490 (0x212A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-885">8490 (0x212A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-886">È già in corso un'altra operazione che richiede l'accesso esclusivo al FSMO PDC.</span><span class="sxs-lookup"><span data-stu-id="93ba9-886">Another operation which requires exclusive access to the PDC FSMO is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-887"><span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERRORE \_ DS \_ tra \_ domini \_ pulizia \_ reqd**</span><span class="sxs-lookup"><span data-stu-id="93ba9-887"><span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERROR\_DS\_CROSS\_DOMAIN\_CLEANUP\_REQD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-888">8491 (0x212B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-888">8491 (0x212B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-889">Un'operazione di spostamento tra domini non è riuscita perché esistono due versioni dell'oggetto spostato, una per ciascuna nei domini di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-889">A cross-domain move operation failed such that two versions of the moved object exist - one each in the source and destination domains.</span></span> <span data-ttu-id="93ba9-890">Per ripristinare lo stato coerente del sistema, è necessario rimuovere l'oggetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-890">The destination object needs to be removed to restore the system to a consistent state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-891"><span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERRORE \_ DS \_ \_ XDOM \_ operazione di spostamento non valida \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-891"><span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERROR\_DS\_ILLEGAL\_XDOM\_MOVE\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-892">8492 (0x212C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-892">8492 (0x212C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-893">Questo oggetto non può essere spostato tra i limiti del dominio perché gli spostamenti tra domini per questa classe non sono consentiti oppure l'oggetto presenta alcune caratteristiche speciali, ad esempio: account attendibile o RID con restrizioni, che ne impediscono lo spostamento.</span><span class="sxs-lookup"><span data-stu-id="93ba9-893">This object may not be moved across domain boundaries either because cross-domain moves for this class are disallowed, or the object has some special characteristics, e.g.: trust account or restricted RID, which prevent its move.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-894"><span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERRORE \_ \_ di DS \_ con \_ il \_ gruppo Acct \_ MEMBERSHPS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-894"><span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERROR\_DS\_CANT\_WITH\_ACCT\_GROUP\_MEMBERSHPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-895">8493 (0x212D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-895">8493 (0x212D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-896">Non è possibile spostare gli oggetti con appartenenze tra i limiti di dominio come dopo lo spostamento. ciò violerebbe le condizioni di appartenenza del gruppo di account.</span><span class="sxs-lookup"><span data-stu-id="93ba9-896">Can't move objects with memberships across domain boundaries as once moved, this would violate the membership conditions of the account group.</span></span> <span data-ttu-id="93ba9-897">Rimuovere l'oggetto da qualsiasi appartenenza a un gruppo di account e riprovare.</span><span class="sxs-lookup"><span data-stu-id="93ba9-897">Remove the object from any account group memberships and retry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-898"><span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**ERRORE per il controller di \_ dominio DS \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-898"><span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**ERROR\_DS\_NC\_MUST\_HAVE\_NC\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-899">8494 (0x212E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-899">8494 (0x212E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-900">Un'intestazione del contesto dei nomi deve essere l'elemento figlio immediato di un'altra intestazione del contesto dei nomi, non di un nodo interno.</span><span class="sxs-lookup"><span data-stu-id="93ba9-900">A naming context head must be the immediate child of another naming context head, not of an interior node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-901"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERRORE \_ DS \_ CR \_ Impossibile \_ \_ convalidare**</span><span class="sxs-lookup"><span data-stu-id="93ba9-901"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERROR\_DS\_CR\_IMPOSSIBLE\_TO\_VALIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-902">8495 (0x212F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-902">8495 (0x212F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-903">La directory non è in grado di convalidare il nome del contesto di denominazione proposto perché non dispone di una replica del contesto dei nomi sopra il contesto dei nomi proposto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-903">The directory cannot validate the proposed naming context name because it does not hold a replica of the naming context above the proposed naming context.</span></span> <span data-ttu-id="93ba9-904">Verificare che il ruolo di master per la denominazione dei domini sia gestito da un server configurato come server di catalogo globale e che il server sia aggiornato con i partner di replica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-904">Please ensure that the domain naming master role is held by a server that is configured as a global catalog server, and that the server is up to date with its replication partners.</span></span> <span data-ttu-id="93ba9-905">(Si applica solo ai master per la denominazione dei domini di Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="93ba9-905">(Applies only to Windows 2000 Domain Naming masters.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-906"><span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERRORE \_ DS \_ DST \_ Domain \_ Not \_ native**</span><span class="sxs-lookup"><span data-stu-id="93ba9-906"><span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERROR\_DS\_DST\_DOMAIN\_NOT\_NATIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-907">8496 (0x2130)</span><span class="sxs-lookup"><span data-stu-id="93ba9-907">8496 (0x2130)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-908">Il dominio di destinazione deve essere in modalità nativa.</span><span class="sxs-lookup"><span data-stu-id="93ba9-908">Destination domain must be in native mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-909"><span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERRORE \_ DS \_ \_ contenitore infrastruttura \_ mancante**</span><span class="sxs-lookup"><span data-stu-id="93ba9-909"><span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERROR\_DS\_MISSING\_INFRASTRUCTURE\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-910">8497 (0x2131)</span><span class="sxs-lookup"><span data-stu-id="93ba9-910">8497 (0x2131)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-911">Non è possibile eseguire l'operazione perché il server non dispone di un contenitore di infrastruttura nel dominio di interesse.</span><span class="sxs-lookup"><span data-stu-id="93ba9-911">The operation cannot be performed because the server does not have an infrastructure container in the domain of interest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-912"><span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERRORE per lo \_ \_ spostamento del \_ \_ gruppo di account \_ di DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-912"><span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERROR\_DS\_CANT\_MOVE\_ACCOUNT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-913">8498 (0x2132)</span><span class="sxs-lookup"><span data-stu-id="93ba9-913">8498 (0x2132)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-914">Lo spostamento tra domini di gruppi di account non vuoti non è consentito.</span><span class="sxs-lookup"><span data-stu-id="93ba9-914">Cross-domain move of non-empty account groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-915"><span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERRORE \_ DS \_ Impossibile \_ spostare \_ il \_ gruppo di risorse**</span><span class="sxs-lookup"><span data-stu-id="93ba9-915"><span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERROR\_DS\_CANT\_MOVE\_RESOURCE\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-916">8499 (0x2133)</span><span class="sxs-lookup"><span data-stu-id="93ba9-916">8499 (0x2133)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-917">Lo spostamento tra domini di gruppi di risorse non vuoti non è consentito.</span><span class="sxs-lookup"><span data-stu-id="93ba9-917">Cross-domain move of non-empty resource groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-918"><span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**ERRORE \_ DS \_ - \_ flag di ricerca non valido \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-918"><span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-919">8500 (0x2134)</span><span class="sxs-lookup"><span data-stu-id="93ba9-919">8500 (0x2134)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-920">I flag di ricerca per l'attributo non sono validi.</span><span class="sxs-lookup"><span data-stu-id="93ba9-920">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="93ba9-921">Il bit ANR è valido solo per gli attributi delle stringhe Unicode o Teletex.</span><span class="sxs-lookup"><span data-stu-id="93ba9-921">The ANR bit is valid only on attributes of Unicode or Teletex strings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-922"><span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERRORE \_ DS \_ No \_ Tree \_ Delete \_ sopra \_ NC**</span><span class="sxs-lookup"><span data-stu-id="93ba9-922"><span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERROR\_DS\_NO\_TREE\_DELETE\_ABOVE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-923">8501 (0x2135)</span><span class="sxs-lookup"><span data-stu-id="93ba9-923">8501 (0x2135)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-924">Non sono consentite eliminazioni di albero a partire da un oggetto che ha un capo NC come discendente.</span><span class="sxs-lookup"><span data-stu-id="93ba9-924">Tree deletions starting at an object which has an NC head as a descendant are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-925"><span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERRORE \_ \_ \_ \_ dell'albero di blocco couldnt DS \_ per l' \_ eliminazione**</span><span class="sxs-lookup"><span data-stu-id="93ba9-925"><span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERROR\_DS\_COULDNT\_LOCK\_TREE\_FOR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-926">8502 (0x2136)</span><span class="sxs-lookup"><span data-stu-id="93ba9-926">8502 (0x2136)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-927">Il servizio directory non è riuscito a bloccare un albero per preparare l'eliminazione di un albero perché l'albero era in uso.</span><span class="sxs-lookup"><span data-stu-id="93ba9-927">The directory service failed to lock a tree in preparation for a tree deletion because the tree was in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-928"><span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERRORE \_ DS \_ couldnt \_ identificare \_ gli oggetti \_ per l' \_ eliminazione della struttura ad albero \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-928"><span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERROR\_DS\_COULDNT\_IDENTIFY\_OBJECTS\_FOR\_TREE\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-929">8503 (0x2137)</span><span class="sxs-lookup"><span data-stu-id="93ba9-929">8503 (0x2137)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-930">Il servizio directory non è riuscito a identificare l'elenco di oggetti da eliminare durante il tentativo di eliminazione di un albero.</span><span class="sxs-lookup"><span data-stu-id="93ba9-930">The directory service failed to identify the list of objects to delete while attempting a tree deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-931"><span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERRORE \_ di \_ \_ inizializzazione Sam DS \_ errore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-931"><span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERROR\_DS\_SAM\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-932">8504 (0x2138)</span><span class="sxs-lookup"><span data-stu-id="93ba9-932">8504 (0x2138)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-933">Inizializzazione gestione account di sicurezza non riuscita a causa dell'errore seguente: %1.</span><span class="sxs-lookup"><span data-stu-id="93ba9-933">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="93ba9-934">Stato di errore: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="93ba9-934">Error Status: 0x%2.</span></span> <span data-ttu-id="93ba9-935">Arrestare il sistema e riavviare in modalità ripristino servizi directory. per informazioni più dettagliate, vedere il registro eventi.</span><span class="sxs-lookup"><span data-stu-id="93ba9-935">Please shutdown this system and reboot into Directory Services Restore Mode, check the event log for more detailed information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-936"><span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**\_violazione del \_ \_ gruppo sensibile DS con \_ errori**</span><span class="sxs-lookup"><span data-stu-id="93ba9-936"><span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**ERROR\_DS\_SENSITIVE\_GROUP\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-937">8505 (0x2139)</span><span class="sxs-lookup"><span data-stu-id="93ba9-937">8505 (0x2139)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-938">Solo un amministratore può modificare l'elenco di appartenenze di un gruppo amministrativo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-938">Only an administrator can modify the membership list of an administrative group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-939"><span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERRORE \_ \_ mod. cant DS \_ \_ PRIMARYGROUPID**</span><span class="sxs-lookup"><span data-stu-id="93ba9-939"><span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERROR\_DS\_CANT\_MOD\_PRIMARYGROUPID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-940">8506 (0x213A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-940">8506 (0x213A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-941">Impossibile modificare l'ID gruppo primario di un account del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="93ba9-941">Cannot change the primary group ID of a domain controller account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-942"><span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERRORE \_ DS \_ schema di base non valido \_ \_ \_ mod**</span><span class="sxs-lookup"><span data-stu-id="93ba9-942"><span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERROR\_DS\_ILLEGAL\_BASE\_SCHEMA\_MOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-943">8507 (0x213B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-943">8507 (0x213B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-944">Viene effettuato un tentativo di modificare lo schema di base.</span><span class="sxs-lookup"><span data-stu-id="93ba9-944">An attempt is made to modify the base schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-945"><span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**\_ \_ \_ modifica dello schema non sicuro DS di errore \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-945"><span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**ERROR\_DS\_NONSAFE\_SCHEMA\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-946">8508 (0x213C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-946">8508 (0x213C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-947">Aggiunta di un nuovo attributo obbligatorio a una classe esistente, eliminazione di un attributo obbligatorio da una classe esistente o aggiunta di un attributo facoltativo alla classe speciale top che non è un attributo backlink (direttamente o tramite ereditarietà, ad esempio, aggiungendo o eliminando una classe ausiliaria) non è consentito.</span><span class="sxs-lookup"><span data-stu-id="93ba9-947">Adding a new mandatory attribute to an existing class, deleting a mandatory attribute from an existing class, or adding an optional attribute to the special class Top that is not a backlink attribute (directly or through inheritance, for example, by adding or deleting an auxiliary class) is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-948"><span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERRORE \_ di \_ aggiornamento dello schema DS non \_ \_ consentito**</span><span class="sxs-lookup"><span data-stu-id="93ba9-948"><span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERROR\_DS\_SCHEMA\_UPDATE\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-949">8509 (0x213D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-949">8509 (0x213D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-950">Aggiornamento dello schema non consentito in questo controller di dominio perché il controller di dominio non è il proprietario del ruolo FSMO dello schema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-950">Schema update is not allowed on this DC because the DC is not the schema FSMO Role Owner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-951"><span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERRORE durante la \_ \_ creazione del cant DS \_ \_ nello \_ schema**</span><span class="sxs-lookup"><span data-stu-id="93ba9-951"><span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERROR\_DS\_CANT\_CREATE\_UNDER\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-952">8510 (0x213E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-952">8510 (0x213E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-953">Non è possibile creare un oggetto di questa classe nel contenitore dello schema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-953">An object of this class cannot be created under the schema container.</span></span> <span data-ttu-id="93ba9-954">Nel contenitore dello schema è possibile creare solo oggetti Attribute-schema e classe-schema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-954">You can only create attribute-schema and class-schema objects under the schema container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-955"><span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERRORE \_ DS \_ installazione \_ Nessuna \_ \_ versione src SCH \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-955"><span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERROR\_DS\_INSTALL\_NO\_SRC\_SCH\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-956">8511 (0x213F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-956">8511 (0x213F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-957">L'installazione della replica/figlio non è riuscita a ottenere l'attributo objectVersion nel contenitore dello schema sul controller di dominio di origine.</span><span class="sxs-lookup"><span data-stu-id="93ba9-957">The replica/child install failed to get the objectVersion attribute on the schema container on the source DC.</span></span> <span data-ttu-id="93ba9-958">L'attributo non è presente nel contenitore dello schema oppure le credenziali specificate non dispongono dell'autorizzazione per leggerlo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-958">Either the attribute is missing on the schema container or the credentials supplied do not have permission to read it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-959"><span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERRORE \_ DS \_ installazione \_ Nessuna \_ \_ versione SCH \_ in \_ inifile**</span><span class="sxs-lookup"><span data-stu-id="93ba9-959"><span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERROR\_DS\_INSTALL\_NO\_SCH\_VERSION\_IN\_INIFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-960">8512 (0x2140)</span><span class="sxs-lookup"><span data-stu-id="93ba9-960">8512 (0x2140)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-961">L'installazione della replica/figlio non è riuscita a leggere l'attributo objectVersion nella sezione dello SCHEMA del file schema.ini nella directory system32.</span><span class="sxs-lookup"><span data-stu-id="93ba9-961">The replica/child install failed to read the objectVersion attribute in the SCHEMA section of the file schema.ini in the system32 directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-962"><span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERRORE \_ DS \_ \_ tipo di gruppo non valido \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-962"><span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERROR\_DS\_INVALID\_GROUP\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-963">8513 (0x2141)</span><span class="sxs-lookup"><span data-stu-id="93ba9-963">8513 (0x2141)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-964">Il tipo di gruppo specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="93ba9-964">The specified group type is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-965"><span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERRORE \_ DS \_ nessun \_ annidamento \_ GLOBALGROUP \_ in \_ MIXEDDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="93ba9-965"><span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERROR\_DS\_NO\_NEST\_GLOBALGROUP\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-966">8514 (0x2142)</span><span class="sxs-lookup"><span data-stu-id="93ba9-966">8514 (0x2142)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-967">Non è possibile nidificare i gruppi globali in un dominio misto se il gruppo è abilitato per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="93ba9-967">You cannot nest global groups in a mixed domain if the group is security-enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-968"><span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERRORE \_ DS \_ nessun \_ annidamento \_ localgroup \_ in \_ MIXEDDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="93ba9-968"><span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERROR\_DS\_NO\_NEST\_LOCALGROUP\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-969">8515 (0x2143)</span><span class="sxs-lookup"><span data-stu-id="93ba9-969">8515 (0x2143)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-970">Non è possibile nidificare i gruppi locali in un dominio misto se il gruppo è abilitato per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="93ba9-970">You cannot nest local groups in a mixed domain if the group is security-enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-971"><span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERRORE \_ DS \_ globale \_ non \_ presente \_ con \_ membro locale**</span><span class="sxs-lookup"><span data-stu-id="93ba9-971"><span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-972">8516 (0x2144)</span><span class="sxs-lookup"><span data-stu-id="93ba9-972">8516 (0x2144)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-973">Un gruppo globale non può avere un gruppo locale come membro.</span><span class="sxs-lookup"><span data-stu-id="93ba9-973">A global group cannot have a local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-974"><span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERRORE \_ DS \_ Global \_ cant \_ con \_ \_ membro universale**</span><span class="sxs-lookup"><span data-stu-id="93ba9-974"><span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_UNIVERSAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-975">8517 (0x2145)</span><span class="sxs-lookup"><span data-stu-id="93ba9-975">8517 (0x2145)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-976">Un gruppo globale non può avere un gruppo universale come membro.</span><span class="sxs-lookup"><span data-stu-id="93ba9-976">A global group cannot have a universal group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-977"><span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERRORE \_ DS \_ universale \_ non \_ può \_ avere \_ membro locale**</span><span class="sxs-lookup"><span data-stu-id="93ba9-977"><span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERROR\_DS\_UNIVERSAL\_CANT\_HAVE\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-978">8518 (0x2146)</span><span class="sxs-lookup"><span data-stu-id="93ba9-978">8518 (0x2146)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-979">Un gruppo universale non può avere un gruppo locale come membro.</span><span class="sxs-lookup"><span data-stu-id="93ba9-979">A universal group cannot have a local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-980"><span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERRORE \_ DS \_ Global \_ cant \_ con \_ \_ membro CROSSDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="93ba9-980"><span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_CROSSDOMAIN\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-981">8519 (0x2147)</span><span class="sxs-lookup"><span data-stu-id="93ba9-981">8519 (0x2147)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-982">Un gruppo globale non può avere un membro tra domini.</span><span class="sxs-lookup"><span data-stu-id="93ba9-982">A global group cannot have a cross-domain member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-983"><span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERRORE nel servizio \_ locale DS con \_ \_ \_ \_ CROSSDOMAIN \_ \_ membro locale**</span><span class="sxs-lookup"><span data-stu-id="93ba9-983"><span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERROR\_DS\_LOCAL\_CANT\_HAVE\_CROSSDOMAIN\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-984">8520 (0x2148)</span><span class="sxs-lookup"><span data-stu-id="93ba9-984">8520 (0x2148)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-985">Un gruppo locale non può avere un altro gruppo locale tra domini come membro.</span><span class="sxs-lookup"><span data-stu-id="93ba9-985">A local group cannot have another cross domain local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-986"><span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**ERRORE \_ DS \_ con \_ \_ membri primari**</span><span class="sxs-lookup"><span data-stu-id="93ba9-986"><span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**ERROR\_DS\_HAVE\_PRIMARY\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-987">8521 (0x2149)</span><span class="sxs-lookup"><span data-stu-id="93ba9-987">8521 (0x2149)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-988">Un gruppo con membri primari non può essere modificato in un gruppo disabilitato per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="93ba9-988">A group with primary members cannot change to a security-disabled group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-989"><span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERRORE \_ di \_ \_ conversione SD stringa DS \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="93ba9-989"><span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERROR\_DS\_STRING\_SD\_CONVERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-990">8522 (0x214A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-990">8522 (0x214A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-991">Il caricamento della cache dello schema non è riuscito a convertire la stringa SD predefinita in un oggetto dello schema di classe.</span><span class="sxs-lookup"><span data-stu-id="93ba9-991">The schema cache load failed to convert the string default SD on a class-schema object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-992"><span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERRORE \_ GC per la \_ denominazione \_ Master DS \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-992"><span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERROR\_DS\_NAMING\_MASTER\_GC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-993">8523 (0x214B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-993">8523 (0x214B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-994">Solo DSA configurato come server di catalogo globale deve essere autorizzato a contenere il ruolo FSMO master per la denominazione dei domini.</span><span class="sxs-lookup"><span data-stu-id="93ba9-994">Only DSAs configured to be Global Catalog servers should be allowed to hold the Domain Naming Master FSMO role.</span></span> <span data-ttu-id="93ba9-995">(Si applica solo ai server Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="93ba9-995">(Applies only to Windows 2000 servers.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-996"><span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERRORE \_ di \_ ricerca DNS DS \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-996"><span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERROR\_DS\_DNS\_LOOKUP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-997">8524 (0x214C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-997">8524 (0x214C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-998">Non è possibile continuare l'operazione DSA a causa di un errore di ricerca DNS.</span><span class="sxs-lookup"><span data-stu-id="93ba9-998">The DSA operation is unable to proceed because of a DNS lookup failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-999"><span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**ERRORE \_ \_ \_ SPN aggiornamento couldnt \_ DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-999"><span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**ERROR\_DS\_COULDNT\_UPDATE\_SPNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1000">8525 (0x214D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1000">8525 (0x214D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1001">Durante l'elaborazione di una modifica al nome host DNS per un oggetto, i valori del nome dell'entità servizio non possono essere mantenuti sincronizzati.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1001">While processing a change to the DNS Host Name for an object, the Service Principal Name values could not be kept in sync.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1002"><span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERRORE \_ di \_ \_ recupero \_ SD**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1002"><span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERROR\_DS\_CANT\_RETRIEVE\_SD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1003">8526 (0x214E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1003">8526 (0x214E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1004">Impossibile leggere l'attributo del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1004">The Security Descriptor attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1005"><span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERRORE \_ \_ chiave DS \_ non \_ univoca**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1005"><span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERROR\_DS\_KEY\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1006">8527 (0x214F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1006">8527 (0x214F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1007">L'oggetto richiesto non è stato trovato, ma è stato trovato un oggetto con tale chiave.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1007">The object requested was not found, but an object with that key was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1008"><span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERRORE \_ DS \_ - \_ \_ sintassi att \_ collegata errata**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1008"><span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERROR\_DS\_WRONG\_LINKED\_ATT\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1009">8528 (0x2150)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1009">8528 (0x2150)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1010">La sintassi dell'attributo collegato aggiunto non è corretta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1010">The syntax of the linked attribute being added is incorrect.</span></span> <span data-ttu-id="93ba9-1011">I collegamenti in diretta possono avere solo la sintassi 2.5.5.1, 2.5.5.7 e 2.5.5.14 e i backlink possono avere solo la sintassi 2.5.5.1.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1011">Forward links can only have syntax 2.5.5.1, 2.5.5.7, and 2.5.5.14, and backlinks can only have syntax 2.5.5.1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1012"><span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERRORE \_ DS \_ Sam \_ need \_ BOOTKEY \_ password**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1012"><span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERROR\_DS\_SAM\_NEED\_BOOTKEY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1013">8529 (0x2151)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1013">8529 (0x2151)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1014">Security Account Manager deve ottenere la password di avvio.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1014">Security Account Manager needs to get the boot password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1015"><span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERRORE \_ DS \_ Sam \_ need \_ \_ floppy BOOTKEY**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1015"><span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERROR\_DS\_SAM\_NEED\_BOOTKEY\_FLOPPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1016">8530 (0x2152)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1016">8530 (0x2152)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1017">Security Account Manager deve ottenere la chiave di avvio dal disco floppy.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1017">Security Account Manager needs to get the boot key from floppy disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1018"><span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERRORE \_ di \_ avvio del cant DS \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1018"><span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERROR\_DS\_CANT\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1019">8531 (0x2153)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1019">8531 (0x2153)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1020">Impossibile avviare il servizio directory.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1020">Directory Service cannot start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1021"><span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERRORE \_ di \_ init DS errore \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1021"><span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERROR\_DS\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1022">8532 (0x2154)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1022">8532 (0x2154)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1023">Impossibile avviare i servizi directory.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1023">Directory Services could not start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1024"><span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERRORE \_ DS \_ No \_ PKT \_ privacy \_ on \_ Connection**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1024"><span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERROR\_DS\_NO\_PKT\_PRIVACY\_ON\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1025">8533 (0x2155)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1025">8533 (0x2155)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1026">Per la connessione tra client e server è richiesta la riservatezza dei pacchetti o una soluzione migliore.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1026">The connection between client and server requires packet privacy or better.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1027"><span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERRORE \_ \_ \_ dominio di origine DS \_ nella \_ foresta**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1027"><span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERROR\_DS\_SOURCE\_DOMAIN\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1028">8534 (0x2156)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1028">8534 (0x2156)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1029">Il dominio di origine potrebbe non trovarsi nella stessa foresta della destinazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1029">The source domain may not be in the same forest as destination.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1030"><span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERRORE \_ \_ \_ dominio di destinazione DS non presente \_ \_ nella \_ foresta**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1030"><span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERROR\_DS\_DESTINATION\_DOMAIN\_NOT\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1031">8535 (0x2157)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1031">8535 (0x2157)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1032">Il dominio di destinazione deve essere presente nell'insieme di strutture.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1032">The destination domain must be in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1033"><span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**controllo della destinazione di DS con errori \_ \_ \_ \_ non \_ abilitato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1033"><span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**ERROR\_DS\_DESTINATION\_AUDITING\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1034">8536 (0x2158)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1034">8536 (0x2158)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1035">Per l'operazione è necessario che sia abilitato il controllo del dominio di destinazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1035">The operation requires that destination domain auditing be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1036"><span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERRORE \_ DS \_ \_ trovare il \_ controller \_ di \_ dominio per il \_ dominio src**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1036"><span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERROR\_DS\_CANT\_FIND\_DC\_FOR\_SRC\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1037">8537 (0x2159)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1037">8537 (0x2159)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1038">L'operazione non è riuscita a individuare un controller di dominio per il dominio di origine.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1038">The operation couldn't locate a DC for the source domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1039"><span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERRORE \_ DS \_ src \_ obj \_ non \_ gruppo \_ o \_ utente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1039"><span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERROR\_DS\_SRC\_OBJ\_NOT\_GROUP\_OR\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1040">8538 (0x215A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1040">8538 (0x215A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1041">L'oggetto di origine deve essere un gruppo o un utente.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1041">The source object must be a group or user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1042"><span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERRORE \_ il \_ SID src DS \_ \_ esiste \_ nella \_ foresta**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1042"><span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERROR\_DS\_SRC\_SID\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1043">8539 (0x215B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1043">8539 (0x215B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1044">Il SID dell'oggetto di origine esiste già nella foresta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1044">The source object's SID already exists in destination forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1045"><span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERRORE \_ DS \_ src \_ e \_ DST \_ classe di oggetti non \_ \_ corrispondenti**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1045"><span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERROR\_DS\_SRC\_AND\_DST\_OBJECT\_CLASS\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1046">8540 (0x215C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1046">8540 (0x215C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1047">L'oggetto di origine e di destinazione deve essere dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1047">The source and destination object must be of the same type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1048"><span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERRORE \_ di \_ inizializzazione Sam \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1048"><span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERROR\_SAM\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1049">8541 (0x215D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1049">8541 (0x215D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1050">Inizializzazione gestione account di sicurezza non riuscita a causa dell'errore seguente: %1.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1050">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="93ba9-1051">Stato di errore: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1051">Error Status: 0x%2.</span></span> <span data-ttu-id="93ba9-1052">Fare clic su OK per arrestare il sistema e riavviare in modalità provvisoria.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1052">Click OK to shut down the system and reboot into Safe Mode.</span></span> <span data-ttu-id="93ba9-1053">Per informazioni dettagliate, vedere il registro eventi.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1053">Check the event log for detailed information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1054"><span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERRORE \_ DS servizio di \_ \_ informazioni dello schema DRA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1054"><span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERROR\_DS\_DRA\_SCHEMA\_INFO\_SHIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1055">8542 (0x215E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1055">8542 (0x215E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1056">Non è stato possibile includere le informazioni sullo schema nella richiesta di replica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1056">Schema information could not be included in the replication request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1057"><span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERRORE \_ \_ \_ dello schema DRA \_ DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1057"><span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERROR\_DS\_DRA\_SCHEMA\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1058">8543 (0x215F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1058">8543 (0x215F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1059">Non è stato possibile completare l'operazione di replica a causa di un'incompatibilità dello schema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1059">The replication operation could not be completed due to a schema incompatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1060"><span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERRORE \_ DS \_ DRA \_ precedente \_ \_ conflitto schema**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1060"><span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERROR\_DS\_DRA\_EARLIER\_SCHEMA\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1061">8544 (0x2160)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1061">8544 (0x2160)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1062">Non è stato possibile completare l'operazione di replica a causa di un'incompatibilità dello schema precedente.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1062">The replication operation could not be completed due to a previous schema incompatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1063"><span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERRORE \_ DS \_ DRA \_ obj \_ NC non \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1063"><span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERROR\_DS\_DRA\_OBJ\_NC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1064">8545 (0x2161)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1064">8545 (0x2161)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1065">Non è stato possibile applicare l'aggiornamento della replica perché l'origine o la destinazione non ha ancora ricevuto informazioni relative a un'operazione di spostamento tra domini recente.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1065">The replication update could not be applied because either the source or the destination has not yet received information regarding a recent cross-domain move operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1066"><span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**ERRORE del controller di \_ dominio DS \_ \_ \_ con \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1066"><span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**ERROR\_DS\_NC\_STILL\_HAS\_DSAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1067">8546 (0x2162)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1067">8546 (0x2162)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1068">Non è stato possibile eliminare il dominio richiesto perché esistono controller di dominio che ospitano ancora questo dominio.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1068">The requested domain could not be deleted because there exist domain controllers that still host this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1069"><span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERRORE \_ \_ GC DS \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1069"><span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERROR\_DS\_GC\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1070">8547 (0x2163)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1070">8547 (0x2163)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1071">L'operazione richiesta può essere eseguita solo in un server di catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1071">The requested operation can be performed only on a global catalog server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1072"><span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERRORE \_ DS \_ locale \_ membro \_ locale \_ \_ solo locale**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1072"><span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERROR\_DS\_LOCAL\_MEMBER\_OF\_LOCAL\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1073">8548 (0x2164)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1073">8548 (0x2164)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1074">Un gruppo locale può essere solo un membro di altri gruppi locali nello stesso dominio.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1074">A local group can only be a member of other local groups in the same domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1075"><span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERRORE \_ DS \_ Nessuna \_ Polinesia \_ nei \_ gruppi universali \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1075"><span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERROR\_DS\_NO\_FPO\_IN\_UNIVERSAL\_GROUPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1076">8549 (0x2165)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1076">8549 (0x2165)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1077">Le entità di sicurezza esterne non possono essere membri di gruppi universali.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1077">Foreign security principals cannot be members of universal groups.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1078"><span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERRORE \_ DS non è \_ \_ \_ possibile aggiungere a \_ GC**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1078"><span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERROR\_DS\_CANT\_ADD\_TO\_GC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1079">8550 (0x2166)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1079">8550 (0x2166)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1080">Per motivi di sicurezza, l'attributo non può essere replicato nel catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1080">The attribute is not allowed to be replicated to the GC because of security reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1081"><span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERRORE \_ DS \_ nessun \_ Checkpoint \_ con \_ PDC**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1081"><span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERROR\_DS\_NO\_CHECKPOINT\_WITH\_PDC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1082">8551 (0x2167)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1082">8551 (0x2167)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1083">Non è stato possibile usare il checkpoint con PDC perché il numero di modifiche attualmente elaborate è eccessivo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1083">The checkpoint with the PDC could not be taken because there too many modifications being processed currently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1084"><span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**\_ \_ controllo origine errore DS \_ \_ non \_ abilitato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1084"><span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**ERROR\_DS\_SOURCE\_AUDITING\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1085">8552 (0x2168)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1085">8552 (0x2168)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1086">Per l'operazione è necessario che sia abilitato il controllo del dominio di origine.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1086">The operation requires that source domain auditing be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1087"><span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERRORE \_ \_ durante la \_ creazione del cant DS \_ nel NC di non \_ dominio \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1087"><span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERROR\_DS\_CANT\_CREATE\_IN\_NONDOMAIN\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1088">8553 (0x2169)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1088">8553 (0x2169)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1089">Gli oggetti entità di sicurezza possono essere creati solo all'interno di contesti di denominazione dei domini.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1089">Security principal objects can only be created inside domain naming contexts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1090"><span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERRORE \_ DS \_ nome non valido \_ \_ per \_ SPN**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1090"><span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERROR\_DS\_INVALID\_NAME\_FOR\_SPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1091">8554 (0x216A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1091">8554 (0x216A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1092">Non è stato possibile costruire un nome dell'entità servizio (SPN) perché il nome host specificato non è nel formato necessario.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1092">A Service Principal Name (SPN) could not be constructed because the provided hostname is not in the necessary format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1093"><span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**ERRORE \_ il \_ filtro DS \_ Usa \_ CONTRUCTED \_ attrs**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1093"><span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**ERROR\_DS\_FILTER\_USES\_CONTRUCTED\_ATTRS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1094">8555 (0x216B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1094">8555 (0x216B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1095">È stato passato un filtro che usa attributi costruiti.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1095">A Filter was passed that uses constructed attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1096"><span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERRORE \_ \_ UNICODEPWD DS \_ non \_ tra \_ virgolette**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1096"><span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERROR\_DS\_UNICODEPWD\_NOT\_IN\_QUOTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1097">8556 (0x216C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1097">8556 (0x216C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1098">Il valore dell'attributo unicodePwd deve essere racchiuso tra virgolette doppie.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1098">The unicodePwd attribute value must be enclosed in double quotes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1099"><span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERRORE \_ di \_ \_ quota account computer DS \_ \_ superata**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1099"><span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERROR\_DS\_MACHINE\_ACCOUNT\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1100">8557 (0x216D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1100">8557 (0x216D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1101">Il computer non è stato aggiunto al dominio.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1101">Your computer could not be joined to the domain.</span></span> <span data-ttu-id="93ba9-1102">È stato superato il numero massimo di account computer che è possibile creare in questo dominio.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1102">You have exceeded the maximum number of computer accounts you are allowed to create in this domain.</span></span> <span data-ttu-id="93ba9-1103">Contattare l'amministratore di sistema per impostare o aumentare il limite.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1103">Contact your system administrator to have this limit reset or increased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1104"><span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**\_ \_ è necessario eseguire l'errore DS \_ \_ \_ sul controller di dominio \_ DST \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1104"><span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**ERROR\_DS\_MUST\_BE\_RUN\_ON\_DST\_DC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1105">8558 (0x216E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1105">8558 (0x216E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1106">Per motivi di sicurezza, è necessario eseguire l'operazione nel controller di dominio di destinazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1106">For security reasons, the operation must be run on the destination DC.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1107"><span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERRORE \_ DS \_ src \_ DC \_ deve \_ essere \_ SP4 \_ o \_ versione successiva**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1107"><span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERROR\_DS\_SRC\_DC\_MUST\_BE\_SP4\_OR\_GREATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1108">8559 (0x216F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1108">8559 (0x216F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1109">Per motivi di sicurezza, il controller di dominio di origine deve essere NT4SP4 o superiore.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1109">For security reasons, the source DC must be NT4SP4 or greater.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1110"><span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERRORE \_ di \_ \_ eliminazione dell'albero del cant \_ \_ critico \_ di DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1110"><span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERROR\_DS\_CANT\_TREE\_DELETE\_CRITICAL\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1111">8560 (0x2170)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1111">8560 (0x2170)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1112">Impossibile eliminare gli oggetti critici del sistema del servizio directory durante le operazioni di eliminazione della struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1112">Critical Directory Service System objects cannot be deleted during tree delete operations.</span></span> <span data-ttu-id="93ba9-1113">È possibile che l'eliminazione della struttura ad albero sia stata eseguita parzialmente.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1113">The tree delete may have been partially performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1114"><span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERRORE \_ nella \_ console di inizializzazione non riuscita di DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1114"><span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERROR\_DS\_INIT\_FAILURE\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1115">8561 (0x2171)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1115">8561 (0x2171)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1116">Impossibile avviare i servizi directory a causa del seguente errore: %1.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1116">Directory Services could not start because of the following error: %1.</span></span> <span data-ttu-id="93ba9-1117">Stato di errore: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1117">Error Status: 0x%2.</span></span> <span data-ttu-id="93ba9-1118">Per arrestare il sistema, fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1118">Please click OK to shutdown the system.</span></span> <span data-ttu-id="93ba9-1119">È possibile usare la Console di ripristino di emergenza per diagnosticare più approfonditamente il problema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1119">You can use the recovery console to diagnose the system further.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1120"><span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERRORE nella console di errore \_ DS \_ Sam \_ init \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1120"><span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERROR\_DS\_SAM\_INIT\_FAILURE\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1121">8562 (0x2172)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1121">8562 (0x2172)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1122">Inizializzazione gestione account di sicurezza non riuscita a causa dell'errore seguente: %1.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1122">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="93ba9-1123">Stato di errore: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1123">Error Status: 0x%2.</span></span> <span data-ttu-id="93ba9-1124">Per arrestare il sistema, fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1124">Please click OK to shutdown the system.</span></span> <span data-ttu-id="93ba9-1125">È possibile usare la Console di ripristino di emergenza per diagnosticare più approfonditamente il problema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1125">You can use the recovery console to diagnose the system further.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1126"><span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERRORE \_ \_ versione foresta \_ DS \_ troppo \_ elevata**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1126"><span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERROR\_DS\_FOREST\_VERSION\_TOO\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1127">8563 (0x2173)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1127">8563 (0x2173)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1128">La versione del sistema operativo non è compatibile con il livello di funzionalità della foresta di servizi di dominio Active Directory corrente o il livello di funzionalità del set di configurazione AD LDS.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1128">The version of the operating system is incompatible with the current AD DS forest functional level or AD LDS Configuration Set functional level.</span></span> <span data-ttu-id="93ba9-1129">È necessario eseguire l'aggiornamento a una nuova versione del sistema operativo prima che il server possa diventare un controller di dominio di servizi di dominio Active Directory o aggiungere un'istanza di AD LDS in questa foresta di servizi di dominio Active Directory o AD LDS set di configurazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1129">You must upgrade to a new version of the operating system before this server can become an AD DS Domain Controller or add an AD LDS Instance in this AD DS Forest or AD LDS Configuration Set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1130"><span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERRORE \_ \_ versione dominio \_ DS \_ troppo \_ alta**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1130"><span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERROR\_DS\_DOMAIN\_VERSION\_TOO\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1131">8564 (0x2174)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1131">8564 (0x2174)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1132">La versione del sistema operativo installata non è compatibile con il livello di funzionalità del dominio corrente.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1132">The version of the operating system installed is incompatible with the current domain functional level.</span></span> <span data-ttu-id="93ba9-1133">È necessario eseguire l'aggiornamento a una nuova versione del sistema operativo prima che il server possa diventare un controller di dominio in questo dominio.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1133">You must upgrade to a new version of the operating system before this server can become a domain controller in this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1134"><span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERRORE \_ \_ versione foresta \_ DS \_ troppo \_ bassa**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1134"><span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERROR\_DS\_FOREST\_VERSION\_TOO\_LOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1135">8565 (0x2175)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1135">8565 (0x2175)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1136">La versione del sistema operativo installata in questo server non supporta più il livello di funzionalità della foresta di servizi di dominio Active Directory corrente o il livello di funzionalità del set di configurazione AD LDS.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1136">The version of the operating system installed on this server no longer supports the current AD DS Forest functional level or AD LDS Configuration Set functional level.</span></span> <span data-ttu-id="93ba9-1137">È necessario aumentare il livello di funzionalità della foresta di Active Directory Domain Services o AD LDS il livello di funzionalità del set di configurazione prima che il server possa diventare un controller di dominio di servizi di dominio Active Directory o un'istanza AD LDS in questa foresta o set</span><span class="sxs-lookup"><span data-stu-id="93ba9-1137">You must raise the AD DS Forest functional level or AD LDS Configuration Set functional level before this server can become an AD DS Domain Controller or an AD LDS Instance in this Forest or Configuration Set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1138"><span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERRORE \_ \_ versione dominio \_ DS \_ troppo \_ basso**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1138"><span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERROR\_DS\_DOMAIN\_VERSION\_TOO\_LOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1139">8566 (0x2176)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1139">8566 (0x2176)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1140">La versione del sistema operativo installata in questo server non supporta più il livello di funzionalità del dominio corrente.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1140">The version of the operating system installed on this server no longer supports the current domain functional level.</span></span> <span data-ttu-id="93ba9-1141">È necessario aumentare il livello di funzionalità del dominio prima che il server possa diventare un controller di dominio in questo dominio.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1141">You must raise the domain functional level before this server can become a domain controller in this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1142"><span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**\_versione non \_ compatibile DS degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1142"><span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**ERROR\_DS\_INCOMPATIBLE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1143">8567 (0x2177)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1143">8567 (0x2177)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1144">La versione del sistema operativo installata in questo server non è compatibile con il livello di funzionalità del dominio o della foresta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1144">The version of the operating system installed on this server is incompatible with the functional level of the domain or forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1145"><span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERRORE \_ DS \_ \_ versione bassa DSA \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1145"><span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERROR\_DS\_LOW\_DSA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1146">8568 (0x2178)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1146">8568 (0x2178)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1147">Non è possibile aumentare il livello di funzionalità del dominio (o della foresta) al valore richiesto perché esistono uno o più controller di dominio nel dominio o nella foresta con un livello di funzionalità non compatibile più basso.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1147">The functional level of the domain (or forest) cannot be raised to the requested value, because there exist one or more domain controllers in the domain (or forest) that are at a lower incompatible functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1148"><span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERRORE \_ DS \_ Nessuna \_ \_ versione \_ del comportamento in \_ MIXEDDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1148"><span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERROR\_DS\_NO\_BEHAVIOR\_VERSION\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1149">8569 (0x2179)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1149">8569 (0x2179)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1150">Impossibile elevare il livello di funzionalità della foresta al valore richiesto perché uno o più domini sono ancora in modalità di dominio misto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1150">The forest functional level cannot be raised to the requested value since one or more domains are still in mixed domain mode.</span></span> <span data-ttu-id="93ba9-1151">Tutti i domini nella foresta devono essere in modalità nativa, in modo da aumentare il livello di funzionalità della foresta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1151">All domains in the forest must be in native mode, for you to raise the forest functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1152"><span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ERRORE \_ DS \_ non \_ supportato \_ per il tipo di ordinamento \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1152"><span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ERROR\_DS\_NOT\_SUPPORTED\_SORT\_ORDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1153">8570 (0x217A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1153">8570 (0x217A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1154">Il tipo di ordinamento richiesto non è supportato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1154">The sort order requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1155"><span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**ERRORE \_ \_ nome DS \_ non \_ univoco**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1155"><span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**ERROR\_DS\_NAME\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1156">8571 (0x217B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1156">8571 (0x217B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1157">Il nome richiesto esiste già come identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1157">The requested name already exists as a unique identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1158"><span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERRORE \_ dell' \_ account computer DS \_ \_ creato \_ PRENT4**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1158"><span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERROR\_DS\_MACHINE\_ACCOUNT\_CREATED\_PRENT4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1159">8572 (0x217C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1159">8572 (0x217C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1160">L'account del computer è stato creato prima di NT4.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1160">The machine account was created pre-NT4.</span></span> <span data-ttu-id="93ba9-1161">È necessario ricreare l'account.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1161">The account needs to be recreated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1162"><span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERRORE \_ DS \_ dall' \_ \_ Archivio delle versioni \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1162"><span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERROR\_DS\_OUT\_OF\_VERSION\_STORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1163">8573 (0x217D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1163">8573 (0x217D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1164">Il database non è presente nell'archivio delle versioni.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1164">The database is out of version store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1165"><span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**controlli di errore \_ DS \_ incompatibili \_ \_ utilizzati**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1165"><span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**ERROR\_DS\_INCOMPATIBLE\_CONTROLS\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1166">8574 (0x217E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1166">8574 (0x217E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1167">Non è possibile continuare l'operazione perché sono stati usati più controlli in conflitto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1167">Unable to continue operation because multiple conflicting controls were used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1168"><span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERRORE \_ DS \_ nessun \_ dominio di riferimento \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1168"><span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERROR\_DS\_NO\_REF\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1169">8575 (0x217F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1169">8575 (0x217F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1170">Impossibile trovare un dominio di riferimento del descrittore di sicurezza valido per questa partizione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1170">Unable to find a valid security descriptor reference domain for this partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1171"><span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**\_ \_ \_ ID collegamento riservato DS \_ errore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1171"><span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**ERROR\_DS\_RESERVED\_LINK\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1172">8576 (0x2180)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1172">8576 (0x2180)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1173">Aggiornamento dello schema non riuscito: l'identificatore di collegamento è riservato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1173">Schema update failed: The link identifier is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1174"><span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**\_ \_ ID collegamento DS \_ errore \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1174"><span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**ERROR\_DS\_LINK\_ID\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1175">8577 (0x2181)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1175">8577 (0x2181)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1176">Aggiornamento dello schema non riuscito: non sono disponibili identificatori di collegamento.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1176">Schema update failed: There are no link identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1177"><span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERRORE \_ DS \_ AG \_ cant \_ con \_ \_ membro universale**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1177"><span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERROR\_DS\_AG\_CANT\_HAVE\_UNIVERSAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1178">8578 (0x2182)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1178">8578 (0x2182)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1179">Un gruppo di account non può avere un gruppo universale come membro.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1179">An account group cannot have a universal group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1180"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERRORE \_ DS \_ MODIFYDN del non \_ consentito \_ dal \_ tipo di istanza \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1180"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERROR\_DS\_MODIFYDN\_DISALLOWED\_BY\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1181">8579 (0x2183)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1181">8579 (0x2183)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1182">Non sono consentite operazioni di ridenominazione o spostamento in intestazioni di contesto dei nomi o oggetti di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1182">Rename or move operations on naming context heads or read-only objects are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1183"><span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERRORE \_ DS \_ nessun \_ oggetto \_ spostamento \_ nel \_ NC dello schema \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1183"><span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERROR\_DS\_NO\_OBJECT\_MOVE\_IN\_SCHEMA\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1184">8580 (0x2184)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1184">8580 (0x2184)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1185">Non sono consentite operazioni di spostamento sugli oggetti nel contesto dei nomi di schema.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1185">Move operations on objects in the schema naming context are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1186"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERRORE \_ DS \_ MODIFYDN del non \_ consentito \_ dal \_ flag**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1186"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERROR\_DS\_MODIFYDN\_DISALLOWED\_BY\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1187">8581 (0x2185)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1187">8581 (0x2185)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1188">Un flag di sistema è stato impostato sull'oggetto e non consente lo spostamento o la ridenominazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1188">A system flag has been set on the object and does not allow the object to be moved or renamed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1189"><span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERRORE \_ DS \_ MODIFYDN del \_ \_ padre errato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1189"><span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERROR\_DS\_MODIFYDN\_WRONG\_GRANDPARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1190">8582 (0x2186)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1190">8582 (0x2186)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1191">Questo oggetto non è autorizzato a modificare il relativo contenitore padre.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1191">This object is not allowed to change its grandparent container.</span></span> <span data-ttu-id="93ba9-1192">Lo spostamento non è consentito per questo oggetto, ma è limitato ai contenitori di pari livello.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1192">Moves are not forbidden on this object, but are restricted to sibling containers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1193"><span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERRORE \_ \_ nome servizio \_ DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1193"><span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERROR\_DS\_NAME\_ERROR\_TRUST\_REFERRAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1194">8583 (0x2187)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1194">8583 (0x2187)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1195">Impossibile risolvere completamente, viene generato un riferimento a un'altra foresta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1195">Unable to resolve completely, a referral to another forest is generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1196"><span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERRORE \_ non \_ supportato \_ nel \_ \_ server standard**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1196"><span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERROR\_NOT\_SUPPORTED\_ON\_STANDARD\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1197">8584 (0x2188)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1197">8584 (0x2188)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1198">L'azione richiesta non è supportata nel server standard.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1198">The requested action is not supported on standard server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1199"><span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERRORE \_ \_ \_ di accesso non è possibile accedere \_ a una \_ parte remota \_ di \_ Active Directory**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1199"><span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERROR\_DS\_CANT\_ACCESS\_REMOTE\_PART\_OF\_AD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1200">8585 (0x2189)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1200">8585 (0x2189)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1201">Non è stato possibile accedere a una partizione del servizio directory che si trova in un server remoto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1201">Could not access a partition of the directory service located on a remote server.</span></span> <span data-ttu-id="93ba9-1202">Assicurarsi che almeno un server sia in esecuzione per la partizione in questione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1202">Make sure at least one server is running for the partition in question.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1203"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERRORE \_ DS \_ CR \_ Impossibile \_ \_ convalidare \_ v2**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1203"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERROR\_DS\_CR\_IMPOSSIBLE\_TO\_VALIDATE\_V2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1204">8586 (0x218A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1204">8586 (0x218A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1205">La directory non può convalidare il nome del contesto dei nomi proposto (o partizione) perché non è presente una replica né può contattare una replica del contesto dei nomi sopra il contesto dei nomi proposto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1205">The directory cannot validate the proposed naming context (or partition) name because it does not hold a replica nor can it contact a replica of the naming context above the proposed naming context.</span></span> <span data-ttu-id="93ba9-1206">Verificare che il contesto dei nomi padre sia registrato correttamente in DNS e che almeno una replica del contesto dei nomi sia raggiungibile dal master per la denominazione dei domini.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1206">Please ensure that the parent naming context is properly registered in DNS, and at least one replica of this naming context is reachable by the Domain Naming master.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1207"><span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**\_ \_ \_ superato limite thread DS \_ errore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1207"><span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**ERROR\_DS\_THREAD\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1208">8587 (0x218B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1208">8587 (0x218B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1209">È stato superato il limite di thread per questa richiesta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1209">The thread limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1210"><span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERRORE \_ DS \_ non \_ più vicino**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1210"><span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERROR\_DS\_NOT\_CLOSEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1211">8588 (0x218C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1211">8588 (0x218C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1212">Il server di catalogo globale non si trova nel sito più vicino.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1212">The Global catalog server is not in the closest site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1213"><span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERRORE \_ DS \_ cant \_ derivare \_ SPN \_ senza \_ \_ ref server**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1213"><span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERROR\_DS\_CANT\_DERIVE\_SPN\_WITHOUT\_SERVER\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1214">8589 (0x218D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1214">8589 (0x218D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1215">DS non può derivare un nome dell'entità servizio (SPN) per l'autenticazione reciproca del server di destinazione perché l'oggetto server corrispondente nel database DS locale non dispone di un attributo serverReference.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1215">The DS cannot derive a service principal name (SPN) with which to mutually authenticate the target server because the corresponding server object in the local DS database has no serverReference attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1216"><span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERRORE \_ DS \_ \_ modalità utente \_ singolo \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1216"><span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERROR\_DS\_SINGLE\_USER\_MODE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1217">8590 (0x218E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1217">8590 (0x218E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1218">Il servizio directory non è stato in grado di attivare la modalità utente singolo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1218">The Directory Service failed to enter single user mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1219"><span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**errore di \_ sintassi di DS \_ NTDSCRIPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1219"><span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**ERROR\_DS\_NTDSCRIPT\_SYNTAX\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1220">8591 (0x218F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1220">8591 (0x218F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1221">Il servizio directory non è in grado di analizzare lo script a causa di un errore di sintassi.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1221">The Directory Service cannot parse the script because of a syntax error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1222"><span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**errore \_ di \_ elaborazione NTDSCRIPT DS \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1222"><span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**ERROR\_DS\_NTDSCRIPT\_PROCESS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1223">8592 (0x2190)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1223">8592 (0x2190)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1224">Il servizio directory non è in grado di elaborare lo script a causa di un errore.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1224">The Directory Service cannot process the script because of an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1225"><span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ERRORE \_ DS \_ \_ REPL diverse \_ epoche**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1225"><span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ERROR\_DS\_DIFFERENT\_REPL\_EPOCHS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1226">8593 (0x2191)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1226">8593 (0x2191)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1227">Il servizio directory non è in grado di eseguire l'operazione richiesta perché i server interessati sono di epoche di replica diverse (che in genere sono correlati a una ridenominazione del dominio in corso).</span><span class="sxs-lookup"><span data-stu-id="93ba9-1227">The directory service cannot perform the requested operation because the servers involved are of different replication epochs (which is usually related to a domain rename that is in progress).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1228"><span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**ERRORE \_ DS \_ DRS \_ Extensions \_ modificate**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1228"><span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**ERROR\_DS\_DRS\_EXTENSIONS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1229">8594 (0x2192)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1229">8594 (0x2192)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1230">È necessario rinegoziare l'associazione al servizio directory a causa di una modifica nelle informazioni sulle estensioni del server.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1230">The directory service binding must be renegotiated due to a change in the server extensions information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1231"><span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERRORE \_ \_ \_ \_ di modifica del set di repliche DS \_ non \_ consentita \_ su \_ CR disabilitato \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1231"><span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERROR\_DS\_REPLICA\_SET\_CHANGE\_NOT\_ALLOWED\_ON\_DISABLED\_CR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1232">8595 (0x2193)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1232">8595 (0x2193)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1233">Operazione non consentita su un riferimento incrociato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1233">Operation not allowed on a disabled cross ref.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1234"><span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERRORE \_ DS \_ nessun \_ msDS \_ IntID**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1234"><span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERROR\_DS\_NO\_MSDS\_INTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1235">8596 (0x2194)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1235">8596 (0x2194)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1236">Errore di aggiornamento dello schema: non sono disponibili valori per msDS-IntId.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1236">Schema update failed: No values for msDS-IntId are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1237"><span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERRORE \_ DS \_ DUP \_ DMS \_ IntID**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1237"><span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERROR\_DS\_DUP\_MSDS\_INTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1238">8597 (0x2195)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1238">8597 (0x2195)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1239">Aggiornamento dello schema non riuscito: msDS-INtId duplicato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1239">Schema update failed: Duplicate msDS-INtId.</span></span> <span data-ttu-id="93ba9-1240">Ripetere l'operazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1240">Retry the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1241"><span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**ERRORE \_ DS \_ presente \_ in \_ RDNATTID**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1241"><span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**ERROR\_DS\_EXISTS\_IN\_RDNATTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1242">8598 (0x2196)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1242">8598 (0x2196)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1243">Eliminazione dello schema non riuscita: l'attributo viene usato in rDNAttID.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1243">Schema deletion failed: attribute is used in rDNAttID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1244"><span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERRORE \_ \_ autorizzazione DS \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1244"><span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERROR\_DS\_AUTHORIZATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1245">8599 (0x2197)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1245">8599 (0x2197)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1246">Il servizio directory non è stato in grado di autorizzare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1246">The directory service failed to authorize the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1247"><span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERRORE \_ DS \_ script non valido \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1247"><span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERROR\_DS\_INVALID\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1248">8600 (0x2198)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1248">8600 (0x2198)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1249">Il servizio directory non è in grado di elaborare lo script perché non è valido.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1249">The Directory Service cannot process the script because it is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1250"><span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**ERRORE \_ DS \_ Remote \_ CROSSREF \_ op \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1250"><span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**ERROR\_DS\_REMOTE\_CROSSREF\_OP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1251">8601 (0x2199)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1251">8601 (0x2199)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1252">Operazione di creazione incrociata remota non riuscita nell'FSMO del master per la denominazione dei domini.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1252">The remote create cross reference operation failed on the Domain Naming Master FSMO.</span></span> <span data-ttu-id="93ba9-1253">L'errore dell'operazione è nei dati estesi.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1253">The operation's error is in the extended data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1254"><span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERRORE \_ DS \_ Cross \_ ref \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1254"><span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERROR\_DS\_CROSS\_REF\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1255">8602 (0x219A)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1255">8602 (0x219A)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1256">Un riferimento incrociato è in uso localmente con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1256">A cross reference is in use locally with the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1257"><span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERRORE \_ DS \_ \_ di derivazione \_ SPN \_ per il \_ \_ dominio eliminato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1257"><span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERROR\_DS\_CANT\_DERIVE\_SPN\_FOR\_DELETED\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1258">8603 (0x219B)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1258">8603 (0x219B)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1259">DS non può derivare un nome dell'entità servizio (SPN) per l'autenticazione reciproca del server di destinazione perché il dominio del server è stato eliminato dalla foresta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1259">The DS cannot derive a service principal name (SPN) with which to mutually authenticate the target server because the server's domain has been deleted from the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1260"><span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERRORE di i/o del servizio \_ DS \_ con controller \_ \_ \_ scrivibile \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1260"><span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERROR\_DS\_CANT\_DEMOTE\_WITH\_WRITEABLE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1261">8604 (0x219C)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1261">8604 (0x219C)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1262">NCs scrivibile impedisce il controller di dominio da abbassamento.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1262">Writeable NCs prevent this DC from demoting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1263"><span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**\_ \_ ID duplicato errore DS \_ \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1263"><span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**ERROR\_DS\_DUPLICATE\_ID\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1264">8605 (0x219D)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1264">8605 (0x219D)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1265">L'oggetto richiesto non dispone di un identificatore univoco e non può essere recuperato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1265">The requested object has a non-unique identifier and cannot be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1266"><span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERRORE \_ DS \_ insufficiente \_ \_ per \_ creare l' \_ oggetto**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1266"><span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERROR\_DS\_INSUFFICIENT\_ATTR\_TO\_CREATE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1267">8606 (0x219E)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1267">8606 (0x219E)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1268">Sono stati assegnati attributi insufficienti per creare un oggetto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1268">Insufficient attributes were given to create an object.</span></span> <span data-ttu-id="93ba9-1269">Questo oggetto potrebbe non esistere perché è possibile che sia stato eliminato e che sia già stato sottoposta a Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1269">This object may not exist because it may have been deleted and already garbage collected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1270"><span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**errore \_ di \_ conversione gruppo DS \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1270"><span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**ERROR\_DS\_GROUP\_CONVERSION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1271">8607 (0x219F)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1271">8607 (0x219F)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1272">Impossibile convertire il gruppo a causa di restrizioni relative agli attributi per il tipo di gruppo richiesto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1272">The group cannot be converted due to attribute restrictions on the requested group type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1273"><span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERRORE \_ DS \_ Impossibile \_ spostare \_ il \_ gruppo di base dell'app \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1273"><span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERROR\_DS\_CANT\_MOVE\_APP\_BASIC\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1274">8608 (0x21A0)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1274">8608 (0x21A0)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1275">Lo spostamento tra domini di gruppi di applicazioni di base non vuoti non è consentito.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1275">Cross-domain move of non-empty basic application groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1276"><span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERRORE \_ DS \_ Impossibile \_ spostare \_ il \_ gruppo di query dell'app \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1276"><span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERROR\_DS\_CANT\_MOVE\_APP\_QUERY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1277">8609 (0x21A1)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1277">8609 (0x21A1)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1278">Lo spostamento tra domini di gruppi di applicazioni basati su query non vuote non è consentito.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1278">Cross-domain move of non-empty query based application groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1279"><span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**ERRORE \_ \_ ruolo DS \_ non \_ verificato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1279"><span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**ERROR\_DS\_ROLE\_NOT\_VERIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1280">8610 (0x21A2)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1280">8610 (0x21A2)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1281">Impossibile verificare la proprietà del ruolo FSMO perché la relativa partizione di directory non è stata replicata correttamente con almeno un partner di replica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1281">The FSMO role ownership could not be verified because its directory partition has not replicated successfully with at least one replication partner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1282"><span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**ERRORE \_ DS \_ WKO \_ Container \_ non può \_ essere \_ speciale**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1282"><span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**ERROR\_DS\_WKO\_CONTAINER\_CANNOT\_BE\_SPECIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1283">8611 (0x21A3)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1283">8611 (0x21A3)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1284">Il contenitore di destinazione per un reindirizzamento di un contenitore di oggetti noto non può essere già un contenitore speciale.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1284">The target container for a redirection of a well known object container cannot already be a special container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1285"><span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERRORE \_ \_ \_ di ridenominazione \_ del dominio DS in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1285"><span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERROR\_DS\_DOMAIN\_RENAME\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1286">8612 (0x21A4)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1286">8612 (0x21A4)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1287">Il servizio directory non è in grado di eseguire l'operazione richiesta perché è in corso un'operazione di ridenominazione del dominio.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1287">The Directory Service cannot perform the requested operation because a domain rename operation is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1288"><span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERRORE \_ DS esistente del controller di dominio \_ \_ ad \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1288"><span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERROR\_DS\_EXISTING\_AD\_CHILD\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1289">8613 (0x21A5)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1289">8613 (0x21A5)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1290">Il servizio directory ha rilevato una partizione figlio al di sotto del nome della partizione richiesta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1290">The directory service detected a child partition below the requested partition name.</span></span> <span data-ttu-id="93ba9-1291">La gerarchia della partizione deve essere creata in un metodo di primo piano.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1291">The partition hierarchy must be created in a top down method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1292"><span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**\_ \_ \_ superamento della durata del REPL DS \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1292"><span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**ERROR\_DS\_REPL\_LIFETIME\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1293">8614 (0x21A6)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1293">8614 (0x21A6)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1294">Il servizio directory non è in grado di eseguire la replica con questo server perché il tempo trascorso dall'ultima replica con il server ha superato la durata dell'oggetto contrassegnato per la rimozione definitiva.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1294">The directory service cannot replicate with this server because the time since the last replication with this server has exceeded the tombstone lifetime.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1295"><span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERRORE \_ DS non \_ consentito \_ nel \_ contenitore di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1295"><span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERROR\_DS\_DISALLOWED\_IN\_SYSTEM\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1296">8615 (0x21A7)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1296">8615 (0x21A7)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1297">L'operazione richiesta non è consentita su un oggetto nel contenitore System.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1297">The requested operation is not allowed on an object under the system container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1298"><span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERRORE \_ \_ coda di invio LDAP di DS con errore \_ \_ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1298"><span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERROR\_DS\_LDAP\_SEND\_QUEUE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1299">8616 (0x21A8)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1299">8616 (0x21A8)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1300">La coda di invio della rete dei server LDAP è stata riempita perché il client non elabora i risultati delle richieste in modo sufficientemente veloce.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1300">The LDAP servers network send queue has filled up because the client is not processing the results of its requests fast enough.</span></span> <span data-ttu-id="93ba9-1301">Non verranno elaborate altre richieste finché il client non viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1301">No more requests will be processed until the client catches up.</span></span> <span data-ttu-id="93ba9-1302">Se il client non viene aggiornato, verrà disconnesso.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1302">If the client does not catch up then it will be disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1303"><span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**\_finestra di \_ \_ \_ pianificazione \_ del servizio DRA di errore DS**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1303"><span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**ERROR\_DS\_DRA\_OUT\_SCHEDULE\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1304">8617 (0x21A9)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1304">8617 (0x21A9)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1305">La replica pianificata non è stata eseguita perché il sistema era troppo occupato per eseguire la richiesta entro la finestra di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1305">The scheduled replication did not take place because the system was too busy to execute the request within the schedule window.</span></span> <span data-ttu-id="93ba9-1306">La coda di replica è in overload.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1306">The replication queue is overloaded.</span></span> <span data-ttu-id="93ba9-1307">Provare a ridurre il numero di partner o a diminuire la frequenza di replica pianificata.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1307">Consider reducing the number of partners or decreasing the scheduled replication frequency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1308"><span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**criterio di errore \_ DS \_ \_ non \_ noto**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1308"><span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**ERROR\_DS\_POLICY\_NOT\_KNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1309">8618 (0x21AA)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1309">8618 (0x21AA)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1310">Al momento non è possibile determinare se il criterio di replica del ramo è disponibile nel controller di dominio dell'hub.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1310">At this time, it cannot be determined if the branch replication policy is available on the hub domain controller.</span></span> <span data-ttu-id="93ba9-1311">Riprovare in un secondo momento per tenere conto delle latenze di replica.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1311">Please retry at a later time to account for replication latencies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1312"><span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERRORE \_ nessun \_ \_ oggetto impostazioni \_ sito**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1312"><span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERROR\_NO\_SITE\_SETTINGS\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1313">8619 (0x21AB)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1313">8619 (0x21AB)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1314">L'oggetto Impostazioni sito per il sito specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1314">The site settings object for the specified site does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1315"><span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERRORE \_ nessun \_ segreto**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1315"><span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERROR\_NO\_SECRETS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1316">8620 (0x21AC)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1316">8620 (0x21AC)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1317">L'archivio account locale non contiene il materiale segreto per l'account specificato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1317">The local account store does not contain secret material for the specified account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1318"><span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERRORE \_ non è stato trovato alcun controller di dominio \_ scrivibile \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1318"><span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERROR\_NO\_WRITABLE\_DC\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1319">8621 (0x21AD)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1319">8621 (0x21AD)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1320">Impossibile trovare un controller di dominio scrivibile nel dominio.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1320">Could not find a writable domain controller in the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1321"><span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERRORE \_ DS \_ nessun \_ \_ oggetto server**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1321"><span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERROR\_DS\_NO\_SERVER\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1322">8622 (0x21AE)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1322">8622 (0x21AE)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1323">L'oggetto server per il controller di dominio non esiste.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1323">The server object for the domain controller does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1324"><span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERRORE \_ DS \_ nessun \_ oggetto NTDSA \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1324"><span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERROR\_DS\_NO\_NTDSA\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1325">8623 (0x21AF)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1325">8623 (0x21AF)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1326">L'oggetto Impostazioni NTDS per il controller di dominio non esiste.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1326">The NTDS Settings object for the domain controller does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1327"><span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERRORE \_ DS \_ \_ ricerca non ASQ \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1327"><span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERROR\_DS\_NON\_ASQ\_SEARCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1328">8624 (0x21B0)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1328">8624 (0x21B0)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1329">L'operazione di ricerca richiesta non è supportata per le ricerche ASQ.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1329">The requested search operation is not supported for ASQ searches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1330"><span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**errore \_ di \_ controllo DS errore \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1330"><span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**ERROR\_DS\_AUDIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1331">8625 (0x21B1)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1331">8625 (0x21B1)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1332">Non è stato possibile generare un evento di controllo obbligatorio per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1332">A required audit event could not be generated for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1333"><span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERRORE \_ DS \_ - \_ \_ sottoalbero del flag di ricerca non valido \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1333"><span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG\_SUBTREE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1334">8626 (0x21B2)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1334">8626 (0x21B2)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1335">I flag di ricerca per l'attributo non sono validi.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1335">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="93ba9-1336">Il bit dell'indice del sottoalbero è valido solo per gli attributi a valore singolo.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1336">The subtree index bit is valid only on single valued attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1337"><span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERRORE \_ DS \_ \_ \_ tupla flag di ricerca non valido \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1337"><span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG\_TUPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1338">8627 (0x21B3)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1338">8627 (0x21B3)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1339">I flag di ricerca per l'attributo non sono validi.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1339">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="93ba9-1340">Il bit dell'indice tupla è valido solo per gli attributi delle stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1340">The tuple index bit is valid only on attributes of Unicode strings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1341"><span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERRORE \_ di \_ tabella gerarchia DS \_ \_ troppo \_ profonda**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1341"><span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERROR\_DS\_HIERARCHY\_TABLE\_TOO\_DEEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1342">8628 (0x21B4)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1342">8628 (0x21B4)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1343">Le rubriche sono troppo profondamente nidificate.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1343">The address books are nested too deeply.</span></span> <span data-ttu-id="93ba9-1344">Impossibile compilare la tabella della gerarchia.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1344">Failed to build the hierarchy table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1345"><span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERRORE \_ DS \_ DRA \_ danneggiato \_ \_ vettoriale**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1345"><span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERROR\_DS\_DRA\_CORRUPT\_UTD\_VECTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1346">8629 (0x21B5)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1346">8629 (0x21B5)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1347">Il vettore di nesso aggiornato specificato è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1347">The specified up-to-date-ness vector is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1348"><span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERRORI \_ \_ segreti DRA di DS \_ \_ negati**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1348"><span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERROR\_DS\_DRA\_SECRETS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1349">8630 (0x21B6)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1349">8630 (0x21B6)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1350">La richiesta di replica dei segreti è stata negata.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1350">The request to replicate secrets is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1351"><span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**\_ \_ \_ ID MAPI riservato DS \_ errore**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1351"><span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**ERROR\_DS\_RESERVED\_MAPI\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1352">8631 (0x21B7)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1352">8631 (0x21B7)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1353">Aggiornamento dello schema non riuscito: l'identificatore MAPI è riservato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1353">Schema update failed: The MAPI identifier is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1354"><span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERRORE \_ \_ ID MAPI \_ DS \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1354"><span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERROR\_DS\_MAPI\_ID\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1355">8632 (0x21B8)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1355">8632 (0x21B8)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1356">Aggiornamento dello schema non riuscito: non sono disponibili identificatori MAPI.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1356">Schema update failed: There are no MAPI identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1357"><span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERRORE del servizio di \_ dominio di \_ \_ \_ krbtgt mancante \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1357"><span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERROR\_DS\_DRA\_MISSING\_KRBTGT\_SECRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1358">8633 (0x21B9)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1358">8633 (0x21B9)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1359">L'operazione di replica non è riuscita perché mancano gli attributi obbligatori dell'oggetto krbtgt locale.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1359">The replication operation failed because the required attributes of the local krbtgt object are missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1360"><span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERRORE \_ \_ nome dominio \_ DS \_ esistente \_ nella \_ foresta**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1360"><span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERROR\_DS\_DOMAIN\_NAME\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1361">8634 (0x21BA)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1361">8634 (0x21BA)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1362">Il nome di dominio del dominio trusted esiste già nella foresta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1362">The domain name of the trusted domain already exists in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1363"><span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERRORE \_ \_ nome flat \_ DS \_ esistente \_ nella \_ foresta**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1363"><span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERROR\_DS\_FLAT\_NAME\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1364">8635 (0x21BB)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1364">8635 (0x21BB)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1365">Il nome flat del dominio trusted esiste già nella foresta.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1365">The flat name of the trusted domain already exists in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1366"><span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**ERRORE \_ \_ \_ nome entità utente non valido \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1366"><span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**ERROR\_INVALID\_USER\_PRINCIPAL\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1367">8636 (0x21BC)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1367">8636 (0x21BC)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1368">Il nome dell'entità utente (UPN) non è valido.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1368">The User Principal Name (UPN) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1369"><span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERRORE \_ del \_ \_ gruppo mappato OID di DS con \_ \_ \_ \_ membri**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1369"><span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERROR\_DS\_OID\_MAPPED\_GROUP\_CANT\_HAVE\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1370">8637 (0x21BD)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1370">8637 (0x21BD)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1371">I gruppi con mapping OID non possono avere membri.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1371">OID mapped groups cannot have members.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1372"><span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERRORE \_ DS \_ DS \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1372"><span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERROR\_DS\_OID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1373">8638 (0x21BE)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1373">8638 (0x21BE)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1374">L'OID specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1374">The specified OID cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1375"><span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERRORE \_ DS servizio di \_ \_ destinazione riciclata \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1375"><span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERROR\_DS\_DRA\_RECYCLED\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1376">8639 (0x21BF)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1376">8639 (0x21BF)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1377">L'operazione di replica non è riuscita perché l'oggetto di destinazione a cui fa riferimento un valore di collegamento viene riciclato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1377">The replication operation failed because the target object referred by a link value is recycled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1378"><span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERRORE \_ DS non \_ consentito di \_ \_ Reindirizzamento del controller di dominio**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1378"><span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERROR\_DS\_DISALLOWED\_NC\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1379">8640 (0x21C0)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1379">8640 (0x21C0)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1380">L'operazione di reindirizzamento non è riuscita perché l'oggetto di destinazione si trova in un NC diverso da quello del controller di dominio corrente.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1380">The redirect operation failed because the target object is in a NC different from the domain NC of the current domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1381"><span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERRORE \_ DS \_ High \_ ADLDS \_ FFL**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1381"><span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERROR\_DS\_HIGH\_ADLDS\_FFL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1382">8641 (0x21C1)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1382">8641 (0x21C1)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1383">Non è possibile ridurre il livello di funzionalità del set di configurazione AD LDS al valore richiesto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1383">The functional level of the AD LDS configuration set cannot be lowered to the requested value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1384"><span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERRORE \_ DS \_ High \_ DSA \_ Version**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1384"><span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERROR\_DS\_HIGH\_DSA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1385">8642 (0x21C2)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1385">8642 (0x21C2)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1386">Il livello di funzionalità del dominio (o della foresta) non può essere abbassato al valore richiesto.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1386">The functional level of the domain (or forest) cannot be lowered to the requested value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1387"><span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERRORE \_ DS \_ low \_ ADLDS \_ FFL**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1387"><span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERROR\_DS\_LOW\_ADLDS\_FFL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1388">8643 (0x21C3)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1388">8643 (0x21C3)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1389">Non è possibile aumentare il livello di funzionalità del set di configurazione AD LDS al valore richiesto, perché esistono una o più istanze di ADLDS con un livello di funzionalità non compatibile più basso.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1389">The functional level of the AD LDS configuration set cannot be raised to the requested value, because there exist one or more ADLDS instances that are at a lower incompatible functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1390"><span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**\_ \_ SID del dominio \_ di errore uguale alla \_ \_ \_ workstation locale**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1390"><span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**ERROR\_DOMAIN\_SID\_SAME\_AS\_LOCAL\_WORKSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1391">8644 (0x21C4)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1391">8644 (0x21C4)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1392">Non è possibile completare l'aggiunta al dominio perché il SID del dominio a cui si è tentato di aggiungere è identico al SID di questo computer.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1392">The domain join cannot be completed because the SID of the domain you attempted to join was identical to the SID of this machine.</span></span> <span data-ttu-id="93ba9-1393">Si tratta di un sintomo di un'installazione del sistema operativo clonata in modo errato.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1393">This is a symptom of an improperly cloned operating system install.</span></span> <span data-ttu-id="93ba9-1394">Eseguire Sysprep sul computer per generare un nuovo SID del computer.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1394">You should run sysprep on this machine in order to generate a new machine SID.</span></span> <span data-ttu-id="93ba9-1395">Per altre informazioni, vedere <https://go.microsoft.com/fwlink/p/?linkid=168895>.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1395">Please see <https://go.microsoft.com/fwlink/p/?linkid=168895> for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1396"><span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERRORE \_ DS- \_ annullamento dell'eliminazione della \_ \_ convalida Sam \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1396"><span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERROR\_DS\_UNDELETE\_SAM\_VALIDATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1397">8645 (0x21C5)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1397">8645 (0x21C5)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1398">L'operazione di annullamento dell'eliminazione non è riuscita perché il nome dell'account SAM o il nome dell'account SAM aggiuntivo dell'oggetto da eliminare è in conflitto con un oggetto attivo esistente.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1398">The undelete operation failed because the Sam Account Name or Additional Sam Account Name of the object being undeleted conflicts with an existing live object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="93ba9-1399"><span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERRORE \_ \_ tipo di account non corretto \_**</span><span class="sxs-lookup"><span data-stu-id="93ba9-1399"><span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERROR\_INCORRECT\_ACCOUNT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ba9-1400">8646 (0x21C6)</span><span class="sxs-lookup"><span data-stu-id="93ba9-1400">8646 (0x21C6)</span></span>
</dt> <dt>



<span data-ttu-id="93ba9-1401">Il sistema non è autorevole per l'account specificato e pertanto non può completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1401">The system is not authoritative for the specified account and therefore cannot complete the operation.</span></span> <span data-ttu-id="93ba9-1402">Ripetere l'operazione usando il provider associato a questo account.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1402">Please retry the operation using the provider associated with this account.</span></span> <span data-ttu-id="93ba9-1403">Se si tratta di un provider online, utilizzare il sito online del provider.</span><span class="sxs-lookup"><span data-stu-id="93ba9-1403">If this is an online provider please use the provider's online site.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="93ba9-1404">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93ba9-1404">Requirements</span></span>



| <span data-ttu-id="93ba9-1405">Requisito</span><span class="sxs-lookup"><span data-stu-id="93ba9-1405">Requirement</span></span> | <span data-ttu-id="93ba9-1406">Valore</span><span class="sxs-lookup"><span data-stu-id="93ba9-1406">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93ba9-1407">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93ba9-1407">Minimum supported client</span></span><br/> | <span data-ttu-id="93ba9-1408">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="93ba9-1408">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="93ba9-1409">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93ba9-1409">Minimum supported server</span></span><br/> | <span data-ttu-id="93ba9-1410">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="93ba9-1410">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="93ba9-1411">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93ba9-1411">Header</span></span><br/>                   | <dl> <span data-ttu-id="93ba9-1412"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="93ba9-1412"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93ba9-1413">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93ba9-1413">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ba9-1414">Codici di errore di sistema</span><span class="sxs-lookup"><span data-stu-id="93ba9-1414">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




