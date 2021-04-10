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
# <a name="system-error-codes-8200-8999"></a>Codici di errore di sistema (8200-8999)

> [!NOTE]
> Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema. Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .

Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) per gli errori da 8200 a 8999. Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .

<dl> <dt>

<span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERRORE \_ DS \_ non \_ installato**
</dt> <dd> <dl> <dt>

8200 (0x2008)
</dt> <dt>



Si è verificato un errore durante l'installazione del servizio directory. Per ulteriori informazioni, vedere il registro eventi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERRORE \_ di \_ appartenenza DS \_ valutato \_ localmente**
</dt> <dd> <dl> <dt>

8201 (0x2009)
</dt> <dt>



Il servizio directory ha valutato le appartenenze ai gruppi localmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERRORE \_ DS \_ nessun \_ attributo \_ o \_ valore**
</dt> <dd> <dl> <dt>

8202 (0x200A)
</dt> <dt>



Il valore o l'attributo del servizio di directory specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERRORE della \_ sintassi degli attributi di DS \_ non valida \_ \_**
</dt> <dd> <dl> <dt>

8203 (0x200B)
</dt> <dt>



La sintassi dell'attributo specificata per il servizio directory non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**\_tipo di attributo DS per errori non \_ \_ \_ definito**
</dt> <dd> <dl> <dt>

8204 (0x200C)
</dt> <dt>



Il tipo di attributo specificato per il servizio directory non è definito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**il \_ valore o l'attributo DS dell'errore \_ \_ \_ \_ esiste**
</dt> <dd> <dl> <dt>

8205 (0x200D)
</dt> <dt>



Il valore o l'attributo del servizio di directory specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERRORE \_ DS \_ occupato**
</dt> <dd> <dl> <dt>

8206 (0x200E)
</dt> <dt>



Il servizio directory è occupato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERRORE \_ DS non \_ disponibile**
</dt> <dd> <dl> <dt>

8207 (0x200F)
</dt> <dt>



Il servizio directory non è disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERRORE \_ DS \_ nessun \_ RID \_ allocato**
</dt> <dd> <dl> <dt>

8208 (0x2010)
</dt> <dt>



Il servizio directory non è in grado di allocare l'identificatore relativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERRORE \_ DS \_ non \_ più \_ RID**
</dt> <dd> <dl> <dt>

8209 (0x2011)
</dt> <dt>



Il servizio directory ha esaurito il pool di identificatori relativi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERRORE \_ DS \_ \_ proprietario ruolo \_ errato**
</dt> <dd> <dl> <dt>

8210 (0x2012)
</dt> <dt>



Non è stato possibile eseguire l'operazione richiesta perché il servizio directory non è il master per quel tipo di operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**errore \_ di \_ inizializzazione di DS RIDMGR \_ \_**
</dt> <dd> <dl> <dt>

8211 (0x2013)
</dt> <dt>



Il servizio directory non è stato in grado di inizializzare il sottosistema che alloca gli identificatori relativi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**\_violazione della \_ \_ classe obj \_ di errore DS**
</dt> <dd> <dl> <dt>

8212 (0x2014)
</dt> <dt>



L'operazione richiesta non soddisfa uno o più vincoli associati alla classe dell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERRORE \_ DS \_ \_ non in \_ \_ foglia**
</dt> <dd> <dl> <dt>

8213 (0x2015)
</dt> <dt>



Il servizio directory è in grado di eseguire l'operazione richiesta solo su un oggetto foglia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**errore \_ DS \_ \_ di errore su \_ RDN**
</dt> <dd> <dl> <dt>

8214 (0x2016)
</dt> <dt>



Il servizio directory non è in grado di eseguire l'operazione richiesta sull'attributo RDN di un oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERRORE \_ DS \_ \_ mod cant \_ \_ classe obj**
</dt> <dd> <dl> <dt>

8215 (0x2017)
</dt> <dt>



Il servizio directory ha rilevato un tentativo di modificare la classe di oggetti di un oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**errore \_ di \_ \_ trasferimento Dom \_ tra \_ i DS**
</dt> <dd> <dl> <dt>

8216 (0x2018)
</dt> <dt>



Non è stato possibile eseguire l'operazione di spostamento tra domini richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERRORE \_ \_ GC DS \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

8217 (0x2019)
</dt> <dt>



Impossibile contattare il server di catalogo globale.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**ERRORE \_ di \_ criteri condivisi**
</dt> <dd> <dl> <dt>

8218 (0x201A)
</dt> <dt>



L'oggetto criteri è condiviso e può essere modificato solo alla radice.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**\_ \_ \_ Impossibile trovare l'oggetto Criteri di errore \_**
</dt> <dd> <dl> <dt>

8219 (0x201B)
</dt> <dt>



L'oggetto criteri non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**\_criteri \_ di errore solo \_ in \_ DS**
</dt> <dd> <dl> <dt>

8220 (0x201C)
</dt> <dt>



Le informazioni sui criteri richieste sono solo nel servizio directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**promozione dell'errore \_ \_ attiva**
</dt> <dd> <dl> <dt>

8221 (0x201D)
</dt> <dt>



Una promozione del controller di dominio è attualmente attiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERRORE \_ Nessuna \_ Promozione \_ attiva**
</dt> <dd> <dl> <dt>

8222 (0x201E)
</dt> <dt>



Una promozione del controller di dominio non è attualmente attiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**errore \_ operazioni DS errore \_ \_**
</dt> <dd> <dl> <dt>

8224 (0x2020)
</dt> <dt>



Si è verificato un errore operativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**errore \_ del \_ protocollo DS di errore \_**
</dt> <dd> <dl> <dt>

8225 (0x2021)
</dt> <dt>



Si è verificato un errore di protocollo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**superato il limite di timeout \_ DS \_ \_**
</dt> <dd> <dl> <dt>

8226 (0x2022)
</dt> <dt>



È stato superato il limite di tempo per la richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERRORE \_ DS \_ SIZELIMIT \_ superato**
</dt> <dd> <dl> <dt>

8227 (0x2023)
</dt> <dt>



È stato superato il limite di dimensioni per questa richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**\_ \_ superato limite di amministrazione DS \_ per \_ errori**
</dt> <dd> <dl> <dt>

8228 (0x2024)
</dt> <dt>



Il limite amministrativo per questa richiesta è stato superato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERRORE \_ DS \_ confronto \_ false**
</dt> <dd> <dl> <dt>

8229 (0x2025)
</dt> <dt>



La risposta di confronto è false.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERRORE \_ DS \_ compare \_ true**
</dt> <dd> <dl> <dt>

8230 (0x2026)
</dt> <dt>



La risposta di confronto è vera.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**il \_ metodo di autenticazione DS con errori \_ non è \_ \_ \_ supportato**
</dt> <dd> <dl> <dt>

8231 (0x2027)
</dt> <dt>



Il metodo di autenticazione richiesto non è supportato dal server.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERRORE \_ \_ autenticazione avanzata \_ DS \_ necessaria**
</dt> <dd> <dl> <dt>

8232 (0x2028)
</dt> <dt>



Per questo server è necessario un metodo di autenticazione più sicuro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**\_autenticazione non \_ appropriata di DS per gli errori \_**
</dt> <dd> <dl> <dt>

8233 (0x2029)
</dt> <dt>



Autenticazione non appropriata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERRORE \_ di \_ autenticazione DS non \_ noto**
</dt> <dd> <dl> <dt>

8234 (0x202A)
</dt> <dt>



Il meccanismo di autenticazione è sconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**\_segnalazione errori DS \_**
</dt> <dd> <dl> <dt>

8235 (0x202B)
</dt> <dt>



Il server ha restituito un riferimento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**ERRORE \_ DS non disponibile per l' \_ \_ estensione del critico \_**
</dt> <dd> <dl> <dt>

8236 (0x202C)
</dt> <dt>



Il server non supporta l'estensione critica richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**ERRORE \_ \_ riservato DS \_ obbligatorio**
</dt> <dd> <dl> <dt>

8237 (0x202D)
</dt> <dt>



Questa richiesta richiede una connessione protetta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERRORE \_ DS non \_ appropriato \_ corrispondente**
</dt> <dd> <dl> <dt>

8238 (0x202E)
</dt> <dt>



Corrispondenza non appropriata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**\_violazione del \_ vincolo \_ DS di errore**
</dt> <dd> <dl> <dt>

8239 (0x202F)
</dt> <dt>



Si è verificata una violazione del vincolo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERRORE \_ DS \_ nessun \_ oggetto di questo tipo \_**
</dt> <dd> <dl> <dt>

8240 (0x2030)
</dt> <dt>



Oggetto inesistente sul server.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**\_ \_ problema alias DS \_ errore**
</dt> <dd> <dl> <dt>

8241 (0x2031)
</dt> <dt>



Si è verificato un problema di alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERRORE \_ DS \_ \_ sintassi DN non valida \_**
</dt> <dd> <dl> <dt>

8242 (0x2032)
</dt> <dt>



È stata specificata una sintassi DN non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**l'errore \_ DS \_ è \_ foglia**
</dt> <dd> <dl> <dt>

8243 (0x2033)
</dt> <dt>



L'oggetto è un oggetto foglia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**ERRORE \_ \_ Deref alias \_ DS \_**
</dt> <dd> <dl> <dt>

8244 (0x2034)
</dt> <dt>



Si è verificato un problema di dereferenziazione dell'alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERRORE \_ DS \_ che non verrà \_ \_ eseguito**
</dt> <dd> <dl> <dt>

8245 (0x2035)
</dt> <dt>



Il server non è in funzione di elaborare la richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**\_ \_ rilevamento ciclo DS \_ errore**
</dt> <dd> <dl> <dt>

8246 (0x2036)
</dt> <dt>



È stato rilevato un ciclo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**\_violazione di \_ denominazione \_ DS errore**
</dt> <dd> <dl> <dt>

8247 (0x2037)
</dt> <dt>



Si è verificata una violazione di denominazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**ERRORE \_ \_ dei risultati di un oggetto DS \_ \_ troppo \_ grande**
</dt> <dd> <dl> <dt>

8248 (0x2038)
</dt> <dt>



Il set di risultati è troppo grande.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**ERRORE \_ DS \_ influiscono su \_ più \_ DSA**
</dt> <dd> <dl> <dt>

8249 (0x2039)
</dt> <dt>



L'operazione ha effetto su più DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERRORE \_ nel \_ server \_ DS**
</dt> <dd> <dl> <dt>

8250 (0x203A)
</dt> <dt>



Il server non è operativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**errore \_ locale DS errore \_ \_**
</dt> <dd> <dl> <dt>

8251 (0x203B)
</dt> <dt>



Si è verificato un errore locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**errore \_ di \_ codifica DS errore \_**
</dt> <dd> <dl> <dt>

8252 (0x203C)
</dt> <dt>



Si è verificato un errore di codifica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**\_errore di \_ decodifica DS di errore \_**
</dt> <dd> <dl> <dt>

8253 (0x203D)
</dt> <dt>



Si è verificato un errore di decodifica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERRORE \_ \_ filtro DS \_ sconosciuto**
</dt> <dd> <dl> <dt>

8254 (0x203E)
</dt> <dt>



Impossibile riconoscere il filtro di ricerca.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**errore \_ di \_ param DS errore \_**
</dt> <dd> <dl> <dt>

8255 (0x203F)
</dt> <dt>



Uno o più parametri non sono validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERRORE \_ DS \_ non \_ supportato**
</dt> <dd> <dl> <dt>

8256 (0x2040)
</dt> <dt>



Il metodo specificato non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERRORE \_ DS \_ nessun \_ risultato \_ restituito**
</dt> <dd> <dl> <dt>

8257 (0x2041)
</dt> <dt>



Nessun risultato restituito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**ERRORE \_ \_ controllo DS \_ non \_ trovato**
</dt> <dd> <dl> <dt>

8258 (0x2042)
</dt> <dt>



Il controllo specificato non è supportato dal server.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERRORE \_ \_ ciclo client \_ DS**
</dt> <dd> <dl> <dt>

8259 (0x2043)
</dt> <dt>



Il client ha rilevato un ciclo di riferimento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**\_limite di riferimento DS per errori \_ \_ \_ superato**
</dt> <dd> <dl> <dt>

8260 (0x2044)
</dt> <dt>



È stato superato il limite di riferimento del set di impostazioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERRORE \_ \_ controllo ordinamento \_ DS \_ mancante**
</dt> <dd> <dl> <dt>

8261 (0x2045)
</dt> <dt>



La ricerca richiede un controllo SORT.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**\_errore di \_ intervallo di offset DS \_ errore \_**
</dt> <dd> <dl> <dt>

8262 (0x2046)
</dt> <dt>



I risultati della ricerca superano l'intervallo di offset specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERRORE \_ DS \_ RIDMGR \_ disabilitato**
</dt> <dd> <dl> <dt>

