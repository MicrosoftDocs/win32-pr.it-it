---
title: Codici di errore WFP (Winerror.h)
description: (WFP) codici di errore specifici.
ms.assetid: 11f3085a-f044-4a78-b47a-59b9086562bf
topic_type:
- apiref
api_name:
- FWP_E_CALLOUT_NOT_FOUND
- FWP_E_CONDITION_NOT_FOUND
- FWP_E_FILTER_NOT_FOUND
- FWP_E_LAYER_NOT_FOUND
- FWP_E_PROVIDER_NOT_FOUND
- FWP_E_PROVIDER_CONTEXT_NOT_FOUND
- FWP_E_SUBLAYER_NOT_FOUND
- FWP_E_NOT_FOUND
- FWP_E_ALREADY_EXISTS
- FWP_E_IN_USE
- FWP_E_DYNAMIC_SESSION_IN_PROGRESS
- FWP_E_WRONG_SESSION
- FWP_E_NO_TXN_IN_PROGRESS
- FWP_E_TXN_IN_PROGRESS
- FWP_E_TXN_ABORTED
- FWP_E_SESSION_ABORTED
- FWP_E_INCOMPATIBLE_TXN
- FWP_E_TIMEOUT
- FWP_E_NET_EVENTS_DISABLED
- FWP_E_INCOMPATIBLE_LAYER
- FWP_E_KM_CLIENTS_ONLY
- FWP_E_LIFETIME_MISMATCH
- FWP_E_BUILTIN_OBJECT
- FWP_E_TOO_MANY_CALLOUTS
- FWP_E_NOTIFICATION_DROPPED
- FWP_E_TRAFFIC_MISMATCH
- FWP_E_INCOMPATIBLE_SA_STATE
- FWP_E_NULL_POINTER
- FWP_E_INVALID_ENUMERATOR
- FWP_E_INVALID_FLAGS
- FWP_E_INVALID_NET_MASK
- FWP_E_INVALID_RANGE
- FWP_E_INVALID_INTERVAL
- FWP_E_ZERO_LENGTH_ARRAY
- FWP_E_NULL_DISPLAY_NAME
- FWP_E_INVALID_ACTION_TYPE
- FWP_E_INVALID_WEIGHT
- FWP_E_MATCH_TYPE_MISMATCH
- FWP_E_TYPE_MISMATCH
- FWP_E_OUT_OF_BOUNDS
- FWP_E_RESERVED
- FWP_E_DUPLICATE_CONDITION
- FWP_E_DUPLICATE_KEYMOD
- FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER
- FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT
- FWP_E_INCOMPATIBLE_AUTH_METHOD
- FWP_E_INCOMPATIBLE_DH_GROUP
- FWP_E_EM_NOT_SUPPORTED
- FWP_E_NEVER_MATCH
- FWP_E_PROVIDER_CONTEXT_MISMATCH
- FWP_E_INVALID_PARAMETER
- FWP_E_TOO_MANY_SUBLAYERS
- FWP_E_CALLOUT_NOTIFICATION_FAILED
- FWP_E_INVALID_AUTH_TRANSFORM
- FWP_E_INVALID_CIPHER_TRANSFORM
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a0e7ee1ab0364a31f136f0c0cdbf87f459225b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477836"
---
# <a name="wfp-error-codes"></a>Codici di errore di WFP

I codici di errore specifici di Windows Filtering Platform (WFP) sono i seguenti.

<dl> <dt>

<span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**\_CALLOUT FWP \_ E \_ non \_ trovato**
</dt> <dd> <dl> <dt>

0x80320001
</dt> <dt>



Il callout non esiste.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**\_condizione FWP \_ E \_ non \_ trovata**
</dt> <dd> <dl> <dt>

0x80320002
</dt> <dt>



La condizione di filtro non esiste.


</dt> </dl> </dd> <dt>

<span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**\_filtro FWP \_ E \_ non \_ trovato**
</dt> <dd> <dl> <dt>

0x80320003
</dt> <dt>



Il filtro non esiste.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**livello di FWP \_ E \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

0x80320004
</dt> <dt>



Il livello non esiste.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**il \_ provider di FWP E \_ non è stato \_ \_ trovato**
</dt> <dd> <dl> <dt>

