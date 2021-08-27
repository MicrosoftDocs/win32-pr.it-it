---
title: Codici di errore WFP (Winerror.h)
description: Codici di errore specifici (WFP).
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
ms.openlocfilehash: 21550e0c8872f0d0f8c067b38044a946f10f452d06ca213dea414d34756ce7ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083201"
---
# <a name="wfp-error-codes"></a>Codici di errore WFP

Windows I codici di errore specifici di Piattaforma filtro (WFP) sono i seguenti.

<dl> <dt>

<span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**CALLOUT \_ E \_ FWP NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

0x80320001
</dt> <dt>



Il callout non esiste.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**CONDIZIONE \_ E FWP \_ \_ NON \_ TROVATA**
</dt> <dd> <dl> <dt>

0x80320002
</dt> <dt>



La condizione di filtro non esiste.


</dt> </dl> </dd> <dt>

<span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**FILTRO \_ E FWP \_ \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

0x80320003
</dt> <dt>



Il filtro non esiste.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**LIVELLO \_ E FWP \_ \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

0x80320004
</dt> <dt>



Il livello non esiste.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**PROVIDER \_ E FWP \_ \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

0x80320005
</dt> <dt>



Il provider non esiste.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**CONTESTO \_ DEL PROVIDER EWP \_ \_ NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

0x80320006
</dt> <dt>



Il contesto del provider non esiste.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**\_SUBLAYER E \_ FWP NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

0x80320007
</dt> <dt>



Il livello secondario non esiste.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**FWP \_ E \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

0x80320008
</dt> <dt>



L'oggetto non esiste.

Le [funzioni IPsecSaContext \* ](fwp-ipsec-functions.md) restituiscono questo errore se l'ID di contesto sa non viene trovato.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**FWP \_ E \_ ESISTE \_ GIÀ**
</dt> <dd> <dl> <dt>

0x80320009
</dt> <dt>



Esiste già un oggetto con tale GUID o LUID.


</dt> </dl> </dd> <dt>

<span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**FWP \_ E \_ IN \_ USO**
</dt> <dd> <dl> <dt>

0x8032000A
</dt> <dt>



L'oggetto fa riferimento ad altri oggetti, quindi non può essere eliminato.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**SESSIONE \_ DINAMICA FWP E \_ \_ IN \_ \_ CORSO**
</dt> <dd> <dl> <dt>

0x8032000B
</dt> <dt>



La chiamata non è consentita dall'interno di una sessione dinamica.


</dt> </dl> </dd> <dt>

<span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**FWP \_ E \_ SESSIONE ERRATA \_**
</dt> <dd> <dl> <dt>

0x8032000C
</dt> <dt>



La chiamata è stata effettuata dalla sessione errata, quindi non può essere completata.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**FWP \_ E \_ NO \_ TXN \_ IN \_ CORSO**
</dt> <dd> <dl> <dt>

0x8032000D
</dt> <dt>



La chiamata deve essere effettuata dall'interno di una transazione esplicita.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**FWP \_ E \_ TXN \_ IN \_ CORSO**
</dt> <dd> <dl> <dt>

0x8032000E
</dt> <dt>



La chiamata non è consentita dall'interno di una transazione esplicita.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**FWP \_ E \_ TXN \_ INTERROTTO**
</dt> <dd> <dl> <dt>

0x8032000F
</dt> <dt>



La transazione esplicita è stata annullata forzatamente.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**SESSIONE \_ E FWP \_ \_ INTERROTTA**
</dt> <dd> <dl> <dt>

0x80320010
</dt> <dt>



La sessione è stata annullata.

L'handle di sessione deve essere chiuso chiamando [**FwpmEngineClose0,**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0)anche se non è più valido. In caso contrario, lo stato sul lato client verrà persa. È necessario creare una nuova sessione chiamando [**FwpmEngineOpen0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**\_ \_ TXN INCOMPATIBILE \_ CON FWP E**
</dt> <dd> <dl> <dt>

0x80320011
</dt> <dt>



La chiamata non è consentita dall'interno di una transazione di sola lettura.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**FWP \_ E \_ TIMEOUT**
</dt> <dd> <dl> <dt>

0x80320012
</dt> <dt>



Timeout della chiamata durante l'attesa dell'acquisizione del blocco della transazione.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**EVENTI \_ FWP E \_ NET \_ \_ DISABILITATI**
</dt> <dd> <dl> <dt>

0x80320013
</dt> <dt>



La raccolta di eventi di diagnostica di rete è disabilitata.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**LIVELLO \_ FWP E \_ \_ INCOMPATIBILE**
</dt> <dd> <dl> <dt>

0x80320014
</dt> <dt>



L'operazione non è supportata dal livello specificato.


</dt> </dl> </dd> <dt>

