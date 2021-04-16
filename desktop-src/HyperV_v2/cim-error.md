---
description: La \_ classe di errore CIM contiene informazioni sull'errore di un'operazione CIM.
ms.assetid: 35acecbd-b972-45b4-9616-2047bba8fd41
title: Classe CIM_Error
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Error
- CIM_Error.ErrorType
- CIM_Error.OtherErrorType
- CIM_Error.OwningEntity
- CIM_Error.MessageID
- CIM_Error.Message
- CIM_Error.MessageArguments
- CIM_Error.PerceivedSeverity
- CIM_Error.ProbableCause
- CIM_Error.ProbableCauseDescription
- CIM_Error.RecommendedActions
- CIM_Error.ErrorSource
- CIM_Error.ErrorSourceFormat
- CIM_Error.OtherErrorSourceFormat
- CIM_Error.CIMStatusCode
- CIM_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59ae2527478235c14a8f856319178afe00c02a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342646"
---
# <a name="cim_error-class"></a><span data-ttu-id="6a3e7-103">\_Classe Error CIM</span><span class="sxs-lookup"><span data-stu-id="6a3e7-103">CIM\_Error class</span></span>

<span data-ttu-id="6a3e7-104">La classe di **\_ errore CIM** contiene informazioni sull'errore di un'operazione CIM.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-104">The **CIM\_Error** class contains information about the failure of a CIM operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a3e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a3e7-105">Syntax</span></span>

``` syntax
[Indication, Abstract, Version("2.22.1"), Exception, UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_Error
{
  uint16 ErrorType;
  string OtherErrorType;
  string OwningEntity;
  string MessageID;
  string Message;
  string MessageArguments[];
  uint16 PerceivedSeverity;
  uint16 ProbableCause;
  string ProbableCauseDescription;
  string RecommendedActions[];
  string ErrorSource;
  uint16 ErrorSourceFormat = 0;
  string OtherErrorSourceFormat;
  uint32 CIMStatusCode;
  string CIMStatusCodeDescription;
};
```

## <a name="members"></a><span data-ttu-id="6a3e7-106">Members</span><span class="sxs-lookup"><span data-stu-id="6a3e7-106">Members</span></span>

<span data-ttu-id="6a3e7-107">La classe di **\_ errore CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6a3e7-107">The **CIM\_Error** class has these types of members:</span></span>

-   [<span data-ttu-id="6a3e7-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6a3e7-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6a3e7-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6a3e7-109">Properties</span></span>

<span data-ttu-id="6a3e7-110">La classe di **\_ errore CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-110">The **CIM\_Error** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6a3e7-111">**CIMStatusCode**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-111">**CIMStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a3e7-112">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a3e7-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-114">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. \|errore DMTF. CODICE \| 2,3 "," DSP0200. DMTF \| CIMError \| 1,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ errore CIM**.**CIMStatusCodeDescription**")</span><span class="sxs-lookup"><span data-stu-id="6a3e7-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201.DMTF\|ERROR.CODE\|2.3", "DSP0200.DMTF\|CIMError\|1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**CIMStatusCodeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="6a3e7-115">Codice di stato CIM che caratterizza questa istanza.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-115">The CIM status code that characterizes this instance.</span></span> <span data-ttu-id="6a3e7-116">Questa proprietà definisce i codici di stato che possono essere restituiti da un listener o un server CIM.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-116">This property defines the status codes that can be return by a CIM server or listener.</span></span>

<dt>

<span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>

<span data-ttu-id="6a3e7-117"><span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM \_ ERRORE \_ errore** (1)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-117"><span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM\_ERR\_FAILED** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-118">Si è verificato un errore generale che non è coperto da un codice di errore più specifico.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-118">A general error occurred that is not covered by a more specific error code.</span></span>

</dd> <dt>

<span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>

<span data-ttu-id="6a3e7-119"><span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM \_ ERRORE di \_ accesso \_ negato** (2)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-119"><span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM\_ERR\_ACCESS\_DENIED** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-120">L'accesso a una risorsa CIM non è disponibile per il client.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-120">Access to a CIM resource was not available to the client.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>

<span data-ttu-id="6a3e7-121"><span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM \_ \_ \_ Spazio dei nomi non valido** (3)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-121"><span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM\_ERR\_INVALID\_NAMESPACE** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-122">Lo spazio dei nomi di destinazione non esiste.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-122">The target namespace does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>

<span data-ttu-id="6a3e7-123"><span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM \_ \_ \_ Parametro Err non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-123"><span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM\_ERR\_INVALID\_PARAMETER** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-124">Uno o più valori di parametro passati al metodo non sono validi.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-124">One or more parameter values passed to the method were invalid.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>

<span data-ttu-id="6a3e7-125"><span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM \_ \_ \_ Classe Err non valida** (5)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-125"><span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM\_ERR\_INVALID\_CLASS** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-126">La classe specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-126">The specified Class does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>

<span data-ttu-id="6a3e7-127"><span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM \_ ERRORE \_ non \_ trovato** (6)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-127"><span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM\_ERR\_NOT\_FOUND** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-128">Impossibile trovare l'oggetto richiesto.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-128">The requested object could not be found.</span></span>

</dd> <dt>

<span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>

<span data-ttu-id="6a3e7-129"><span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM \_ ERR \_ non \_ supportato** (7)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-129"><span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM\_ERR\_NOT\_SUPPORTED** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-130">L'operazione richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-130">The requested operation is not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>