8263 (0x2047)
</dt> <dt>



Il servizio directory ha rilevato che il sottosistema che alloca gli identificatori relativi è disabilitato. Questo può verificarsi come meccanismo di protezione quando il sistema determina che una parte significativa degli identificatori relativi (RID) è stata esaurita. <https://go.microsoft.com/fwlink/p/?linkid=228610>Per la procedura di riabilitazione della creazione dell'account, vedere la procedura consigliata per la procedura di diagnostica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**ERRORE \_ DS \_ radice \_ deve \_ essere \_ NC**
</dt> <dd> <dl> <dt>

8301 (0x206D)
</dt> <dt>



L'oggetto radice deve essere il capo di un contesto dei nomi. L'oggetto radice non può avere un elemento padre di cui è stata creata un'istanza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERRORE \_ DS \_ aggiunta \_ replica \_ inibita**
</dt> <dd> <dl> <dt>

8302 (0x206E)
</dt> <dt>



Impossibile eseguire l'operazione di aggiunta replica. Per creare la replica, il contesto dei nomi deve essere scrivibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERRORE \_ DS \_ att \_ non \_ def \_ nello \_ schema**
</dt> <dd> <dl> <dt>

8303 (0x206F)
</dt> <dt>



Si è verificato un riferimento a un attributo non definito nello schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**\_ \_ dimensioni massime \_ obj errore DS \_ \_ superate**
</dt> <dd> <dl> <dt>

8304 (0x2070)
</dt> <dt>



È stata superata la dimensione massima di un oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**ERRORE \_ DS \_ \_ nome stringa \_ obj \_ esistente**
</dt> <dd> <dl> <dt>

8305 (0x2071)
</dt> <dt>



È stato effettuato un tentativo di aggiungere un oggetto alla directory con un nome già in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERRORE \_ DS \_ nessun \_ RDN \_ definito \_ nello \_ schema**
</dt> <dd> <dl> <dt>

8306 (0x2072)
</dt> <dt>



È stato effettuato un tentativo di aggiungere un oggetto di una classe che non dispone di un RDN definito nello schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**ERRORE \_ directory \_ RDN non \_ \_ corrispondente \_ schema**
</dt> <dd> <dl> <dt>

8307 (0x2073)
</dt> <dt>



È stato effettuato un tentativo di aggiungere un oggetto utilizzando un RDN che non è il RDN definito nello schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERRORE \_ DS \_ nessun \_ \_ atts richiesto \_ trovato**
</dt> <dd> <dl> <dt>

8308 (0x2074)
</dt> <dt>



Nessuno degli attributi richiesti è stato trovato negli oggetti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERRORE \_ del \_ buffer utente DS \_ \_ su \_ Small**
</dt> <dd> <dl> <dt>

8309 (0x2075)
</dt> <dt>



Il buffer utente è troppo piccolo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**ERRORE \_ DS \_ att \_ \_ non è \_ in \_ obj**
</dt> <dd> <dl> <dt>

8310 (0x2076)
</dt> <dt>



L'attributo specificato nell'operazione non è presente nell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERRORE \_ DS \_ - \_ operazione mod non valida \_**
</dt> <dd> <dl> <dt>

8311 (0x2077)
</dt> <dt>



Operazione di modifica non valida. Alcuni aspetti della modifica non sono consentiti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**ERRORE \_ DS \_ obj \_ troppo \_ grande**
</dt> <dd> <dl> <dt>

8312 (0x2078)
</dt> <dt>



L'oggetto specificato è troppo grande.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERRORE \_ DS \_ \_ tipo istanza non valida \_**
</dt> <dd> <dl> <dt>

8313 (0x2079)
</dt> <dt>



Il tipo di istanza specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERRORE \_ DS \_ MASTERDSA \_ obbligatorio**
</dt> <dd> <dl> <dt>

8314 (0x207A)
</dt> <dt>



L'operazione deve essere eseguita in un DSA master.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**\_classe dell'oggetto DS di errore \_ \_ \_ obbligatoria**
</dt> <dd> <dl> <dt>

8315 (0x207B)
</dt> <dt>



È necessario specificare l'attributo della classe di oggetti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**ERRORE \_ DS \_ manca \_ l' \_ att obbligatorio**
</dt> <dd> <dl> <dt>

8316 (0x207C)
</dt> <dt>



Attributo obbligatorio mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERRORE \_ DS \_ att \_ non \_ def \_ per la \_ classe**
</dt> <dd> <dl> <dt>

8317 (0x207D)
</dt> <dt>



È stato effettuato un tentativo di modificare un oggetto per includere un attributo che non è valido per la relativa classe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**ERRORE \_ DS \_ att \_ già \_ esistente**
</dt> <dd> <dl> <dt>

8318 (0x207E)
</dt> <dt>



L'attributo specificato è già presente nell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERRORE non è stato \_ \_ aggiunto alcun \_ \_ \_ valore att di DS**
</dt> <dd> <dl> <dt>

8320 (0x2080)
</dt> <dt>



L'attributo specificato non è presente o non ha valori.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERRORE \_ DS \_ \_ valore singolo \_ vincolo**
</dt> <dd> <dl> <dt>

8321 (0x2081)
</dt> <dt>



Sono stati specificati più valori per un attributo che può avere un solo valore.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**ERRORE \_ \_ vincolo intervallo \_ DS**
</dt> <dd> <dl> <dt>

8322 (0x2082)
</dt> <dt>



Un valore per l'attributo non è compreso nell'intervallo di valori accettabile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**ERRORE \_ DS \_ att \_ Val \_ \_ esiste già**
</dt> <dd> <dl> <dt>

8323 (0x2083)
</dt> <dt>



Il valore specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERRORE \_ REM cant di DS non \_ \_ \_ presente \_**
</dt> <dd> <dl> <dt>

8324 (0x2084)
</dt> <dt>



Impossibile rimuovere l'attributo perché non è presente nell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**ERRORE \_ \_ REM cant di DS \_ \_ mancato \_ att \_ Val**
</dt> <dd> <dl> <dt>

8325 (0x2085)
</dt> <dt>



Impossibile rimuovere il valore dell'attributo perché non è presente nell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**ERRORE \_ DS \_ root \_ cant \_ be \_ sottoriferimento**
</dt> <dd> <dl> <dt>

8326 (0x2086)
</dt> <dt>



L'oggetto radice specificato non può essere un sottoriferimento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERRORE \_ DS \_ nessun \_ concatenamento**
</dt> <dd> <dl> <dt>

8327 (0x2087)
</dt> <dt>



Il concatenamento non è consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERRORE \_ DS \_ non \_ concatenato \_ EVAL**
</dt> <dd> <dl> <dt>

8328 (0x2088)
</dt> <dt>



La valutazione concatenata non è consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERRORE \_ DS \_ nessun \_ \_ oggetto padre**
</dt> <dd> <dl> <dt>

8329 (0x2089)
</dt> <dt>



Il padre dell'oggetto è privo di istanza o è stato eliminato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**ERRORE \_ DS \_ padre \_ è \_ un \_ alias**
</dt> <dd> <dl> <dt>

8330 (0x208A)
</dt> <dt>



Non è consentito disporre di un elemento padre che è un alias. Gli alias sono oggetti foglia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERRORE \_ nel \_ \_ \_ master e nei \_ \_ rep di DS**
</dt> <dd> <dl> <dt>

8331 (0x208B)
</dt> <dt>



L'oggetto e l'elemento padre devono essere dello stesso tipo, sia master che entrambe le repliche.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**gli errori \_ DS sono \_ \_ disponibili**
</dt> <dd> <dl> <dt>

8332 (0x208C)
</dt> <dt>



Impossibile eseguire l'operazione perché sono presenti oggetti figlio. Questa operazione può essere eseguita solo su un oggetto foglia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**ERRORE \_ DS \_ obj \_ non \_ trovato**
</dt> <dd> <dl> <dt>

8333 (0x208D)
</dt> <dt>



Impossibile trovare l'oggetto directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**ERRORE \_ di \_ obj con alias DS \_ \_ mancante**
</dt> <dd> <dl> <dt>

8334 (0x208E)
</dt> <dt>



Oggetto con alias mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**sintassi per i \_ \_ nomi non validi DS \_ errore \_**
</dt> <dd> <dl> <dt>

8335 (0x208F)
</dt> <dt>



Il nome dell'oggetto presenta una sintassi non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**ERRORE \_ \_ alias DS \_ punta \_ a \_ alias**
</dt> <dd> <dl> <dt>

8336 (0x2090)
</dt> <dt>



Non è consentito che un alias faccia riferimento a un altro alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERRORE \_ di \_ Deref cant di DS \_ \_**
</dt> <dd> <dl> <dt>

8337 (0x2091)
</dt> <dt>



Non è possibile dereferenziare l'alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERRORE \_ DS \_ dall' \_ \_ ambito**
</dt> <dd> <dl> <dt>

8338 (0x2092)
</dt> <dt>



L'operazione non rientra nell'ambito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERRORE di \_ dominio DS \_ \_ \_ rimosso**
</dt> <dd> <dl> <dt>

8339 (0x2093)
</dt> <dt>



L'operazione non può continuare perché è in corso la rimozione dell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERRORE \_ di \_ \_ eliminazione \_ DSA \_ obj**
</dt> <dd> <dl> <dt>

8340 (0x2094)
</dt> <dt>



Non è possibile eliminare l'oggetto DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**errore \_ generico DS errore \_ \_**
</dt> <dd> <dl> <dt>

8341 (0x2095)
</dt> <dt>



Si è verificato un errore del servizio directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**ERRORE \_ DS \_ DSA \_ deve \_ essere \_ int \_ Master**
</dt> <dd> <dl> <dt>

8342 (0x2096)
</dt> <dt>



L'operazione può essere eseguita solo su un oggetto master DSA interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERRORE \_ \_ classe DS \_ non \_ DSA**
</dt> <dd> <dl> <dt>

8343 (0x2097)
</dt> <dt>



L'oggetto deve essere di classe DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**\_diritti di \_ \_ accesso insuff di DS \_ errore**
</dt> <dd> <dl> <dt>

8344 (0x2098)
</dt> <dt>



Diritti di accesso insufficienti per eseguire l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERRORE \_ DS \_ superiore non valido \_**
</dt> <dd> <dl> <dt>

8345 (0x2099)
</dt> <dt>



Non è possibile aggiungere l'oggetto perché l'elemento padre non è presente nell'elenco dei migliori.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**\_attributo DS \_ \_ di errore \_ di proprietà di \_ Sam**
</dt> <dd> <dl> <dt>

8346 (0x209A)
</dt> <dt>



L'accesso all'attributo non è consentito perché l'attributo appartiene a gestione account di sicurezza (SAM).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERRORE \_ \_ nome DS \_ numero troppe \_ \_ parti**
</dt> <dd> <dl> <dt>

8347 (0x209B)
</dt> <dt>



Il nome contiene troppe parti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**\_nome DS \_ errore \_ troppo \_ lungo**
</dt> <dd> <dl> <dt>

8348 (0x209C)
</dt> <dt>



Nome troppo lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**\_ \_ valore nome DS \_ errore \_ troppo \_ lungo**
</dt> <dd> <dl> <dt>

8349 (0x209D)
</dt> <dt>



Il valore del nome è troppo lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERRORE \_ nome DS non \_ \_ analizzabile**
</dt> <dd> <dl> <dt>

8350 (0x209E)
</dt> <dt>



Il servizio directory ha rilevato un errore durante l'analisi di un nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERRORE \_ \_ nome DS \_ tipo \_ sconosciuto**
</dt> <dd> <dl> <dt>

8351 (0x209F)
</dt> <dt>



Il servizio directory non è in grado di ottenere il tipo di attributo per un nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERRORE \_ DS \_ non è \_ un \_ oggetto**
</dt> <dd> <dl> <dt>

8352 (0x20A0)
</dt> <dt>



Il nome non identifica un oggetto. il nome identifica un oggetto fantasma.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERRORE di \_ DS \_ sec \_ desc \_ troppo \_ breve**
</dt> <dd> <dl> <dt>

8353 (0x20A1)
</dt> <dt>



Il descrittore di sicurezza è troppo breve.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERRORE \_ DS \_ sec \_ desc \_ non valido**
</dt> <dd> <dl> <dt>

8354 (0x20A2)
</dt> <dt>



Il descrittore di sicurezza non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERRORE \_ DS \_ nessun \_ \_ nome eliminato**
</dt> <dd> <dl> <dt>

8355 (0x20A3)
</dt> <dt>



Impossibile creare il nome per l'oggetto eliminato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**ERRORE \_ DS \_ sottoriferimento \_ deve \_ avere \_ padre**
</dt> <dd> <dl> <dt>

8356 (0x20A4)
</dt> <dt>