<span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**SOLO \_ CLIENT FWP E \_ KM \_ \_**
</dt> <dd> <dl> <dt>

0x80320015
</dt> <dt>



La chiamata è consentita solo per i chiamanti in modalità kernel.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**MANCATA \_ CORRISPONDENZA DELLA DURATA DI FWP E \_ \_**
</dt> <dd> <dl> <dt>

0x80320016
</dt> <dt>



La chiamata ha tentato di associare due oggetti a durate incompatibili.

Per [altre informazioni sulla durata e](object-management.md) sull'associazione degli oggetti, vedere Gestione oggetti.


</dt> </dl> </dd> <dt>

<span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**OGGETTO \_ INCORPORATO FWP E \_ \_**
</dt> <dd> <dl> <dt>

0x80320017
</dt> <dt>



L'oggetto è incorporato, quindi non può essere eliminato.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**NUMERO DI \_ \_ \_ CALLOUT FWP E \_ TROPPI**
</dt> <dd> <dl> <dt>

0x80320018
</dt> <dt>



È stato raggiunto il numero massimo di callout.

Al massimo, è possibile registrare 100.000 callout contemporaneamente.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**NOTIFICA \_ FWP E \_ \_ ELIMINATA**
</dt> <dd> <dl> <dt>

0x80320019
</dt> <dt>



Impossibile recapitare una notifica perché una coda di messaggi è alla capacità massima.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**MANCATA \_ CORRISPONDENZA DEL TRAFFICO FWP E \_ \_**
</dt> <dd> <dl> <dt>

0x8032001A
</dt> <dt>



I parametri del traffico di rete non corrispondono a quelli per il contesto di associazione di sicurezza.

[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) può essere chiamato più volte, ma il chiamante deve specificare lo stesso [**TRAFFICO \_ IPSEC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) ogni volta. Questo errore viene restituito se una chiamata successiva fornisce un indirizzo **IPSEC \_ TRAFFIC0 diverso.**


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**FWP \_ E STATO DI FIRMA DI ACCESSO CONDIVISO \_ \_ INCOMPATIBILE \_**
</dt> <dd> <dl> <dt>

0x8032001B
</dt> <dt>



La chiamata non è consentita per lo stato dell'associazione di sicurezza (SA) corrente.

Le funzioni di contesto sa devono essere chiamate in un ordine specifico:

-   [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)
-   [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)
-   [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)
-   [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)

Questo errore viene restituito se vengono chiamati in ordine.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**PUNTATORE NULL \_ FWP E \_ \_**
</dt> <dd> <dl> <dt>

0x8032001C
</dt> <dt>



Un puntatore obbligatorio è Null.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**\_ENUMERATORE FWP E \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

0x8032001D
</dt> <dt>



Un valore dell'enumeratore in una struttura non è compreso nell'intervallo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**FLAG FWP \_ E \_ NON \_ VALIDI**
</dt> <dd> <dl> <dt>

0x8032001E
</dt> <dt>



Il campo flags contiene un valore non valido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**MASCHERA DI \_ RETE FWP E \_ NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

0x8032001F
</dt> <dt>



Un network mask non è valido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**INTERVALLO \_ FWP E \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

0x80320020
</dt> <dt>



Una [**struttura FWP \_ RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0) non è valida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**INTERVALLO \_ FWP E \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

0x80320021
</dt> <dt>



L'intervallo di tempo non è valido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**MATRICE \_ FWP E \_ DI \_ LUNGHEZZA \_ ZERO**
</dt> <dd> <dl> <dt>

0x80320022
</dt> <dt>



Matrice che deve contenere almeno un elemento con lunghezza zero.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**NOME \_ VISUALIZZATO NULL FWP E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80320023
</dt> <dt>



Il **displayData.name** non può essere Null.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**TIPO DI \_ AZIONE FWP E \_ NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

0x80320024
</dt> <dt>



Il tipo di azione non è uno dei tipi di azione consentiti per un filtro.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**PESO \_ FWP E \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

0x80320025
</dt> <dt>



Il peso del filtro non è valido.

Per [altre informazioni, vedere Assegnazione del peso](filter-weight-assignment.md) del filtro.


</dt> </dl> </dd> <dt>

<span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**MANCATA \_ CORRISPONDENZA DEL TIPO DI \_ \_ CORRISPONDENZA \_ FWP E**
</dt> <dd> <dl> <dt>

0x80320026
</dt> <dt>



Una condizione di filtro contiene un tipo di corrispondenza non compatibile con gli operandi.

Per [**altre informazioni, vedere Tipo di \_ corrispondenza \_ FWP.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type)


</dt> </dl> </dd> <dt>

<span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**MANCATA \_ CORRISPONDENZA DEL TIPO FWP E \_ \_**
</dt> <dd> <dl> <dt>

0x80320027
</dt> <dt>



