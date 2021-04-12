---
title: Servizi Desktop remoto codici di errore del provider WMI (Wbemcli. h)
description: Errori restituiti dal provider WMI Servizi Desktop remoto. Per un elenco di altri errori WMI, vedere costanti di errore WMI.
ms.assetid: 1e68c41d-f321-4bc5-ba30-b69f5ba741eb
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WBEM_E_FAILED
- WBEM_E_NOT_FOUND
- WBEM_E_PROVIDER_FAILURE
- WBEM_E_TYPE_MISMATCH
- WBEM_E_OUT_OF_MEMORY
- WBEM_E_INVALID_PARAMETER
- WBEM_E_NOT_AVAILABLE
- WBEM_E_NOT_SUPPORTED
- WBEM_E_INVALID_NAMESPACE
- WBEM_E_INVALID_OBJECT
- WBEM_E_INITIALIZATION_FAILURE
- WBEM_E_INVALID_OPERATION
- WBEM_E_INVALID_QUERY
- WBEM_E_INVALID_QUERY_TYPE
- WBEM_E_ALREADY_EXISTS
- WBEM_E_INVALID_SYNTAX
- WBEM_E_READ_ONLY
- WBEM_E_PROVIDER_NOT_CAPABLE
- WBEM_E_ILLEGAL_NULL
- WBEM_E_VALUE_OUT_OF_RANGE
- WBEM_E_INVALID_METHOD
- WBEM_E_INVALID_METHOD_PARAMETERS
- WBEM_E_INVALID_OBJECT_PATH
api_location:
- Wbemcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252015a5d80a1487033ad285ce3080f4d666f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518988"
---
# <a name="remote-desktop-services-wmi-provider-error-codes"></a><span data-ttu-id="948d6-104">Servizi Desktop remoto codici di errore del provider WMI</span><span class="sxs-lookup"><span data-stu-id="948d6-104">Remote Desktop Services WMI provider error codes</span></span>

