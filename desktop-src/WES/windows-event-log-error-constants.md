---
title: Costanti di errore nel registro eventi di Windows (WinError. h)
description: Di seguito sono riportati i codici di errore definiti nel registro eventi di Windows.
ms.assetid: 889ea4ae-dede-45d5-9293-cec85d81f010
topic_type:
- apiref
api_name:
- ERROR_EVT_INVALID_CHANNEL_PATH
- ERROR_EVT_INVALID_QUERY
- ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND
- ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND
- ERROR_EVT_INVALID_PUBLISHER_NAME
- ERROR_EVT_INVALID_EVENT_DATA
- ERROR_EVT_CHANNEL_NOT_FOUND
- ERROR_EVT_MALFORMED_XML_TEXT
- ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL
- ERROR_EVT_CONFIGURATION_ERROR
- ERROR_EVT_QUERY_RESULT_STALE
- ERROR_EVT_QUERY_RESULT_INVALID_POSITION
- ERROR_EVT_NON_VALIDATING_MSXML
- ERROR_EVT_FILTER_ALREADYSCOPED
- ERROR_EVT_FILTER_NOTELTSET
- ERROR_EVT_FILTER_INVARG
- ERROR_EVT_FILTER_INVTEST
- ERROR_EVT_FILTER_INVTYPE
- ERROR_EVT_FILTER_PARSEERR
- ERROR_EVT_FILTER_UNSUPPORTEDOP
- ERROR_EVT_FILTER_UNEXPECTEDTOKEN
- ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL
- ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE
- ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE
- ERROR_EVT_CHANNEL_CANNOT_ACTIVATE
- ERROR_EVT_FILTER_TOO_COMPLEX
- ERROR_EVT_MESSAGE_NOT_FOUND
- ERROR_EVT_MESSAGE_ID_NOT_FOUND
- ERROR_EVT_UNRESOLVED_VALUE_INSERT
- ERROR_EVT_UNRESOLVED_PARAMETER_INSERT
- ERROR_EVT_MAX_INSERTS_REACHED
- ERROR_EVT_EVENT_DEFINITION_NOT_FOUND
- ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND
- ERROR_EVT_VERSION_TOO_OLD
- ERROR_EVT_VERSION_TOO_NEW
- ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY
- ERROR_EVT_PUBLISHER_DISABLED
- ERROR_EVT_FILTER_OUT_OF_RANGE
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa5443d98c53d6abedbe3a0027e8e2e524ae9df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302540"
---
# <a name="windows-event-log-error-constants"></a><span data-ttu-id="abf41-103">Costanti di errore nel registro eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="abf41-103">Windows Event Log Error Constants</span></span>

<span data-ttu-id="abf41-104">Di seguito sono riportati i codici di errore definiti nel registro eventi di Windows.</span><span class="sxs-lookup"><span data-stu-id="abf41-104">The following are the error codes that Windows Event Log defines.</span></span>

<dl> <dt>

<span data-ttu-id="abf41-105"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERRORE \_ evt \_ \_ percorso del canale non valido \_**</span><span class="sxs-lookup"><span data-stu-id="abf41-105"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-106">15000</span><span class="sxs-lookup"><span data-stu-id="abf41-106">15000</span></span>
</dt> <dt>



<span data-ttu-id="abf41-107">Il percorso del canale specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="abf41-107">The specified channel path is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-108"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERRORE \_ evt \_ query non valida \_**</span><span class="sxs-lookup"><span data-stu-id="abf41-108"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERROR\_EVT\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-109">15001</span><span class="sxs-lookup"><span data-stu-id="abf41-109">15001</span></span>
</dt> <dt>



<span data-ttu-id="abf41-110">La query specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="abf41-110">The specified query is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-111"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERRORE \_ evt \_ pubblicazione \_ metadati \_ non \_ trovati**</span><span class="sxs-lookup"><span data-stu-id="abf41-111"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERROR\_EVT\_PUBLISHER\_METADATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-112">15002</span><span class="sxs-lookup"><span data-stu-id="abf41-112">15002</span></span>
</dt> <dt>



<span data-ttu-id="abf41-113">Impossibile trovare i metadati del provider nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="abf41-113">The provider metadata cannot be found in the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-114"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERRORE \_ evt \_ modello di evento \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="abf41-114"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERROR\_EVT\_EVENT\_TEMPLATE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-115">15003</span><span class="sxs-lookup"><span data-stu-id="abf41-115">15003</span></span>
</dt> <dt>



