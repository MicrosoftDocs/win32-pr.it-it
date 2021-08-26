---
description: Descrive i codici di errore 12000-1599 definiti nel file di intestazione WinError.h ed è destinato agli sviluppatori.
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: Codici di errore di sistema (12000-15999) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: aa250eb26db3a2dfefda4c8b31bb2bbfd5e5d6415ea50d7279121fb09302c7ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058991"
---
# <a name="system-error-codes-12000-15999"></a>Codici di errore di sistema (12000-15999)

> [!NOTE]
> Queste informazioni sono destinate agli sviluppatori che ese tracciano errori di sistema. Per altri errori, ad esempio problemi con Windows, è disponibile un elenco di risorse nella [pagina Codici di](system-error-codes.md) errore.

L'elenco seguente descrive i [codici di errore di](system-error-codes.md) sistema (errori da 12000 a 15999). Vengono restituiti dalla [**funzione GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la [**funzione FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il flag **FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>**ERRORE \_ INTERNET\_\***
</dt> <dd> <dl> <dt>

12000 - 12175 (0x2EE0)
</dt> <dt>



Vedere [Codici di errore Internet](../wininet/wininet-errors.md) e WinInet.h.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>**ERRORE \_ DEL CRITERIO \_ QM IPSEC \_ \_**
</dt> <dd> <dl> <dt>

13000 (0x32C8)
</dt> <dt>



Il criterio in modalità rapida specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**ERRORE \_ CRITERI \_ QM IPSEC NON \_ \_ \_ TROVATI**
</dt> <dd> <dl> <dt>

13001 (0x32C9)
</dt> <dt>



Impossibile trovare i criteri in modalità rapida specificati.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERRORE \_ DEL CRITERIO \_ QM IPSEC \_ IN \_ \_ USO**
</dt> <dd> <dl> <dt>

13002 (0x32CA)
</dt> <dt>



Viene usato il criterio in modalità rapida specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**ERRORE \_ IL CRITERIO MM IPSEC \_ \_ \_ ESISTE**
</dt> <dd> <dl> <dt>

13003 (0x32CB)
</dt> <dt>



Il criterio in modalità principale specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERRORE \_ DEL CRITERIO MM IPSEC NON \_ \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

13004 (0x32CC)
</dt> <dt>



Impossibile trovare i criteri in modalità principale specificati.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**ERRORE \_ DEL CRITERIO MM IPSEC IN \_ \_ \_ \_ USO**
</dt> <dd> <dl> <dt>

13005 (0x32CD)
</dt> <dt>



Viene usato il criterio in modalità principale specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERRORE \_ DEL FILTRO MM IPSEC \_ \_ \_ ESISTENTE**
</dt> <dd> <dl> <dt>

13006 (0x32CE)
</dt> <dt>



Il filtro in modalità principale specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERRORE \_ FILTRO MM IPSEC NON \_ \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

13007 (0x32CF)
</dt> <dt>



Il filtro in modalità principale specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERRORE \_ DEL FILTRO DEL TRASPORTO IPSEC \_ \_ \_**
</dt> <dd> <dl> <dt>

13008 (0x32D0)
</dt> <dt>



Il filtro della modalità di trasporto specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERRORE \_ FILTRO TRASPORTO IPSEC NON \_ \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

13009 (0x32D1)
</dt> <dt>



Il filtro della modalità di trasporto specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERRORE \_ DELL'AUTENTICAZIONE \_ MM \_ IPSEC \_ ESISTENTE**
</dt> <dd> <dl> <dt>

13010 (0x32D2)
</dt> <dt>



L'elenco di autenticazione in modalità principale specificato esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERRORE \_ DI AUTENTICAZIONE MM \_ IPSEC NON \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

13011 (0x32D3)
</dt> <dt>



L'elenco di autenticazione in modalità principale specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERRORE \_ DI AUTENTICAZIONE MM \_ \_ IPSEC IN \_ \_ USO**
</dt> <dd> <dl> <dt>

13012 (0x32D4)
</dt> <dt>



Viene usato l'elenco di autenticazione in modalità principale specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**ERRORE \_ CRITERIO MM PREDEFINITO IPSEC NON \_ \_ \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

13013 (0x32D5)
</dt> <dt>



I criteri in modalità principale predefiniti specificati non sono stati trovati.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERRORE \_ DI AUTENTICAZIONE MM PREDEFINITA \_ \_ IPSEC NON \_ \_ \_ TROVATA**
</dt> <dd> <dl> <dt>

13014 (0x32D6)
</dt> <dt>



L'elenco di autenticazione in modalità principale predefinito specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERRORE \_ CRITERI \_ QM PREDEFINITI \_ IPSEC NON \_ \_ \_ TROVATI**
</dt> <dd> <dl> <dt>

13015 (0x32D7)
</dt> <dt>



I criteri in modalità rapida predefiniti specificati non sono stati trovati.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERRORE \_ DEL FILTRO TUNNEL IPSEC \_ \_ \_ ESISTENTE**
</dt> <dd> <dl> <dt>

13016 (0x32D8)
</dt> <dt>



Il filtro in modalità tunnel specificato esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**ERRORE \_ FILTRO TUNNEL IPSEC NON \_ \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

13017 (0x32D9)
</dt> <dt>



Il filtro in modalità tunnel specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERRORE \_ FILTRO IPSEC \_ MM ELIMINAZIONE \_ IN \_ \_ SOSPESO**
</dt> <dd> <dl> <dt>

13018 (0x32DA)
</dt> <dt>



Il filtro modalità principale è in sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**ERRORE FILTRO \_ TRASPORTO IPSEC \_ IN SOSPESO \_ \_ \_ ELIMINAZIONE**
</dt> <dd> <dl> <dt>

13019 (0x32DB)
</dt> <dt>



Il filtro di trasporto è in sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**ERRORE FILTRO \_ TUNNEL IPSEC \_ IN SOSPESO \_ \_ \_ ELIMINAZIONE**
</dt> <dd> <dl> <dt>

13020 (0x32DC)
</dt> <dt>



Il filtro del tunnel è in sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERRORE \_ DI ELIMINAZIONE DEI CRITERI MM \_ IPSEC IN \_ \_ \_ SOSPESO**
</dt> <dd> <dl> <dt>

13021 (0x32DD)
</dt> <dt>



I criteri in modalità principale sono in sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERRORE \_ DI ELIMINAZIONE IN SOSPESO \_ \_ DELL'AUTENTICAZIONE MM \_ \_ IPSEC**
</dt> <dd> <dl> <dt>

13022 (0x32DE)
</dt> <dt>



Il bundle di autenticazione in modalità principale è in sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**ERRORE \_ DURANTE L'ELIMINAZIONE \_ DEI CRITERI QM IPSEC \_ IN \_ \_ SOSPESO**
</dt> <dd> <dl> <dt>

13023 (0x32DF)
</dt> <dt>



I criteri in modalità rapida sono in sospeso.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**AVVISO \_ IPSEC \_ MM POLICY \_ \_ PRUNED**
</dt> <dd> <dl> <dt>

13024 (0x32E0)
</dt> <dt>



I criteri in modalità principale sono stati aggiunti correttamente, ma alcune delle offerte richieste non sono supportate.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**AVVISO \_ CRITERI \_ QM IPSEC \_ \_ ESEGUITI**
</dt> <dd> <dl> <dt>

13025 (0x32E1)
</dt> <dt>



I criteri in modalità rapida sono stati aggiunti correttamente, ma alcune delle offerte richieste non sono supportate.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERRORE \_ IPSEC \_ IKE \_ NEG \_ STATUS \_ BEGIN**
</dt> <dd> <dl> <dt>

13800 (0x35E8)
</dt> <dt>



ERRORE \_ IPSEC \_ IKE \_ NEG \_ STATUS \_ BEGIN


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERRORE \_ DI AUTENTICAZIONE \_ IKE IPSEC \_ NON \_ RIUSCITA**
</dt> <dd> <dl> <dt>

13801 (0x35E9)
</dt> <dt>



Le credenziali di autenticazione IKE non sono accettabili.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERRORE \_ \_ ATTRIB IKE IPSEC \_ \_ NON RIUSCITO**
</dt> <dd> <dl> <dt>

13802 (0x35EA)
</dt> <dt>



Gli attributi di sicurezza IKE non sono accettabili.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERRORE \_ NEGOZIAZIONE \_ IKE IPSEC \_ IN \_ SOSPESO**
</dt> <dd> <dl> <dt>

13803 (0x35EB)
</dt> <dt>



Negoziazione IKE in corso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**ERRORE \_ DI ELABORAZIONE GENERALE \_ IKE IPSEC \_ \_ \_**
</dt> <dd> <dl> <dt>

13804 (0x35EC)
</dt> <dt>



Errore di elaborazione generale.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**ERRORE \_ TIMEOUT \_ IKE IPSEC \_ \_**
</dt> <dd> <dl> <dt>

13805 (0x35ED)
</dt> <dt>



Timeout della negoziazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERRORE \_ IPSEC \_ IKE \_ NO \_ CERT**
</dt> <dd> <dl> <dt>

13806 (0x35EE)
</dt> <dt>



IKE non è riuscito a trovare un certificato del computer valido. Contattare l'amministratore della sicurezza di rete per l'installazione di un certificato valido nell'archivio certificati appropriato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERRORE \_ IPSEC \_ IKE \_ SA \_ DELETED**
</dt> <dd> <dl> <dt>

13807 (0x35EF)
</dt> <dt>



Sa IKE eliminata dal peer prima del completamento dell'impostazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERRORE \_ IPSEC \_ IKE \_ SA \_ REAPED**
</dt> <dd> <dl> <dt>

13808 (0x35F0)
</dt> <dt>



L'sa IKE è stata eliminata prima del completamento dell'installazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**ERRORE \_ IPSEC \_ IKE \_ MM ACQUIRE \_ \_ DROP**
</dt> <dd> <dl> <dt>

13809 (0x35F1)
</dt> <dt>



La richiesta di negoziazione è stata inviata in coda troppo a lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**ERRORE \_ IPSEC \_ IKE \_ QM \_ ACQUIRE \_ DROP**
</dt> <dd> <dl> <dt>

13810 (0x35F2)
</dt> <dt>



La richiesta di negoziazione è stata inviata in coda troppo a lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERRORE \_ IPSEC \_ IKE \_ QUEUE DROP \_ \_ MM**
</dt> <dd> <dl> <dt>

13811 (0x35F3)
</dt> <dt>



La richiesta di negoziazione è stata inviata in coda troppo a lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**ERRORE \_ IPSEC \_ IKE \_ QUEUE DROP \_ \_ NO \_ MM**
</dt> <dd> <dl> <dt>

13812 (0x35F4)
</dt> <dt>



La richiesta di negoziazione è stata inviata in coda troppo a lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERRORE \_ IPSEC \_ IKE \_ DROP NO \_ \_ RESPONSE**
</dt> <dd> <dl> <dt>

13813 (0x35F5)
</dt> <dt>



Nessuna risposta dal peer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**ERRORE \_ IPSEC \_ IKE \_ MM DELAY \_ \_ DROP**
</dt> <dd> <dl> <dt>

13814 (0x35F6)
</dt> <dt>



La negoziazione ha richiesto troppo tempo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**ERRORE \_ IPSEC \_ IKE \_ QM \_ DELAY \_ DROP**
</dt> <dd> <dl> <dt>

13815 (0x35F7)
</dt> <dt>



La negoziazione ha richiesto troppo tempo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**ERRORE \_ \_ IKE IPSEC \_**
</dt> <dd> <dl> <dt>

13816 (0x35F8)
</dt> <dt>



Si è verificato un errore sconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERRORE \_ IPSEC \_ IKE \_ CRL \_ NON RIUSCITO**
</dt> <dd> <dl> <dt>

13817 (0x35F9)
</dt> <dt>



Controllo delle revoche di certificati non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERRORE \_ IKE \_ IPSEC \_ UTILIZZO CHIAVE NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

13818 (0x35FA)
</dt> <dt>



Utilizzo della chiave del certificato non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERRORE \_ IPSEC \_ IKE \_ TIPO DI CERTIFICATO \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

13819 (0x35FB)
</dt> <dt>



Tipo di certificato non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERRORE \_ IPSEC \_ IKE \_ NO PRIVATE \_ \_ KEY**
</dt> <dd> <dl> <dt>

13820 (0x35FC)
</dt> <dt>



La negoziazione IKE non è riuscita perché il certificato del computer usato non ha una chiave privata. I certificati IPsec richiedono una chiave privata. Contattare l'amministratore della protezione di rete per informazioni sulla sostituzione con un certificato con una chiave privata.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERRORE \_ IPSEC \_ IKE \_ \_ REKEY SIMULTANEO**
</dt> <dd> <dl> <dt>

13821 (0x35FD)
</dt> <dt>



Sono state rilevate chiavi simultanee.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**ERRORE \_ IPSEC \_ IKE \_ DH \_ FAIL**
</dt> <dd> <dl> <dt>

13822 (0x35FE)
</dt> <dt>



Errore nel Diffie-Hellman calcolo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERRORE \_ PAYLOAD \_ CRITICO IKE IPSEC \_ NON \_ \_ \_ RICONOSCIUTO**
</dt> <dd> <dl> <dt>

13823 (0x35FF)
</dt> <dt>



Non so come elaborare il payload critico.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERRORE \_ INTESTAZIONE \_ IKE IPSEC \_ NON \_ VALIDA**
</dt> <dd> <dl> <dt>

