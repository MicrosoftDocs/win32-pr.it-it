---
description: Descrive i codici di errore 1700-3999 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: 7e57c087-53e4-443d-9227-21d9eb3cc71f
title: Codici di errore di sistema (1700-3999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 23b90db71a6e2e84b28f4aafc94475e9e82e3e7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877317"
---
# <a name="system-error-codes-1700-3999"></a>Codici di errore di sistema (1700-3999)

> [!NOTE]
> Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema. Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .

Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) per gli errori da 1700 a 3999. Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .

<dl> <dt>

<span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**\_ \_ \_ Binding stringa non valido \_ RPC**
</dt> <dd> <dl> <dt>

1700 (0x6A4)
</dt> <dt>



Binding stringa non valido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**\_ \_ \_ tipo \_ di \_ binding RPC S errato**
</dt> <dd> <dl> <dt>

1701 (0x6A5)
</dt> <dt>



Il tipo dell'handle di binding non è corretto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**\_binding RPC S \_ non valido \_**
</dt> <dd> <dl> <dt>

1702 (0x6A6)
</dt> <dt>



Handle di binding non valido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**RPC \_ S \_ PROTSEQ \_ non \_ supportato**
</dt> <dd> <dl> <dt>

1703 (0x6A7)
</dt> <dt>



La sequenza del protocollo RPC non è supportata.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**\_ \_ \_ PROTSEQ RPC non valido \_**
</dt> <dd> <dl> <dt>

1704 (0x6A8)
</dt> <dt>



Sequenza del protocollo RPC non valida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**\_ \_ \_ UUID stringa non valido \_ RPC**
</dt> <dd> <dl> <dt>

1705 (0x6A9)
</dt> <dt>



L'identificatore univoco universale (UUID) della stringa non è valido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**\_ \_ \_ formato endpoint non valido \_ RPC**
</dt> <dd> <dl> <dt>

1706 (0x6AA)
</dt> <dt>



Il formato dell'endpoint non è valido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**\_ \_ \_ \_ indirizzi NET addr non validi in RPC**
</dt> <dd> <dl> <dt>

1707 (0x6AB)
</dt> <dt>



L'indirizzo di rete non è valido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**\_non è \_ stato \_ trovato alcun endpoint \_ RPC**
</dt> <dd> <dl> <dt>

1708 (0x6AC)
</dt> <dt>



Non è stato trovato alcun endpoint.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**TIMEOUT di RPC \_ \_ non valido \_**
</dt> <dd> <dl> <dt>

1709 (0x6AD)
</dt> <dt>



Il valore di timeout non è valido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**l' \_ oggetto RPC non è stato \_ \_ \_ trovato**
</dt> <dd> <dl> <dt>

1710 (0x6AE)
</dt> <dt>



L'identificatore univoco universale (UUID) dell'oggetto non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**la RPC \_ è \_ già \_ registrata**
</dt> <dd> <dl> <dt>

1711 (0x6AF)
</dt> <dt>



L'identificatore univoco universale (UUID) dell'oggetto è già stato registrato.


</dt> </dl> </dd> <dt>

<span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**il \_ tipo RPC è \_ \_ già \_ registrato**
</dt> <dd> <dl> <dt>

1712 (0x6B0)
</dt> <dt>



L'identificatore univoco universale (UUID) del tipo è già stato registrato.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC \_ \_ già in \_ ascolto**
</dt> <dd> <dl> <dt>

1713 (0x6B1)
</dt> <dt>



Il server RPC è già in ascolto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**\_PROTSEQS RPC \_ non \_ \_ registrato**
</dt> <dd> <dl> <dt>

1714 (0x6B2)
</dt> <dt>



Nessuna sequenza di protocollo registrata.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC \_ \_ non in \_ ascolto**
</dt> <dd> <dl> <dt>

1715 (0x6B3)
</dt> <dt>



Il server RPC non è in ascolto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**tipo di gestione \_ \_ sconosciuto RPC \_ \_**
</dt> <dd> <dl> <dt>

1716 (0x6B4)
</dt> <dt>



Il tipo di gestione è sconosciuto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC \_ \_ sconosciuto \_ se**
</dt> <dd> <dl> <dt>

1717 (0x6B5)
</dt> <dt>



L'interfaccia è sconosciuta.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**\_ \_ nessun binding RPC \_ S**
</dt> <dd> <dl> <dt>

1718 (0x6B6)
</dt> <dt>



Nessuna associazione.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**\_ \_ n \_ PROTSEQS di RPC**
</dt> <dd> <dl> <dt>

1719 (0x6B7)
</dt> <dt>



Nessuna sequenza di protocolli.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**\_ \_ Impossibile creare l' \_ \_ endpoint di RPC S**
</dt> <dd> <dl> <dt>

1720 (0x6B8)
</dt> <dt>



Impossibile creare l'endpoint.


</dt> </dl> </dd> <dt>

<span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**\_ \_ risorse di RPC esaurite \_ \_**
</dt> <dd> <dl> <dt>

1721 (0x6B9)
</dt> <dt>



Sono disponibili risorse insufficienti per completare questa operazione.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**\_server RPC \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

1722 (0x6BA)
</dt> <dt>



Server RPC non disponibile.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**\_server RPC \_ \_ troppo \_ occupato**
</dt> <dd> <dl> <dt>

1723 (0x6BB)
</dt> <dt>



Il server RPC è troppo occupato per completare questa operazione.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**\_Opzioni di \_ rete non valide per \_ RPC \_**
</dt> <dd> <dl> <dt>

1724 (0x6BC)
</dt> <dt>



Le opzioni di rete non sono valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC \_ \_ Nessuna \_ chiamata \_ attiva**
</dt> <dd> <dl> <dt>

1725 (0x6BD)
</dt> <dt>



Non sono presenti chiamate a procedure remote attive in questo thread.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**\_chiamata RPC \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

1726 (0x6BE)
</dt> <dt>



La chiamata di procedura remota non è riuscita.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**\_chiamata RPC \_ \_ non riuscita \_ dne**
</dt> <dd> <dl> <dt>