<span data-ttu-id="6a3e7-131"><span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM \_ \_Classe ERR \_ con \_ elementi figlio** (8)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-131"><span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM\_ERR\_CLASS\_HAS\_CHILDREN** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-132">Non è possibile eseguire l'operazione su questa classe perché contiene istanze.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-132">Operation cannot be carried out on this class since it has instances.</span></span>

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>

<span data-ttu-id="6a3e7-133"><span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM \_ \_Classe ERR \_ con \_ istanze** (9)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-133"><span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM\_ERR\_CLASS\_HAS\_INSTANCES** (9)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-134">Non è possibile eseguire l'operazione su questa classe perché contiene istanze.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-134">Operation cannot be carried out on this class since it has instances.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>

<span data-ttu-id="6a3e7-135"><span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM \_ \_SUPERCLASSE \_ Err non valida** (10)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-135"><span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM\_ERR\_INVALID\_SUPERCLASS** (10)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-136">Non è possibile eseguire l'operazione perché la superclasse specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-136">Operation cannot be carried out since the specified superclass does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>

<span data-ttu-id="6a3e7-137"><span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM \_ ERR \_ già \_ esistente** (11)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-137"><span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM\_ERR\_ALREADY\_EXISTS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-138">Non è possibile eseguire l'operazione perché esiste già un oggetto.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-138">Operation cannot be carried out because an object already exists.</span></span>

</dd> <dt>

<span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>

<span data-ttu-id="6a3e7-139"><span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM \_ \_Nessuna \_ \_ proprietà di questo tipo** (12)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-139"><span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM\_ERR\_NO\_SUCH\_PROPERTY** (12)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-140">La proprietà specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-140">The specified Property does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>

<span data-ttu-id="6a3e7-141"><span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM \_ \_ \_ MANCAta corrispondenza del tipo Err** (13)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-141"><span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM\_ERR\_TYPE\_MISMATCH** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-142">Il valore specificato non è compatibile con il tipo.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-142">The value supplied is incompatible with the type.</span></span>

</dd> <dt>

<span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>

<span data-ttu-id="6a3e7-143"><span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM \_ Il \_ linguaggio di query ERR \_ non è \_ \_ supportato** (14)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-143"><span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM\_ERR\_QUERY\_LANGUAGE\_NOT\_SUPPORTED** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-144">Il linguaggio di query non è riconosciuto né supportato.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-144">The query language is not recognized or supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>

<span data-ttu-id="6a3e7-145"><span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM \_ \_ \_ Query Err non valida** (15)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-145"><span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM\_ERR\_INVALID\_QUERY** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-146">La query non è valida per il linguaggio di query specificato.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-146">The query is not valid for the specified query language.</span></span>

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>

<span data-ttu-id="6a3e7-147"><span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM \_ \_Metodo ERR \_ non \_ disponibile** (16)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-147"><span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM\_ERR\_METHOD\_NOT\_AVAILABLE** (16)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-148">Impossibile eseguire il metodo estrinseco.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-148">The extrinsic Method could not be executed.</span></span>

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>

<span data-ttu-id="6a3e7-149"><span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM \_ \_Metodo ERR \_ non \_ trovato** (17)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-149"><span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM\_ERR\_METHOD\_NOT\_FOUND** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-150">Il metodo estrinseco specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-150">The specified extrinsic Method does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>

<span data-ttu-id="6a3e7-151"><span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM \_ \_ \_ Risposta imprevista Err** (18)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-151"><span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM\_ERR\_UNEXPECTED\_RESPONSE** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-152">La risposta restituita all'operazione asincrona non era prevista.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-152">The returned response to the asynchronous operation was not expected.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>

<span data-ttu-id="6a3e7-153"><span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM \_ \_ \_ \_ Destinazione risposta ERR non valida** (19)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-153"><span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM\_ERR\_INVALID\_RESPONSE\_DESTINATION** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-154">La destinazione specificata per la risposta asincrona non è valida.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-154">The specified destination for the asynchronous response is not valid.</span></span>

</dd> <dt>

<span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>

<span data-ttu-id="6a3e7-155"><span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM \_ \_Spazio dei nomi ERR \_ non \_ vuoto** (20)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-155"><span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM\_ERR\_NAMESPACE\_NOT\_EMPTY** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-156">Lo spazio dei nomi specificato non è vuoto.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-156">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>

<span data-ttu-id="6a3e7-157"><span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM \_ ERRORE \_ nel \_ \_ contesto di enumerazione non valido** (21)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-157"><span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM\_ERR\_INVALID\_ENUMERATION\_CONTEXT** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-158">Il contesto di enumerazione specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-158">The enumeration context supplied is not valid.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>

<span data-ttu-id="6a3e7-159"><span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM \_ ERRORE \_ di \_ \_ timeout operazione non valida** (22)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-159"><span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM\_ERR\_INVALID\_OPERATION\_TIMEOUT** (22)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-160">Lo spazio dei nomi specificato non è vuoto.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-160">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>

<span data-ttu-id="6a3e7-161"><span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM \_ Il \_ pull ERR \_ è \_ stato \_ abbandonato** (23)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-161"><span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM\_ERR\_PULL\_HAS\_BEEN\_ABANDONED** (23)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-162">Lo spazio dei nomi specificato non è vuoto.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-162">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>

