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
# <a name="windows-event-log-error-constants"></a>Costanti di errore nel registro eventi di Windows

Di seguito sono riportati i codici di errore definiti nel registro eventi di Windows.

<dl> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERRORE \_ evt \_ \_ percorso del canale non valido \_**
</dt> <dd> <dl> <dt>

15000
</dt> <dt>



Il percorso del canale specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERRORE \_ evt \_ query non valida \_**
</dt> <dd> <dl> <dt>

15001
</dt> <dt>



La query specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERRORE \_ evt \_ pubblicazione \_ metadati \_ non \_ trovati**
</dt> <dd> <dl> <dt>

15002
</dt> <dt>



Impossibile trovare i metadati del provider nella risorsa.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERRORE \_ evt \_ modello di evento \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

15003
</dt> <dt>



Il modello per la definizione di un evento non è stato trovato nella risorsa.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERRORE \_ evt \_ \_ nome dell'autore non valido \_**
</dt> <dd> <dl> <dt>

15004
</dt> <dt>



Il nome del provider specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERRORE \_ evt \_ \_ dati evento non validi \_**
</dt> <dd> <dl> <dt>

15005
</dt> <dt>



I dati dell'evento generati dal provider non sono compatibili con la definizione del modello di evento nel manifesto del provider.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERRORE \_ \_ canale evt \_ non \_ trovato**
</dt> <dd> <dl> <dt>

15007
</dt> <dt>



Impossibile trovare il canale specificato. Controllare la configurazione del canale.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERRORE \_ evt \_ \_ testo XML non valido \_**
</dt> <dd> <dl> <dt>

15008
</dt> <dt>



Il testo XML specificato non è ben formato. Per ulteriori informazioni, chiamare la funzione [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) .


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERRORE \_ evt \_ sottoscrizione \_ al \_ \_ canale diretto**
</dt> <dd> <dl> <dt>

15009
</dt> <dt>



Non è possibile sottoscrivere un canale analitico o di debug; gli eventi per un canale analitico o di debug passano direttamente a un file di log e non possono essere sottoscritti.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**errore \_ di \_ configurazione di evt \_**
</dt> <dd> <dl> <dt>

15010
</dt> <dt>



Errore di configurazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERRORE il \_ risultato della query evt non è \_ \_ \_ aggiornato**
</dt> <dd> <dl> <dt>

15011
</dt> <dt>



Il risultato della query non è valido. Questo problema può essere dovuto al fatto che il log è stato cancellato o spostato dopo la creazione del risultato della query. Rilasciare l'oggetto risultato della query ed eseguire nuovamente la query.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERRORE \_ il \_ risultato della query evt \_ \_ posizione non valida \_**
</dt> <dd> <dl> <dt>

15012
</dt> <dt>



Il cursore per il risultato della query non sta puntando a una posizione valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERRORE \_ evt \_ non \_ convalida \_ MSXML**
</dt> <dd> <dl> <dt>

15013
</dt> <dt>



Il parser MSXML registrato non supporta la convalida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERRORE \_ evt \_ filtro \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014
</dt> <dt>



Un'espressione può essere seguita da una modifica dell'operazione dell'ambito solo se l'espressione restituisce un set di nodi e non fa già parte di un'altra modifica dell'operazione dell'ambito.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERRORE \_ evt \_ filtro \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015
</dt> <dt>



Non è possibile eseguire un'operazione di passaggio da un termine che non rappresenta un set di elementi.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERRORE \_ evt \_ filtro \_ INVARG**
</dt> <dd> <dl> <dt>

15016
</dt> <dt>



Gli argomenti sul lato sinistro di un operatore binario devono essere attributi, nodi o variabili e gli argomenti sul lato destro devono essere costanti.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERRORE \_ evt \_ filtro \_ INVTEST**
</dt> <dd> <dl> <dt>

15017
</dt> <dt>



Un'operazione Step deve coinvolgere un test di nodo o, nel caso di un predicato, un'espressione algebrica sulla quale testare ogni nodo nel set di nodi identificato dal set di nodi precedente può essere valutato.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERRORE \_ evt \_ filtro \_ INVTYPE**
</dt> <dd> <dl> <dt>

15018
</dt> <dt>



Questo tipo di dati non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERRORE \_ evt \_ filtro \_ PARSEERR**
</dt> <dd> <dl> <dt>

15019
</dt> <dt>



Si è verificato un errore di sintassi nella posizione specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERRORE \_ evt \_ filtro \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020
</dt> <dt>