1727 (0x6BF)
</dt> <dt>



La chiamata di procedura remota non è riuscita e non è stata eseguita.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**\_errore del \_ protocollo RPC S \_**
</dt> <dd> <dl> <dt>

1728 (0x6C0)
</dt> <dt>



Si è verificato un errore del protocollo RPC (Remote Procedure Call).


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**\_ \_ accesso proxy RPC \_ \_ negato**
</dt> <dd> <dl> <dt>

1729 (0x6C1)
</dt> <dt>



L'accesso al proxy HTTP è stato negato.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**\_ \_ \_ SYN trans non supportato \_**
</dt> <dd> <dl> <dt>

1730 (0x6C2)
</dt> <dt>



La sintassi di trasferimento non è supportata dal server RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**\_tipo non \_ supportato di RPC \_**
</dt> <dd> <dl> <dt>

1732 (0x6C4)
</dt> <dt>



Il tipo di identificatore univoco universale (UUID) non è supportato.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**il \_ \_ tag RPC non è valido \_**
</dt> <dd> <dl> <dt>

1733 (0x6C5)
</dt> <dt>



Il tag non è valido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**\_binding RPC \_ non valido \_**
</dt> <dd> <dl> <dt>

1734 (0x6C6)
</dt> <dt>



I limiti della matrice non sono validi.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**\_ \_ nessun nome di \_ voce \_ della RPC**
</dt> <dd> <dl> <dt>

1735 (0x6C7)
</dt> <dt>



Il binding non contiene un nome di voce.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**la \_ sintassi del nome della RPC \_ non è valida \_ \_**
</dt> <dd> <dl> <dt>

1736 (0x6C8)
</dt> <dt>



La sintassi del nome non è valida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**la \_ sintassi del nome non è \_ supportata in \_ RPC \_**
</dt> <dd> <dl> <dt>

1737 (0x6C9)
</dt> <dt>



La sintassi del nome non è supportata.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**\_UUID S \_ \_ nessun \_ Indirizzo**
</dt> <dd> <dl> <dt>

1739 (0x6CB)
</dt> <dt>



Non è disponibile alcun indirizzo di rete da usare per costruire un identificatore univoco universale (UUID).


</dt> </dl> </dd> <dt>

<span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**\_ \_ endpoint DUPLICAto \_ RPC**
</dt> <dd> <dl> <dt>

1740 (0x6CC)
</dt> <dt>



L'endpoint è un duplicato.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**\_tipo di \_ \_ autenticazione sconosciuto \_ RPC**
</dt> <dd> <dl> <dt>

1741 (0x6CD)
</dt> <dt>



Il tipo di autenticazione è sconosciuto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**il \_ \_ numero massimo di chiamate RPC è \_ \_ troppo \_ piccolo**
</dt> <dd> <dl> <dt>

1742 (0x6CE)
</dt> <dt>



Il numero massimo di chiamate è troppo piccolo.


</dt> </dl> </dd> <dt>

<span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**\_stringa RPC \_ \_ troppo \_ lungo**
</dt> <dd> <dl> <dt>

1743 (0x6CF)
</dt> <dt>



Stringa troppo lunga.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**RPC \_ S \_ PROTSEQ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

1744 (0x6D0)
</dt> <dt>



La sequenza del protocollo RPC non è stata trovata.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**PROCNUM RPC non \_ \_ compreso nell' \_ \_ \_ intervallo**
</dt> <dd> <dl> <dt>

1745 (0x6D1)
</dt> <dt>



Il numero di procedura non è compreso nell'intervallo.


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**\_binding RPC \_ \_ \_ non privo di \_ autenticazione**
</dt> <dd> <dl> <dt>

1746 (0x6D2)
</dt> <dt>



Il binding non contiene informazioni di autenticazione.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**\_ \_ \_ servizio AuthN sconosciuto di \_ RPC**
</dt> <dd> <dl> <dt>

1747 (0x6D3)
</dt> <dt>



Il servizio di autenticazione è sconosciuto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**\_ \_ \_ livello auth sconosciuto \_ di RPC**
</dt> <dd> <dl> <dt>

1748 (0x6D4)
</dt> <dt>



Il livello di autenticazione è sconosciuto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**\_ \_ \_ identità autenticazione non valida \_ RPC**
</dt> <dd> <dl> <dt>

1749 (0x6D5)
</dt> <dt>



Il contesto di sicurezza non è valido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**\_ \_ \_ servizio AUTHZ sconosciuto \_ RPC**
</dt> <dd> <dl> <dt>

1750 (0x6D6)
</dt> <dt>



Il servizio di autorizzazione è sconosciuto.


</dt> </dl> </dd> <dt>

<span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**\_ \_ voce non valida per EPT \_**
</dt> <dd> <dl> <dt>

1751 (0x6D7)
</dt> <dt>



La voce non è valida.


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**\_ \_ \_ operazioni eseguibili di EPT S \_**
</dt> <dd> <dl> <dt>

1752 (0x6D8)
</dt> <dt>



L'endpoint server non è in grado di eseguire l'operazione.


</dt> </dl> </dd> <dt>

<span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT \_ S \_ non \_ registrato**
</dt> <dd> <dl> <dt>

1753 (0x6D9)
</dt> <dt>



Nessun endpoint disponibile nel mapper degli endpoint.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**\_nessun elemento \_ RPC \_ da \_ esportare**
</dt> <dd> <dl> <dt>

1754 (0x6DA)
</dt> <dt>



Non sono state esportate interfacce.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**\_nome non \_ completo \_ RPC**
</dt> <dd> <dl> <dt>

1755 (0x6DB)
</dt> <dt>



Il nome della voce è incompleto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC \_ S \_ \_ opzione vers non valida \_**
</dt> <dd> <dl> <dt>

1756 (0x6DC)
</dt> <dt>



L'opzione version non è valida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**\_ \_ nessun \_ altro \_ membro della RPC**
</dt> <dd> <dl> <dt>

1757 (0x6DD)
</dt> <dt>



