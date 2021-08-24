---
description: Descrive i codici di errore 8200-8999 definiti nel file di intestazione WinError.h ed è destinato agli sviluppatori.
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: Codici di errore di sistema (8200-8999) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: e9fd65025c3d51575cb0ece83cba14e0c62980d11a60ec6cb351919b6c7714c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572961"
---
# <a name="system-error-codes-8200-8999"></a>Codici di errore di sistema (8200-8999)

> [!NOTE]
> Queste informazioni sono destinate agli sviluppatori che ese tracciano errori di sistema. Per altri errori, ad esempio problemi con Windows, è disponibile un elenco di risorse nella [pagina Codici di](system-error-codes.md) errore.

L'elenco seguente descrive i [codici di errore di](system-error-codes.md) sistema per gli errori da 8200 a 8999. Vengono restituiti dalla [**funzione GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la [**funzione FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il flag **FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERRORE \_ DS \_ NON \_ INSTALLATO**
</dt> <dd> <dl> <dt>

8200 (0x2008)
</dt> <dt>



Si è verificato un errore durante l'installazione del servizio directory. Per altre informazioni, vedere il registro eventi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERRORE \_ DI VALUTAZIONE \_ DELL'APPARTENENZA DS \_ IN \_ LOCALE**
</dt> <dd> <dl> <dt>

8201 (0x2009)
</dt> <dt>



Il servizio directory ha valutato le appartenenze ai gruppi in locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERRORE \_ DS \_ NESSUN ATTRIBUTO O \_ \_ \_ VALORE**
</dt> <dd> <dl> <dt>

8202 (0x200A)
</dt> <dt>



L'attributo o il valore del servizio directory specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERRORE \_ SINTASSI \_ DELL'ATTRIBUTO DS NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

8203 (0x200B)
</dt> <dt>



La sintassi dell'attributo specificata per il servizio directory non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**ERRORE \_ TIPO DI ATTRIBUTO DS NON \_ \_ \_ DEFINITO**
</dt> <dd> <dl> <dt>

8204 (0x200C)
</dt> <dt>



Il tipo di attributo specificato per il servizio directory non è definito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**ERRORE \_ DELL'ATTRIBUTO \_ O DEL VALORE \_ \_ DS \_ ESISTENTE**
</dt> <dd> <dl> <dt>

8205 (0x200D)
</dt> <dt>



L'attributo o il valore del servizio directory specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERRORE \_ DS \_ OCCUPATO**
</dt> <dd> <dl> <dt>

8206 (0x200E)
</dt> <dt>



Il servizio directory è occupato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERRORE \_ DS \_ NON DISPONIBILE**
</dt> <dd> <dl> <dt>

8207 (0x200F)
</dt> <dt>



Il servizio directory non è disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERRORE \_ DS \_ NO \_ RIDS \_ ALLOCATED**
</dt> <dd> <dl> <dt>

8208 (0x2010)
</dt> <dt>



Il servizio directory non è in grado di allocare l'identificatore relativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERRORE \_ DS \_ NO MORE \_ \_ RIDS**
</dt> <dd> <dl> <dt>

8209 (0x2011)
</dt> <dt>



Il servizio directory ha esaurito il pool di identificatori relativi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERRORE \_ DS \_ PROPRIETARIO DEL RUOLO \_ NON \_ CORRETTO**
</dt> <dd> <dl> <dt>

8210 (0x2012)
</dt> <dt>



Impossibile eseguire l'operazione richiesta perché il servizio directory non è il master per quel tipo di operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**ERRORE \_ DS \_ RIDMGR \_ INIT \_ ERROR**
</dt> <dd> <dl> <dt>

8211 (0x2013)
</dt> <dt>



Il servizio directory non è stato in grado di inizializzare il sottosistema che alloca gli identificatori relativi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**ERRORE \_ DI VIOLAZIONE \_ DELLA CLASSE OBJ \_ DS \_**
</dt> <dd> <dl> <dt>

8212 (0x2014)
</dt> <dt>



L'operazione richiesta non soddisfa uno o più vincoli associati alla classe dell'oggetto .


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERRORE \_ DS \_ CANT \_ ON NON \_ \_ LEAF**
</dt> <dd> <dl> <dt>

8213 (0x2015)
</dt> <dt>



Il servizio directory può eseguire l'operazione richiesta solo su un oggetto foglia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**ERRORE \_ DS \_ CANT \_ IN \_ RDN**
</dt> <dd> <dl> <dt>

8214 (0x2016)
</dt> <dt>



Il servizio directory non può eseguire l'operazione richiesta sull'attributo RDN di un oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**CLASSE \_ OBJ ERROR DS \_ CANT \_ \_ \_ MOD**
</dt> <dd> <dl> <dt>

8215 (0x2017)
</dt> <dt>



Il servizio directory ha rilevato un tentativo di modificare la classe di oggetti di un oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**ERRORE \_ DS \_ CROSS DOM \_ MOVE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

8216 (0x2018)
</dt> <dt>



Impossibile eseguire l'operazione di spostamento tra domini richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERRORE \_ DS \_ GC NON \_ \_ DISPONIBILE**
</dt> <dd> <dl> <dt>

8217 (0x2019)
</dt> <dt>



Impossibile contattare il server di catalogo globale.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**ERRORE \_ DEI CRITERI \_ CONDIVISI**
</dt> <dd> <dl> <dt>

8218 (0x201A)
</dt> <dt>



L'oggetto criteri è condiviso e può essere modificato solo nella radice.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**OGGETTO \_ CRITERI DI ERRORE NON \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

8219 (0x201B)
</dt> <dt>



L'oggetto criteri non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**CRITERI \_ DI ERRORE SOLO IN \_ \_ \_ DS**
</dt> <dd> <dl> <dt>

8220 (0x201C)
</dt> <dt>



Le informazioni sui criteri richieste si trova solo nel servizio directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**PROMOZIONE \_ DEGLI \_ ERRORI ATTIVA**
</dt> <dd> <dl> <dt>

8221 (0x201D)
</dt> <dt>



Un innalzamento di livello del controller di dominio è attualmente attivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERRORE \_ NESSUNA \_ PROMOZIONE \_ ATTIVA**
</dt> <dd> <dl> <dt>

8222 (0x201E)
</dt> <dt>



L'innalzamento di livello di un controller di dominio non è attualmente attivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**ERRORE \_ DELLE OPERAZIONI DS \_ \_**
</dt> <dd> <dl> <dt>

8224 (0x2020)
</dt> <dt>



Si è verificato un errore di operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**ERRORE \_ DEL PROTOCOLLO DS \_ \_**
</dt> <dd> <dl> <dt>

8225 (0x2021)
</dt> <dt>



Si è verificato un errore di protocollo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**ERRORE \_ DS \_ TIMELIMIT \_ SUPERATO**
</dt> <dd> <dl> <dt>

8226 (0x2022)
</dt> <dt>



È stato superato il limite di tempo per questa richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERRORE \_ DS \_ SIZELIMIT \_ SUPERATO**
</dt> <dd> <dl> <dt>

8227 (0x2023)
</dt> <dt>



È stato superato il limite di dimensioni per questa richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**LIMITE \_ AMMINISTRATORE DS \_ DI ERRORE \_ \_ SUPERATO**
</dt> <dd> <dl> <dt>

8228 (0x2024)
</dt> <dt>



È stato superato il limite amministrativo per questa richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERRORE \_ DS \_ COMPARE \_ FALSE**
</dt> <dd> <dl> <dt>

8229 (0x2025)
</dt> <dt>



La risposta di confronto era false.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERRORE \_ DS \_ COMPARE \_ TRUE**
</dt> <dd> <dl> <dt>

8230 (0x2026)
</dt> <dt>



La risposta di confronto era true.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**ERRORE \_ METODO DI AUTENTICAZIONE \_ \_ DS NON \_ \_ SUPPORTATO**
</dt> <dd> <dl> <dt>

8231 (0x2027)
</dt> <dt>



Il metodo di autenticazione richiesto non è supportato dal server.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERRORE \_ DS \_ STRONG \_ AUTH \_ REQUIRED**
</dt> <dd> <dl> <dt>

8232 (0x2028)
</dt> <dt>



Per questo server è necessario un metodo di autenticazione più sicuro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**ERRORE \_ DS \_ INAPPROPRIATE \_ AUTH**
</dt> <dd> <dl> <dt>

8233 (0x2029)
</dt> <dt>



Autenticazione non appropriata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERRORE \_ DS \_ AUTH \_ UNKNOWN**
</dt> <dd> <dl> <dt>

8234 (0x202A)
</dt> <dt>



Il meccanismo di autenticazione è sconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**SEGNALAZIONE \_ ERRORE DS \_**
</dt> <dd> <dl> <dt>

8235 (0x202B)
</dt> <dt>



Il server ha restituito un riferimento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**ERRORE \_ DS \_ UNAVAILABLE \_ CRIT \_ EXTENSION**
</dt> <dd> <dl> <dt>

8236 (0x202C)
</dt> <dt>



Il server non supporta l'estensione critica richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**ERRORE \_ DS \_ CONFIDENTIALITY \_ REQUIRED**
</dt> <dd> <dl> <dt>

8237 (0x202D)
</dt> <dt>



Questa richiesta richiede una connessione sicura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERRORE DI \_ CORRISPONDENZA \_ INAPPROPRIATA DS \_**
</dt> <dd> <dl> <dt>

8238 (0x202E)
</dt> <dt>



Corrispondenza inappropriata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**ERRORE DI \_ VIOLAZIONE DEL VINCOLO DS \_ \_**
</dt> <dd> <dl> <dt>

8239 (0x202F)
</dt> <dt>



Si è verificata una violazione di vincolo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERRORE \_ DS \_ NO SUCH \_ \_ OBJECT**
</dt> <dd> <dl> <dt>

8240 (0x2030)
</dt> <dt>



Oggetto inesistente sul server.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**ERRORE DEL \_ PROBLEMA RELATIVO \_ ALL'ALIAS DS \_**
</dt> <dd> <dl> <dt>

8241 (0x2031)
</dt> <dt>



Si è verificato un problema di alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**SINTASSI \_ DN \_ \_ DS NON \_ VALIDA**
</dt> <dd> <dl> <dt>

8242 (0x2032)
</dt> <dt>



È stata specificata una sintassi dn non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**ERRORE \_ DS \_ IS \_ LEAF**
</dt> <dd> <dl> <dt>

8243 (0x2033)
</dt> <dt>



L'oggetto è un oggetto foglia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**ERRORE \_ DEL PROBLEMA DI \_ \_ DEREF DELL'ALIAS DS \_**
</dt> <dd> <dl> <dt>

8244 (0x2034)
</dt> <dt>



Si è verificato un problema di dereferenziazione degli alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERRORE \_ CHE DS \_ NON È IN GRADO DI \_ \_ ESEGUIRE**
</dt> <dd> <dl> <dt>

8245 (0x2035)
</dt> <dt>



Il server non è in grado di elaborare la richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**ERRORE \_ DI RILEVAMENTO DEL CICLO DS \_ \_**
</dt> <dd> <dl> <dt>

8246 (0x2036)
</dt> <dt>



È stato rilevato un ciclo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**ERRORE DI \_ VIOLAZIONE DI \_ DENOMINAZIONE DS \_**
</dt> <dd> <dl> <dt>

8247 (0x2037)
</dt> <dt>



Si verifica una violazione di denominazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**ERRORE \_ NEI RISULTATI \_ DELL'OGGETTO \_ DS TROPPO \_ \_ GRANDI**
</dt> <dd> <dl> <dt>

8248 (0x2038)
</dt> <dt>



Il set di risultati è troppo grande.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**ERRORE \_ DS \_ INFLUISCE \_ SU PIÙ \_ DSAS**
</dt> <dd> <dl> <dt>

8249 (0x2039)
</dt> <dt>



L'operazione interessa più DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERRORE \_ DS \_ SERVER \_ DOWN**
</dt> <dd> <dl> <dt>

8250 (0x203A)
</dt> <dt>



Il server non è operativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**ERRORE \_ DS \_ LOCAL \_ ERROR**
</dt> <dd> <dl> <dt>

8251 (0x203B)
</dt> <dt>



Si è verificato un errore locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**ERRORE DI \_ CODIFICA DS \_ \_**
</dt> <dd> <dl> <dt>

8252 (0x203C)
</dt> <dt>



Si è verificato un errore di codifica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**ERRORE \_ DI DECODIFICA DS \_ \_**
</dt> <dd> <dl> <dt>

8253 (0x203D)
</dt> <dt>



Si è verificato un errore di decodifica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERRORE \_ FILTRO DS \_ \_ SCONOSCIUTO**
</dt> <dd> <dl> <dt>

8254 (0x203E)
</dt> <dt>



Il filtro di ricerca non può essere riconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**ERRORE \_ DS \_ PARAM \_ ERROR**
</dt> <dd> <dl> <dt>

8255 (0x203F)
</dt> <dt>



Uno o più parametri non sono validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERRORE \_ DS \_ NON \_ SUPPORTATO**
</dt> <dd> <dl> <dt>

8256 (0x2040)
</dt> <dt>



Il metodo specificato non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERRORE \_ DS \_ NESSUN RISULTATO \_ \_ RESTITUITO**
</dt> <dd> <dl> <dt>

8257 (0x2041)
</dt> <dt>



Non sono stati restituiti risultati.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**ERRORE \_ DI CONTROLLO DS NON \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

8258 (0x2042)
</dt> <dt>



Il controllo specificato non è supportato dal server.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERRORE \_ DEL CICLO DEL CLIENT \_ DS \_**
</dt> <dd> <dl> <dt>