Il padre di un nuovo sottoriferimento deve esistere.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**ERRORE \_ DS \_ NCName \_ deve \_ essere \_ NC**
</dt> <dd> <dl> <dt>

8357 (0x20A5)
</dt> <dt>



L'oggetto deve essere un contesto dei nomi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERRORE \_ DS \_ cant \_ Add \_ System \_ only**
</dt> <dd> <dl> <dt>

8358 (0x20A6)
</dt> <dt>



Non è consentito aggiungere un attributo di proprietà del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**la \_ classe DS degli errori \_ \_ deve \_ essere \_ concreta**
</dt> <dd> <dl> <dt>

8359 (0x20A7)
</dt> <dt>



La classe dell'oggetto deve essere strutturale; non è possibile creare un'istanza di una classe astratta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERRORE \_ DS \_ non valido \_**
</dt> <dd> <dl> <dt>

8360 (0x20A8)
</dt> <dt>



Impossibile trovare l'oggetto dello schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**ERRORE \_ DS \_ obj \_ GUID \_ esistente**
</dt> <dd> <dl> <dt>

8361 (0x20A9)
</dt> <dt>



Un oggetto locale con questo GUID (Dead o Alive) esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERRORE \_ DS \_ non \_ in \_ BACKLINK**
</dt> <dd> <dl> <dt>

8362 (0x20AA)
</dt> <dt>



Impossibile eseguire l'operazione su un collegamento indietro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERRORE \_ DS \_ nessun \_ CROSSREF \_ per \_ NC**
</dt> <dd> <dl> <dt>

8363 (0x20AB)
</dt> <dt>



Impossibile trovare il riferimento incrociato per il contesto dei nomi specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERRORE \_ di \_ arresto di \_ DS**
</dt> <dd> <dl> <dt>

8364 (0x20AC)
</dt> <dt>



Non è stato possibile eseguire l'operazione perché è in corso la chiusura del servizio directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**\_ \_ operazione sconosciuta DS \_ errore**
</dt> <dd> <dl> <dt>

8365 (0x20AD)
</dt> <dt>



La richiesta del servizio directory non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERRORE \_ DS \_ \_ proprietario ruolo non valido \_**
</dt> <dd> <dl> <dt>

8366 (0x20AE)
</dt> <dt>



Impossibile leggere l'attributo del proprietario del ruolo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERRORE \_ DS \_ couldnt \_ Contact \_ FSMO**
</dt> <dd> <dl> <dt>

8367 (0x20AF)
</dt> <dt>



L'operazione FSMO richiesta non è riuscita. Impossibile contattare il proprietario FSMO corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERRORE \_ di \_ \_ \_ ridenominazione DN Cross NC \_**
</dt> <dd> <dl> <dt>

8368 (0x20B0)
</dt> <dt>



Non è consentita la modifica di un DN in un contesto di denominazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERRORE \_ \_ solo del sistema cant DS \_ mod \_ \_**
</dt> <dd> <dl> <dt>

8369 (0x20B1)
</dt> <dt>



L'attributo non può essere modificato perché appartiene al sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERRORE \_ \_ solo Replicator \_ DS**
</dt> <dd> <dl> <dt>

8370 (0x20B2)
</dt> <dt>



Questa funzione può essere eseguita solo da Replicator.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERRORE \_ DS \_ obj \_ classe \_ non \_ definita**
</dt> <dd> <dl> <dt>

8371 (0x20B3)
</dt> <dt>



La classe specificata non è definita.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERRORE \_ DS \_ obj \_ classe \_ non \_ sottoclasse**
</dt> <dd> <dl> <dt>

8372 (0x20B4)
</dt> <dt>



La classe specificata non è una sottoclasse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**\_ \_ riferimento nome DS \_ errore \_ non valido**
</dt> <dd> <dl> <dt>

8373 (0x20B5)
</dt> <dt>



Il riferimento al nome non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**ERRORE di \_ DS \_ Cross \_ ref \_ esistente**
</dt> <dd> <dl> <dt>

8374 (0x20B6)
</dt> <dt>



Esiste già un riferimento incrociato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERRORE \_ DS \_ cant \_ del \_ master \_ CROSSREF**
</dt> <dd> <dl> <dt>

8375 (0x20B7)
</dt> <dt>



Non è consentito eliminare un riferimento incrociato master.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERRORE del \_ sottoalbero di DS per la \_ \_ notifica \_ \_ \_**
</dt> <dd> <dl> <dt>

8376 (0x20B8)
</dt> <dt>



Le notifiche del sottoalbero sono supportate solo nelle intestazioni NC.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**\_ \_ filtro notifiche DS \_ errore \_ troppo \_ complesso**
</dt> <dd> <dl> <dt>

8377 (0x20B9)
</dt> <dt>



Il filtro di notifica è troppo complesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERRORE \_ RDN di DS \_ DUP \_**
</dt> <dd> <dl> <dt>

8378 (0x20BA)
</dt> <dt>



Aggiornamento dello schema non riuscito: RDN duplicato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ID errore \_ DS \_ DUP \_**
</dt> <dd> <dl> <dt>

8379 (0x20BB)
</dt> <dt>



Aggiornamento dello schema non riuscito: OID duplicato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**ERRORE \_ DS \_ DUP \_ \_ ID MAPI**
</dt> <dd> <dl> <dt>

8380 (0x20BC)
</dt> <dt>



Aggiornamento dello schema non riuscito: identificatore MAPI duplicato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**\_ \_ \_ \_ GUID ID schema duplicato errore DS \_**
</dt> <dd> <dl> <dt>

8381 (0x20BD)
</dt> <dt>



Aggiornamento dello schema non riuscito: GUID ID schema duplicato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERRORE \_ DS \_ DUP \_ \_ nome visualizzato \_ LDAP**
</dt> <dd> <dl> <dt>

8382 (0x20BE)
</dt> <dt>



Aggiornamento dello schema non riuscito: nome visualizzato LDAP duplicato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERRORE \_ di \_ test semantico di DS \_ \_**
</dt> <dd> <dl> <dt>

8383 (0x20BF)
</dt> <dt>



Aggiornamento schema non riuscito: intervallo-inferiore minore di intervallo superiore.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERRORE \_ di \_ sintassi DS non \_ corrispondente**
</dt> <dd> <dl> <dt>

8384 (0x20C0)
</dt> <dt>



Aggiornamento dello schema non riuscito: sintassi non corrispondente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**ERRORE \_ DS \_ \_ in \_ deve \_ avere**
</dt> <dd> <dl> <dt>

8385 (0x20C1)
</dt> <dt>



Eliminazione dello schema non riuscita: l'attributo viene usato in must-contain.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**ERRORE \_ DS \_ presente \_ in \_ potrebbe \_ avere**
</dt> <dd> <dl> <dt>

8386 (0x20C2)
</dt> <dt>



L'eliminazione dello schema non è riuscita: l'attributo viene utilizzato in può contenere.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**ERRORE \_ DS non \_ esistente \_ potrebbe \_ avere**
</dt> <dd> <dl> <dt>

8387 (0x20C3)
</dt> <dt>



Aggiornamento dello schema non riuscito: l'attributo in può contenere non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**ERRORE \_ DS non \_ esistente \_ deve \_ contenere**
</dt> <dd> <dl> <dt>

8388 (0x20C4)
</dt> <dt>



Aggiornamento dello schema non riuscito: l'attributo in must-contain non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERRORE \_ del \_ \_ test CLS \_ aux \_ DS**
</dt> <dd> <dl> <dt>

8389 (0x20C5)
</dt> <dt>



Aggiornamento dello schema non riuscito: la classe nell'elenco di classi aux non esiste o non è una classe ausiliaria.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERRORE di \_ DS non \_ esistente \_ \_ sup**
</dt> <dd> <dl> <dt>

8390 (0x20C6)
</dt> <dt>



Aggiornamento dello schema non riuscito: la classe in poss-superiors non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERRORE \_ \_ \_ test sottocls \_ di \_ DS errore**
</dt> <dd> <dl> <dt>

8391 (0x20C7)
</dt> <dt>



Aggiornamento dello schema non riuscito: la classe nell'elenco subclassOf non esiste o non soddisfa le regole della gerarchia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERRORE \_ DS \_ \_ \_ \_ sintassi ID RDN non \_ valida**
</dt> <dd> <dl> <dt>

8392 (0x20C8)
</dt> <dt>



L'aggiornamento dello schema non è riuscito: la sintassi di RDN-att-ID non è corretta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**ERRORE \_ DS \_ presente \_ nella \_ \_ CLS aux**
</dt> <dd> <dl> <dt>

8393 (0x20C9)
</dt> <dt>



Eliminazione dello schema non riuscita: la classe viene usata come classe ausiliaria.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**ERRORE \_ DS \_ presente \_ in \_ Sub \_ CLS**
</dt> <dd> <dl> <dt>

8394 (0x20CA)
</dt> <dt>



Eliminazione dello schema non riuscita: la classe viene usata come classe secondaria.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**ERRORE \_ DS \_ presente \_ nel \_ \_ sup sup**
</dt> <dd> <dl> <dt>

8395 (0x20CB)
</dt> <dt>



Eliminazione dello schema non riuscita: la classe viene utilizzata come superiore.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**ERRORE \_ DS \_ RECALCSCHEMA \_ non riuscito**
</dt> <dd> <dl> <dt>

8396 (0x20CC)
</dt> <dt>



Errore di aggiornamento dello schema durante il ricalcolo della cache di convalida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERRORE \_ di \_ eliminazione albero DS \_ \_ non \_ completata**
</dt> <dd> <dl> <dt>

8397 (0x20CD)
</dt> <dt>



L'eliminazione dell'albero non è stata completata. La richiesta deve essere eseguita di nuovo per continuare a eliminare l'albero.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERRORE \_ di \_ eliminazione del cant DS \_**
</dt> <dd> <dl> <dt>

8398 (0x20CE)
</dt> <dt>



Non è stato possibile eseguire l'operazione di eliminazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**\_ID richiesta \_ \_ dello schema \_ \_ di errore DS**
</dt> <dd> <dl> <dt>

8399 (0x20CF)
</dt> <dt>



Impossibile leggere l'identificatore di classe governas per il record dello schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**\_ \_ \_ \_ sintassi dello schema \_ di errore DS non valida**
</dt> <dd> <dl> <dt>

8400 (0x20D0)
</dt> <dt>



La sintassi dello schema dell'attributo non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERRORE \_ \_ nella cache del cant DS \_ \_**
</dt> <dd> <dl> <dt>

8401 (0x20D1)
</dt> <dt>



Non è stato possibile memorizzare nella cache l'attributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERRORE \_ \_ \_ classe cache cant \_ DS**
</dt> <dd> <dl> <dt>

8402 (0x20D2)
</dt> <dt>



Impossibile memorizzare nella cache la classe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERRORE di DS per la \_ \_ \_ rimozione \_ \_ della cache att**
</dt> <dd> <dl> <dt>

8403 (0x20D3)
</dt> <dt>



Impossibile rimuovere l'attributo dalla cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**errore durante la \_ \_ \_ rimozione \_ \_ della cache della classe di DS**
</dt> <dd> <dl> <dt>

8404 (0x20D4)
</dt> <dt>



Non è stato possibile rimuovere la classe dalla cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**errore durante il \_ \_ recupero del \_ \_ DN DS**
</dt> <dd> <dl> <dt>

8405 (0x20D5)
</dt> <dt>



Impossibile leggere l'attributo del nome distinto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERRORE \_ DS \_ mancante \_ SUPREF**
</dt> <dd> <dl> <dt>

8406 (0x20D6)
</dt> <dt>



Non è stato configurato alcun riferimento superiore per il servizio directory. Il servizio directory non è quindi in grado di emettere riferimenti a oggetti esterni a questa foresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**errore durante il \_ \_ recupero dell' \_ \_ istanza di DS**
</dt> <dd> <dl> <dt>

8407 (0x20D7)
</dt> <dt>



Impossibile recuperare l'attributo del tipo di istanza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**ERRORE \_ di \_ incoerenza del codice DS \_**
</dt> <dd> <dl> <dt>

8408 (0x20D8)
</dt> <dt>



Si è verificato un errore interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**errore \_ database DS errore \_ \_**
</dt> <dd> <dl> <dt>

8409 (0x20D9)
</dt> <dt>



Si è verificato un errore del database.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERRORE \_ DS \_ governsID \_ mancante**
</dt> <dd> <dl> <dt>

8410 (0x20DA)
</dt> <dt>



Attributo GOVERNSID mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**ERRORE in \_ DS mancante per l' \_ \_ \_ att previsto**
</dt> <dd> <dl> <dt>

8411 (0x20DB)
</dt> <dt>



Manca un attributo previsto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERRORE \_ DS \_ NCName \_ mancante \_ \_ riferimento CR**
</dt> <dd> <dl> <dt>