Non sono disponibili altri membri.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC \_ \_ non \_ tutti i \_ obj non \_ esportati**
</dt> <dd> <dl> <dt>

1758 (0x6DE)
</dt> <dt>



Non è necessario annullarne l'esportazione.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**\_interfaccia RPC \_ \_ non \_ trovata**
</dt> <dd> <dl> <dt>

1759 (0x6DF)
</dt> <dt>



L'interfaccia non è stata trovata.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**la \_ \_ voce RPC \_ \_ esiste già**
</dt> <dd> <dl> <dt>

1760 (0x6E0)
</dt> <dt>



La voce esiste già.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**la \_ \_ voce RPC \_ non è \_ stata trovata**
</dt> <dd> <dl> <dt>

1761 (0x6E1)
</dt> <dt>



La voce non è stata trovata.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**\_ \_ servizio nome RPC \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

1762 (0x6E2)
</dt> <dt>



Il servizio nome non è disponibile.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**\_ \_ \_ ID NAF non valido \_ in RPC**
</dt> <dd> <dl> <dt>

1763 (0x6E3)
</dt> <dt>



La famiglia di indirizzi di rete non è valida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC \_ \_ non può \_ supportare**
</dt> <dd> <dl> <dt>

1764 (0x6E4)
</dt> <dt>



L'operazione richiesta non è supportata.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**\_non è \_ \_ disponibile alcun \_ contesto per la RPC**
</dt> <dd> <dl> <dt>

1765 (0x6E5)
</dt> <dt>



Non è disponibile alcun contesto di sicurezza per consentire la rappresentazione.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**\_ \_ errore interno di \_ RPC**
</dt> <dd> <dl> <dt>

1766 (0x6E6)
</dt> <dt>



Si è verificato un errore interno in una chiamata di procedura remota (RPC).


</dt> </dl> </dd> <dt>

<span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**\_ \_ divisione zero di \_ RPC**
</dt> <dd> <dl> <dt>

1767 (0x6E7)
</dt> <dt>



Il server RPC ha tentato una divisione di interi per zero.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**\_errore di \_ indirizzo \_ RPC**
</dt> <dd> <dl> <dt>

1768 (0x6E8)
</dt> <dt>



Si è verificato un errore di indirizzamento nel server RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**\_ \_ \_ zero div FP \_ di RPC**
</dt> <dd> <dl> <dt>

1769 (0x6E9)
</dt> <dt>



Un'operazione a virgola mobile nel server RPC ha causato una divisione per zero.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**\_ \_ underflow FP di \_ RPC**
</dt> <dd> <dl> <dt>

1770 (0x6EA)
</dt> <dt>



Si è verificato un underflow a virgola mobile nel server RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**\_ \_ overflow FP di \_ RPC**
</dt> <dd> <dl> <dt>

1771 (0x6EB)
</dt> <dt>



Si è verificato un overflow a virgola mobile nel server RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC \_ X \_ \_ altre \_ voci**
</dt> <dd> <dl> <dt>

1772 (0x6EC)
</dt> <dt>



L'elenco dei server RPC disponibili per l'associazione di handle automatici è stato esaurito.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**\_errore di \_ trasporto char X SS RPC \_ \_ \_ \_ non riuscito**
</dt> <dd> <dl> <dt>

1773 (0x6ED)
</dt> <dt>



Impossibile aprire il file della tabella di conversione dei caratteri.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**\_ \_ \_ \_ \_ file Short trans del carattere RPC X SS \_**
</dt> <dd> <dl> <dt>

1774 (0x6EE)
</dt> <dt>



Il file contenente la tabella di conversione dei caratteri ha meno di 512 byte.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC \_ X \_ SS \_ nel \_ \_ contesto null**
</dt> <dd> <dl> <dt>

1775 (0x6EF)
</dt> <dt>



Un handle di contesto null è stato passato dal client all'host durante una chiamata di procedura remota.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**\_contesto RPC \_ X \_ SS \_ danneggiato**
</dt> <dd> <dl> <dt>

1777 (0x6F1)
</dt> <dt>



Handle di contesto modificato durante una chiamata di procedura remota.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**\_handle RPC X \_ SS non \_ \_ corrispondenti**
</dt> <dd> <dl> <dt>

1778 (0x6F2)
</dt> <dt>



Gli handle di binding passati a una chiamata di procedura remota non corrispondono.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC \_ X \_ SS \_ non può \_ ottenere un \_ handle di chiamata \_**
</dt> <dd> <dl> <dt>

1779 (0x6F3)
</dt> <dt>



Lo stub non è in grado di ottenere l'handle di chiamata di procedura remota.


</dt> </dl> </dd> <dt>

<span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**\_puntatore di \_ \_ riferimento null RPC X \_**
</dt> <dd> <dl> <dt>

1780 (0x6F4)
</dt> <dt>



Un puntatore di riferimento null è stato passato allo stub.


</dt> </dl> </dd> <dt>

<span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**\_valore enum X RPC non \_ compreso nell' \_ \_ \_ \_ intervallo**
</dt> <dd> <dl> <dt>

1781 (0x6F5)
</dt> <dt>



Il valore di enumerazione è esterno all'intervallo.


</dt> </dl> </dd> <dt>

<span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**\_numero di byte RPC X \_ \_ \_ troppo \_ piccolo**
</dt> <dd> <dl> <dt>

1782 (0x6F6)
</dt> <dt>



Il numero di byte è troppo piccolo.


</dt> </dl> </dd> <dt>

<span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**\_ \_ dati stub non validi RPC X \_ \_**
</dt> <dd> <dl> <dt>

1783 (0x6F7)
</dt> <dt>



Lo stub ha ricevuto dati non validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**ERRORE \_ \_ buffer utente non valido \_**
</dt> <dd> <dl> <dt>

1784 (0x6F8)
</dt> <dt>



Il buffer utente specificato non è valido per l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**ERRORE \_ supporto non riconosciuto \_**
</dt> <dd> <dl> <dt>

1785 (0x6F9)
</dt> <dt>