Questo operatore non è supportato da questa implementazione del filtro.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERRORE \_ evt \_ filtro \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021
</dt> <dt>



Il token rilevato è imprevisto.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERRORE \_ evt \_ \_ operazione non \_ valida \_ su \_ canale diretto abilitato \_**
</dt> <dd> <dl> <dt>

15022
</dt> <dt>



Non è possibile eseguire l'operazione richiesta su un canale analitico o di debug abilitato. È necessario disabilitare il canale prima di eseguire l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERRORE \_ evt \_ \_ valore della \_ proprietà del canale non valido \_**
</dt> <dd> <dl> <dt>

15023
</dt> <dt>



La proprietà Channel contiene un valore non valido. Il tipo del valore potrebbe non essere valido, il valore potrebbe non essere compreso nell'intervallo oppure il valore non può essere aggiornato o non è supportato per questo tipo di canale.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERRORE \_ evt \_ valore della proprietà del server di pubblicazione non valido \_ \_ \_**
</dt> <dd> <dl> <dt>

15024
</dt> <dt>



La proprietà del provider contiene un valore non valido. Il tipo del valore potrebbe non essere valido, il valore potrebbe non essere compreso nell'intervallo oppure il valore non può essere aggiornato o non è supportato per questo tipo di provider.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERRORE \_ \_ \_ non è possibile attivare il canale evt \_**
</dt> <dd> <dl> <dt>

15025
</dt> <dt>



Non è stato possibile attivare il canale.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERRORE \_ \_ filtro evt \_ troppo \_ complesso**
</dt> <dd> <dl> <dt>

15026
</dt> <dt>



L'espressione XPath ha superato la complessità supportata. Semplificare l'espressione o suddividerla in due o più espressioni semplici.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERRORE \_ evt \_ messaggio \_ non \_ trovato**
</dt> <dd> <dl> <dt>

15027
</dt> <dt>



La risorsa messaggio è presente, ma il messaggio non viene trovato nella stringa o nella tabella messaggi.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERRORE \_ evt \_ \_ ID messaggio \_ non \_ trovato**
</dt> <dd> <dl> <dt>

15028
</dt> <dt>



Impossibile trovare l'identificatore del messaggio.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERRORE \_ evt \_ \_ inserimento valore non risolto \_**
</dt> <dd> <dl> <dt>

15029
</dt> <dt>



Impossibile trovare la stringa di sostituzione per l'indice di inserimento.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERRORE \_ evt \_ \_ inserimento parametro non risolto \_**
</dt> <dd> <dl> <dt>

15030
</dt> <dt>



Impossibile trovare la stringa di descrizione per il riferimento al parametro (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERRORE \_ evt \_ numero massimo di \_ inserimenti \_ raggiunti**
</dt> <dd> <dl> <dt>

15031
</dt> <dt>



È stato raggiunto il numero massimo di sostituzioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERRORE \_ evt \_ \_ \_ Impossibile trovare la definizione dell'evento \_**
</dt> <dd> <dl> <dt>

15032
</dt> <dt>



Impossibile trovare la definizione dell'evento per l'identificatore dell'evento.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERRORE \_ nelle \_ \_ impostazioni locali del messaggio evt \_ non \_ trovato**
</dt> <dd> <dl> <dt>

15033
</dt> <dt>



La risorsa specifica delle impostazioni locali per il messaggio desiderato non è presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERRORE \_ evt \_ versione \_ troppo \_ vecchia**
</dt> <dd> <dl> <dt>

15034
</dt> <dt>



La risorsa è troppo vecchia per essere compatibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERRORE \_ evt \_ versione \_ troppo \_ nuova**
</dt> <dd> <dl> <dt>

15035
</dt> <dt>



La risorsa è troppo nuova per essere compatibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERRORE \_ evt \_ Impossibile \_ aprire il \_ canale \_ della \_ query**
</dt> <dd> <dl> <dt>

15036
</dt> <dt>



Non è possibile aprire il canale in corrispondenza dell'indice specificato della query.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERRORE \_ evt \_ Autore \_ disabilitato**
</dt> <dd> <dl> <dt>

15037
</dt> <dt>



Il provider è stato disabilitato e le relative risorse non sono disponibili. Questo problema può verificarsi quando il provider viene disinstallato o aggiornato.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERRORE \_ evt \_ filtro \_ non \_ \_ compreso nell'intervallo**
</dt> <dd> <dl> <dt>

15038
</dt> <dt>



Tentativo di creare un tipo numerico non compreso nell'intervallo valido.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



 

 