8412 (0x20DC)
</dt> <dt>



Nel contesto di denominazione specificato manca un riferimento incrociato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**\_ \_ \_ errore controllo sicurezza DS \_ errore**
</dt> <dd> <dl> <dt>

8413 (0x20DD)
</dt> <dt>



Si è verificato un errore di controllo di sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**ERRORE \_ \_ schema DS \_ non \_ caricato**
</dt> <dd> <dl> <dt>

8414 (0x20DE)
</dt> <dt>



Lo schema non è caricato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERRORE \_ \_ \_ allocatore schema DS \_ non riuscito**
</dt> <dd> <dl> <dt>

8415 (0x20DF)
</dt> <dt>



Allocazione dello schema non riuscita. Verificare che la memoria del computer sia insufficiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERRORE nella sintassi della richiesta \_ \_ \_ dello schema DS att \_ \_**
</dt> <dd> <dl> <dt>

8416 (0x20E0)
</dt> <dt>



Impossibile ottenere la sintassi necessaria per lo schema dell'attributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**errore \_ \_ GCVERIFY DS \_**
</dt> <dd> <dl> <dt>

8417 (0x20E1)
</dt> <dt>



Verifica del catalogo globale non riuscita. Il catalogo globale non è disponibile o non supporta l'operazione. Una parte della directory non è attualmente disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERRORE \_ di \_ schema DRA di DS non \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

8418 (0x20E2)
</dt> <dt>



L'operazione di replica non è riuscita a causa di una mancata corrispondenza dello schema tra i server necessari.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERRORE \_ DS \_ non \_ trovato \_ DSA \_ obj**
</dt> <dd> <dl> <dt>

8419 (0x20E3)
</dt> <dt>



Impossibile trovare l'oggetto DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**errore durante la ricerca del controller di dominio per l'errore \_ DS \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

8420 (0x20E4)
</dt> <dt>



Impossibile trovare il contesto dei nomi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERRORE \_ DS \_ \_ trovare \_ NC \_ nella \_ cache**
</dt> <dd> <dl> <dt>

8421 (0x20E5)
</dt> <dt>



Il contesto dei nomi non è stato trovato nella cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**errore durante il \_ \_ recupero dell' \_ \_ elemento figlio di DS**
</dt> <dd> <dl> <dt>

8422 (0x20E6)
</dt> <dt>



Impossibile recuperare l'oggetto figlio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERRORE \_ di \_ sicurezza DS- \_ modifica non valida \_**
</dt> <dd> <dl> <dt>

8423 (0x20E7)
</dt> <dt>



La modifica non è consentita per motivi di sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERRORE \_ DS \_ cant \_ Replace \_ Hidden \_ REC**
</dt> <dd> <dl> <dt>

8424 (0x20E8)
</dt> <dt>



L'operazione non è in grado di sostituire il record nascosto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERRORE \_ DS \_ \_ file di gerarchia non valido \_**
</dt> <dd> <dl> <dt>

8425 (0x20E9)
</dt> <dt>



Il file della gerarchia non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERRORE \_ nella \_ \_ tabella della gerarchia di compilazione \_ DS \_**
</dt> <dd> <dl> <dt>

8426 (0x20EA)
</dt> <dt>



Tentativo di compilazione della tabella della gerarchia non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**ERRORE \_ \_ param configurazione \_ DS \_ mancante**
</dt> <dd> <dl> <dt>

8427 (0x20EB)
</dt> <dt>



Il parametro di configurazione della directory non è presente nel registro di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERRORE \_ DS durante il \_ conteggio degli \_ \_ indici AB \_ non riuscito**
</dt> <dd> <dl> <dt>

8428 (0x20EC)
</dt> <dt>



Il tentativo di conteggio degli indici di Rubrica non è riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERRORE \_ \_ malloc tabella della gerarchia DS \_ \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

8429 (0x20ED)
</dt> <dt>



Impossibile allocare la tabella della gerarchia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERRORE \_ interno DS errore \_ \_**
</dt> <dd> <dl> <dt>

8430 (0x20EE)
</dt> <dt>



Si è verificato un errore interno del servizio directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**errore di \_ DS \_ sconosciuto \_**
</dt> <dd> <dl> <dt>

8431 (0x20EF)
</dt> <dt>



Il servizio directory ha rilevato un errore sconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**l' \_ errore \_ radice DS \_ richiede la \_ classe \_ Top**
</dt> <dd> <dl> <dt>

8432 (0x20F0)
</dt> <dt>



Un oggetto radice richiede una classe di "Top".


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERRORE \_ DS che \_ rifiuta \_ i \_ ruoli FSMO**
</dt> <dd> <dl> <dt>

8433 (0x20F1)
</dt> <dt>



Questo server di directory viene arrestato e non è in grado di assumere la proprietà di nuovi ruoli di operazione a master singolo a virgola mobile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**ERRORE \_ DS \_ \_ Impostazioni FSMO \_ mancanti**
</dt> <dd> <dl> <dt>

8434 (0x20F2)
</dt> <dt>



Nel servizio directory mancano le informazioni di configurazione obbligatorie e non è in grado di determinare la proprietà dei ruoli di operazione a master singolo a virgola mobile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERRORE \_ DS \_ non è \_ in grado di \_ cedere i \_ ruoli**
</dt> <dd> <dl> <dt>

8435 (0x20F3)
</dt> <dt>



Il servizio directory non è stato in grado di trasferire la proprietà di uno o più ruoli di operazione a master singolo mobili ad altri server.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERRORE \_ DS \_ DRA \_ generico**
</dt> <dd> <dl> <dt>

8436 (0x20F4)
</dt> <dt>



Operazione di replica non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERRORE \_ DS \_ DRA \_ - \_ parametro non valido**
</dt> <dd> <dl> <dt>

8437 (0x20F5)
</dt> <dt>



Parametro non valido specificato per l'operazione di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERRORE \_ DS \_ DS \_ occupato**
</dt> <dd> <dl> <dt>

8438 (0x20F6)
</dt> <dt>



Il servizio directory è troppo occupato per completare l'operazione di replica in questo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERRORE \_ DS \_ DRA \_ errato \_ DN**
</dt> <dd> <dl> <dt>

8439 (0x20F7)
</dt> <dt>



Il nome distinto specificato per l'operazione di replica non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERRORE \_ DS \_ DRA \_ errato \_ NC**
</dt> <dd> <dl> <dt>

8440 (0x20F8)
</dt> <dt>



Il contesto dei nomi specificato per l'operazione di replica non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERRORE \_ del \_ DN DRA DS \_ \_ esistente**
</dt> <dd> <dl> <dt>

8441 (0x20F9)
</dt> <dt>



Il nome distinto specificato per questa operazione di replica esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**errore \_ \_ interno DRA \_ DS \_ errore**
</dt> <dd> <dl> <dt>

8442 (0x20FA)
</dt> <dt>



Si è verificato un errore interno del sistema di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERRORE \_ DS \_ DRA \_ incoerente \_ dit**
</dt> <dd> <dl> <dt>

8443 (0x20FB)
</dt> <dt>



L'operazione di replica ha rilevato un'incoerenza del database.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERRORE \_ di \_ connessione DRA DS \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

8444 (0x20FC)
</dt> <dt>



Impossibile contattare il server specificato per l'operazione di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**\_tipo di \_ \_ istanza non \_ valida \_ del servizio di dominio errore DS**
</dt> <dd> <dl> <dt>

8445 (0x20FD)
</dt> <dt>



L'operazione di replica ha rilevato un oggetto con un tipo di istanza non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERRORE servizi \_ di dominio Active Directory- \_ \_ out \_ di \_ MEM**
</dt> <dd> <dl> <dt>

8446 (0x20FE)
</dt> <dt>



L'operazione di replica non è riuscita ad allocare memoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**\_problema di \_ \_ posta DRA di DS \_ errore**
</dt> <dd> <dl> <dt>

8447 (0x20FF)
</dt> <dt>



L'operazione di replica ha rilevato un errore con il sistema di posta elettronica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**ERRORE \_ di \_ riferimento DRA DS \_ \_ già \_ esistente**
</dt> <dd> <dl> <dt>

8448 (0x2100)
</dt> <dt>



Le informazioni di riferimento per la replica per il server di destinazione esistono già.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERRORE \_ di \_ riferimento DRA DS \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

8449 (0x2101)
</dt> <dt>



Le informazioni di riferimento per la replica per il server di destinazione non esistono.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERRORE \_ DS \_ DRA \_ obj \_ is \_ Rep \_ source**
</dt> <dd> <dl> <dt>

8450 (0x2102)
</dt> <dt>



Il contesto dei nomi non può essere rimosso perché viene replicato in un altro server.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**errore \_ del \_ database DRA di DS \_ errore \_**
</dt> <dd> <dl> <dt>

8451 (0x2103)
</dt> <dt>



Si è verificato un errore di database durante l'operazione di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERRORE \_ DS \_ DRA \_ Nessuna \_ replica**
</dt> <dd> <dl> <dt>

8452 (0x2104)
</dt> <dt>



Il contesto dei nomi è in corso di rimozione o non viene replicato dal server specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERRORE \_ \_ accesso DRA \_ DS \_ negato**
</dt> <dd> <dl> <dt>

8453 (0x2105)
</dt> <dt>



Accesso alla replica negato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**\_ \_ DRA non è \_ \_ supportato per l'errore DS**
</dt> <dd> <dl> <dt>

8454 (0x2106)
</dt> <dt>



L'operazione richiesta non è supportata da questa versione del servizio directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERRORE \_ \_ RPC DRA \_ \_ annullato**
</dt> <dd> <dl> <dt>

8455 (0x2107)
</dt> <dt>



La chiamata di procedura remota di replica è stata annullata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**ERRORE \_ \_ \_ codice sorgente DRA \_ disabilitato**
</dt> <dd> <dl> <dt>

8456 (0x2108)
</dt> <dt>



Il server di origine rifiuta attualmente le richieste di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERRORE \_ del \_ sink DRA DS \_ \_ disabilitato**
</dt> <dd> <dl> <dt>

8457 (0x2109)
</dt> <dt>



Il server di destinazione rifiuta le richieste di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**ERRORE \_ \_ \_ : conflitto nome DRA DS \_**
</dt> <dd> <dl> <dt>

8458 (0x210A)
</dt> <dt>



L'operazione di replica non è riuscita a causa di un conflitto di nomi di oggetti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERRORE \_ \_ \_ codice sorgente DRA \_ reinstallato**
</dt> <dd> <dl> <dt>

8459 (0x210B)
</dt> <dt>



L'origine della replica è stata reinstallata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERRORE \_ del \_ DRA DS \_ mancante \_**
</dt> <dd> <dl> <dt>

8460 (0x210C)
</dt> <dt>



L'operazione di replica non è riuscita perché manca un oggetto padre obbligatorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERRORE \_ DS \_ DRA \_ interrotto**
</dt> <dd> <dl> <dt>

8461 (0x210D)
</dt> <dt>



L'operazione di replica è stata interrotta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERRORE servizi di \_ dominio Active Directory per errore \_ \_ \_**
</dt> <dd> <dl> <dt>

8462 (0x210E)
</dt> <dt>



Il tentativo di sincronizzazione della replica è stato abbandonato a causa di una mancanza di aggiornamenti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERRORE \_ di \_ arresto DRA DS \_**
</dt> <dd> <dl> <dt>

8463 (0x210F)
</dt> <dt>



L'operazione di replica è stata interrotta perché è in corso l'arresto del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERRORE \_ DS \_ DRA \_ incompatibile \_ \_ set parziale**
</dt> <dd> <dl> <dt>

8464 (0x2110)
</dt> <dt>



Tentativo di sincronizzazione non riuscito perché il controller di dominio di destinazione è attualmente in attesa di sincronizzare nuovi attributi parziali dall'origine. Questa condizione è normale se una modifica dello schema recente ha modificato il set di attributi parziali. Il set di attributi parziali di destinazione non è un subset del set di attributi parziali di origine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**ERRORE \_ DS \_ \_ origine DRA \_ è \_ una \_ replica parziale**
</dt> <dd> <dl> <dt>

8465 (0x2111)
</dt> <dt>



Il tentativo di sincronizzazione della replica non è riuscito perché una replica master ha tentato di eseguire la sincronizzazione da una replica parziale.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERRORE \_ di \_ connessione Extn DRA di DS \_ \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

8466 (0x2112)
</dt> <dt>



Il server specificato per l'operazione di replica è stato contattato, ma il server non è stato in grado di contattare un server aggiuntivo necessario per completare l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERRORE \_ schema di installazione di DS non \_ \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

8467 (0x2113)
</dt> <dt>