Il supporto disco non è stato riconosciuto. Potrebbe non essere formattato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**ERRORE \_ nessun \_ \_ segreto LSA attendibile \_**
</dt> <dd> <dl> <dt>

1786 (0x6FA)
</dt> <dt>



La workstation non dispone di un segreto di attendibilità.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**ERRORE \_ nessun \_ \_ account SAM attendibile \_**
</dt> <dd> <dl> <dt>

1787 (0x6FB)
</dt> <dt>



Il database di sicurezza nel server non dispone di un account computer per la relazione di trust tra workstation.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**ERRORE \_ dominio attendibile errore \_ \_**
</dt> <dd> <dl> <dt>

1788 (0x6FC)
</dt> <dt>



La relazione di trust tra il dominio primario e il dominio trusted non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**ERRORE \_ relazione attendibile errore \_ \_**
</dt> <dd> <dl> <dt>

1789 (0x6FD)
</dt> <dt>



La relazione di trust tra questa workstation e il dominio primario non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**ERRORE di \_ attendibilità \_**
</dt> <dd> <dl> <dt>

1790 (0x6FE)
</dt> <dt>



Accesso alla rete non riuscito.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**\_chiamata RPC \_ \_ in \_ corso**
</dt> <dd> <dl> <dt>

1791 (0x6FF)
</dt> <dt>



È già in corso una chiamata di procedura remota per questo thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**ERRORE \_ Netlogon \_ non \_ avviato**
</dt> <dd> <dl> <dt>

1792 (0x700)
</dt> <dt>



È stato effettuato un tentativo di accesso, ma il servizio di accesso alla rete non è stato avviato.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**l'account di errore è \_ \_ scaduto**
</dt> <dd> <dl> <dt>

1793 (0x701)
</dt> <dt>



L'account dell'utente è scaduto.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**il \_ REdirector di \_ errore \_ ha \_ handle aperti**
</dt> <dd> <dl> <dt>

1794 (0x702)
</dt> <dt>



Il redirector è in uso e non può essere scaricato.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**\_driver della stampante di errore \_ \_ già \_ installato**
</dt> <dd> <dl> <dt>

1795 (0x703)
</dt> <dt>



Il driver della stampante specificato è già installato.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**ERRORE \_ \_ porta sconosciuta**
</dt> <dd> <dl> <dt>

1796 (0x704)
</dt> <dt>



La porta specificata è sconosciuta.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**ERRORE \_ \_ driver della stampante sconosciuto \_**
</dt> <dd> <dl> <dt>

1797 (0x705)
</dt> <dt>



Il driver della stampante è sconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**ERRORE \_ sconosciuto \_ PRINTPROCESSOR**
</dt> <dd> <dl> <dt>

1798 (0x706)
</dt> <dt>



Il processore di stampa è sconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**ERRORE \_ \_ file separatore non valido \_**
</dt> <dd> <dl> <dt>

1799 (0x707)
</dt> <dt>



Il file separatore specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**ERRORE \_ priorità non valida \_**
</dt> <dd> <dl> <dt>

1800 (0x708)
</dt> <dt>



La priorità specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**ERRORE \_ \_ nome stampante non valido \_**
</dt> <dd> <dl> <dt>

1801 (0x709)
</dt> <dt>



Il nome della stampante non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**la \_ stampante degli errori \_ \_ esiste già**
</dt> <dd> <dl> <dt>

1802 (0x70A)
</dt> <dt>



La stampante esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**ERRORE \_ \_ comando stampante non valido \_**
</dt> <dd> <dl> <dt>

1803 (0x70B)
</dt> <dt>



Il comando della stampante non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERRORE di tipo di dati \_ non valido \_**
</dt> <dd> <dl> <dt>

1804 (0x70C)
</dt> <dt>



Il tipo di dati specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**ERRORE \_ di \_ ambiente non valido**
</dt> <dd> <dl> <dt>

1805 (0x70D)
</dt> <dt>



L'ambiente specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**\_ \_ nessun \_ binding RPC S \_**
</dt> <dd> <dl> <dt>

1806 (0x70E)
</dt> <dt>



Non sono presenti altre associazioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**ERRORE \_ NOlogon- \_ \_ account trust \_ tra domini**
</dt> <dd> <dl> <dt>

1807 (0x70F)
</dt> <dt>



L'account utilizzato è un account trust tra domini. Per accedere a questo server, utilizzare l'account utente globale o l'account utente locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**ERRORE \_ NOlogon \_ workstation \_ trust \_ account**
</dt> <dd> <dl> <dt>

1808 (0x710)
</dt> <dt>



L'account utilizzato è un account computer. Per accedere a questo server, utilizzare l'account utente globale o l'account utente locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**ERRORE \_ nologo \_ server \_ trust \_ account**
</dt> <dd> <dl> <dt>

1809 (0x711)
</dt> <dt>



L'account utilizzato è un account di attendibilità del server. Per accedere a questo server, utilizzare l'account utente globale o l'account utente locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**Trust del dominio di errore non \_ \_ \_ coerente**
</dt> <dd> <dl> <dt>

1810 (0x712)
</dt> <dt>



Il nome o l'ID di sicurezza (SID) del dominio specificato non è coerente con le informazioni sull'attendibilità per tale dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**ERRORE \_ del \_ server \_ con \_ handle aperti**
</dt> <dd> <dl> <dt>

1811 (0x713)
</dt> <dt>



Il server è in uso e non può essere scaricato.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**dati della risorsa di errore \_ \_ \_ non \_ trovati**
</dt> <dd> <dl> <dt>

1812 (0x714)
</dt> <dt>



Il file di immagine specificato non contiene una sezione delle risorse.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**\_ \_ \_ Impossibile trovare il tipo di risorsa errore \_**
</dt> <dd> <dl> <dt>

1813 (0x715)
</dt> <dt>



Il tipo di risorsa specificato non è stato trovato nel file di immagine.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**\_ \_ \_ Impossibile trovare il nome della risorsa di errore \_**
</dt> <dd> <dl> <dt>