<span data-ttu-id="948d6-105">Nell'elenco seguente sono elencati gli errori WMI restituiti dal provider WMI Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="948d6-105">The following list lists the WMI errors returned by the Remote Desktop Services WMI provider.</span></span> <span data-ttu-id="948d6-106">Per un elenco di altri errori WMI, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="948d6-106">For a list of other WMI errors, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="948d6-107"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM \_ E \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="948d6-107"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM\_E\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-108">2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="948d6-108">2147749889 (0x80041001)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-109">La chiamata al metodo non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="948d6-109">The method call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-110"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="948d6-110"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-111">2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="948d6-111">2147749890 (0x80041002)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-112">Impossibile trovare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="948d6-112">The object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-113"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**\_errore del \_ provider WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="948d6-113"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM\_E\_PROVIDER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-114">2147749892 (0x80041004)</span><span class="sxs-lookup"><span data-stu-id="948d6-114">2147749892 (0x80041004)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-115">Il provider ha avuto esito negativo in un momento diverso dall'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="948d6-115">The provider has failed at some time other than during initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-116"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**\_tipo WBEM E non \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="948d6-116"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-117">2147749893 (0x80041005)</span><span class="sxs-lookup"><span data-stu-id="948d6-117">2147749893 (0x80041005)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-118">Si è verificata una mancata corrispondenza del tipo.</span><span class="sxs-lookup"><span data-stu-id="948d6-118">A type mismatch has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-119"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM \_ E \_ \_ \_ memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="948d6-119"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM\_E\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-120">2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="948d6-120">2147749894 (0x80041006)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-121">Memoria insufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="948d6-121">There was not enough memory for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-122"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_parametro WBEM E \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="948d6-122"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-123">2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="948d6-123">2147749896 (0x80041008)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-124">Uno dei parametri della chiamata non è corretto.</span><span class="sxs-lookup"><span data-stu-id="948d6-124">One of the parameters to the call is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-125"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="948d6-125"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM\_E\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-126">2147749897 (0x80041009)</span><span class="sxs-lookup"><span data-stu-id="948d6-126">2147749897 (0x80041009)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-127">La risorsa, tipicamente un server remoto, non è attualmente disponibile.</span><span class="sxs-lookup"><span data-stu-id="948d6-127">The resource, typically a remote server, is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-128"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="948d6-128"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM\_E\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-129">2147749900 (0x8004100C)</span><span class="sxs-lookup"><span data-stu-id="948d6-129">2147749900 (0x8004100C)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-130">La funzionalità o l'operazione non è supportata.</span><span class="sxs-lookup"><span data-stu-id="948d6-130">The feature or operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-131"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**\_ \_ spazio dei nomi WBEM E non valido \_**</span><span class="sxs-lookup"><span data-stu-id="948d6-131"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM\_E\_INVALID\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-132">2147749902 (0x8004100E)</span><span class="sxs-lookup"><span data-stu-id="948d6-132">2147749902 (0x8004100E)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-133">Impossibile trovare lo spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="948d6-133">The specified namespace could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-134"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**\_oggetto WBEM E \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="948d6-134"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-135">2147749903 (0x8004100F)</span><span class="sxs-lookup"><span data-stu-id="948d6-135">2147749903 (0x8004100F)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-136">L'istanza specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="948d6-136">The specified instance is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-137"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_errore di \_ inizializzazione WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="948d6-137"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM\_E\_INITIALIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-138">2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="948d6-138">2147749908 (0x80041014)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-139">Non è stato possibile inizializzare un modulo, ad esempio un provider, per motivi interni.</span><span class="sxs-lookup"><span data-stu-id="948d6-139">A module, such as a provider, failed to initialize for internal reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-140"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_operazione WBEM E \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="948d6-140"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM\_E\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-141">2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="948d6-141">2147749910 (0x80041016)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-142">Il tipo di operazione richiesta non è valido.</span><span class="sxs-lookup"><span data-stu-id="948d6-142">The requested operation is not valid.</span></span> <span data-ttu-id="948d6-143">Questo errore si applica generalmente a tentativi non validi di eliminare classi o proprietà.</span><span class="sxs-lookup"><span data-stu-id="948d6-143">This error usually applies to invalid attempts to delete classes or properties.</span></span> <span data-ttu-id="948d6-144">Questo errore viene restituito quando si tenta di modificare una proprietà di sostituzione del server tramite il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="948d6-144">This error is returned on an attempt to modify a server-override property through group policy control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-145"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_query WBEM E \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="948d6-145"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM\_E\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-146">2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="948d6-146">2147749911 (0x80041017)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-147">La sintassi della query non è valida.</span><span class="sxs-lookup"><span data-stu-id="948d6-147">The query was not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-148"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_tipo di query WBEM E \_ non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="948d6-148"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM\_E\_INVALID\_QUERY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-149">2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="948d6-149">2147749912 (0x80041018)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-150">Il linguaggio della query richiesta non è supportato.</span><span class="sxs-lookup"><span data-stu-id="948d6-150">The requested query language is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-151"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="948d6-151"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-152">2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="948d6-152">2147749913 (0x80041019)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-153">In un'operazione Put è stato specificato il flag **wbemChangeFlagCreateOnly** , ma l'istanza esiste già.</span><span class="sxs-lookup"><span data-stu-id="948d6-153">In a put operation, the **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-154"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_sintassi WBEM E \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="948d6-154"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM\_E\_INVALID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-155">2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="948d6-155">2147749921 (0x80041021)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-156">La query non è sintatticamente valida.</span><span class="sxs-lookup"><span data-stu-id="948d6-156">Query is not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-157"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ sola lettura \_**</span><span class="sxs-lookup"><span data-stu-id="948d6-157"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM\_E\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-158">2147749923 (0x80041023)</span><span class="sxs-lookup"><span data-stu-id="948d6-158">2147749923 (0x80041023)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-159">La proprietà che si tenta di modificare è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="948d6-159">The property that you are attempting to modify is read-only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-160"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**il \_ provider WBEM E \_ \_ non è \_ in grado di supportare**</span><span class="sxs-lookup"><span data-stu-id="948d6-160"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM\_E\_PROVIDER\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-161">2147749924 (0x80041024)</span><span class="sxs-lookup"><span data-stu-id="948d6-161">2147749924 (0x80041024)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-162">Il provider non è in grado di eseguire l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="948d6-162">The provider cannot perform the requested operation.</span></span> <span data-ttu-id="948d6-163">L'operazione potrebbe includere una query troppo complessa, il recupero di un'istanza, la creazione di una classe, l'aggiornamento di una classe, l'eliminazione di una classe o l'enumerazione di una classe.</span><span class="sxs-lookup"><span data-stu-id="948d6-163">The operation could include a query that is too complex, retrieving an instance, creating a class, updating a class, deleting a class, or enumerating a class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-164"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ null non valido \_**</span><span class="sxs-lookup"><span data-stu-id="948d6-164"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM\_E\_ILLEGAL\_NULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-165">2147749928 (0x80041028)</span><span class="sxs-lookup"><span data-stu-id="948d6-165">2147749928 (0x80041028)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-166">Non è stato specificato **alcun** valore / **null** per una proprietà che non può essere  / **null**, ad esempio una chiave contrassegnata da un qualificatore di [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**indicizzato**](/windows/desktop/WmiSdk/optional-qualifiers)o [**Not \_ null**](/windows/desktop/WmiSdk/optional-qualifiers) .</span><span class="sxs-lookup"><span data-stu-id="948d6-166">A value of **Nothing**/**NULL** was specified for a property that cannot be **Nothing**/**NULL**, such as one that is marked by a [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Indexed**](/windows/desktop/WmiSdk/optional-qualifiers), or [**Not\_Null**](/windows/desktop/WmiSdk/optional-qualifiers) qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-167"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_valore WBEM E non compreso nell' \_ \_ \_ \_ intervallo**</span><span class="sxs-lookup"><span data-stu-id="948d6-167"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM\_E\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-168">2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="948d6-168">2147749931 (0x8004102B)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-169">La richiesta è stata eseguita con un valore esterno all'intervallo o è incompatibile con il tipo.</span><span class="sxs-lookup"><span data-stu-id="948d6-169">The request was made with an out-of-range value, or is incompatible with the type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-170"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ metodo non valido \_**</span><span class="sxs-lookup"><span data-stu-id="948d6-170"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM\_E\_INVALID\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-171">2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="948d6-171">2147749934 (0x8004102E)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-172">Il metodo richiesto non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="948d6-172">The requested method is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-173"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_parametri del metodo WBEM E \_ non validi \_ \_**</span><span class="sxs-lookup"><span data-stu-id="948d6-173"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM\_E\_INVALID\_METHOD\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-174">2147749935 (0x8004102F)</span><span class="sxs-lookup"><span data-stu-id="948d6-174">2147749935 (0x8004102F)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-175">I parametri forniti per il metodo non sono validi.</span><span class="sxs-lookup"><span data-stu-id="948d6-175">The parameters provided for the method are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="948d6-176"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**\_percorso dell'oggetto WBEM E \_ non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="948d6-176"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM\_E\_INVALID\_OBJECT\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d6-177">2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="948d6-177">2147749946 (0x8004103A)</span></span>
</dt> <dt>



<span data-ttu-id="948d6-178">Il percorso dell'oggetto specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="948d6-178">The specified object path was not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="948d6-179">Requisiti</span><span class="sxs-lookup"><span data-stu-id="948d6-179">Requirements</span></span>



| <span data-ttu-id="948d6-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="948d6-180">Requirement</span></span> | <span data-ttu-id="948d6-181">Valore</span><span class="sxs-lookup"><span data-stu-id="948d6-181">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="948d6-182">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="948d6-182">Minimum supported client</span></span><br/> | <span data-ttu-id="948d6-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="948d6-183">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="948d6-184">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="948d6-184">Minimum supported server</span></span><br/> | <span data-ttu-id="948d6-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="948d6-185">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="948d6-186">Intestazione</span><span class="sxs-lookup"><span data-stu-id="948d6-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="948d6-187"><dt>Wbemcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="948d6-187"><dt>Wbemcli.h</dt></span></span> </dl> |



 