0x80320005
</dt> <dt>



Il provider non esiste.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**il \_ contesto del provider FWP E \_ non è stato \_ \_ \_ trovato**
</dt> <dd> <dl> <dt>

0x80320006
</dt> <dt>



Il contesto del provider non esiste.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**sottolivello di FWP \_ E \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

0x80320007
</dt> <dt>



Il sottolivello non esiste.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**FWP \_ E \_ non \_ trovato**
</dt> <dd> <dl> <dt>

0x80320008
</dt> <dt>



L'oggetto non esiste.

Le [funzioni \* IPsecSaContext](fwp-ipsec-functions.md) restituiscono questo errore se l'ID del contesto SA non viene trovato.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**FWP \_ E \_ \_ esiste già**
</dt> <dd> <dl> <dt>

0x80320009
</dt> <dt>



Un oggetto con tale GUID o LUID esiste già.


</dt> </dl> </dd> <dt>

<span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**FWP \_ E \_ in \_ uso**
</dt> <dd> <dl> <dt>

0x8032000A
</dt> <dt>



Gli altri oggetti fanno riferimento all'oggetto, pertanto non può essere eliminato.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**\_ \_ sessione dinamica FWP \_ E \_ in \_ corso**
</dt> <dd> <dl> <dt>

0x8032000B
</dt> <dt>



La chiamata non è consentita all'interno di una sessione dinamica.


</dt> </dl> </dd> <dt>

<span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**FWP \_ E \_ sessione errata \_**
</dt> <dd> <dl> <dt>

0x8032000C
</dt> <dt>



La chiamata è stata eseguita dalla sessione errata, quindi non può essere completata.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**FWP \_ E \_ nessun \_ transazione \_ in \_ corso**
</dt> <dd> <dl> <dt>

0x8032000D
</dt> <dt>



La chiamata deve essere eseguita dall'interno di una transazione esplicita.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**FWP \_ E \_ transazione \_ in \_ corso**
</dt> <dd> <dl> <dt>

0x8032000E
</dt> <dt>



La chiamata non è consentita all'interno di una transazione esplicita.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**FWP \_ E \_ transazione \_ interrotti**
</dt> <dd> <dl> <dt>

0x8032000F
</dt> <dt>



La transazione esplicita è stata annullata forzatamente.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**\_sessione FWP \_ E \_ interrotta**
</dt> <dd> <dl> <dt>

0x80320010
</dt> <dt>



La sessione è stata annullata.

È necessario chiudere l'handle di sessione chiamando [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0), anche se non è più valido. in caso contrario, lo stato del lato client verrà perso. È necessario creare una nuova sessione chiamando [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**\_transazione FWP E \_ incompatibile \_**
</dt> <dd> <dl> <dt>

0x80320011
</dt> <dt>



La chiamata non è consentita all'interno di una transazione di sola lettura.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**FWP \_ E \_ timeout**
</dt> <dd> <dl> <dt>

0x80320012
</dt> <dt>



Timeout della chiamata durante l'attesa dell'acquisizione del blocco della transazione.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**\_eventi FWP \_ E \_ net \_ disabilitati**
</dt> <dd> <dl> <dt>

0x80320013
</dt> <dt>



La raccolta di eventi di diagnostica di rete è disabilitata.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**\_livello FWP E \_ incompatibile \_**
</dt> <dd> <dl> <dt>

0x80320014
</dt> <dt>



L'operazione non è supportata dal livello specificato.


</dt> </dl> </dd> <dt>

<span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**\_ \_ \_ solo client FWP E \_ km**
</dt> <dd> <dl> <dt>

0x80320015
</dt> <dt>



La chiamata è consentita solo per i chiamanti in modalità kernel.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**FWP \_ E \_ durata non \_ corrispondenti**
</dt> <dd> <dl> <dt>

0x80320016
</dt> <dt>



La chiamata ha tentato di associare due oggetti con durate incompatibili.

Per ulteriori informazioni sulla durata degli oggetti e sull'associazione di oggetti, vedere [gestione](object-management.md) degli oggetti.


</dt> </dl> </dd> <dt>

<span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**\_oggetto FWP E \_ Builtin \_**
</dt> <dd> <dl> <dt>

0x80320017
</dt> <dt>