1814 (0x716)
</dt> <dt>



Il nome di risorsa specificato non è stato trovato nel file di immagine.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**\_ \_ \_ Impossibile trovare la risorsa di errore lang \_**
</dt> <dd> <dl> <dt>

1815 (0x717)
</dt> <dt>



Impossibile trovare l'ID lingua della risorsa specificato nel file di immagine.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**ERRORE \_ di \_ quota insufficiente \_**
</dt> <dd> <dl> <dt>

1816 (0x718)
</dt> <dt>



Non c'è abbastanza disponibilità di quota per elaborare il comando.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**\_non ci \_ sono \_ interfacce di RPC**
</dt> <dd> <dl> <dt>

1817 (0x719)
</dt> <dt>



Nessuna interfaccia registrata.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**\_chiamata RPC \_ \_ annullata**
</dt> <dd> <dl> <dt>

1818 (0x71A)
</dt> <dt>



La chiamata di procedura remota è stata annullata.


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**\_binding RPC \_ \_ incompleto**
</dt> <dd> <dl> <dt>

1819 (0x71B)
</dt> <dt>



L'handle di associazione non contiene tutte le informazioni necessarie.


</dt> </dl> </dd> <dt>

<span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**\_errore di \_ comunicazione RPC S \_**
</dt> <dd> <dl> <dt>

1820 (0x71C)
</dt> <dt>



Si è verificato un errore di comunicazione durante una chiamata di procedura remota.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**il \_ livello di autenticazione non è \_ supportato in \_ RPC \_**
</dt> <dd> <dl> <dt>

1821 (0x71D)
</dt> <dt>



Il livello di autenticazione richiesto non è supportato.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**\_ \_ \_ nome princ non presente \_ in RPC**
</dt> <dd> <dl> <dt>

1822 (0x71E)
</dt> <dt>



Nessun nome entità registrato.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**\_errore RPC S \_ Not \_ RPC \_**
</dt> <dd> <dl> <dt>

1823 (0x71F)
</dt> <dt>



L'errore specificato non è un codice di errore RPC di Windows valido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**\_ \_ \_ solo locale UUID \_ di RPC**
</dt> <dd> <dl> <dt>

1824 (0x720)
</dt> <dt>



È stato allocato un UUID valido solo in questo computer.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**errore pkg di RPC \_ s \_ sec \_ \_**
</dt> <dd> <dl> <dt>

1825 (0x721)
</dt> <dt>



Si è verificato un errore specifico del pacchetto di sicurezza.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC \_ \_ non \_ annullata**
</dt> <dd> <dl> <dt>

1826 (0x722)
</dt> <dt>



Il thread non è stato annullato.


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**\_ \_ azione es non valida RPC X \_ \_**
</dt> <dd> <dl> <dt>

1827 (0x723)
</dt> <dt>



Operazione non valida sull'handle di codifica/decodifica.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC \_ X \_ errata \_ \_ versione es**
</dt> <dd> <dl> <dt>

1828 (0x724)
</dt> <dt>



Versione non compatibile del pacchetto di serializzazione.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**RPC \_ X \_ \_ versione stub errata \_**
</dt> <dd> <dl> <dt>

1829 (0x725)
</dt> <dt>



Versione non compatibile dello stub RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**RPC \_ X \_ \_ oggetto pipe non valido \_**
</dt> <dd> <dl> <dt>

1830 (0x726)
</dt> <dt>



L'oggetto pipe RPC non è valido o è danneggiato.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**\_ordine di \_ pipe non corretto RPC X \_ \_**
</dt> <dd> <dl> <dt>

1831 (0x727)
</dt> <dt>



Si è tentato di eseguire un'operazione non valida su un oggetto pipe RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**\_ \_ versione pipe non corretta RPC X \_ \_**
</dt> <dd> <dl> <dt>

1832 (0x728)
</dt> <dt>



Versione pipe RPC non supportata.


</dt> </dl> </dd> <dt>

<span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**\_ \_ autenticazione cookie di \_ RPC \_ non riuscita**
</dt> <dd> <dl> <dt>

1833 (0x729)
</dt> <dt>



Il server proxy HTTP ha rifiutato la connessione perché l'autenticazione del cookie non è riuscita.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**il \_ \_ membro del gruppo RPC non è \_ stato \_ \_ trovato**
</dt> <dd> <dl> <dt>

1898 (0x76A)
</dt> <dt>



Impossibile trovare il membro del gruppo.


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**\_ \_ creazione cant di \_ EPT**
</dt> <dd> <dl> <dt>

1899 (0x76B)
</dt> <dt>



Non è stato possibile creare la voce del database di mapping degli endpoint.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**\_oggetto RPC \_ non valido \_**
</dt> <dd> <dl> <dt>

1900 (0x76C)
</dt> <dt>



L'identificatore univoco universale (UUID) dell'oggetto è l'UUID Nil.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**ERRORE \_ ora non valido \_**
</dt> <dd> <dl> <dt>

1901 (0x76D)
</dt> <dt>



L'ora specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**ERRORE \_ \_ nome modulo non valido \_**
</dt> <dd> <dl> <dt>

1902 (0x76E)
</dt> <dt>



Il nome del modulo specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**ERRORE \_ dimensione formato non valido \_ \_**
</dt> <dd> <dl> <dt>

1903 (0x76F)
</dt> <dt>



Dimensioni del form specificate non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**ERRORE \_ già \_ in attesa**
</dt> <dd> <dl> <dt>

1904 (0x770)
</dt> <dt>



L'handle della stampante specificato è già in attesa.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**stampante di errore \_ \_ eliminata**
</dt> <dd> <dl> <dt>

1905 (0x771)
</dt> <dt>



La stampante specificata è stata eliminata.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**ERRORE \_ di \_ stato della stampante non valido \_**
</dt> <dd> <dl> <dt>

1906 (0x772)
</dt> <dt>



Lo stato della stampante non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**è \_ \_ necessario \_ modificare la password di errore**
</dt> <dd> <dl> <dt>