La versione dello schema del servizio directory della foresta di origine non è compatibile con la versione del servizio directory nel computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**\_ \_ ID collegamento duplicato errore DS \_ \_**
</dt> <dd> <dl> <dt>

8468 (0x2114)
</dt> <dt>



Aggiornamento dello schema non riuscito: esiste già un attributo con lo stesso identificatore di collegamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**errore durante la risoluzione del \_ \_ nome DS \_ \_**
</dt> <dd> <dl> <dt>

8469 (0x2115)
</dt> <dt>



Traduzione del nome: errore di elaborazione generica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**\_errore di nome DS per errori \_ \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

8470 (0x2116)
</dt> <dt>



Traduzione del nome: non è stato possibile trovare il nome o il diritto insufficiente per visualizzare il nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**errore \_ \_ nome DS \_ \_ non \_ univoco**
</dt> <dd> <dl> <dt>

8471 (0x2117)
</dt> <dt>



Traduzione del nome: nome di input mappato a più di un nome di output.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**errore \_ \_ nome DS \_ errore \_ nessun \_ mapping**
</dt> <dd> <dl> <dt>

8472 (0x2118)
</dt> <dt>



Traduzione del nome: il nome di input è stato trovato, ma non il formato di output associato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERRORE \_ DS \_ nome \_ \_ dominio \_ solo errore**
</dt> <dd> <dl> <dt>

8473 (0x2119)
</dt> <dt>



Traduzione del nome: Impossibile risolvere completamente, è stato trovato solo il dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**errore \_ \_ nome DS \_ errore \_ nessun \_ mapping sintattico \_**
</dt> <dd> <dl> <dt>

8474 (0x211A)
</dt> <dt>



Traduzione del nome: non è possibile eseguire il mapping puramente sintattico al client senza passare alla rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERRORE \_ \_ mod di \_ att \_ costruito DS**
</dt> <dd> <dl> <dt>

8475 (0x211B)
</dt> <dt>



La modifica di un attributo costruito non è consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**ERRORE \_ DS \_ - \_ \_ classe om obj \_ non corretta**
</dt> <dd> <dl> <dt>

8476 (0x211C)
</dt> <dt>



La classe OM-Object-Object specificata non è corretta per un attributo con la sintassi specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERRORE \_ \_ REPL DRA \_ \_ in sospeso**
</dt> <dd> <dl> <dt>

8477 (0x211D)
</dt> <dt>



La richiesta di replica è stata inviata. in attesa di risposta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERRORE \_ DS \_ DS \_ obbligatorio**
</dt> <dd> <dl> <dt>

8478 (0x211E)
</dt> <dt>



L'operazione richiesta richiede un servizio directory e nessuno è disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERRORE \_ DS \_ \_ \_ nome visualizzato LDAP non valido \_**
</dt> <dd> <dl> <dt>

8479 (0x211F)
</dt> <dt>



Il nome visualizzato LDAP della classe o dell'attributo contiene caratteri non ASCII.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERRORE \_ DS \_ - \_ ricerca non di base \_**
</dt> <dd> <dl> <dt>

8480 (0x2120)
</dt> <dt>



L'operazione di ricerca richiesta è supportata solo per le ricerche di base.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERRORE \_ di \_ \_ recupero \_ atts di DS**
</dt> <dd> <dl> <dt>

8481 (0x2121)
</dt> <dt>



La ricerca non è riuscita a recuperare gli attributi dal database.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERRORE \_ DS \_ BACKLINK \_ senza \_ collegamento**
</dt> <dd> <dl> <dt>

8482 (0x2122)
</dt> <dt>



L'operazione di aggiornamento dello schema ha tentato di aggiungere un attributo di collegamento a ritroso che non dispone di un collegamento in avanti corrispondente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERRORE \_ DS \_ Epoch non \_ corrispondente**
</dt> <dd> <dl> <dt>

8483 (0x2123)
</dt> <dt>



L'origine e la destinazione di uno spostamento tra domini non concordano sul numero di Epoch dell'oggetto. L'origine o la destinazione non dispone della versione più recente dell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERRORE \_ \_ nome src DS non \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

8484 (0x2124)
</dt> <dt>



L'origine e la destinazione di uno spostamento tra domini non concordano sul nome corrente dell'oggetto. L'origine o la destinazione non dispone della versione più recente dell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERRORE \_ DS \_ src \_ ed \_ DST \_ NC \_ identico**
</dt> <dd> <dl> <dt>

8485 (0x2125)
</dt> <dt>



L'origine e la destinazione per l'operazione di spostamento tra domini sono identiche. Il chiamante deve usare un'operazione di spostamento locale anziché un'operazione di spostamento tra domini.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERRORE \_ \_ NC DS DST non \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

8486 (0x2126)
</dt> <dt>



L'origine e la destinazione di uno spostamento tra domini non sono concordate sui contesti di denominazione della foresta. L'origine o la destinazione non dispone della versione più recente del contenitore di partizioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERRORE \_ DS \_ non \_ autorevole \_ per \_ \_ NC DST**
</dt> <dd> <dl> <dt>

8487 (0x2127)
</dt> <dt>



La destinazione di uno spostamento tra domini non è autorevole per il contesto dei nomi di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERRORE \_ DS \_ src \_ GUID non \_ corrispondente**
</dt> <dd> <dl> <dt>

8488 (0x2128)
</dt> <dt>



L'origine e la destinazione di uno spostamento tra domini non concordano sull'identità dell'oggetto di origine. L'origine o la destinazione non dispone della versione più recente dell'oggetto di origine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERRORE \_ di \_ spostamento del cant DS \_ \_ \_ oggetto eliminato**
</dt> <dd> <dl> <dt>

8489 (0x2129)
</dt> <dt>



L'oggetto spostato tra domini è già noto per essere eliminato dal server di destinazione. Il server di origine non dispone della versione più recente dell'oggetto di origine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**\_ \_ operazione PDC errore \_ DS \_ in \_ corso**
</dt> <dd> <dl> <dt>

8490 (0x212A)
</dt> <dt>



È già in corso un'altra operazione che richiede l'accesso esclusivo al FSMO PDC.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERRORE \_ DS \_ tra \_ domini \_ pulizia \_ reqd**
</dt> <dd> <dl> <dt>

8491 (0x212B)
</dt> <dt>



Un'operazione di spostamento tra domini non è riuscita perché esistono due versioni dell'oggetto spostato, una per ciascuna nei domini di origine e di destinazione. Per ripristinare lo stato coerente del sistema, è necessario rimuovere l'oggetto di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERRORE \_ DS \_ \_ XDOM \_ operazione di spostamento non valida \_**
</dt> <dd> <dl> <dt>

8492 (0x212C)
</dt> <dt>



Questo oggetto non può essere spostato tra i limiti del dominio perché gli spostamenti tra domini per questa classe non sono consentiti oppure l'oggetto presenta alcune caratteristiche speciali, ad esempio: account attendibile o RID con restrizioni, che ne impediscono lo spostamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERRORE \_ \_ di DS \_ con \_ il \_ gruppo Acct \_ MEMBERSHPS**
</dt> <dd> <dl> <dt>

8493 (0x212D)
</dt> <dt>



Non è possibile spostare gli oggetti con appartenenze tra i limiti di dominio come dopo lo spostamento. ciò violerebbe le condizioni di appartenenza del gruppo di account. Rimuovere l'oggetto da qualsiasi appartenenza a un gruppo di account e riprovare.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**ERRORE per il controller di \_ dominio DS \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

8494 (0x212E)
</dt> <dt>



Un'intestazione del contesto dei nomi deve essere l'elemento figlio immediato di un'altra intestazione del contesto dei nomi, non di un nodo interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERRORE \_ DS \_ CR \_ Impossibile \_ \_ convalidare**
</dt> <dd> <dl> <dt>

8495 (0x212F)
</dt> <dt>



La directory non è in grado di convalidare il nome del contesto di denominazione proposto perché non dispone di una replica del contesto dei nomi sopra il contesto dei nomi proposto. Verificare che il ruolo di master per la denominazione dei domini sia gestito da un server configurato come server di catalogo globale e che il server sia aggiornato con i partner di replica. (Si applica solo ai master per la denominazione dei domini di Windows 2000).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERRORE \_ DS \_ DST \_ Domain \_ Not \_ native**
</dt> <dd> <dl> <dt>

8496 (0x2130)
</dt> <dt>



Il dominio di destinazione deve essere in modalità nativa.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERRORE \_ DS \_ \_ contenitore infrastruttura \_ mancante**
</dt> <dd> <dl> <dt>

8497 (0x2131)
</dt> <dt>



Non è possibile eseguire l'operazione perché il server non dispone di un contenitore di infrastruttura nel dominio di interesse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERRORE per lo \_ \_ spostamento del \_ \_ gruppo di account \_ di DS**
</dt> <dd> <dl> <dt>

8498 (0x2132)
</dt> <dt>



Lo spostamento tra domini di gruppi di account non vuoti non è consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERRORE \_ DS \_ Impossibile \_ spostare \_ il \_ gruppo di risorse**
</dt> <dd> <dl> <dt>

8499 (0x2133)
</dt> <dt>



Lo spostamento tra domini di gruppi di risorse non vuoti non è consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**ERRORE \_ DS \_ - \_ flag di ricerca non valido \_**
</dt> <dd> <dl> <dt>

8500 (0x2134)
</dt> <dt>



I flag di ricerca per l'attributo non sono validi. Il bit ANR è valido solo per gli attributi delle stringhe Unicode o Teletex.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERRORE \_ DS \_ No \_ Tree \_ Delete \_ sopra \_ NC**
</dt> <dd> <dl> <dt>

8501 (0x2135)
</dt> <dt>



Non sono consentite eliminazioni di albero a partire da un oggetto che ha un capo NC come discendente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERRORE \_ \_ \_ \_ dell'albero di blocco couldnt DS \_ per l' \_ eliminazione**
</dt> <dd> <dl> <dt>

8502 (0x2136)
</dt> <dt>



Il servizio directory non è riuscito a bloccare un albero per preparare l'eliminazione di un albero perché l'albero era in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERRORE \_ DS \_ couldnt \_ identificare \_ gli oggetti \_ per l' \_ eliminazione della struttura ad albero \_**
</dt> <dd> <dl> <dt>

8503 (0x2137)
</dt> <dt>



Il servizio directory non è riuscito a identificare l'elenco di oggetti da eliminare durante il tentativo di eliminazione di un albero.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERRORE \_ di \_ \_ inizializzazione Sam DS \_ errore**
</dt> <dd> <dl> <dt>

8504 (0x2138)
</dt> <dt>



Inizializzazione gestione account di sicurezza non riuscita a causa dell'errore seguente: %1. Stato di errore: 0x %2. Arrestare il sistema e riavviare in modalità ripristino servizi directory. per informazioni più dettagliate, vedere il registro eventi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**\_violazione del \_ \_ gruppo sensibile DS con \_ errori**
</dt> <dd> <dl> <dt>

8505 (0x2139)
</dt> <dt>



Solo un amministratore può modificare l'elenco di appartenenze di un gruppo amministrativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERRORE \_ \_ mod. cant DS \_ \_ PRIMARYGROUPID**
</dt> <dd> <dl> <dt>

8506 (0x213A)
</dt> <dt>



Impossibile modificare l'ID gruppo primario di un account del controller di dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERRORE \_ DS \_ schema di base non valido \_ \_ \_ mod**
</dt> <dd> <dl> <dt>

8507 (0x213B)
</dt> <dt>



Viene effettuato un tentativo di modificare lo schema di base.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**\_ \_ \_ modifica dello schema non sicuro DS di errore \_**
</dt> <dd> <dl> <dt>

8508 (0x213C)
</dt> <dt>



Aggiunta di un nuovo attributo obbligatorio a una classe esistente, eliminazione di un attributo obbligatorio da una classe esistente o aggiunta di un attributo facoltativo alla classe speciale top che non è un attributo backlink (direttamente o tramite ereditarietà, ad esempio, aggiungendo o eliminando una classe ausiliaria) non è consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERRORE \_ di \_ aggiornamento dello schema DS non \_ \_ consentito**
</dt> <dd> <dl> <dt>

8509 (0x213D)
</dt> <dt>



Aggiornamento dello schema non consentito in questo controller di dominio perché il controller di dominio non è il proprietario del ruolo FSMO dello schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERRORE durante la \_ \_ creazione del cant DS \_ \_ nello \_ schema**
</dt> <dd> <dl> <dt>

8510 (0x213E)
</dt> <dt>



Non è possibile creare un oggetto di questa classe nel contenitore dello schema. Nel contenitore dello schema è possibile creare solo oggetti Attribute-schema e classe-schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERRORE \_ DS \_ installazione \_ Nessuna \_ \_ versione src SCH \_**
</dt> <dd> <dl> <dt>

8511 (0x213F)
</dt> <dt>