8259 (0x2043)
</dt> <dt>



È stato rilevato un ciclo di riferimenti dal client.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**È STATO \_ SUPERATO IL LIMITE DI \_ \_ SEGNALAZIONI DS \_**
</dt> <dd> <dl> <dt>

8260 (0x2044)
</dt> <dt>



È stato superato il limite di riferimenti preimpostato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERRORE CONTROLLO \_ ORDINAMENTO DS \_ \_ \_ MANCANTE**
</dt> <dd> <dl> <dt>

8261 (0x2045)
</dt> <dt>



La ricerca richiede un controllo SORT.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**ERRORE DI \_ INTERVALLO OFFSET DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8262 (0x2046)
</dt> <dt>



I risultati della ricerca superano l'intervallo di offset specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERRORE \_ DS \_ RIDMGR \_ DISABILITATO**
</dt> <dd> <dl> <dt>

8263 (0x2047)
</dt> <dt>



Il servizio directory ha rilevato che il sottosistema che alloca identificatori relativi è disabilitato. Ciò può verificarsi come meccanismo di protezione quando il sistema determina che una parte significativa di identificatori relativi (RID) è stata esaurita. Vedere per <https://go.microsoft.com/fwlink/p/?linkid=228610> i passaggi di diagnostica consigliati e la procedura per abilitare nuovamente la creazione dell'account.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**\_L'ERRORE DS \_ ROOT DEVE ESSERE \_ \_ \_ NC**
</dt> <dd> <dl> <dt>

8301 (0x206D)
</dt> <dt>



L'oggetto radice deve essere l'elemento head di un contesto dei nomi. L'oggetto radice non può avere un elemento padre di cui è stata creata un'istanza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERRORE \_ DS \_ ADD REPLICA \_ \_ INIBITO**
</dt> <dd> <dl> <dt>

8302 (0x206E)
</dt> <dt>



Impossibile eseguire l'operazione di aggiunta della replica. Il contesto dei nomi deve essere scrivibile per creare la replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERRORE \_ DS \_ ATT \_ NOT DEF \_ \_ NELLO \_ SCHEMA**
</dt> <dd> <dl> <dt>

8303 (0x206F)
</dt> <dt>



Si è verificato un riferimento a un attributo non definito nello schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**ERRORE \_ DS \_ MAX \_ OBJ SIZE \_ \_ EXCEEDED**
</dt> <dd> <dl> <dt>

8304 (0x2070)
</dt> <dt>



È stata superata la dimensione massima di un oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**ERRORE \_ DS \_ OBJ \_ STRING NAME \_ \_ EXISTS**
</dt> <dd> <dl> <dt>

8305 (0x2071)
</dt> <dt>



È stato effettuato un tentativo di aggiungere un oggetto alla directory con un nome già in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERRORE \_ DS \_ NO \_ RDN DEFINITO NELLO \_ \_ \_ SCHEMA**
</dt> <dd> <dl> <dt>

8306 (0x2072)
</dt> <dt>



È stato effettuato un tentativo di aggiungere un oggetto di una classe che non dispone di un RDN definito nello schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**ERRORE \_ DS \_ RDN \_ NON CORRISPONDE ALLO \_ \_ SCHEMA**
</dt> <dd> <dl> <dt>

8307 (0x2073)
</dt> <dt>



È stato effettuato un tentativo di aggiungere un oggetto usando un RDN che non è il nome RDN definito nello schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERRORE \_ DS \_ NON TROVATO \_ \_ ATTS \_ RICHIESTO**
</dt> <dd> <dl> <dt>

8308 (0x2074)
</dt> <dt>



Nessuno degli attributi richiesti è stato trovato sugli oggetti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERRORE \_ DS \_ USER BUFFER TO \_ \_ \_ SMALL**
</dt> <dd> <dl> <dt>

8309 (0x2075)
</dt> <dt>



Il buffer utente è troppo piccolo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**ERRORE \_ DS \_ ATT \_ NON È \_ \_ IN \_ OBJ**
</dt> <dd> <dl> <dt>

8310 (0x2076)
</dt> <dt>



L'attributo specificato nell'operazione non è presente nell'oggetto .


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERRORE \_ DS \_ OPERAZIONE MOD \_ NON \_ VALIDA**
</dt> <dd> <dl> <dt>

8311 (0x2077)
</dt> <dt>



Operazione di modifica non valida. Alcuni aspetti della modifica non sono consentiti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**OBJ DS DI ERRORE \_ \_ TROPPO \_ \_ GRANDE**
</dt> <dd> <dl> <dt>

8312 (0x2078)
</dt> <dt>



L'oggetto specificato è troppo grande.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERRORE \_ DS \_ TIPO DI ISTANZA \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

8313 (0x2079)
</dt> <dt>



Il tipo di istanza specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERRORE \_ DS \_ MASTERDSA \_ OBBLIGATORIO**
</dt> <dd> <dl> <dt>

8314 (0x207A)
</dt> <dt>



L'operazione deve essere eseguita in un DSA master.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**RICHIESTA \_ CLASSE DI OGGETTO DS \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

8315 (0x207B)
</dt> <dt>



È necessario specificare l'attributo della classe di oggetti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**ERRORE \_ DS \_ MANCANTE \_ \_ ATT OBBLIGATORIO**
</dt> <dd> <dl> <dt>

8316 (0x207C)
</dt> <dt>



Attributo obbligatorio mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERRORE \_ DS \_ ATT \_ NOT DEF PER LA \_ \_ \_ CLASSE**
</dt> <dd> <dl> <dt>

8317 (0x207D)
</dt> <dt>



È stato effettuato un tentativo di modificare un oggetto in modo da includere un attributo non valido per la relativa classe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**ERRORE \_ DS \_ ATT \_ GIÀ \_ ESISTENTE**
</dt> <dd> <dl> <dt>

8318 (0x207E)
</dt> <dt>



L'attributo specificato è già presente nell'oggetto .


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERRORE \_ DS \_ CANT \_ ADD \_ ATT \_ VALUES**
</dt> <dd> <dl> <dt>

8320 (0x2080)
</dt> <dt>



L'attributo specificato non è presente o non ha valori.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERRORE \_ - VINCOLO A VALORE \_ \_ SINGOLO DS \_**
</dt> <dd> <dl> <dt>

8321 (0x2081)
</dt> <dt>



Sono stati specificati più valori per un attributo che può avere un solo valore.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**VINCOLO \_ DI INTERVALLO DS \_ \_ ERRORE**
</dt> <dd> <dl> <dt>

8322 (0x2082)
</dt> <dt>



Un valore per l'attributo non è compreso nell'intervallo di valori accettabile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**ERRORE \_ DS \_ ATT \_ VAL GIÀ \_ \_ ESISTENTE**
</dt> <dd> <dl> <dt>

8323 (0x2083)
</dt> <dt>



Il valore specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERRORE \_ DS \_ CANT \_ REM \_ MISSING \_ ATT**
</dt> <dd> <dl> <dt>

8324 (0x2084)
</dt> <dt>



Impossibile rimuovere l'attributo perché non è presente nell'oggetto .


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**ERRORE \_ DS \_ CANT \_ REM \_ MANCANTE \_ ATT \_ VAL**
</dt> <dd> <dl> <dt>

8325 (0x2085)
</dt> <dt>



Impossibile rimuovere il valore dell'attributo perché non è presente nell'oggetto .


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**ERRORE \_ DS \_ ROOT \_ CANT BE \_ \_ SUBREF**
</dt> <dd> <dl> <dt>

8326 (0x2086)
</dt> <dt>



L'oggetto radice specificato non può essere un sottorif.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERRORE \_ DS \_ NO \_ CHAINING**
</dt> <dd> <dl> <dt>

8327 (0x2087)
</dt> <dt>



Il concatenamento non è consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERRORE \_ DS \_ NO \_ CHAINED \_ EVAL**
</dt> <dd> <dl> <dt>

8328 (0x2088)
</dt> <dt>



La valutazione concatenata non è consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERRORE \_ DS \_ NESSUN OGGETTO \_ \_ PADRE**
</dt> <dd> <dl> <dt>

8329 (0x2089)
</dt> <dt>



Il padre dell'oggetto è privo di istanza o è stato eliminato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**\_L'ELEMENTO PADRE DS \_ ERRORE È UN \_ \_ \_ ALIAS**
</dt> <dd> <dl> <dt>

8330 (0x208A)
</dt> <dt>



La presenza di un elemento padre che è un alias non è consentita. Gli alias sono oggetti foglia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERRORE \_ DS \_ CANT \_ MIX MASTER \_ \_ E \_ REPS**
</dt> <dd> <dl> <dt>

8331 (0x208B)
</dt> <dt>



L'oggetto e l'elemento padre devono essere dello stesso tipo, sia master che repliche.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**ERRORE \_ DS \_ CHILDREN \_ EXIST**
</dt> <dd> <dl> <dt>

8332 (0x208C)
</dt> <dt>



Impossibile eseguire l'operazione perché esistono oggetti figlio. Questa operazione può essere eseguita solo su un oggetto foglia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**ERRORE \_ DS \_ OBJ \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

8333 (0x208D)
</dt> <dt>



Oggetto directory non trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**OBJ \_ CON ALIAS DS \_ \_ \_ MANCANTE**
</dt> <dd> <dl> <dt>

8334 (0x208E)
</dt> <dt>



Oggetto con alias mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**SINTASSI \_ DEL NOME NON VALIDO DS \_ \_ \_ ERRORE**
</dt> <dd> <dl> <dt>

8335 (0x208F)
</dt> <dt>



La sintassi del nome dell'oggetto non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**\_L'ALIAS DS \_ DI ERRORE PUNTA \_ \_ \_ ALL'ALIAS**
</dt> <dd> <dl> <dt>

8336 (0x2090)
</dt> <dt>



Non è consentito che un alias faccia riferimento a un altro alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERRORE \_ DS \_ CANT \_ DEREF \_ ALIAS**
</dt> <dd> <dl> <dt>

8337 (0x2091)
</dt> <dt>



Non è possibile dereferenziare l'alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERRORE \_ DS \_ FUORI \_ \_ AMBITO**
</dt> <dd> <dl> <dt>

8338 (0x2092)
</dt> <dt>



L'operazione non è in ambito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERRORE \_ DURANTE LA RIMOZIONE \_ DELL'OGGETTO DS \_ \_**
</dt> <dd> <dl> <dt>

8339 (0x2093)
</dt> <dt>



L'operazione non può continuare perché l'oggetto è in corso di rimozione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERRORE \_ DS \_ CANT \_ DELETE \_ DSA \_ OBJ**
</dt> <dd> <dl> <dt>

8340 (0x2094)
</dt> <dt>



Impossibile eliminare l'oggetto DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**ERRORE \_ DS \_ GENERIC \_ ERROR**
</dt> <dd> <dl> <dt>

8341 (0x2095)
</dt> <dt>



Si è verificato un errore del servizio directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**ERRORE \_ DS \_ DSA \_ DEVE ESSERE INT \_ \_ \_ MASTER**
</dt> <dd> <dl> <dt>

8342 (0x2096)
</dt> <dt>



L'operazione può essere eseguita solo su un oggetto DSA master interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERRORE \_ DELLA CLASSE DS NON \_ \_ \_ DSA**
</dt> <dd> <dl> <dt>

8343 (0x2097)
</dt> <dt>



L'oggetto deve essere della classe DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**ERRORE \_ DS \_ INSUFF \_ ACCESS \_ RIGHTS**
</dt> <dd> <dl> <dt>

8344 (0x2098)
</dt> <dt>



Diritti di accesso insufficienti per eseguire l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERRORE \_ DS \_ NON VALIDO \_ SUPERIORE**
</dt> <dd> <dl> <dt>

8345 (0x2099)
</dt> <dt>



Impossibile aggiungere l'oggetto perché l'elemento padre non è in elenco di possibili superiori.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**ERRORE \_ DELL'ATTRIBUTO DS \_ DI PROPRIETÀ DI \_ \_ \_ SAM**
</dt> <dd> <dl> <dt>

8346 (0x209A)
</dt> <dt>



L'accesso all'attributo non è consentito perché l'attributo è di proprietà di Gestione account di sicurezza (SAM).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERRORE \_ NOME DS \_ TROPPE \_ \_ \_ PARTI**
</dt> <dd> <dl> <dt>

8347 (0x209B)
</dt> <dt>



Il nome ha troppe parti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**ERRORE \_ NOME DS \_ TROPPO \_ \_ LUNGO**
</dt> <dd> <dl> <dt>

8348 (0x209C)
</dt> <dt>



Nome troppo lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**ERRORE \_ VALORE NOME DS TROPPO \_ \_ \_ \_ LUNGO**
</dt> <dd> <dl> <dt>

8349 (0x209D)
</dt> <dt>



Il valore del nome è troppo lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERRORE \_ DS \_ NAME \_ UNPARSEABLE**
</dt> <dd> <dl> <dt>

8350 (0x209E)
</dt> <dt>



Il servizio directory ha rilevato un errore durante l'analisi di un nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERRORE \_ TIPO NOME DS \_ \_ \_ SCONOSCIUTO**
</dt> <dd> <dl> <dt>

8351 (0x209F)
</dt> <dt>



Il servizio directory non può ottenere il tipo di attributo per un nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERRORE \_ DS \_ NON UN \_ \_ OGGETTO**
</dt> <dd> <dl> <dt>

8352 (0x20A0)
</dt> <dt>



Il nome non identifica un oggetto. il nome identifica un fantasma.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERRORE \_ DS \_ SEC \_ DESC TROPPO \_ \_ BREVE**
</dt> <dd> <dl> <dt>