1907 (0x773)
</dt> <dt>



È necessario modificare la password dell'utente prima dell'accesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**\_ \_ \_ Impossibile trovare il controller di dominio di errore \_**
</dt> <dd> <dl> <dt>

1908 (0x774)
</dt> <dt>



Non è stato possibile trovare il controller di dominio per questo dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**\_account errore \_ bloccato \_**
</dt> <dd> <dl> <dt>

1909 (0x775)
</dt> <dt>



L'account a cui si fa riferimento è attualmente bloccato e potrebbe non essere connesso a.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**o \_ Oxid non valido \_**
</dt> <dd> <dl> <dt>

1910 (0x776)
</dt> <dt>



Impossibile trovare l'utilità di esportazione oggetti specificata.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**o \_ OID non valido \_**
</dt> <dd> <dl> <dt>

1911 (0x777)
</dt> <dt>



Impossibile trovare l'oggetto specificato.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**o \_ set non valido \_**
</dt> <dd> <dl> <dt>

1912 (0x778)
</dt> <dt>



Il set di resolver di oggetti specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**\_invio di \_ RPC \_ incompleto**
</dt> <dd> <dl> <dt>

1913 (0x779)
</dt> <dt>



Alcuni dati restano da inviare nel buffer della richiesta.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**\_ \_ \_ handle asincrono non valido \_ RPC**
</dt> <dd> <dl> <dt>

1914 (0x77A)
</dt> <dt>



Handle di chiamata di procedura remota asincrona non valido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**\_ \_ \_ chiamata asincrona non valida \_ in RPC**
</dt> <dd> <dl> <dt>

1915 (0x77B)
</dt> <dt>



Handle di chiamata RPC asincrono non valido per questa operazione.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**\_pipe RPC \_ X \_ chiusa**
</dt> <dd> <dl> <dt>

1916 (0x77C)
</dt> <dt>



L'oggetto pipe RPC è già stato chiuso.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**\_errore di \_ disciplina della pipe RPC X \_ \_**
</dt> <dd> <dl> <dt>

1917 (0x77D)
</dt> <dt>



La chiamata RPC è stata completata prima dell'elaborazione di tutte le pipe.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**\_pipe RPC \_ X \_ vuota**
</dt> <dd> <dl> <dt>

1918 (0x77E)
</dt> <dt>



Dalla pipe RPC non sono disponibili altri dati.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**ERRORE \_ nessun \_ siteName**
</dt> <dd> <dl> <dt>

1919 (0x77F)
</dt> <dt>



Nessun nome di sito disponibile per questo computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ERRORE \_ di \_ accesso al \_ file**
</dt> <dd> <dl> <dt>

1920 (0x780)
</dt> <dt>



Non è possibile accedere al file dal sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**errore durante la \_ \_ risoluzione del \_ nome file**
</dt> <dd> <dl> <dt>

1921 (0x781)
</dt> <dt>



Il nome del file non può essere risolto dal sistema.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**tipo di voce RPC non \_ \_ \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

1922 (0x782)
</dt> <dt>



La voce non è del tipo previsto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC \_ \_ non \_ tutti i \_ obj \_ esportati**
</dt> <dd> <dl> <dt>

1923 (0x783)
</dt> <dt>



Non tutti gli UUID degli oggetti possono essere esportati nella voce specificata.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**\_interfaccia RPC \_ \_ non \_ esportata**
</dt> <dd> <dl> <dt>

1924 (0x784)
</dt> <dt>



Impossibile esportare l'interfaccia nella voce specificata.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**\_ \_ il profilo RPC \_ non è stato \_ aggiunto**
</dt> <dd> <dl> <dt>

1925 (0x785)
</dt> <dt>



Impossibile aggiungere la voce del profilo specificata.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC \_ per \_ PRF \_ \_ non \_ aggiunti**
</dt> <dd> <dl> <dt>

1926 (0x786)
</dt> <dt>



Non è stato possibile aggiungere l'elemento del profilo specificato.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC \_ \_ PRF \_ ELT \_ non \_ rimosso**
</dt> <dd> <dl> <dt>

1927 (0x787)
</dt> <dt>



Non è stato possibile rimuovere l'elemento del profilo specificato.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC \_ \_ GRP \_ ELT \_ non \_ aggiunto**
</dt> <dd> <dl> <dt>

1928 (0x788)
</dt> <dt>



Non è stato possibile aggiungere l'elemento di gruppo.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**RPC \_ \_ GRP \_ ELT \_ non \_ rimosso**
</dt> <dd> <dl> <dt>

1929 (0x789)
</dt> <dt>



Non è stato possibile rimuovere l'elemento del gruppo.


</dt> </dl> </dd> <dt>

<span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**ERRORE \_ km \_ driver \_ bloccato**
</dt> <dd> <dl> <dt>

1930 (0x78A)
</dt> <dt>



Il driver della stampante non è compatibile con i criteri abilitati nel computer che blocca i driver NT 4,0.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**contesto di errore \_ \_ scaduto**
</dt> <dd> <dl> <dt>

1931 (0x78B)
</dt> <dt>



Il contesto è scaduto e non può più essere utilizzato.


</dt> </dl> </dd> <dt>

<span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**ERRORE \_ per \_ \_ quota di attendibilità utente \_ \_ superata**
</dt> <dd> <dl> <dt>

1932 (0x78C)
</dt> <dt>



È stata superata la quota di creazione trust delegata dell'utente corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**ERRORE per \_ tutte le \_ quote di \_ attendibilità utente \_ \_ superate**
</dt> <dd> <dl> <dt>

1933 (0x78D)
</dt> <dt>



È stata superata la quota totale di creazione attendibile delegata.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**\_ \_ \_ superamento della quota di attendibilità Elimina utente \_ errore \_**
</dt> <dd> <dl> <dt>

1934 (0x78E)
</dt> <dt>



È stata superata la quota di eliminazione Trust delegata dell'utente corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**ERRORE \_ del \_ firewall di autenticazione \_**
</dt> <dd> <dl> <dt>