L'installazione della replica/figlio non è riuscita a ottenere l'attributo objectVersion nel contenitore dello schema sul controller di dominio di origine. L'attributo non è presente nel contenitore dello schema oppure le credenziali specificate non dispongono dell'autorizzazione per leggerlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERRORE \_ DS \_ installazione \_ Nessuna \_ \_ versione SCH \_ in \_ inifile**
</dt> <dd> <dl> <dt>

8512 (0x2140)
</dt> <dt>



L'installazione della replica/figlio non è riuscita a leggere l'attributo objectVersion nella sezione dello SCHEMA del file schema.ini nella directory system32.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERRORE \_ DS \_ \_ tipo di gruppo non valido \_**
</dt> <dd> <dl> <dt>

8513 (0x2141)
</dt> <dt>



Il tipo di gruppo specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERRORE \_ DS \_ nessun \_ annidamento \_ GLOBALGROUP \_ in \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8514 (0x2142)
</dt> <dt>



Non è possibile nidificare i gruppi globali in un dominio misto se il gruppo è abilitato per la sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERRORE \_ DS \_ nessun \_ annidamento \_ localgroup \_ in \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8515 (0x2143)
</dt> <dt>



Non è possibile nidificare i gruppi locali in un dominio misto se il gruppo è abilitato per la sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERRORE \_ DS \_ globale \_ non \_ presente \_ con \_ membro locale**
</dt> <dd> <dl> <dt>

8516 (0x2144)
</dt> <dt>



Un gruppo globale non può avere un gruppo locale come membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERRORE \_ DS \_ Global \_ cant \_ con \_ \_ membro universale**
</dt> <dd> <dl> <dt>

8517 (0x2145)
</dt> <dt>



Un gruppo globale non può avere un gruppo universale come membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERRORE \_ DS \_ universale \_ non \_ può \_ avere \_ membro locale**
</dt> <dd> <dl> <dt>

8518 (0x2146)
</dt> <dt>



Un gruppo universale non può avere un gruppo locale come membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERRORE \_ DS \_ Global \_ cant \_ con \_ \_ membro CROSSDOMAIN**
</dt> <dd> <dl> <dt>

8519 (0x2147)
</dt> <dt>



Un gruppo globale non può avere un membro tra domini.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERRORE nel servizio \_ locale DS con \_ \_ \_ \_ CROSSDOMAIN \_ \_ membro locale**
</dt> <dd> <dl> <dt>

8520 (0x2148)
</dt> <dt>



Un gruppo locale non può avere un altro gruppo locale tra domini come membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**ERRORE \_ DS \_ con \_ \_ membri primari**
</dt> <dd> <dl> <dt>

8521 (0x2149)
</dt> <dt>



Un gruppo con membri primari non può essere modificato in un gruppo disabilitato per la sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERRORE \_ di \_ \_ conversione SD stringa DS \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

8522 (0x214A)
</dt> <dt>



Il caricamento della cache dello schema non è riuscito a convertire la stringa SD predefinita in un oggetto dello schema di classe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERRORE \_ GC per la \_ denominazione \_ Master DS \_**
</dt> <dd> <dl> <dt>

8523 (0x214B)
</dt> <dt>



Solo DSA configurato come server di catalogo globale deve essere autorizzato a contenere il ruolo FSMO master per la denominazione dei domini. (Si applica solo ai server Windows 2000).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERRORE \_ di \_ ricerca DNS DS \_ errore \_**
</dt> <dd> <dl> <dt>

8524 (0x214C)
</dt> <dt>



Non è possibile continuare l'operazione DSA a causa di un errore di ricerca DNS.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**ERRORE \_ \_ \_ SPN aggiornamento couldnt \_ DS**
</dt> <dd> <dl> <dt>

8525 (0x214D)
</dt> <dt>



Durante l'elaborazione di una modifica al nome host DNS per un oggetto, i valori del nome dell'entità servizio non possono essere mantenuti sincronizzati.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERRORE \_ di \_ \_ recupero \_ SD**
</dt> <dd> <dl> <dt>

8526 (0x214E)
</dt> <dt>



Impossibile leggere l'attributo del descrittore di sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERRORE \_ \_ chiave DS \_ non \_ univoca**
</dt> <dd> <dl> <dt>

8527 (0x214F)
</dt> <dt>



L'oggetto richiesto non è stato trovato, ma è stato trovato un oggetto con tale chiave.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERRORE \_ DS \_ - \_ \_ sintassi att \_ collegata errata**
</dt> <dd> <dl> <dt>

8528 (0x2150)
</dt> <dt>



La sintassi dell'attributo collegato aggiunto non è corretta. I collegamenti in diretta possono avere solo la sintassi 2.5.5.1, 2.5.5.7 e 2.5.5.14 e i backlink possono avere solo la sintassi 2.5.5.1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERRORE \_ DS \_ Sam \_ need \_ BOOTKEY \_ password**
</dt> <dd> <dl> <dt>

8529 (0x2151)
</dt> <dt>



Security Account Manager deve ottenere la password di avvio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERRORE \_ DS \_ Sam \_ need \_ \_ floppy BOOTKEY**
</dt> <dd> <dl> <dt>

8530 (0x2152)
</dt> <dt>



Security Account Manager deve ottenere la chiave di avvio dal disco floppy.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERRORE \_ di \_ avvio del cant DS \_**
</dt> <dd> <dl> <dt>

8531 (0x2153)
</dt> <dt>



Impossibile avviare il servizio directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERRORE \_ di \_ init DS errore \_**
</dt> <dd> <dl> <dt>

8532 (0x2154)
</dt> <dt>



Impossibile avviare i servizi directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERRORE \_ DS \_ No \_ PKT \_ privacy \_ on \_ Connection**
</dt> <dd> <dl> <dt>

8533 (0x2155)
</dt> <dt>



Per la connessione tra client e server è richiesta la riservatezza dei pacchetti o una soluzione migliore.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERRORE \_ \_ \_ dominio di origine DS \_ nella \_ foresta**
</dt> <dd> <dl> <dt>

8534 (0x2156)
</dt> <dt>



Il dominio di origine potrebbe non trovarsi nella stessa foresta della destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERRORE \_ \_ \_ dominio di destinazione DS non presente \_ \_ nella \_ foresta**
</dt> <dd> <dl> <dt>

8535 (0x2157)
</dt> <dt>



Il dominio di destinazione deve essere presente nell'insieme di strutture.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**controllo della destinazione di DS con errori \_ \_ \_ \_ non \_ abilitato**
</dt> <dd> <dl> <dt>

8536 (0x2158)
</dt> <dt>



Per l'operazione è necessario che sia abilitato il controllo del dominio di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERRORE \_ DS \_ \_ trovare il \_ controller \_ di \_ dominio per il \_ dominio src**
</dt> <dd> <dl> <dt>

8537 (0x2159)
</dt> <dt>



L'operazione non è riuscita a individuare un controller di dominio per il dominio di origine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERRORE \_ DS \_ src \_ obj \_ non \_ gruppo \_ o \_ utente**
</dt> <dd> <dl> <dt>

8538 (0x215A)
</dt> <dt>



L'oggetto di origine deve essere un gruppo o un utente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERRORE \_ il \_ SID src DS \_ \_ esiste \_ nella \_ foresta**
</dt> <dd> <dl> <dt>

8539 (0x215B)
</dt> <dt>



Il SID dell'oggetto di origine esiste già nella foresta di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERRORE \_ DS \_ src \_ e \_ DST \_ classe di oggetti non \_ \_ corrispondenti**
</dt> <dd> <dl> <dt>

8540 (0x215C)
</dt> <dt>



L'oggetto di origine e di destinazione deve essere dello stesso tipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERRORE \_ di \_ inizializzazione Sam \_**
</dt> <dd> <dl> <dt>

8541 (0x215D)
</dt> <dt>



Inizializzazione gestione account di sicurezza non riuscita a causa dell'errore seguente: %1. Stato di errore: 0x %2. Fare clic su OK per arrestare il sistema e riavviare in modalità provvisoria. Per informazioni dettagliate, vedere il registro eventi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERRORE \_ DS servizio di \_ \_ informazioni dello schema DRA \_ \_**
</dt> <dd> <dl> <dt>

8542 (0x215E)
</dt> <dt>



Non è stato possibile includere le informazioni sullo schema nella richiesta di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERRORE \_ \_ \_ dello schema DRA \_ DS**
</dt> <dd> <dl> <dt>

8543 (0x215F)
</dt> <dt>



Non è stato possibile completare l'operazione di replica a causa di un'incompatibilità dello schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERRORE \_ DS \_ DRA \_ precedente \_ \_ conflitto schema**
</dt> <dd> <dl> <dt>

8544 (0x2160)
</dt> <dt>



Non è stato possibile completare l'operazione di replica a causa di un'incompatibilità dello schema precedente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERRORE \_ DS \_ DRA \_ obj \_ NC non \_ corrispondente**
</dt> <dd> <dl> <dt>

8545 (0x2161)
</dt> <dt>



Non è stato possibile applicare l'aggiornamento della replica perché l'origine o la destinazione non ha ancora ricevuto informazioni relative a un'operazione di spostamento tra domini recente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**ERRORE del controller di \_ dominio DS \_ \_ \_ con \_ DSA**
</dt> <dd> <dl> <dt>

8546 (0x2162)
</dt> <dt>



Non è stato possibile eliminare il dominio richiesto perché esistono controller di dominio che ospitano ancora questo dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERRORE \_ \_ GC DS \_ obbligatorio**
</dt> <dd> <dl> <dt>

8547 (0x2163)
</dt> <dt>



L'operazione richiesta può essere eseguita solo in un server di catalogo globale.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERRORE \_ DS \_ locale \_ membro \_ locale \_ \_ solo locale**
</dt> <dd> <dl> <dt>

8548 (0x2164)
</dt> <dt>



Un gruppo locale può essere solo un membro di altri gruppi locali nello stesso dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERRORE \_ DS \_ Nessuna \_ Polinesia \_ nei \_ gruppi universali \_**
</dt> <dd> <dl> <dt>

8549 (0x2165)
</dt> <dt>



Le entità di sicurezza esterne non possono essere membri di gruppi universali.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERRORE \_ DS non è \_ \_ \_ possibile aggiungere a \_ GC**
</dt> <dd> <dl> <dt>

8550 (0x2166)
</dt> <dt>



Per motivi di sicurezza, l'attributo non può essere replicato nel catalogo globale.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERRORE \_ DS \_ nessun \_ Checkpoint \_ con \_ PDC**
</dt> <dd> <dl> <dt>

8551 (0x2167)
</dt> <dt>



Non è stato possibile usare il checkpoint con PDC perché il numero di modifiche attualmente elaborate è eccessivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**\_ \_ controllo origine errore DS \_ \_ non \_ abilitato**
</dt> <dd> <dl> <dt>

8552 (0x2168)
</dt> <dt>



Per l'operazione è necessario che sia abilitato il controllo del dominio di origine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERRORE \_ \_ durante la \_ creazione del cant DS \_ nel NC di non \_ dominio \_**
</dt> <dd> <dl> <dt>

8553 (0x2169)
</dt> <dt>



Gli oggetti entità di sicurezza possono essere creati solo all'interno di contesti di denominazione dei domini.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERRORE \_ DS \_ nome non valido \_ \_ per \_ SPN**
</dt> <dd> <dl> <dt>

8554 (0x216A)
</dt> <dt>



Non è stato possibile costruire un nome dell'entità servizio (SPN) perché il nome host specificato non è nel formato necessario.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**ERRORE \_ il \_ filtro DS \_ Usa \_ CONTRUCTED \_ attrs**
</dt> <dd> <dl> <dt>

8555 (0x216B)
</dt> <dt>



È stato passato un filtro che usa attributi costruiti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERRORE \_ \_ UNICODEPWD DS \_ non \_ tra \_ virgolette**
</dt> <dd> <dl> <dt>

8556 (0x216C)
</dt> <dt>



Il valore dell'attributo unicodePwd deve essere racchiuso tra virgolette doppie.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERRORE \_ di \_ \_ quota account computer DS \_ \_ superata**
</dt> <dd> <dl> <dt>

8557 (0x216D)
</dt> <dt>



Il computer non è stato aggiunto al dominio. È stato superato il numero massimo di account computer che è possibile creare in questo dominio. Contattare l'amministratore di sistema per impostare o aumentare il limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**\_ \_ è necessario eseguire l'errore DS \_ \_ \_ sul controller di dominio \_ DST \_**
</dt> <dd> <dl> <dt>

8558 (0x216E)
</dt> <dt>



Per motivi di sicurezza, è necessario eseguire l'operazione nel controller di dominio di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERRORE \_ DS \_ src \_ DC \_ deve \_ essere \_ SP4 \_ o \_ versione successiva**
</dt> <dd> <dl> <dt>