8353 (0x20A1)
</dt> <dt>



Il descrittore di sicurezza è troppo breve.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERRORE \_ DS \_ SEC \_ DESC NON \_ VALIDO**
</dt> <dd> <dl> <dt>

8354 (0x20A2)
</dt> <dt>



Il descrittore di sicurezza non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERRORE \_ DS \_ NO DELETED \_ \_ NAME**
</dt> <dd> <dl> <dt>

8355 (0x20A3)
</dt> <dt>



Impossibile creare il nome per l'oggetto eliminato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**\_L'ERRORE DS \_ SUBREF \_ DEVE AVERE UN \_ ELEMENTO \_ PADRE**
</dt> <dd> <dl> <dt>

8356 (0x20A4)
</dt> <dt>



L'elemento padre di un nuovo sottoref deve esistere.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**ERRORE \_ DS \_ NCNAME \_ DEVE ESSERE \_ \_ NC**
</dt> <dd> <dl> <dt>

8357 (0x20A5)
</dt> <dt>



L'oggetto deve essere un contesto dei nomi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERRORE \_ DS \_ CANT \_ ADD SYSTEM \_ \_ ONLY**
</dt> <dd> <dl> <dt>

8358 (0x20A6)
</dt> <dt>



Non è consentito aggiungere un attributo di proprietà del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**LA \_ CLASSE DS \_ ERROR DEVE \_ ESSERE \_ \_ CONCRETA**
</dt> <dd> <dl> <dt>

8359 (0x20A7)
</dt> <dt>



La classe dell'oggetto deve essere strutturale. non è possibile creare un'istanza di una classe astratta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERRORE \_ DS \_ NON VALIDO \_ DMD**
</dt> <dd> <dl> <dt>

8360 (0x20A8)
</dt> <dt>



Impossibile trovare l'oggetto schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**ERRORE \_ DS \_ OBJ \_ GUID \_ EXISTS**
</dt> <dd> <dl> <dt>

8361 (0x20A9)
</dt> <dt>



Esiste già un oggetto locale con questo GUID (attivo o non attivo).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERRORE \_ DS \_ NOT ON \_ \_ BACKLINK**
</dt> <dd> <dl> <dt>

8362 (0x20AA)
</dt> <dt>



L'operazione non può essere eseguita su un collegamento indietro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERRORE \_ DS \_ NO \_ CROSSREF PER \_ \_ NC**
</dt> <dd> <dl> <dt>

8363 (0x20AB)
</dt> <dt>



Impossibile trovare il riferimento incrociato per il contesto dei nomi specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERRORE \_ DURANTE \_ L'ARRESTO DI \_ DS**
</dt> <dd> <dl> <dt>

8364 (0x20AC)
</dt> <dt>



Impossibile eseguire l'operazione perché il servizio directory è in fase di arresto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**ERRORE \_ OPERAZIONE \_ SCONOSCIUTA DS \_**
</dt> <dd> <dl> <dt>

8365 (0x20AD)
</dt> <dt>



La richiesta del servizio directory non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERRORE \_ DS \_ PROPRIETARIO DEL RUOLO \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

8366 (0x20AE)
</dt> <dt>



Impossibile leggere l'attributo del proprietario del ruolo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERRORE \_ DS \_ COULDNT \_ CONTACT \_ FSMO**
</dt> <dd> <dl> <dt>

8367 (0x20AF)
</dt> <dt>



L'operazione FSMO richiesta non è riuscita. Impossibile contattare il proprietario FSMO corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERRORE \_ DS \_ CROSS \_ NC \_ DN \_ RENAME**
</dt> <dd> <dl> <dt>

8368 (0x20B0)
</dt> <dt>



La modifica di un DN in un contesto dei nomi non è consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERRORE \_ DS \_ CANT \_ MOD SYSTEM \_ \_ ONLY**
</dt> <dd> <dl> <dt>

8369 (0x20B1)
</dt> <dt>



L'attributo non può essere modificato perché è di proprietà del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERRORE \_ SOLO \_ REPLICATORE DS \_**
</dt> <dd> <dl> <dt>

8370 (0x20B2)
</dt> <dt>



Solo il replicatore può eseguire questa funzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERRORE \_ DELLA CLASSE OBJ DS \_ NON \_ \_ \_ DEFINITA**
</dt> <dd> <dl> <dt>

8371 (0x20B3)
</dt> <dt>



La classe specificata non è definita.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERRORE \_ DS \_ OBJ \_ CLASS NOT \_ \_ SUBCLASS**
</dt> <dd> <dl> <dt>

8372 (0x20B4)
</dt> <dt>



La classe specificata non è una sottoclasse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**ERRORE RIFERIMENTO \_ NOME DS \_ NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

8373 (0x20B5)
</dt> <dt>



Il riferimento al nome non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**ERRORE \_ DS \_ CROSS REF \_ \_ EXISTS**
</dt> <dd> <dl> <dt>

8374 (0x20B6)
</dt> <dt>



Esiste già un riferimento incrociato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERRORE \_ DS \_ CANT \_ DEL MASTER \_ \_ CROSSREF**
</dt> <dd> <dl> <dt>

8375 (0x20B7)
</dt> <dt>



Non è consentito eliminare un riferimento incrociato master.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERRORE \_ DS \_ SUBTREE \_ NOTIFY NOT \_ \_ NC \_ HEAD**
</dt> <dd> <dl> <dt>

8376 (0x20B8)
</dt> <dt>



Le notifiche del sottoalbero sono supportate solo nelle testine NC.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**ERRORE \_ DS \_ NOTIFY FILTER TOO \_ \_ \_ COMPLEX**
</dt> <dd> <dl> <dt>

8377 (0x20B9)
</dt> <dt>



Il filtro di notifica è troppo complesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERRORE \_ DS \_ DUP \_ RDN**
</dt> <dd> <dl> <dt>

8378 (0x20BA)
</dt> <dt>



Aggiornamento dello schema non riuscito: RDN duplicato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ERRORE \_ DS \_ DUP \_ OID**
</dt> <dd> <dl> <dt>

8379 (0x20BB)
</dt> <dt>



Aggiornamento dello schema non riuscito: OID duplicato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**ERRORE \_ DS \_ DUP \_ MAPI \_ ID**
</dt> <dd> <dl> <dt>

8380 (0x20BC)
</dt> <dt>



Aggiornamento dello schema non riuscito: identificatore MAPI duplicato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**ERRORE \_ DS \_ DUP \_ SCHEMA ID \_ \_ GUID**
</dt> <dd> <dl> <dt>

8381 (0x20BD)
</dt> <dt>



Aggiornamento dello schema non riuscito: GUID id schema duplicato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERRORE \_ DS \_ DUP \_ LDAP DISPLAY \_ \_ NAME**
</dt> <dd> <dl> <dt>

8382 (0x20BE)
</dt> <dt>



Aggiornamento dello schema non riuscito: nome visualizzato LDAP duplicato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERRORE \_ TEST \_ \_ SEMANTICO DS ATT \_**
</dt> <dd> <dl> <dt>

8383 (0x20BF)
</dt> <dt>



Aggiornamento dello schema non riuscito: intervallo inferiore all'intervallo superiore.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERRORE DI \_ SINTASSI \_ DS \_ NON CORRISPONDENTE**
</dt> <dd> <dl> <dt>

8384 (0x20C0)
</dt> <dt>



Aggiornamento dello schema non riuscito: sintassi non corrispondente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**\_L'ERRORE DS \_ EXISTS IN DEVE \_ \_ \_ AVERE**
</dt> <dd> <dl> <dt>

8385 (0x20C1)
</dt> <dt>



Eliminazione dello schema non riuscita: l'attributo viene usato in must-contain.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**\_L'ERRORE DS \_ ESISTE IN PUÒ \_ \_ \_ AVERE**
</dt> <dd> <dl> <dt>

8386 (0x20C2)
</dt> <dt>



Eliminazione dello schema non riuscita: l'attributo viene usato in may-contain.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**ERRORE \_ DS \_ NON ESISTENTE \_ \_**
</dt> <dd> <dl> <dt>

8387 (0x20C3)
</dt> <dt>



Aggiornamento dello schema non riuscito: l'attributo in may-contain non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**ERRORE \_ DS \_ INESISTENTE \_ DEVE \_ AVERE**
</dt> <dd> <dl> <dt>

8388 (0x20C4)
</dt> <dt>



Aggiornamento dello schema non riuscito: l'attributo in must-contain non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERRORE \_ DS \_ AUX \_ CLS \_ TEST \_ FAIL**
</dt> <dd> <dl> <dt>

8389 (0x20C5)
</dt> <dt>



Aggiornamento dello schema non riuscito: la classe nell'elenco di classi ausiliarie non esiste o non è una classe ausiliaria.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERRORE \_ DS \_ \_ POSS \_ SUP INESISTENTE**
</dt> <dd> <dl> <dt>

8390 (0x20C6)
</dt> <dt>



Aggiornamento dello schema non riuscito: la classe in poss-superiors non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERRORE \_ DS \_ SUB \_ CLS TEST \_ \_ FAIL**
</dt> <dd> <dl> <dt>

8391 (0x20C7)
</dt> <dt>



Aggiornamento dello schema non riuscito: la classe nell'elenco subclassof non esiste o non soddisfa le regole di gerarchia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERRORE \_ DS \_ SINTASSI \_ ID RDN \_ ATT NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

8392 (0x20C8)
</dt> <dt>



Aggiornamento dello schema non riuscito: La sintassi di Rdn-Att-Id non è corretta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**ERRORE \_ DS \_ ESISTENTE IN \_ \_ AUX \_ CLS**
</dt> <dd> <dl> <dt>

8393 (0x20C9)
</dt> <dt>



Eliminazione dello schema non riuscita: la classe viene usata come classe ausiliaria.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**ERRORE \_ DS \_ PRESENTE IN \_ SUB \_ \_ CLS**
</dt> <dd> <dl> <dt>

8394 (0x20CA)
</dt> <dt>



Eliminazione dello schema non riuscita: la classe viene usata come sottoclasse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**ERRORE \_ DS \_ EXISTS IN \_ \_ POSS \_ SUP**
</dt> <dd> <dl> <dt>

8395 (0x20CB)
</dt> <dt>



Eliminazione dello schema non riuscita: la classe viene usata come poss superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**ERRORE \_ DS \_ RECALCSCHEMA \_ FAILED**
</dt> <dd> <dl> <dt>

8396 (0x20CC)
</dt> <dt>



Aggiornamento dello schema non riuscito durante il ricalcolo della cache di convalida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERRORE DURANTE \_ L'ELIMINAZIONE \_ DELL'ALBERO \_ DS \_ NON \_ COMPLETATA**
</dt> <dd> <dl> <dt>

8397 (0x20CD)
</dt> <dt>



L'eliminazione dell'albero non è stata completata. Per continuare a eliminare l'albero, è necessario eseguire di nuovo la richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERRORE \_ DS \_ CANT \_ DELETE**
</dt> <dd> <dl> <dt>

8398 (0x20CE)
</dt> <dt>



Impossibile eseguire l'operazione di eliminazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**ERRORE \_ DS \_ ATT \_ SCHEMA \_ REQ \_ ID**
</dt> <dd> <dl> <dt>

8399 (0x20CF)
</dt> <dt>



Impossibile leggere l'identificatore di classe governs per il record dello schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**ERRORE \_ DS \_ SINTASSI \_ DELLO SCHEMA ATT NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

8400 (0x20D0)
</dt> <dt>



La sintassi dello schema dell'attributo non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERRORE \_ DS \_ CANT \_ CACHE \_ ATT**
</dt> <dd> <dl> <dt>

8401 (0x20D1)
</dt> <dt>



Impossibile memorizzare l'attributo nella cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERROR \_ DS \_ CANT \_ CACHE \_ CLASS**
</dt> <dd> <dl> <dt>

8402 (0x20D2)
</dt> <dt>



Impossibile memorizzare la classe nella cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERRORE \_ DS \_ CANT \_ REMOVE \_ ATT \_ CACHE**
</dt> <dd> <dl> <dt>

8403 (0x20D3)
</dt> <dt>



Impossibile rimuovere l'attributo dalla cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**ERRORE \_ DS \_ CANT \_ REMOVE CLASS \_ \_ CACHE**
</dt> <dd> <dl> <dt>

8404 (0x20D4)
</dt> <dt>



Impossibile rimuovere la classe dalla cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**ERRORE \_ DS \_ CANT \_ RETRIEVE \_ DN**
</dt> <dd> <dl> <dt>

8405 (0x20D5)
</dt> <dt>



Impossibile leggere l'attributo del nome distinto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERRORE \_ DS \_ MISSING \_ SUPREF**
</dt> <dd> <dl> <dt>

8406 (0x20D6)
</dt> <dt>



Non è stato configurato alcun riferimento superiore per il servizio directory. Il servizio directory non è quindi in grado di rilasciare riferimenti a oggetti esterni a questa foresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**ERRORE \_ DS \_ CANT \_ RETRIEVE \_ INSTANCE**
</dt> <dd> <dl> <dt>

8407 (0x20D7)
</dt> <dt>



Impossibile recuperare l'attributo del tipo di istanza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**\_INCOERENZA DEL CODICE DS \_ \_ DI ERRORE**
</dt> <dd> <dl> <dt>

8408 (0x20D8)
</dt> <dt>



Si è verificato un errore interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**ERRORE \_ DEL DATABASE DS \_ \_**
</dt> <dd> <dl> <dt>

8409 (0x20D9)
</dt> <dt>