<span data-ttu-id="6a3e7-163"><span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM \_ \_ \_ Non è possibile \_ \_ abbandonare Err pull** (24)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-163"><span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM\_ERR\_PULL\_CANNOT\_BE\_ABANDONED** (24)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-164">Il tentativo di abbandonare un'operazione pull non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-164">The attempt to abandon a pull operation has failed.</span></span>

</dd> <dt>

<span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>

<span data-ttu-id="6a3e7-165"><span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM \_ L' \_ enumerazione filtrata ERR \_ \_ non è \_ supportata** (25)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-165"><span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM\_ERR\_FILTERED\_ENUMERATION\_NOT\_SUPPORTED** (25)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-166">Enumeratrions filtrati non supportati.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-166">Filtered Enumeratrions are not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>

<span data-ttu-id="6a3e7-167"><span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM \_ \_Continuazione ERR \_ su \_ errore \_ non \_ supportata** (26)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-167"><span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM\_ERR\_CONTINUATION\_ON\_ERROR\_NOT\_SUPPORTED** (26)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-168">Continua in un errore non supportato.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-168">Continue on error is not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>

<span data-ttu-id="6a3e7-169"><span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM \_ \_ \_ \_ Superamento dei limiti del server Err** (27)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-169"><span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM\_ERR\_SERVER\_LIMITS\_EXCEEDED** (27)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-170">Sono stati superati i limiti del server WBEM (ad esempio memoria, connessioni,...).</span><span class="sxs-lookup"><span data-stu-id="6a3e7-170">The WBEM Server limits have been exceeded (e.g. memory, connections, ...).</span></span>

</dd> <dt>

<span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>

<span data-ttu-id="6a3e7-171"><span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM \_ \_Arresto del \_ server \_ \_ Err** (28)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-171"><span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM\_ERR\_SERVER\_IS\_SHUTTING\_DOWN** (28)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-172">È in corso l'arresto del server WBEM.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-172">The WBEM Server is shutting down.</span></span>

</dd> <dt>

<span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>

<span data-ttu-id="6a3e7-173"><span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM \_ \_Funzionalità query \_ Err \_ non \_ supportata** (29)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-173"><span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM\_ERR\_QUERY\_FEATURE\_NOT\_SUPPORTED** (29)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-174">La funzionalità di query specificata non è supportata.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-174">The specified Query Feature is not supported.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6a3e7-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6a3e7-176">**CIMStatusCodeDescription**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-176">**CIMStatusCodeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a3e7-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a3e7-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-179">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. \|errore DMTF. Descrizione \| 2,3 "," DSP0200. DMTF \| CIMError \| 1,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ errore CIM**.**CIMStatusCode**")</span><span class="sxs-lookup"><span data-stu-id="6a3e7-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201.DMTF\|ERROR.DESCRIPTION\|2.3", "DSP0200.DMTF\|CIMError\|1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**CIMStatusCode**")</span></span>
</dt> </dl>

<span data-ttu-id="6a3e7-180">Stringa in formato libero che contiene una descrizione leggibile del valore della proprietà **CIMStatusCode** .</span><span class="sxs-lookup"><span data-stu-id="6a3e7-180">A free-form string that contains a human-readable description of the **CIMStatusCode** property value.</span></span>

> [!Note]  
> <span data-ttu-id="6a3e7-181">Questa descrizione può estendersi, ma deve essere coerente con la definizione di **CIMStatusCode**.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-181">This description may extend, but must be consistent with the definition of **CIMStatusCode**.</span></span>

 

</dd> <dt>

<span data-ttu-id="6a3e7-182">**ErrorSource**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-182">**ErrorSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a3e7-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a3e7-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-185">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ errore CIM**.**ErrorSourceFormat**")</span><span class="sxs-lookup"><span data-stu-id="6a3e7-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="6a3e7-186">Informazioni che identificano l'entità che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-186">Information that identifies the entity that generated the error.</span></span> <span data-ttu-id="6a3e7-187">Se l'entità è modellata dallo schema CIM, questa proprietà contiene il percorso dell'istanza codificata come parametro di stringa.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-187">If the entity is modeled by the CIM Schema, this property contains the path to the instance encoded as a string parameter.</span></span> <span data-ttu-id="6a3e7-188">In caso contrario, la proprietà contiene una stringa che assegna un nome all'entità che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-188">Otherwise, the property contains a string that names the entity that generated the error.</span></span> <span data-ttu-id="6a3e7-189">Il formato di questa proprietà è specificato dalla proprietà **ErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="6a3e7-189">The format of this property is specified by the **ErrorSourceFormat** property.</span></span>

</dd> <dt>

<span data-ttu-id="6a3e7-190">**ErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-190">**ErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a3e7-191">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a3e7-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-193">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ errore CIM**.**ErrorSource**","**\_ errore CIM**.**OtherErrorSourceFormat**")</span><span class="sxs-lookup"><span data-stu-id="6a3e7-193">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSource**", "**CIM\_Error**.**OtherErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="6a3e7-194">Formato della proprietà **ErrorSource** .</span><span class="sxs-lookup"><span data-stu-id="6a3e7-194">The format of the **ErrorSource** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6a3e7-195"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-195"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-196">Il formato è sconosciuto o non interpretabile in maniera significativa da un'applicazione client CIM.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-196">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6a3e7-197"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-197"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-198">Il formato è definito dal valore della proprietà **OtherErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="6a3e7-198">The format is defined by the value of the **OtherErrorSourceFormat** property.</span></span>

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span data-ttu-id="6a3e7-199"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-199"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-200">Percorso dell'oggetto CIM come definito nella specifica dell'infrastruttura CIM.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-200">A CIM Object Path as defined in the CIM Infrastructure specification.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6a3e7-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6a3e7-202">**ErrorType**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-202">**ErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a3e7-203">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a3e7-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-205">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ errore CIM**.**OtherErrorType**")</span><span class="sxs-lookup"><span data-stu-id="6a3e7-205">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**OtherErrorType**")</span></span>
</dt> </dl>