L'oggetto è incorporato, pertanto non può essere eliminato.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**FWP \_ E \_ troppi \_ \_ callout**
</dt> <dd> <dl> <dt>

0x80320018
</dt> <dt>



È stato raggiunto il numero massimo di callout.

Al massimo, i callout 100.000 possono essere registrati nello stesso momento.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**notifica di FWP \_ E \_ \_ rilasciata**
</dt> <dd> <dl> <dt>

0x80320019
</dt> <dt>



Non è stato possibile recapitare una notifica perché una coda di messaggi è alla capacità massima.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**FWP \_ E \_ traffico non \_ corrispondenti**
</dt> <dd> <dl> <dt>

0x8032001A
</dt> <dt>



I parametri del traffico di rete non corrispondono a quelli per il contesto dell'associazione di sicurezza.

[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) può essere chiamato più volte, ma il chiamante deve specificare lo stesso [**\_ TRAFFIC0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) ogni volta. Questo errore viene restituito se una chiamata successiva fornisce un **\_ TRAFFIC0 IPSec** diverso.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**\_stato sa FWP E \_ incompatibile \_ \_**
</dt> <dd> <dl> <dt>

0x8032001B
</dt> <dt>



La chiamata non è consentita per lo stato dell'associazione di sicurezza (SA) corrente.

Le funzioni di contesto SA devono essere chiamate in un ordine specifico:

-   [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)
-   [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)
-   [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)
-   [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)

Questo errore viene restituito se viene chiamato fuori ordine.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**FWP \_ E \_ \_ puntatore null**
</dt> <dd> <dl> <dt>

0x8032001C
</dt> <dt>



Un puntatore obbligatorio è null.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**\_ \_ enumeratore FWP E non valido \_**
</dt> <dd> <dl> <dt>

0x8032001D
</dt> <dt>



Un valore di enumeratore in una struttura non è compreso nell'intervallo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**\_flag FWP E \_ non validi \_**
</dt> <dd> <dl> <dt>

0x8032001E
</dt> <dt>



Il campo dei flag contiene un valore non valido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**FWP \_ E \_ \_ net \_ mask non valido**
</dt> <dd> <dl> <dt>

0x8032001F
</dt> <dt>



Una network mask non è valida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**FWP \_ E \_ intervallo non valido \_**
</dt> <dd> <dl> <dt>

0x80320020
</dt> <dt>



Una [**struttura \_ RANGE0 di FWP**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0) non è valida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**FWP \_ E \_ intervallo non valido \_**
</dt> <dd> <dl> <dt>

0x80320021
</dt> <dt>



L'intervallo di tempo non è valido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**FWP \_ E \_ \_ matrice di lunghezza zero \_**
</dt> <dd> <dl> <dt>

0x80320022
</dt> <dt>



Una matrice che deve contenere almeno un elemento ha lunghezza zero.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**\_ \_ \_ nome visualizzato FWP E \_ null**
</dt> <dd> <dl> <dt>

0x80320023
</dt> <dt>



Il campo **displayData.Name** non può essere null.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**FWP \_ E \_ \_ tipo di azione non valido \_**
</dt> <dd> <dl> <dt>

0x80320024
</dt> <dt>



Il tipo di azione non è uno dei tipi di azione consentiti per un filtro.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**FWP \_ E \_ peso non valido \_**
</dt> <dd> <dl> <dt>

0x80320025
</dt> <dt>



Il peso del filtro non è valido.

Per ulteriori informazioni, vedere l' [assegnazione del peso del filtro](filter-weight-assignment.md) .


</dt> </dl> </dd> <dt>

<span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**tipo di corrispondenza di FWP \_ E non \_ \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

0x80320026
</dt> <dt>



Una condizione di filtro contiene un tipo di corrispondenza che non è compatibile con gli operandi.

Per ulteriori informazioni, vedere [**\_ \_ tipo di corrispondenza FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) .


</dt> </dl> </dd> <dt>

<span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**tipo di FWP \_ E non \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

0x80320027
</dt> <dt>



Una struttura [**FWP \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0) o una [**struttura \_ \_ VALUE0 di FWPM Condition**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0) è di tipo errato.


</dt> </dl> </dd> <dt>

<span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**FWP \_ E \_ fuori \_ \_ limite**
</dt> <dd> <dl> <dt>