Si è verificato un errore del database.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERRORE \_ DS \_ GOVERNSID \_ MANCANTE**
</dt> <dd> <dl> <dt>

8410 (0x20DA)
</dt> <dt>



Attributo GOVERNSID mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**ERRORE \_ DS \_ MANCANTE \_ \_ ATT PREVISTO**
</dt> <dd> <dl> <dt>

8411 (0x20DB)
</dt> <dt>



Attributo previsto mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERRORE \_ DS \_ NCNAME \_ MISSING \_ CR \_ REF**
</dt> <dd> <dl> <dt>

8412 (0x20DC)
</dt> <dt>



Nel contesto dei nomi specificato manca un riferimento incrociato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**ERRORE DI \_ CONTROLLO DELLA \_ SICUREZZA DS \_ \_**
</dt> <dd> <dl> <dt>

8413 (0x20DD)
</dt> <dt>



Si è verificato un errore di controllo di sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**ERRORE \_ SCHEMA DS \_ NON \_ \_ CARICATO**
</dt> <dd> <dl> <dt>

8414 (0x20DE)
</dt> <dt>



Lo schema non è caricato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERRORE \_ DS \_ SCHEMA \_ ALLOC \_ FAILED**
</dt> <dd> <dl> <dt>

8415 (0x20DF)
</dt> <dt>



Allocazione dello schema non riuscita. Controllare se la memoria del computer è insufficiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERRORE \_ SINTASSI DI DS \_ ATT \_ SCHEMA \_ REQ \_**
</dt> <dd> <dl> <dt>

8416 (0x20E0)
</dt> <dt>



Impossibile ottenere la sintassi necessaria per lo schema dell'attributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**ERRORE \_ DS \_ \_ GCVERIFY ERROR**
</dt> <dd> <dl> <dt>

8417 (0x20E1)
</dt> <dt>



La verifica del catalogo globale non è riuscita. Il catalogo globale non è disponibile o non supporta l'operazione. Parte della directory non è attualmente disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERRORE \_ DS \_ DRA SCHEMA \_ \_ MISMATCH**
</dt> <dd> <dl> <dt>

8418 (0x20E2)
</dt> <dt>



L'operazione di replica non è riuscita a causa di una mancata corrispondenza dello schema tra i server coinvolti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERRORE \_ DS \_ CANT \_ FIND \_ DSA \_ OBJ**
</dt> <dd> <dl> <dt>

8419 (0x20E3)
</dt> <dt>



Impossibile trovare l'oggetto DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**ERRORE \_ DS \_ CANT \_ FIND EXPECTED \_ \_ NC**
</dt> <dd> <dl> <dt>

8420 (0x20E4)
</dt> <dt>



Impossibile trovare il contesto dei nomi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERRORE \_ DS \_ CANT \_ FIND \_ NC IN \_ \_ CACHE**
</dt> <dd> <dl> <dt>

8421 (0x20E5)
</dt> <dt>



Impossibile trovare il contesto dei nomi nella cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**ERRORE \_ DS \_ CANT \_ RETRIEVE \_ CHILD**
</dt> <dd> <dl> <dt>

8422 (0x20E6)
</dt> <dt>



Impossibile recuperare l'oggetto figlio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERRORE DI \_ MODIFICA NON VALIDA DELLA SICUREZZA \_ \_ DS \_**
</dt> <dd> <dl> <dt>

8423 (0x20E7)
</dt> <dt>



La modifica non è stata consentita per motivi di sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERRORE \_ DS \_ CANT \_ REPLACE HIDDEN \_ \_ REC**
</dt> <dd> <dl> <dt>

8424 (0x20E8)
</dt> <dt>



L'operazione non può sostituire il record nascosto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERRORE FILE \_ DI \_ GERARCHIA \_ DS NON \_ VALIDO**
</dt> <dd> <dl> <dt>

8425 (0x20E9)
</dt> <dt>



Il file della gerarchia non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERRORE TABELLA \_ \_ GERARCHIA \_ DI COMPILAZIONE \_ DS NON \_ RIUSCITA**
</dt> <dd> <dl> <dt>

8426 (0x20EA)
</dt> <dt>



Tentativo di compilazione della tabella della gerarchia non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**ERRORE \_ DS \_ CONFIG \_ PARAM \_ MANCANTE**
</dt> <dd> <dl> <dt>

8427 (0x20EB)
</dt> <dt>



Il parametro di configurazione della directory non è presente nel Registro di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERRORE \_ DS \_ COUNTING \_ AB \_ INDICES \_ FAILED**
</dt> <dd> <dl> <dt>

8428 (0x20EC)
</dt> <dt>



Tentativo di conteggio degli indici della rubrica non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERRORE TABELLA \_ GERARCHIA DS \_ \_ \_ MALLOC \_ NON RIUSCITA**
</dt> <dd> <dl> <dt>

8429 (0x20ED)
</dt> <dt>



L'allocazione della tabella della gerarchia non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERRORE \_ INTERNO DS \_ \_**
</dt> <dd> <dl> <dt>

8430 (0x20EE)
</dt> <dt>



Il servizio directory ha rilevato un errore interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**ERRORE \_ DS \_ UNKNOWN \_ ERROR**
</dt> <dd> <dl> <dt>

8431 (0x20EF)
</dt> <dt>



Il servizio directory ha rilevato un errore sconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**LA \_ RADICE DS \_ ERROR RICHIEDE LA CLASSE \_ \_ \_ TOP**
</dt> <dd> <dl> <dt>

8432 (0x20F0)
</dt> <dt>



Un oggetto radice richiede una classe 'top'.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERRORE \_ DS \_ CHE RIFIUTA I \_ RUOLI \_ FSMO**
</dt> <dd> <dl> <dt>

8433 (0x20F1)
</dt> <dt>



Questo server di directory è in fase di arresto e non può assumere la proprietà dei nuovi ruoli di operazione a master singolo mobile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**ERRORE \_ DS \_ IMPOSTAZIONI \_ FSMO \_ MANCANTI**
</dt> <dd> <dl> <dt>

8434 (0x20F2)
</dt> <dt>



Il servizio directory non contiene informazioni di configurazione obbligatorie e non è in grado di determinare la proprietà dei ruoli delle operazioni a master singolo mobili.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERRORE \_ DS \_ NON È IN GRADO DI RIMUOVERE I \_ \_ \_ RUOLI**
</dt> <dd> <dl> <dt>

8435 (0x20F3)
</dt> <dt>



Il servizio directory non è stato in grado di trasferire la proprietà di uno o più ruoli di operazione a master singolo mobile ad altri server.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERRORE \_ DS \_ DRA \_ GENERIC**
</dt> <dd> <dl> <dt>

8436 (0x20F4)
</dt> <dt>



L'operazione di replica non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERRORE \_ DS \_ DRA PARAMETRO NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

8437 (0x20F5)
</dt> <dt>



È stato specificato un parametro non valido per questa operazione di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERRORE \_ DS \_ DRA \_ OCCUPATO**
</dt> <dd> <dl> <dt>

8438 (0x20F6)
</dt> <dt>



Il servizio directory è troppo occupato per completare l'operazione di replica in questo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERRORE \_ DS \_ DRA BAD \_ \_ DN**
</dt> <dd> <dl> <dt>

8439 (0x20F7)
</dt> <dt>



Il nome distinto specificato per questa operazione di replica non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERRORE \_ DS \_ DRA BAD \_ \_ NC**
</dt> <dd> <dl> <dt>

8440 (0x20F8)
</dt> <dt>



Il contesto dei nomi specificato per questa operazione di replica non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERRORE \_ DS \_ DS \_ DN \_ ESISTENTE**
</dt> <dd> <dl> <dt>

8441 (0x20F9)
</dt> <dt>



Il nome distinto specificato per questa operazione di replica esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**ERRORE \_ DS \_ ERRORE \_ INTERNO DRA \_**
</dt> <dd> <dl> <dt>

8442 (0x20FA)
</dt> <dt>



Il sistema di replica ha rilevato un errore interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERRORE \_ DS \_ DRA INCONSISTENT \_ \_ DIT**
</dt> <dd> <dl> <dt>

8443 (0x20FB)
</dt> <dt>



L'operazione di replica ha rilevato un'incoerenza del database.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERRORE \_ CONNESSIONE \_ DS DRA NON \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

8444 (0x20FC)
</dt> <dt>



Impossibile contattare il server specificato per questa operazione di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERRORE \_ DS \_ DRA TIPO DI ISTANZA NON \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

8445 (0x20FD)
</dt> <dt>



L'operazione di replica ha rilevato un oggetto con un tipo di istanza non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERRORE \_ DS \_ DRA OUT \_ OF \_ \_ MEM**
</dt> <dd> <dl> <dt>

8446 (0x20FE)
</dt> <dt>



L'operazione di replica non è riuscita ad allocare memoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**ERRORE \_ PROBLEMA DI POSTA ELETTRONICA \_ DS DRA \_ \_**
</dt> <dd> <dl> <dt>

8447 (0x20FF)
</dt> <dt>



L'operazione di replica ha rilevato un errore con il sistema di posta elettronica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**ERRORE \_ DS \_ DRA REF \_ GIÀ \_ \_ ESISTENTE**
</dt> <dd> <dl> <dt>

8448 (0x2100)
</dt> <dt>



Le informazioni di riferimento sulla replica per il server di destinazione esistono già.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERRORE \_ DS \_ DRA REF NON \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

8449 (0x2101)
</dt> <dt>



Le informazioni di riferimento sulla replica per il server di destinazione non esistono.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERRORE \_ DS \_ DRA \_ OBJ IS REP \_ \_ \_ SOURCE**
</dt> <dd> <dl> <dt>

8450 (0x2102)
</dt> <dt>



Impossibile rimuovere il contesto dei nomi perché viene replicato in un altro server.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**ERRORE \_ DS \_ DRA DB \_ \_ ERROR**
</dt> <dd> <dl> <dt>

8451 (0x2103)
</dt> <dt>



L'operazione di replica ha rilevato un errore del database.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERRORE \_ DS \_ DRA NO \_ \_ REPLICA**
</dt> <dd> <dl> <dt>

8452 (0x2104)
</dt> <dt>



Il contesto dei nomi è in fase di rimozione o non viene replicato dal server specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERRORE \_ DS \_ ACCESSO DRA \_ \_ NEGATO**
</dt> <dd> <dl> <dt>

8453 (0x2105)
</dt> <dt>



L'accesso alla replica è stato negato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**ERRORE \_ DS \_ DRA NON \_ \_ SUPPORTATO**
</dt> <dd> <dl> <dt>

8454 (0x2106)
</dt> <dt>



L'operazione richiesta non è supportata da questa versione del servizio directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERRORE \_ DS \_ DRA RPC \_ \_ ANNULLATO**
</dt> <dd> <dl> <dt>

8455 (0x2107)
</dt> <dt>



La chiamata di procedura remota di replica è stata annullata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**ERRORE \_ DS \_ ORIGINE DRA \_ \_ DISABILITATA**
</dt> <dd> <dl> <dt>

8456 (0x2108)
</dt> <dt>



Il server di origine sta attualmente rifiutando le richieste di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERRORE \_ DS \_ DRA SINK \_ \_ DISABILITATO**
</dt> <dd> <dl> <dt>

8457 (0x2109)
</dt> <dt>



Il server di destinazione sta attualmente rifiutando le richieste di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**ERRORE \_ DS \_ DRA NAME \_ \_ COLLISION**
</dt> <dd> <dl> <dt>

8458 (0x210A)
</dt> <dt>



L'operazione di replica non è riuscita a causa di un conflitto di nomi di oggetti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERRORE \_ DELL'ORIGINE \_ DS DRA \_ \_ REINSTALLATA**
</dt> <dd> <dl> <dt>

8459 (0x210B)
</dt> <dt>



L'origine della replica è stata reinstallata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERRORE \_ DS \_ DRA \_ \_ MANCANTE PADRE**
</dt> <dd> <dl> <dt>

8460 (0x210C)
</dt> <dt>



L'operazione di replica non è riuscita perché manca un oggetto padre obbligatorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERRORE \_ DS \_ DRA \_ PREEMPTED**
</dt> <dd> <dl> <dt>

8461 (0x210D)
</dt> <dt>



L'operazione di replica è stata preempted.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERRORE \_ DS \_ DRA ABANDON \_ \_ SYNC**
</dt> <dd> <dl> <dt>

8462 (0x210E)
</dt> <dt>



Il tentativo di sincronizzazione della replica è stato abbandonato a causa della mancanza di aggiornamenti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERRORE \_ DS \_ DRA \_ SHUTDOWN**
</dt> <dd> <dl> <dt>

8463 (0x210F)
</dt> <dt>



L'operazione di replica è stata terminata perché il sistema è in fase di arresto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERRORE \_ DS \_ DRA \_ INCOMPATIBILE \_ SET \_ PARZIALE**
</dt> <dd> <dl> <dt>

8464 (0x2110)
</dt> <dt>



Tentativo di sincronizzazione non riuscito perché il controller di dominio di destinazione è attualmente in attesa di sincronizzare nuovi attributi parziali dall'origine. Questa condizione è normale se una modifica recente dello schema ha modificato il set di attributi parziali. Il set di attributi parziali di destinazione non è un subset del set di attributi parziali di origine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**ERRORE \_ DS \_ DRA SOURCE IS PARTIAL \_ \_ \_ \_ REPLICA**
</dt> <dd> <dl> <dt>

8465 (0x2111)
</dt> <dt>



Il tentativo di sincronizzazione della replica non è riuscito perché una replica master ha tentato di eseguire la sincronizzazione da una replica parziale.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERRORE \_ DS \_ DRA \_ EXTN \_ CONNECTION \_ FAILED**
</dt> <dd> <dl> <dt>