<span data-ttu-id="abf41-116">Il modello per la definizione di un evento non è stato trovato nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="abf41-116">The template for an event definition cannot be found in the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-117"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERRORE \_ evt \_ \_ nome dell'autore non valido \_**</span><span class="sxs-lookup"><span data-stu-id="abf41-117"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-118">15004</span><span class="sxs-lookup"><span data-stu-id="abf41-118">15004</span></span>
</dt> <dt>



<span data-ttu-id="abf41-119">Il nome del provider specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="abf41-119">The specified provider name is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-120"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERRORE \_ evt \_ \_ dati evento non validi \_**</span><span class="sxs-lookup"><span data-stu-id="abf41-120"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERROR\_EVT\_INVALID\_EVENT\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-121">15005</span><span class="sxs-lookup"><span data-stu-id="abf41-121">15005</span></span>
</dt> <dt>



<span data-ttu-id="abf41-122">I dati dell'evento generati dal provider non sono compatibili con la definizione del modello di evento nel manifesto del provider.</span><span class="sxs-lookup"><span data-stu-id="abf41-122">The event data raised by the provider is not compatible with the event template definition in the provider's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-123"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERRORE \_ \_ canale evt \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="abf41-123"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERROR\_EVT\_CHANNEL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-124">15007</span><span class="sxs-lookup"><span data-stu-id="abf41-124">15007</span></span>
</dt> <dt>



<span data-ttu-id="abf41-125">Impossibile trovare il canale specificato.</span><span class="sxs-lookup"><span data-stu-id="abf41-125">The specified channel cannot be found.</span></span> <span data-ttu-id="abf41-126">Controllare la configurazione del canale.</span><span class="sxs-lookup"><span data-stu-id="abf41-126">Check the channel configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-127"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERRORE \_ evt \_ \_ testo XML non valido \_**</span><span class="sxs-lookup"><span data-stu-id="abf41-127"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERROR\_EVT\_MALFORMED\_XML\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-128">15008</span><span class="sxs-lookup"><span data-stu-id="abf41-128">15008</span></span>
</dt> <dt>