<span data-ttu-id="6a3e7-206">Tipo di errore primario.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-206">The primary error type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6a3e7-207"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-207"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6a3e7-208"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-208"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>

<span data-ttu-id="6a3e7-209"><span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**Errore di comunicazione** (2)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-209"><span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**Communications Error** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-210">Gli errori di questo tipo sono associati principalmente alle procedure e/o ai processi necessari per il trasferimento di informazioni da un punto a un altro.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-210">Errors of this type are principally associated with the procedures and/or processes required to convey information from one point to another.</span></span>

</dd> <dt>

<span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>

<span data-ttu-id="6a3e7-211"><span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**Errore di qualità del servizio** (3)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-211"><span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**Quality of Service Error** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-212">Gli errori di questo tipo sono associati principalmente a errori che comportano una riduzione delle prestazioni o delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-212">Errors of this type are principally associated with failures that result in reduced functionality or performance.</span></span>

</dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="6a3e7-213"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Errore software** (4)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-213"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Error** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-214">Un errore di questo tipo è associato principalmente a un errore software o di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-214">Error of this type are principally associated with a software or processing fault.</span></span>

</dd> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>

<span data-ttu-id="6a3e7-215"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Errore hardware** (5)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-215"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-216">Gli errori di questo tipo sono associati principalmente a un errore hardware o di apparecchiature.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-216">Errors of this type are principally associated with an equipment or hardware failure.</span></span>

</dd> <dt>

<span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>

<span data-ttu-id="6a3e7-217"><span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**Errore ambientale** (6)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-217"><span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**Environmental Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-218">altre considerazioni sull'ambiente.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-218">other environmental considerations.</span></span>

</dd> <dt>

<span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>

<span data-ttu-id="6a3e7-219"><span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**Errore di sicurezza** (7)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-219"><span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**Security Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-220">Gli errori di questo tipo sono associati a violazioni di sicurezza, rilevamento di virus e problemi simili.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-220">Errors of this type are associated with security violations, detection of viruses, and similar issues.</span></span>

</dd> <dt>

<span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>

<span data-ttu-id="6a3e7-221"><span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**Errore di oversubscription** (8)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-221"><span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**Oversubscription Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-222">Gli errori di questo tipo sono associati principalmente all'esito negativo di allocare risorse sufficienti per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-222">Errors of this type are principally associated with the failure to allocate sufficient resources to complete the operation.</span></span>

</dd> <dt>

<span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>

<span data-ttu-id="6a3e7-223"><span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**Errore di risorsa non disponibile** (9)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-223"><span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**Unavailable Resource Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-224">Gli errori di questo tipo sono associati principalmente all'esito negativo dell'accesso a una risorsa necessaria.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-224">Errors of this type are principally associated with the failure to access a required resource.</span></span>

</dd> <dt>

<span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>

<span data-ttu-id="6a3e7-225"><span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>**Errore operazione non supportata** (10)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-225"><span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>**Unsupported Operation Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-226">Gli errori di questo tipo sono associati principalmente a richieste non supportate.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-226">Errors of this type are principally associated with requests that are not supported.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6a3e7-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6a3e7-228">**Messaggio**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-228">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a3e7-229">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a3e7-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-231">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ errore CIM**.**MessageID**","**\_ errore CIM**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="6a3e7-231">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**MessageID**", "**CIM\_Error**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="6a3e7-232">Messaggio formattato.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-232">The formatted message.</span></span>

> [!Note]  
> <span data-ttu-id="6a3e7-233">Questo messaggio viene creato combinando gli elementi dinamici della proprietà **MessageArguments** con gli elementi statici della proprietà **MessageID** e quindi aggiungendoli al registro di sistema dei messaggi o al catalogo associato a **OwningEntity**.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-233">This message is created by combining dynamic elements of the **MessageArguments** property with the static elements of the **MessageID** property, and then adding them to a message registry or catalog associated with the **OwningEntity**.</span></span>

 

</dd> <dt>

<span data-ttu-id="6a3e7-234">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-234">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a3e7-235">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-235">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a3e7-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-237">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ errore CIM**.**MessageID**","**\_ errore CIM**.**Messaggio**")</span><span class="sxs-lookup"><span data-stu-id="6a3e7-237">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**MessageID**", "**CIM\_Error**.**Message**")</span></span>
</dt> </dl>

<span data-ttu-id="6a3e7-238">Matrice che contiene il contenuto dinamico del messaggio.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-238">An array that contains the dynamic content of the message.</span></span>

</dd> <dt>

<span data-ttu-id="6a3e7-239">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-239">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a3e7-240">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a3e7-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-242">Qualificatori: [**obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ errore CIM**.**Messaggio**","**\_ errore CIM**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="6a3e7-242">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**Message**", "**CIM\_Error**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="6a3e7-243">Stringa opaca che identifica in modo univoco, all'interno dell'ambito di OwningEntity, il formato del messaggio.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-243">An opaque string that uniquely identifies, within the scope of the OwningEntity, the format of the Message.</span></span>

</dd> <dt>