8466 (0x2112)
</dt> <dt>



Il server specificato per questa operazione di replica è stato contattato, ma non è stato in grado di contattare un server aggiuntivo necessario per completare l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERRORE \_ DI MANCATA \_ CORRISPONDENZA DELLO SCHEMA DI INSTALLAZIONE \_ \_ DS**
</dt> <dd> <dl> <dt>

8467 (0x2113)
</dt> <dt>



La versione dello schema del servizio directory della foresta di origine non è compatibile con la versione del servizio directory nel computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**ERRORE \_ DS \_ DUP \_ LINK \_ ID**
</dt> <dd> <dl> <dt>

8468 (0x2114)
</dt> <dt>



Aggiornamento dello schema non riuscito: esiste già un attributo con lo stesso identificatore di collegamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**ERRORE \_ DURANTE LA RISOLUZIONE DELL'ERRORE DEL NOME \_ \_ \_ DS**
</dt> <dd> <dl> <dt>

8469 (0x2115)
</dt> <dt>



Conversione del nome: errore di elaborazione generico.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**ERRORE \_ NOME DS \_ NON \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

8470 (0x2116)
</dt> <dt>



Traduzione del nome: impossibile trovare il nome o diritto insufficiente per visualizzare il nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**ERRORE \_ NOME DS \_ ERRORE NON \_ \_ \_ UNIVOCO**
</dt> <dd> <dl> <dt>

8471 (0x2117)
</dt> <dt>



Conversione del nome: nome di input mappato a più di un nome di output.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**ERRORE \_ DS \_ NAME ERROR NO \_ \_ \_ MAPPING**
</dt> <dd> <dl> <dt>

8472 (0x2118)
</dt> <dt>



Conversione del nome: nome di input trovato, ma non il formato di output associato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERRORE \_ DS \_ NAME ERROR DOMAIN \_ \_ \_ ONLY**
</dt> <dd> <dl> <dt>

8473 (0x2119)
</dt> <dt>



Conversione dei nomi: impossibile risolvere completamente, è stato trovato solo il dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**ERRORE \_ DS \_ NAME ERROR NO \_ \_ \_ SYNTACTICAL \_ MAPPING**
</dt> <dd> <dl> <dt>

8474 (0x211A)
</dt> <dt>



Conversione dei nomi: non è possibile eseguire il mapping puramente sintattico nel client senza uscire in rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERRORE \_ DS \_ CONSTRUCTED \_ ATT \_ MOD**
</dt> <dd> <dl> <dt>

8475 (0x211B)
</dt> <dt>



La modifica di un attributo costruito non è consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**ERRORE \_ DS \_ WRONG \_ OM \_ OBJ \_ CLASS**
</dt> <dd> <dl> <dt>

8476 (0x211C)
</dt> <dt>



OM-Object-Class specificato non è corretto per un attributo con la sintassi specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERRORE \_ DS \_ DRA \_ REPL \_ PENDING**
</dt> <dd> <dl> <dt>

8477 (0x211D)
</dt> <dt>



La richiesta di replica è stata inviata. in attesa di risposta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERRORE \_ DS \_ DS \_ OBBLIGATORIO**
</dt> <dd> <dl> <dt>

8478 (0x211E)
</dt> <dt>



L'operazione richiesta richiede un servizio directory e non ne è disponibile nessuno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERRORE \_ DS \_ NOME VISUALIZZATO LDAP \_ NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

8479 (0x211F)
</dt> <dt>



Il nome visualizzato LDAP della classe o dell'attributo contiene caratteri non ASCII.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERRORE \_ RICERCA \_ DS NON DI \_ \_ BASE**
</dt> <dd> <dl> <dt>

8480 (0x2120)
</dt> <dt>



L'operazione di ricerca richiesta è supportata solo per le ricerche di base.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERRORE \_ DS \_ CANT \_ RETRIEVE \_ ATTS**
</dt> <dd> <dl> <dt>

8481 (0x2121)
</dt> <dt>



La ricerca non è riuscita a recuperare gli attributi dal database.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERRORE \_ DI \_ BACKLINK DS \_ SENZA \_ COLLEGAMENTO**
</dt> <dd> <dl> <dt>

8482 (0x2122)
</dt> <dt>



L'operazione di aggiornamento dello schema ha tentato di aggiungere un attributo di collegamento a ritroso che non ha un collegamento in avanti corrispondente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERRORE \_ DS \_ EPOCH \_ MISMATCH**
</dt> <dd> <dl> <dt>

8483 (0x2123)
</dt> <dt>



L'origine e la destinazione di uno spostamento tra domini non concordano sul numero di periodo dell'oggetto. L'origine o la destinazione non dispone della versione più recente dell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERRORE \_ DS \_ SRC \_ NAME \_ MISMATCH**
</dt> <dd> <dl> <dt>

8484 (0x2124)
</dt> <dt>



L'origine e la destinazione di uno spostamento tra domini non concordano sul nome corrente dell'oggetto. L'origine o la destinazione non dispone della versione più recente dell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERRORE \_ DS \_ SRC \_ E \_ DST \_ NC \_ IDENTICO**
</dt> <dd> <dl> <dt>

8485 (0x2125)
</dt> <dt>



L'origine e la destinazione per l'operazione di spostamento tra domini sono identiche. Il chiamante deve usare l'operazione di spostamento locale anziché l'operazione di spostamento tra domini.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERRORE \_ DS \_ DST \_ NC \_ MISMATCH**
</dt> <dd> <dl> <dt>

8486 (0x2126)
</dt> <dt>



L'origine e la destinazione di uno spostamento tra domini non sono in accordo sui contesti di denominazione nella foresta. L'origine o la destinazione non dispone della versione più recente del contenitore Partizioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERRORE \_ DS \_ NOT \_ AUTHORITIVE \_ FOR \_ DST \_ NC**
</dt> <dd> <dl> <dt>

8487 (0x2127)
</dt> <dt>



La destinazione di uno spostamento tra domini non è autorevole per il contesto dei nomi di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERRORE \_ DS \_ SRC \_ GUID NON \_ CORRISPONDENTE**
</dt> <dd> <dl> <dt>

8488 (0x2128)
</dt> <dt>



L'origine e la destinazione di uno spostamento tra domini non concordano sull'identità dell'oggetto di origine. L'origine o la destinazione non dispone della versione più recente dell'oggetto di origine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERRORE \_ DS \_ CANT \_ MOVE DELETED \_ \_ OBJECT**
</dt> <dd> <dl> <dt>

8489 (0x2129)
</dt> <dt>



L'oggetto spostato tra domini è già noto per essere eliminato dal server di destinazione. Il server di origine non dispone della versione più recente dell'oggetto di origine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**ERRORE \_ DURANTE L'OPERAZIONE \_ PDC \_ DS IN \_ \_ CORSO**
</dt> <dd> <dl> <dt>

8490 (0x212A)
</dt> <dt>



È già in corso un'altra operazione che richiede l'accesso esclusivo al FSMO PDC.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERRORE \_ DS \_ CROSS DOMAIN \_ CLEANUP \_ \_ REQD**
</dt> <dd> <dl> <dt>

8491 (0x212B)
</dt> <dt>



Un'operazione di spostamento tra domini non è riuscita in modo che esistano due versioni dell'oggetto spostato, una ognuna nei domini di origine e di destinazione. L'oggetto di destinazione deve essere rimosso per ripristinare lo stato coerente del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERRORE \_ DS \_ OPERAZIONE DI SPOSTAMENTO \_ XDOM NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

8492 (0x212C)
</dt> <dt>



Questo oggetto non può essere spostato tra i limiti di dominio perché gli spostamenti tra domini per questa classe non sono consentiti o l'oggetto presenta alcune caratteristiche speciali, ad esempio un account di attendibilità o un RID con restrizioni, che ne impediscono lo spostamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERRORE \_ DS \_ CANT \_ WITH \_ ACCT GROUP \_ \_ MEMBERSHPS**
</dt> <dd> <dl> <dt>

8493 (0x212D)
</dt> <dt>



Non è possibile spostare oggetti con appartenenze tra i limiti di dominio perché una volta spostati, ciò violerebbe le condizioni di appartenenza del gruppo di account. Rimuovere l'oggetto dalle appartenenze a gruppi di account e riprovare.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**ERRORE \_ DS \_ NC \_ DEVE AVERE \_ \_ NC \_ PADRE**
</dt> <dd> <dl> <dt>

8494 (0x212E)
</dt> <dt>



Un'head del contesto dei nomi deve essere l'elemento figlio immediato di un altro head del contesto dei nomi, non di un nodo interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERRORE \_ DS \_ CR \_ IMPOSSIBILE \_ \_ CONVALIDARE**
</dt> <dd> <dl> <dt>

8495 (0x212F)
</dt> <dt>



La directory non può convalidare il nome del contesto dei nomi proposto perché non contiene una replica del contesto dei nomi al di sopra del contesto dei nomi proposto. Assicurarsi che il ruolo di master per la denominazione dei domini sia utilizzato da un server configurato come server di catalogo globale e che il server sia aggiornato con i partner di replica. Si applica solo ai Windows 2000 Domain Naming.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERRORE \_ DS \_ DST \_ DOMAIN NOT \_ \_ NATIVE**
</dt> <dd> <dl> <dt>

8496 (0x2130)
</dt> <dt>



Il dominio di destinazione deve essere in modalità nativa.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERRORE \_ DS \_ - CONTENITORE INFRASTRUTTURA \_ \_ MANCANTE**
</dt> <dd> <dl> <dt>

8497 (0x2131)
</dt> <dt>



Non è possibile eseguire l'operazione perché il server non dispone di un contenitore dell'infrastruttura nel dominio di interesse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERRORE \_ DS \_ CANT \_ MOVE ACCOUNT \_ \_ GROUP**
</dt> <dd> <dl> <dt>

8498 (0x2132)
</dt> <dt>



Lo spostamento tra domini di gruppi di account non vuoti non è consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERRORE \_ DS \_ CANT \_ MOVE RESOURCE \_ \_ GROUP**
</dt> <dd> <dl> <dt>

8499 (0x2133)
</dt> <dt>



Lo spostamento tra domini di gruppi di risorse non vuoti non è consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**ERRORE \_ DS \_ FLAG DI RICERCA \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

8500 (0x2134)
</dt> <dt>



I flag di ricerca per l'attributo non sono validi. Il bit ANR è valido solo per attributi di stringhe Unicode o Teletex.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERRORE \_ DS \_ NO TREE DELETE ABOVE \_ \_ \_ \_ NC**
</dt> <dd> <dl> <dt>

8501 (0x2135)
</dt> <dt>



Le eliminazioni dell'albero a partire da un oggetto che ha un'head NC come discendente non sono consentite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERRORE \_ DS \_ COULDNT \_ LOCK TREE \_ \_ FOR \_ DELETE**
</dt> <dd> <dl> <dt>

8502 (0x2136)
</dt> <dt>



Il servizio directory non è riuscito a bloccare un albero in preparazione per l'eliminazione di un albero perché era in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERRORE \_ DS \_ COULDNT \_ IDENTIFY OBJECTS FOR TREE \_ \_ \_ \_ DELETE**
</dt> <dd> <dl> <dt>

8503 (0x2137)
</dt> <dt>



Il servizio directory non è riuscito a identificare l'elenco di oggetti da eliminare durante il tentativo di eliminazione di un albero.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERRORE \_ DS \_ SAM \_ INIT \_ FAILURE**
</dt> <dd> <dl> <dt>

8504 (0x2138)
</dt> <dt>



Inizializzazione di Gestione account di sicurezza non riuscita a causa dell'errore seguente: %1. Stato errore: 0x%2. Arrestare il sistema e riavviare il sistema in modalità ripristino servizi directory. Per informazioni più dettagliate, controllare il registro eventi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**ERRORE \_ VIOLAZIONE GRUPPO SENSIBILE \_ \_ DS \_**
</dt> <dd> <dl> <dt>

8505 (0x2139)
</dt> <dt>



Solo un amministratore può modificare l'elenco di appartenenze di un gruppo amministrativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERRORE \_ DS \_ CANT \_ MOD \_ PRIMARYGROUPID**
</dt> <dd> <dl> <dt>

8506 (0x213A)
</dt> <dt>



Impossibile modificare l'ID gruppo primario di un account controller di dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERRORE \_ DS \_ NON VALIDO BASE \_ SCHEMA \_ \_ MOD**
</dt> <dd> <dl> <dt>

8507 (0x213B)
</dt> <dt>



Si è tentato di modificare lo schema di base.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**ERRORE \_ DI MODIFICA DELLO SCHEMA NON SICURO \_ \_ DS \_**
</dt> <dd> <dl> <dt>

8508 (0x213C)
</dt> <dt>



L'aggiunta di un nuovo attributo obbligatorio a una classe esistente, l'eliminazione di un attributo obbligatorio da una classe esistente o l'aggiunta di un attributo facoltativo alla classe speciale Top che non è un attributo backlink (direttamente o tramite ereditarietà, ad esempio aggiungendo o eliminando una classe ausiliaria) non è consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERRORE \_ DS \_ SCHEMA UPDATE \_ \_ DISALLOWED**
</dt> <dd> <dl> <dt>

8509 (0x213D)
</dt> <dt>



L'aggiornamento dello schema non è consentito in questo controller di dominio perché il controller di dominio non è il proprietario del ruolo FSMO dello schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERRORE \_ DS \_ CANT \_ CREATE IN \_ \_ SCHEMA**
</dt> <dd> <dl> <dt>

8510 (0x213E)
</dt> <dt>



