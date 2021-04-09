---
description: Sono incluse informazioni sulla gravità, la cause, le azioni consigliate e altri dati correlati all'esito negativo di un'operazione CIM.
ms.assetid: 128B9ECE-D26C-4A7D-BFB7-69CD986B0DBA
title: Classe Msvm_Error
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Error
- Msvm_Error.ErrorType
- Msvm_Error.OtherErrorType
- Msvm_Error.OwningEntity
- Msvm_Error.MessageID
- Msvm_Error.Message
- Msvm_Error.MessageArguments
- Msvm_Error.PerceivedSeverity
- Msvm_Error.ProbableCause
- Msvm_Error.ProbableCauseDescription
- Msvm_Error.RecommendedActions
- Msvm_Error.ErrorSource
- Msvm_Error.ErrorSourceFormat
- Msvm_Error.OtherErrorSourceFormat
- Msvm_Error.CIMStatusCode
- Msvm_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56b3b30f1d64146db2554d097b11104df09ba018
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050085"
---
# <a name="msvm_error-class"></a><span data-ttu-id="b0103-103">\_Classe di errore MSVM</span><span class="sxs-lookup"><span data-stu-id="b0103-103">Msvm\_Error class</span></span>

<span data-ttu-id="b0103-104">Classe specializzata che contiene informazioni sulla gravità, la cause, le azioni consigliate e altri dati correlati all'esito negativo di un'operazione CIM.</span><span class="sxs-lookup"><span data-stu-id="b0103-104">A specialized class that contains information about the severity, cause, recommended actions, and other data related to the failure of a CIM Operation.</span></span>

<span data-ttu-id="b0103-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b0103-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0103-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0103-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Error : CIM_Error
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

## <a name="members"></a><span data-ttu-id="b0103-107">Members</span><span class="sxs-lookup"><span data-stu-id="b0103-107">Members</span></span>

<span data-ttu-id="b0103-108">La classe di **\_ errore MSVM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b0103-108">The **Msvm\_Error** class has these types of members:</span></span>