<span data-ttu-id="6a3e7-244">**OtherErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-244">**OtherErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a3e7-245">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a3e7-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-247">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ errore CIM**.**ErrorSourceFormat**")</span><span class="sxs-lookup"><span data-stu-id="6a3e7-247">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="6a3e7-248">Stringa che definisce il valore **ErrorSourceFormat** quando **ErrorSourceFormat** è impostato su "1" (other).</span><span class="sxs-lookup"><span data-stu-id="6a3e7-248">A string that defines the **ErrorSourceFormat** value when **ErrorSourceFormat** is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="6a3e7-249">**OtherErrorType**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-249">**OtherErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a3e7-250">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a3e7-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-252">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ errore CIM**.**ErrorType**")</span><span class="sxs-lookup"><span data-stu-id="6a3e7-252">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorType**")</span></span>
</dt> </dl>

<span data-ttu-id="6a3e7-253">Stringa in formato libero che descrive il valore di **ErrorType** quando è impostato su "1" (other).</span><span class="sxs-lookup"><span data-stu-id="6a3e7-253">A free-form string that describes the **ErrorType** value when it is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="6a3e7-254">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-254">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a3e7-255">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a3e7-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a3e7-257">ID univoco dell'entità che possiede il formato del messaggio descritto da questa istanza.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-257">The unique ID of the entity that owns the format of the message described by this instance.</span></span>

> [!Note]  
> <span data-ttu-id="6a3e7-258">Questa proprietà deve includere un nome con copyright, marchio o univoco di proprietà dell'entità business o del corpo degli standard che ha definito il formato del messaggio.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-258">This property must include a copyrighted, trademarked, or unique name that is owned by the business entity or standards body that defined the message format.</span></span>

 

</dd> <dt>

<span data-ttu-id="6a3e7-259">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-259">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a3e7-260">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-260">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a3e7-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-262">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Gravità percepita ")</span><span class="sxs-lookup"><span data-stu-id="6a3e7-262">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="6a3e7-263">Descrizione della gravità dell'errore dal punto di visualizzazione dell'elemento che ha inviato il messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-263">A description of the error severity from the point of view of the element that sent the error message.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6a3e7-264"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-264"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-265">la gravità percepita dell'indicazione è sconosciuta o indeterminata.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-265">the Perceived Severity of the indication is unknown or indeterminate.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6a3e7-266"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-266"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-267">Indica che il valore della gravità è reperibile nella proprietà **OtherSeverity** .</span><span class="sxs-lookup"><span data-stu-id="6a3e7-267">Indicates that the Severity's value can be found in the **OtherSeverity** property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="6a3e7-268"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informazioni** (2)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-268"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-269">Quando si fornisce una risposta informativa, è necessario utilizzare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-269">Information should be used when providing an informative response.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="6a3e7-270"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Danneggiato/avviso** (3)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-270"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-271">Deve essere usato quando è appropriato per consentire all'utente di decidere se è necessaria un'azione.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-271">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="6a3e7-272"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Secondario** (4)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-272"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-273">L'azione è necessaria, ma in questo momento la situazione non è grave.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-273">Action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="6a3e7-274"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principale** (5)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-274"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-275">L'azione è ora necessaria.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-275">Action is needed NOW.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="6a3e7-276"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (6)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-276"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-277">L'azione è ora necessaria e l'ambito è ampio (probabilmente verrà generata un'interruzione imminente a una risorsa critica).</span><span class="sxs-lookup"><span data-stu-id="6a3e7-277">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="6a3e7-278"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irreversibile/irreversibile** (7)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-278"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6a3e7-279">si è verificato un errore, ma è troppo tardi per intraprendere un'azione correttiva.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-279">an error occurred, but it's too late to take remedial action.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6a3e7-280"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-280"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6a3e7-281">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-281">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a3e7-282">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a3e7-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-284">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Probabile "," Recommendation. ITU \| M3100. probableCause "," ITU-IANA-Alarm-TC "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Error**.**ProbableCauseDescription**")</span><span class="sxs-lookup"><span data-stu-id="6a3e7-284">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Probable cause", "Recommendation.ITU\|M3100.probableCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ProbableCauseDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="6a3e7-285">Descrizione della probabile cause dell'errore.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-285">A description of te probable cause of the error.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6a3e7-286">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-286">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6a3e7-287">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-287">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

<span data-ttu-id="6a3e7-288">**Errore scheda/scheda** (2)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-288">**Adapter/Card Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="6a3e7-289">**Errore del sottosistema dell'applicazione** (3)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-289">**Application Subsystem Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

<span data-ttu-id="6a3e7-290">**Larghezza di banda ridotta** (4)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-290">**Bandwidth Reduced** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

<span data-ttu-id="6a3e7-291">**Errore di creazione connessione** (5)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-291">**Connection Establishment Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

<span data-ttu-id="6a3e7-292">**Errore del protocollo di comunicazione** (6)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-292">**Communications Protocol Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="6a3e7-293">**Errore del sottosistema di comunicazione** (7)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-293">**Communications Subsystem Failure** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

<span data-ttu-id="6a3e7-294">**Errore di configurazione/personalizzazione** (8)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-294">**Configuration/Customization Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

<span data-ttu-id="6a3e7-295">**Congestione** (9)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-295">**Congestion** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

<span data-ttu-id="6a3e7-296">**Dati danneggiati** (10)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-296">**Corrupt Data** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

<span data-ttu-id="6a3e7-297">**Limite cicli CPU superato** (11)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-297">**CPU Cycles Limit Exceeded** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