Non è possibile creare un oggetto di questa classe nel contenitore dello schema. È possibile creare oggetti attribute-schema e class-schema solo nel contenitore dello schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERRORE \_ DS \_ INSTALL NO \_ \_ SRC SCH \_ \_ VERSION**
</dt> <dd> <dl> <dt>

8511 (0x213F)
</dt> <dt>



L'installazione della replica/figlio non è riuscita a ottenere l'attributo objectVersion nel contenitore dello schema nel controller di dominio di origine. L'attributo non è presente nel contenitore dello schema o le credenziali fornite non dispongono dell'autorizzazione per leggerlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERRORE \_ DS \_ INSTALL NO SCH VERSION IN \_ \_ \_ \_ \_ INIFILE**
</dt> <dd> <dl> <dt>

8512 (0x2140)
</dt> <dt>



L'installazione della replica/figlio non è riuscita a leggere l'attributo objectVersion nella sezione SCHEMA del file schema.ini nella directory system32.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERRORE \_ DS \_ TIPO DI GRUPPO \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

8513 (0x2141)
</dt> <dt>



Il tipo di gruppo specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERRORE \_ DS \_ NO NEST \_ \_ GLOBALGROUP IN \_ \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8514 (0x2142)
</dt> <dt>



Non è possibile annidare gruppi globali in un dominio misto se il gruppo è abilitato per la sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERRORE \_ DS \_ NO NEST \_ \_ LOCALGROUP IN \_ \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8515 (0x2143)
</dt> <dt>



Non è possibile annidare gruppi locali in un dominio misto se il gruppo è abilitato per la sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERRORE \_ DS \_ GLOBAL \_ CANT HAVE LOCAL \_ \_ \_ MEMBER**
</dt> <dd> <dl> <dt>

8516 (0x2144)
</dt> <dt>



Un gruppo globale non può avere un gruppo locale come membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERRORE \_ DS \_ GLOBAL \_ CANT HAVE UNIVERSAL \_ \_ \_ MEMBER**
</dt> <dd> <dl> <dt>

8517 (0x2145)
</dt> <dt>



Un gruppo globale non può avere un gruppo universale come membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERRORE \_ DS \_ UNIVERSAL \_ CANT HAVE LOCAL \_ \_ \_ MEMBER**
</dt> <dd> <dl> <dt>

8518 (0x2146)
</dt> <dt>



Un gruppo universale non può avere un gruppo locale come membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERRORE \_ DS \_ GLOBAL \_ CANT HAVE \_ \_ CROSSDOMAIN \_ MEMBER**
</dt> <dd> <dl> <dt>

8519 (0x2147)
</dt> <dt>



Un gruppo globale non può avere un membro tra domini.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERRORE \_ DS \_ LOCAL \_ CANT HAVE \_ \_ CROSSDOMAIN LOCAL \_ \_ MEMBER**
</dt> <dd> <dl> <dt>

8520 (0x2148)
</dt> <dt>



Un gruppo locale non può avere un altro gruppo locale tra domini come membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**ERRORE \_ DS \_ HAVE PRIMARY \_ \_ MEMBERS**
</dt> <dd> <dl> <dt>

8521 (0x2149)
</dt> <dt>



Un gruppo con membri primari non può passare a un gruppo con sicurezza disabilitata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERRORE \_ DS \_ STRING \_ SD CONVERSION \_ \_ FAILED**
</dt> <dd> <dl> <dt>

8522 (0x214A)
</dt> <dt>



Il caricamento della cache dello schema non è riuscito a convertire la stringa SD predefinita in un oggetto class-schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERRORE \_ DS \_ NAMING MASTER \_ \_ GC**
</dt> <dd> <dl> <dt>

8523 (0x214B)
</dt> <dt>



Solo gli account DSA configurati come server di catalogo globale devono essere autorizzati a contenere il ruolo FSMO domain naming master. Si applica solo a Windows 2000 server.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERRORE \_ DI RICERCA DNS \_ DS \_ \_**
</dt> <dd> <dl> <dt>

8524 (0x214C)
</dt> <dt>



L'operazione DSA non è in grado di procedere a causa di un errore di ricerca DNS.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**ERRORE \_ DS \_ COULDNT \_ UPDATE \_ SPN**
</dt> <dd> <dl> <dt>

8525 (0x214D)
</dt> <dt>



Durante l'elaborazione di una modifica al nome host DNS per un oggetto, i valori del nome dell'entità servizio non possono essere mantenuti sincronizzati.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERRORE \_ DS \_ CANT \_ RETRIEVE \_ SD**
</dt> <dd> <dl> <dt>

8526 (0x214E)
</dt> <dt>



Impossibile leggere l'attributo Descrittore di sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERRORE \_ CHIAVE DS \_ NON \_ \_ UNIVOCA**
</dt> <dd> <dl> <dt>

8527 (0x214F)
</dt> <dt>



L'oggetto richiesto non è stato trovato, ma è stato trovato un oggetto con tale chiave.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERRORE \_ DS \_ SINTASSI \_ \_ ATT \_ COLLEGATA ERRATA**
</dt> <dd> <dl> <dt>

8528 (0x2150)
</dt> <dt>



La sintassi dell'attributo collegato aggiunto non è corretta. I collegamenti in avanti possono avere solo la sintassi 2.5.5.1, 2.5.5.7 e 2.5.5.14 e i backlink possono avere solo la sintassi 2.5.5.1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERRORE \_ DS \_ SAM NEED \_ \_ BOOTKEY \_ PASSWORD**
</dt> <dd> <dl> <dt>

8529 (0x2151)
</dt> <dt>



Security Account Manager deve ottenere la password di avvio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERRORE \_ DS \_ SAM NEED \_ \_ BOOTKEY \_ FLOPPY**
</dt> <dd> <dl> <dt>

8530 (0x2152)
</dt> <dt>



Security Account Manager deve ottenere la chiave di avvio dal disco floppy.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERRORE \_ DS \_ CANT \_ START**
</dt> <dd> <dl> <dt>

8531 (0x2153)
</dt> <dt>



Impossibile avviare il servizio directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERRORE \_ DS \_ INIT \_ FAILURE**
</dt> <dd> <dl> <dt>

8532 (0x2154)
</dt> <dt>



Impossibile avviare i servizi directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERRORE \_ DS \_ NO \_ PKT PRIVACY ON \_ \_ \_ CONNECTION**
</dt> <dd> <dl> <dt>

8533 (0x2155)
</dt> <dt>



La connessione tra client e server richiede la privacy dei pacchetti o una migliore.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERRORE \_ DOMINIO DI ORIGINE \_ DS NELLA \_ \_ \_ FORESTA**
</dt> <dd> <dl> <dt>

8534 (0x2156)
</dt> <dt>



Il dominio di origine potrebbe non essere nella stessa foresta della destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERRORE \_ DOMINIO DI DESTINAZIONE \_ \_ DS NON NELLA \_ \_ \_ FORESTA**
</dt> <dd> <dl> <dt>

8535 (0x2157)
</dt> <dt>



Il dominio di destinazione deve essere nella foresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**ERRORE \_ CONTROLLO DESTINAZIONE DS NON \_ \_ \_ \_ ABILITATO**
</dt> <dd> <dl> <dt>

8536 (0x2158)
</dt> <dt>



L'operazione richiede che sia abilitato il controllo del dominio di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERRORE \_ DS \_ CANT \_ FIND DC FOR \_ \_ \_ SRC \_ DOMAIN**
</dt> <dd> <dl> <dt>

8537 (0x2159)
</dt> <dt>



L'operazione non è riuscita a individuare un controller di dominio per il dominio di origine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERRORE \_ DS \_ SRC \_ OBJ \_ NON GRUPPO \_ \_ O \_ UTENTE**
</dt> <dd> <dl> <dt>

8538 (0x215A)
</dt> <dt>



L'oggetto di origine deve essere un gruppo o un utente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERRORE \_ DS \_ SRC \_ SID \_ PRESENTE NELLA \_ \_ FORESTA**
</dt> <dd> <dl> <dt>

8539 (0x215B)
</dt> <dt>



Il SID dell'oggetto di origine esiste già nella foresta di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERRORE \_ DS \_ SRC \_ E CLASSE DI \_ OGGETTI DST NON \_ \_ \_ CORRISPONDENTI**
</dt> <dd> <dl> <dt>

8540 (0x215C)
</dt> <dt>



L'oggetto di origine e di destinazione deve essere dello stesso tipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERRORE \_ SAM \_ INIT \_ FAILURE**
</dt> <dd> <dl> <dt>

8541 (0x215D)
</dt> <dt>



Inizializzazione di Gestione account di sicurezza non riuscita a causa dell'errore seguente: %1. Stato errore: 0x%2. Fare clic su OK per arrestare il sistema e riavviare Cassaforte modalità. Controllare il registro eventi per informazioni dettagliate.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERRORE \_ DS \_ DRA SCHEMA INFO \_ \_ \_ SHIP**
</dt> <dd> <dl> <dt>

8542 (0x215E)
</dt> <dt>



Impossibile includere le informazioni sullo schema nella richiesta di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERRORE \_ DURANTE IL CONFLITTO DELLO SCHEMA \_ DS \_ \_ DRA**
</dt> <dd> <dl> <dt>

8543 (0x215F)
</dt> <dt>



Impossibile completare l'operazione di replica a causa di un'incompatibilità dello schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERRORE \_ DS \_ DRA EARLIER \_ SCHEMA \_ \_ CONFLICT**
</dt> <dd> <dl> <dt>

8544 (0x2160)
</dt> <dt>



Impossibile completare l'operazione di replica a causa di un'incompatibilità dello schema precedente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERRORE \_ DS \_ DRA \_ OBJ \_ NC NON \_ CORRISPONDENTE**
</dt> <dd> <dl> <dt>

8545 (0x2161)
</dt> <dt>



Impossibile applicare l'aggiornamento della replica perché l'origine o la destinazione non ha ancora ricevuto informazioni relative a una recente operazione di spostamento tra domini.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**ERRORE \_ DS \_ NC \_ HA ANCORA \_ \_ DSAS**
</dt> <dd> <dl> <dt>

8546 (0x2162)
</dt> <dt>



Impossibile eliminare il dominio richiesto perché esistono controller di dominio che ospitano ancora questo dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERRORE \_ DS \_ GC \_ OBBLIGATORIO**
</dt> <dd> <dl> <dt>

8547 (0x2163)
</dt> <dt>



L'operazione richiesta può essere eseguita solo in un server di catalogo globale.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERRORE \_ MEMBRO LOCALE DS SOLO \_ \_ \_ \_ \_ LOCALE**
</dt> <dd> <dl> <dt>

8548 (0x2164)
</dt> <dt>



Un gruppo locale può essere membro solo di altri gruppi locali nello stesso dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERRORE \_ DS \_ NO \_ FPO NEI GRUPPI \_ \_ \_ UNIVERSALI**
</dt> <dd> <dl> <dt>

8549 (0x2165)
</dt> <dt>



Le entità di sicurezza estere non possono essere membri di gruppi universali.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERRORE \_ DS \_ CANT \_ ADD TO \_ \_ GC**
</dt> <dd> <dl> <dt>

8550 (0x2166)
</dt> <dt>



L'attributo non può essere replicato nel catalogo globale per motivi di sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERRORE \_ DS \_ NO CHECKPOINT \_ CON \_ \_ PDC**
</dt> <dd> <dl> <dt>

8551 (0x2167)
</dt> <dt>



Impossibile eseguire il checkpoint con il PDC perché sono attualmente in corso troppe modifiche.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**ERRORE \_ CONTROLLO ORIGINE DS NON \_ \_ \_ \_ ABILITATO**
</dt> <dd> <dl> <dt>

8552 (0x2168)
</dt> <dt>



L'operazione richiede che il controllo del dominio di origine sia abilitato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERRORE \_ DS \_ CANT \_ CREATE IN \_ \_ NONDOMAIN \_ NC**
</dt> <dd> <dl> <dt>

8553 (0x2169)
</dt> <dt>



Gli oggetti entità di sicurezza possono essere creati solo all'interno di contesti di denominazione di dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERRORE \_ DS \_ NOME NON VALIDO PER IL NOME \_ \_ \_ SPN**
</dt> <dd> <dl> <dt>

8554 (0x216A)
</dt> <dt>



Non è stato possibile costruire un nome dell'entità servizio (SPN) perché il nome host specificato non è nel formato necessario.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**IL \_ FILTRO DS \_ DEGLI ERRORI USA GLI \_ \_ \_ ATTR CONTRUTTI**
</dt> <dd> <dl> <dt>

8555 (0x216B)
</dt> <dt>



È stato passato un filtro che usa attributi costruiti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERRORE \_ DS \_ UNICODEPWD \_ NON TRA \_ \_ VIRGOLETTE**
</dt> <dd> <dl> <dt>

8556 (0x216C)
</dt> <dt>



Il valore dell'attributo unicodePwd deve essere racchiuso tra virgolette doppie.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERRORE \_ DI SUPERAMENTO \_ DELLA QUOTA \_ DELL'ACCOUNT DEL \_ COMPUTER DS \_**
</dt> <dd> <dl> <dt>

8557 (0x216D)
</dt> <dt>



Non è stato possibile aggiungere il computer al dominio. È stato superato il numero massimo di account computer che è possibile creare in questo dominio. Per reimpostare o aumentare il limite, contattare l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**ERRORE \_ DS \_ DEVE ESSERE ESEGUITO NEL CONTROLLER DI DOMINIO \_ \_ \_ \_ DST \_**
</dt> <dd> <dl> <dt>