13824 (0x3600)
</dt> <dt>



Intestazione non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERRORE \_ IPSEC \_ IKE \_ NESSUN \_ CRITERIO**
</dt> <dd> <dl> <dt>

13825 (0x3601)
</dt> <dt>



Nessun criterio configurato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERRORE \_ FIRMA \_ IKE IPSEC \_ NON \_ VALIDA**
</dt> <dd> <dl> <dt>

13826 (0x3602)
</dt> <dt>



Impossibile verificare la firma.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**ERRORE \_ IPSEC \_ IKE \_ KERBEROS \_ ERROR**
</dt> <dd> <dl> <dt>

13827 (0x3603)
</dt> <dt>



Impossibile eseguire l'autenticazione con Kerberos.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERRORE \_ IPSEC \_ IKE \_ NO PUBLIC \_ \_ KEY**
</dt> <dd> <dl> <dt>

13828 (0x3604)
</dt> <dt>



Il certificato del peer non dispone di una chiave pubblica.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERRORE \_ IPSEC \_ IKE \_ PROCESS \_ ERR**
</dt> <dd> <dl> <dt>

13829 (0x3605)
</dt> <dt>



Errore durante l'elaborazione del payload dell'errore.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERRORE \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ SA**
</dt> <dd> <dl> <dt>

13830 (0x3606)
</dt> <dt>



Errore durante l'elaborazione del payload sa.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**ERRORE \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ PROP**
</dt> <dd> <dl> <dt>

13831 (0x3607)
</dt> <dt>



Errore durante l'elaborazione del payload della proposta.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERRORE \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ TRANS**
</dt> <dd> <dl> <dt>

13832 (0x3608)
</dt> <dt>



Errore durante l'elaborazione del payload di trasformazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**ERRORE \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ KE**
</dt> <dd> <dl> <dt>

13833 (0x3609)
</dt> <dt>



Errore durante l'elaborazione del payload KE.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**ERRORE \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ ID**
</dt> <dd> <dl> <dt>

13834 (0x360A)
</dt> <dt>



Errore durante l'elaborazione del payload dell'ID.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**ERRORE \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ CERT**
</dt> <dd> <dl> <dt>

13835 (0x360B)
</dt> <dt>



Errore durante l'elaborazione del payload del certificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERRORE \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ CERT \_ REQ**
</dt> <dd> <dl> <dt>

13836 (0x360C)
</dt> <dt>



Errore durante l'elaborazione del payload della richiesta di certificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERRORE \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ HASH**
</dt> <dd> <dl> <dt>

13837 (0x360D)
</dt> <dt>



Errore durante l'elaborazione del payload hash.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**ERRORE \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ SIG**
</dt> <dd> <dl> <dt>

13838 (0x360E)
</dt> <dt>



Errore durante l'elaborazione del payload della firma.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERRORE \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ NONCE**
</dt> <dd> <dl> <dt>

13839 (0x360F)
</dt> <dt>



Errore durante l'elaborazione del payload nonce.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**ERRORE \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ NOTIFY**
</dt> <dd> <dl> <dt>

13840 (0x3610)
</dt> <dt>



Errore durante l'elaborazione del payload di notifica.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**ERRORE \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ DELETE**
</dt> <dd> <dl> <dt>

13841 (0x3611)
</dt> <dt>



Errore durante l'elaborazione del payload di eliminazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**ERRORE \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ VENDOR**
</dt> <dd> <dl> <dt>

13842 (0x3612)
</dt> <dt>



Errore durante l'elaborazione del payload VendorId.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERRORE \_ PAYLOAD \_ IKE IKE \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

13843 (0x3613)
</dt> <dt>



Payload non valido ricevuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERRORE \_ IPSEC \_ IKE \_ LOAD SOFT \_ \_ SA**
</dt> <dd> <dl> <dt>

13844 (0x3614)
</dt> <dt>



Sa soft caricata.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERRORE \_ IPSEC \_ IKE \_ SOFT SA \_ \_ TORN \_ DOWN**
</dt> <dd> <dl> <dt>

13845 (0x3615)
</dt> <dt>



Sa soft disassociata.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERRORE \_ \_ IKE IKE \_ COOKIE NON \_ VALIDO**
</dt> <dd> <dl> <dt>

13846 (0x3616)
</dt> <dt>



Cookie non valido ricevuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERRORE \_ IPSEC \_ IKE \_ NO PEER \_ \_ CERT**
</dt> <dd> <dl> <dt>

13847 (0x3617)
</dt> <dt>



Il peer non è riuscito a inviare un certificato computer valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERRORE \_ CRL \_ PEER IKE IPSEC \_ NON \_ \_ RIUSCITO**
</dt> <dd> <dl> <dt>

13848 (0x3618)
</dt> <dt>



Controllo di revoca della certificazione del certificato del peer non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**ERRORE \_ DI MODIFICA DEI CRITERI \_ IKE \_ \_ IPSEC**
</dt> <dd> <dl> <dt>

13849 (0x3619)
</dt> <dt>



Nuove SA invalidate da criteri formate con criteri obsoleti.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**ERRORE \_ IPSEC \_ IKE \_ NO MM \_ \_ POLICY**
</dt> <dd> <dl> <dt>

13850 (0x361A)
</dt> <dt>



Non sono disponibili criteri IKE in modalità principale.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERRORE \_ IPSEC \_ IKE \_ NOTCBPRIV**
</dt> <dd> <dl> <dt>

13851 (0x361B)
</dt> <dt>



Non è stato possibile abilitato il privilegio TCB.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERRORE \_ IPSEC \_ IKE \_ SECLOADFAIL**
</dt> <dd> <dl> <dt>

13852 (0x361C)
</dt> <dt>



Impossibile caricare SECURITY.DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERRORE \_ IPSEC \_ IKE \_ FAILSSPINIT**
</dt> <dd> <dl> <dt>

13853 (0x361D)
</dt> <dt>



Impossibile ottenere l'indirizzo di invio della tabella delle funzioni di sicurezza da SSPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERRORE \_ IPSEC \_ IKE \_ FAILQUERYSSP**
</dt> <dd> <dl> <dt>

13854 (0x361E)
</dt> <dt>



Impossibile eseguire una query sul pacchetto Kerberos per ottenere le dimensioni massime del token.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERRORE \_ IPSEC \_ IKE \_ SRVACQFAIL**
</dt> <dd> <dl> <dt>

13855 (0x361F)
</dt> <dt>



Impossibile ottenere le credenziali del server Kerberos per il servizio \_ IKE IPSEC ISAKMP/ERROR. \_ L'autenticazione Kerberos non funzionerà. Il motivo più probabile è la mancanza di appartenenza al dominio. Questo è normale se il computer è membro di un gruppo di lavoro.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERRORE \_ IPSEC \_ IKE \_ SRVQUERYCRED**
</dt> <dd> <dl> <dt>

13856 (0x3620)
</dt> <dt>



Impossibile determinare il nome dell'entità SSPI per il servizio IKE IPSEC ISAKMP/ERROR \_ \_ ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERRORE \_ IPSEC \_ IKE \_ GETSPIFAIL**
</dt> <dd> <dl> <dt>

13857 (0x3621)
</dt> <dt>



Impossibile ottenere il nuovo SPI per la sa in ingresso dal driver IPsec. La causa più comune è che il driver non dispone del filtro corretto. Controllare i criteri per verificare i filtri.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERRORE \_ FILTRO \_ IPSEC IKE \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

13858 (0x3622)
</dt> <dt>



Il filtro specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERRORE \_ IPSEC \_ IKE \_ MEMORIA \_ \_ INSUFFICIENTE**
</dt> <dd> <dl> <dt>

13859 (0x3623)
</dt> <dt>



L'allocazione di memoria ha avuto esito negativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERRORE IKE IKE ADD UPDATE KEY FAILED (ERRORE \_ IPSEC \_ IKE ADD UPDATE \_ KEY \_ \_ \_ FAILED)**
</dt> <dd> <dl> <dt>

13860 (0x3624)
</dt> <dt>



Impossibile aggiungere l'associazione di sicurezza al driver IPsec. La causa più comune è se il completamento della negoziazione IKE ha richiesto troppo tempo. Se il problema persiste, ridurre il carico sul computer che causa l'errore.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERRORE \_ CRITERI \_ IPSEC IKE \_ NON \_ VALIDI**
</dt> <dd> <dl> <dt>

13861 (0x3625)
</dt> <dt>



Criteri non validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERRORE \_ IPSEC \_ IKE \_ SCONOSCIUTO \_ DOI**
</dt> <dd> <dl> <dt>

13862 (0x3626)
</dt> <dt>



DOI non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**ERRORE \_ IPSEC \_ IKE \_ SITUAZIONE NON \_ VALIDA**
</dt> <dd> <dl> <dt>

13863 (0x3627)
</dt> <dt>



Situazione non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**ERRORE \_ IPSEC \_ IKE \_ DH \_ FAILURE**
</dt> <dd> <dl> <dt>

13864 (0x3628)
</dt> <dt>



Diffie-Hellman errore.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERRORE \_ GRUPPO \_ IPSEC IKE \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

13865 (0x3629)
</dt> <dt>



Gruppo Diffie-Hellman non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERRORE \_ IPSEC \_ IKE \_ ENCRYPT**
</dt> <dd> <dl> <dt>

13866 (0x362A)
</dt> <dt>



Errore durante la crittografia del payload.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERRORE \_ DI DECRITTOGRAFIA \_ IKE IPSEC \_**
</dt> <dd> <dl> <dt>

13867 (0x362B)
</dt> <dt>



Errore durante la decrittografia del payload.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERRORE \_ DI CORRISPONDENZA DEI CRITERI \_ IKE IPSEC \_ \_**
</dt> <dd> <dl> <dt>

13868 (0x362C)
</dt> <dt>



Errore di corrispondenza dei criteri.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERRORE \_ IPSEC \_ IKE \_ ID NON \_ SUPPORTATO**
</dt> <dd> <dl> <dt>

13869 (0x362D)
</dt> <dt>



ID non supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERRORE \_ DI HASH \_ IKE IKE \_ IPSEC NON \_ VALIDO**
</dt> <dd> <dl> <dt>

13870 (0x362E)
</dt> <dt>



Verifica dell'hash non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERRORE \_ IPSEC \_ IKE \_ HASH NON \_ \_ VALIDO ALG**
</dt> <dd> <dl> <dt>

13871 (0x362F)
</dt> <dt>



Algoritmo hash non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERRORE \_ IPSEC \_ IKE \_ DIMENSIONI HASH NON \_ \_ VALIDE**
</dt> <dd> <dl> <dt>

13872 (0x3630)
</dt> <dt>



Dimensioni hash non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERRORE \_ IPSEC \_ IKE \_ NON VALIDO ENCRYPT \_ \_ ALG**
</dt> <dd> <dl> <dt>

13873 (0x3631)
</dt> <dt>



Algoritmo di crittografia non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERRORE \_ IPSEC \_ IKE \_ NON VALIDO \_ AUTH \_ ALG**
</dt> <dd> <dl> <dt>

13874 (0x3632)
</dt> <dt>



Algoritmo di autenticazione non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERRORE \_ IPSEC \_ IKE \_ NON VALIDO \_ SIG**
</dt> <dd> <dl> <dt>

13875 (0x3633)
</dt> <dt>



Firma del certificato non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERRORE \_ CARICAMENTO \_ IKE IPSEC \_ NON \_ RIUSCITO**
</dt> <dd> <dl> <dt>

13876 (0x3634)
</dt> <dt>



Caricamento non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERRORE \_ IPSEC \_ IKE \_ RPC \_ DELETE**
</dt> <dd> <dl> <dt>

13877 (0x3635)
</dt> <dt>



Eliminato tramite chiamata RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERRORE \_ IPSEC \_ IKE \_ BENIGN \_ REINIT**
</dt> <dd> <dl> <dt>

13878 (0x3636)
</dt> <dt>



Stato temporaneo creato per eseguire la reinizializzazione. Non si tratta di un errore reale.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERRORE \_ IPSEC \_ IKE \_ INVALID \_ RESPONDER LIFETIME \_ \_ NOTIFY**
</dt> <dd> <dl> <dt>

13879 (0x3637)
</dt> <dt>



Il valore di durata ricevuto nella notifica sulla durata del risponditore è inferiore al valore minimo Windows 2000 configurato. Correggere i criteri nel computer peer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERRORE \_ IPSEC \_ IKE \_ VERSIONE PRINCIPALE NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

13880 (0x3638)
</dt> <dt>



Il destinatario non può gestire la versione di IKE specificata nell'intestazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERRORE \_ IPSEC \_ IKE \_ \_ CERT \_ KEYLEN NON VALIDO**
</dt> <dd> <dl> <dt>

13881 (0x3639)
</dt> <dt>



La lunghezza della chiave nel certificato è troppo piccola per i requisiti di sicurezza configurati.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**ERRORE \_ IPSEC \_ IKE \_ MM \_ LIMIT**
</dt> <dd> <dl> <dt>

13882 (0x363A)
</dt> <dt>



È stato superato il numero massimo di SA MM stabilite per il peer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERRORE \_ DI NEGOZIAZIONE \_ IKE IPSEC \_ \_ DISABILITATO**
</dt> <dd> <dl> <dt>

13883 (0x363B)
</dt> <dt>



IKE ha ricevuto un criterio che disabilita la negoziazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**ERRORE \_ IPSEC \_ IKE \_ QM \_ LIMIT**
</dt> <dd> <dl> <dt>