-   [<span data-ttu-id="b0103-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b0103-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0103-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b0103-110">Properties</span></span>

<span data-ttu-id="b0103-111">La classe di **\_ errore MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b0103-111">The **Msvm\_Error** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0103-112">**CIMStatusCode**</span><span class="sxs-lookup"><span data-stu-id="b0103-112">**CIMStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0103-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0103-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0103-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b0103-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0103-115">Codice di stato CIM che caratterizza questa istanza.</span><span class="sxs-lookup"><span data-stu-id="b0103-115">The CIM status code that characterizes this instance.</span></span> <span data-ttu-id="b0103-116">Questa proprietà definisce i codici di stato che possono essere restituiti da un listener o un server CIM conforme.</span><span class="sxs-lookup"><span data-stu-id="b0103-116">This property defines the status codes that may be return by a conforming CIM Server or Listener.</span></span> <span data-ttu-id="b0103-117">Non tutti i codici di stato sono validi per ogni operazione.</span><span class="sxs-lookup"><span data-stu-id="b0103-117">Not all status codes are valid for each operation.</span></span> <span data-ttu-id="b0103-118">La specifica per ogni operazione deve definire i codici di stato che possono essere restituiti da tale operazione.</span><span class="sxs-lookup"><span data-stu-id="b0103-118">The specification for each operation should define the status codes that may be returned by that operation.</span></span> <span data-ttu-id="b0103-119">Sono definiti i valori seguenti per il codice di stato CIM.</span><span class="sxs-lookup"><span data-stu-id="b0103-119">The following values for CIM status code are defined.</span></span> <span data-ttu-id="b0103-120">Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0103-120">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>



| <span data-ttu-id="b0103-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b0103-121">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="b0103-122">Significato</span><span class="sxs-lookup"><span data-stu-id="b0103-122">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span><dl> <span data-ttu-id="b0103-123"><dt>**CIM \_ ERRORE \_**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-123"><dt>**CIM\_ERR\_FAILED**</dt> <dt>1</dt></span></span> </dl>                                                                       | <span data-ttu-id="b0103-124">Si è verificato un errore generale che non è coperto da un codice di errore più specifico.</span><span class="sxs-lookup"><span data-stu-id="b0103-124">A general error occurred that is not covered by a more specific error code.</span></span><br/>    |
| <span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span><dl> <span data-ttu-id="b0103-125"><dt>**CIM \_ ERRORE di \_ accesso \_ negato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-125"><dt>**CIM\_ERR\_ACCESS\_DENIED**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="b0103-126">L'accesso a una risorsa CIM non è disponibile per il client.</span><span class="sxs-lookup"><span data-stu-id="b0103-126">Access to a CIM resource was not available to the client.</span></span><br/>                      |
| <span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span><dl> <span data-ttu-id="b0103-127"><dt>**CIM \_ ERRORE \_ \_ spazio dei nomi**</dt> <dt>3</dt> errato</span><span class="sxs-lookup"><span data-stu-id="b0103-127"><dt>**CIM\_ERR\_INVALID\_NAMESPACE**</dt> <dt>3</dt></span></span> </dl>                                     | <span data-ttu-id="b0103-128">Lo spazio dei nomi di destinazione non esiste.</span><span class="sxs-lookup"><span data-stu-id="b0103-128">The target namespace does not exist.</span></span><br/>                                           |
| <span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span><dl> <span data-ttu-id="b0103-129"><dt>**CIM \_ ERR \_ \_ parametro 4 non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b0103-129"><dt>**CIM\_ERR\_INVALID\_PARAMETER**</dt> <dt>4</dt></span></span> </dl>                                     | <span data-ttu-id="b0103-130">Uno o più valori di parametro passati al metodo non sono validi.</span><span class="sxs-lookup"><span data-stu-id="b0103-130">One or more parameter values passed to the method were invalid.</span></span><br/>                |
| <span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span><dl> <span data-ttu-id="b0103-131"><dt>**CIM \_ ERR \_ \_ classe 5 non valida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b0103-131"><dt>**CIM\_ERR\_INVALID\_CLASS**</dt> <dt>5</dt></span></span> </dl>                                                 | <span data-ttu-id="b0103-132">La classe specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="b0103-132">The specified class does not exist.</span></span><br/>                                            |
| <span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span><dl> <span data-ttu-id="b0103-133"><dt>**CIM \_ ERRORE \_ non \_ trovato**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-133"><dt>**CIM\_ERR\_NOT\_FOUND**</dt> <dt>6</dt></span></span> </dl>                                                             | <span data-ttu-id="b0103-134">Impossibile trovare l'oggetto richiesto.</span><span class="sxs-lookup"><span data-stu-id="b0103-134">The requested object could not be found.</span></span><br/>                                       |
| <span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span><dl> <span data-ttu-id="b0103-135"><dt>**CIM \_ ERR \_ non \_ supportato**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-135"><dt>**CIM\_ERR\_NOT\_SUPPORTED**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="b0103-136">L'operazione richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="b0103-136">The requested operation is not supported.</span></span><br/>                                      |
| <span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span><dl> <span data-ttu-id="b0103-137"><dt>**CIM \_ \_Classe ERR \_ con \_ figli**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-137"><dt>**CIM\_ERR\_CLASS\_HAS\_CHILDREN**</dt> <dt>8</dt></span></span> </dl>                                 | <span data-ttu-id="b0103-138">Non è possibile eseguire l'operazione su questa classe perché contiene istanze.</span><span class="sxs-lookup"><span data-stu-id="b0103-138">Operation cannot be carried out on this class because it has instances.</span></span><br/>        |
| <span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span><dl> <span data-ttu-id="b0103-139"><dt>**CIM \_ \_Classe ERR \_ con \_ istanze**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-139"><dt>**CIM\_ERR\_CLASS\_HAS\_INSTANCES**</dt> <dt>9</dt></span></span> </dl>                              | <span data-ttu-id="b0103-140">Non è possibile eseguire l'operazione su questa classe perché contiene istanze.</span><span class="sxs-lookup"><span data-stu-id="b0103-140">Operation cannot be carried out on this class since it has instances.</span></span><br/>          |
| <span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span><dl> <span data-ttu-id="b0103-141"><dt>**CIM \_ ERRORE \_ \_ superclasse**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-141"><dt>**CIM\_ERR\_INVALID\_SUPERCLASS**</dt> <dt>10</dt></span></span> </dl>                                 | <span data-ttu-id="b0103-142">Non è possibile eseguire l'operazione perché la superclasse specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="b0103-142">Operation cannot be carried out since the specified superclass does not exist.</span></span><br/> |
| <span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span><dl> <span data-ttu-id="b0103-143"><dt>**CIM \_ Il \_ Err \_ esiste già**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-143"><dt>**CIM\_ERR\_ALREADY\_EXISTS**</dt> <dt>11</dt></span></span> </dl>                                             | <span data-ttu-id="b0103-144">Non è possibile eseguire l'operazione perché esiste già un oggetto.</span><span class="sxs-lookup"><span data-stu-id="b0103-144">Operation cannot be carried out because an object already exists.</span></span><br/>              |
| <span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span><dl> <span data-ttu-id="b0103-145"><dt>**CIM \_ \_Nessuna \_ \_ proprietà di questo tipo**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-145"><dt>**CIM\_ERR\_NO\_SUCH\_PROPERTY**</dt> <dt>12</dt></span></span> </dl>                                      | <span data-ttu-id="b0103-146">La proprietà specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="b0103-146">The specified Property does not exist.</span></span><br/>                                         |
| <span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span><dl> <span data-ttu-id="b0103-147"><dt>**CIM \_ Tipo ERR non \_ \_ corrispondente**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-147"><dt>**CIM\_ERR\_TYPE\_MISMATCH**</dt> <dt>13</dt></span></span> </dl>                                                | <span data-ttu-id="b0103-148">Il valore specificato non è compatibile con il tipo.</span><span class="sxs-lookup"><span data-stu-id="b0103-148">The value supplied is incompatible with the type.</span></span><br/>                              |
| <span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span><dl> <span data-ttu-id="b0103-149"><dt>**CIM \_ Il \_ linguaggio di query ERR \_ non è \_ \_ supportato**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-149"><dt>**CIM\_ERR\_QUERY\_LANGUAGE\_NOT\_SUPPORTED**</dt> <dt>14</dt></span></span> </dl> | <span data-ttu-id="b0103-150">Il linguaggio di query non è riconosciuto né supportato.</span><span class="sxs-lookup"><span data-stu-id="b0103-150">The query language is not recognized or supported.</span></span><br/>                             |
| <span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span><dl> <span data-ttu-id="b0103-151"><dt>**CIM \_ \_ \_ Query Err non valida**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-151"><dt>**CIM\_ERR\_INVALID\_QUERY**</dt> <dt>15</dt></span></span> </dl>                                                | <span data-ttu-id="b0103-152">La query non è valida per il linguaggio di query specificato.</span><span class="sxs-lookup"><span data-stu-id="b0103-152">The query is not valid for the specified query language.</span></span><br/>                       |
| <span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span><dl> <span data-ttu-id="b0103-153"><dt>**CIM \_ \_Metodo ERR \_ non \_ disponibile**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-153"><dt>**CIM\_ERR\_METHOD\_NOT\_AVAILABLE**</dt> <dt>16</dt></span></span> </dl>                          | <span data-ttu-id="b0103-154">Impossibile eseguire il metodo estrinseco.</span><span class="sxs-lookup"><span data-stu-id="b0103-154">The extrinsic method could not be executed.</span></span><br/>                                    |
| <span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span><dl> <span data-ttu-id="b0103-155"><dt>**CIM \_ \_Metodo ERR \_ non \_ trovato**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-155"><dt>**CIM\_ERR\_METHOD\_NOT\_FOUND**</dt> <dt>17</dt></span></span> </dl>                                      | <span data-ttu-id="b0103-156">Il metodo estrinseco specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="b0103-156">The specified extrinsic method does not exist.</span></span><br/>                                 |
| <span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span><dl> <span data-ttu-id="b0103-157"><dt>**CIM \_ \_ \_ Risposta imprevista a Err**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-157"><dt>**CIM\_ERR\_UNEXPECTED\_RESPONSE**</dt> <dt>18</dt></span></span> </dl>                              | <span data-ttu-id="b0103-158">La risposta restituita all'operazione asincrona non era prevista.</span><span class="sxs-lookup"><span data-stu-id="b0103-158">The returned response to the asynchronous operation was not expected.</span></span><br/>          |
| <span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span><dl> <span data-ttu-id="b0103-159"><dt>**CIM \_ ERRORE \_ \_ \_ destinazione risposta non valida**</dt> <dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-159"><dt>**CIM\_ERR\_INVALID\_RESPONSE\_DESTINATION**</dt> <dt>19</dt></span></span> </dl>  | <span data-ttu-id="b0103-160">La destinazione specificata per la risposta asincrona non è valida.</span><span class="sxs-lookup"><span data-stu-id="b0103-160">The specified destination for the asynchronous response is not valid.</span></span><br/>          |
| <span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span><dl> <span data-ttu-id="b0103-161"><dt>**CIM \_ \_Spazio dei nomi ERR \_ non \_ vuoto**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-161"><dt>**CIM\_ERR\_NAMESPACE\_NOT\_EMPTY**</dt> <dt>20</dt></span></span> </dl>                             | <span data-ttu-id="b0103-162">Lo spazio dei nomi specificato non è vuoto.</span><span class="sxs-lookup"><span data-stu-id="b0103-162">The specified namespace is not empty.</span></span><br/>                                          |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="b0103-163"><dt>**DMTF riservato**</dt> <dt>21 = *valore*</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-163"><dt>**DMTF Reserved**</dt> <dt>21 = *value* </dt></span></span> </dl>                            | <span data-ttu-id="b0103-164">Valori riservati.</span><span class="sxs-lookup"><span data-stu-id="b0103-164">Reserved values.</span></span><br/>                                                               |



 

</dd> <dt>

<span data-ttu-id="b0103-165">**CIMStatusCodeDescription**</span><span class="sxs-lookup"><span data-stu-id="b0103-165">**CIMStatusCodeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0103-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b0103-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0103-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b0103-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0103-168">Stringa contenente una descrizione leggibile dall'utente della proprietà **CIMStatusCode** .</span><span class="sxs-lookup"><span data-stu-id="b0103-168">A string containing a user-readable description of the **CIMStatusCode** property.</span></span> <span data-ttu-id="b0103-169">Questa descrizione può estendersi, ma deve essere coerente con la definizione di **CIMStatusCode**.</span><span class="sxs-lookup"><span data-stu-id="b0103-169">This description may extend, but must be consistent with, the definition of **CIMStatusCode**.</span></span> <span data-ttu-id="b0103-170">Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0103-170">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b0103-171">**ErrorSource**</span><span class="sxs-lookup"><span data-stu-id="b0103-171">**ErrorSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0103-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b0103-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0103-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b0103-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0103-174">Informazioni di identificazione dell'entità, ovvero l'istanza, che genera l'errore.</span><span class="sxs-lookup"><span data-stu-id="b0103-174">The identifying information of the entity (the instance) generating the error.</span></span> <span data-ttu-id="b0103-175">Se questa entità è modellata nello schema CIM, questa proprietà contiene il percorso dell'istanza codificata come parametro di stringa.</span><span class="sxs-lookup"><span data-stu-id="b0103-175">If this entity is modeled in the CIM Schema, this property contains the path of the instance encoded as a string parameter.</span></span> <span data-ttu-id="b0103-176">Se non è modellato, la proprietà contiene una stringa di identificazione che assegna un nome all'entità che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="b0103-176">If not modeled, the property contains some identifying string that names the entity that generated the error.</span></span> <span data-ttu-id="b0103-177">Il percorso o la stringa di identificazione viene formattato in base alla proprietà **ErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="b0103-177">The path or identifying string is formatted per the **ErrorSourceFormat** property.</span></span> <span data-ttu-id="b0103-178">Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0103-178">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b0103-179">**ErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="b0103-179">**ErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0103-180">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0103-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0103-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b0103-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0103-182">Il formato della proprietà **ErrorSource** è interpretabile in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b0103-182">The format of the **ErrorSource** property is interpretable based on the value of this property.</span></span> <span data-ttu-id="b0103-183">Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85))ed è sempre impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="b0103-183">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)), and it is always set to 0.</span></span>



| <span data-ttu-id="b0103-184">Valore</span><span class="sxs-lookup"><span data-stu-id="b0103-184">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="b0103-185">Significato</span><span class="sxs-lookup"><span data-stu-id="b0103-185">Meaning</span></span>                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="b0103-186"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-186"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="b0103-187">Il formato è sconosciuto o non interpretabile in maniera significativa da un'applicazione client CIM.</span><span class="sxs-lookup"><span data-stu-id="b0103-187">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span><br/>                                         |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="b0103-188"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-188"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                          | <span data-ttu-id="b0103-189">Il formato è definito dal valore della proprietà **OtherErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="b0103-189">The format is defined by the value of the **OtherErrorSourceFormat** property.</span></span><br/>                                               |
| <span id="CIMObjectHandle"></span><span id="cimobjecthandle"></span><span id="CIMOBJECTHANDLE"></span><dl> <span data-ttu-id="b0103-190"><dt>**CIMObjectHandle**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-190"><dt>**CIMObjectHandle**</dt> <dt>2 </dt></span></span> </dl> | <span data-ttu-id="b0103-191">Per identificare l'entità, viene usato un handle di oggetto CIM, codificato usando la sintassi MOF definita per objectHandle non terminale.</span><span class="sxs-lookup"><span data-stu-id="b0103-191">A CIM Object Handle, encoded using the MOF syntax defined for the objectHandle non-terminal, is used to identify the entity.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b0103-192">**ErrorType**</span><span class="sxs-lookup"><span data-stu-id="b0103-192">**ErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0103-193">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0103-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0103-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b0103-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0103-195">Classificazione primaria dell'errore.</span><span class="sxs-lookup"><span data-stu-id="b0103-195">Primary classification of the error.</span></span> <span data-ttu-id="b0103-196">Vengono definiti i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b0103-196">The following values are defined.</span></span> <span data-ttu-id="b0103-197">Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0103-197">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>



| <span data-ttu-id="b0103-198">Valore</span><span class="sxs-lookup"><span data-stu-id="b0103-198">Value</span></span>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="b0103-199">Significato</span><span class="sxs-lookup"><span data-stu-id="b0103-199">Meaning</span></span>                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="b0103-200"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-200"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                                                   |                                                                                                                                                          |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="b0103-201"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-201"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                                                           |                                                                                                                                                          |
| <span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span><dl> <span data-ttu-id="b0103-202"><dt>**Errore di comunicazione**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-202"><dt>**Communications Error**</dt> <dt>2</dt></span></span> </dl>                               | <span data-ttu-id="b0103-203">Gli errori di questo tipo sono associati principalmente alle procedure e/o ai processi necessari per il trasferimento di informazioni da un punto a un altro.</span><span class="sxs-lookup"><span data-stu-id="b0103-203">Errors of this type are principally associated with the procedures and/or processes required to convey information from one point to another.</span></span><br/> |
| <span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span><dl> <span data-ttu-id="b0103-204"><dt>**Qualità del servizio-errore**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-204"><dt>**Quality of Service Error**</dt> <dt>3</dt></span></span> </dl>               | <span data-ttu-id="b0103-205">Gli errori di questo tipo sono associati principalmente a errori che comportano una riduzione delle prestazioni o delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="b0103-205">Errors of this type are principally associated with failures that result in reduced functionality or performance.</span></span><br/>                             |
| <span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span><dl> <span data-ttu-id="b0103-206"><dt>**Errore software**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-206"><dt>**Software Error**</dt> <dt>4</dt></span></span> </dl>                                                       | <span data-ttu-id="b0103-207">Un errore di questo tipo è associato principalmente a un errore software o di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="b0103-207">Error of this type are principally associated with a software or processing fault.</span></span><br/>                                                            |
| <span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span><dl> <span data-ttu-id="b0103-208"><dt>**Errore hardware**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-208"><dt>**Hardware Error**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="b0103-209">Gli errori di questo tipo sono associati principalmente a un errore hardware o di apparecchiature.</span><span class="sxs-lookup"><span data-stu-id="b0103-209">Errors of this type are principally associated with an equipment or hardware failure.</span></span><br/>                                                         |
| <span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span><dl> <span data-ttu-id="b0103-210"><dt>**Errore ambientale**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-210"><dt>**Environmental Error**</dt> <dt>6</dt></span></span> </dl>                                   | <span data-ttu-id="b0103-211">Gli errori di questo tipo sono associati principalmente a una condizione di errore relativa alla struttura o ad altre considerazioni sull'ambiente.</span><span class="sxs-lookup"><span data-stu-id="b0103-211">Errors of this type are principally associated with a failure condition relating to the facility, or other environmental considerations.</span></span><br/>      |
| <span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span><dl> <span data-ttu-id="b0103-212"><dt>**Errore di sicurezza**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-212"><dt>**Security Error**</dt> <dt>7</dt></span></span> </dl>                                                       | <span data-ttu-id="b0103-213">Gli errori di questo tipo sono associati a violazioni di sicurezza, rilevamento di virus e problemi simili.</span><span class="sxs-lookup"><span data-stu-id="b0103-213">Errors of this type are associated with security violations, detection of viruses, and similar issues.</span></span><br/>                                        |
| <span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span><dl> <span data-ttu-id="b0103-214"><dt>**Errore oversubscription**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-214"><dt>**Oversubscription Error**</dt> <dt>8</dt></span></span> </dl>                       | <span data-ttu-id="b0103-215">Gli errori di questo tipo sono associati principalmente all'esito negativo di allocare risorse sufficienti per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b0103-215">Errors of this type are principally associated with the failure to allocate sufficient resources to complete the operation.</span></span><br/>                   |
| <span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span><dl> <span data-ttu-id="b0103-216"><dt>**Errore di risorsa non disponibile**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-216"><dt>**Unavailable Resource Error**</dt> <dt>9</dt></span></span> </dl>       | <span data-ttu-id="b0103-217">Gli errori di questo tipo sono associati principalmente all'esito negativo dell'accesso a una risorsa necessaria.</span><span class="sxs-lookup"><span data-stu-id="b0103-217">Errors of this type are principally associated with the failure to access a required resource.</span></span><br/>                                                |
| <span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span><dl> <span data-ttu-id="b0103-218"><dt>**Errore di operazione**</dt> <dt>10</dt> non supportato</span><span class="sxs-lookup"><span data-stu-id="b0103-218"><dt>**Unsupported Operation Error**</dt> <dt>10 </dt></span></span> </dl> | <span data-ttu-id="b0103-219">Gli errori di questo tipo sono associati principalmente a richieste non supportate.</span><span class="sxs-lookup"><span data-stu-id="b0103-219">Errors of this type are principally associated with requests that are not supported.</span></span><br/>                                                          |



 

</dd> <dt>

<span data-ttu-id="b0103-220">**Messaggio**</span><span class="sxs-lookup"><span data-stu-id="b0103-220">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0103-221">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b0103-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0103-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b0103-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0103-223">Messaggio formattato.</span><span class="sxs-lookup"><span data-stu-id="b0103-223">The formatted message.</span></span> <span data-ttu-id="b0103-224">Questo messaggio viene costruito applicando il contenuto dinamico del messaggio, descritto in **MessageArguments**, alla stringa di formato identificata in modo univoco, all'interno dell'ambito di **OwningEntity**, da **MessageID**.</span><span class="sxs-lookup"><span data-stu-id="b0103-224">This message is constructed by applying the dynamic content of the message, described in **MessageArguments**, to the format string uniquely identified, within the scope of the **OwningEntity**, by **MessageID**.</span></span> <span data-ttu-id="b0103-225">Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0103-225">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b0103-226">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="b0103-226">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0103-227">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b0103-227">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b0103-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b0103-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0103-229">Matrice contenente il contenuto dinamico del messaggio.</span><span class="sxs-lookup"><span data-stu-id="b0103-229">An array containing the dynamic content of the message.</span></span> <span data-ttu-id="b0103-230">Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0103-230">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b0103-231">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="b0103-231">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0103-232">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b0103-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0103-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b0103-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0103-234">Stringa opaca che identifica in modo univoco, all'interno dell'ambito di **OwningEntity**, il formato del messaggio.</span><span class="sxs-lookup"><span data-stu-id="b0103-234">An opaque string that uniquely identifies, within the scope of the **OwningEntity**, the format of the message.</span></span> <span data-ttu-id="b0103-235">Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0103-235">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b0103-236">**OtherErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="b0103-236">**OtherErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0103-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b0103-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0103-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b0103-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0103-239">Stringa che definisce i valori "other" per **ErrorSourceFormat**.</span><span class="sxs-lookup"><span data-stu-id="b0103-239">A string defining "Other" values for **ErrorSourceFormat**.</span></span> <span data-ttu-id="b0103-240">Questo valore deve essere impostato su un valore non NULL quando **ErrorSourceFormat** è impostato su un valore di 1 (other).</span><span class="sxs-lookup"><span data-stu-id="b0103-240">This value must be set to a non-NULL value when **ErrorSourceFormat** is set to a value of 1 (Other).</span></span> <span data-ttu-id="b0103-241">Per tutti gli altri valori di **ErrorSourceFormat**, il valore di questa stringa deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="b0103-241">For all other values of **ErrorSourceFormat**, the value of this string must be set to **Null**.</span></span> <span data-ttu-id="b0103-242">Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0103-242">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b0103-243">**OtherErrorType**</span><span class="sxs-lookup"><span data-stu-id="b0103-243">**OtherErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0103-244">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b0103-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0103-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b0103-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0103-246">Stringa che descrive **ErrorType** quando 1, (other), viene specificato come **ErrorType**.</span><span class="sxs-lookup"><span data-stu-id="b0103-246">A string that describes the **ErrorType** when 1, (Other), is specified as the **ErrorType**.</span></span> <span data-ttu-id="b0103-247">Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0103-247">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b0103-248">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="b0103-248">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0103-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b0103-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0103-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b0103-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0103-251">Stringa che identifica in modo univoco l'entità a cui appartiene la definizione del formato del messaggio descritto in questa istanza.</span><span class="sxs-lookup"><span data-stu-id="b0103-251">A string that uniquely identifies the entity that owns the definition of the format of the message described in this instance.</span></span> <span data-ttu-id="b0103-252">**OwningEntity** deve includere un nome con copyright, marchio o in altro modo univoco di proprietà dell'entità di business o del corpo degli standard che definisce il formato.</span><span class="sxs-lookup"><span data-stu-id="b0103-252">**OwningEntity** must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity or standards body defining the format.</span></span> <span data-ttu-id="b0103-253">Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0103-253">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b0103-254">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="b0103-254">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0103-255">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0103-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0103-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b0103-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0103-257">Valore enumerato che descrive la gravità dell'errore dal punto di vista del notificatore: 2-basso deve essere usato per problemi non critici, ad esempio parametri non validi, utilizzo errato, funzionalità non supportate.</span><span class="sxs-lookup"><span data-stu-id="b0103-257">An enumerated value that describes the severity of the error from the notifier's point of view: 2 - Low should be used for noncritical issues such as invalid parameters, incorrect usage, unsupported functionality.</span></span> <span data-ttu-id="b0103-258">3-medium deve essere usato per indicare che l'azione è necessaria, ma in questo momento la situazione non è grave.</span><span class="sxs-lookup"><span data-stu-id="b0103-258">3 - Medium should be used to indicate action is needed, but the situation is not serious at this time.</span></span> <span data-ttu-id="b0103-259">4-High deve essere usato per indicare che l'azione è ora necessaria.</span><span class="sxs-lookup"><span data-stu-id="b0103-259">4 - High should be used to indicate action is needed now.</span></span> <span data-ttu-id="b0103-260">5: è consigliabile usare un valore irreversibile per indicare una perdita di dati o un errore irreversibile del sistema o del servizio.</span><span class="sxs-lookup"><span data-stu-id="b0103-260">5 - Fatal should be used to indicate a loss of data or unrecoverable system or service failure.</span></span> <span data-ttu-id="b0103-261">Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0103-261">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="b0103-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b0103-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-263"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Bassa** (2)</span><span class="sxs-lookup"><span data-stu-id="b0103-263"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-264"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Media** (3)</span><span class="sxs-lookup"><span data-stu-id="b0103-264"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medium** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-265"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alta** (4)</span><span class="sxs-lookup"><span data-stu-id="b0103-265"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-266"><span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**Irreversibile** (5)</span><span class="sxs-lookup"><span data-stu-id="b0103-266"><span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**Fatal** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b0103-267">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="b0103-267">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0103-268">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0103-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0103-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b0103-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0103-270">Valore enumerato che descrive la probabile cause dell'errore.</span><span class="sxs-lookup"><span data-stu-id="b0103-270">An enumerated value that describes the probable cause of the error.</span></span> <span data-ttu-id="b0103-271">Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0103-271">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="b0103-272"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b0103-272"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-273"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b0103-273"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-274"><span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Errore scheda/scheda** (2)</span><span class="sxs-lookup"><span data-stu-id="b0103-274"><span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Adapter/Card Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-275"><span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Errore del sottosistema dell'applicazione** (3)</span><span class="sxs-lookup"><span data-stu-id="b0103-275"><span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Application Subsystem Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-276"><span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Larghezza di banda ridotta** (4)</span><span class="sxs-lookup"><span data-stu-id="b0103-276"><span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Bandwidth Reduced** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-277"><span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Errore di creazione connessione** (5)</span><span class="sxs-lookup"><span data-stu-id="b0103-277"><span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Connection Establishment Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-278"><span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Errore del protocollo di comunicazione** (6)</span><span class="sxs-lookup"><span data-stu-id="b0103-278"><span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Communications Protocol Error** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-279"><span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Errore del sottosistema di comunicazione** (7)</span><span class="sxs-lookup"><span data-stu-id="b0103-279"><span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Communications Subsystem Failure** (7)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-280"><span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Errore di configurazione/personalizzazione** (8)</span><span class="sxs-lookup"><span data-stu-id="b0103-280"><span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Configuration/Customization Error** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-281"><span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Congestione** (9)</span><span class="sxs-lookup"><span data-stu-id="b0103-281"><span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Congestion** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-282"><span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**Dati danneggiati** (10)</span><span class="sxs-lookup"><span data-stu-id="b0103-282"><span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**Corrupt Data** (10)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-283"><span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**Limite cicli CPU superato** (11)</span><span class="sxs-lookup"><span data-stu-id="b0103-283"><span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**CPU Cycles Limit Exceeded** (11)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-284"><span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**Errore del set di dati/modem** (12)</span><span class="sxs-lookup"><span data-stu-id="b0103-284"><span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**Dataset/Modem Error** (12)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-285"><span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**Segnale danneggiato** (13)</span><span class="sxs-lookup"><span data-stu-id="b0103-285"><span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**Degraded Signal** (13)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-286"><span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**Errore di interfaccia DTE-DCE** (14)</span><span class="sxs-lookup"><span data-stu-id="b0103-286"><span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**DTE-DCE Interface Error** (14)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-287"><span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**Sportello enclosure aperto** (15)</span><span class="sxs-lookup"><span data-stu-id="b0103-287"><span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**Enclosure Door Open** (15)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-288"><span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Malfunzionamento delle apparecchiature** (16)</span><span class="sxs-lookup"><span data-stu-id="b0103-288"><span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Equipment Malfunction** (16)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-289"><span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Vibrazione eccessiva** (17)</span><span class="sxs-lookup"><span data-stu-id="b0103-289"><span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Excessive Vibration** (17)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-290"><span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**Errore di formato del file** (18)</span><span class="sxs-lookup"><span data-stu-id="b0103-290"><span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**File Format Error** (18)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-291"><span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**Fire detected** (19)</span><span class="sxs-lookup"><span data-stu-id="b0103-291"><span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**Fire Detected** (19)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-292"><span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>**Flood rilevato** (20)</span><span class="sxs-lookup"><span data-stu-id="b0103-292"><span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>**Flood Detected** (20)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-293"><span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Errore di framing** (21)</span><span class="sxs-lookup"><span data-stu-id="b0103-293"><span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Framing Error** (21)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-294"><span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**Problema HVAC** (22)</span><span class="sxs-lookup"><span data-stu-id="b0103-294"><span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**HVAC Problem** (22)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-295"><span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Umidità inaccettabile** (23)</span><span class="sxs-lookup"><span data-stu-id="b0103-295"><span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Humidity Unacceptable** (23)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-296"><span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**Errore del dispositivo di I/O** (24)</span><span class="sxs-lookup"><span data-stu-id="b0103-296"><span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**I/O Device Error** (24)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-297"><span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Errore dispositivo di input** (25)</span><span class="sxs-lookup"><span data-stu-id="b0103-297"><span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Input Device Error** (25)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-298"><span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**Errore LAN** (26)</span><span class="sxs-lookup"><span data-stu-id="b0103-298"><span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**LAN Error** (26)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-299"><span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>È stata **rilevata una perdita non tossica** (27)</span><span class="sxs-lookup"><span data-stu-id="b0103-299"><span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>**Non-Toxic Leak Detected** (27)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-300"><span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Errore di trasmissione del nodo locale** (28)</span><span class="sxs-lookup"><span data-stu-id="b0103-300"><span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Local Node Transmission Error** (28)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-301"><span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Perdita di frame** (29)</span><span class="sxs-lookup"><span data-stu-id="b0103-301"><span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Loss of Frame** (29)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-302"><span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Perdita del segnale** (30)</span><span class="sxs-lookup"><span data-stu-id="b0103-302"><span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Loss of Signal** (30)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-303"><span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**//31 approvvigionamento materiale esaurito** (31)</span><span class="sxs-lookup"><span data-stu-id="b0103-303"><span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**//31 Material Supply Exhausted** (31)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-304"><span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Problema del multiplexer** (32)</span><span class="sxs-lookup"><span data-stu-id="b0103-304"><span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Multiplexer Problem** (32)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-305"><span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Memoria insufficiente** (33)</span><span class="sxs-lookup"><span data-stu-id="b0103-305"><span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Out of Memory** (33)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-306"><span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Errore dispositivo di output** (34)</span><span class="sxs-lookup"><span data-stu-id="b0103-306"><span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Output Device Error** (34)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-307"><span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**Prestazioni** ridotte (35)</span><span class="sxs-lookup"><span data-stu-id="b0103-307"><span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**Performance Degraded** (35)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-308"><span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Problema di alimentazione** (36)</span><span class="sxs-lookup"><span data-stu-id="b0103-308"><span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Power Problem** (36)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-309"><span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Pressione inaccettabile** (37)</span><span class="sxs-lookup"><span data-stu-id="b0103-309"><span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Pressure Unacceptable** (37)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-310"><span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Problema del processore (errore interno del computer)** (38)</span><span class="sxs-lookup"><span data-stu-id="b0103-310"><span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Processor Problem (Internal Machine Error)** (38)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-311"><span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Errore della pompa** (39)</span><span class="sxs-lookup"><span data-stu-id="b0103-311"><span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Pump Failure** (39)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-312"><span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Dimensione coda superata** (40)</span><span class="sxs-lookup"><span data-stu-id="b0103-312"><span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Queue Size Exceeded** (40)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-313"><span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Errore di ricezione** (41)</span><span class="sxs-lookup"><span data-stu-id="b0103-313"><span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Receive Failure** (41)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-314"><span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Errore del ricevitore** (42)</span><span class="sxs-lookup"><span data-stu-id="b0103-314"><span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Receiver Failure** (42)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-315"><span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Errore di trasmissione del nodo remoto** (43)</span><span class="sxs-lookup"><span data-stu-id="b0103-315"><span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Remote Node Transmission Error** (43)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-316"><span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Risorsa alla capacità o al prossimo livello** (44)</span><span class="sxs-lookup"><span data-stu-id="b0103-316"><span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Resource at or Nearing Capacity** (44)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-317"><span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Tempo di risposta eccessivo** (45)</span><span class="sxs-lookup"><span data-stu-id="b0103-317"><span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Response Time Excessive** (45)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-318"><span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Frequenza di ritrasmissione eccessiva** (46)</span><span class="sxs-lookup"><span data-stu-id="b0103-318"><span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Retransmission Rate Excessive** (46)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-319"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Errore software** (47)</span><span class="sxs-lookup"><span data-stu-id="b0103-319"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Error** (47)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-320"><span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**Programma software terminato in modo anomalo** (48)</span><span class="sxs-lookup"><span data-stu-id="b0103-320"><span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**Software Program Abnormally Terminated** (48)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-321"><span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Errore del programma software (risultati non corretti)** (49)</span><span class="sxs-lookup"><span data-stu-id="b0103-321"><span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Software Program Error (Incorrect Results)** (49)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-322"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Problema di capacità di archiviazione** (50)</span><span class="sxs-lookup"><span data-stu-id="b0103-322"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Capacity Problem** (50)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-323"><span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Temperatura inaccettabile** (51)</span><span class="sxs-lookup"><span data-stu-id="b0103-323"><span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Temperature Unacceptable** (51)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-324"><span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Soglia superata** (52)</span><span class="sxs-lookup"><span data-stu-id="b0103-324"><span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Threshold Crossed** (52)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-325"><span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Problema di temporizzazione** (53)</span><span class="sxs-lookup"><span data-stu-id="b0103-325"><span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Timing Problem** (53)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-326"><span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>È stata **rilevata una perdita tossica** (54)</span><span class="sxs-lookup"><span data-stu-id="b0103-326"><span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>**Toxic Leak Detected** (54)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-327"><span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Errore di trasmissione** (55)</span><span class="sxs-lookup"><span data-stu-id="b0103-327"><span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Transmit Failure** (55)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-328"><span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**Errore della trasmittente** (56)</span><span class="sxs-lookup"><span data-stu-id="b0103-328"><span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**Transmitter Failure** (56)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-329"><span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Risorsa sottostante non disponibile** (57)</span><span class="sxs-lookup"><span data-stu-id="b0103-329"><span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Underlying Resource Unavailable** (57)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-330"><span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Versione non corrispondente** (58)</span><span class="sxs-lookup"><span data-stu-id="b0103-330"><span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Version Mismatch** (58)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-331"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Avviso precedente cancellato** (59)</span><span class="sxs-lookup"><span data-stu-id="b0103-331"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Previous Alert Cleared** (59)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-332"><span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**60 tentativi di accesso non riusciti** (60)</span><span class="sxs-lookup"><span data-stu-id="b0103-332"><span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**//60 Login Attempts Failed** (60)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-333"><span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Rilevato virus software** (61)</span><span class="sxs-lookup"><span data-stu-id="b0103-333"><span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Software Virus Detected** (61)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-334"><span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Protezione hardware violata** (62)</span><span class="sxs-lookup"><span data-stu-id="b0103-334"><span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Hardware Security Breached** (62)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-335"><span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Rilevato un attacco Denial of Service** (63)</span><span class="sxs-lookup"><span data-stu-id="b0103-335"><span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Denial of Service Detected** (63)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-336"><span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**Mancata corrispondenza delle credenziali di sicurezza** (64)</span><span class="sxs-lookup"><span data-stu-id="b0103-336"><span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**Security Credential Mismatch** (64)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-337"><span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**Accesso non autorizzato** (65)</span><span class="sxs-lookup"><span data-stu-id="b0103-337"><span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**Unauthorized Access** (65)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-338"><span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Allarme ricevuto** (66)</span><span class="sxs-lookup"><span data-stu-id="b0103-338"><span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Alarm Received** (66)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-339"><span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Perdita di puntatore** (67)</span><span class="sxs-lookup"><span data-stu-id="b0103-339"><span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Loss of Pointer** (67)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-340"><span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>**Mancata corrispondenza del payload** (68)</span><span class="sxs-lookup"><span data-stu-id="b0103-340"><span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>**Payload Mismatch** (68)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-341"><span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Errore di trasmissione** (69)</span><span class="sxs-lookup"><span data-stu-id="b0103-341"><span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Transmission Error** (69)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-342"><span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Frequenza degli errori eccessiva** (70)</span><span class="sxs-lookup"><span data-stu-id="b0103-342"><span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Excessive Error Rate** (70)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-343"><span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**Problema di traccia** (71)</span><span class="sxs-lookup"><span data-stu-id="b0103-343"><span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**Trace Problem** (71)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-344"><span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Elemento non disponibile** (72)</span><span class="sxs-lookup"><span data-stu-id="b0103-344"><span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Element Unavailable** (72)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-345"><span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**Elemento mancante** (73)</span><span class="sxs-lookup"><span data-stu-id="b0103-345"><span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**Element Missing** (73)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-346"><span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Perdita di più frame** (74)</span><span class="sxs-lookup"><span data-stu-id="b0103-346"><span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Loss of Multi Frame** (74)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-347"><span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Errore canale broadcast** (75)</span><span class="sxs-lookup"><span data-stu-id="b0103-347"><span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Broadcast Channel Failure** (75)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-348"><span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**Ricevuto messaggio non valido** (76)</span><span class="sxs-lookup"><span data-stu-id="b0103-348"><span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**Invalid Message Received** (76)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-349"><span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Errore di routing** (77)</span><span class="sxs-lookup"><span data-stu-id="b0103-349"><span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Routing Failure** (77)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-350"><span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Errore backplane** (78)</span><span class="sxs-lookup"><span data-stu-id="b0103-350"><span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Backplane Failure** (78)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-351"><span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Duplicazione degli identificatori** (79)</span><span class="sxs-lookup"><span data-stu-id="b0103-351"><span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Identifier Duplication** (79)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-352"><span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Errore nel percorso di protezione** (80)</span><span class="sxs-lookup"><span data-stu-id="b0103-352"><span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Protection Path Failure** (80)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-353"><span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Perdita di sincronizzazione o mancata corrispondenza** (81)</span><span class="sxs-lookup"><span data-stu-id="b0103-353"><span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Sync Loss or Mismatch** (81)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-354"><span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Problema terminale** (82)</span><span class="sxs-lookup"><span data-stu-id="b0103-354"><span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Terminal Problem** (82)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-355"><span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Errore di clock in tempo reale** (83)</span><span class="sxs-lookup"><span data-stu-id="b0103-355"><span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Real Time Clock Failure** (83)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-356"><span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Errore antenna** (84)</span><span class="sxs-lookup"><span data-stu-id="b0103-356"><span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Antenna Failure** (84)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-357"><span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Errore di ricarica della batteria** (85)</span><span class="sxs-lookup"><span data-stu-id="b0103-357"><span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Battery Charging Failure** (85)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-358"><span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**Errore del disco** (86)</span><span class="sxs-lookup"><span data-stu-id="b0103-358"><span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**Disk Failure** (86)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-359"><span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Errore di salto della frequenza** (87)</span><span class="sxs-lookup"><span data-stu-id="b0103-359"><span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Frequency Hopping Failure** (87)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-360"><span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Perdita di ridondanza** (88)</span><span class="sxs-lookup"><span data-stu-id="b0103-360"><span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Loss of Redundancy** (88)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-361"><span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Errore alimentatore** (89)</span><span class="sxs-lookup"><span data-stu-id="b0103-361"><span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Power Supply Failure** (89)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-362"><span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Problema relativo alla qualità del segnale** (90)</span><span class="sxs-lookup"><span data-stu-id="b0103-362"><span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Signal Quality Problem** (90)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-363"><span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>Scaricamento **batteria 91** (91)</span><span class="sxs-lookup"><span data-stu-id="b0103-363"><span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>**//91 Battery Discharging** (91)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-364"><span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Errore batteria** (92)</span><span class="sxs-lookup"><span data-stu-id="b0103-364"><span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Battery Failure** (92)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-365"><span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Problema di alimentazione commerciale** (93)</span><span class="sxs-lookup"><span data-stu-id="b0103-365"><span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Commercial Power Problem** (93)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-366"><span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Errore ventola** (94)</span><span class="sxs-lookup"><span data-stu-id="b0103-366"><span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Fan Failure** (94)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-367"><span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**Errore del motore** (95)</span><span class="sxs-lookup"><span data-stu-id="b0103-367"><span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**Engine Failure** (95)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-368"><span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Errore del sensore** (96)</span><span class="sxs-lookup"><span data-stu-id="b0103-368"><span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Sensor Failure** (96)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-369"><span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Errore fusibile** (97)</span><span class="sxs-lookup"><span data-stu-id="b0103-369"><span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Fuse Failure** (97)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-370"><span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Errore del generatore** (98)</span><span class="sxs-lookup"><span data-stu-id="b0103-370"><span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Generator Failure** (98)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-371"><span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Batteria insufficiente** (99)</span><span class="sxs-lookup"><span data-stu-id="b0103-371"><span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Low Battery** (99)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-372"><span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Carburante basso** (100)</span><span class="sxs-lookup"><span data-stu-id="b0103-372"><span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Low Fuel** (100)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-373"><span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Acqua bassa** (101)</span><span class="sxs-lookup"><span data-stu-id="b0103-373"><span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Low Water** (101)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-374"><span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Gas esplosivo** (102)</span><span class="sxs-lookup"><span data-stu-id="b0103-374"><span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Explosive Gas** (102)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-375"><span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**Venti elevati** (103)</span><span class="sxs-lookup"><span data-stu-id="b0103-375"><span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**High Winds** (103)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-376"><span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Accumulo di ghiaccio** (104)</span><span class="sxs-lookup"><span data-stu-id="b0103-376"><span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Ice Buildup** (104)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-377"><span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**Fumo** (105)</span><span class="sxs-lookup"><span data-stu-id="b0103-377"><span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**Smoke** (105)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-378"><span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**Memoria non corrispondente** (106)</span><span class="sxs-lookup"><span data-stu-id="b0103-378"><span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**Memory Mismatch** (106)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-379"><span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Cicli esauriti CPU** (107)</span><span class="sxs-lookup"><span data-stu-id="b0103-379"><span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Out of CPU Cycles** (107)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-380"><span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Problema relativo all'ambiente software** (108)</span><span class="sxs-lookup"><span data-stu-id="b0103-380"><span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Software Environment Problem** (108)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-381"><span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Errore di download del software** (109)</span><span class="sxs-lookup"><span data-stu-id="b0103-381"><span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Software Download Failure** (109)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-382"><span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**Elemento reinizializzato** (110)</span><span class="sxs-lookup"><span data-stu-id="b0103-382"><span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**Element Reinitialized** (110)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-383"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Timeout** (111)</span><span class="sxs-lookup"><span data-stu-id="b0103-383"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Timeout** (111)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-384"><span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Problemi di registrazione** (112)</span><span class="sxs-lookup"><span data-stu-id="b0103-384"><span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Logging Problems** (112)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-385"><span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>**Perdita rilevata** (113)</span><span class="sxs-lookup"><span data-stu-id="b0103-385"><span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>**Leak Detected** (113)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-386"><span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Errore del meccanismo di protezione** (114)</span><span class="sxs-lookup"><span data-stu-id="b0103-386"><span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Protection Mechanism Failure** (114)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-387"><span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**115 protezione errore risorse** (115)</span><span class="sxs-lookup"><span data-stu-id="b0103-387"><span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**//115 Protecting Resource Failure** (115)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-388"><span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**Incoerenza del database** (116)</span><span class="sxs-lookup"><span data-stu-id="b0103-388"><span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**Database Inconsistency** (116)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-389"><span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Errore di autenticazione** (117)</span><span class="sxs-lookup"><span data-stu-id="b0103-389"><span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Authentication Failure** (117)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-390"><span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Violazione della riservatezza** (118)</span><span class="sxs-lookup"><span data-stu-id="b0103-390"><span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Breach of Confidentiality** (118)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-391"><span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Manomissione cavo** (119)</span><span class="sxs-lookup"><span data-stu-id="b0103-391"><span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Cable Tamper** (119)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-392"><span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Informazioni ritardate** (120)</span><span class="sxs-lookup"><span data-stu-id="b0103-392"><span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Delayed Information** (120)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-393"><span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Informazioni duplicate** (121)</span><span class="sxs-lookup"><span data-stu-id="b0103-393"><span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Duplicate Information** (121)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-394"><span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Informazioni mancanti** (122)</span><span class="sxs-lookup"><span data-stu-id="b0103-394"><span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Information Missing** (122)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-395"><span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Modifica delle informazioni** (123)</span><span class="sxs-lookup"><span data-stu-id="b0103-395"><span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Information Modification** (123)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-396"><span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Informazioni fuori sequenza** (124)</span><span class="sxs-lookup"><span data-stu-id="b0103-396"><span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Information Out of Sequence** (124)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-397"><span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**Chiave scaduta** (125)</span><span class="sxs-lookup"><span data-stu-id="b0103-397"><span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**Key Expired** (125)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-398"><span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Errore di non ripudio** (126)</span><span class="sxs-lookup"><span data-stu-id="b0103-398"><span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Non-Repudiation Failure** (126)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-399"><span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Attività fuori orario** (127)</span><span class="sxs-lookup"><span data-stu-id="b0103-399"><span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Out of Hours Activity** (127)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-400"><span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**Fuori servizio** (128)</span><span class="sxs-lookup"><span data-stu-id="b0103-400"><span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**Out of Service** (128)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-401"><span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Errore procedurale** (129)</span><span class="sxs-lookup"><span data-stu-id="b0103-401"><span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Procedural Error** (129)</span></span>
</dt> <dt>

<span data-ttu-id="b0103-402"><span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Informazioni impreviste** (130)</span><span class="sxs-lookup"><span data-stu-id="b0103-402"><span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Unexpected Information** (130 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b0103-403">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="b0103-403">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0103-404">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b0103-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0103-405">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b0103-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0103-406">Stringa che descrive la probabile cause dell'errore.</span><span class="sxs-lookup"><span data-stu-id="b0103-406">A string that describes the probable cause of the error.</span></span> <span data-ttu-id="b0103-407">Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0103-407">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b0103-408">**RecommendedActions**</span><span class="sxs-lookup"><span data-stu-id="b0103-408">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0103-409">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="b0103-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b0103-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b0103-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0103-411">Stringa che descrive le azioni consigliate da eseguire per risolvere l'errore.</span><span class="sxs-lookup"><span data-stu-id="b0103-411">A string that describes recommended actions to take to resolve the error.</span></span> <span data-ttu-id="b0103-412">Questa proprietà viene ereditata da un [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0103-412">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0103-413">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0103-413">Remarks</span></span>

<span data-ttu-id="b0103-414">L'accesso alla classe di **\_ errore MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="b0103-414">Access to the **Msvm\_Error** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b0103-415">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b0103-415">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0103-416">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0103-416">Requirements</span></span>



| <span data-ttu-id="b0103-417">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0103-417">Requirement</span></span> | <span data-ttu-id="b0103-418">Valore</span><span class="sxs-lookup"><span data-stu-id="b0103-418">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0103-419">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0103-419">Minimum supported client</span></span><br/> | <span data-ttu-id="b0103-420">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b0103-420">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b0103-421">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0103-421">Minimum supported server</span></span><br/> | <span data-ttu-id="b0103-422">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b0103-422">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b0103-423">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b0103-423">Namespace</span></span><br/>                | <span data-ttu-id="b0103-424">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b0103-424">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b0103-425">MOF</span><span class="sxs-lookup"><span data-stu-id="b0103-425">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0103-426"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-426"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0103-427">DLL</span><span class="sxs-lookup"><span data-stu-id="b0103-427">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0103-428"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b0103-428"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b0103-429">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0103-429">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0103-430">**\_Errore CIM**</span><span class="sxs-lookup"><span data-stu-id="b0103-430">**CIM\_Error**</span></span>](cim-error.md)
</dt> <dt>

<span data-ttu-id="b0103-431">[**\_Errore CIM**](/previous-versions//cc150671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b0103-431">[**CIM\_Error**](/previous-versions//cc150671(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b0103-432">Classi di gestione del sistema virtuale</span><span class="sxs-lookup"><span data-stu-id="b0103-432">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