<span data-ttu-id="6a3e7-298">**Errore del set di dati/modem** (12)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-298">**Dataset/Modem Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

<span data-ttu-id="6a3e7-299">**Segnale danneggiato** (13)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-299">**Degraded Signal** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

<span data-ttu-id="6a3e7-300">**Errore di interfaccia DTE-DCE** (14)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-300">**DTE-DCE Interface Error** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

<span data-ttu-id="6a3e7-301">**Sportello enclosure aperto** (15)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-301">**Enclosure Door Open** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

<span data-ttu-id="6a3e7-302">**Malfunzionamento delle apparecchiature** (16)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-302">**Equipment Malfunction** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

<span data-ttu-id="6a3e7-303">**Vibrazione eccessiva** (17)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-303">**Excessive Vibration** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

<span data-ttu-id="6a3e7-304">**Errore di formato del file** (18)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-304">**File Format Error** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

<span data-ttu-id="6a3e7-305">**Fire detected** (19)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-305">**Fire Detected** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

<span data-ttu-id="6a3e7-306">**Flood rilevato** (20)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-306">**Flood Detected** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

<span data-ttu-id="6a3e7-307">**Errore di framing** (21)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-307">**Framing Error** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

<span data-ttu-id="6a3e7-308">**Problema HVAC** (22)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-308">**HVAC Problem** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

<span data-ttu-id="6a3e7-309">**Umidità inaccettabile** (23)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-309">**Humidity Unacceptable** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

<span data-ttu-id="6a3e7-310">**Errore del dispositivo di I/O** (24)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-310">**I/O Device Error** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

<span data-ttu-id="6a3e7-311">**Errore dispositivo di input** (25)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-311">**Input Device Error** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

<span data-ttu-id="6a3e7-312">**Errore LAN** (26)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-312">**LAN Error** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="6a3e7-313">È stata **rilevata una perdita non tossica** (27)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-313">**Non-Toxic Leak Detected** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="6a3e7-314">**Errore di trasmissione del nodo locale** (28)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-314">**Local Node Transmission Error** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

<span data-ttu-id="6a3e7-315">**Perdita di frame** (29)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-315">**Loss of Frame** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

<span data-ttu-id="6a3e7-316">**Perdita del segnale** (30)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-316">**Loss of Signal** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

<span data-ttu-id="6a3e7-317">**Approvvigionamento materiale esaurito** (31)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-317">**Material Supply Exhausted** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

<span data-ttu-id="6a3e7-318">**Problema del multiplexer** (32)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-318">**Multiplexer Problem** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

<span data-ttu-id="6a3e7-319">**Memoria insufficiente** (33)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-319">**Out of Memory** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

<span data-ttu-id="6a3e7-320">**Errore dispositivo di output** (34)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-320">**Output Device Error** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

<span data-ttu-id="6a3e7-321">**Prestazioni** ridotte (35)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-321">**Performance Degraded** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

<span data-ttu-id="6a3e7-322">**Problema di alimentazione** (36)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-322">**Power Problem** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

<span data-ttu-id="6a3e7-323">**Pressione inaccettabile** (37)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-323">**Pressure Unacceptable** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

<span data-ttu-id="6a3e7-324">**Problema del processore (errore interno del computer)** (38)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-324">**Processor Problem (Internal Machine Error)** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

<span data-ttu-id="6a3e7-325">**Errore della pompa** (39)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-325">**Pump Failure** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

<span data-ttu-id="6a3e7-326">**Dimensione coda superata** (40)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-326">**Queue Size Exceeded** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

<span data-ttu-id="6a3e7-327">**Errore di ricezione** (41)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-327">**Receive Failure** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

<span data-ttu-id="6a3e7-328">**Errore del ricevitore** (42)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-328">**Receiver Failure** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="6a3e7-329">**Errore di trasmissione del nodo remoto** (43)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-329">**Remote Node Transmission Error** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

<span data-ttu-id="6a3e7-330">**Risorsa alla capacità o al prossimo livello** (44)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-330">**Resource at or Nearing Capacity** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

<span data-ttu-id="6a3e7-331">**Tempo di risposta eccessivo** (45)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-331">**Response Time Excessive** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

<span data-ttu-id="6a3e7-332">**Frequenza di ritrasmissione eccessiva** (46)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-332">**Retransmission Rate Excessive** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="6a3e7-333">**Errore software** (47)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-333">**Software Error** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

<span data-ttu-id="6a3e7-334">**Programma software terminato in modo anomalo** (48)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-334">**Software Program Abnormally Terminated** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

<span data-ttu-id="6a3e7-335">**Errore del programma software (risultati non corretti)** (49)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-335">**Software Program Error (Incorrect Results)** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

<span data-ttu-id="6a3e7-336">**Problema di capacità di archiviazione** (50)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-336">**Storage Capacity Problem** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

<span data-ttu-id="6a3e7-337">**Temperatura inaccettabile** (51)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-337">**Temperature Unacceptable** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

<span data-ttu-id="6a3e7-338">**Soglia superata** (52)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-338">**Threshold Crossed** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

<span data-ttu-id="6a3e7-339">**Problema di temporizzazione** (53)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-339">**Timing Problem** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="6a3e7-340">È stata **rilevata una perdita tossica** (54)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-340">**Toxic Leak Detected** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

<span data-ttu-id="6a3e7-341">**Errore di trasmissione** (55)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-341">**Transmit Failure** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