13884 (0x363C)
</dt> <dt>



Raggiunto il limite massimo di modalità rapida per la modalità principale. Verrà avviata la nuova modalità principale.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERRORE \_ IPSEC \_ IKE \_ MM \_ SCADUTO**
</dt> <dd> <dl> <dt>

13885 (0x363D)
</dt> <dt>



La durata dell'sa in modalità principale è scaduta o il peer ha inviato un'eliminazione in modalità principale.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**ERRORE \_ DEL \_ PEER IKE IPSEC \_ MM \_ \_ RITENUTO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

13886 (0x363E)
</dt> <dt>



Sa in modalità principale ritenuta non valida perché il peer ha interrotto la risposta.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERRORE \_ IPSEC \_ IKE \_ CERT \_ CHAIN POLICY \_ \_ MISMATCH**
</dt> <dd> <dl> <dt>

13887 (0x363F)
</dt> <dt>



Il certificato non viene concatenato a una radice attendibile nei criteri IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERRORE \_ \_ IKE IKE \_ ID MESSAGGIO \_ \_ IMPREVISTO**
</dt> <dd> <dl> <dt>

13888 (0x3640)
</dt> <dt>



Ricevuto ID messaggio imprevisto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERRORE \_ IPSEC \_ IKE \_ PAYLOAD DI AUTENTICAZIONE \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

13889 (0x3641)
</dt> <dt>



Ricevute offerte di autenticazione non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERRORE \_ \_ IKE \_ IKE DOS \_ COOKIE \_ INVIATO**
</dt> <dd> <dl> <dt>

13890 (0x3642)
</dt> <dt>



Invio di una notifica del cookie DoS all'iniziatore.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERRORE \_ DI ARRESTO \_ IKE IPSEC \_ \_**
</dt> <dd> <dl> <dt>

13891 (0x3643)
</dt> <dt>



Arresto del servizio IKE in fase di arresto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERRORE \_ DI AUTENTICAZIONE \_ IKE \_ CGA IPSEC \_ NON \_ RIUSCITA**
</dt> <dd> <dl> <dt>

13892 (0x3644)
</dt> <dt>



Impossibile verificare l'associazione tra l'indirizzo CGA e il certificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERRORE \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ NATOA**
</dt> <dd> <dl> <dt>

13893 (0x3645)
</dt> <dt>



Errore durante l'elaborazione del payload NatOA.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERRORE \_ IPSEC \_ IKE \_ MM NON VALIDO \_ \_ PER \_ QM**
</dt> <dd> <dl> <dt>

13894 (0x3646)
</dt> <dt>



I parametri della modalità principale non sono validi per questa modalità rapida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**ERRORE \_ IPSEC \_ IKE \_ QM \_ SCADUTO**
</dt> <dd> <dl> <dt>

13895 (0x3647)
</dt> <dt>



La firma di accesso condiviso in modalità rapida è scaduta dal driver IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERRORE \_ IPSEC \_ IKE \_ TROPPI \_ \_ FILTRI**
</dt> <dd> <dl> <dt>

13896 (0x3648)
</dt> <dt>



Sono stati rilevati troppi filtri IKEEXT aggiunti dinamicamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERRORE \_ IPSEC \_ IKE \_ NEG \_ STATUS \_ END**
</dt> <dd> <dl> <dt>

13897 (0x3649)
</dt> <dt>



ERRORE \_ IPSEC \_ IKE \_ NEG \_ STATUS \_ END


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERRORE \_ IPSEC \_ IKE \_ KILL \_ DUMMY \_ NAP \_ TUNNEL**
</dt> <dd> <dl> <dt>

13898 (0x364A)
</dt> <dt>



L'autenticazione di Protezione accesso alla rete è riuscita ed è necessario eliminare il tunnel IKEv2 di Protezione accesso alla rete fittizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**ERRORE \_ DI ASSEGNAZIONE \_ IPSEC INTERNA \_ \_ \_ \_ IPSEC NON RIUSCITA**
</dt> <dd> <dl> <dt>

13899 (0x364B)
</dt> <dt>



Errore durante l'assegnazione dell'indirizzo IP interno all'iniziatore in modalità tunnel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERRORE \_ IPSEC \_ IKE \_ REQUIRE CP \_ \_ PAYLOAD \_ MISSING**
</dt> <dd> <dl> <dt>

13900 (0x364C)
</dt> <dt>



Richiesta payload di configurazione mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERRORE \_ NEGOZIAZIONE RAPPRESENTAZIONE MODULO CHIAVE IPSEC \_ \_ IN \_ \_ \_ SOSPESO**
</dt> <dd> <dl> <dt>

13901 (0x364D)
</dt> <dt>



È in corso una negoziazione in esecuzione come principio di sicurezza che ha emesso la connessione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERRORE \_ DI COESISTENZA \_ IKE IPSEC \_ \_**
</dt> <dd> <dl> <dt>

13902 (0x364E)
</dt> <dt>



La firma di accesso condiviso è stata eliminata a causa della coesistenza di IKEv1/AuthIP.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERRORE \_ IPSEC \_ IKE \_ RATELIMIT \_ DROP**
</dt> <dd> <dl> <dt>

13903 (0x364F)
</dt> <dt>



La richiesta SA in ingresso è stata eliminata a causa della limitazione della frequenza degli indirizzi IP peer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERRORE \_ IL \_ PEER IKE IPSEC \_ NON SUPPORTA \_ \_ \_ MOBIKE**
</dt> <dd> <dl> <dt>

13904 (0x3650)
</dt> <dt>



Il peer non supporta MOBIKE.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERRORE \_ DI AUTORIZZAZIONE \_ IKE IPSEC \_ \_**
</dt> <dd> <dl> <dt>

13905 (0x3651)
</dt> <dt>



Associazione di sicurezza non autorizzata.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERRORE IPSEC IKE STRONG CRED AUTHORIZATION FAILURE (ERRORE DI \_ \_ AUTORIZZAZIONE CRED FORTE IKE \_ \_ \_ \_ IPSEC)**
</dt> <dd> <dl> <dt>

13906 (0x3652)
</dt> <dt>



L'azienda SA non è autorizzata perché non esiste una credenziale basata su PKINIT sufficientemente forte.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERRORE \_ DI AUTORIZZAZIONE \_ IKE IPSEC \_ CON NUOVO TENTATIVO \_ \_ \_ \_ FACOLTATIVO**
</dt> <dd> <dl> <dt>

13907 (0x3653)
</dt> <dt>



Associazione di sicurezza non autorizzata. Potrebbe essere necessario immettere credenziali aggiornate o diverse, ad esempio una smart card.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**ERRORE \_ DI AUTORIZZAZIONE CRED SICURO IKE IPSEC \_ E ERRORE \_ \_ \_ \_ \_ CERTMAP \_**
</dt> <dd> <dl> <dt>

13908 (0x3654)
</dt> <dt>



L'azienda SA non è autorizzata perché non esiste una credenziale basata su PKINIT sufficientemente forte. Potrebbe trattarsi di un errore di mapping da certificato ad account per l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERRORE \_ IPSEC \_ IKE \_ NEG \_ STATUS EXTENDED \_ \_ END**
</dt> <dd> <dl> <dt>

13909 (0x3655)
</dt> <dt>



ERRORE \_ IPSEC \_ IKE \_ NEG \_ STATUS EXTENDED \_ \_ END


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERRORE \_ IPSEC \_ BAD \_ SPI**
</dt> <dd> <dl> <dt>

13910 (0x3656)
</dt> <dt>



L'spi nel pacchetto non corrisponde a una sa IPsec valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**ERRORE DURATA \_ SA IPSEC \_ \_ \_ SCADUTA**
</dt> <dd> <dl> <dt>

13911 (0x3657)
</dt> <dt>



Il pacchetto è stato ricevuto in una sa IPsec la cui durata è scaduta.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**ERRORE \_ IPSEC - FIRMA DI ACCESSO \_ CONDIVISO NON \_ CORRETTO**
</dt> <dd> <dl> <dt>

13912 (0x3658)
</dt> <dt>



Il pacchetto è stato ricevuto in una firma di accesso condiviso IPsec che non corrisponde alle caratteristiche del pacchetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERRORE \_ CONTROLLO RIPRODUZIONE IPSEC NON \_ \_ \_ RIUSCITO**
</dt> <dd> <dl> <dt>

13913 (0x3659)
</dt> <dt>



Controllo di riproduzione del numero di sequenza del pacchetto non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERRORE \_ IPSEC \_ PACCHETTO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

13914 (0x365A)
</dt> <dt>



L'intestazione IPsec e/o il trailer nel pacchetto non sono validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**ERRORE \_ CONTROLLO INTEGRITÀ IPSEC NON \_ \_ \_ RIUSCITO**
</dt> <dd> <dl> <dt>

13915 (0x365B)
</dt> <dt>



Controllo di integrità IPsec non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**ERRORE \_ ELIMINAZIONE TESTO NON \_ CRITTOGRAFATO IPSEC \_ \_**
</dt> <dd> <dl> <dt>

13916 (0x365C)
</dt> <dt>



IPsec ha eliminato un pacchetto di testo non crittografato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERRORE \_ DI ELIMINAZIONE DEL FIREWALL DI \_ \_ AUTENTICAZIONE IPSEC \_**
</dt> <dd> <dl> <dt>

13917 (0x365D)
</dt> <dt>



IPsec ha eliminato un pacchetto ESP in ingresso in modalità firewall autenticata. Questo calo è non dannoso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERRORE \_ DI ELIMINAZIONE DELLA LIMITAZIONE \_ \_ IPSEC**
</dt> <dd> <dl> <dt>

13918 (0x365E)
</dt> <dt>



IPsec ha eliminato un pacchetto a causa della limitazione DoS.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERRORE \_ BLOCCO \_ DOSP \_ IPSEC**
</dt> <dd> <dl> <dt>

13925 (0x3665)
</dt> <dt>



Protezione DoS IPsec corrisponde a una regola di blocco esplicita.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERRORE \_ IPSEC \_ DOSP \_ RECEIVED \_ MULTICAST**
</dt> <dd> <dl> <dt>

13926 (0x3666)
</dt> <dt>



Protezione DoS IPsec ha ricevuto un pacchetto multicast specifico IPsec che non è consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERRORE \_ IPSEC \_ DOSP \_ PACCHETTO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

13927 (0x3667)
</dt> <dt>



Protezione DoS IPsec ha ricevuto un pacchetto formattato in modo non corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**ERRORE \_ RICERCA STATO DOSP IPSEC \_ NON \_ \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

13928 (0x3668)
</dt> <dt>



La protezione DoS IPsec non è riuscita a cercare lo stato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**ERROR \_ IPSEC \_ DOSP \_ MAX \_ ENTRIES**
</dt> <dd> <dl> <dt>

13929 (0x3669)
</dt> <dt>



La protezione DoS IPsec non è riuscita a creare lo stato perché è stato raggiunto il numero massimo di voci consentite dai criteri.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERRORE \_ IPSEC \_ DOSP \_ KEYMOD \_ NON \_ CONSENTITO**
</dt> <dd> <dl> <dt>

13930 (0x366A)
</dt> <dt>



Protezione DoS IPsec ha ricevuto un pacchetto di negoziazione IPsec per un modulo di gestione delle chiavi che non è consentito dai criteri.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERRORE \_ IPSEC \_ DOSP \_ NON \_ INSTALLATO**
</dt> <dd> <dl> <dt>

13931 (0x366B)
</dt> <dt>



La protezione DoS IPsec non è stata abilitata.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERRORE \_ \_ DOSP MAX IPSEC \_ PER CODE IP \_ \_ \_ RATELIMIT \_**
</dt> <dd> <dl> <dt>

13932 (0x366C)
</dt> <dt>



Protezione DoS IPsec non è riuscita a creare una coda per limite di frequenza IP interno perché è stato raggiunto il numero massimo di code consentite dai criteri.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**ERRORE \_ SEZIONE SXS \_ NON \_ \_ TROVATA**
</dt> <dd> <dl> <dt>

14000 (0x36B0)
</dt> <dt>



La sezione richiesta non era presente nel contesto di attivazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERRORE \_ SXS \_ CANT \_ GEN \_ ACTCTX**
</dt> <dd> <dl> <dt>

14001 (0x36B1)
</dt> <dt>



Impossibile avviare l'applicazione perché la configurazione side-by-side non è corretta. Per altri dettagli, vedere il registro eventi dell'applicazione o usare lo strumento sxstrace.exe riga di comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERRORE \_ SXS \_ FORMATO \_ ACTCTXDATA NON \_ VALIDO**
</dt> <dd> <dl> <dt>

14002 (0x36B2)
</dt> <dt>



Il formato dei dati di associazione dell'applicazione non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERRORE \_ ASSEMBLY SXS \_ NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

14003 (0x36B3)
</dt> <dt>



L'assembly a cui si fa riferimento non è installato nel sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**ERRORE \_ NEL FORMATO DEL MANIFESTO SXS \_ \_ \_**
</dt> <dd> <dl> <dt>

14004 (0x36B4)
</dt> <dt>



Il file manifesto non inizia con le informazioni necessarie sul tag e sul formato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**ERRORE \_ DI ANALISI MANIFESTO SXS \_ \_ \_**
</dt> <dd> <dl> <dt>

14005 (0x36B5)
</dt> <dt>