1935 (0x78F)
</dt> <dt>



Il computer a cui si sta effettuando l'accesso è protetto da un firewall di autenticazione. L'account specificato non è autorizzato a eseguire l'autenticazione nel computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**ERRORE \_ \_ connessioni di stampa Remote \_ \_ bloccate**
</dt> <dd> <dl> <dt>

1936 (0x790)
</dt> <dt>



Le connessioni remote allo spooler di stampa sono bloccate da un set di criteri nel computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**ERRORE \_ NTLM \_ bloccato**
</dt> <dd> <dl> <dt>

1937 (0x791)
</dt> <dt>



Autenticazione non riuscita perché l'autenticazione NTLM è stata disabilitata.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**modifica della password di errore \_ \_ \_ obbligatoria**
</dt> <dd> <dl> <dt>

1938 (0x792)
</dt> <dt>



Errore di accesso: i criteri EAS richiedono che l'utente modifichi la password prima di poter eseguire questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**ERRORE \_ nel \_ formato pixel non valido \_**
</dt> <dd> <dl> <dt>

2000 (0x7D0)
</dt> <dt>



Il formato pixel non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**ERRORE \_ \_ driver errato**
</dt> <dd> <dl> <dt>

2001 (0x7D1)
</dt> <dt>



Il driver specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**ERRORE \_ \_ stile finestra non valido \_**
</dt> <dd> <dl> <dt>

2002 (0x7D2)
</dt> <dt>



Lo stile della finestra o l'attributo della classe non è valido per questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**ERRORE \_ metafile \_ non \_ supportato**
</dt> <dd> <dl> <dt>

2003 (0x7D3)
</dt> <dt>



Operazione metafile richiesta non supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**\_trasformazione errore \_ non \_ supportata**
</dt> <dd> <dl> <dt>

2004 (0x7D4)
</dt> <dt>



Operazione di trasformazione richiesta non supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**il \_ ritaglio degli errori \_ non è \_ supportato**
</dt> <dd> <dl> <dt>

2005 (0x7D5)
</dt> <dt>



Operazione di ritaglio richiesta non supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**ERRORE \_ CMM non valido \_**
</dt> <dd> <dl> <dt>

2010 (0x7DA)
</dt> <dt>



Il modulo di gestione colori specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**ERRORE \_ profilo non valido \_**
</dt> <dd> <dl> <dt>

2011 (0x7DB)
</dt> <dt>



Il profilo colori specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**Tag di errore \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

2012 (0x7DC)
</dt> <dt>



Il tag specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**Tag di errore \_ \_ non \_ presente**
</dt> <dd> <dl> <dt>

2013 (0x7DD)
</dt> <dt>



Un tag obbligatorio non è presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**ERRORE \_ tag duplicato \_**
</dt> <dd> <dl> <dt>

2014 (0x7DE)
</dt> <dt>



Il tag specificato è già presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**\_profilo errore \_ non \_ associato \_ al \_ dispositivo**
</dt> <dd> <dl> <dt>

2015 (0x7DF)
</dt> <dt>



Il profilo colori specificato non è associato al dispositivo specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**\_profilo errore \_ non \_ trovato**
</dt> <dd> <dl> <dt>

2016 (0x7E0)
</dt> <dt>



Il profilo colori specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**ERRORE \_ dello \_ spazio di colore non valido**
</dt> <dd> <dl> <dt>

2017 (0x7E1)
</dt> <dt>



Lo spazio dei colori specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ERRORE \_ ICM \_ non \_ abilitato**
</dt> <dd> <dl> <dt>

2018 (0x7E2)
</dt> <dt>



La gestione dei colori dell'immagine non è abilitata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**errore durante l' \_ eliminazione di \_ MCI. \_**
</dt> <dd> <dl> <dt>

2019 (0x7E3)
</dt> <dt>



Si è verificato un errore durante l'eliminazione della trasformazione colore.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**\_trasformazione errore non valida \_**
</dt> <dd> <dl> <dt>

2020 (0x7E4)
</dt> <dt>



La trasformazione colore specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**ERRORE di \_ corrispondenza dello spazio di colore \_**
</dt> <dd> <dl> <dt>

2021 (0x7E5)
</dt> <dt>



La trasformazione specificata non corrisponde allo spazio dei colori della bitmap.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**ERRORE \_ ColorIndex non valido \_**
</dt> <dd> <dl> <dt>

2022 (0x7E6)
</dt> <dt>



L'indice dei colori denominato specificato non è presente nel profilo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**\_il profilo errore non \_ corrisponde al \_ \_ \_ dispositivo**
</dt> <dd> <dl> <dt>

2023 (0x7E7)
</dt> <dt>



Il profilo specificato è destinato a un dispositivo di un tipo diverso dal dispositivo specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**ERRORE \_ connesso \_ altra \_ password**
</dt> <dd> <dl> <dt>

2108 (0x83C)
</dt> <dt>



La connessione di rete è stata eseguita correttamente, ma all'utente è stata richiesta una password diversa da quella specificata in origine.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**ERRORE \_ connesso \_ altra \_ password \_ predefinita**
</dt> <dd> <dl> <dt>

2109 (0x83D)
</dt> <dt>



La connessione di rete è stata eseguita correttamente usando le credenziali predefinite.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**ERRORE \_ \_ nome utente errato**
</dt> <dd> <dl> <dt>

2202 (0x89A)
</dt> <dt>



Il nome utente specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**ERRORE \_ non \_ connesso**
</dt> <dd> <dl> <dt>

2250 (0x8CA)
</dt> <dt>



Questa connessione di rete non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**ERRORE di \_ apertura dei \_ file**
</dt> <dd> <dl> <dt>

2401 (0x961)
</dt> <dt>



Questa connessione di rete contiene file aperti o richieste in sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**ERRORE \_ \_ connessioni attive**
</dt> <dd> <dl> <dt>

2402 (0x962)
</dt> <dt>



Sono ancora presenti connessioni attive.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**\_dispositivo \_ di errore in \_ uso**
</dt> <dd> <dl> <dt>