<span data-ttu-id="6a3e7-342">**Errore della trasmittente** (56)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-342">**Transmitter Failure** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

<span data-ttu-id="6a3e7-343">**Risorsa sottostante non disponibile** (57)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-343">**Underlying Resource Unavailable** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

<span data-ttu-id="6a3e7-344">**Versione non corrispondente** (58)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-344">**Version Mismatch** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

<span data-ttu-id="6a3e7-345">**Avviso precedente cancellato** (59)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-345">**Previous Alert Cleared** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

<span data-ttu-id="6a3e7-346">**Tentativi di accesso non riusciti** (60)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-346">**Login Attempts Failed** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

<span data-ttu-id="6a3e7-347">**Rilevato virus software** (61)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-347">**Software Virus Detected** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

<span data-ttu-id="6a3e7-348">**Protezione hardware violata** (62)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-348">**Hardware Security Breached** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

<span data-ttu-id="6a3e7-349">**Rilevato un attacco Denial of Service** (63)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-349">**Denial of Service Detected** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

<span data-ttu-id="6a3e7-350">**Mancata corrispondenza delle credenziali di sicurezza** (64)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-350">**Security Credential Mismatch** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

<span data-ttu-id="6a3e7-351">**Accesso non autorizzato** (65)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-351">**Unauthorized Access** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

<span data-ttu-id="6a3e7-352">**Allarme ricevuto** (66)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-352">**Alarm Received** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

<span data-ttu-id="6a3e7-353">**Perdita di puntatore** (67)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-353">**Loss of Pointer** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

<span data-ttu-id="6a3e7-354">**Mancata corrispondenza del payload** (68)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-354">**Payload Mismatch** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

<span data-ttu-id="6a3e7-355">**Errore di trasmissione** (69)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-355">**Transmission Error** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

<span data-ttu-id="6a3e7-356">**Frequenza degli errori eccessiva** (70)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-356">**Excessive Error Rate** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

<span data-ttu-id="6a3e7-357">**Problema di traccia** (71)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-357">**Trace Problem** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

<span data-ttu-id="6a3e7-358">**Elemento non disponibile** (72)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-358">**Element Unavailable** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

<span data-ttu-id="6a3e7-359">**Elemento mancante** (73)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-359">**Element Missing** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

<span data-ttu-id="6a3e7-360">**Perdita di più frame** (74)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-360">**Loss of Multi Frame** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

<span data-ttu-id="6a3e7-361">**Errore canale broadcast** (75)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-361">**Broadcast Channel Failure** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

<span data-ttu-id="6a3e7-362">**Ricevuto messaggio non valido** (76)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-362">**Invalid Message Received** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

<span data-ttu-id="6a3e7-363">**Errore di routing** (77)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-363">**Routing Failure** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

<span data-ttu-id="6a3e7-364">**Errore backplane** (78)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-364">**Backplane Failure** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

<span data-ttu-id="6a3e7-365">**Duplicazione degli identificatori** (79)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-365">**Identifier Duplication** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

<span data-ttu-id="6a3e7-366">**Errore nel percorso di protezione** (80)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-366">**Protection Path Failure** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

<span data-ttu-id="6a3e7-367">**Perdita di sincronizzazione o mancata corrispondenza** (81)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-367">**Sync Loss or Mismatch** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

<span data-ttu-id="6a3e7-368">**Problema terminale** (82)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-368">**Terminal Problem** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

<span data-ttu-id="6a3e7-369">**Errore di clock in tempo reale** (83)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-369">**Real Time Clock Failure** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

<span data-ttu-id="6a3e7-370">**Errore antenna** (84)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-370">**Antenna Failure** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

<span data-ttu-id="6a3e7-371">**Errore di ricarica della batteria** (85)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-371">**Battery Charging Failure** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

<span data-ttu-id="6a3e7-372">**Errore del disco** (86)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-372">**Disk Failure** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

<span data-ttu-id="6a3e7-373">**Errore di salto della frequenza** (87)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-373">**Frequency Hopping Failure** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

<span data-ttu-id="6a3e7-374">**Perdita di ridondanza** (88)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-374">**Loss of Redundancy** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

<span data-ttu-id="6a3e7-375">**Errore alimentatore** (89)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-375">**Power Supply Failure** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

<span data-ttu-id="6a3e7-376">**Problema relativo alla qualità del segnale** (90)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-376">**Signal Quality Problem** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

<span data-ttu-id="6a3e7-377">Scaricamento **della batteria** (91)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-377">**Battery Discharging** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

<span data-ttu-id="6a3e7-378">**Errore batteria** (92)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-378">**Battery Failure** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

<span data-ttu-id="6a3e7-379">**Problema di alimentazione commerciale** (93)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-379">**Commercial Power Problem** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

<span data-ttu-id="6a3e7-380">**Errore ventola** (94)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-380">**Fan Failure** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

<span data-ttu-id="6a3e7-381">**Errore del motore** (95)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-381">**Engine Failure** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

<span data-ttu-id="6a3e7-382">**Errore del sensore** (96)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-382">**Sensor Failure** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

<span data-ttu-id="6a3e7-383">**Errore fusibile** (97)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-383">**Fuse Failure** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

<span data-ttu-id="6a3e7-384">**Errore del generatore** (98)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-384">**Generator Failure** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

<span data-ttu-id="6a3e7-385">**Batteria insufficiente** (99)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-385">**Low Battery** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

<span data-ttu-id="6a3e7-386">**Carburante basso** (100)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-386">**Low Fuel** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