<span data-ttu-id="abf41-129">Il testo XML specificato non è ben formato.</span><span class="sxs-lookup"><span data-stu-id="abf41-129">The specified XML text was not well-formed.</span></span> <span data-ttu-id="abf41-130">Per ulteriori informazioni, chiamare la funzione [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) .</span><span class="sxs-lookup"><span data-stu-id="abf41-130">For more information, call the [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-131"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERRORE \_ evt \_ sottoscrizione \_ al \_ \_ canale diretto**</span><span class="sxs-lookup"><span data-stu-id="abf41-131"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERROR\_EVT\_SUBSCRIPTION\_TO\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-132">15009</span><span class="sxs-lookup"><span data-stu-id="abf41-132">15009</span></span>
</dt> <dt>



<span data-ttu-id="abf41-133">Non è possibile sottoscrivere un canale analitico o di debug; gli eventi per un canale analitico o di debug passano direttamente a un file di log e non possono essere sottoscritti.</span><span class="sxs-lookup"><span data-stu-id="abf41-133">You cannot subscribe to an Analytic or Debug channel; the events for an Analytic or Debug channel go directly to a log file and cannot be subscribed to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-134"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**errore \_ di \_ configurazione di evt \_**</span><span class="sxs-lookup"><span data-stu-id="abf41-134"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**ERROR\_EVT\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-135">15010</span><span class="sxs-lookup"><span data-stu-id="abf41-135">15010</span></span>
</dt> <dt>



<span data-ttu-id="abf41-136">Errore di configurazione.</span><span class="sxs-lookup"><span data-stu-id="abf41-136">A configuration error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-137"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERRORE il \_ risultato della query evt non è \_ \_ \_ aggiornato**</span><span class="sxs-lookup"><span data-stu-id="abf41-137"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERROR\_EVT\_QUERY\_RESULT\_STALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-138">15011</span><span class="sxs-lookup"><span data-stu-id="abf41-138">15011</span></span>
</dt> <dt>



<span data-ttu-id="abf41-139">Il risultato della query non è valido.</span><span class="sxs-lookup"><span data-stu-id="abf41-139">The query result is not valid.</span></span> <span data-ttu-id="abf41-140">Questo problema può essere dovuto al fatto che il log è stato cancellato o spostato dopo la creazione del risultato della query.</span><span class="sxs-lookup"><span data-stu-id="abf41-140">This may be due to the log being cleared or rolling over after the query result was created.</span></span> <span data-ttu-id="abf41-141">Rilasciare l'oggetto risultato della query ed eseguire nuovamente la query.</span><span class="sxs-lookup"><span data-stu-id="abf41-141">Release the query result object and reissue the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-142"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERRORE \_ il \_ risultato della query evt \_ \_ posizione non valida \_**</span><span class="sxs-lookup"><span data-stu-id="abf41-142"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERROR\_EVT\_QUERY\_RESULT\_INVALID\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-143">15012</span><span class="sxs-lookup"><span data-stu-id="abf41-143">15012</span></span>
</dt> <dt>



<span data-ttu-id="abf41-144">Il cursore per il risultato della query non sta puntando a una posizione valida.</span><span class="sxs-lookup"><span data-stu-id="abf41-144">The cursor for the query result is not pointing to a valid position.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-145"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERRORE \_ evt \_ non \_ convalida \_ MSXML**</span><span class="sxs-lookup"><span data-stu-id="abf41-145"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR\_EVT\_NON\_VALIDATING\_MSXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-146">15013</span><span class="sxs-lookup"><span data-stu-id="abf41-146">15013</span></span>
</dt> <dt>



<span data-ttu-id="abf41-147">Il parser MSXML registrato non supporta la convalida.</span><span class="sxs-lookup"><span data-stu-id="abf41-147">The registered MSXML parser does not support validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-148"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERRORE \_ evt \_ filtro \_ ALREADYSCOPED**</span><span class="sxs-lookup"><span data-stu-id="abf41-148"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR\_EVT\_FILTER\_ALREADYSCOPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-149">15014</span><span class="sxs-lookup"><span data-stu-id="abf41-149">15014</span></span>
</dt> <dt>



<span data-ttu-id="abf41-150">Un'espressione può essere seguita da una modifica dell'operazione dell'ambito solo se l'espressione restituisce un set di nodi e non fa già parte di un'altra modifica dell'operazione dell'ambito.</span><span class="sxs-lookup"><span data-stu-id="abf41-150">An expression can be followed by a change of scope operation only if the expression evaluates to a node set and is not already part of some other change of scope operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-151"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERRORE \_ evt \_ filtro \_ NOTELTSET**</span><span class="sxs-lookup"><span data-stu-id="abf41-151"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR\_EVT\_FILTER\_NOTELTSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-152">15015</span><span class="sxs-lookup"><span data-stu-id="abf41-152">15015</span></span>
</dt> <dt>



<span data-ttu-id="abf41-153">Non è possibile eseguire un'operazione di passaggio da un termine che non rappresenta un set di elementi.</span><span class="sxs-lookup"><span data-stu-id="abf41-153">Cannot perform a step operation from a term that does not represent an element set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-154"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERRORE \_ evt \_ filtro \_ INVARG**</span><span class="sxs-lookup"><span data-stu-id="abf41-154"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERROR\_EVT\_FILTER\_INVARG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-155">15016</span><span class="sxs-lookup"><span data-stu-id="abf41-155">15016</span></span>
</dt> <dt>



<span data-ttu-id="abf41-156">Gli argomenti sul lato sinistro di un operatore binario devono essere attributi, nodi o variabili e gli argomenti sul lato destro devono essere costanti.</span><span class="sxs-lookup"><span data-stu-id="abf41-156">The arguments on the left side of a binary operator must be either attributes, nodes, or variables, and the arguments on the right side must be constants.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-157"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERRORE \_ evt \_ filtro \_ INVTEST**</span><span class="sxs-lookup"><span data-stu-id="abf41-157"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERROR\_EVT\_FILTER\_INVTEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-158">15017</span><span class="sxs-lookup"><span data-stu-id="abf41-158">15017</span></span>
</dt> <dt>



<span data-ttu-id="abf41-159">Un'operazione Step deve coinvolgere un test di nodo o, nel caso di un predicato, un'espressione algebrica sulla quale testare ogni nodo nel set di nodi identificato dal set di nodi precedente può essere valutato.</span><span class="sxs-lookup"><span data-stu-id="abf41-159">A step operation must involve either a node test or, in the case of a predicate, an algebraic expression against which to test each node in the node set identified by the preceding node set can be evaluated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-160"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERRORE \_ evt \_ filtro \_ INVTYPE**</span><span class="sxs-lookup"><span data-stu-id="abf41-160"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERROR\_EVT\_FILTER\_INVTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-161">15018</span><span class="sxs-lookup"><span data-stu-id="abf41-161">15018</span></span>
</dt> <dt>



<span data-ttu-id="abf41-162">Questo tipo di dati non è supportato.</span><span class="sxs-lookup"><span data-stu-id="abf41-162">This data type not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-163"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERRORE \_ evt \_ filtro \_ PARSEERR**</span><span class="sxs-lookup"><span data-stu-id="abf41-163"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERROR\_EVT\_FILTER\_PARSEERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-164">15019</span><span class="sxs-lookup"><span data-stu-id="abf41-164">15019</span></span>
</dt> <dt>



<span data-ttu-id="abf41-165">Si è verificato un errore di sintassi nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="abf41-165">A syntax error occurred at the specified position.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-166"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERRORE \_ evt \_ filtro \_ UNSUPPORTEDOP**</span><span class="sxs-lookup"><span data-stu-id="abf41-166"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERROR\_EVT\_FILTER\_UNSUPPORTEDOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-167">15020</span><span class="sxs-lookup"><span data-stu-id="abf41-167">15020</span></span>
</dt> <dt>



<span data-ttu-id="abf41-168">Questo operatore non è supportato da questa implementazione del filtro.</span><span class="sxs-lookup"><span data-stu-id="abf41-168">This operator is unsupported by this implementation of the filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-169"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERRORE \_ evt \_ filtro \_ UNEXPECTEDTOKEN**</span><span class="sxs-lookup"><span data-stu-id="abf41-169"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR\_EVT\_FILTER\_UNEXPECTEDTOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-170">15021</span><span class="sxs-lookup"><span data-stu-id="abf41-170">15021</span></span>
</dt> <dt>



<span data-ttu-id="abf41-171">Il token rilevato è imprevisto.</span><span class="sxs-lookup"><span data-stu-id="abf41-171">The token encountered was unexpected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-172"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERRORE \_ evt \_ \_ operazione non \_ valida \_ su \_ canale diretto abilitato \_**</span><span class="sxs-lookup"><span data-stu-id="abf41-172"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERROR\_EVT\_INVALID\_OPERATION\_OVER\_ENABLED\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-173">15022</span><span class="sxs-lookup"><span data-stu-id="abf41-173">15022</span></span>
</dt> <dt>



<span data-ttu-id="abf41-174">Non è possibile eseguire l'operazione richiesta su un canale analitico o di debug abilitato.</span><span class="sxs-lookup"><span data-stu-id="abf41-174">The requested operation cannot be performed over an enabled Analytic or Debug channel.</span></span> <span data-ttu-id="abf41-175">È necessario disabilitare il canale prima di eseguire l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="abf41-175">You must disable the channel before performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-176"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERRORE \_ evt \_ \_ valore della \_ proprietà del canale non valido \_**</span><span class="sxs-lookup"><span data-stu-id="abf41-176"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-177">15023</span><span class="sxs-lookup"><span data-stu-id="abf41-177">15023</span></span>
</dt> <dt>



<span data-ttu-id="abf41-178">La proprietà Channel contiene un valore non valido.</span><span class="sxs-lookup"><span data-stu-id="abf41-178">The channel property contains a value that is not valid.</span></span> <span data-ttu-id="abf41-179">Il tipo del valore potrebbe non essere valido, il valore potrebbe non essere compreso nell'intervallo oppure il valore non può essere aggiornato o non è supportato per questo tipo di canale.</span><span class="sxs-lookup"><span data-stu-id="abf41-179">The value's type may not be valid, the value may be out of range, or the value cannot be updated or is not supported for this type of channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-180"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERRORE \_ evt \_ valore della proprietà del server di pubblicazione non valido \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="abf41-180"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-181">15024</span><span class="sxs-lookup"><span data-stu-id="abf41-181">15024</span></span>
</dt> <dt>



<span data-ttu-id="abf41-182">La proprietà del provider contiene un valore non valido.</span><span class="sxs-lookup"><span data-stu-id="abf41-182">The provider property contains a value that is not valid.</span></span> <span data-ttu-id="abf41-183">Il tipo del valore potrebbe non essere valido, il valore potrebbe non essere compreso nell'intervallo oppure il valore non può essere aggiornato o non è supportato per questo tipo di provider.</span><span class="sxs-lookup"><span data-stu-id="abf41-183">The value's type may not be valid, the value may be out of range, or the value cannot be updated or is not supported for this type of provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-184"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERRORE \_ \_ \_ non è possibile attivare il canale evt \_**</span><span class="sxs-lookup"><span data-stu-id="abf41-184"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERROR\_EVT\_CHANNEL\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-185">15025</span><span class="sxs-lookup"><span data-stu-id="abf41-185">15025</span></span>
</dt> <dt>



<span data-ttu-id="abf41-186">Non è stato possibile attivare il canale.</span><span class="sxs-lookup"><span data-stu-id="abf41-186">The channel failed to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-187"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERRORE \_ \_ filtro evt \_ troppo \_ complesso**</span><span class="sxs-lookup"><span data-stu-id="abf41-187"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERROR\_EVT\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-188">15026</span><span class="sxs-lookup"><span data-stu-id="abf41-188">15026</span></span>
</dt> <dt>



<span data-ttu-id="abf41-189">L'espressione XPath ha superato la complessità supportata.</span><span class="sxs-lookup"><span data-stu-id="abf41-189">The XPath expression exceeded supported complexity.</span></span> <span data-ttu-id="abf41-190">Semplificare l'espressione o suddividerla in due o più espressioni semplici.</span><span class="sxs-lookup"><span data-stu-id="abf41-190">Simplify the expression or split it into two or more simple expressions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-191"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERRORE \_ evt \_ messaggio \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="abf41-191"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERROR\_EVT\_MESSAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-192">15027</span><span class="sxs-lookup"><span data-stu-id="abf41-192">15027</span></span>
</dt> <dt>



<span data-ttu-id="abf41-193">La risorsa messaggio è presente, ma il messaggio non viene trovato nella stringa o nella tabella messaggi.</span><span class="sxs-lookup"><span data-stu-id="abf41-193">The message resource is present, but the message is not found in the string or message table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-194"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERRORE \_ evt \_ \_ ID messaggio \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="abf41-194"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERROR\_EVT\_MESSAGE\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-195">15028</span><span class="sxs-lookup"><span data-stu-id="abf41-195">15028</span></span>
</dt> <dt>



<span data-ttu-id="abf41-196">Impossibile trovare l'identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="abf41-196">The message identifier cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-197"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERRORE \_ evt \_ \_ inserimento valore non risolto \_**</span><span class="sxs-lookup"><span data-stu-id="abf41-197"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERROR\_EVT\_UNRESOLVED\_VALUE\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-198">15029</span><span class="sxs-lookup"><span data-stu-id="abf41-198">15029</span></span>
</dt> <dt>



<span data-ttu-id="abf41-199">Impossibile trovare la stringa di sostituzione per l'indice di inserimento.</span><span class="sxs-lookup"><span data-stu-id="abf41-199">The substitution string for the insert index cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-200"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERRORE \_ evt \_ \_ inserimento parametro non risolto \_**</span><span class="sxs-lookup"><span data-stu-id="abf41-200"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERROR\_EVT\_UNRESOLVED\_PARAMETER\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-201">15030</span><span class="sxs-lookup"><span data-stu-id="abf41-201">15030</span></span>
</dt> <dt>



<span data-ttu-id="abf41-202">Impossibile trovare la stringa di descrizione per il riferimento al parametro (%1).</span><span class="sxs-lookup"><span data-stu-id="abf41-202">The description string for parameter reference (%1) cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-203"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERRORE \_ evt \_ numero massimo di \_ inserimenti \_ raggiunti**</span><span class="sxs-lookup"><span data-stu-id="abf41-203"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERROR\_EVT\_MAX\_INSERTS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-204">15031</span><span class="sxs-lookup"><span data-stu-id="abf41-204">15031</span></span>
</dt> <dt>



<span data-ttu-id="abf41-205">È stato raggiunto il numero massimo di sostituzioni.</span><span class="sxs-lookup"><span data-stu-id="abf41-205">The maximum number of replacements has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-206"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERRORE \_ evt \_ \_ \_ Impossibile trovare la definizione dell'evento \_**</span><span class="sxs-lookup"><span data-stu-id="abf41-206"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERROR\_EVT\_EVENT\_DEFINITION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-207">15032</span><span class="sxs-lookup"><span data-stu-id="abf41-207">15032</span></span>
</dt> <dt>



<span data-ttu-id="abf41-208">Impossibile trovare la definizione dell'evento per l'identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="abf41-208">The event definition cannot be found for the event identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-209"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERRORE \_ nelle \_ \_ impostazioni locali del messaggio evt \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="abf41-209"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERROR\_EVT\_MESSAGE\_LOCALE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-210">15033</span><span class="sxs-lookup"><span data-stu-id="abf41-210">15033</span></span>
</dt> <dt>



<span data-ttu-id="abf41-211">La risorsa specifica delle impostazioni locali per il messaggio desiderato non è presente.</span><span class="sxs-lookup"><span data-stu-id="abf41-211">The locale-specific resource for the desired message is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-212"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERRORE \_ evt \_ versione \_ troppo \_ vecchia**</span><span class="sxs-lookup"><span data-stu-id="abf41-212"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERROR\_EVT\_VERSION\_TOO\_OLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-213">15034</span><span class="sxs-lookup"><span data-stu-id="abf41-213">15034</span></span>
</dt> <dt>



<span data-ttu-id="abf41-214">La risorsa è troppo vecchia per essere compatibile.</span><span class="sxs-lookup"><span data-stu-id="abf41-214">The resource is too old to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-215"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERRORE \_ evt \_ versione \_ troppo \_ nuova**</span><span class="sxs-lookup"><span data-stu-id="abf41-215"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERROR\_EVT\_VERSION\_TOO\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-216">15035</span><span class="sxs-lookup"><span data-stu-id="abf41-216">15035</span></span>
</dt> <dt>



<span data-ttu-id="abf41-217">La risorsa è troppo nuova per essere compatibile.</span><span class="sxs-lookup"><span data-stu-id="abf41-217">The resource is too new to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-218"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERRORE \_ evt \_ Impossibile \_ aprire il \_ canale \_ della \_ query**</span><span class="sxs-lookup"><span data-stu-id="abf41-218"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERROR\_EVT\_CANNOT\_OPEN\_CHANNEL\_OF\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-219">15036</span><span class="sxs-lookup"><span data-stu-id="abf41-219">15036</span></span>
</dt> <dt>



<span data-ttu-id="abf41-220">Non è possibile aprire il canale in corrispondenza dell'indice specificato della query.</span><span class="sxs-lookup"><span data-stu-id="abf41-220">The channel at the specified index of the query cannot be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-221"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERRORE \_ evt \_ Autore \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="abf41-221"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERROR\_EVT\_PUBLISHER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-222">15037</span><span class="sxs-lookup"><span data-stu-id="abf41-222">15037</span></span>
</dt> <dt>



<span data-ttu-id="abf41-223">Il provider è stato disabilitato e le relative risorse non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="abf41-223">The provider has been disabled and its resources are not available.</span></span> <span data-ttu-id="abf41-224">Questo problema può verificarsi quando il provider viene disinstallato o aggiornato.</span><span class="sxs-lookup"><span data-stu-id="abf41-224">This can occur when the provider is uninstalled or upgraded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="abf41-225"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERRORE \_ evt \_ filtro \_ non \_ \_ compreso nell'intervallo**</span><span class="sxs-lookup"><span data-stu-id="abf41-225"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERROR\_EVT\_FILTER\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf41-226">15038</span><span class="sxs-lookup"><span data-stu-id="abf41-226">15038</span></span>
</dt> <dt>



<span data-ttu-id="abf41-227">Tentativo di creare un tipo numerico non compreso nell'intervallo valido.</span><span class="sxs-lookup"><span data-stu-id="abf41-227">Attempted to create a numeric type that is outside of its valid range.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abf41-228">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abf41-228">Requirements</span></span>



| <span data-ttu-id="abf41-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="abf41-229">Requirement</span></span> | <span data-ttu-id="abf41-230">Valore</span><span class="sxs-lookup"><span data-stu-id="abf41-230">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="abf41-231">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abf41-231">Minimum supported client</span></span><br/> | <span data-ttu-id="abf41-232">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="abf41-232">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="abf41-233">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abf41-233">Minimum supported server</span></span><br/> | <span data-ttu-id="abf41-234">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="abf41-234">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="abf41-235">Intestazione</span><span class="sxs-lookup"><span data-stu-id="abf41-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="abf41-236"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="abf41-236"><dt>WinError.h</dt></span></span> </dl> |



 

 