0x80320028
</dt> <dt>



Un valore integer non è compreso nell'intervallo consentito.


</dt> </dl> </dd> <dt>

<span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**FWP \_ E \_ riservato**
</dt> <dd> <dl> <dt>

0x80320029
</dt> <dt>



Un campo riservato è diverso da zero.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**FWP \_ E \_ condizione duplicata \_**
</dt> <dd> <dl> <dt>

0x8032002A
</dt> <dt>



Un filtro non può contenere più condizioni che operano su un singolo campo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**\_KEYMOD FWP E \_ duplicati \_**
</dt> <dd> <dl> <dt>

0x8032002B
</dt> <dt>



Un criterio non può contenere lo stesso modulo di trasparenza più di una volta.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**\_azione FWP \_ E \_ incompatibile \_ con il \_ livello**
</dt> <dd> <dl> <dt>

0x8032002C
</dt> <dt>



Il tipo di azione non è compatibile con il livello.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**\_azione FWP \_ E \_ incompatibile \_ con il \_ sottolivello**
</dt> <dd> <dl> <dt>

0x8032002D
</dt> <dt>



Il tipo di azione non è compatibile con il sottolivello.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**\_ \_ contesto di FWP E \_ incompatibile \_ con il \_ livello**
</dt> <dd> <dl> <dt>

0x8032002E
</dt> <dt>



Il contesto non elaborato o il contesto del provider non è compatibile con il livello.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**\_ \_ contesto di FWP E \_ incompatibile \_ con il \_ CALLOUT**
</dt> <dd> <dl> <dt>

0x8032002F
</dt> <dt>



Il contesto non elaborato o il contesto del provider non è compatibile con il callout.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**FWP \_ E \_ metodo di \_ autenticazione incompatibile \_**
</dt> <dd> <dl> <dt>

0x80320030
</dt> <dt>



Il metodo di autenticazione non è compatibile con il tipo di criteri.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**FWP \_ E \_ \_ gruppo DH incompatibile \_**
</dt> <dd> <dl> <dt>

0x80320031L
</dt> <dt>



Il gruppo di Diffie-Hellman non è compatibile con il tipo di criteri.


</dt> </dl> </dd> <dt>

<span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**FWP \_ E \_ em \_ non \_ supportati**
</dt> <dd> <dl> <dt>

0x80320032
</dt> <dt>



Un criterio IKE non può contenere criteri per la modalità estesa.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**FWP \_ E \_ non \_ corrispondono mai**
</dt> <dd> <dl> <dt>

0x80320033
</dt> <dt>



Il modello di enumerazione o la sottoscrizione non corrisponderà mai ad alcun oggetto.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**contesto del provider di FWP \_ E non \_ \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

0x80320034
</dt> <dt>



Il tipo del contesto del provider non è corretto.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**\_parametro FWP E \_ non valido \_**
</dt> <dd> <dl> <dt>

0x80320035
</dt> <dt>



Parametro non corretto.

Possibili cause dell'errore:

-   [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) è stato chiamato senza impostare il flag **FWPM \_ tunnel \_ flag \_ Point \_ su \_ Point** e con condizioni diverse dall'indirizzo locale/remoto.
-   Stringa Unicode non valida o stringa Unicode contenente caratteri non stampabili.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**FWP \_ E \_ troppi \_ \_ sottolivelli**
</dt> <dd> <dl> <dt>

0x80320036
</dt> <dt>



È stato raggiunto il numero massimo di sottolivelli.

WFP supporta al massimo 2 6 sottolivelli.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**\_notifica FWP \_ E \_ CALLOUT \_ non riuscita**
</dt> <dd> <dl> <dt>

0x80320037
</dt> <dt>



La funzione di notifica per un callout ha restituito un errore.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**FWP \_ E \_ \_ trasformazione autenticazione non valida \_**
</dt> <dd> <dl> <dt>

0x80320038
</dt> <dt>



Trasformazione autenticazione IPsec non valida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**FWP \_ E \_ \_ trasformazione di crittografia non valida \_**
</dt> <dd> <dl> <dt>

0x80320039
</dt> <dt>



Trasformazione crittografia IPsec non valida.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Winerror. h</dt> </dl> |



 

 





