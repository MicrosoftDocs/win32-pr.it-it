---
title: Windows Costanti di errore del registro eventi (WinError.h)
description: Di seguito sono riportati i codici di errore Windows registro eventi.
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
ms.openlocfilehash: e0f6f0bd3e2805c02dad78c064b56a443bfbb596cf42f25e9b52ac7ba584f123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031941"
---
# <a name="windows-event-log-error-constants"></a>Windows Costanti di errore del registro eventi

Di seguito sono riportati i codici di errore Windows registro eventi.

<dl> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERRORE \_ EVT \_ PERCORSO CANALE NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

15000
</dt> <dt>



Il percorso del canale specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERRORE \_ EVT \_ QUERY NON \_ VALIDA**
</dt> <dd> <dl> <dt>

15001
</dt> <dt>



La query specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERRORE \_ METADATI DEL SERVER DI PUBBLICAZIONE EVT NON \_ \_ \_ \_ TROVATI**
</dt> <dd> <dl> <dt>

15002
</dt> <dt>



Impossibile trovare i metadati del provider nella risorsa.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERRORE \_ DEL MODELLO DI EVENTO EVT NON \_ \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

15003
</dt> <dt>



Impossibile trovare il modello per una definizione di evento nella risorsa.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERRORE \_ EVT \_ NOME SERVER DI PUBBLICAZIONE NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

15004
</dt> <dt>



Il nome del provider specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERRORE \_ EVT \_ DATI EVENTO NON \_ \_ VALIDI**
</dt> <dd> <dl> <dt>

15005
</dt> <dt>



I dati dell'evento generati dal provider non sono compatibili con la definizione del modello di evento nel manifesto del provider.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERRORE \_ CANALE EVT \_ NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

15007
</dt> <dt>



Impossibile trovare il canale specificato. Controllare la configurazione del canale.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERRORE \_ EVT \_ TESTO XML IN FORMATO NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

15008
</dt> <dt>



Il formato del testo XML specificato non è corretto. Per altre informazioni, chiamare [**la funzione EvtGetExtendedStatus.**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus)


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERRORE \_ DELLA SOTTOSCRIZIONE EVT \_ AL CANALE \_ \_ \_ DIRETTO**
</dt> <dd> <dl> <dt>

15009
</dt> <dt>



Non è possibile sottoscrivere un canale analitico o di debug. Gli eventi per un canale analitico o di debug passano direttamente a un file di log e non possono essere sottoscritti.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**ERRORE \_ DI CONFIGURAZIONE \_ EVT \_**
</dt> <dd> <dl> <dt>

15010
</dt> <dt>



Errore di configurazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERRORE \_ EVT \_ QUERY RESULT \_ \_ STALE**
</dt> <dd> <dl> <dt>

15011
</dt> <dt>



Il risultato della query non è valido. Il problema potrebbe essere dovuto alla ripulita o al roll over del log dopo la creazione del risultato della query. Rilasciare l'oggetto risultato della query e riemettere la query.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERRORE \_ DI POSIZIONE NON VALIDA DEL RISULTATO DELLA QUERY EVT \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

15012
</dt> <dt>



Il cursore per il risultato della query non punta a una posizione valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR \_ EVT \_ NON \_ VALIDATING \_ MSXML**
</dt> <dd> <dl> <dt>

15013
</dt> <dt>



Il parser MSXML non supporta la convalida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR \_ EVT \_ FILTER \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014
</dt> <dt>



Un'espressione può essere seguita da un'operazione di modifica dell'ambito solo se l'espressione restituisce un set di nodi e non fa già parte di un'altra operazione di modifica dell'ambito.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR \_ EVT \_ FILTER \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015
</dt> <dt>



Impossibile eseguire un'operazione di passaggio da un termine che non rappresenta un set di elementi.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERRORE \_ EVT \_ FILTER \_ INVARG**
</dt> <dd> <dl> <dt>

15016
</dt> <dt>



Gli argomenti a sinistra di un operatore binario devono essere attributi, nodi o variabili e gli argomenti a destra devono essere costanti.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERRORE \_ EVT \_ FILTER \_ INVTEST**
</dt> <dd> <dl> <dt>

15017
</dt> <dt>



Un'operazione di passaggio deve coinvolgere un test del nodo o, nel caso di un predicato, un'espressione algebrica rispetto alla quale testare ogni nodo nel set di nodi identificato dal set di nodi precedente può essere valutata.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERRORE \_ EVT \_ FILTER \_ INVTYPE**
</dt> <dd> <dl> <dt>

15018
</dt> <dt>



Questo tipo di dati non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERRORE \_ EVT \_ FILTER \_ PARSEERR**
</dt> <dd> <dl> <dt>

15019
</dt> <dt>