Il file manifesto contiene uno o più errori di sintassi.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**CONTESTO \_ DI ATTIVAZIONE SXS \_ DI ERRORE \_ \_ DISABILITATO**
</dt> <dd> <dl> <dt>

14006 (0x36B6)
</dt> <dt>



L'applicazione ha tentato di attivare un contesto di attivazione disabilitato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**ERRORE \_ CHIAVE SXS \_ NON \_ \_ TROVATA**
</dt> <dd> <dl> <dt>

14007 (0x36B7)
</dt> <dt>



La chiave di ricerca richiesta non è stata trovata in alcun contesto di attivazione attivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**ERRORE \_ CONFLITTO DI VERSIONE SXS \_ \_**
</dt> <dd> <dl> <dt>

14008 (0x36B8)
</dt> <dt>



Una versione del componente richiesta dall'applicazione è in conflitto con un'altra versione del componente già attiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERRORE \_ SXS \_ TIPO DI SEZIONE \_ \_ ERRATO**
</dt> <dd> <dl> <dt>

14009 (0x36B9)
</dt> <dt>



La sezione del contesto di attivazione del tipo richiesto non corrisponde all'API di query usata.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**QUERY \_ DI THREAD SXS \_ DI ERRORE \_ \_ DISABILITATE**
</dt> <dd> <dl> <dt>

14010 (0x36BA)
</dt> <dt>



La mancanza di risorse di sistema richiede la disabilitazione dell'attivazione isolata per il thread di esecuzione corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**IMPOSTAZIONE \_ PREDEFINITA DEL PROCESSO SXS DI ERRORE GIÀ \_ \_ \_ \_ IMPOSTATA**
</dt> <dd> <dl> <dt>

14011 (0x36BB)
</dt> <dt>



Il tentativo di impostare il contesto di attivazione predefinito del processo non è riuscito perché il contesto di attivazione predefinito del processo è già stato impostato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERRORE \_ GRUPPO DI CODIFICA SXS \_ \_ \_ SCONOSCIUTO**
</dt> <dd> <dl> <dt>

14012 (0x36BC)
</dt> <dt>



L'identificatore del gruppo di codifica specificato non è riconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERRORE \_ DI CODIFICA SXS \_ \_ SCONOSCIUTA**
</dt> <dd> <dl> <dt>

14013 (0x36BD)
</dt> <dt>



La codifica richiesta non è riconosciuta.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERRORE \_ SXS \_ URI DELLO SPAZIO DEI NOMI XML NON \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

14014 (0x36BE)
</dt> <dt>



Il manifesto contiene un riferimento a un URI non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**DIPENDENZA \_ DEL MANIFESTO RADICE SXS NON \_ \_ \_ \_ \_ INSTALLATA**
</dt> <dd> <dl> <dt>

14015 (0x36BF)
</dt> <dt>



Il manifesto dell'applicazione contiene un riferimento a un assembly dipendente che non è installato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**DIPENDENZA \_ DEL MANIFESTO FOGLIA SXS NON \_ \_ \_ \_ \_ INSTALLATA**
</dt> <dd> <dl> <dt>

14016 (0x36C0)
</dt> <dt>



Il manifesto per un assembly utilizzato dall'applicazione ha un riferimento a un assembly dipendente che non è installato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERRORE \_ SXS \_ ATTRIBUTO DI IDENTITÀ \_ \_ DELL'ASSEMBLY \_ NON VALIDO**
</dt> <dd> <dl> <dt>

14017 (0x36C1)
</dt> <dt>



Il manifesto contiene un attributo per l'identità dell'assembly non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**MANIFESTO \_ SXS ERRORE \_ \_ MANCANTE SPAZIO DEI NOMI PREDEFINITO \_ \_ \_ OBBLIGATORIO**
</dt> <dd> <dl> <dt>

14018 (0x36C2)
</dt> <dt>



Nel manifesto manca la specifica dello spazio dei nomi predefinita necessaria nell'elemento assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERRORE \_ MANIFESTO SXS \_ NON VALIDO SPAZIO DEI NOMI PREDEFINITO \_ \_ \_ \_ OBBLIGATORIO**
</dt> <dd> <dl> <dt>

14019 (0x36C3)
</dt> <dt>



Il manifesto ha uno spazio dei nomi predefinito specificato nell'elemento assembly, ma il relativo valore non è "urn:schemas-microsoft-com:asm.v1".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERRORE SXS PRIVATE MANIFEST CROSS PATH WITH REPARSE POINT (PERCORSO INCROCIATO DEL MANIFESTO PRIVATO \_ SXS \_ \_ CON \_ \_ \_ \_ REPARSE \_ POINT)**
</dt> <dd> <dl> <dt>

14020 (0x36C4)
</dt> <dt>



Il manifesto privato probed ha incrociato un percorso con un reparse point non supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERRORE \_ NOME DLL \_ DUPLICATO SXS \_ \_**
</dt> <dd> <dl> <dt>

14021 (0x36C5)
</dt> <dt>



Due o più componenti a cui fa riferimento direttamente o indirettamente il manifesto dell'applicazione hanno file con lo stesso nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERRORE \_ SXS \_ DUPLICATE \_ WINDOWCLASS \_ NAME**
</dt> <dd> <dl> <dt>

14022 (0x36C6)
</dt> <dt>



Due o più componenti a cui fa riferimento direttamente o indirettamente il manifesto dell'applicazione hanno classi finestra con lo stesso nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**ERRORE \_ SXS \_ DUPLICATE \_ CLSID**
</dt> <dd> <dl> <dt>

14023 (0x36C7)
</dt> <dt>



Due o più componenti a cui fa riferimento direttamente o indirettamente il manifesto dell'applicazione hanno gli stessi CLSID del server COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**ERRORE \_ SXS \_ DUPLICATE \_ IID**
</dt> <dd> <dl> <dt>

14024 (0x36C8)
</dt> <dt>



Due o più componenti a cui fa riferimento direttamente o indirettamente il manifesto dell'applicazione hanno proxy per gli stessi ID di interfaccia COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERRORE \_ SXS \_ DUPLICATE \_ TLBID**
</dt> <dd> <dl> <dt>

14025 (0x36C9)
</dt> <dt>



Due o più componenti a cui fa riferimento direttamente o indirettamente il manifesto dell'applicazione hanno gli stessi TLBID della libreria dei tipi COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**PROGID \_ DUPLICATO SXS \_ \_ ERRORE**
</dt> <dd> <dl> <dt>

14026 (0x36CA)
</dt> <dt>



Due o più componenti a cui fa riferimento direttamente o indirettamente il manifesto dell'applicazione hanno gli stessi ProgID COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERRORE \_ SXS \_ NOME ASSEMBLY \_ \_ DUPLICATO**
</dt> <dd> <dl> <dt>

14027 (0x36CB)
</dt> <dt>



Due o più componenti a cui fa riferimento direttamente o indirettamente il manifesto dell'applicazione sono versioni diverse dello stesso componente che non sono consentite.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERRORE \_ DI MANCATA \_ CORRISPONDENZA DELL'HASH DEL FILE \_ SXS \_**
</dt> <dd> <dl> <dt>

14028 (0x36CC)
</dt> <dt>



Il file di un componente non corrisponde alle informazioni di verifica presenti nel manifesto del componente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**ERRORE \_ DI ANALISI DEI CRITERI SXS \_ \_ \_**
</dt> <dd> <dl> <dt>

14029 (0x36CD)
</dt> <dt>



Il manifesto dei criteri contiene uno o più errori di sintassi.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERRORE \_ SXS \_ XML E \_ \_ MISSINGQUOTE**
</dt> <dd> <dl> <dt>

14030 (0x36CE)
</dt> <dt>



Errore di analisi manifesto: era previsto un valore letterale stringa, ma non è stato trovato alcun carattere virgolette di apertura.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERRORE \_ SXS \_ XML E \_ \_ COMMENTSYNTAX**
</dt> <dd> <dl> <dt>

14031 (0x36CF)
</dt> <dt>



Errore di analisi manifesto: è stata usata una sintassi non corretta in un commento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERRORE \_ SXS \_ XML E \_ \_ BADSTARTNAMECHAR**
</dt> <dd> <dl> <dt>

14032 (0x36D0)
</dt> <dt>



Errore di analisi manifesto: un nome è stato avviato con un carattere non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERRORE \_ SXS \_ XML E \_ \_ BADNAMECHAR**
</dt> <dd> <dl> <dt>

14033 (0x36D1)
</dt> <dt>



Errore di analisi manifesto: un nome contiene un carattere non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERRORE \_ SXS \_ XML E \_ \_ BADCHARINSTRING**
</dt> <dd> <dl> <dt>

14034 (0x36D2)
</dt> <dt>



Errore di analisi manifesto: un valore letterale stringa contiene un carattere non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERRORE \_ SXS \_ XML E \_ \_ XMLDECLSYNTAX**
</dt> <dd> <dl> <dt>

14035 (0x36D3)
</dt> <dt>



Errore di analisi manifesto: sintassi non valida per una dichiarazione XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERRORE \_ SXS \_ XML E \_ \_ BADCHARDATA**
</dt> <dd> <dl> <dt>

14036 (0x36D4)
</dt> <dt>



Errore di analisi manifesto: è stato trovato un carattere non valido nel contenuto di testo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERRORE \_ SXS \_ XML E \_ \_ MISSINGWHITESPACE**
</dt> <dd> <dl> <dt>

14037 (0x36D5)
</dt> <dt>



Errore di analisi manifesto: spazio vuoto richiesto mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERRORE \_ SXS \_ XML E \_ \_ EXPECTINGTAGEND**
</dt> <dd> <dl> <dt>

14038 (0x36D6)
</dt> <dt>



Errore di analisi manifesto: previsto il carattere '>'.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERRORE \_ SXS \_ XML E \_ \_ MISSINGSEMICOLON**
</dt> <dd> <dl> <dt>

14039 (0x36D7)
</dt> <dt>



Errore di analisi manifesto: è previsto un carattere punto e virgola.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERRORE \_ SXS \_ XML E \_ \_ UNBALANCEDPAREN**
</dt> <dd> <dl> <dt>

14040 (0x36D8)
</dt> <dt>



Errore di analisi manifesto: parentesi non bilanciate.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERRORE \_ SXS \_ XML E \_ \_ INTERNALERROR**
</dt> <dd> <dl> <dt>

14041 (0x36D9)
</dt> <dt>



Errore di analisi manifesto: errore interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERRORE \_ SXS \_ XML E SPAZIO VUOTO \_ \_ \_ IMPREVISTO**
</dt> <dd> <dl> <dt>

14042 (0x36DA)
</dt> <dt>



Errore di analisi manifesto: lo spazio vuoto non è consentito in questa posizione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERRORE \_ SXS \_ XML E CODIFICA \_ \_ INCOMPLETA \_**
</dt> <dd> <dl> <dt>

14043 (0x36DB)
</dt> <dt>



Errore di analisi manifesto: fine del file raggiunta in stato non valido per la codifica corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERRORE \_ SXS \_ XML E \_ \_ \_ PAREN MANCANTE**
</dt> <dd> <dl> <dt>

14044 (0x36DC)
</dt> <dt>



Errore di analisi manifesto: parentesi mancanti.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERRORE \_ SXS \_ XML E \_ \_ EXPECTINGCLOSEQUOTE**
</dt> <dd> <dl> <dt>

14045 (0x36DD)
</dt> <dt>