<span data-ttu-id="6a3e7-387">**Acqua bassa** (101)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-387">**Low Water** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

<span data-ttu-id="6a3e7-388">**Gas esplosivo** (102)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-388">**Explosive Gas** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

<span data-ttu-id="6a3e7-389">**Venti elevati** (103)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-389">**High Winds** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

<span data-ttu-id="6a3e7-390">**Accumulo di ghiaccio** (104)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-390">**Ice Buildup** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

<span data-ttu-id="6a3e7-391">**Fumo** (105)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-391">**Smoke** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

<span data-ttu-id="6a3e7-392">**Memoria non corrispondente** (106)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-392">**Memory Mismatch** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

<span data-ttu-id="6a3e7-393">**Cicli esauriti CPU** (107)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-393">**Out of CPU Cycles** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

<span data-ttu-id="6a3e7-394">**Problema relativo all'ambiente software** (108)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-394">**Software Environment Problem** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

<span data-ttu-id="6a3e7-395">**Errore di download del software** (109)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-395">**Software Download Failure** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

<span data-ttu-id="6a3e7-396">**Elemento reinizializzato** (110)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-396">**Element Reinitialized** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

<span data-ttu-id="6a3e7-397">**Timeout** (111)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-397">**Timeout** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

<span data-ttu-id="6a3e7-398">**Problemi di registrazione** (112)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-398">**Logging Problems** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

<span data-ttu-id="6a3e7-399">**Perdita rilevata** (113)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-399">**Leak Detected** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

<span data-ttu-id="6a3e7-400">**Errore del meccanismo di protezione** (114)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-400">**Protection Mechanism Failure** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

<span data-ttu-id="6a3e7-401">**Protezione** di un errore di risorse (115)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-401">**Protecting Resource Failure** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

<span data-ttu-id="6a3e7-402">**Incoerenza del database** (116)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-402">**Database Inconsistency** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

<span data-ttu-id="6a3e7-403">**Errore di autenticazione** (117)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-403">**Authentication Failure** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

<span data-ttu-id="6a3e7-404">**Violazione della riservatezza** (118)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-404">**Breach of Confidentiality** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

<span data-ttu-id="6a3e7-405">**Manomissione cavo** (119)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-405">**Cable Tamper** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

<span data-ttu-id="6a3e7-406">**Informazioni ritardate** (120)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-406">**Delayed Information** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

<span data-ttu-id="6a3e7-407">**Informazioni duplicate** (121)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-407">**Duplicate Information** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

<span data-ttu-id="6a3e7-408">**Informazioni mancanti** (122)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-408">**Information Missing** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

<span data-ttu-id="6a3e7-409">**Modifica delle informazioni** (123)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-409">**Information Modification** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

<span data-ttu-id="6a3e7-410">**Informazioni fuori sequenza** (124)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-410">**Information Out of Sequence** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

<span data-ttu-id="6a3e7-411">**Chiave scaduta** (125)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-411">**Key Expired** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

<span data-ttu-id="6a3e7-412">**Errore di non ripudio** (126)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-412">**Non-Repudiation Failure** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

<span data-ttu-id="6a3e7-413">**Attività fuori orario** (127)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-413">**Out of Hours Activity** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

<span data-ttu-id="6a3e7-414">**Fuori servizio** (128)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-414">**Out of Service** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

<span data-ttu-id="6a3e7-415">**Errore procedurale** (129)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-415">**Procedural Error** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

<span data-ttu-id="6a3e7-416">**Informazioni impreviste** (130)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-416">**Unexpected Information** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6a3e7-417">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6a3e7-417">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6a3e7-418">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-418">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a3e7-419">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-420">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a3e7-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-421">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ errore CIM**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="6a3e7-421">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="6a3e7-422">Stringa in formato libero che descrive la probabile cause dell'errore, quando la proprietà **ProbableCause** è impostata su "1" (other).</span><span class="sxs-lookup"><span data-stu-id="6a3e7-422">A free-form string that describes the probable cause of the error, when the **ProbableCause** property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="6a3e7-423">**RecommendedActions**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-423">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a3e7-424">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="6a3e7-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6a3e7-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a3e7-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a3e7-426">Matrice di stringhe in formato libero che descrivono le azioni consigliate da eseguire per risolvere l'errore.</span><span class="sxs-lookup"><span data-stu-id="6a3e7-426">An array of free-form strings that describe the recommended actions to take to resolve the error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a3e7-427">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a3e7-427">Requirements</span></span>



| <span data-ttu-id="6a3e7-428">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a3e7-428">Requirement</span></span> | <span data-ttu-id="6a3e7-429">Valore</span><span class="sxs-lookup"><span data-stu-id="6a3e7-429">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a3e7-430">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a3e7-430">Minimum supported client</span></span><br/> | <span data-ttu-id="6a3e7-431">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6a3e7-431">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6a3e7-432">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a3e7-432">Minimum supported server</span></span><br/> | <span data-ttu-id="6a3e7-433">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a3e7-433">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6a3e7-434">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6a3e7-434">Namespace</span></span><br/>                | <span data-ttu-id="6a3e7-435">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6a3e7-435">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6a3e7-436">MOF</span><span class="sxs-lookup"><span data-stu-id="6a3e7-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a3e7-437"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a3e7-437"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a3e7-438">DLL</span><span class="sxs-lookup"><span data-stu-id="6a3e7-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a3e7-439"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6a3e7-439"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