8558 (0x216E)
</dt> <dt>



Per motivi di sicurezza, l'operazione deve essere eseguita nel controller di dominio di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERRORE \_ DS \_ SRC \_ DC DEVE ESSERE \_ \_ \_ SP4 \_ O VERSIONE \_ SUCCESSIVA**
</dt> <dd> <dl> <dt>

8559 (0x216F)
</dt> <dt>



Per motivi di sicurezza, il controller di dominio di origine deve essere NT4SP4 o versione successiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERRORE \_ DS \_ CANT \_ TREE DELETE \_ \_ CRITICAL \_ OBJ**
</dt> <dd> <dl> <dt>

8560 (0x2170)
</dt> <dt>



Gli oggetti critici del sistema del servizio directory non possono essere eliminati durante le operazioni di eliminazione dell'albero. È possibile che l'eliminazione dell'albero sia stata eseguita parzialmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERRORE \_ DS \_ INIT \_ FAILURE \_ CONSOLE**
</dt> <dd> <dl> <dt>

8561 (0x2171)
</dt> <dt>



Impossibile avviare Servizi directory a causa dell'errore seguente: %1. Stato errore: 0x%2. Fare clic su OK per arrestare il sistema. È possibile usare la Console di ripristino di emergenza per diagnosticare più approfonditamente il problema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERRORE \_ DS \_ SAM \_ INIT FAILURE \_ \_ CONSOLE**
</dt> <dd> <dl> <dt>

8562 (0x2172)
</dt> <dt>



Inizializzazione di Gestione account di sicurezza non riuscita a causa dell'errore seguente: %1. Stato errore: 0x%2. Fare clic su OK per arrestare il sistema. È possibile usare la Console di ripristino di emergenza per diagnosticare più approfonditamente il problema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERRORE \_ VERSIONE FORESTA \_ DS TROPPO \_ \_ \_ ALTA**
</dt> <dd> <dl> <dt>

8563 (0x2173)
</dt> <dt>



La versione del sistema operativo non è compatibile con il livello di funzionalità corrente della foresta di Servizi di dominio Active Directory o con AD LDS di funzionalità del set di configurazione. È necessario eseguire l'aggiornamento a una nuova versione del sistema operativo prima che questo server possa diventare un controller di dominio active directory o aggiungere un'istanza di AD LDS in questa foresta di Active Directory o nel set di configurazione di AD LDS.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERRORE \_ VERSIONE DOMINIO \_ DS TROPPO \_ \_ \_ ALTA**
</dt> <dd> <dl> <dt>

8564 (0x2174)
</dt> <dt>



La versione del sistema operativo installata non è compatibile con il livello di funzionalità del dominio corrente. È necessario eseguire l'aggiornamento a una nuova versione del sistema operativo prima che questo server possa diventare un controller di dominio in questo dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERRORE \_ VERSIONE FORESTA \_ DS TROPPO \_ \_ \_ BASSA**
</dt> <dd> <dl> <dt>

8565 (0x2175)
</dt> <dt>



La versione del sistema operativo installata in questo server non supporta più il livello di funzionalità corrente della foresta di Servizi di dominio Active Directory o AD LDS di funzionalità del set di configurazione. È necessario aumentare il livello di funzionalità foresta servizi di dominio Active Directory o il livello di funzionalità del set di configurazione di AD LDS prima che questo server possa diventare un controller di dominio active directory o un'istanza di AD LDS in questa foresta o set di configurazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERRORE \_ VERSIONE DEL DOMINIO \_ \_ DS TROPPO \_ \_ BASSA**
</dt> <dd> <dl> <dt>

8566 (0x2176)
</dt> <dt>



La versione del sistema operativo installata in questo server non supporta più il livello di funzionalità del dominio corrente. È necessario aumentare il livello di funzionalità del dominio prima che questo server possa diventare un controller di dominio in questo dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**ERRORE \_ VERSIONE DS \_ INCOMPATIBILE \_**
</dt> <dd> <dl> <dt>

8567 (0x2177)
</dt> <dt>



La versione del sistema operativo installata in questo server non è compatibile con il livello di funzionalità del dominio o della foresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERRORE \_ VERSIONE \_ \_ DSA BASSA \_**
</dt> <dd> <dl> <dt>

8568 (0x2178)
</dt> <dt>



Il livello di funzionalità del dominio (o della foresta) non può essere elevato al valore richiesto, perché esistono uno o più controller di dominio nel dominio (o foresta) a un livello funzionale incompatibile inferiore.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERRORE \_ DS \_ NO BEHAVIOR VERSION IN \_ \_ \_ \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8569 (0x2179)
</dt> <dt>



Il livello di funzionalità della foresta non può essere elevato al valore richiesto perché uno o più domini sono ancora in modalità dominio misto. Tutti i domini nella foresta devono essere in modalità nativa per poter aumentare il livello di funzionalità della foresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ERRORE \_ DS \_ NON SUPPORTATO \_ \_ \_ ORDINAMENTO**
</dt> <dd> <dl> <dt>

8570 (0x217A)
</dt> <dt>



L'ordinamento richiesto non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**ERRORE \_ DS \_ NAME NOT \_ \_ UNIQUE**
</dt> <dd> <dl> <dt>

8571 (0x217B)
</dt> <dt>



Il nome richiesto esiste già come identificatore univoco.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERRORE \_ DURANTE LA CREAZIONE DELL'ACCOUNT DEL COMPUTER DS \_ \_ \_ \_ PRENT4**
</dt> <dd> <dl> <dt>

8572 (0x217C)
</dt> <dt>



L'account del computer è stato creato prima di NT4. L'account deve essere ricreato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERRORE \_ DS \_ FUORI \_ \_ DALL'ARCHIVIO \_ VERSIONI**
</dt> <dd> <dl> <dt>

8573 (0x217D)
</dt> <dt>



Il database non è più disponibile nell'archivio versioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**ERRORE \_ DURANTE L'USO \_ DI CONTROLLI INCOMPATIBILI \_ DS \_**
</dt> <dd> <dl> <dt>

8574 (0x217E)
</dt> <dt>



Impossibile continuare l'operazione perché sono stati usati più controlli in conflitto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERRORE \_ DS \_ NO REF \_ \_ DOMAIN**
</dt> <dd> <dl> <dt>

8575 (0x217F)
</dt> <dt>



Impossibile trovare un dominio di riferimento del descrittore di sicurezza valido per questa partizione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**ERRORE \_ ID COLLEGAMENTO RISERVATO DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8576 (0x2180)
</dt> <dt>



Aggiornamento dello schema non riuscito: l'identificatore del collegamento è riservato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**ERRORE \_ ID COLLEGAMENTO DS NON \_ \_ \_ \_ DISPONIBILE**
</dt> <dd> <dl> <dt>

8577 (0x2181)
</dt> <dt>



Aggiornamento dello schema non riuscito: non sono disponibili identificatori di collegamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERRORE \_ DS \_ AG \_ CANT HAVE UNIVERSAL \_ \_ \_ MEMBER**
</dt> <dd> <dl> <dt>

8578 (0x2182)
</dt> <dt>



Un gruppo di account non può avere un gruppo universale come membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERRORE \_ DS \_ MODIFYDN \_ NON CONSENTITO DAL TIPO DI \_ \_ \_ ISTANZA**
</dt> <dd> <dl> <dt>

8579 (0x2183)
</dt> <dt>



Non sono consentite operazioni di ridenominazione o spostamento in testine del contesto dei nomi o oggetti di sola lettura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERRORE \_ DS \_ NO OBJECT MOVE IN SCHEMA \_ \_ \_ \_ \_ NC**
</dt> <dd> <dl> <dt>

8580 (0x2184)
</dt> <dt>



Le operazioni di spostamento su oggetti nel contesto dei nomi dello schema non sono consentite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERRORE \_ DS \_ MODIFYDN \_ NON CONSENTITO DAL \_ \_ FLAG**
</dt> <dd> <dl> <dt>

8581 (0x2185)
</dt> <dt>



Nell'oggetto è stato impostato un flag di sistema che non consente lo spostamento o la ridenominazione dell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERRORE \_ DS \_ MODIFYDN \_ WRONG \_ GRANDPARENT**
</dt> <dd> <dl> <dt>

8582 (0x2186)
</dt> <dt>



A questo oggetto non è consentito modificare il relativo contenitore padre. Gli spostamenti non sono consentiti su questo oggetto, ma sono limitati ai contenitori di pari livello.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERRORE \_ DS \_ NAME ERROR TRUST \_ \_ \_ REFERRAL**
</dt> <dd> <dl> <dt>

8583 (0x2187)
</dt> <dt>



Non è possibile risolvere completamente, viene generata una segnalazione a un'altra foresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERRORE \_ NON SUPPORTATO NEL SERVER \_ \_ \_ \_ STANDARD**
</dt> <dd> <dl> <dt>

8584 (0x2188)
</dt> <dt>



L'azione richiesta non è supportata nel server standard.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERRORE \_ DS \_ CANT \_ ACCESS REMOTE PART OF \_ \_ \_ \_ AD**
</dt> <dd> <dl> <dt>

8585 (0x2189)
</dt> <dt>



Impossibile accedere a una partizione del servizio directory che si trova in un server remoto. Assicurarsi che sia in esecuzione almeno un server per la partizione in questione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERRORE \_ DS \_ CR \_ IMPOSSIBILE \_ \_ CONVALIDARE \_ V2**
</dt> <dd> <dl> <dt>

8586 (0x218A)
</dt> <dt>



La directory non può convalidare il nome del contesto dei nomi (o della partizione) proposto perché non contiene una replica né può contattare una replica del contesto dei nomi al di sopra del contesto dei nomi proposto. Assicurarsi che il contesto dei nomi padre sia registrato correttamente in DNS e che almeno una replica di questo contesto dei nomi sia raggiungibile dal master di denominazione di dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**LIMITE \_ DI THREAD DS DI ERRORE \_ \_ \_ SUPERATO**
</dt> <dd> <dl> <dt>

8587 (0x218B)
</dt> <dt>



È stato superato il limite di thread per questa richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERRORE \_ DS \_ NON PIÙ \_ VICINO**
</dt> <dd> <dl> <dt>

8588 (0x218C)
</dt> <dt>



Il server di catalogo globale non si trova nel sito più vicino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERRORE \_ DS \_ CANT \_ DERIVE \_ SPN WITHOUT SERVER \_ \_ \_ REF**
</dt> <dd> <dl> <dt>

8589 (0x218D)
</dt> <dt>



DS non può derivare un nome dell'entità servizio (SPN) con cui autenticare reciprocamente il server di destinazione perché l'oggetto server corrispondente nel database DS locale non ha alcun attributo serverReference.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERRORE \_ MODALITÀ UTENTE SINGOLO DS NON \_ \_ \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

8590 (0x218E)
</dt> <dt>



Il servizio directory non è riuscito a entrare in modalità utente singolo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**ERRORE \_ DI SINTASSI \_ NTDSCRIPT DS \_ \_**
</dt> <dd> <dl> <dt>

8591 (0x218F)
</dt> <dt>



Il servizio directory non è in grado di analizzare lo script a causa di un errore di sintassi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**ERRORE \_ DS \_ NTDSCRIPT \_ PROCESS \_ ERROR**
</dt> <dd> <dl> <dt>

8592 (0x2190)
</dt> <dt>



Il servizio directory non è in grado di elaborare lo script a causa di un errore.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ERRORE \_ DS \_ DIVERSI \_ REPL \_ EPOCHS**
</dt> <dd> <dl> <dt>

8593 (0x2191)
</dt> <dt>



Il servizio directory non è in grado di eseguire l'operazione richiesta perché i server interessati sono di epoche di replica diverse, in genere correlate a una ridenominazione di dominio in corso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**ERRORE \_ DELLE ESTENSIONI \_ DRS \_ DS \_ MODIFICATE**
</dt> <dd> <dl> <dt>

8594 (0x2192)
</dt> <dt>



L'associazione al servizio directory deve essere rinegoziata a causa di una modifica nelle informazioni sulle estensioni del server.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**MODIFICA \_ DEL SET DI REPLICHE DS NON \_ \_ \_ \_ \_ CONSENTITA IN \_ \_ \_ CR DISABILITATO**
</dt> <dd> <dl> <dt>

8595 (0x2193)
</dt> <dt>



Operazione non consentita in un riferimento incrociato disabilitato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERRORE \_ DS \_ NO \_ MSDS \_ INTID**
</dt> <dd> <dl> <dt>

8596 (0x2194)
</dt> <dt>



Aggiornamento dello schema non riuscito: non sono disponibili valori per msDS-IntId.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERRORE \_ DS \_ DUP \_ MSDS \_ INTID**
</dt> <dd> <dl> <dt>

8597 (0x2195)
</dt> <dt>



Aggiornamento dello schema non riuscito: msDS-INtId duplicato. Ripetere l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**ERRORE \_ DS \_ PRESENTE IN \_ \_ RDNATTID**
</dt> <dd> <dl> <dt>

8598 (0x2196)
</dt> <dt>



Eliminazione dello schema non riuscita: l'attributo viene usato in rDNAttID.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERRORE \_ DI AUTORIZZAZIONE DS NON \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

8599 (0x2197)
</dt> <dt>



Il servizio directory non è riuscito ad autorizzare la richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**SCRIPT \_ DI ERRORE DS NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

8600 (0x2198)
</dt> <dt>



Il servizio directory non è in grado di elaborare lo script perché non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**ERRORE \_ DS \_ REMOTE \_ CROSSREF OP NON \_ \_ RIUSCITO**
</dt> <dd> <dl> <dt>

8601 (0x2199)
</dt> <dt>