8559 (0x216F)
</dt> <dt>



Per motivi di sicurezza, il controller di dominio di origine deve essere NT4SP4 o superiore.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERRORE \_ di \_ \_ eliminazione dell'albero del cant \_ \_ critico \_ di DS**
</dt> <dd> <dl> <dt>

8560 (0x2170)
</dt> <dt>



Impossibile eliminare gli oggetti critici del sistema del servizio directory durante le operazioni di eliminazione della struttura ad albero. È possibile che l'eliminazione della struttura ad albero sia stata eseguita parzialmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERRORE \_ nella \_ console di inizializzazione non riuscita di DS \_ \_**
</dt> <dd> <dl> <dt>

8561 (0x2171)
</dt> <dt>



Impossibile avviare i servizi directory a causa del seguente errore: %1. Stato di errore: 0x %2. Per arrestare il sistema, fare clic su OK. È possibile usare la Console di ripristino di emergenza per diagnosticare più approfonditamente il problema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERRORE nella console di errore \_ DS \_ Sam \_ init \_ \_**
</dt> <dd> <dl> <dt>

8562 (0x2172)
</dt> <dt>



Inizializzazione gestione account di sicurezza non riuscita a causa dell'errore seguente: %1. Stato di errore: 0x %2. Per arrestare il sistema, fare clic su OK. È possibile usare la Console di ripristino di emergenza per diagnosticare più approfonditamente il problema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERRORE \_ \_ versione foresta \_ DS \_ troppo \_ elevata**
</dt> <dd> <dl> <dt>

8563 (0x2173)
</dt> <dt>



La versione del sistema operativo non è compatibile con il livello di funzionalità della foresta di servizi di dominio Active Directory corrente o il livello di funzionalità del set di configurazione AD LDS. È necessario eseguire l'aggiornamento a una nuova versione del sistema operativo prima che il server possa diventare un controller di dominio di servizi di dominio Active Directory o aggiungere un'istanza di AD LDS in questa foresta di servizi di dominio Active Directory o AD LDS set di configurazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERRORE \_ \_ versione dominio \_ DS \_ troppo \_ alta**
</dt> <dd> <dl> <dt>

8564 (0x2174)
</dt> <dt>



La versione del sistema operativo installata non è compatibile con il livello di funzionalità del dominio corrente. È necessario eseguire l'aggiornamento a una nuova versione del sistema operativo prima che il server possa diventare un controller di dominio in questo dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERRORE \_ \_ versione foresta \_ DS \_ troppo \_ bassa**
</dt> <dd> <dl> <dt>

8565 (0x2175)
</dt> <dt>



La versione del sistema operativo installata in questo server non supporta più il livello di funzionalità della foresta di servizi di dominio Active Directory corrente o il livello di funzionalità del set di configurazione AD LDS. È necessario aumentare il livello di funzionalità della foresta di Active Directory Domain Services o AD LDS il livello di funzionalità del set di configurazione prima che il server possa diventare un controller di dominio di servizi di dominio Active Directory o un'istanza AD LDS in questa foresta o set


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERRORE \_ \_ versione dominio \_ DS \_ troppo \_ basso**
</dt> <dd> <dl> <dt>

8566 (0x2176)
</dt> <dt>



La versione del sistema operativo installata in questo server non supporta più il livello di funzionalità del dominio corrente. È necessario aumentare il livello di funzionalità del dominio prima che il server possa diventare un controller di dominio in questo dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**\_versione non \_ compatibile DS degli errori \_**
</dt> <dd> <dl> <dt>

8567 (0x2177)
</dt> <dt>



La versione del sistema operativo installata in questo server non è compatibile con il livello di funzionalità del dominio o della foresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERRORE \_ DS \_ \_ versione bassa DSA \_**
</dt> <dd> <dl> <dt>

8568 (0x2178)
</dt> <dt>



Non è possibile aumentare il livello di funzionalità del dominio (o della foresta) al valore richiesto perché esistono uno o più controller di dominio nel dominio o nella foresta con un livello di funzionalità non compatibile più basso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERRORE \_ DS \_ Nessuna \_ \_ versione \_ del comportamento in \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8569 (0x2179)
</dt> <dt>



Impossibile elevare il livello di funzionalità della foresta al valore richiesto perché uno o più domini sono ancora in modalità di dominio misto. Tutti i domini nella foresta devono essere in modalità nativa, in modo da aumentare il livello di funzionalità della foresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ERRORE \_ DS \_ non \_ supportato \_ per il tipo di ordinamento \_**
</dt> <dd> <dl> <dt>

8570 (0x217A)
</dt> <dt>



Il tipo di ordinamento richiesto non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**ERRORE \_ \_ nome DS \_ non \_ univoco**
</dt> <dd> <dl> <dt>

8571 (0x217B)
</dt> <dt>



Il nome richiesto esiste già come identificatore univoco.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERRORE \_ dell' \_ account computer DS \_ \_ creato \_ PRENT4**
</dt> <dd> <dl> <dt>

8572 (0x217C)
</dt> <dt>



L'account del computer è stato creato prima di NT4. È necessario ricreare l'account.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERRORE \_ DS \_ dall' \_ \_ Archivio delle versioni \_**
</dt> <dd> <dl> <dt>

8573 (0x217D)
</dt> <dt>



Il database non è presente nell'archivio delle versioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**controlli di errore \_ DS \_ incompatibili \_ \_ utilizzati**
</dt> <dd> <dl> <dt>

8574 (0x217E)
</dt> <dt>



Non è possibile continuare l'operazione perché sono stati usati più controlli in conflitto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERRORE \_ DS \_ nessun \_ dominio di riferimento \_**
</dt> <dd> <dl> <dt>

8575 (0x217F)
</dt> <dt>



Impossibile trovare un dominio di riferimento del descrittore di sicurezza valido per questa partizione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**\_ \_ \_ ID collegamento riservato DS \_ errore**
</dt> <dd> <dl> <dt>

8576 (0x2180)
</dt> <dt>



Aggiornamento dello schema non riuscito: l'identificatore di collegamento è riservato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**\_ \_ ID collegamento DS \_ errore \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

8577 (0x2181)
</dt> <dt>



Aggiornamento dello schema non riuscito: non sono disponibili identificatori di collegamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERRORE \_ DS \_ AG \_ cant \_ con \_ \_ membro universale**
</dt> <dd> <dl> <dt>

8578 (0x2182)
</dt> <dt>



Un gruppo di account non può avere un gruppo universale come membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERRORE \_ DS \_ MODIFYDN del non \_ consentito \_ dal \_ tipo di istanza \_**
</dt> <dd> <dl> <dt>

8579 (0x2183)
</dt> <dt>



Non sono consentite operazioni di ridenominazione o spostamento in intestazioni di contesto dei nomi o oggetti di sola lettura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERRORE \_ DS \_ nessun \_ oggetto \_ spostamento \_ nel \_ NC dello schema \_**
</dt> <dd> <dl> <dt>

8580 (0x2184)
</dt> <dt>



Non sono consentite operazioni di spostamento sugli oggetti nel contesto dei nomi di schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERRORE \_ DS \_ MODIFYDN del non \_ consentito \_ dal \_ flag**
</dt> <dd> <dl> <dt>

8581 (0x2185)
</dt> <dt>



Un flag di sistema è stato impostato sull'oggetto e non consente lo spostamento o la ridenominazione dell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERRORE \_ DS \_ MODIFYDN del \_ \_ padre errato**
</dt> <dd> <dl> <dt>

8582 (0x2186)
</dt> <dt>



Questo oggetto non è autorizzato a modificare il relativo contenitore padre. Lo spostamento non è consentito per questo oggetto, ma è limitato ai contenitori di pari livello.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERRORE \_ \_ nome servizio \_ DS \_ \_**
</dt> <dd> <dl> <dt>

8583 (0x2187)
</dt> <dt>



Impossibile risolvere completamente, viene generato un riferimento a un'altra foresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERRORE \_ non \_ supportato \_ nel \_ \_ server standard**
</dt> <dd> <dl> <dt>

8584 (0x2188)
</dt> <dt>



L'azione richiesta non è supportata nel server standard.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERRORE \_ \_ \_ di accesso non è possibile accedere \_ a una \_ parte remota \_ di \_ Active Directory**
</dt> <dd> <dl> <dt>

8585 (0x2189)
</dt> <dt>



Non è stato possibile accedere a una partizione del servizio directory che si trova in un server remoto. Assicurarsi che almeno un server sia in esecuzione per la partizione in questione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERRORE \_ DS \_ CR \_ Impossibile \_ \_ convalidare \_ v2**
</dt> <dd> <dl> <dt>

8586 (0x218A)
</dt> <dt>



La directory non può convalidare il nome del contesto dei nomi proposto (o partizione) perché non è presente una replica né può contattare una replica del contesto dei nomi sopra il contesto dei nomi proposto. Verificare che il contesto dei nomi padre sia registrato correttamente in DNS e che almeno una replica del contesto dei nomi sia raggiungibile dal master per la denominazione dei domini.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**\_ \_ \_ superato limite thread DS \_ errore**
</dt> <dd> <dl> <dt>

8587 (0x218B)
</dt> <dt>



È stato superato il limite di thread per questa richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERRORE \_ DS \_ non \_ più vicino**
</dt> <dd> <dl> <dt>

8588 (0x218C)
</dt> <dt>



Il server di catalogo globale non si trova nel sito più vicino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERRORE \_ DS \_ cant \_ derivare \_ SPN \_ senza \_ \_ ref server**
</dt> <dd> <dl> <dt>

8589 (0x218D)
</dt> <dt>



DS non può derivare un nome dell'entità servizio (SPN) per l'autenticazione reciproca del server di destinazione perché l'oggetto server corrispondente nel database DS locale non dispone di un attributo serverReference.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERRORE \_ DS \_ \_ modalità utente \_ singolo \_ non riuscita**
</dt> <dd> <dl> <dt>

8590 (0x218E)
</dt> <dt>



Il servizio directory non è stato in grado di attivare la modalità utente singolo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**errore di \_ sintassi di DS \_ NTDSCRIPT \_ \_**
</dt> <dd> <dl> <dt>

8591 (0x218F)
</dt> <dt>



Il servizio directory non è in grado di analizzare lo script a causa di un errore di sintassi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**errore \_ di \_ elaborazione NTDSCRIPT DS \_ errore \_**
</dt> <dd> <dl> <dt>

8592 (0x2190)
</dt> <dt>



Il servizio directory non è in grado di elaborare lo script a causa di un errore.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ERRORE \_ DS \_ \_ REPL diverse \_ epoche**
</dt> <dd> <dl> <dt>

8593 (0x2191)
</dt> <dt>



Il servizio directory non è in grado di eseguire l'operazione richiesta perché i server interessati sono di epoche di replica diverse (che in genere sono correlati a una ridenominazione del dominio in corso).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**ERRORE \_ DS \_ DRS \_ Extensions \_ modificate**
</dt> <dd> <dl> <dt>

8594 (0x2192)
</dt> <dt>



È necessario rinegoziare l'associazione al servizio directory a causa di una modifica nelle informazioni sulle estensioni del server.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERRORE \_ \_ \_ \_ di modifica del set di repliche DS \_ non \_ consentita \_ su \_ CR disabilitato \_**
</dt> <dd> <dl> <dt>

8595 (0x2193)
</dt> <dt>



Operazione non consentita su un riferimento incrociato disabilitato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERRORE \_ DS \_ nessun \_ msDS \_ IntID**
</dt> <dd> <dl> <dt>

8596 (0x2194)
</dt> <dt>



Errore di aggiornamento dello schema: non sono disponibili valori per msDS-IntId.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERRORE \_ DS \_ DUP \_ DMS \_ IntID**
</dt> <dd> <dl> <dt>

8597 (0x2195)
</dt> <dt>



Aggiornamento dello schema non riuscito: msDS-INtId duplicato. Ripetere l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**ERRORE \_ DS \_ presente \_ in \_ RDNATTID**
</dt> <dd> <dl> <dt>

8598 (0x2196)
</dt> <dt>



Eliminazione dello schema non riuscita: l'attributo viene usato in rDNAttID.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERRORE \_ \_ autorizzazione DS \_ non riuscita**
</dt> <dd> <dl> <dt>

8599 (0x2197)
</dt> <dt>



Il servizio directory non è stato in grado di autorizzare la richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERRORE \_ DS \_ script non valido \_**
</dt> <dd> <dl> <dt>

8600 (0x2198)
</dt> <dt>



Il servizio directory non è in grado di elaborare lo script perché non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**ERRORE \_ DS \_ Remote \_ CROSSREF \_ op \_ non riuscita**
</dt> <dd> <dl> <dt>

8601 (0x2199)
</dt> <dt>