Una [**struttura FWP \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0) o [**una struttura FWPM \_ CONDITION \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0) è di tipo errato.


</dt> </dl> </dd> <dt>

<span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**FWP \_ E FUORI DAI \_ \_ \_ LIMITI**
</dt> <dd> <dl> <dt>

0x80320028
</dt> <dt>



Un valore intero non è compreso nell'intervallo consentito.


</dt> </dl> </dd> <dt>

<span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**FWP \_ E \_ RISERVATO**
</dt> <dd> <dl> <dt>

0x80320029
</dt> <dt>



Un campo riservato è diverso da zero.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**CONDIZIONE \_ DI \_ DUPLICAZIONE FWP E \_**
</dt> <dd> <dl> <dt>

0x8032002A
</dt> <dt>



Un filtro non può contenere più condizioni che operano su un singolo campo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**FWP \_ E \_ DUPLICATE \_ KEYMOD**
</dt> <dd> <dl> <dt>

0x8032002B
</dt> <dt>



Un criterio non può contenere più volte lo stesso modulo di keying.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**AZIONE \_ E FWP \_ \_ INCOMPATIBILE \_ CON IL \_ LIVELLO**
</dt> <dd> <dl> <dt>

0x8032002C
</dt> <dt>



Il tipo di azione non è compatibile con il livello.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**AZIONE \_ E FWP \_ \_ INCOMPATIBILE \_ CON \_ SUBLAYER**
</dt> <dd> <dl> <dt>

0x8032002D
</dt> <dt>



Il tipo di azione non è compatibile con il livello secondario.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**CONTESTO \_ FWP E \_ \_ INCOMPATIBILE \_ CON IL \_ LIVELLO**
</dt> <dd> <dl> <dt>

0x8032002E
</dt> <dt>



Il contesto non elaborato o il contesto del provider non è compatibile con il livello.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**CONTESTO \_ FWP E \_ \_ INCOMPATIBILE \_ CON \_ CALLOUT**
</dt> <dd> <dl> <dt>

0x8032002F
</dt> <dt>



Il contesto non elaborato o il contesto del provider non è compatibile con il callout.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**METODO DI \_ AUTENTICAZIONE FWP E \_ \_ INCOMPATIBILE \_**
</dt> <dd> <dl> <dt>

0x80320030
</dt> <dt>



Il metodo di autenticazione non è compatibile con il tipo di criteri.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**FWP \_ E \_ GRUPPO \_ DH INCOMPATIBILE \_**
</dt> <dd> <dl> <dt>

0x80320031L
</dt> <dt>



Il Diffie-Hellman non è compatibile con il tipo di criteri.


</dt> </dl> </dd> <dt>

<span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**E \_ EM FWP \_ \_ NON \_ SUPPORTATI**
</dt> <dd> <dl> <dt>

0x80320032
</dt> <dt>



I criteri IKE non possono contenere criteri in modalità estesa.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**FWP \_ E \_ NEVER \_ MATCH**
</dt> <dd> <dl> <dt>

0x80320033
</dt> <dt>



Il modello o la sottoscrizione di enumerazione non corrisponderà mai ad alcun oggetto.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**MANCATA \_ CORRISPONDENZA DEL CONTESTO DEL \_ PROVIDER EWP \_ \_**
</dt> <dd> <dl> <dt>

0x80320034
</dt> <dt>



Il contesto del provider è di tipo errato.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**PARAMETRO \_ FWP E \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

0x80320035
</dt> <dt>



Parametro non corretto.

Possibili motivi di questo errore:

-   [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) è stato chiamato senza impostare il flag **FWPM \_ TUNNEL FLAG POINT TO \_ \_ \_ \_ POINT** e con condizioni diverse dall'indirizzo locale/remoto.
-   Stringa Unicode non valida o stringa Unicode contenente caratteri non stampabili.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**TROPPI \_ \_ \_ SOTTOLIVELLI FWP E \_**
</dt> <dd> <dl> <dt>

0x80320036
</dt> <dt>



È stato raggiunto il numero massimo di sottolivelli.

Il WFP supporta al massimo 2 6 sottolivelli.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**NOTIFICA \_ DI CALLOUT E \_ FWP \_ NON \_ RIUSCITA**
</dt> <dd> <dl> <dt>

0x80320037
</dt> <dt>



La funzione di notifica per un callout ha restituito un errore.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**FWP \_ E \_ TRASFORMAZIONE \_ DELL'AUTENTICAZIONE NON \_ VALIDA**
</dt> <dd> <dl> <dt>

0x80320038
</dt> <dt>



La trasformazione di autenticazione IPsec non è valida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**TRASFORMAZIONE DI \_ CRITTOGRAFIA FWP E \_ NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

0x80320039
</dt> <dt>



La trasformazione di crittografia IPsec non è valida.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Winerror</dt> </dl> |



 

 