L'operazione di creazione remota di riferimenti incrociati non è riuscita nell'FSMO domain naming master. L'errore dell'operazione è nei dati estesi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERRORE \_ DS \_ CROSS REF \_ \_ OCCUPATO**
</dt> <dd> <dl> <dt>

8602 (0x219A)
</dt> <dt>



Un riferimento incrociato è in uso in locale con lo stesso nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERRORE \_ DS \_ CANT \_ DERIVE \_ SPN FOR DELETED \_ \_ \_ DOMAIN**
</dt> <dd> <dl> <dt>

8603 (0x219B)
</dt> <dt>



DS non può derivare un nome dell'entità servizio (SPN) con cui autenticare reciprocamente il server di destinazione perché il dominio del server è stato eliminato dalla foresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERRORE \_ DS \_ CANT \_ DEMOTE \_ WITH \_ WRITEABLE \_ NC**
</dt> <dd> <dl> <dt>

8604 (0x219C)
</dt> <dt>



I controller di rete scrivibili impediscono l'abbassamento di livello di questo controller di dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**ERRORE \_ RILEVATO \_ ID DUPLICATO \_ DS \_**
</dt> <dd> <dl> <dt>

8605 (0x219D)
</dt> <dt>



L'oggetto richiesto ha un identificatore non univoco e non può essere recuperato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERRORE \_ DS \_ INSUFFICIENT \_ ATTR PER CREARE \_ \_ \_ L'OGGETTO**
</dt> <dd> <dl> <dt>

8606 (0x219E)
</dt> <dt>



Sono stati specificati attributi insufficienti per creare un oggetto. Questo oggetto potrebbe non esistere perché potrebbe essere stato eliminato e già sottoposto a Garbage Collection.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**ERRORE \_ DI CONVERSIONE GRUPPO DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8607 (0x219F)
</dt> <dt>



Impossibile convertire il gruppo a causa di restrizioni di attributo per il tipo di gruppo richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERRORE \_ DS \_ CANT \_ MOVE APP \_ \_ BASIC \_ GROUP**
</dt> <dd> <dl> <dt>

8608 (0x21A0)
</dt> <dt>



Lo spostamento tra domini di gruppi di applicazioni di base non vuoti non è consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERRORE \_ DS \_ CANT \_ MOVE APP \_ \_ QUERY \_ GROUP**
</dt> <dd> <dl> <dt>

8609 (0x21A1)
</dt> <dt>



Lo spostamento tra domini di gruppi di applicazioni non vuoti basati su query non è consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**ERRORE \_ DEL RUOLO DS NON \_ \_ \_ VERIFICATO**
</dt> <dd> <dl> <dt>

8610 (0x21A2)
</dt> <dt>



Impossibile verificare la proprietà del ruolo FSMO perché la relativa partizione di directory non è stata replicata correttamente con almeno un partner di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**ERRORE \_ IL CONTENITORE \_ WKO \_ DS NON PUÒ ESSERE \_ \_ \_ SPECIALE**
</dt> <dd> <dl> <dt>

8611 (0x21A3)
</dt> <dt>



Il contenitore di destinazione per un reindirizzamento di un contenitore di oggetti noto non può essere già un contenitore speciale.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERRORE \_ DURANTE LA \_ RIDENOMINAZIONE DEL DOMINIO DS \_ \_ IN \_ CORSO**
</dt> <dd> <dl> <dt>

8612 (0x21A4)
</dt> <dt>



Il servizio directory non può eseguire l'operazione richiesta perché è in corso un'operazione di ridenominazione del dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERRORE \_ DS \_ ESISTENTE AD \_ CHILD \_ \_ NC**
</dt> <dd> <dl> <dt>

8613 (0x21A5)
</dt> <dt>



Il servizio directory ha rilevato una partizione figlio sotto il nome di partizione richiesto. La gerarchia di partizione deve essere creata in un metodo dall'alto verso il basso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**È STATO \_ SUPERATO L'ERRORE DS \_ REPL \_ LIFETIME \_ EXCEEDED**
</dt> <dd> <dl> <dt>

8614 (0x21A6)
</dt> <dt>



Il servizio directory non può eseguire la replica con questo server perché l'ora dell'ultima replica con questo server ha superato la durata dell'oggetto contrassegnato per la rimozione definitiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERRORE \_ DS \_ NON CONSENTITO NEL \_ CONTENITORE DI \_ \_ SISTEMA**
</dt> <dd> <dl> <dt>

8615 (0x21A7)
</dt> <dt>



L'operazione richiesta non è consentita su un oggetto nel contenitore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERRORE \_ DS \_ LDAP SEND QUEUE \_ \_ \_ FULL**
</dt> <dd> <dl> <dt>

8616 (0x21A8)
</dt> <dt>



La coda di invio di rete dei server LDAP è stata riempita perché il client non elabora i risultati delle richieste in modo sufficientemente rapido. Non verranno elaborate altre richieste fino al completamento del client. Se il client non si raggiunge, verrà disconnesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**ERRORE \_ DS \_ DRA OUT SCHEDULE \_ \_ \_ WINDOW**
</dt> <dd> <dl> <dt>

8617 (0x21A9)
</dt> <dt>



La replica pianificata non è stata eseguita perché il sistema era troppo occupato per eseguire la richiesta all'interno dell'intervallo di pianificazione. La coda di replica è sovraccarica. Provare a ridurre il numero di partner o a ridurre la frequenza di replica pianificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**ERRORE \_ CRITERI DS \_ NON \_ \_ NOTI**
</dt> <dd> <dl> <dt>

8618 (0x21AA)
</dt> <dt>



Al momento non è possibile determinare se i criteri di replica del ramo sono disponibili nel controller di dominio dell'hub. Riprovare in un secondo momento per tenere conto delle latenze di replica.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERRORE \_ NESSUN OGGETTO IMPOSTAZIONI \_ \_ \_ SITO**
</dt> <dd> <dl> <dt>

8619 (0x21AB)
</dt> <dt>



L'oggetto impostazioni del sito per il sito specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERRORE \_ NESSUN \_ SEGRETO**
</dt> <dd> <dl> <dt>

8620 (0x21AC)
</dt> <dt>



L'archivio account locale non contiene materiale segreto per l'account specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERRORE \_ NESSUN CONTROLLER DI DOMINIO \_ \_ \_ SCRIVIBILE TROVATO**
</dt> <dd> <dl> <dt>

8621 (0x21AD)
</dt> <dt>



Impossibile trovare un controller di dominio scrivibile nel dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERRORE \_ DS \_ NO SERVER \_ \_ OBJECT**
</dt> <dd> <dl> <dt>

8622 (0x21AE)
</dt> <dt>



L'oggetto server per il controller di dominio non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERRORE \_ DS \_ NO \_ NTDSA \_ OBJECT**
</dt> <dd> <dl> <dt>

8623 (0x21AF)
</dt> <dt>



L'oggetto Impostazioni NTDS per il controller di dominio non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERRORE \_ DS \_ NON \_ ASQ \_ SEARCH**
</dt> <dd> <dl> <dt>

8624 (0x21B0)
</dt> <dt>



L'operazione di ricerca richiesta non è supportata per le ricerche ASQ.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**ERRORE \_ DS \_ AUDIT \_ FAILURE**
</dt> <dd> <dl> <dt>

8625 (0x21B1)
</dt> <dt>



Non è stato possibile generare un evento di controllo obbligatorio per l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERRORE \_ DS \_ \_ SOTTOALBERO \_ DEL FLAG DI RICERCA NON \_ VALIDO**
</dt> <dd> <dl> <dt>

8626 (0x21B2)
</dt> <dt>



I flag di ricerca per l'attributo non sono validi. Il bit di indice del sottoalbero è valido solo per attributi a valore singolo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERRORE \_ TUPLA FLAG DI RICERCA NON \_ \_ \_ \_ VALIDA DS**
</dt> <dd> <dl> <dt>

8627 (0x21B3)
</dt> <dt>



I flag di ricerca per l'attributo non sono validi. Il bit di indice della tupla è valido solo per gli attributi delle stringhe Unicode.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERRORE \_ DELLA TABELLA DELLA \_ \_ GERARCHIA DS \_ TROPPO \_ PROFONDA**
</dt> <dd> <dl> <dt>

8628 (0x21B4)
</dt> <dt>



Le rubriche sono annidate troppo in profondità. Impossibile compilare la tabella della gerarchia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERRORE \_ DS \_ DRA DANNEGGIATO \_ \_ VETTORE UTD \_**
</dt> <dd> <dl> <dt>

8629 (0x21B5)
</dt> <dt>



Il vettore di ness aggiornato specificato è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERRORE \_ DS \_ DRA SECRETS \_ \_ DENIED**
</dt> <dd> <dl> <dt>

8630 (0x21B6)
</dt> <dt>



La richiesta di replica dei segreti viene negata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**ERRORE \_ DS \_ RESERVED \_ MAPI \_ ID**
</dt> <dd> <dl> <dt>

8631 (0x21B7)
</dt> <dt>



Aggiornamento dello schema non riuscito: l'identificatore MAPI è riservato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERRORE \_ DS \_ MAPI ID NOT AVAILABLE (ID MAPI DS \_ \_ NON \_ DISPONIBILE)**
</dt> <dd> <dl> <dt>

8632 (0x21B8)
</dt> <dt>



Aggiornamento dello schema non riuscito: non sono disponibili identificatori MAPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERRORE \_ DS \_ DRA MISSING \_ \_ KRBTGT \_ SECRET**
</dt> <dd> <dl> <dt>

8633 (0x21B9)
</dt> <dt>



L'operazione di replica non è riuscita perché mancano gli attributi obbligatori dell'oggetto krbtgt locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERRORE \_ DURANTE L'ESISTENZA \_ DEL NOME DI DOMINIO \_ \_ DS NELLA \_ \_ FORESTA**
</dt> <dd> <dl> <dt>

8634 (0x21BA)
</dt> <dt>



Il nome di dominio del dominio trusted esiste già nella foresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERRORE \_ DS \_ FLAT NAME EXISTS IN \_ \_ \_ \_ FOREST**
</dt> <dd> <dl> <dt>

8635 (0x21BB)
</dt> <dt>



Il nome flat del dominio trusted esiste già nella foresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**ERRORE NOME \_ \_ ENTITÀ UTENTE NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

8636 (0x21BC)
</dt> <dt>



Il nome dell'entità utente (UPN) non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERRORE \_ DS \_ OID \_ IL GRUPPO MAPPATO NON PUÒ \_ \_ AVERE \_ \_ MEMBRI**
</dt> <dd> <dl> <dt>

8637 (0x21BD)
</dt> <dt>



I gruppi di cui è stato eseguito il mapping OID non possono avere membri.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERRORE \_ DS \_ OID \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

8638 (0x21BE)
</dt> <dt>



Impossibile trovare l'OID specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERRORE \_ DS \_ DRA \_ RECYCLED \_ TARGET**
</dt> <dd> <dl> <dt>

8639 (0x21BF)
</dt> <dt>



L'operazione di replica non è riuscita perché l'oggetto di destinazione a cui fa riferimento un valore di collegamento è stato riciclato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERRORE \_ DS \_ NON CONSENTITO REINDIRIZZAMENTO \_ NC \_**
</dt> <dd> <dl> <dt>

8640 (0x21C0)
</dt> <dt>



L'operazione di reindirizzamento non è riuscita perché l'oggetto di destinazione si trova in un controller di rete diverso dal controller di dominio del controller di dominio corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERRORE \_ DS \_ HIGH \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8641 (0x21C1)
</dt> <dt>



Il livello di funzionalità del set AD LDS non può essere abbassato al valore richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERRORE \_ VERSIONE \_ \_ DSA \_ ELEVATA**
</dt> <dd> <dl> <dt>

8642 (0x21C2)
</dt> <dt>



Il livello di funzionalità del dominio (o della foresta) non può essere abbassato al valore richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERRORE \_ DS \_ LOW \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8643 (0x21C3)
</dt> <dt>



Il livello di funzionalità del set di AD LDS non può essere elevato al valore richiesto, perché esistono una o più istanze di ADLDS a un livello funzionale incompatibile inferiore.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**SID \_ DOMINIO ERRORE UGUALE ALLA WORKSTATION \_ \_ \_ \_ \_ LOCALE**
</dt> <dd> <dl> <dt>

8644 (0x21C4)
</dt> <dt>



Non è possibile completare l'aggiunta al dominio perché il SID del dominio a cui si è tentato di aggiungersi è identico al SID del computer. Questo è un sintomo di un'installazione del sistema operativo clonata in modo non corretto. È consigliabile eseguire sysprep in questo computer per generare un nuovo SID del computer. Per altre informazioni, vedere <https://go.microsoft.com/fwlink/p/?linkid=168895>.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERRORE \_ DI \_ ANNULLAMENTO DELL'ELIMINAZIONE \_ DELLA CONVALIDA SAM NON \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

8645 (0x21C5)
</dt> <dt>



L'operazione di annullamento dell'eliminazione non è riuscita perché il nome dell'account Sam o il nome account Sam aggiuntivo dell'oggetto di cui non è stata annullata l'eliminazione è in conflitto con un oggetto live esistente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERRORE TIPO \_ DI \_ ACCOUNT NON \_ CORRETTO**
</dt> <dd> <dl> <dt>

8646 (0x21C6)
</dt> <dt>



Il sistema non è autorevole per l'account specificato e pertanto non può completare l'operazione. Ripetere l'operazione usando il provider associato a questo account. Se si tratta di un provider online, usare il sito online del provider.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Winerror</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore di sistema](system-error-codes.md)
</dt> </dl>

 

 