2404 (0x964)
</dt> <dt>



Il dispositivo è usato da un processo attivo e non può essere disconnesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**ERRORE \_ di \_ monitoraggio stampa sconosciuto \_**
</dt> <dd> <dl> <dt>

3000 (0xBB8)
</dt> <dt>



Il monitor di stampa specificato è sconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**\_driver della \_ stampante \_ di errore in \_ uso**
</dt> <dd> <dl> <dt>

3001 (0xBB9)
</dt> <dt>



Il driver della stampante specificato è attualmente in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**\_ \_ \_ Impossibile trovare il file di SPOOLing degli errori \_**
</dt> <dd> <dl> <dt>

3002 (0xBBA)
</dt> <dt>



Impossibile trovare il file di spooling.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**ERRORE \_ SPL \_ nessun \_ StartDoc**
</dt> <dd> <dl> <dt>

3003 (0xBBB)
</dt> <dt>



Una chiamata StartDocPrinter non è stata rilasciata.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**ERRORE \_ SPL \_ nessun \_ ADDJOB**
</dt> <dd> <dl> <dt>

3004 (0xBBC)
</dt> <dt>



Una chiamata AddJob non è stata rilasciata.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**processore di stampa degli errori \_ \_ \_ già \_ installato**
</dt> <dd> <dl> <dt>

3005 (0xBBD)
</dt> <dt>



Il processore di stampa specificato è già stato installato.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**il monitoraggio della stampa degli errori è \_ \_ \_ già \_ installato**
</dt> <dd> <dl> <dt>

3006 (0xBBE)
</dt> <dt>



Il monitor di stampa specificato è già stato installato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**ERRORE \_ di \_ monitoraggio stampa non valido \_**
</dt> <dd> <dl> <dt>

3007 (0xBBF)
</dt> <dt>



Il monitor di stampa specificato non dispone delle funzioni obbligatorie.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**\_monitoraggio di stampa degli errori \_ \_ in \_ uso**
</dt> <dd> <dl> <dt>

3008 (0xBC0)
</dt> <dt>



Il monitor di stampa specificato è attualmente in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**ERRORE \_ della stampante \_ con \_ processi in \_ coda**
</dt> <dd> <dl> <dt>

3009 (0xBC1)
</dt> <dt>



L'operazione richiesta non è consentita quando sono presenti processi accodati alla stampante.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**ERRORE \_ di \_ riavvio \_ necessario**
</dt> <dd> <dl> <dt>

3010 (0xBC2)
</dt> <dt>



Operazione richiesta completata. Le modifiche non saranno effettive fino al riavvio del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**ERRORE \_ di \_ riavvio \_ necessario**
</dt> <dd> <dl> <dt>

3011 (0xBC3)
</dt> <dt>



Operazione richiesta completata. Le modifiche non saranno effettive fino a quando il servizio non viene riavviato.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**ERRORE di \_ stampante \_ non \_ trovato**
</dt> <dd> <dl> <dt>

3012 (0xBC4)
</dt> <dt>



Non sono state trovate stampanti.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**\_ \_ avviso driver stampante \_ errore**
</dt> <dd> <dl> <dt>

3013 (0xBC5)
</dt> <dt>



Il driver della stampante è noto come inaffidabile.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**\_driver della stampante di errore \_ \_ bloccato**
</dt> <dd> <dl> <dt>

3014 (0xBC6)
</dt> <dt>



Il driver della stampante è noto per danneggiare il sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**ERRORE \_ \_ del pacchetto driver della stampante \_ \_ in \_ uso**
</dt> <dd> <dl> <dt>

3015 (0xBC7)
</dt> <dt>



Il pacchetto di driver della stampante specificato è attualmente in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**\_ \_ \_ \_ Impossibile trovare il pacchetto driver di base errore \_**
</dt> <dd> <dl> <dt>

3016 (0xBC8)
</dt> <dt>



Impossibile trovare un pacchetto driver di base richiesto dal pacchetto driver della stampante.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**ERRORE \_ di \_ riavvio \_ richiesto**
</dt> <dd> <dl> <dt>

3017 (0xBC9)
</dt> <dt>



L'operazione richiesta non è riuscita. Per eseguire il rollback delle modifiche apportate, è necessario riavviare il sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**ERRORE \_ di \_ riavvio \_ avviato**
</dt> <dd> <dl> <dt>

3018 (0xBCA)
</dt> <dt>



L'operazione richiesta non è riuscita. È stato avviato un riavvio del sistema per eseguire il rollback delle modifiche apportate.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**errore durante il \_ download del driver della stampante \_ \_ \_**
</dt> <dd> <dl> <dt>

3019 (0xBCB)
</dt> <dt>



Il driver della stampante specificato non è stato trovato nel sistema ed è necessario scaricarlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**riavvio del processo di stampa degli errori \_ \_ \_ \_ obbligatorio**
</dt> <dd> <dl> <dt>

3020 (0xBCC)
</dt> <dt>



Impossibile stampare il processo di stampa richiesto. Per un aggiornamento del sistema di stampa è necessario inviare nuovamente il processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**ERRORE \_ del \_ \_ manifesto del driver della stampante non valido \_**
</dt> <dd> <dl> <dt>

3021 (0xBCD)
</dt> <dt>



Il driver della stampante non contiene un manifesto valido o contiene troppi manifesti.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**stampante di errore \_ \_ non \_ condivisibile**
</dt> <dd> <dl> <dt>

3022 (0xBCE)
</dt> <dt>



La stampante specificata non può essere condivisa.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**richiesta di errore \_ \_ sospesa**
</dt> <dd> <dl> <dt>

3050 (0xBEA)
</dt> <dt>



L'operazione è stata sospesa.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**ERRORI i/o \_ \_ ristampati \_ come \_ memorizzati nella cache**
</dt> <dd> <dl> <dt>

3950 (0xF6E)
</dt> <dt>



Eseguire nuovamente l'operazione specificata come operazione di i/o memorizzato nella cache.


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

 

 