Si è verificato un errore di sintassi nella posizione specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERRORE \_ EVT \_ FILTER \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020
</dt> <dt>



Questo operatore non è supportato da questa implementazione del filtro.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERRORE \_ EVT \_ FILTER \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021
</dt> <dt>



Il token rilevato è imprevisto.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERRORE \_ EVT \_ INVALID OPERATION OVER ENABLED DIRECT \_ \_ \_ \_ \_ CHANNEL**
</dt> <dd> <dl> <dt>

15022
</dt> <dt>



L'operazione richiesta non può essere eseguita su un canale analitico o di debug abilitato. È necessario disabilitare il canale prima di eseguire l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERRORE \_ EVT \_ VALORE PROPRIETÀ CANALE NON \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

15023
</dt> <dt>



La proprietà del canale contiene un valore non valido. Il tipo del valore potrebbe non essere valido, il valore potrebbe non essere compreso nell'intervallo oppure il valore non può essere aggiornato o non è supportato per questo tipo di canale.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERRORE \_ EVT \_ VALORE PROPRIETÀ SERVER DI PUBBLICAZIONE NON \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

15024
</dt> <dt>



La proprietà del provider contiene un valore non valido. Il tipo del valore potrebbe non essere valido, il valore potrebbe non essere compreso nell'intervallo oppure il valore non può essere aggiornato o non è supportato per questo tipo di provider.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERRORE \_ DURANTE L'ATTIVAZIONE DEL CANALE EVT \_ \_ \_**
</dt> <dd> <dl> <dt>

15025
</dt> <dt>



L'attivazione del canale non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERRORE \_ FILTRO EVT \_ TROPPO \_ \_ COMPLESSO**
</dt> <dd> <dl> <dt>

15026
</dt> <dt>



L'espressione XPath ha superato la complessità supportata. Semplificare l'espressione o dividerla in due o più espressioni semplici.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**MESSAGGIO \_ DI ERRORE EVT \_ NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

15027
</dt> <dt>



La risorsa messaggio è presente, ma il messaggio non viene trovato nella stringa o nella tabella dei messaggi.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERRORE \_ ID MESSAGGIO EVT \_ NON \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

15028
</dt> <dt>



Impossibile trovare l'identificatore del messaggio.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERRORE \_ EVT \_ UNRESOLVED \_ VALUE \_ INSERT**
</dt> <dd> <dl> <dt>

15029
</dt> <dt>



Impossibile trovare la stringa di sostituzione per l'indice di inserimento.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERRORE \_ EVT \_ UNRESOLVED \_ PARAMETER \_ INSERT**
</dt> <dd> <dl> <dt>

15030
</dt> <dt>



Impossibile trovare la stringa di descrizione per il riferimento al parametro (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERRORE \_ EVT \_ MAX \_ INSERTS \_ REACHED**
</dt> <dd> <dl> <dt>

15031
</dt> <dt>



È stato raggiunto il numero massimo di sostituzioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERRORE \_ DI DEFINIZIONE DELL'EVENTO EVT \_ \_ NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

15032
</dt> <dt>



Impossibile trovare la definizione dell'evento per l'identificatore dell'evento.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERRORE \_ DELLE IMPOSTAZIONI LOCALI DEL MESSAGGIO \_ \_ EVT NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

15033
</dt> <dt>



La risorsa specifica delle impostazioni locali per il messaggio desiderato non è presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERRORE \_ VERSIONE EVT \_ TROPPO \_ \_ VECCHIA**
</dt> <dd> <dl> <dt>

15034
</dt> <dt>



La risorsa è troppo vecchia per essere compatibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERRORE \_ VERSIONE EVT \_ TROPPO \_ \_ NUOVA**
</dt> <dd> <dl> <dt>

15035
</dt> <dt>



La risorsa è troppo nuova per essere compatibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERRORE \_ EVT: \_ IMPOSSIBILE APRIRE IL CANALE DELLA \_ \_ \_ \_ QUERY**
</dt> <dd> <dl> <dt>

15036
</dt> <dt>



Impossibile aprire il canale in corrispondenza dell'indice specificato della query.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERRORE \_ DEL SERVER DI PUBBLICAZIONE EVT \_ \_ DISABILITATO**
</dt> <dd> <dl> <dt>

15037
</dt> <dt>



Il provider è stato disabilitato e le relative risorse non sono disponibili. Ciò può verificarsi quando il provider viene disinstallato o aggiornato.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**FILTRO \_ EVT \_ DI ERRORE NON COMPRESO \_ \_ \_ NELL'INTERVALLO**
</dt> <dd> <dl> <dt>

15038
</dt> <dt>



Tentativo di creare un tipo numerico non compreso nell'intervallo valido.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Winerror</dt> </dl> |



 

 