Errore di analisi manifesto: manca un carattere virgolette di chiusura singolo o doppio ( \\ ' \\ o ").


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERRORE \_ SXS \_ XML E PIÙ DUE \_ \_ \_ PUNTI**
</dt> <dd> <dl> <dt>

14046 (0x36DE)
</dt> <dt>



Errore di analisi manifesto: non sono consentiti più due punti in un nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERRORE \_ SXS \_ XML E \_ \_ DECIMALE NON \_ VALIDO**
</dt> <dd> <dl> <dt>

14047 (0x36DF)
</dt> <dt>



Errore di analisi manifesto: carattere non valido per la cifra decimale.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERRORE \_ SXS \_ XML E \_ \_ \_ ESADECIMALE NON VALIDO**
</dt> <dd> <dl> <dt>

14048 (0x36E0)
</dt> <dt>



Errore di analisi manifesto: carattere non valido per la cifra esadecimale.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERRORE \_ SXS \_ XML E UNICODE NON \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

14049 (0x36E1)
</dt> <dt>



Errore di analisi manifesto: valore di carattere Unicode non valido per questa piattaforma.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERRORE \_ SXS \_ XML E \_ \_ WHITESPACEORQUESTIONMARK**
</dt> <dd> <dl> <dt>

14050 (0x36E2)
</dt> <dt>



Errore di analisi manifesto: previsto spazio vuoto o '?'.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERRORE \_ SXS \_ XML E \_ \_ UNEXPECTEDENDTAG**
</dt> <dd> <dl> <dt>

14051 (0x36E3)
</dt> <dt>



Errore di analisi manifesto: tag di fine non previsto in questo percorso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERRORE \_ SXS \_ XML E \_ \_ UNCLOSEDTAG**
</dt> <dd> <dl> <dt>

14052 (0x36E4)
</dt> <dt>



Errore di analisi manifesto: i tag seguenti non sono stati chiusi: %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERRORE \_ SXS \_ XML E \_ \_ DUPLICATEATTRIBUTE**
</dt> <dd> <dl> <dt>

14053 (0x36E5)
</dt> <dt>



Errore di analisi manifesto: attributo duplicato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERRORE \_ SXS \_ XML E \_ \_ MULTIPLEROOTS**
</dt> <dd> <dl> <dt>

14054 (0x36E6)
</dt> <dt>



Errore di analisi manifesto: è consentito un solo elemento di primo livello in un documento XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERRORE \_ SXS \_ XML E \_ \_ INVALIDATROOTLEVEL**
</dt> <dd> <dl> <dt>

14055 (0x36E7)
</dt> <dt>



Errore di analisi manifesto: non valido al livello superiore del documento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERRORE \_ SXS \_ XML E \_ \_ BADXMLDECL**
</dt> <dd> <dl> <dt>

14056 (0x36E8)
</dt> <dt>



Errore di analisi manifesto: dichiarazione xml non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERRORE \_ SXS \_ XML E \_ \_ MISSINGROOT**
</dt> <dd> <dl> <dt>

14057 (0x36E9)
</dt> <dt>



Errore di analisi manifesto: il documento XML deve avere un elemento di primo livello.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERRORE \_ SXS \_ XML E \_ \_ UNEXPECTEDEOF**
</dt> <dd> <dl> <dt>

14058 (0x36EA)
</dt> <dt>



Errore di analisi manifesto: fine del file imprevista.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERRORE \_ SXS \_ XML E \_ \_ BADPEREFINSUBSET**
</dt> <dd> <dl> <dt>

14059 (0x36EB)
</dt> <dt>



Errore di analisi manifesto: le entità parametro non possono essere usate all'interno di dichiarazioni di markup in un subset interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERRORE \_ SXS \_ XML E \_ \_ UNCLOSEDSTARTTAG**
</dt> <dd> <dl> <dt>

14060 (0x36EC)
</dt> <dt>



Errore di analisi manifesto: l'elemento non è stato chiuso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERRORE \_ SXS \_ XML E \_ \_ UNCLOSEDENDTAG**
</dt> <dd> <dl> <dt>

14061 (0x36ED)
</dt> <dt>



Errore di analisi manifesto: nell'elemento end manca il carattere '>'.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERRORE \_ SXS \_ XML E \_ \_ UNCLOSEDSTRING**
</dt> <dd> <dl> <dt>

14062 (0x36EE)
</dt> <dt>



Errore di analisi manifesto: un valore letterale stringa non è stato chiuso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERRORE \_ SXS \_ XML E \_ \_ UNCLOSEDCOMMENT**
</dt> <dd> <dl> <dt>

14063 (0x36EF)
</dt> <dt>



Errore di analisi manifesto: un commento non è stato chiuso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERRORE \_ SXS \_ XML E \_ \_ UNCLOSEDDECL**
</dt> <dd> <dl> <dt>

14064 (0x36F0)
</dt> <dt>



Errore di analisi manifesto: una dichiarazione non è stata chiusa.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERRORE \_ SXS \_ XML E \_ \_ UNCLOSEDCDATA**
</dt> <dd> <dl> <dt>

14065 (0x36F1)
</dt> <dt>



Errore di analisi manifesto: una sezione CDATA non è stata chiusa.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERRORE \_ SXS \_ XML E \_ \_ RESERVEDNAMESPACE**
</dt> <dd> <dl> <dt>

14066 (0x36F2)
</dt> <dt>



Errore di analisi manifesto: il prefisso dello spazio dei nomi non può iniziare con la stringa riservata "xml".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERRORE \_ SXS \_ XML E \_ \_ INVALIDENCODING**
</dt> <dd> <dl> <dt>

14067 (0x36F3)
</dt> <dt>



Errore di analisi manifesto: il sistema non supporta la codifica specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERRORE \_ SXS \_ XML E \_ \_ INVALIDSWITCH**
</dt> <dd> <dl> <dt>

14068 (0x36F4)
</dt> <dt>



Errore di analisi manifesto: passaggio dalla codifica corrente alla codifica specificata non supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERRORE \_ SXS \_ XML E \_ \_ BADXMLCASE**
</dt> <dd> <dl> <dt>

14069 (0x36F5)
</dt> <dt>



Errore di analisi manifesto: il nome 'xml' è riservato e deve essere minuscolo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERRORE \_ SXS \_ XML E \_ \_ \_ STANDALONE NON VALIDO**
</dt> <dd> <dl> <dt>

14070 (0x36F6)
</dt> <dt>



Errore di analisi manifesto: l'attributo autonomo deve avere il valore 'yes' o 'no'.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERRORE \_ SXS \_ XML E UNEXPECTED \_ \_ \_ STANDALONE**
</dt> <dd> <dl> <dt>

14071 (0x36F7)
</dt> <dt>



Errore di analisi manifesto: l'attributo autonomo non può essere usato in entità esterne.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERRORE \_ SXS \_ XML E VERSIONE NON \_ \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

14072 (0x36F8)
</dt> <dt>



Errore di analisi manifesto: numero di versione non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERRORE \_ SXS \_ XML E \_ \_ MISSINGEQUALS**
</dt> <dd> <dl> <dt>

14073 (0x36F9)
</dt> <dt>



Errore di analisi manifesto: segno di uguale mancante tra l'attributo e il valore dell'attributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**ERRORE \_ DI RIPRISTINO DELLA PROTEZIONE SXS NON \_ \_ \_ RIUSCITO**
</dt> <dd> <dl> <dt>

14074 (0x36FA)
</dt> <dt>



Errore di Protezione assembly: impossibile recuperare l'assembly specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**ERRORE \_ CHIAVE PUBBLICA DI PROTEZIONE SXS TROPPO \_ \_ \_ \_ \_ BREVE**
</dt> <dd> <dl> <dt>

14075 (0x36FB)
</dt> <dt>



Errore di protezione assembly: la chiave pubblica per un assembly era troppo breve per essere consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERRORE \_ DEL CATALOGO DI PROTEZIONE SXS NON \_ \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

14076 (0x36FC)
</dt> <dt>



Errore di protezione dell'assembly: il catalogo per un assembly non è valido o non corrisponde al manifesto dell'assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERRORE \_ SXS \_ HRESULT NON \_ TRADUCIBILE**
</dt> <dd> <dl> <dt>

14077 (0x36FD)
</dt> <dt>



Impossibile convertire un HRESULT in un codice di errore Win32 corrispondente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**ERRORE \_ FILE DEL CATALOGO DI PROTEZIONE SXS \_ \_ \_ \_ MANCANTE**
</dt> <dd> <dl> <dt>

14078 (0x36FE)
</dt> <dt>



Errore di protezione assembly: il catalogo per un assembly è mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**ERRORE \_ SXS \_ ATTRIBUTO DI IDENTITÀ \_ \_ DELL'ASSEMBLY \_ MANCANTE**
</dt> <dd> <dl> <dt>

14079 (0x36FF)
</dt> <dt>



Nell'identità dell'assembly fornita mancano uno o più attributi che devono essere presenti in questo contesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERRORE \_ SXS NOME ATTRIBUTO DI IDENTITÀ ASSEMBLY NON \_ \_ \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

14080 (0x3700)
</dt> <dt>



L'identità dell'assembly fornita ha uno o più nomi di attributo che contengono caratteri non consentiti nei nomi XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERRORE \_ DELL'ASSEMBLY SXS \_ \_ MANCANTE**
</dt> <dd> <dl> <dt>

14081 (0x3701)
</dt> <dt>



Impossibile trovare l'assembly a cui si fa riferimento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**ERRORE \_ SXS \_ STACK DI ATTIVAZIONE \_ \_ DANNEGGIATO**
</dt> <dd> <dl> <dt>

14082 (0x3702)
</dt> <dt>



Lo stack di attivazione del contesto di attivazione per il thread di esecuzione in esecuzione è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**ERRORE \_ SXS \_ CORRUPTION**
</dt> <dd> <dl> <dt>

14083 (0x3703)
</dt> <dt>



I metadati di isolamento dell'applicazione per questo processo o thread sono danneggiati.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**DISATTIVAZIONE \_ ANTICIPATA DI SXS \_ DI \_ ERRORE**
</dt> <dd> <dl> <dt>

14084 (0x3704)
</dt> <dt>



Il contesto di attivazione disattivato non è quello attivato più di recente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**DISATTIVAZIONE \_ SXS \_ NON VALIDA \_ DELL'ERRORE**
</dt> <dd> <dl> <dt>

14085 (0x3705)
</dt> <dt>



Il contesto di attivazione disattivato non è attivo per il thread di esecuzione corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERRORE \_ SXS \_ PIÙ \_ DISATTIVAZIONE**
</dt> <dd> <dl> <dt>

14086 (0x3706)
</dt> <dt>



Il contesto di attivazione in fase di disattivazione è già stato disattivato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**RICHIESTA \_ TERMINAZIONE DEL PROCESSO SXS \_ DI \_ \_ ERRORE**
</dt> <dd> <dl> <dt>

14087 (0x3707)
</dt> <dt>



Un componente usato dalla funzionalità di isolamento ha richiesto di terminare il processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**CONTESTO DI \_ ATTIVAZIONE DELLA VERSIONE SXS \_ DI \_ \_ ERRORE**
</dt> <dd> <dl> <dt>

14088 (0x3708)
</dt> <dt>



Un componente in modalità kernel rilascia un riferimento in un contesto di attivazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**CONTESTO \_ DI ATTIVAZIONE PREDEFINITO DEL SISTEMA SXS \_ \_ \_ \_ VUOTO \_**
</dt> <dd> <dl> <dt>

14089 (0x3709)
</dt> <dt>



Impossibile generare il contesto di attivazione dell'assembly predefinito del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERRORE \_ SXS \_ VALORE \_ DELL'ATTRIBUTO IDENTITY NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

14090 (0x370A)
</dt> <dt>



Il valore di un attributo in un'identità non è compreso nell'intervallo valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERRORE \_ SXS \_ NOME ATTRIBUTO IDENTITY NON \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

14091 (0x370B)
</dt> <dt>



Il nome di un attributo in un'identità non è compreso nell'intervallo valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**ERRORE \_ SXS \_ IDENTITY DUPLICATE \_ \_ ATTRIBUTE**
</dt> <dd> <dl> <dt>

14092 (0x370C)
</dt> <dt>



Un'identità contiene due definizioni per lo stesso attributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**ERRORE \_ SXS \_ IDENTITY PARSE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

14093 (0x370D)
</dt> <dt>



Il formato della stringa di identità non è corretto. Ciò può essere dovuto a una virgola finale, a più di due attributi senza nome, al nome dell'attributo mancante o al valore dell'attributo mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERRORE \_ STRINGA DI SOSTITUZIONE NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

14094 (0x370E)
</dt> <dt>



Il formato di una stringa contenente contenuto sostituibile localizzato non è corretto. Il simbolo del dollaro ($) è stato seguito da un valore diverso da una parentesi sinistra o da un altro simbolo di dollaro oppure la parentesi destra di una sostituzione non è stata trovata.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERRORE \_ SXS \_ TOKEN DI CHIAVE PUBBLICA NON \_ \_ \_ CORRETTO**
</dt> <dd> <dl> <dt>

14095 (0x370F)
</dt> <dt>



Il token di chiave pubblica non corrisponde alla chiave pubblica specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**ERRORE- \_ STRINGA DI SOSTITUZIONE NON \_ \_ MAPPATA**
</dt> <dd> <dl> <dt>

14096 (0x3710)
</dt> <dt>



Una stringa di sostituzione non ha alcun mapping.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERRORE \_ DELL'ASSEMBLY SXS \_ \_ NON \_ BLOCCATO**
</dt> <dd> <dl> <dt>

14097 (0x3711)
</dt> <dt>



Il componente deve essere bloccato prima di effettuare la richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERRORE \_ DELL'ARCHIVIO COMPONENTI SXS \_ \_ \_ DANNEGGIATO**
</dt> <dd> <dl> <dt>

14098 (0x3712)
</dt> <dt>



L'archivio componenti è stato danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERRORE \_ PROGRAMMA DI INSTALLAZIONE AVANZATA NON \_ \_ RIUSCITO**
</dt> <dd> <dl> <dt>

14099 (0x3713)
</dt> <dt>



Un programma di installazione avanzato non è riuscito durante l'installazione o la manutenzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**ERRORE \_ DI \_ MANCATA CORRISPONDENZA DELLA CODIFICA XML \_**
</dt> <dd> <dl> <dt>

14100 (0x3714)
</dt> <dt>



La codifica dei caratteri nella dichiarazione XML non corrisponde alla codifica usata nel documento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**ERRORE \_ SXS \_ MANIFEST IDENTITY SAME BUT CONTENTS \_ \_ \_ \_ \_ DIFFERENT**
</dt> <dd> <dl> <dt>

14101 (0x3715)
</dt> <dt>



Le identità dei manifesti sono identiche, ma il relativo contenuto è diverso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**IDENTITÀ \_ SXS \_ DI ERRORE \_ DIVERSE**
</dt> <dd> <dl> <dt>

14102 (0x3716)
</dt> <dt>



Le identità dei componenti sono diverse.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**\_L'ASSEMBLY SXS \_ DI ERRORE NON È UNA \_ \_ \_ \_ DISTRIBUZIONE**
</dt> <dd> <dl> <dt>

14103 (0x3717)
</dt> <dt>



L'assembly non è una distribuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**FILE \_ SXS \_ DI ERRORE CHE NON FA PARTE \_ \_ \_ \_ DELL'ASSEMBLY**
</dt> <dd> <dl> <dt>

14104 (0x3718)
</dt> <dt>



Il file non fa parte dell'assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**MANIFESTO \_ SXS \_ DI ERRORE TROPPO \_ \_ GRANDE**
</dt> <dd> <dl> <dt>

14105 (0x3719)
</dt> <dt>



Le dimensioni del manifesto superano il valore massimo consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**IMPOSTAZIONE \_ SXS \_ DI ERRORE NON \_ \_ REGISTRATA**
</dt> <dd> <dl> <dt>

14106 (0x371A)
</dt> <dt>



L'impostazione non è registrata.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERRORE \_ DI CHIUSURA DELLA TRANSAZIONE SXS \_ \_ \_ INCOMPLETA**
</dt> <dd> <dl> <dt>

14107 (0x371B)
</dt> <dt>



Uno o più membri obbligatori della transazione non sono presenti.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERRORE \_ DEL PROGRAMMA DI INSTALLAZIONE PRIMITIVA SMI \_ NON \_ \_ RIUSCITO**
</dt> <dd> <dl> <dt>

14108 (0x371C)
</dt> <dt>



Il programma di installazione della primitiva SMI non è riuscito durante l'installazione o la manutenzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**ERRORE \_ COMANDO GENERICO NON \_ \_ RIUSCITO**
</dt> <dd> <dl> <dt>

14109 (0x371D)
</dt> <dt>



Un eseguibile di comando generico ha restituito un risultato che indica un errore.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**ERRORE \_ HASH FILE SXS \_ \_ \_ MANCANTE**
</dt> <dd> <dl> <dt>

14110 (0x371E)
</dt> <dt>



Un componente non contiene informazioni di verifica file nel manifesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERRORE \_ EVT \_ PERCORSO CANALE NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

15000 (0x3A98)
</dt> <dt>



Il percorso del canale specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERRORE \_ EVT \_ QUERY NON \_ VALIDA**
</dt> <dd> <dl> <dt>

15001 (0x3A99)
</dt> <dt>



La query specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERRORE \_ DEI METADATI DEL SERVER DI PUBBLICAZIONE EVT \_ NON \_ \_ \_ TROVATI**
</dt> <dd> <dl> <dt>

15002 (0x3A9A)
</dt> <dt>



Impossibile trovare i metadati dell'editore nella risorsa.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERRORE \_ DEL MODELLO DI EVENTO EVT NON \_ \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

15003 (0x3A9B)
</dt> <dt>



Impossibile trovare il modello per una definizione di evento nella risorsa (errore = %1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERRORE \_ EVT \_ NOME SERVER DI PUBBLICAZIONE NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

15004 (0x3A9C)
</dt> <dt>



Il nome del server di pubblicazione specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERRORE \_ EVT \_ DATI DI EVENTO NON \_ \_ VALIDI**
</dt> <dd> <dl> <dt>

15005 (0x3A9D)
</dt> <dt>



I dati degli eventi generati dal server di pubblicazione non sono compatibili con la definizione del modello di evento nel manifesto dell'editore.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERRORE \_ CANALE EVT \_ NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

15007 (0x3A9F)
</dt> <dt>



Impossibile trovare il canale specificato. Controllare la configurazione del canale.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERRORE \_ EVT \_ TESTO XML IN FORMATO NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

15008 (0x3AA0)
</dt> <dt>



Il formato del testo XML specificato non è corretto. Per altri dettagli, vedere Errore esteso.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERRORE \_ DELLA SOTTOSCRIZIONE EVT \_ AL CANALE \_ \_ \_ DIRETTO**
</dt> <dd> <dl> <dt>

15009 (0x3AA1)
</dt> <dt>



Il chiamante sta tentando di sottoscrivere un canale diretto che non è consentito. Gli eventi per un canale diretto passano direttamente a un file di log e non possono essere sottoscritti.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**ERRORE \_ DI CONFIGURAZIONE EVT \_ \_**
</dt> <dd> <dl> <dt>

15010 (0x3AA2)
</dt> <dt>



Errore di configurazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERRORE \_ EVT \_ QUERY RESULT \_ \_ STALE**
</dt> <dd> <dl> <dt>

15011 (0x3AA3)
</dt> <dt>



Il risultato della query non è valido o non è valido. Ciò può essere dovuto alla ripulita o al roll over del log dopo la creazione del risultato della query. Gli utenti devono gestire questo codice rilasciando l'oggetto risultato della query e riemettendo la query.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERRORE EVT QUERY RESULT INVALID POSITION (POSIZIONE NON VALIDA DEL RISULTATO \_ DELLA QUERY EVT) \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

15012 (0x3AA4)
</dt> <dt>



Il risultato della query è attualmente in una posizione non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERRORE \_ EVT \_ NON CONVALIDA \_ MSXML \_**
</dt> <dd> <dl> <dt>

15013 (0x3AA5)
</dt> <dt>



Le MSXML non supportano la convalida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**FILTRO \_ EVT \_ ERROR \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014 (0x3AA6)
</dt> <dt>



Un'espressione può essere seguita da un'operazione di modifica dell'ambito solo se restituisce un set di nodi e non fa già parte di un'altra operazione di modifica dell'ambito.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERRORE \_ EVT \_ FILTER \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015 (0x3AA7)
</dt> <dt>



Non è possibile eseguire un'operazione di passaggio da un termine che non rappresenta un set di elementi.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERRORE \_ EVT \_ FILTER \_ INVARG**
</dt> <dd> <dl> <dt>

15016 (0x3AA8)
</dt> <dt>



Gli argomenti sul lato sinistro per gli operatori binari devono essere attributi, nodi o variabili e gli argomenti sul lato destro devono essere costanti.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERRORE \_ EVT \_ FILTER \_ INVTEST**
</dt> <dd> <dl> <dt>

15017 (0x3AA9)
</dt> <dt>



Un'operazione di passaggio deve includere un test del nodo o, nel caso di un predicato, può essere valutata un'espressione algebrica in base alla quale testare ogni nodo nel set di nodi identificato dal set di nodi precedente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERRORE \_ EVT \_ FILTER \_ INVTYPE**
</dt> <dd> <dl> <dt>

15018 (0x3AAA)
</dt> <dt>



Questo tipo di dati non è attualmente supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERRORE \_ EVT \_ FILTER \_ PARSEERR**
</dt> <dd> <dl> <dt>

15019 (0x3AAB)
</dt> <dt>



Si è verificato un errore di sintassi nella posizione %1!d!.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERRORE \_ EVT \_ FILTER \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020 (0x3AAC)
</dt> <dt>



Questo operatore non è supportato da questa implementazione del filtro.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERRORE \_ EVT \_ FILTER \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021 (0x3AAD)
</dt> <dt>



Il token rilevato è imprevisto.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERRORE \_ EVT \_ OPERAZIONE NON VALIDA SU CANALE DIRETTO \_ \_ \_ \_ \_ ABILITATO**
</dt> <dd> <dl> <dt>

15022 (0x3AAE)
</dt> <dt>



L'operazione richiesta non può essere eseguita su un canale diretto abilitato. Il canale deve essere prima disabilitato prima di eseguire l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERRORE \_ EVT \_ VALORE DELLA PROPRIETÀ DEL CANALE NON \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

15023 (0x3AAF)
</dt> <dt>



Proprietà canale %1!s! contiene un valore non valido. Il valore ha un tipo non valido, non è compreso nell'intervallo valido, non può essere aggiornato o non è supportato da questo tipo di canale.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERRORE \_ EVT \_ VALORE DELLA PROPRIETÀ PUBLISHER NON \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

15024 (0x3AB0)
</dt> <dt>



Publisher proprietà %1!s! contiene un valore non valido. Il valore ha un tipo non valido, non è compreso nell'intervallo valido, non può essere aggiornato o non è supportato da questo tipo di server di pubblicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERRORE \_ DURANTE L'ATTIVAZIONE DEL CANALE EVT \_ \_ \_**
</dt> <dd> <dl> <dt>

15025 (0x3AB1)
</dt> <dt>



L'attivazione del canale non riesce.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERRORE \_ FILTRO EVT \_ TROPPO \_ \_ COMPLESSO**
</dt> <dd> <dl> <dt>

15026 (0x3AB2)
</dt> <dt>



L'espressione xpath ha superato la complessità supportata. Semplificarla o dividerla in due o più espressioni semplici.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**MESSAGGIO \_ DI ERRORE EVT \_ NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

15027 (0x3AB3)
</dt> <dt>



la risorsa messaggio è presente, ma il messaggio non viene trovato nella tabella di stringhe/messaggi.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERRORE \_ ID MESSAGGIO EVT \_ NON \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

15028 (0x3AB4)
</dt> <dt>



Impossibile trovare l'ID del messaggio desiderato.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERRORE \_ EVT \_ UNRESOLVED \_ VALUE \_ INSERT**
</dt> <dd> <dl> <dt>

15029 (0x3AB5)
</dt> <dt>



Impossibile trovare la stringa di sostituzione per l'indice di inserimento (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERRORE \_ EVT \_ UNRESOLVED \_ PARAMETER \_ INSERT**
</dt> <dd> <dl> <dt>

15030 (0x3AB6)
</dt> <dt>



Impossibile trovare la stringa di descrizione per il riferimento al parametro (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERRORE \_ DURANTE IL NUMERO MASSIMO DI \_ \_ INSERIMENTI \_ RAGGIUNTO**
</dt> <dd> <dl> <dt>

15031 (0x3AB7)
</dt> <dt>



È stato raggiunto il numero massimo di sostituzioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERRORE \_ NELLA DEFINIZIONE \_ \_ DELL'EVENTO EVT \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

15032 (0x3AB8)
</dt> <dt>



Impossibile trovare la definizione dell'evento per l'ID evento (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERRORE \_ IMPOSTAZIONI LOCALI DEL MESSAGGIO \_ \_ EVT NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

15033 (0x3AB9)
</dt> <dt>



La risorsa specifica delle impostazioni locali per il messaggio desiderato non è presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERRORE \_ VERSIONE EVT \_ TROPPO \_ \_ VECCHIA**
</dt> <dd> <dl> <dt>

15034 (0x3ABA)
</dt> <dt>



La risorsa è troppo vecchia per essere compatibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERRORE \_ VERSIONE EVT \_ TROPPO \_ \_ NUOVA**
</dt> <dd> <dl> <dt>

15035 (0x3ABB)
</dt> <dt>



La risorsa è troppo nuova per essere compatibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERRORE \_ EVT: \_ IMPOSSIBILE APRIRE IL CANALE DELLA \_ \_ \_ \_ QUERY**
</dt> <dd> <dl> <dt>

15036 (0x3ABC)
</dt> <dt>



Il canale in corrispondenza dell'indice %1!d! della query non può essere aperta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERRORE \_ EVT \_ PUBLISHER \_ DISABLED**
</dt> <dd> <dl> <dt>

15037 (0x3ABD)
</dt> <dt>



Il server di pubblicazione è stato disabilitato e la relativa risorsa non è disponibile. Ciò si verifica in genere quando il server di pubblicazione è in fase di disinstallazione o aggiornamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERRORE \_ FILTRO EVT \_ NON COMPRESO \_ \_ \_ NELL'INTERVALLO**
</dt> <dd> <dl> <dt>

15038 (0x3ABE)
</dt> <dt>



Si è tentato di creare un tipo numerico non compreso nell'intervallo valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERRORE \_ EC SUBSCRIPTION CANNOT \_ \_ \_ ACTIVATE**
</dt> <dd> <dl> <dt>

15080 (0x3AE8)
</dt> <dt>



L'attivazione della sottoscrizione non riesce.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERRORE \_ EC \_ LOG \_ DISABLED**
</dt> <dd> <dl> <dt>

15081 (0x3AE9)
</dt> <dt>



Il log della sottoscrizione è disabilitato e non può essere usato per inoltrare eventi a . Prima di attivare la sottoscrizione, è necessario che il log sia abilitato.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERRORE \_ EC \_ CIRCULAR \_ FORWARDING**
</dt> <dd> <dl> <dt>

15082 (0x3AEA)
</dt> <dt>



Quando si inoltrano eventi dal computer locale a se stesso, la query della sottoscrizione non può contenere il log di destinazione della sottoscrizione.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERRORE \_ EC \_ CREDSTORE \_ FULL**
</dt> <dd> <dl> <dt>

15083 (0x3AEB)
</dt> <dt>



L'archivio credenziali usato per salvare le credenziali è pieno.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERRORE \_ EC \_ CRED NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

15084 (0x3AEC)
</dt> <dt>



Le credenziali usate da questa sottoscrizione non sono disponibili nell'archivio credenziali.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERRORE \_ EC NO ACTIVE \_ \_ \_ CHANNEL**
</dt> <dd> <dl> <dt>

15085 (0x3AED)
</dt> <dt>



Non è stato trovato alcun canale attivo per la query.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**ERRORE \_ FILE MUI \_ NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

15100 (0x3AFC)
</dt> <dt>



Il caricatore di risorse non è riuscito a trovare il file MUI.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERRORE \_ MUI \_ FILE NON \_ VALIDO**
</dt> <dd> <dl> <dt>

15101 (0x3AFD)
</dt> <dt>



Il caricatore di risorse non è riuscito a caricare il file MUI perché la convalida del file non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERRORE \_ MUI \_ INVALID \_ RC \_ CONFIG**
</dt> <dd> <dl> <dt>

15102 (0x3AFE)
</dt> <dt>



Il manifesto RC è danneggiato con dati di Garbage Collection o versione non supportata o elemento obbligatorio mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERRORE \_ MUI \_ NOME IMPOSTAZIONI LOCALI \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

15103 (0x3AFF)
</dt> <dt>



Il manifesto RC ha un nome di impostazioni cultura non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERRORE \_ MUI \_ INVALID \_ ULTIMATEFALLBACK \_ NAME**
</dt> <dd> <dl> <dt>

15104 (0x3B00)
</dt> <dt>



Il manifesto RC ha un nome ultimatefallback non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERRORE \_ FILE MUI \_ NON \_ \_ CARICATO**
</dt> <dd> <dl> <dt>

15105 (0x3B01)
</dt> <dt>



La cache del caricatore di risorse non ha caricato una voce MUI.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**ERRORE \_ RESOURCE \_ ENUM USER \_ \_ STOP**
</dt> <dd> <dl> <dt>

15106 (0x3B02)
</dt> <dt>



L'utente ha arrestato l'enumerazione delle risorse.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERRORE \_ MUI \_ INTLSETTINGS \_ UILANG \_ NON \_ INSTALLATO**
</dt> <dd> <dl> <dt>

15107 (0x3B03)
</dt> <dt>



Installazione della lingua dell'interfaccia utente non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERRORE \_ \_ INTLSETTINGS MUI \_ NOME IMPOSTAZIONI LOCALI NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

15108 (0x3B04)
</dt> <dt>



Installazione delle impostazioni locali non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERRORE \_ MRM \_ RUNTIME NO DEFAULT OR NEUTRAL \_ \_ \_ \_ \_ RESOURCE**
</dt> <dd> <dl> <dt>

15110 (0x3B06)
</dt> <dt>



Una risorsa non ha un valore predefinito o neutro.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERRORE \_ MRM \_ NON VALIDO \_ PRICONFIG**
</dt> <dd> <dl> <dt>

15111 (0x3B07)
</dt> <dt>



File di configurazione PRI non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**ERRORE \_ MRM \_ TIPO DI FILE \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

15112 (0x3B08)
</dt> <dt>



Tipo di file non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERRORE \_ QUALIFICATORE MRM \_ \_ SCONOSCIUTO**
</dt> <dd> <dl> <dt>

15113 (0x3B09)
</dt> <dt>



Qualificatore sconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**ERRORE \_ MRM \_ : VALORE \_ QUALIFICATORE NON \_ VALIDO**
</dt> <dd> <dl> <dt>

15114 (0x3B0A)
</dt> <dt>



Valore del qualificatore non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERRORE \_ MRM \_ NO \_ CANDIDATE**
</dt> <dd> <dl> <dt>

15115 (0x3B0B)
</dt> <dt>



Nessun candidato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERRORE \_ MRM \_ NO MATCH OR DEFAULT \_ \_ \_ \_ CANDIDATE**
</dt> <dd> <dl> <dt>

15116 (0x3B0C)
</dt> <dt>



ResourceMap o NamedResource ha un elemento che non ha una risorsa predefinita o neutra.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**ERRORE \_ DI MANCATA \_ CORRISPONDENZA DEL TIPO DI \_ \_ RISORSA MRM**
</dt> <dd> <dl> <dt>

15117 (0x3B0D)
</dt> <dt>



Tipo ResourceCandidate non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**ERRORE \_ NOME MAPPA \_ \_ \_ DUPLICATO MRM**
</dt> <dd> <dl> <dt>

15118 (0x3B0E)
</dt> <dt>



Mapping delle risorse duplicato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**ERRORE \_ MRM \_ DUPLICATE \_ ENTRY**
</dt> <dd> <dl> <dt>

15119 (0x3B0F)
</dt> <dt>



Voce duplicata.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**ERRORE \_ MRM \_ INVALID RESOURCE \_ \_ IDENTIFIER**
</dt> <dd> <dl> <dt>

15120 (0x3B10)
</dt> <dt>



Identificatore di risorsa non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**ERRORE \_ MRM \_ FILEPATH \_ TOO \_ LONG**
</dt> <dd> <dl> <dt>

15121 (0x3B11)
</dt> <dt>



Percorso file troppo lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**ERRORE \_ MRM UNSUPPORTED DIRECTORY TYPE (TIPO DI DIRECTORY MRM \_ NON \_ \_ SUPPORTATO)**
</dt> <dd> <dl> <dt>

15122 (0x3B12)
</dt> <dt>



Tipo di directory non supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERRORE \_ MRM \_ FILE PRI NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

15126 (0x3B16)
</dt> <dt>



File PRI non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**ERRORE \_ MRM \_ DENOMINATO RESOURCE NOT \_ \_ \_ FOUND**
</dt> <dd> <dl> <dt>

15127 (0x3B17)
</dt> <dt>



NamedResource non trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**ERRORE \_ MAPPA MRM \_ NON \_ \_ TROVATA**
</dt> <dd> <dl> <dt>

15135 (0x3B1F)
</dt> <dt>



ResourceMap non trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**ERRORE \_ MRM \_ NON SUPPORTATO TIPO \_ DI \_ PROFILO**
</dt> <dd> <dl> <dt>

15136 (0x3B20)
</dt> <dt>



Tipo di profilo MRT non supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERRORE \_ OPERATORE \_ QUALIFICATORE NON \_ \_ VALIDO MRM**
</dt> <dd> <dl> <dt>

15137 (0x3B21)
</dt> <dt>



Operatore qualificatore non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERRORE \_ MRM \_ INDETERMINATE \_ QUALIFIER \_ VALUE**
</dt> <dd> <dl> <dt>

15138 (0x3B22)
</dt> <dt>



Impossibile determinare il valore del qualificatore o il valore del qualificatore non è stato impostato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**ERRORE \_ MRM \_ AUTOMERGE \_ ABILITATO**
</dt> <dd> <dl> <dt>

15139 (0x3B23)
</dt> <dt>



L'opzione Automerge è abilitata nel file PRI.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**ERRORE \_ MRM \_ TOO MANY \_ \_ RESOURCES**
</dt> <dd> <dl> <dt>

15140 (0x3B24)
</dt> <dt>



Troppe risorse definite per il pacchetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERRORE \_ MCA \_ NON VALIDA STRINGA \_ DI \_ FUNZIONALITÀ**
</dt> <dd> <dl> <dt>

15200 (0x3B60)
</dt> <dt>



Il monitoraggio ha restituito una stringa di funzionalità DDC/CI non conforme alla specifica ACCESS.bus 3.0, DDC/CI 1.1 o MCCS 2 Revisione 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERRORE \_ MCA \_ VERSIONE \_ VCP NON \_ VALIDA**
</dt> <dd> <dl> <dt>

15201 (0x3B61)
</dt> <dt>



Il codice VCP versione VCP (0xDF) del monitoraggio ha restituito un valore di versione non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**ERRORE \_ DEL MONITORAGGIO MCA CHE VIOLA LA \_ SPECIFICA \_ \_ \_ MCCS**
</dt> <dd> <dl> <dt>

15202 (0x3B62)
</dt> <dt>



Il monitoraggio non è conforme alla specifica MCCS che dichiara di supportare.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERRORE \_ DI \_ MANCATA CORRISPONDENZA DELLA VERSIONE \_ MCA \_ MCCS**
</dt> <dd> <dl> <dt>

15203 (0x3B63)
</dt> <dt>



La versione MCCS nella funzionalità mccs ver di un monitoraggio non corrisponde alla versione MCCS segnalata dal monitoraggio quando viene usato il codice \_ VCP vcp versione (0xDF).


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERRORE \_ MCA \_ VERSIONE \_ MCCS NON \_ SUPPORTATA**
</dt> <dd> <dl> <dt>

15204 (0x3B64)
</dt> <dt>



L'API di configurazione del monitoraggio funziona solo con i monitor che supportano la specifica MCCS 1.0, la specifica MCCS 2.0 o la specifica MCCS 2.0 Revisione 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**ERRORE \_ INTERNO MCA \_ \_**
</dt> <dd> <dl> <dt>

15205 (0x3B65)
</dt> <dt>



Si è verificato un errore interno dell'API di configurazione del monitoraggio.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERRORE \_ \_ MCA: TIPO DI TECNOLOGIA NON VALIDO \_ \_ \_ RESTITUITO**
</dt> <dd> <dl> <dt>

15206 (0x3B66)
</dt> <dt>



Il monitoraggio ha restituito un tipo di tecnologia di monitoraggio non valido. CRT, Tutto e LCD (TFT) sono esempi di tipi di tecnologia di monitoraggio. Questo errore implica che il monitoraggio viola la specifica MCCS 2.0 o MCCS 2.0 Revisione 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERRORE \_ MCA \_ NON SUPPORTATO PER LA TEMPERATURA DEI \_ \_ COLORI**
</dt> <dd> <dl> <dt>

15207 (0x3B67)
</dt> <dt>



Il chiamante [**di SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) ha specificato una temperatura di colore non supportate dal monitoraggio corrente. Questo errore implica che il monitoraggio viola la specifica MCCS 2.0 o MCCS 2.0 Revisione 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERRORE \_ DISPOSITIVO DI SISTEMA \_ \_ AMBIGUO**
</dt> <dd> <dl> <dt>

15250 (0x3B92)
</dt> <dt>



Il dispositivo di sistema richiesto non può essere identificato a causa di più dispositivi indistinguibili che corrispondono potenzialmente ai criteri di identificazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**ERRORE \_ DISPOSITIVO DI SISTEMA NON \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

15299 (0x3BC3)
</dt> <dt>



Impossibile trovare il dispositivo di sistema richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**\_HASH DEGLI ERRORI NON \_ \_ SUPPORTATO**
</dt> <dd> <dl> <dt>

15300 (0x3BC4)
</dt> <dt>



La generazione di hash per la versione hash e il tipo di hash specificati non è abilitata nel server.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**HASH \_ DI ERRORE NON \_ \_ PRESENTE**
</dt> <dd> <dl> <dt>

15301 (0x3BC5)
</dt> <dt>



L'hash richiesto dal server non è disponibile o non è più valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERRORE \_ PROVIDER \_ IC \_ SECONDARIO NON \_ \_ REGISTRATO**
</dt> <dd> <dl> <dt>

15321 (0x3BD9)
</dt> <dt>



L'istanza del controller di interrupt secondario che gestisce l'interrupt specificato non è registrata.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERRORE INFORMAZIONI \_ CLIENT GPIO \_ NON \_ \_ VALIDE**
</dt> <dd> <dl> <dt>

15322 (0x3BDA)
</dt> <dt>



Le informazioni fornite dal driver client GPIO non sono valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**ERRORE \_ VERSIONE GPIO \_ NON \_ \_ SUPPORTATA**
</dt> <dd> <dl> <dt>

15323 (0x3BDB)
</dt> <dt>



La versione specificata dal driver client GPIO non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**ERRORE \_ GPIO \_ PACCHETTO DI REGISTRAZIONE NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

15324 (0x3BDC)
</dt> <dt>



Il pacchetto di registrazione fornito dal driver client GPIO non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**ERRORE \_ OPERAZIONE GPIO \_ \_ NEGATA**
</dt> <dd> <dl> <dt>

15325 (0x3BDD)
</dt> <dt>



L'operazione richiesta non è supportata per l'handle specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERRORE \_ GPIO \_ MODALITÀ DI CONNESSIONE \_ INCOMPATIBILE \_**
</dt> <dd> <dl> <dt>

15326 (0x3BDE)
</dt> <dt>



La modalità di connessione richiesta è in conflitto con una modalità esistente in uno o più pin specificati.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERRORE \_ DI INTERRUPT GPIO \_ GIÀ SENZA \_ \_ MASCHERA**
</dt> <dd> <dl> <dt>

15327 (0x3BDF)
</dt> <dt>



L'interrupt richiesto per l'annullamento del mascheramento non è mascherato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**ERRORE NON \_ È \_ POSSIBILE CAMBIARE \_ RUNLEVEL**
</dt> <dd> <dl> <dt>

15400 (0x3C28)
</dt> <dt>



L'opzione del livello di esecuzione richiesta non può essere completata correttamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERRORE - \_ IMPOSTAZIONE \_ RUNLEVEL \_ NON VALIDA**
</dt> <dd> <dl> <dt>

15401 (0x3C29)
</dt> <dt>



Il servizio ha un'impostazione del livello di esecuzione non valida. Il livello di esecuzione per un servizio non deve essere superiore al livello di esecuzione dei servizi dipendenti.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**ERRORE \_ RUNLEVEL \_ SWITCH \_ TIMEOUT**
</dt> <dd> <dl> <dt>

15402 (0x3C2A)
</dt> <dt>



L'opzione del livello di esecuzione richiesta non può essere completata correttamente perché uno o più servizi non verranno arresti o riavviati entro il timeout specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**ERRORE \_ RUNLEVEL \_ SWITCH AGENT \_ \_ TIMEOUT**
</dt> <dd> <dl> <dt>

15403 (0x3C2B)
</dt> <dt>



Un agente switch a livello di esecuzione non ha risposto entro il timeout specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**ERRORE \_ OPZIONE RUNLEVEL \_ IN \_ \_ CORSO**
</dt> <dd> <dl> <dt>

15404 (0x3C2C)
</dt> <dt>



È in corso un cambio di livello di esecuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**AVVIO \_ AUTOMATICO DEI SERVIZI DI ERRORE NON \_ \_ RIUSCITO**
</dt> <dd> <dl> <dt>

15405 (0x3C2D)
</dt> <dt>



Non è stato possibile avviare uno o più servizi durante la fase di avvio del servizio di un commutatore a livello di esecuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERRORE \_ ARRESTO ATTIVITÀ COM IN \_ \_ \_ SOSPESO**
</dt> <dd> <dl> <dt>

15501 (0x3C8D)
</dt> <dt>



La richiesta di arresto dell'attività non può essere completata immediatamente perché l'attività richiede più tempo per l'arresto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE DEL PACCHETTO APERTO NON \_ \_ RIUSCITO**
</dt> <dd> <dl> <dt>

15600 (0x3CF0)
</dt> <dt>



Impossibile aprire il pacchetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE \_ DEL PACCHETTO NON \_ TROVATO**
</dt> <dd> <dl> <dt>

15601 (0x3CF1)
</dt> <dt>



Il pacchetto non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**ERRORE DURANTE \_ L'INSTALLAZIONE \_ DEL PACCHETTO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

15602 (0x3CF2)
</dt> <dt>



I dati del pacchetto non sono validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE DELLA RISOLUZIONE DELLA DIPENDENZA NON \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

15603 (0x3CF3)
</dt> <dt>



Aggiornamenti del pacchetto non riusciti, convalida delle dipendenze o dei conflitti.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERRORE DURANTE \_ \_ \_ L'INSTALLAZIONE DI SPAZIO SU DISCO \_ \_ INSUFFICIENTE**
</dt> <dd> <dl> <dt>

15604 (0x3CF4)
</dt> <dt>



Lo spazio su disco nel computer non è sufficiente. Liberare spazio e riprovare.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE DELLA \_ RETE**
</dt> <dd> <dl> <dt>

15605 (0x3CF5)
</dt> <dt>



Si è verificato un problema durante il download del prodotto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE DELLA \_ REGISTRAZIONE**
</dt> <dd> <dl> <dt>

15606 (0x3CF6)
</dt> <dt>



Impossibile registrare il pacchetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE DI UN ERRORE DI \_ ANNULLAMENTO DELLA REGISTRAZIONE**
</dt> <dd> <dl> <dt>

15607 (0x3CF7)
</dt> <dt>



Impossibile annullare la registrazione del pacchetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**ERRORE DURANTE \_ L'INSTALLAZIONE \_ ANNULLA**
</dt> <dd> <dl> <dt>

15608 (0x3CF8)
</dt> <dt>



L'utente ha annullato la richiesta di installazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE NON RIUSCITA**
</dt> <dd> <dl> <dt>

15609 (0x3CF9)
</dt> <dt>



Installazione non riuscita. Contattare il fornitore del software.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**ERRORE \_ RIMOZIONE \_ NON RIUSCITA**
</dt> <dd> <dl> <dt>

15610 (0x3CFA)
</dt> <dt>



Rimozione non riuscita. Contattare il fornitore del software.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**IL \_ PACCHETTO DI ERRORI ESISTE \_ \_ GIÀ**
</dt> <dd> <dl> <dt>

15611 (0x3CFB)
</dt> <dt>



Il pacchetto fornito è già installato e la reinstallazione del pacchetto è stata bloccata. Controllare il AppXDeployment-Server eventi per informazioni dettagliate.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**CORREZIONE \_ \_ DELL'ERRORE NECESSARIO**
</dt> <dd> <dl> <dt>

15612 (0x3CFC)
</dt> <dt>



Impossibile avviare l'applicazione. Provare a reinstallare l'applicazione per risolvere il problema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE DEL PREREQUISITO \_ NON RIUSCITO**
</dt> <dd> <dl> <dt>

15613 (0x3CFD)
</dt> <dt>



Non è stato possibile completare un prerequisito per un'installazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**ERRORE NEL \_ \_ REPOSITORY DEL PACCHETTO \_ DANNEGGIATO**
</dt> <dd> <dl> <dt>

15614 (0x3CFE)
</dt> <dt>



Il repository dei pacchetti è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE DEI \_ CRITERI**
</dt> <dd> <dl> <dt>

15615 (0x3CFF)
</dt> <dt>



Per installare questa applicazione, è necessaria una licenza Windows developer o un sistema abilitato per il sideload.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**ERRORE DURANTE \_ L'AGGIORNAMENTO DEL \_ PACCHETTO**
</dt> <dd> <dl> <dt>

15616 (0x3D00)
</dt> <dt>



L'applicazione non può essere avviata perché è in fase di aggiornamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**DISTRIBUZIONE \_ DEGLI ERRORI BLOCCATA DAI \_ \_ \_ CRITERI**
</dt> <dd> <dl> <dt>

15617 (0x3D01)
</dt> <dt>



L'operazione di distribuzione del pacchetto è bloccata dai criteri. Contattare l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**PACCHETTI \_ DI ERRORI IN \_ \_ USO**
</dt> <dd> <dl> <dt>

15618 (0x3D02)
</dt> <dt>



Impossibile installare il pacchetto perché le risorse che modifica sono attualmente in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**ERRORE FILE \_ DI \_ RIPRISTINO \_ DANNEGGIATO**
</dt> <dd> <dl> <dt>

15619 (0x3D03)
</dt> <dt>



Impossibile recuperare il pacchetto perché i dati necessari per il ripristino sono danneggiati.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERRORE FIRMA \_ DI GESTIONE A FASI NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

15620 (0x3D04)
</dt> <dt>



La firma non è valida. Per eseguire la registrazione in modalità sviluppatore, AppxSignature.p7x e AppxBlockMap.xml devono essere validi o non devono essere presenti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**ERRORE DURANTE \_ \_ L'ELIMINAZIONE \_ DELL'APPLICAZIONE ESISTENTEI \_ STORE DI DATI NON È \_ RIUSCITO**
</dt> <dd> <dl> <dt>

15621 (0x3D05)
</dt> <dt>



Si è verificato un errore durante l'eliminazione dei dati dell'applicazione esistenti del pacchetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE \_ DEL DOWNGRADE DEL PACCHETTO**
</dt> <dd> <dl> <dt>

15622 (0x3D06)
</dt> <dt>



Non è stato possibile installare il pacchetto perché è già installata una versione successiva del pacchetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**CORREZIONE \_ DEL SISTEMA DI \_ \_ ERRORI**
</dt> <dd> <dl> <dt>

15623 (0x3D07)
</dt> <dt>



È stato rilevato un errore in un file binario di sistema. Provare ad aggiornare il PC per risolvere il problema.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**ERRORE \_ DI INTEGRITÀ APPX ERRORE CLR \_ \_ \_ \_ NGEN**
</dt> <dd> <dl> <dt>

15624 (0x3D08)
</dt> <dt>



È stato rilevato un file binario NGEN CLR danneggiato nel sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**ERRORE \_ FILE DI RESILIENZA \_ \_ DANNEGGIATO**
</dt> <dd> <dl> <dt>

15625 (0x3D09)
</dt> <dt>



Impossibile riprendere l'operazione perché i dati necessari per il ripristino sono danneggiati.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE DEL SERVIZIO FIREWALL NON IN \_ \_ \_ ESECUZIONE**
</dt> <dd> <dl> <dt>

15626 (0x3D0A)
</dt> <dt>



Non è stato possibile installare il pacchetto perché il Windows firewall non è in esecuzione. Abilitare il Windows firewall e riprovare.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**ERRORE APPMODEL \_ \_ NESSUN \_ PACCHETTO**
</dt> <dd> <dl> <dt>

15700 (0x3D54)
</dt> <dt>



Il processo non ha un'identità del pacchetto.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**RUNTIME DEL PACCHETTO \_ DI \_ ERRORI APPMODEL \_ \_ DANNEGGIATO**
</dt> <dd> <dl> <dt>

15701 (0x3D55)
</dt> <dt>



Le informazioni di runtime del pacchetto sono danneggiate.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**IDENTITÀ DEL PACCHETTO ERRORI APPMODEL \_ \_ \_ \_ DANNEGGIATA**
</dt> <dd> <dl> <dt>

15702 (0x3D56)
</dt> <dt>



L'identità del pacchetto è danneggiata.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**ERRORE APPMODEL \_ \_ NESSUNA \_ APPLICAZIONE**
</dt> <dd> <dl> <dt>

15703 (0x3D57)
</dt> <dt>



Il processo non ha un'identità dell'applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**ERRORE \_ L'ARCHIVIO \_ DI CARICAMENTO DELLO STATO NON È \_ \_ RIUSCITO**
</dt> <dd> <dl> <dt>

15800 (0x3DB8)
</dt> <dt>



Caricamento dell'archivio stati non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**ERRORE \_ STATO GET VERSION \_ \_ \_ FAILED**
</dt> <dd> <dl> <dt>

15801 (0x3DB9)
</dt> <dt>



Il recupero della versione dello stato per l'applicazione non è riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**ERRORE VERSIONE \_ DEL SET DI STATI NON \_ \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

15802 (0x3DBA)
</dt> <dt>



L'impostazione della versione dello stato per l'applicazione non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**REIMPOSTAZIONE \_ \_ STRUTTURATA DELLO \_ STATO DI ERRORE \_ NON RIUSCITA**
</dt> <dd> <dl> <dt>

15803 (0x3DBB)
</dt> <dt>



La reimpostazione dello stato strutturato dell'applicazione non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**ERRORE STATO \_ APERTURA \_ \_ CONTENITORE \_ NON RIUSCITA**
</dt> <dd> <dl> <dt>

15804 (0x3DBC)
</dt> <dt>



Il gestore di stato non è riuscito ad aprire il contenitore.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**ERRORE STATO \_ CREAZIONE \_ \_ CONTENITORE \_ NON RIUSCITA**
</dt> <dd> <dl> <dt>

15805 (0x3DBD)
</dt> <dt>



Il gestore di stato non è riuscito a creare il contenitore.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**ERRORE STATO \_ ELIMINAZIONE \_ \_ CONTENITORE \_ NON RIUSCITA**
</dt> <dd> <dl> <dt>

15806 (0x3DBE)
</dt> <dt>



Il gestore di stato non è riuscito a eliminare il contenitore.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**\_L'IMPOSTAZIONE DI LETTURA DELLO STATO DI ERRORE NON È \_ \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

15807 (0x3DBF)
</dt> <dt>



Il gestore di stato non è riuscito a leggere l'impostazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**ERRORE IMPOSTAZIONE \_ SCRITTURA \_ STATO NON \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

15808 (0x3DC0)
</dt> <dt>



Il gestore di stato non è riuscito a scrivere l'impostazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**\_L'IMPOSTAZIONE DI ELIMINAZIONE DELLO STATO DI ERRORE NON È \_ \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

15809 (0x3DC1)
</dt> <dt>



Il gestore di stato non è riuscito a eliminare l'impostazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**IMPOSTAZIONE \_ QUERY STATO ERRORE NON \_ \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

15810 (0x3DC2)
</dt> <dt>



Gestione stato non è riuscito a eseguire una query sull'impostazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**ERRORE STATO \_ LETTURA \_ IMPOSTAZIONE \_ \_ COMPOSITA NON \_ RIUSCITA**
</dt> <dd> <dl> <dt>

15811 (0x3DC3)
</dt> <dt>



Il gestore di stato non è riuscito a leggere l'impostazione composita.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**ERRORE SCRITTURA \_ \_ IMPOSTAZIONE \_ \_ COMPOSITA STATO NON \_ RIUSCITA**
</dt> <dd> <dl> <dt>

15812 (0x3DC4)
</dt> <dt>



Gestione stato non è riuscito a scrivere l'impostazione composita.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**ERRORE STATO \_ ENUMERAZIONE \_ \_ CONTENITORE \_ NON RIUSCITO**
</dt> <dd> <dl> <dt>

15813 (0x3DC5)
</dt> <dt>



Il gestore di stato non è riuscito a enumerare i contenitori.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**ERRORE STATO \_ ENUMERAZIONE \_ IMPOSTAZIONI NON \_ \_ RIUSCITE**
</dt> <dd> <dl> <dt>

15814 (0x3DC6)
</dt> <dt>



State Manager non è riuscito a enumerare le impostazioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**LIMITE \_ DELLE DIMENSIONI DEL VALORE \_ \_ \_ DELL'IMPOSTAZIONE \_ COMPOSITA STATO ERRORE \_ \_ SUPERATO**
</dt> <dd> <dl> <dt>

15815 (0x3DC7)
</dt> <dt>



Le dimensioni del valore dell'impostazione composita del gestore di stato hanno superato il limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**LIMITE \_ DELLE DIMENSIONI DEL VALORE \_ \_ \_ DELL'IMPOSTAZIONE DELLO \_ STATO DI ERRORE \_ SUPERATO**
</dt> <dd> <dl> <dt>

15816 (0x3DC8)
</dt> <dt>



Le dimensioni del valore dell'impostazione del gestore di stato hanno superato il limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**LIMITE \_ DIMENSIONI NOME IMPOSTAZIONE STATO ERRORE \_ \_ \_ \_ \_ SUPERATO**
</dt> <dd> <dl> <dt>

15817 (0x3DC9)
</dt> <dt>



La lunghezza del nome dell'impostazione del gestore dello stato ha superato il limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**LIMITE \_ DIMENSIONI \_ NOME \_ \_ CONTENITORE STATO ERRORE \_ \_ SUPERATO**
</dt> <dd> <dl> <dt>

15818 (0x3DCA)
</dt> <dt>



La lunghezza del nome del contenitore di gestione dello stato ha superato il limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**ERRORE \_ API \_ NON DISPONIBILE**
</dt> <dd> <dl> <dt>

15841 (0x3DE1)
</dt> <dt>



Questa API non può essere usata nel contesto del tipo di applicazione del chiamante.


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

 

 