Operazione di creazione incrociata remota non riuscita nell'FSMO del master per la denominazione dei domini. L'errore dell'operazione è nei dati estesi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERRORE \_ DS \_ Cross \_ ref \_ occupato**
</dt> <dd> <dl> <dt>

8602 (0x219A)
</dt> <dt>



Un riferimento incrociato è in uso localmente con lo stesso nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERRORE \_ DS \_ \_ di derivazione \_ SPN \_ per il \_ \_ dominio eliminato**
</dt> <dd> <dl> <dt>

8603 (0x219B)
</dt> <dt>



DS non può derivare un nome dell'entità servizio (SPN) per l'autenticazione reciproca del server di destinazione perché il dominio del server è stato eliminato dalla foresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERRORE di i/o del servizio \_ DS \_ con controller \_ \_ \_ scrivibile \_**
</dt> <dd> <dl> <dt>

8604 (0x219C)
</dt> <dt>



NCs scrivibile impedisce il controller di dominio da abbassamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**\_ \_ ID duplicato errore DS \_ \_ trovato**
</dt> <dd> <dl> <dt>

8605 (0x219D)
</dt> <dt>



L'oggetto richiesto non dispone di un identificatore univoco e non può essere recuperato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERRORE \_ DS \_ insufficiente \_ \_ per \_ creare l' \_ oggetto**
</dt> <dd> <dl> <dt>

8606 (0x219E)
</dt> <dt>



Sono stati assegnati attributi insufficienti per creare un oggetto. Questo oggetto potrebbe non esistere perché è possibile che sia stato eliminato e che sia già stato sottoposta a Garbage Collection.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**errore \_ di \_ conversione gruppo DS \_ errore \_**
</dt> <dd> <dl> <dt>

8607 (0x219F)
</dt> <dt>



Impossibile convertire il gruppo a causa di restrizioni relative agli attributi per il tipo di gruppo richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERRORE \_ DS \_ Impossibile \_ spostare \_ il \_ gruppo di base dell'app \_**
</dt> <dd> <dl> <dt>

8608 (0x21A0)
</dt> <dt>



Lo spostamento tra domini di gruppi di applicazioni di base non vuoti non è consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERRORE \_ DS \_ Impossibile \_ spostare \_ il \_ gruppo di query dell'app \_**
</dt> <dd> <dl> <dt>

8609 (0x21A1)
</dt> <dt>



Lo spostamento tra domini di gruppi di applicazioni basati su query non vuote non è consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**ERRORE \_ \_ ruolo DS \_ non \_ verificato**
</dt> <dd> <dl> <dt>

8610 (0x21A2)
</dt> <dt>



Impossibile verificare la proprietà del ruolo FSMO perché la relativa partizione di directory non è stata replicata correttamente con almeno un partner di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**ERRORE \_ DS \_ WKO \_ Container \_ non può \_ essere \_ speciale**
</dt> <dd> <dl> <dt>

8611 (0x21A3)
</dt> <dt>



Il contenitore di destinazione per un reindirizzamento di un contenitore di oggetti noto non può essere già un contenitore speciale.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERRORE \_ \_ \_ di ridenominazione \_ del dominio DS in \_ corso**
</dt> <dd> <dl> <dt>

8612 (0x21A4)
</dt> <dt>



Il servizio directory non è in grado di eseguire l'operazione richiesta perché è in corso un'operazione di ridenominazione del dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERRORE \_ DS esistente del controller di dominio \_ \_ ad \_ \_**
</dt> <dd> <dl> <dt>

8613 (0x21A5)
</dt> <dt>



Il servizio directory ha rilevato una partizione figlio al di sotto del nome della partizione richiesta. La gerarchia della partizione deve essere creata in un metodo di primo piano.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**\_ \_ \_ superamento della durata del REPL DS \_**
</dt> <dd> <dl> <dt>

8614 (0x21A6)
</dt> <dt>



Il servizio directory non è in grado di eseguire la replica con questo server perché il tempo trascorso dall'ultima replica con il server ha superato la durata dell'oggetto contrassegnato per la rimozione definitiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERRORE \_ DS non \_ consentito \_ nel \_ contenitore di sistema \_**
</dt> <dd> <dl> <dt>

8615 (0x21A7)
</dt> <dt>



L'operazione richiesta non è consentita su un oggetto nel contenitore System.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERRORE \_ \_ coda di invio LDAP di DS con errore \_ \_ \_ completo**
</dt> <dd> <dl> <dt>

8616 (0x21A8)
</dt> <dt>



La coda di invio della rete dei server LDAP è stata riempita perché il client non elabora i risultati delle richieste in modo sufficientemente veloce. Non verranno elaborate altre richieste finché il client non viene aggiornato. Se il client non viene aggiornato, verrà disconnesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**\_finestra di \_ \_ \_ pianificazione \_ del servizio DRA di errore DS**
</dt> <dd> <dl> <dt>

8617 (0x21A9)
</dt> <dt>



La replica pianificata non è stata eseguita perché il sistema era troppo occupato per eseguire la richiesta entro la finestra di pianificazione. La coda di replica è in overload. Provare a ridurre il numero di partner o a diminuire la frequenza di replica pianificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**criterio di errore \_ DS \_ \_ non \_ noto**
</dt> <dd> <dl> <dt>

8618 (0x21AA)
</dt> <dt>



Al momento non è possibile determinare se il criterio di replica del ramo è disponibile nel controller di dominio dell'hub. Riprovare in un secondo momento per tenere conto delle latenze di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERRORE \_ nessun \_ \_ oggetto impostazioni \_ sito**
</dt> <dd> <dl> <dt>

8619 (0x21AB)
</dt> <dt>



L'oggetto Impostazioni sito per il sito specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERRORE \_ nessun \_ segreto**
</dt> <dd> <dl> <dt>

8620 (0x21AC)
</dt> <dt>



L'archivio account locale non contiene il materiale segreto per l'account specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERRORE \_ non è stato trovato alcun controller di dominio \_ scrivibile \_ \_**
</dt> <dd> <dl> <dt>

8621 (0x21AD)
</dt> <dt>



Impossibile trovare un controller di dominio scrivibile nel dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERRORE \_ DS \_ nessun \_ \_ oggetto server**
</dt> <dd> <dl> <dt>

8622 (0x21AE)
</dt> <dt>



L'oggetto server per il controller di dominio non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERRORE \_ DS \_ nessun \_ oggetto NTDSA \_**
</dt> <dd> <dl> <dt>

8623 (0x21AF)
</dt> <dt>



L'oggetto Impostazioni NTDS per il controller di dominio non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERRORE \_ DS \_ \_ ricerca non ASQ \_**
</dt> <dd> <dl> <dt>

8624 (0x21B0)
</dt> <dt>



L'operazione di ricerca richiesta non è supportata per le ricerche ASQ.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**errore \_ di \_ controllo DS errore \_**
</dt> <dd> <dl> <dt>

8625 (0x21B1)
</dt> <dt>



Non è stato possibile generare un evento di controllo obbligatorio per l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERRORE \_ DS \_ - \_ \_ sottoalbero del flag di ricerca non valido \_**
</dt> <dd> <dl> <dt>

8626 (0x21B2)
</dt> <dt>



I flag di ricerca per l'attributo non sono validi. Il bit dell'indice del sottoalbero è valido solo per gli attributi a valore singolo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERRORE \_ DS \_ \_ \_ tupla flag di ricerca non valido \_**
</dt> <dd> <dl> <dt>

8627 (0x21B3)
</dt> <dt>



I flag di ricerca per l'attributo non sono validi. Il bit dell'indice tupla è valido solo per gli attributi delle stringhe Unicode.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERRORE \_ di \_ tabella gerarchia DS \_ \_ troppo \_ profonda**
</dt> <dd> <dl> <dt>

8628 (0x21B4)
</dt> <dt>



Le rubriche sono troppo profondamente nidificate. Impossibile compilare la tabella della gerarchia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERRORE \_ DS \_ DRA \_ danneggiato \_ \_ vettoriale**
</dt> <dd> <dl> <dt>

8629 (0x21B5)
</dt> <dt>



Il vettore di nesso aggiornato specificato è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERRORI \_ \_ segreti DRA di DS \_ \_ negati**
</dt> <dd> <dl> <dt>

8630 (0x21B6)
</dt> <dt>



La richiesta di replica dei segreti è stata negata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**\_ \_ \_ ID MAPI riservato DS \_ errore**
</dt> <dd> <dl> <dt>

8631 (0x21B7)
</dt> <dt>



Aggiornamento dello schema non riuscito: l'identificatore MAPI è riservato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERRORE \_ \_ ID MAPI \_ DS \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

8632 (0x21B8)
</dt> <dt>



Aggiornamento dello schema non riuscito: non sono disponibili identificatori MAPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERRORE del servizio di \_ dominio di \_ \_ \_ krbtgt mancante \_**
</dt> <dd> <dl> <dt>

8633 (0x21B9)
</dt> <dt>



L'operazione di replica non è riuscita perché mancano gli attributi obbligatori dell'oggetto krbtgt locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERRORE \_ \_ nome dominio \_ DS \_ esistente \_ nella \_ foresta**
</dt> <dd> <dl> <dt>

8634 (0x21BA)
</dt> <dt>



Il nome di dominio del dominio trusted esiste già nella foresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERRORE \_ \_ nome flat \_ DS \_ esistente \_ nella \_ foresta**
</dt> <dd> <dl> <dt>

8635 (0x21BB)
</dt> <dt>



Il nome flat del dominio trusted esiste già nella foresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**ERRORE \_ \_ \_ nome entità utente non valido \_**
</dt> <dd> <dl> <dt>

8636 (0x21BC)
</dt> <dt>



Il nome dell'entità utente (UPN) non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERRORE \_ del \_ \_ gruppo mappato OID di DS con \_ \_ \_ \_ membri**
</dt> <dd> <dl> <dt>

8637 (0x21BD)
</dt> <dt>



I gruppi con mapping OID non possono avere membri.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERRORE \_ DS \_ DS \_ non \_ trovato**
</dt> <dd> <dl> <dt>

8638 (0x21BE)
</dt> <dt>



L'OID specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERRORE \_ DS servizio di \_ \_ destinazione riciclata \_**
</dt> <dd> <dl> <dt>

8639 (0x21BF)
</dt> <dt>



L'operazione di replica non è riuscita perché l'oggetto di destinazione a cui fa riferimento un valore di collegamento viene riciclato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERRORE \_ DS non \_ consentito di \_ \_ Reindirizzamento del controller di dominio**
</dt> <dd> <dl> <dt>

8640 (0x21C0)
</dt> <dt>



L'operazione di reindirizzamento non è riuscita perché l'oggetto di destinazione si trova in un NC diverso da quello del controller di dominio corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERRORE \_ DS \_ High \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8641 (0x21C1)
</dt> <dt>



Non è possibile ridurre il livello di funzionalità del set di configurazione AD LDS al valore richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERRORE \_ DS \_ High \_ DSA \_ Version**
</dt> <dd> <dl> <dt>

8642 (0x21C2)
</dt> <dt>



Il livello di funzionalità del dominio (o della foresta) non può essere abbassato al valore richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERRORE \_ DS \_ low \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8643 (0x21C3)
</dt> <dt>



Non è possibile aumentare il livello di funzionalità del set di configurazione AD LDS al valore richiesto, perché esistono una o più istanze di ADLDS con un livello di funzionalità non compatibile più basso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**\_ \_ SID del dominio \_ di errore uguale alla \_ \_ \_ workstation locale**
</dt> <dd> <dl> <dt>

8644 (0x21C4)
</dt> <dt>



Non è possibile completare l'aggiunta al dominio perché il SID del dominio a cui si è tentato di aggiungere è identico al SID di questo computer. Si tratta di un sintomo di un'installazione del sistema operativo clonata in modo errato. Eseguire Sysprep sul computer per generare un nuovo SID del computer. Per altre informazioni, vedere <https://go.microsoft.com/fwlink/p/?linkid=168895>.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERRORE \_ DS- \_ annullamento dell'eliminazione della \_ \_ convalida Sam \_ non riuscita**
</dt> <dd> <dl> <dt>

8645 (0x21C5)
</dt> <dt>



L'operazione di annullamento dell'eliminazione non è riuscita perché il nome dell'account SAM o il nome dell'account SAM aggiuntivo dell'oggetto da eliminare è in conflitto con un oggetto attivo esistente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERRORE \_ \_ tipo di account non corretto \_**
</dt> <dd> <dl> <dt>

8646 (0x21C6)
</dt> <dt>



Il sistema non è autorevole per l'account specificato e pertanto non può completare l'operazione. Ripetere l'operazione usando il provider associato a questo account. Se si tratta di un provider online, utilizzare il sito online del provider.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore di sistema](system-error-codes.md)
</dt> </dl>

 

 




