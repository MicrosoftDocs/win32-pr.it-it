---
description: Descrive i codici di errore 12000-1599 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: Codici di errore di sistema (12000-15999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8cac8adf6d8a4cf8f60fe978eb6f99f5efc1b9fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483324"
---
# <a name="system-error-codes-12000-15999"></a>Codici di errore di sistema (12000-15999)

> [!NOTE]
> Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema. Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .

Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) (errori da 12000 a 15999). Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .

<dl> <dt>

<span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>**Errore \_ \_Internet \** _
</dt> <dd> <dl> <dt>

12000-12175 (0x2EE0)
</dt> <dt>



Vedere [codici di errore Internet](../wininet/wininet-errors.md) e Wininet. h.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ errore per il criterio di criteri di verifica *\_ IPSec \_ \_ \_ esistente**
</dt> <dd> <dl> <dt>

13000 (0x32C8)
</dt> <dt>



Il criterio in modalità rapida specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**\_ \_ \_ \_ Impossibile trovare il criterio \_ della linea di errore IPSec**
</dt> <dd> <dl> <dt>

13001 (0x32C9)
</dt> <dt>



Impossibile trovare i criteri in modalità rapida specificati.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERRORE \_ \_ per il \_ criterio \_ di \_ utilizzo criteri di errore IPSec**
</dt> <dd> <dl> <dt>

13002 (0x32CA)
</dt> <dt>



Vengono utilizzati i criteri in modalità rapida specificati.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**il \_ criterio di errore IPSec \_ mm \_ \_ esiste**
</dt> <dd> <dl> <dt>

13003 (0x32CB)
</dt> <dt>



Il criterio della modalità principale specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERRORE \_ IPSec \_ mm \_ criterio \_ non \_ trovato**
</dt> <dd> <dl> <dt>

13004 (0x32CC)
</dt> <dt>



Il criterio della modalità principale specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**\_ \_ criterio di errore IPSec mm \_ \_ in \_ uso**
</dt> <dd> <dl> <dt>

13005 (0x32CD)
</dt> <dt>



Viene utilizzato il criterio della modalità principale specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERRORE \_ IPSec \_ mm \_ filtro \_ esistente**
</dt> <dd> <dl> <dt>

13006 (0x32CE)
</dt> <dt>



Il filtro della modalità principale specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERRORE \_ di \_ filtro IPSec mm \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

13007 (0x32CF)
</dt> <dt>



Il filtro in modalità principale specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERRORE \_ \_ filtro trasporto \_ IPSec \_ esistente**
</dt> <dd> <dl> <dt>

13008 (0x32D0)
</dt> <dt>



Il filtro della modalità di trasporto specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERRORE \_ di \_ filtro trasporto IPSec \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

13009 (0x32D1)
</dt> <dt>



Il filtro della modalità di trasporto specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERRORE \_ \_ autenticazione IPSec \_ mm \_ esistente**
</dt> <dd> <dl> <dt>

13010 (0x32D2)
</dt> <dt>



L'elenco di autenticazione in modalità principale specificato esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERRORE \_ IPSec \_ mm \_ auth \_ non \_ trovato**
</dt> <dd> <dl> <dt>

13011 (0x32D3)
</dt> <dt>



L'elenco di autenticazione in modalità principale specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERRORE \_ \_ \_ di autenticazione IPSec mm \_ in \_ uso**
</dt> <dd> <dl> <dt>

13012 (0x32D4)
</dt> <dt>



Viene utilizzato l'elenco di autenticazione in modalità principale specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**errore \_ errore \_ IPSec \_ predefinito \_ mm \_ non \_ trovato**
</dt> <dd> <dl> <dt>

13013 (0x32D5)
</dt> <dt>



Il criterio della modalità principale predefinito specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERRORE \_ di \_ autenticazione predefinita IPSec \_ mm \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

13014 (0x32D6)
</dt> <dt>



L'elenco di autenticazione in modalità principale predefinito specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERRORE \_ \_ \_ \_ \_ Impossibile trovare criteri mq predefiniti \_ IPSec**
</dt> <dd> <dl> <dt>

13015 (0x32D7)
</dt> <dt>



Impossibile trovare i criteri in modalità rapida predefiniti specificati.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERRORE \_ \_ filtro tunnel \_ IPSec \_ esistente**
</dt> <dd> <dl> <dt>

13016 (0x32D8)
</dt> <dt>



Il filtro in modalità tunnel specificato esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**\_ \_ \_ \_ Impossibile trovare il filtro del tunnel IPSec di errore \_**
</dt> <dd> <dl> <dt>

13017 (0x32D9)
</dt> <dt>



Il filtro in modalità tunnel specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERRORE \_ di \_ \_ eliminazione del filtro IPSec \_ in sospeso \_**
</dt> <dd> <dl> <dt>

13018 (0x32DA)
</dt> <dt>



Il filtro in modalità principale è in attesa di eliminazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**errore durante l' \_ \_ \_ \_ eliminazione in sospeso del filtro trasporto \_ IPSec**
</dt> <dd> <dl> <dt>

13019 (0x32DB)
</dt> <dt>



Il filtro di trasporto è in attesa di eliminazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**errore durante l' \_ \_ \_ \_ eliminazione in sospeso del filtro tunnel \_ IPSec**
</dt> <dd> <dl> <dt>

13020 (0x32DC)
</dt> <dt>



L'eliminazione del filtro del tunnel è in sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERRORE \_ del \_ criterio IPSec mm \_ \_ eliminazione in sospeso \_**
</dt> <dd> <dl> <dt>

13021 (0x32DD)
</dt> <dt>



Il criterio della modalità principale è in attesa di eliminazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERRORE \_ di \_ autenticazione IPSec mm- \_ \_ eliminazione in sospeso \_**
</dt> <dd> <dl> <dt>

13022 (0x32DE)
</dt> <dt>



Il bundle di autenticazione in modalità principale è in attesa di eliminazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**errore durante l' \_ \_ \_ \_ eliminazione in sospeso del criterio \_ per l'IPSec**
</dt> <dd> <dl> <dt>

13023 (0x32DF)
</dt> <dt>



L'eliminazione dei criteri in modalità rapida è in sospeso.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**AVVISO \_ \_ criteri IPSec \_ mm \_ eliminati**
</dt> <dd> <dl> <dt>

13024 (0x32E0)
</dt> <dt>



Il criterio della modalità principale è stato aggiunto correttamente, ma alcune delle offerte richieste non sono supportate.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**AVVISO \_ di \_ criteri di mq IPSec \_ \_ eliminati**
</dt> <dd> <dl> <dt>

13025 (0x32E1)
</dt> <dt>



Il criterio della modalità rapida è stato aggiunto correttamente, ma alcune delle offerte richieste non sono supportate.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERRORE \_ di \_ stato negativo IPSec IKE- \_ \_ \_ inizio**
</dt> <dd> <dl> <dt>

13800 (0x35E8)
</dt> <dt>



ERRORE \_ di \_ stato negativo IPSec IKE- \_ \_ \_ inizio


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERRORE \_ \_ autenticazione IKE \_ IPSec \_ non riuscita**
</dt> <dd> <dl> <dt>

13801 (0x35E9)
</dt> <dt>



Le credenziali di autenticazione IKE sono inaccettabili.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERRORE \_ \_ attrib IKE \_ IPSec \_ non riuscita**
</dt> <dd> <dl> <dt>

13802 (0x35EA)
</dt> <dt>



Gli attributi di sicurezza IKE sono inaccettabili.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERRORE \_ di \_ negoziazione IKE IPSec \_ \_ in sospeso**
</dt> <dd> <dl> <dt>

13803 (0x35EB)
</dt> <dt>



Negoziazione IKE in corso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**errore \_ di \_ \_ elaborazione generale \_ IKE \_ IPSec errore**
</dt> <dd> <dl> <dt>

13804 (0x35EC)
</dt> <dt>



Errore di elaborazione generale.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**\_ \_ Timeout IKE IPSec \_ errore \_**
</dt> <dd> <dl> <dt>

13805 (0x35ED)
</dt> <dt>



Timeout della negoziazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERRORE \_ IPSec \_ IKE \_ nessun \_ certificato**
</dt> <dd> <dl> <dt>

13806 (0x35EE)
</dt> <dt>



IKE non è riuscito a trovare il certificato del computer valido. Contattare l'amministratore della sicurezza di rete per informazioni sull'installazione di un certificato valido nell'archivio certificati appropriato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERRORE \_ \_ SA IPSec \_ IKE \_ eliminato**
</dt> <dd> <dl> <dt>

13807 (0x35EF)
</dt> <dt>



La SA IKE è stata eliminata dal peer prima del completamento dell'installazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERRORE \_ \_ SA IPSec \_ IKE \_ raccolto**
</dt> <dd> <dl> <dt>

13808 (0x35F0)
</dt> <dt>



Il SA IKE è stato eliminato prima del completamento dell'installazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**errore durante l' \_ \_ \_ \_ acquisizione \_ del protocollo IPSec**
</dt> <dd> <dl> <dt>

13809 (0x35F1)
</dt> <dt>



La richiesta di negoziazione è rimasta in coda troppo a lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**errore durante l' \_ \_ acquisizione dell' \_ \_ \_ istruzione IPSec**
</dt> <dd> <dl> <dt>

13810 (0x35F2)
</dt> <dt>



La richiesta di negoziazione è rimasta in coda troppo a lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERRORE \_ di \_ \_ ricezione coda \_ IKE \_ IPSec**
</dt> <dd> <dl> <dt>

13811 (0x35F3)
</dt> <dt>



La richiesta di negoziazione è rimasta in coda troppo a lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**errore durante la coda di messaggi \_ \_ IKE IPSec \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

13812 (0x35F4)
</dt> <dt>



La richiesta di negoziazione è rimasta in coda troppo a lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERRORE \_ di \_ \_ eliminazione \_ Nessuna \_ risposta IKE IPSec**
</dt> <dd> <dl> <dt>

13813 (0x35F5)
</dt> <dt>



Nessuna risposta da peer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**errore errore \_ IPSec \_ IKE \_ mm \_ ritardo \_**
</dt> <dd> <dl> <dt>

13814 (0x35F6)
</dt> <dt>



La negoziazione ha impiegato troppo tempo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**errore durante la rimozione del \_ \_ \_ \_ ritardo IKE \_ .**
</dt> <dd> <dl> <dt>

13815 (0x35F7)
</dt> <dt>



La negoziazione ha impiegato troppo tempo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**errore \_ IKE IPSec errore \_ \_**
</dt> <dd> <dl> <dt>

13816 (0x35F8)
</dt> <dt>



Si è verificato un errore sconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERRORE \_ \_ CRL IKE \_ IPSec \_ non riuscito**
</dt> <dd> <dl> <dt>

13817 (0x35F9)
</dt> <dt>



Verifica revoca certificato non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERRORE \_ di \_ utilizzo della chiave IKE IPSec \_ non valido \_ \_**
</dt> <dd> <dl> <dt>

13818 (0x35FA)
</dt> <dt>



Utilizzo chiave del certificato non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERRORE \_ IPSec \_ IKE \_ \_ tipo di certificato non valido \_**
</dt> <dd> <dl> <dt>

13819 (0x35FB)
</dt> <dt>



Tipo di certificato non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERRORE \_ IPSec \_ IKE \_ Nessuna \_ \_ chiave privata**
</dt> <dd> <dl> <dt>

13820 (0x35FC)
</dt> <dt>



Negoziazione IKE non riuscita perché il certificato del computer utilizzato non dispone di una chiave privata. I certificati IPsec richiedono una chiave privata. Contattare l'amministratore della sicurezza di rete per la sostituzione con un certificato con una chiave privata.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERRORE \_ \_ \_ REKEY simultaneo IKE IPSec \_**
</dt> <dd> <dl> <dt>

13821 (0x35FD)
</dt> <dt>



Sono state rilevate richiavi simultanee.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**errore \_ errore \_ IPSec \_ DH \_**
</dt> <dd> <dl> <dt>

13822 (0x35FE)
</dt> <dt>



Errore nel calcolo Diffie-Hellman.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERRORE \_ \_ \_ payload critico IKE \_ IPSec \_ non \_ riconosciuto**
</dt> <dd> <dl> <dt>

13823 (0x35FF)
</dt> <dt>



Non si sa come elaborare il payload critico.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERRORE \_ dell' \_ intestazione IKE IPSec \_ non valida \_**
</dt> <dd> <dl> <dt>

13824 (0x3600)
</dt> <dt>



Intestazione non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERRORE \_ IPSec \_ IKE \_ nessun \_ criterio**
</dt> <dd> <dl> <dt>

13825 (0x3601)
</dt> <dt>



Nessun criterio configurato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERRORE \_ di \_ firma IKE IPSec \_ non valida \_**
</dt> <dd> <dl> <dt>

13826 (0x3602)
</dt> <dt>



Impossibile verificare la firma.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**errore \_ \_ \_ errore Kerberos IKE \_ IPSec**
</dt> <dd> <dl> <dt>

13827 (0x3603)
</dt> <dt>



Non è stato possibile eseguire l'autenticazione tramite Kerberos.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERRORE \_ \_ IKE IPSec \_ Nessuna \_ \_ chiave pubblica**
</dt> <dd> <dl> <dt>

13828 (0x3604)
</dt> <dt>



Il certificato del peer non ha una chiave pubblica.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERRORE \_ \_ processo IKE \_ IPSec \_ errore**
</dt> <dd> <dl> <dt>

13829 (0x3605)
</dt> <dt>



Errore durante l'elaborazione del payload degli errori.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERRORE \_ del \_ processo IKE IPSec \_ \_ Err \_ sa**
</dt> <dd> <dl> <dt>

13830 (0x3606)
</dt> <dt>



Errore durante l'elaborazione del payload SA.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**ERRORE \_ \_ processo IKE IPSec \_ processo \_ Err \_ prop**
</dt> <dd> <dl> <dt>

13831 (0x3607)
</dt> <dt>



Errore durante l'elaborazione del payload della proposta.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERRORE \_ \_ processo IKE \_ IPSec \_ \_ transazione**
</dt> <dd> <dl> <dt>

13832 (0x3608)
</dt> <dt>



Errore durante l'elaborazione del payload di trasformazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**ERRORE \_ il \_ processo IKE IPSec \_ \_ Err \_ ke**
</dt> <dd> <dl> <dt>

13833 (0x3609)
</dt> <dt>



Errore durante l'elaborazione del payload KE.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**errore \_ errore \_ IPSec \_ processo \_ IKE \_ ID**
</dt> <dd> <dl> <dt>

13834 (0x360A)
</dt> <dt>



Errore durante l'elaborazione del payload dell'ID.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**ERRORE \_ \_ processo IKE IPSec \_ processo \_ Err \_ certificato**
</dt> <dd> <dl> <dt>

13835 (0x360B)
</dt> <dt>



Errore durante l'elaborazione del payload del certificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERRORE \_ \_ processo IKE \_ IPSec \_ Err \_ CERT \_ req**
</dt> <dd> <dl> <dt>

13836 (0x360C)
</dt> <dt>



Errore durante l'elaborazione del payload della richiesta di certificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERRORE \_ dell' \_ \_ \_ hash Err del processo IKE IPSec \_**
</dt> <dd> <dl> <dt>

13837 (0x360D)
</dt> <dt>



Errore durante l'elaborazione del payload hash.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**ERRORE \_ \_ processo IKE \_ IPSec \_ Err \_ sig**
</dt> <dd> <dl> <dt>

13838 (0x360E)
</dt> <dt>



Errore durante l'elaborazione del payload della firma.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERRORE \_ \_ nonce del \_ processo \_ IKE \_ IPSec**
</dt> <dd> <dl> <dt>

13839 (0x360F)
</dt> <dt>



Errore durante l'elaborazione del payload nonce.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**errore \_ errore \_ IPSec \_ processo \_ IKE \_ notifica**
</dt> <dd> <dl> <dt>

13840 (0x3610)
</dt> <dt>



Errore durante l'elaborazione del payload di notifica.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**errore \_ errore \_ IPSec \_ processo \_ IKE \_ Delete**
</dt> <dd> <dl> <dt>

13841 (0x3611)
</dt> <dt>



Errore durante l'elaborazione del payload Delete.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**ERRORE \_ del \_ \_ \_ Fornitore Err del processo IKE IPSec \_**
</dt> <dd> <dl> <dt>

13842 (0x3612)
</dt> <dt>



Errore durante l'elaborazione del payload VendorId.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERRORE \_ \_ payload IKE \_ non valido \_**
</dt> <dd> <dl> <dt>

13843 (0x3613)
</dt> <dt>



Ricevuto payload non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERRORE \_ di \_ \_ caricamento \_ software IKE \_ IPSec**
</dt> <dd> <dl> <dt>

13844 (0x3614)
</dt> <dt>



Il SA è stato caricato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERRORE dell'amministratore di \_ \_ \_ software IKE Soft \_ sa \_ \_**
</dt> <dd> <dl> <dt>

13845 (0x3615)
</dt> <dt>



Abbassamento di SA soft.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERRORE \_ \_ IKE IPSec \_ non valido \_**
</dt> <dd> <dl> <dt>

13846 (0x3616)
</dt> <dt>



Ricevuto cookie non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERRORE \_ IPSec \_ \_ non IKE \_ nessun \_ certificato peer**
</dt> <dd> <dl> <dt>

13847 (0x3617)
</dt> <dt>



Il peer non è riuscito a inviare un certificato macchina valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERRORE \_ del \_ \_ peer CRL IKE IPSec \_ \_ non riuscito**
</dt> <dd> <dl> <dt>

13848 (0x3618)
</dt> <dt>



Verifica revoca certificati del certificato del peer non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**errore durante la \_ \_ modifica dei criteri IKE IPSec \_ \_**
</dt> <dd> <dl> <dt>

13849 (0x3619)
</dt> <dt>



Il nuovo criterio è stato invalidato con firma di accesso condiviso con criteri obsoleti.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**\_ \_ criterio IKE errore IPSec \_ No \_ mm \_**
</dt> <dd> <dl> <dt>

13850 (0x361A)
</dt> <dt>



Non sono disponibili criteri IKE in modalità principale.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERRORE \_ IPSec \_ \_ NOTCBPRIV IKE**
</dt> <dd> <dl> <dt>

13851 (0x361B)
</dt> <dt>



Non è stato possibile abilitare il privilegio TCB.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERRORE \_ IPSec \_ \_ SECLOADFAIL IKE**
</dt> <dd> <dl> <dt>

13852 (0x361C)
</dt> <dt>



Non è stato possibile caricare SECURITY.DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERRORE \_ IPSec \_ \_ FAILSSPINIT IKE**
</dt> <dd> <dl> <dt>

13853 (0x361D)
</dt> <dt>



Non è stato possibile ottenere l'indirizzo di invio della tabella della funzione di sicurezza da SSPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERRORE \_ IPSec \_ \_ FAILQUERYSSP IKE**
</dt> <dd> <dl> <dt>

13854 (0x361E)
</dt> <dt>



Impossibile eseguire una query sul pacchetto Kerberos per ottenere le dimensioni massime del token.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERRORE \_ IPSec \_ \_ SRVACQFAIL IKE**
</dt> <dd> <dl> <dt>

13855 (0x361F)
</dt> <dt>



Non è stato possibile ottenere le credenziali del server Kerberos per il servizio IKE ISAKMP/ERROR \_ IPSec \_ . L'autenticazione Kerberos non funzionerà. La causa più probabile di questo problema è la mancanza di appartenenza al dominio. Questo comportamento è normale se il computer è membro di un gruppo di lavoro.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERRORE \_ IPSec \_ \_ SRVQUERYCRED IKE**
</dt> <dd> <dl> <dt>

13856 (0x3620)
</dt> <dt>



Impossibile determinare il nome dell'entità SSPI per il \_ servizio IKE IPSec/errore \_ ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERRORE \_ IPSec \_ \_ GETSPIFAIL IKE**
</dt> <dd> <dl> <dt>

13857 (0x3621)
</dt> <dt>



Non è stato possibile ottenere il nuovo SPI per la SA in ingresso dal driver IPsec. La ragione più comune è che il driver non dispone del filtro corretto. Verificare i criteri per verificare i filtri.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERRORE \_ del \_ filtro IKE IPSec \_ non valido \_**
</dt> <dd> <dl> <dt>

13858 (0x3622)
</dt> <dt>



Il filtro specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERRORE \_ \_ \_ \_ di \_ memoria IKE IPSec**
</dt> <dd> <dl> <dt>

13859 (0x3623)
</dt> <dt>



L'allocazione di memoria ha avuto esito negativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERRORE \_ di \_ aggiunta della chiave di aggiornamento IKE IPSec \_ \_ \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

13860 (0x3624)
</dt> <dt>



Non è stato possibile aggiungere l'associazione di sicurezza al driver IPsec. La ragione più comune è rappresentata dal fatto che la negoziazione IKE ha impiegato troppo tempo per il completamento. Se il problema persiste, ridurre il carico sul computer che ha generato l'errore.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERRORE \_ del \_ criterio IKE IPSec \_ non valido \_**
</dt> <dd> <dl> <dt>

13861 (0x3625)
</dt> <dt>



Criterio non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERRORE \_ IPSec \_ \_ sconosciuto IKE \_**
</dt> <dd> <dl> <dt>

13862 (0x3626)
</dt> <dt>



DOI non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**situazione di errore \_ \_ IKE IPSec \_ non valida \_**
</dt> <dd> <dl> <dt>

13863 (0x3627)
</dt> <dt>



Situazione non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**errore \_ errore \_ DH IKE IPSec \_ \_**
</dt> <dd> <dl> <dt>

13864 (0x3628)
</dt> <dt>



Errore Diffie-Hellman.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERRORE \_ del \_ gruppo IKE IPSec \_ non valido \_**
</dt> <dd> <dl> <dt>

13865 (0x3629)
</dt> <dt>



Gruppo di Diffie-Hellman non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERRORE \_ di \_ crittografia IKE IPSec \_**
</dt> <dd> <dl> <dt>

13866 (0x362A)
</dt> <dt>



Errore durante la crittografia del payload.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERRORE \_ di \_ \_ decrittografia IKE IPSec**
</dt> <dd> <dl> <dt>

13867 (0x362B)
</dt> <dt>



Errore durante la decrittografia del payload.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERRORE \_ \_ criterio IKE \_ IPSec \_ corrispondente**
</dt> <dd> <dl> <dt>

13868 (0x362C)
</dt> <dt>



Errore di corrispondenza dei criteri.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERRORE \_ di \_ ID IKE IPSec non \_ supportato \_**
</dt> <dd> <dl> <dt>

13869 (0x362D)
</dt> <dt>



ID non supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERRORE \_ di \_ \_ hash IKE non valido \_**
</dt> <dd> <dl> <dt>

13870 (0x362E)
</dt> <dt>



Verifica hash non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERRORE \_ dell' \_ \_ \_ hash ALG non \_ valido per IPSec**
</dt> <dd> <dl> <dt>

13871 (0x362F)
</dt> <dt>



Algoritmo hash non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERRORE \_ della \_ dimensione hash IKE IPSec \_ non valida \_ \_**
</dt> <dd> <dl> <dt>

13872 (0x3630)
</dt> <dt>



Dimensioni hash non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERRORE \_ \_ IKE IPSec \_ non valido \_ crittografare \_ ALG**
</dt> <dd> <dl> <dt>

13873 (0x3631)
</dt> <dt>



Algoritmo di crittografia non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERRORE \_ \_ AUTH IPSec \_ non \_ valido \_**
</dt> <dd> <dl> <dt>

13874 (0x3632)
</dt> <dt>



Algoritmo di autenticazione non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERRORE \_ del \_ sig IPSec IKE \_ non valido \_**
</dt> <dd> <dl> <dt>

13875 (0x3633)
</dt> <dt>



Firma del certificato non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERRORE \_ di \_ caricamento IKE IPSec \_ \_ non riuscito**
</dt> <dd> <dl> <dt>

13876 (0x3634)
</dt> <dt>



Il caricamento non è riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERRORE \_ IPSec \_ IKE \_ \_ Delete RPC**
</dt> <dd> <dl> <dt>

13877 (0x3635)
</dt> <dt>



Eliminato tramite la chiamata RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERRORE \_ IPSec \_ IKE \_ BENIGNo \_ reinit**
</dt> <dd> <dl> <dt>

13878 (0x3636)
</dt> <dt>



Stato temporaneo creato per eseguire la reinizializzazione. Non si tratta di un errore reale.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERRORE \_ di \_ \_ notifica della \_ durata del risponditore IKE IPSec non valido \_ \_**
</dt> <dd> <dl> <dt>

13879 (0x3637)
</dt> <dt>



Il valore di durata ricevuto nella notifica di durata del risponditore è inferiore al valore minimo di Windows 2000 configurato. Correggere i criteri nel computer peer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERRORE \_ della \_ \_ \_ versione principale IKE non valida IPSec \_**
</dt> <dd> <dl> <dt>

13880 (0x3638)
</dt> <dt>



Il destinatario non è in grado di gestire la versione di IKE specificata nell'intestazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERRORE \_ IPSec \_ IKE \_ non \_ valido \_ KEYLEN**
</dt> <dd> <dl> <dt>

13881 (0x3639)
</dt> <dt>



La lunghezza della chiave nel certificato è troppo piccola per i requisiti di sicurezza configurati.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**limite di errore \_ IKE per IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13882 (0x363A)
</dt> <dt>



Superato il numero massimo di SAs MM stabilite al peer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERRORE \_ di \_ negoziazione IKE IPSec \_ \_ disabilitato**
</dt> <dd> <dl> <dt>

13883 (0x363B)
</dt> <dt>



IKE ha ricevuto un criterio che disabilita la negoziazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**limite per l'errore \_ IPSec \_ IKE \_ \_**
</dt> <dd> <dl> <dt>

13884 (0x363C)
</dt> <dt>



È stato raggiunto il limite massimo della modalità rapida per la modalità principale. Verrà avviata la nuova modalità principale.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERRORE \_ IPSec \_ IKE \_ mm \_ scaduto**
</dt> <dd> <dl> <dt>

13885 (0x363D)
</dt> <dt>



Durata SA della modalità principale scaduta o peer inviato un'eliminazione in modalità principale.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**errore \_ del \_ peer IKE IPSec \_ \_ \_ in \_ errore**
</dt> <dd> <dl> <dt>

13886 (0x363E)
</dt> <dt>



Si presuppone che l'associazione di modalità principale non sia valida perché il peer ha smesso di rispondere.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERRORE \_ di \_ criteri catena di certificati IKE IPSec non \_ \_ \_ \_ corrispondenti**
</dt> <dd> <dl> <dt>

13887 (0x363F)
</dt> <dt>



Il certificato non viene concatenato a una radice attendibile nei criteri IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERRORE \_ \_ \_ ID messaggio imprevisto IKE IPSec \_ \_**
</dt> <dd> <dl> <dt>

13888 (0x3640)
</dt> <dt>



ID messaggio imprevisto ricevuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERRORE \_ IPSec \_ IKE \_ non \_ valido \_ payload di autenticazione**
</dt> <dd> <dl> <dt>

13889 (0x3641)
</dt> <dt>



Sono state ricevute offerte di autenticazione non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERRORE \_ del \_ \_ cookie DOS IKE IPSec \_ \_ inviato**
</dt> <dd> <dl> <dt>

13890 (0x3642)
</dt> <dt>



Notifica del cookie DoS inviata all'initiator.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERRORE \_ di \_ \_ arresto IKE IPSec \_**
</dt> <dd> <dl> <dt>

13891 (0x3643)
</dt> <dt>



Arresto del servizio IKE in corso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERRORE \_ di \_ autenticazione di IKE CGA per IPSec \_ \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

13892 (0x3644)
</dt> <dt>



Impossibile verificare l'associazione tra l'indirizzo CGA e il certificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERRORE \_ \_ processo IKE \_ IPSec \_ Err \_ Nato**
</dt> <dd> <dl> <dt>

13893 (0x3645)
</dt> <dt>



Errore durante l'elaborazione del payload NatO.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERRORE \_ \_ IKE IPSec \_ non valido \_ mm \_ per \_ QM**
</dt> <dd> <dl> <dt>

13894 (0x3646)
</dt> <dt>



I parametri della modalità principale non sono validi per questa modalità rapida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**errore per IPSec di IKE per errore \_ \_ \_ \_ scaduto**
</dt> <dd> <dl> <dt>

13895 (0x3647)
</dt> <dt>



La modalità rapida SA è scaduta dal driver IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERRORI \_ di \_ IKE IPSec \_ troppi \_ \_ filtri**
</dt> <dd> <dl> <dt>

13896 (0x3648)
</dt> <dt>



Sono stati rilevati troppi filtri IKEEXT aggiunti dinamicamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERRORE \_ di \_ stato neg IPSec IKE- \_ \_ \_ fine**
</dt> <dd> <dl> <dt>

13897 (0x3649)
</dt> <dt>



ERRORE \_ di \_ stato neg IPSec IKE- \_ \_ \_ fine


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERRORE \_ di \_ IPSec \_ Killing \_ \_ NAP del \_ tunnel**
</dt> <dd> <dl> <dt>

13898 (0x364A)
</dt> <dt>



La riautenticazione NAP è stata completata ed è necessario eliminare il tunnel IKEv2 del NAP fittizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**errore \_ di \_ \_ \_ assegnazione IP interno \_ IKE errore IPSec \_**
</dt> <dd> <dl> <dt>

13899 (0x364B)
</dt> <dt>



Errore durante l'assegnazione dell'indirizzo IP interno all'initiator in modalità tunnel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERRORE \_ IKE IPSec che \_ \_ richiede il \_ \_ payload CP \_ mancante**
</dt> <dd> <dl> <dt>

13900 (0x364C)
</dt> <dt>



Richiede il payload della configurazione mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERRORE \_ di \_ negoziazione della rappresentazione del modulo della chiave IPsec \_ \_ \_ \_ in sospeso**
</dt> <dd> <dl> <dt>

13901 (0x364D)
</dt> <dt>



Una negoziazione eseguita come principio di sicurezza che ha emesso la connessione è in corso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERRORE \_ di \_ \_ coesistenza IKE IPSec \_**
</dt> <dd> <dl> <dt>

13902 (0x364E)
</dt> <dt>



Il SA è stato eliminato a causa di una coesistenza IKEv1/AuthIP non è possibile verificare.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERRORE \_ \_ \_ eliminazione RATELIMIT IKE \_ IPSec**
</dt> <dd> <dl> <dt>

13903 (0x364F)
</dt> <dt>



La richiesta SA in ingresso è stata eliminata a causa della limitazione della frequenza degli indirizzi IP peer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERRORE \_ il \_ peer IKE IPSec non \_ \_ \_ supporta \_ MOBIKE**
</dt> <dd> <dl> <dt>

13904 (0x3650)
</dt> <dt>



Il peer non supporta MOBIKE.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERRORE \_ di \_ autorizzazione IKE IPSec \_ \_**
</dt> <dd> <dl> <dt>

13905 (0x3651)
</dt> <dt>



Associazione di sicurezza non autorizzata.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERRORE \_ di \_ \_ \_ autorizzazione creda \_ IKE con errore \_ IPSec**
</dt> <dd> <dl> <dt>

13906 (0x3652)
</dt> <dt>



Lo stabilimento SA non è autorizzato perché non sono presenti credenziali basate su PKINIT sufficientemente complesse.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERRORE \_ \_ di autorizzazione IKE IPSec errore \_ \_ \_ con \_ ripetizione facoltativa \_**
</dt> <dd> <dl> <dt>

13907 (0x3653)
</dt> <dt>



Associazione di sicurezza non autorizzata. Potrebbe essere necessario immettere credenziali aggiornate o diverse, ad esempio una smart card.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**errore \_ IPSec attendibile \_ IKE \_ \_ \_ \_ e \_ CERTMAP \_ errore**
</dt> <dd> <dl> <dt>

13908 (0x3654)
</dt> <dt>



Lo stabilimento SA non è autorizzato perché non sono presenti credenziali basate su PKINIT sufficientemente complesse. Questo potrebbe essere correlato a un errore di mapping da certificato a account per il SA.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERRORE \_ di \_ \_ stato neg IPSec IKE \_ stato \_ esteso \_**
</dt> <dd> <dl> <dt>

13909 (0x3655)
</dt> <dt>



ERRORE \_ di \_ \_ stato neg IPSec IKE \_ stato \_ esteso \_


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERRORE \_ SPI IPSec non \_ valido \_**
</dt> <dd> <dl> <dt>

13910 (0x3656)
</dt> <dt>



Il valore SPI nel pacchetto non corrisponde a un SA IPsec valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**\_ \_ Durata SA IPSec \_ errore \_ scaduta**
</dt> <dd> <dl> <dt>

13911 (0x3657)
</dt> <dt>



Il pacchetto è stato ricevuto su un SA IPsec la cui durata è scaduta.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**ERRORE \_ IPSec \_ errato del \_ sa**
</dt> <dd> <dl> <dt>

13912 (0x3658)
</dt> <dt>



Il pacchetto è stato ricevuto su un SA IPsec che non corrisponde alle caratteristiche del pacchetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERRORE \_ di \_ Verifica riproduzione \_ IPSec \_ non riuscita**
</dt> <dd> <dl> <dt>

13913 (0x3659)
</dt> <dt>



Controllo riproduzione numero di sequenza del pacchetto non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERRORE \_ del \_ pacchetto IPSec non valido \_**
</dt> <dd> <dl> <dt>

13914 (0x365A)
</dt> <dt>



L'intestazione IPsec e/o il trailer nel pacchetto non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**errore durante il \_ \_ controllo di integrità IPSec \_ \_**
</dt> <dd> <dl> <dt>

13915 (0x365B)
</dt> <dt>



Controllo integrità IPsec non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**\_eliminazione del \_ testo non crittografato IPsec \_ \_**
</dt> <dd> <dl> <dt>

13916 (0x365C)
</dt> <dt>



IPsec ha eliminato un pacchetto di testo non crittografato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERRORE \_ \_ \_ eliminazione firewall autenticazione \_ IPSec**
</dt> <dd> <dl> <dt>

13917 (0x365D)
</dt> <dt>



IPsec ha eliminato un pacchetto ESP in ingresso in modalità firewall autenticato. Questa eliminazione è benigna.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERRORE \_ di \_ eliminazione della limitazione IPSec \_**
</dt> <dd> <dl> <dt>

13918 (0x365E)
</dt> <dt>



IPsec ha eliminato un pacchetto a causa della limitazione delle richieste DoS.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERRORE \_ \_ blocco DoSP \_ IPSec**
</dt> <dd> <dl> <dt>

13925 (0x3665)
</dt> <dt>



La protezione DoS IPsec corrisponde a una regola di blocco esplicita.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERRORE \_ \_ DoSP IPSec \_ ricevuto dal \_ multicast**
</dt> <dd> <dl> <dt>

13926 (0x3666)
</dt> <dt>



La protezione DoS IPsec ha ricevuto un pacchetto multicast specifico per IPsec che non è consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERRORE \_ del \_ pacchetto DoSP IPSec \_ non valido \_**
</dt> <dd> <dl> <dt>

13927 (0x3667)
</dt> <dt>



La protezione DoS IPsec ha ricevuto un pacchetto formattato in modo errato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**errore durante la \_ \_ \_ ricerca dello stato DoSP \_ IPSec \_**
</dt> <dd> <dl> <dt>

13928 (0x3668)
</dt> <dt>



La protezione DoS IPsec non è riuscita a cercare lo stato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**\_ \_ \_ numero massimo di \_ voci DoSP IPSec**
</dt> <dd> <dl> <dt>

13929 (0x3669)
</dt> <dt>



La protezione DoS IPsec non è riuscita a creare lo stato perché è stato raggiunto il numero massimo di voci consentite dai criteri.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERRORE \_ IPSec \_ DoSP \_ KEYMOD \_ non \_ consentito**
</dt> <dd> <dl> <dt>

13930 (0x366A)
</dt> <dt>



La protezione DoS IPsec ha ricevuto un pacchetto di negoziazione IPsec per un modulo di chiavi non consentito dai criteri.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERRORE \_ \_ DoSP IPSec \_ non \_ installato**
</dt> <dd> <dl> <dt>

13931 (0x366B)
</dt> <dt>



La protezione DoS IPsec non è stata abilitata.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERRORE \_ IPSec \_ DoSP \_ Max \_ per \_ IP \_ RATELIMIT \_ code**
</dt> <dd> <dl> <dt>

13932 (0x366C)
</dt> <dt>



La protezione DoS IPsec non è riuscita a creare una coda per il limite di frequenza IP interno perché è stato raggiunto il numero massimo di code consentite dai criteri.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**\_sezione errore \_ SxS \_ non \_ trovata**
</dt> <dd> <dl> <dt>

14000 (0x36B0)
</dt> <dt>



La sezione richiesta non è presente nel contesto di attivazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERRORE \_ SxS \_ \_ ACTCTX generazione \_ non riuscita**
</dt> <dd> <dl> <dt>

14001 (0x36B1)
</dt> <dt>



Non è stato possibile avviare l'applicazione perché la configurazione affiancata non è corretta. Per informazioni dettagliate, vedere il registro eventi dell'applicazione o usare lo strumento della riga di comando sxstrace.exe.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERRORE \_ SxS \_ non \_ valido \_ formato ACTCTXDATA**
</dt> <dd> <dl> <dt>

14002 (0x36B2)
</dt> <dt>



Il formato dei dati di associazione dell'applicazione non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERRORE \_ dell' \_ assembly SxS \_ non \_ trovato**
</dt> <dd> <dl> <dt>

14003 (0x36B3)
</dt> <dt>



L'assembly a cui si fa riferimento non è installato nel sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**\_errore di \_ \_ formato manifesto SxS errore \_**
</dt> <dd> <dl> <dt>

14004 (0x36B4)
</dt> <dt>



Il file manifesto non inizia con il tag e le informazioni di formato richiesti.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**errore \_ di \_ analisi del manifesto SxS \_ errore \_**
</dt> <dd> <dl> <dt>

14005 (0x36B5)
</dt> <dt>



Il file manifesto contiene uno o più errori di sintassi.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**\_contesto di attivazione SxS di errore \_ \_ \_ disabilitato**
</dt> <dd> <dl> <dt>

14006 (0x36B6)
</dt> <dt>



L'applicazione ha tentato di attivare un contesto di attivazione disabilitato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**\_chiave SxS di errore \_ \_ non \_ trovata**
</dt> <dd> <dl> <dt>

14007 (0x36B7)
</dt> <dt>



La chiave di ricerca richiesta non è stata trovata in alcun contesto di attivazione attiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**\_ \_ conflitto versione SxS \_ errore**
</dt> <dd> <dl> <dt>

14008 (0x36B8)
</dt> <dt>



Una versione del componente richiesta dall'applicazione è in conflitto con un'altra versione del componente già attiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERRORE \_ SxS \_ \_ tipo di sezione errato \_**
</dt> <dd> <dl> <dt>

14009 (0x36B9)
</dt> <dt>



Il tipo della sezione del contesto di attivazione richiesta non corrisponde all'API di query usata.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**\_ \_ query thread SxS \_ errore \_ disabilitata**
</dt> <dd> <dl> <dt>

14010 (0x36BA)
</dt> <dt>



La mancanza di risorse di sistema ha richiesto l'attivazione isolata per essere disabilitata per il thread di esecuzione corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERRORE \_ SxS \_ processo \_ predefinito \_ già \_ impostato**
</dt> <dd> <dl> <dt>

14011 (0x36BB)
</dt> <dt>



Tentativo di impostazione del contesto di attivazione predefinito del processo non riuscito perché il contesto di attivazione predefinito del processo è già stato impostato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERRORE \_ SxS \_ \_ gruppo di codifica sconosciuto \_**
</dt> <dd> <dl> <dt>

14012 (0x36BC)
</dt> <dt>



L'identificatore del gruppo di codifica specificato non è riconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERRORE \_ SxS \_ \_ codifica sconosciuta**
</dt> <dd> <dl> <dt>

14013 (0x36BD)
</dt> <dt>



La codifica richiesta non è riconosciuta.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERRORE \_ SxS \_ non \_ valido \_ URI dello spazio dei nomi XML \_**
</dt> <dd> <dl> <dt>

14014 (0x36BE)
</dt> <dt>



Il manifesto contiene un riferimento a un URI non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**\_ \_ dipendenza manifesto radice errore SxS \_ \_ \_ non \_ installata**
</dt> <dd> <dl> <dt>

14015 (0x36BF)
</dt> <dt>



Il manifesto dell'applicazione contiene un riferimento a un assembly dipendente che non è installato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**\_ \_ dipendenza manifesto foglia errore SxS \_ \_ \_ non \_ installata**
</dt> <dd> <dl> <dt>

14016 (0x36C0)
</dt> <dt>



Il manifesto di un assembly utilizzato dall'applicazione contiene un riferimento a un assembly dipendente che non è installato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERRORE \_ SxS \_ \_ \_ attributo identità assembly non valido \_**
</dt> <dd> <dl> <dt>

14017 (0x36C1)
</dt> <dt>



Il manifesto contiene un attributo per l'identità dell'assembly non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**il \_ manifesto SxS errore \_ \_ manca \_ \_ \_ lo spazio dei nomi predefinito obbligatorio**
</dt> <dd> <dl> <dt>

14018 (0x36C2)
</dt> <dt>



Nel manifesto manca la specifica dello spazio dei nomi predefinita richiesta nell'elemento assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERRORE \_ del \_ manifesto SxS \_ non valido. \_ \_ \_ spazio dei nomi predefinito obbligatorio**
</dt> <dd> <dl> <dt>

14019 (0x36C3)
</dt> <dt>



Per il manifesto è stato specificato uno spazio dei nomi predefinito nell'elemento assembly, ma il relativo valore non è "urn: schemas-microsoft-com: ASM. V1".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERRORE \_ SxS \_ privato del \_ manifesto privato \_ \_ \_ con \_ punto di analisi \_**
</dt> <dd> <dl> <dt>

14020 (0x36C4)
</dt> <dt>



Il manifesto privato Probe ha superato un percorso con un reparse point non supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERRORE \_ SxS \_ \_ nome dll duplicato \_**
</dt> <dd> <dl> <dt>

14021 (0x36C5)
</dt> <dt>



Due o più componenti a cui viene fatto riferimento direttamente o indirettamente dal manifesto dell'applicazione hanno file con lo stesso nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERRORE \_ SxS \_ duplicato \_ WINDOWCLASS \_ nome**
</dt> <dd> <dl> <dt>

14022 (0x36C6)
</dt> <dt>



Due o più componenti a cui viene fatto riferimento direttamente o indirettamente dal manifesto dell'applicazione hanno classi finestra con lo stesso nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**\_ \_ CLSID duplicato errore SxS \_**
</dt> <dd> <dl> <dt>

14023 (0x36C7)
</dt> <dt>



Due o più componenti a cui viene fatto riferimento in modo diretto o indiretto dal manifesto dell'applicazione hanno gli stessi CLSID del server COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**\_ \_ IID duplicato errore SxS \_**
</dt> <dd> <dl> <dt>

14024 (0x36C8)
</dt> <dt>



Due o più componenti a cui viene fatto riferimento direttamente o indirettamente dal manifesto dell'applicazione hanno proxy per la stessa interfaccia COM IID.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERRORE \_ SxS \_ duplicato \_ TLBID**
</dt> <dd> <dl> <dt>

14025 (0x36C9)
</dt> <dt>



Due o più componenti a cui viene fatto riferimento direttamente o indirettamente dal manifesto dell'applicazione hanno lo stesso TLBIDs della libreria dei tipi COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**\_ \_ ProgID duplicato errore SxS \_**
</dt> <dd> <dl> <dt>

14026 (0x36CA)
</dt> <dt>



Due o più componenti a cui viene fatto riferimento in modo diretto o indiretto dal manifesto dell'applicazione hanno gli stessi ProgID COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERRORE \_ SxS \_ duplicato \_ \_ nome assembly**
</dt> <dd> <dl> <dt>

14027 (0x36CB)
</dt> <dt>



Due o più componenti a cui viene fatto riferimento in modo diretto o indiretto dal manifesto dell'applicazione sono versioni diverse dello stesso componente. questa operazione non è consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERRORE \_ di \_ hash file SxS non \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

14028 (0x36CC)
</dt> <dt>



Il file di un componente non corrisponde alle informazioni di verifica presenti nel manifesto del componente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**errore \_ di \_ analisi criteri SxS \_ errore \_**
</dt> <dd> <dl> <dt>

14029 (0x36CD)
</dt> <dt>



Il manifesto dei criteri contiene uno o più errori di sintassi.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERRORE \_ SxS \_ XML \_ E \_ MISSINGQUOTE**
</dt> <dd> <dl> <dt>

14030 (0x36CE)
</dt> <dt>



Errore di analisi del manifesto: è previsto un valore letterale stringa, ma non è stato trovato alcun carattere virgolette di apertura.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERRORE \_ SxS \_ XML \_ E \_ COMMENTSYNTAX**
</dt> <dd> <dl> <dt>

14031 (0x36CF)
</dt> <dt>



Errore di analisi del manifesto: sintassi non corretta in un commento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERRORE \_ SxS \_ XML \_ E \_ BADSTARTNAMECHAR**
</dt> <dd> <dl> <dt>

14032 (0x36D0)
</dt> <dt>



Errore di analisi del manifesto: è stato avviato un nome con un carattere non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERRORE \_ SxS \_ XML \_ E \_ BADNAMECHAR**
</dt> <dd> <dl> <dt>

14033 (0x36D1)
</dt> <dt>



Errore di analisi del manifesto: un nome contiene un carattere non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERRORE \_ SxS \_ XML \_ E \_ BADCHARINSTRING**
</dt> <dd> <dl> <dt>

14034 (0x36D2)
</dt> <dt>



Errore di analisi del manifesto: un valore letterale stringa contiene un carattere non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERRORE \_ SxS \_ XML \_ E \_ XMLDECLSYNTAX**
</dt> <dd> <dl> <dt>

14035 (0x36D3)
</dt> <dt>



Errore di analisi del manifesto: sintassi non valida per una dichiarazione XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERRORE \_ SxS \_ XML \_ E \_ BADCHARDATA**
</dt> <dd> <dl> <dt>

14036 (0x36D4)
</dt> <dt>



Errore di analisi del manifesto: è stato trovato un carattere non valido nel contenuto di testo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERRORE \_ SxS \_ XML \_ E \_ MISSINGWHITESPACE**
</dt> <dd> <dl> <dt>

14037 (0x36D5)
</dt> <dt>



Errore di analisi del manifesto: manca lo spazio vuoto obbligatorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERRORE \_ SxS \_ XML \_ E \_ EXPECTINGTAGEND**
</dt> <dd> <dl> <dt>

14038 (0x36D6)
</dt> <dt>



Errore di analisi del manifesto: previsto il carattere ' >'.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERRORE \_ SxS \_ XML \_ E \_ MISSINGSEMICOLON**
</dt> <dd> <dl> <dt>

14039 (0x36D7)
</dt> <dt>



Errore di analisi del manifesto: previsto punto e virgola.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNBALANCEDPAREN**
</dt> <dd> <dl> <dt>

14040 (0x36D8)
</dt> <dt>



Errore di analisi del manifesto: parentesi non bilanciate.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERRORE \_ SxS \_ XML \_ E \_ INTERNALERROR**
</dt> <dd> <dl> <dt>

14041 (0x36D9)
</dt> <dt>



Errore di analisi del manifesto: errore interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERRORE \_ SxS \_ XML \_ E \_ \_ spazio vuoto imprevisto**
</dt> <dd> <dl> <dt>

14042 (0x36DA)
</dt> <dt>



Errore di analisi del manifesto: lo spazio vuoto non è consentito in questa posizione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERRORE \_ SxS \_ XML \_ E \_ codifica incompleta \_**
</dt> <dd> <dl> <dt>

14043 (0x36DB)
</dt> <dt>



Errore di analisi del manifesto: la fine del file è stata raggiunta in stato non valido per la codifica corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERRORE \_ SxS \_ XML \_ E \_ \_ parentesi mancante**
</dt> <dd> <dl> <dt>

14044 (0x36DC)
</dt> <dt>



Errore di analisi del manifesto: parentesi mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERRORE \_ SxS \_ XML \_ E \_ EXPECTINGCLOSEQUOTE**
</dt> <dd> <dl> <dt>

14045 (0x36DD)
</dt> <dt>



Errore di analisi del manifesto: virgolette di chiusura singole o doppie ( \\ ' o \\ ") mancanti.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERROR \_ SxS \_ XML \_ E \_ più \_ due punti**
</dt> <dd> <dl> <dt>

14046 (0x36DE)
</dt> <dt>



Errore di analisi del manifesto: non sono consentiti più due punti in un nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERRORE \_ SxS \_ XML \_ E \_ \_ decimale non valido**
</dt> <dd> <dl> <dt>

14047 (0x36DF)
</dt> <dt>



Errore di analisi del manifesto: carattere non valido per la cifra decimale.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERRORE \_ SxS \_ XML \_ E \_ esadecimali non valido \_**
</dt> <dd> <dl> <dt>

14048 (0x36E0)
</dt> <dt>



Errore di analisi del manifesto: carattere non valido per la cifra esadecimale.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERROR \_ SxS \_ XML \_ E \_ Unicode non valido \_**
</dt> <dd> <dl> <dt>

14049 (0x36E1)
</dt> <dt>



Errore di analisi del manifesto: valore del carattere Unicode non valido per questa piattaforma.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERRORE \_ SxS \_ XML \_ E \_ WHITESPACEORQUESTIONMARK**
</dt> <dd> <dl> <dt>

14050 (0x36E2)
</dt> <dt>



Errore di analisi del manifesto: è previsto uno spazio vuoto o '?'.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNEXPECTEDENDTAG**
</dt> <dd> <dl> <dt>

14051 (0x36E3)
</dt> <dt>



Errore di analisi del manifesto: il tag di fine non era previsto in questa posizione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNCLOSEDTAG**
</dt> <dd> <dl> <dt>

14052 (0x36E4)
</dt> <dt>



Errore di analisi del manifesto: i seguenti tag non sono stati chiusi: %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERRORE \_ SxS \_ XML \_ E \_ DUPLICATEATTRIBUTE**
</dt> <dd> <dl> <dt>

14053 (0x36E5)
</dt> <dt>



Errore di analisi del manifesto: attributo duplicato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERRORE \_ SxS \_ XML \_ E \_ MULTIPLEROOTS**
</dt> <dd> <dl> <dt>

14054 (0x36E6)
</dt> <dt>



Errore di analisi del manifesto: in un documento XML è consentito un solo elemento di primo livello.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERRORE \_ SxS \_ XML \_ E \_ INVALIDATROOTLEVEL**
</dt> <dd> <dl> <dt>

14055 (0x36E7)
</dt> <dt>



Errore di analisi del manifesto: non valido al livello principale del documento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERRORE \_ SxS \_ XML \_ E \_ BADXMLDECL**
</dt> <dd> <dl> <dt>

14056 (0x36E8)
</dt> <dt>



Errore di analisi del manifesto: dichiarazione XML non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERRORE \_ SxS \_ XML \_ E \_ MISSINGROOT**
</dt> <dd> <dl> <dt>

14057 (0x36E9)
</dt> <dt>



Errore di analisi del manifesto: il documento XML deve contenere un elemento di livello principale.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNEXPECTEDEOF**
</dt> <dd> <dl> <dt>

14058 (0x36EA)
</dt> <dt>



Errore di analisi del manifesto: fine del file imprevista.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERRORE \_ SxS \_ XML \_ E \_ BADPEREFINSUBSET**
</dt> <dd> <dl> <dt>

14059 (0x36EB)
</dt> <dt>



Errore di analisi del manifesto: le entità parametro non possono essere usate nelle dichiarazioni di markup in un subset interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNCLOSEDSTARTTAG**
</dt> <dd> <dl> <dt>

14060 (0x36EC)
</dt> <dt>



Errore di analisi del manifesto: l'elemento non è stato chiuso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNCLOSEDENDTAG**
</dt> <dd> <dl> <dt>

14061 (0x36ED)
</dt> <dt>



Errore di analisi del manifesto: nell'elemento End manca il carattere ' >'.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNCLOSEDSTRING**
</dt> <dd> <dl> <dt>

14062 (0x36EE)
</dt> <dt>



Errore di analisi del manifesto: un valore letterale stringa non è stato chiuso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNCLOSEDCOMMENT**
</dt> <dd> <dl> <dt>

14063 (0x36EF)
</dt> <dt>



Errore di analisi del manifesto: un commento non è stato chiuso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNCLOSEDDECL**
</dt> <dd> <dl> <dt>

14064 (0x36F0)
</dt> <dt>



Errore di analisi del manifesto: una dichiarazione non è stata chiusa.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNCLOSEDCDATA**
</dt> <dd> <dl> <dt>

14065 (0x36F1)
</dt> <dt>



Errore di analisi del manifesto: una sezione CDATA non è stata chiusa.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERRORE \_ SxS \_ XML \_ E \_ RESERVEDNAMESPACE**
</dt> <dd> <dl> <dt>

14066 (0x36F2)
</dt> <dt>



Errore di analisi del manifesto: il prefisso dello spazio dei nomi non può iniziare con la stringa riservata "XML".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERRORE \_ SxS \_ XML \_ E \_ INVALIDENCODING**
</dt> <dd> <dl> <dt>

14067 (0x36F3)
</dt> <dt>



Errore di analisi del manifesto: il sistema non supporta la codifica specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERRORE \_ SxS \_ XML \_ E \_ INVALIDSWITCH**
</dt> <dd> <dl> <dt>

14068 (0x36F4)
</dt> <dt>



Errore di analisi del manifesto: l'opzione dalla codifica corrente alla codifica specificata non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERRORE \_ SxS \_ XML \_ E \_ BADXMLCASE**
</dt> <dd> <dl> <dt>

14069 (0x36F5)
</dt> <dt>



Errore di analisi del manifesto: il nome "XML" è riservato e deve essere in lettere minuscole.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERRORE \_ SxS \_ XML \_ E \_ \_ autonomo non valido**
</dt> <dd> <dl> <dt>

14070 (0x36F6)
</dt> <dt>



Errore di analisi del manifesto: il valore dell'attributo standalone deve essere ' Yes ' o ' No '.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERROR \_ SxS \_ XML \_ E \_ imprevisto \_ autonomo**
</dt> <dd> <dl> <dt>

14071 (0x36F7)
</dt> <dt>



Errore di analisi del manifesto: l'attributo standalone non può essere utilizzato in entità esterne.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERRORE \_ SxS \_ XML \_ E \_ versione non valida \_**
</dt> <dd> <dl> <dt>

14072 (0x36F8)
</dt> <dt>



Errore di analisi del manifesto: numero di versione non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERRORE \_ SxS \_ XML \_ E \_ MISSINGEQUALS**
</dt> <dd> <dl> <dt>

14073 (0x36F9)
</dt> <dt>



Errore di analisi del manifesto: manca il segno di uguale tra l'attributo e il valore dell'attributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**errore durante il \_ \_ ripristino della protezione SxS \_ \_**
</dt> <dd> <dl> <dt>

14074 (0x36FA)
</dt> <dt>



Errore di protezione dell'assembly: Impossibile recuperare l'assembly specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**\_chiave pubblica di errore SxS \_ Protection \_ \_ \_ troppo \_ breve**
</dt> <dd> <dl> <dt>

14075 (0x36FB)
</dt> <dt>



Errore di protezione dell'assembly: la chiave pubblica per un assembly è troppo corta per essere consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERRORE \_ \_ Catalogo protezione \_ SxS \_ non \_ valido**
</dt> <dd> <dl> <dt>

14076 (0x36FC)
</dt> <dt>



Errore di protezione dell'assembly: il catalogo di un assembly non è valido o non corrisponde al manifesto dell'assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERRORE \_ SxS non \_ convertibile \_ SxS**
</dt> <dd> <dl> <dt>

14077 (0x36FD)
</dt> <dt>



Non è stato possibile convertire un valore HRESULT in un codice di errore Win32 corrispondente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**errore \_ nel \_ \_ file di catalogo della protezione \_ SxS errore \_**
</dt> <dd> <dl> <dt>

14078 (0x36FE)
</dt> <dt>



Errore di protezione dell'assembly: manca il catalogo di un assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**\_attributo di \_ \_ identità assembly \_ mancante \_ nell'errore SxS**
</dt> <dd> <dl> <dt>

14079 (0x36FF)
</dt> <dt>



Nell'identità dell'assembly specificata mancano uno o più attributi che devono essere presenti in questo contesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERRORE \_ SxS \_ \_ \_ \_ nome attributo identità assembly \_ non valido**
</dt> <dd> <dl> <dt>

14080 (0x3700)
</dt> <dt>



L'identità dell'assembly fornita ha uno o più nomi di attributo che contengono caratteri non consentiti nei nomi XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERRORE \_ \_ assembly SxS \_ mancante**
</dt> <dd> <dl> <dt>

14081 (0x3701)
</dt> <dt>



Impossibile trovare l'assembly a cui si fa riferimento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**\_stack di \_ \_ attivazione danneggiato SxS di \_ errore**
</dt> <dd> <dl> <dt>

14082 (0x3702)
</dt> <dt>



Lo stack di attivazione del contesto di attivazione per il thread in esecuzione è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**\_ \_ danneggiamento SxS errore**
</dt> <dd> <dl> <dt>

14083 (0x3703)
</dt> <dt>



I metadati di isolamento dell'applicazione per questo processo o thread sono diventati danneggiati.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERRORE \_ SxS \_ prima di \_ disattivazione**
</dt> <dd> <dl> <dt>

14084 (0x3704)
</dt> <dt>



Il contesto di attivazione da disattivare non è quello attivato più di recente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERRORE \_ SxS \_ non valido di \_ disattivazione**
</dt> <dd> <dl> <dt>

14085 (0x3705)
</dt> <dt>



Il contesto di attivazione da disattivare non è attivo per il thread di esecuzione corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERRORE \_ SxS \_ più \_ disattivazione**
</dt> <dd> <dl> <dt>

14086 (0x3706)
</dt> <dt>



Il contesto di attivazione disattivato è già stato disattivato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**\_terminazione del processo SxS di errore \_ \_ \_ richiesta**
</dt> <dd> <dl> <dt>

14087 (0x3707)
</dt> <dt>



Un componente utilizzato dalla funzionalità di isolamento ha richiesto l'interruzione del processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**\_contesto di \_ attivazione della versione SxS \_ di errore \_**
</dt> <dd> <dl> <dt>

14088 (0x3708)
</dt> <dt>



Un componente in modalità kernel sta rilasciando un riferimento in un contesto di attivazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERRORE \_ nel \_ \_ contesto di attivazione predefinito del sistema SxS \_ \_ \_ vuoto**
</dt> <dd> <dl> <dt>

14089 (0x3709)
</dt> <dt>



Impossibile generare il contesto di attivazione dell'assembly predefinito di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERRORE \_ SxS \_ \_ valore dell' \_ attributo \_ Identity non valido**
</dt> <dd> <dl> <dt>

14090 (0x370A)
</dt> <dt>



Il valore di un attributo in un'identità non è compreso nell'intervallo valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERRORE \_ SxS \_ \_ \_ nome attributo identità non valido \_**
</dt> <dd> <dl> <dt>

14091 (0x370B)
</dt> <dt>



Il nome di un attributo in un'identità non è compreso nell'intervallo valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**\_ \_ \_ attributo duplicato identità SxS errore \_**
</dt> <dd> <dl> <dt>

14092 (0x370C)
</dt> <dt>



Un'identità contiene due definizioni per lo stesso attributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**errore \_ di \_ analisi identità SxS \_ errore \_**
</dt> <dd> <dl> <dt>

14093 (0x370D)
</dt> <dt>



Il formato della stringa di identità non è valido. Questo problema può essere dovuto a una virgola finale, a più di due attributi senza nome, a un nome di attributo mancante o a un valore di attributo mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERRORE \_ stringa di \_ sostituzione non valido \_**
</dt> <dd> <dl> <dt>

14094 (0x370E)
</dt> <dt>



Formato non corretto di una stringa contenente contenuto sostituibile localizzato. Un segno di dollaro ($) è stato seguito da un elemento diverso da una parentesi aperta o da un altro segno di dollaro o dalla parentesi destra di una sostituzione non trovata.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERRORE \_ SxS \_ \_ chiave pubblica non corretta \_ \_**
</dt> <dd> <dl> <dt>

14095 (0x370F)
</dt> <dt>



Il token di chiave pubblica non corrisponde alla chiave pubblica specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**errore durante il \_ mapping della \_ stringa di sostituzione \_**
</dt> <dd> <dl> <dt>

14096 (0x3710)
</dt> <dt>



Una stringa di sostituzione non ha alcun mapping.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERRORE \_ \_ assembly SxS \_ non \_ bloccato**
</dt> <dd> <dl> <dt>

14097 (0x3711)
</dt> <dt>



Prima di eseguire la richiesta, è necessario bloccare il componente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERRORE \_ \_ archivio componenti \_ SxS \_ danneggiato**
</dt> <dd> <dl> <dt>

14098 (0x3712)
</dt> <dt>



L'archivio componenti è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERRORE \_ del \_ programma di installazione avanzato \_ non riuscito**
</dt> <dd> <dl> <dt>

14099 (0x3713)
</dt> <dt>



Un programma di installazione avanzato non è riuscito durante l'installazione o la manutenzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**ERRORE \_ di \_ codifica XML non \_ corrispondente**
</dt> <dd> <dl> <dt>

14100 (0x3714)
</dt> <dt>



La codifica dei caratteri nella dichiarazione XML non corrisponde alla codifica utilizzata nel documento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**errore di identità del manifesto SxS di errore, \_ \_ \_ \_ \_ ma \_ contenuto \_ diverso**
</dt> <dd> <dl> <dt>

14101 (0x3715)
</dt> <dt>



Le identità dei manifesti sono identiche, ma il relativo contenuto è diverso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**\_identità SxS di errore \_ \_ diverse**
</dt> <dd> <dl> <dt>

14102 (0x3716)
</dt> <dt>



Le identità dei componenti sono diverse.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**\_ \_ l'assembly SxS \_ \_ di errore non è \_ una \_ distribuzione**
</dt> <dd> <dl> <dt>

14103 (0x3717)
</dt> <dt>



L'assembly non è una distribuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERRORE \_ SxS \_ file \_ non \_ fa parte \_ dell' \_ assembly**
</dt> <dd> <dl> <dt>

14104 (0x3718)
</dt> <dt>



Il file non fa parte dell'assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**\_manifesto SxS \_ errore \_ troppo \_ grande**
</dt> <dd> <dl> <dt>

14105 (0x3719)
</dt> <dt>



Le dimensioni del manifesto superano il valore massimo consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**\_impostazione errore \_ SxS \_ non \_ registrata**
</dt> <dd> <dl> <dt>

14106 (0x371A)
</dt> <dt>



L'impostazione non è registrata.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERRORE \_ di \_ chiusura della transazione SxS \_ \_ incompleta**
</dt> <dd> <dl> <dt>

14107 (0x371B)
</dt> <dt>



Uno o più membri obbligatori della transazione non sono presenti.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERRORE \_ del \_ programma di installazione primitive SMI \_ \_ non riuscito**
</dt> <dd> <dl> <dt>

14108 (0x371C)
</dt> <dt>



Il programma di installazione primitive SMI non è riuscito durante l'installazione o la manutenzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**ERRORE \_ \_ comando generico \_ non riuscito**
</dt> <dd> <dl> <dt>

14109 (0x371D)
</dt> <dt>



Un eseguibile del comando generico ha restituito un risultato che indica un errore.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**\_ \_ hash file SxS \_ errore \_ mancante**
</dt> <dd> <dl> <dt>

14110 (0x371E)
</dt> <dt>



Nel manifesto di un componente mancano le informazioni di verifica del file.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERRORE \_ evt \_ \_ percorso del canale non valido \_**
</dt> <dd> <dl> <dt>

15000 (0x3A98)
</dt> <dt>



Il percorso del canale specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERRORE \_ evt \_ query non valida \_**
</dt> <dd> <dl> <dt>

15001 (0x3A99)
</dt> <dt>



La query specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERRORE \_ evt \_ pubblicazione \_ metadati \_ non \_ trovati**
</dt> <dd> <dl> <dt>

15002 (0x3A9A)
</dt> <dt>



Impossibile trovare i metadati del server di pubblicazione nella risorsa.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERRORE \_ evt \_ modello di evento \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

15003 (0x3A9B)
</dt> <dt>



Il modello per la definizione di un evento non è stato trovato nella risorsa (errore = %1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERRORE \_ evt \_ \_ nome dell'autore non valido \_**
</dt> <dd> <dl> <dt>

15004 (0x3A9C)
</dt> <dt>



Il nome del server di pubblicazione specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERRORE \_ evt \_ \_ dati evento non validi \_**
</dt> <dd> <dl> <dt>

15005 (0x3A9D)
</dt> <dt>



I dati dell'evento generati dal server di pubblicazione non sono compatibili con la definizione del modello di evento nel manifesto del server di pubblicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERRORE \_ \_ canale evt \_ non \_ trovato**
</dt> <dd> <dl> <dt>

15007 (0x3A9F)
</dt> <dt>



Il canale specificato non è stato trovato. Controllare la configurazione del canale.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERRORE \_ evt \_ \_ testo XML non valido \_**
</dt> <dd> <dl> <dt>

15008 (0x3AA0)
</dt> <dt>



Il testo XML specificato non è ben formato. Per ulteriori informazioni, vedere l'errore esteso.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERRORE \_ evt \_ sottoscrizione \_ al \_ \_ canale diretto**
</dt> <dd> <dl> <dt>

15009 (0x3AA1)
</dt> <dt>



Il chiamante sta provando a sottoscrivere un canale diretto che non è consentito. Gli eventi per un canale diretto passano direttamente a un file di log e non possono essere sottoscritti.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**errore \_ di \_ configurazione di evt \_**
</dt> <dd> <dl> <dt>

15010 (0x3AA2)
</dt> <dt>



Errore di configurazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERRORE il \_ risultato della query evt non è \_ \_ \_ aggiornato**
</dt> <dd> <dl> <dt>

15011 (0x3AA3)
</dt> <dt>



Il risultato della query non è aggiornato o non è valido. Questo problema può essere dovuto al fatto che il log è stato cancellato o spostato dopo la creazione del risultato della query. Gli utenti devono gestire questo codice rilasciando l'oggetto risultato della query ed eseguendo nuovamente la query.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERRORE \_ il \_ risultato della query evt \_ \_ posizione non valida \_**
</dt> <dd> <dl> <dt>

15012 (0x3AA4)
</dt> <dt>



Il risultato della query si trova attualmente in una posizione non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERRORE \_ evt \_ non \_ convalida \_ MSXML**
</dt> <dd> <dl> <dt>

15013 (0x3AA5)
</dt> <dt>



MSXML registrato non supporta la convalida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERRORE \_ evt \_ filtro \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014 (0x3AA6)
</dt> <dt>



Un'espressione può essere seguita solo da una modifica dell'operazione di ambito se restituisce un set di nodi e non fa già parte di un'altra modifica dell'operazione dell'ambito.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERRORE \_ evt \_ filtro \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015 (0x3AA7)
</dt> <dt>



Non è possibile eseguire un'operazione step da un termine che non rappresenta un set di elementi.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERRORE \_ evt \_ filtro \_ INVARG**
</dt> <dd> <dl> <dt>

15016 (0x3AA8)
</dt> <dt>



Gli argomenti del lato sinistro per gli operatori binari devono essere attributi, nodi o variabili e gli argomenti lato destro devono essere costanti.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERRORE \_ evt \_ filtro \_ INVTEST**
</dt> <dd> <dl> <dt>

15017 (0x3AA9)
</dt> <dt>



Un'operazione Step deve coinvolgere un test di nodo o, nel caso di un predicato, un'espressione algebrica sulla quale testare ogni nodo nel set di nodi identificato dal set di nodi precedente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERRORE \_ evt \_ filtro \_ INVTYPE**
</dt> <dd> <dl> <dt>

15018 (0x3AAA)
</dt> <dt>



Questo tipo di dati non è attualmente supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERRORE \_ evt \_ filtro \_ PARSEERR**
</dt> <dd> <dl> <dt>

15019 (0x3AAB)
</dt> <dt>



Si è verificato un errore di sintassi nella posizione %1! d!.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERRORE \_ evt \_ filtro \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020 (0x3AAC)
</dt> <dt>



Questo operatore non è supportato da questa implementazione del filtro.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERRORE \_ evt \_ filtro \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021 (0x3AAD)
</dt> <dt>



Il token rilevato è imprevisto.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERRORE \_ evt \_ \_ operazione non \_ valida \_ su \_ canale diretto abilitato \_**
</dt> <dd> <dl> <dt>

15022 (0x3AAE)
</dt> <dt>



L'operazione richiesta non può essere eseguita su un canale diretto abilitato. Il canale deve prima essere disabilitato prima di eseguire l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERRORE \_ evt \_ \_ valore della \_ proprietà del canale non valido \_**
</dt> <dd> <dl> <dt>

15023 (0x3AAF)
</dt> <dt>



Proprietà canale %1! s! contiene un valore non valido. Il valore di tipo non valido, non è compreso nell'intervallo valido, non può essere aggiornato o non è supportato da questo tipo di canale.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERRORE \_ evt \_ valore della proprietà del server di pubblicazione non valido \_ \_ \_**
</dt> <dd> <dl> <dt>

15024 (0x3AB0)
</dt> <dt>



Proprietà server di pubblicazione %1! s! contiene un valore non valido. Il valore di tipo non valido, non è compreso nell'intervallo valido, non può essere aggiornato o non è supportato da questo tipo di server di pubblicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERRORE \_ \_ \_ non è possibile attivare il canale evt \_**
</dt> <dd> <dl> <dt>

15025 (0x3AB1)
</dt> <dt>



Non è possibile attivare il canale.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERRORE \_ \_ filtro evt \_ troppo \_ complesso**
</dt> <dd> <dl> <dt>

15026 (0x3AB2)
</dt> <dt>



L'espressione XPath ha superato la complessità supportata. Symplify o suddividerlo in due o più espressioni semplici.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERRORE \_ evt \_ messaggio \_ non \_ trovato**
</dt> <dd> <dl> <dt>

15027 (0x3AB3)
</dt> <dt>



la risorsa messaggio è presente, ma il messaggio non viene trovato nella tabella stringa/messaggio.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERRORE \_ evt \_ \_ ID messaggio \_ non \_ trovato**
</dt> <dd> <dl> <dt>

15028 (0x3AB4)
</dt> <dt>



Impossibile trovare l'ID di messaggio per il messaggio desiderato.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERRORE \_ evt \_ \_ inserimento valore non risolto \_**
</dt> <dd> <dl> <dt>

15029 (0x3AB5)
</dt> <dt>



Impossibile trovare la stringa di sostituzione per l'indice di inserimento (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERRORE \_ evt \_ \_ inserimento parametro non risolto \_**
</dt> <dd> <dl> <dt>

15030 (0x3AB6)
</dt> <dt>



Impossibile trovare la stringa di descrizione per il riferimento al parametro (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERRORE \_ evt \_ numero massimo di \_ inserimenti \_ raggiunti**
</dt> <dd> <dl> <dt>

15031 (0x3AB7)
</dt> <dt>



È stato raggiunto il numero massimo di sostituzioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERRORE \_ evt \_ \_ \_ Impossibile trovare la definizione dell'evento \_**
</dt> <dd> <dl> <dt>

15032 (0x3AB8)
</dt> <dt>



Impossibile trovare la definizione dell'evento per l'ID evento (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERRORE \_ nelle \_ \_ impostazioni locali del messaggio evt \_ non \_ trovato**
</dt> <dd> <dl> <dt>

15033 (0x3AB9)
</dt> <dt>



La risorsa specifica delle impostazioni locali per il messaggio desiderato non è presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERRORE \_ evt \_ versione \_ troppo \_ vecchia**
</dt> <dd> <dl> <dt>

15034 (0x3ABA)
</dt> <dt>



La risorsa è troppo vecchia per essere compatibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERRORE \_ evt \_ versione \_ troppo \_ nuova**
</dt> <dd> <dl> <dt>

15035 (0x3ABB)
</dt> <dt>



La risorsa è troppo nuova per essere compatibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERRORE \_ evt \_ Impossibile \_ aprire il \_ canale \_ della \_ query**
</dt> <dd> <dl> <dt>

15036 (0x3ABC)
</dt> <dt>



Il canale in corrispondenza dell'indice %1! d! non è possibile aprire la query.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERRORE \_ evt \_ Autore \_ disabilitato**
</dt> <dd> <dl> <dt>

15037 (0x3ABD)
</dt> <dt>



Il server di pubblicazione è stato disabilitato e la relativa risorsa non è disponibile. Questo problema si verifica in genere quando è in corso la disinstallazione o l'aggiornamento del server di pubblicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERRORE \_ evt \_ filtro \_ non \_ \_ compreso nell'intervallo**
</dt> <dd> <dl> <dt>

15038 (0x3ABE)
</dt> <dt>



Tentativo di creare un tipo numerico non compreso nell'intervallo valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERRORE \_ \_ \_ non è possibile attivare la sottoscrizione EC \_**
</dt> <dd> <dl> <dt>

15080 (0x3AE8)
</dt> <dt>



Non è possibile attivare la sottoscrizione.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERRORE \_ \_ Registro EC \_ disabilitato**
</dt> <dd> <dl> <dt>

15081 (0x3AE9)
</dt> <dt>



Il log della sottoscrizione è in stato disabilitato e non può essere utilizzato per l'invio di eventi a. Il log deve prima essere abilitato prima di poter attivare la sottoscrizione.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERRORE \_ di \_ inoltri circolari EC \_**
</dt> <dd> <dl> <dt>

15082 (0x3AEA)
</dt> <dt>



Quando si esegue l'invio di eventi dal computer locale a se stesso, la query della sottoscrizione non può contenere il log di destinazione della sottoscrizione.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERRORE \_ EC \_ CREDSTORE \_ completo**
</dt> <dd> <dl> <dt>

15083 (0x3AEB)
</dt> <dt>



L'archivio delle credenziali utilizzato per salvare le credenziali è pieno.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERRORE \_ EC \_ cred \_ non \_ trovato**
</dt> <dd> <dl> <dt>

15084 (0x3AEC)
</dt> <dt>



Le credenziali usate da questa sottoscrizione non sono state trovate nell'archivio credenziali.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERRORE \_ EC \_ nessun \_ \_ canale attivo**
</dt> <dd> <dl> <dt>

15085 (0x3AED)
</dt> <dt>



Nessun canale attivo trovato per la query.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**ERRORE \_ \_ file MUI \_ non \_ trovato**
</dt> <dd> <dl> <dt>

15100 (0x3AFC)
</dt> <dt>



Il caricatore di risorse non è riuscito a trovare il file MUI.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERRORE \_ MUI \_ file non valido \_**
</dt> <dd> <dl> <dt>

15101 (0x3AFD)
</dt> <dt>



Il caricatore di risorse non è riuscito a caricare il file MUI perché il file non supera la convalida.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERRORE \_ MUI \_ non valido per la \_ \_ configurazione RC**
</dt> <dd> <dl> <dt>

15102 (0x3AFE)
</dt> <dt>



Il manifesto RC è danneggiato con dati di Garbage Collection o versioni non supportate o elementi necessari mancanti.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERRORE \_ MUI \_ \_ nome delle impostazioni locali non valido \_**
</dt> <dd> <dl> <dt>

15103 (0x3AFF)
</dt> <dt>



Il manifesto RC ha un nome di impostazioni cultura non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERRORE \_ MUI \_ \_ nome ULTIMATEFALLBACK non valido \_**
</dt> <dd> <dl> <dt>

15104 (0x3B00)
</dt> <dt>



Il manifesto RC presenta un nome ultimatefallback non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERRORE \_ \_ file MUI \_ non \_ caricato**
</dt> <dd> <dl> <dt>

15105 (0x3B01)
</dt> <dt>



La cache del caricatore di risorse non ha caricato una voce MUI.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**errore \_ \_ dell'enumerazione della risorsa di \_ errore \_**
</dt> <dd> <dl> <dt>

15106 (0x3B02)
</dt> <dt>



Enumerazione di risorse arrestata dall'utente.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERRORE \_ MUI \_ INTLSETTINGS \_ UILANG \_ non \_ installato**
</dt> <dd> <dl> <dt>

15107 (0x3B03)
</dt> <dt>



Installazione della lingua dell'interfaccia utente non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERRORE \_ MUI \_ INTLSETTINGS \_ \_ nome impostazioni locali non valido \_**
</dt> <dd> <dl> <dt>

15108 (0x3B04)
</dt> <dt>



Installazione delle impostazioni locali non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERRORE di runtime di gestione della \_ messaggistica \_ \_ senza \_ \_ risorsa predefinita o \_ neutra \_**
</dt> <dd> <dl> <dt>

15110 (0x3B06)
</dt> <dt>



Una risorsa non dispone di un valore predefinito o neutro.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERRORE di gestione della \_ messaggistica \_ file priconfig non valido \_**
</dt> <dd> <dl> <dt>

15111 (0x3B07)
</dt> <dt>



File di configurazione PRI non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**\_tipo di \_ file non valido per \_ la gestione errori \_**
</dt> <dd> <dl> <dt>

15112 (0x3B08)
</dt> <dt>



Tipo di file non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERRORE di gestione del \_ \_ \_ qualificatore sconosciuto**
</dt> <dd> <dl> <dt>

15113 (0x3B09)
</dt> <dt>



Qualificatore sconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**errore durante la gestione del \_ \_ qualificatore della messaggistica non valida \_ \_**
</dt> <dd> <dl> <dt>

15114 (0x3B0A)
</dt> <dt>



Valore qualificatore non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERRORE di gestione del \_ record \_ non \_ candidato**
</dt> <dd> <dl> <dt>

15115 (0x3B0B)
</dt> <dt>



Non è stato trovato alcun candidato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERRORE di gestione della \_ messaggistica \_ non \_ corrispondente \_ o \_ \_ candidato predefinito**
</dt> <dd> <dl> <dt>

15116 (0x3B0C)
</dt> <dt>



Per ResourceMap o NamedResource è presente un elemento che non ha una risorsa predefinita o neutra.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**tipo di risorsa gestione errori non \_ \_ \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

15117 (0x3B0D)
</dt> <dt>



Tipo ResourceCandidate non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**\_ \_ nome mappa duplicato errore \_ Gestione errori \_**
</dt> <dd> <dl> <dt>

15118 (0x3B0E)
</dt> <dt>



Mappa delle risorse duplicata.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**\_ \_ voce duplicata di gestione errori \_**
</dt> <dd> <dl> <dt>

15119 (0x3B0F)
</dt> <dt>



Voce duplicata.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**errore durante la gestione dell' \_ \_ identificatore di risorsa non valido \_ \_**
</dt> <dd> <dl> <dt>

15120 (0x3B10)
</dt> <dt>



Identificatore di risorsa non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**errore \_ filePath di gestione errori \_ \_ troppo \_ lungo**
</dt> <dd> <dl> <dt>

15121 (0x3B11)
</dt> <dt>



FilePath troppo lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**\_tipo di \_ Directory non supportato \_ dalla gestione errori di messaggistica \_**
</dt> <dd> <dl> <dt>

15122 (0x3B12)
</dt> <dt>



Tipo di directory non supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERRORE di gestione del \_ \_ \_ file PRI non valido \_**
</dt> <dd> <dl> <dt>

15126 (0x3B16)
</dt> <dt>



File PRI non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**\_ \_ \_ \_ Impossibile trovare la risorsa \_ di gestione degli errori denominata**
</dt> <dd> <dl> <dt>

15127 (0x3B17)
</dt> <dt>



NamedResource non trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**\_ \_ \_ Impossibile trovare la mappa di gestione della messaggistica degli errori \_**
</dt> <dd> <dl> <dt>

15135 (0x3B1F)
</dt> <dt>



ResourceMap non trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**\_tipo di \_ profilo non supportato \_ per la gestione errori di messaggistica \_**
</dt> <dd> <dl> <dt>

15136 (0x3B20)
</dt> <dt>



Tipo di profilo MRT non supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERRORE di gestione \_ \_ \_ qualificatore non valido \_**
</dt> <dd> <dl> <dt>

15137 (0x3B21)
</dt> <dt>



Operatore qualificatore non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**\_ \_ \_ valore QUALIFICATOre indeterminato di gestione errori \_**
</dt> <dd> <dl> <dt>

15138 (0x3B22)
</dt> <dt>



Impossibile determinare il valore del qualificatore o il valore del qualificatore non è stato impostato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**errore di MERGE automatico della messaggistica di errore \_ \_ \_ abilitato**
</dt> <dd> <dl> <dt>

15139 (0x3B23)
</dt> <dt>



L'operazione di merge automatico è abilitata nel file PRI.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**errore durante la gestione di un \_ \_ numero eccessivo di \_ \_ risorse**
</dt> <dd> <dl> <dt>

15140 (0x3B24)
</dt> <dt>



Troppe risorse definite per il pacchetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERRORE \_ MCA \_ funzionalità non valide \_ \_ stringa**
</dt> <dd> <dl> <dt>

15200 (0x3B60)
</dt> <dt>



Il monitoraggio ha restituito una stringa di funzionalità DDC/CI non conforme alla specifica ACCESS. bus 3,0, DDC/CI 1,1 o MCCS 2 Revision 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERRORE \_ MCA \_ \_ versione VCP non valida \_**
</dt> <dd> <dl> <dt>

15201 (0x3B61)
</dt> <dt>



Il codice VCP della versione VCP (0xDF) del monitoraggio ha restituito un valore di versione non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**ERRORE \_ \_ Monitor MCA \_ viola la \_ \_ specifica MCCS**
</dt> <dd> <dl> <dt>

15202 (0x3B62)
</dt> <dt>



Il monitoraggio non è conforme alla specifica MCCS che attesta per il supporto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERRORE \_ di \_ versione di MCCS MCA non \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

15203 (0x3B63)
</dt> <dt>



La versione di MCCS nella funzionalità MCCS ver di un monitoraggio \_ non corrisponde alla versione di MCCS che il monitoraggio segnala quando viene usato il codice VCP della versione VCP (0xDF).


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERRORE \_ MCA \_ \_ versione MCCS non supportata \_**
</dt> <dd> <dl> <dt>

15204 (0x3B64)
</dt> <dt>



L'API di configurazione del monitoraggio funziona solo con i monitoraggi che supportano la specifica MCCS 1,0, la specifica MCCS 2,0 o la specifica MCCS 2,0 Revisione 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**errore \_ interno MCA errore \_ \_**
</dt> <dd> <dl> <dt>

15205 (0x3B65)
</dt> <dt>



Si è verificato un errore interno dell'API di configurazione del monitoraggio.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERRORE \_ MCA \_ tipo di tecnologia non valido \_ \_ \_ restituito**
</dt> <dd> <dl> <dt>

15206 (0x3B66)
</dt> <dt>



Il monitoraggio ha restituito un tipo di tecnologia di monitoraggio non valido. CRT, plasma e LCD (TFT) sono esempi di tipi di tecnologia di monitoraggio. Questo errore indica che il monitoraggio ha violato la specifica MCCS 2,0 o MCCS 2,0 Revisione 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERRORE per la temperatura di colore non supportata da \_ MCA \_ \_ \_**
</dt> <dd> <dl> <dt>

15207 (0x3B67)
</dt> <dt>



Il chiamante di [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) ha specificato una temperatura di colore non supportata dal monitoraggio corrente. Questo errore indica che il monitoraggio ha violato la specifica MCCS 2,0 o MCCS 2,0 Revisione 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERRORE \_ ambiguo \_ dispositivo di sistema \_**
</dt> <dd> <dl> <dt>

15250 (0x3B92)
</dt> <dt>



Il dispositivo di sistema richiesto non può essere identificato a causa di più dispositivi indistinguibili che potenzialmente corrispondono ai criteri di identificazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**ERRORE \_ di \_ dispositivo di sistema \_ non \_ trovato**
</dt> <dd> <dl> <dt>

15299 (0x3BC3)
</dt> <dt>



Il dispositivo di sistema richiesto non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**\_hash errore \_ non \_ supportato**
</dt> <dd> <dl> <dt>

15300 (0x3BC4)
</dt> <dt>



La generazione di hash per la versione hash e il tipo hash specificati non è abilitata nel server.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**\_hash errore \_ non \_ presente**
</dt> <dd> <dl> <dt>

15301 (0x3BC5)
</dt> <dt>



L'hash richiesto dal server non è disponibile o non è più valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERRORE \_ del \_ provider IC secondario \_ \_ non \_ registrato**
</dt> <dd> <dl> <dt>

15321 (0x3BD9)
</dt> <dt>



L'istanza del controller di interrupt secondario che gestisce l'interrupt specificato non è registrata.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERRORE \_ GPIO \_ \_ informazioni client \_ non valide**
</dt> <dd> <dl> <dt>

15322 (0x3BDA)
</dt> <dt>



Le informazioni fornite dal driver client GPIO non sono valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**ERRORE \_ GPIO \_ versione \_ non \_ supportata**
</dt> <dd> <dl> <dt>

15323 (0x3BDB)
</dt> <dt>



La versione specificata dal driver client di GPIO non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**errore durante il \_ GPIO del pacchetto di \_ registrazione non valido \_ \_**
</dt> <dd> <dl> <dt>

15324 (0x3BDC)
</dt> <dt>



Il pacchetto di registrazione fornito dal driver client di GPIO non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**ERRORE \_ GPIO \_ operazione \_ negata**
</dt> <dd> <dl> <dt>

15325 (0x3BDD)
</dt> <dt>



L'operazione richiesta non è supportata per l'handle specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERRORE \_ GPIO \_ modalità di \_ connessione incompatibile \_**
</dt> <dd> <dl> <dt>

15326 (0x3BDE)
</dt> <dt>



La modalità di connessione richiesta è in conflitto con una modalità esistente in uno o più dei PIN specificati.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERRORE \_ GPIO \_ interrupt \_ già senza \_ maschera**
</dt> <dd> <dl> <dt>

15327 (0x3BDF)
</dt> <dt>



L'interrupt richiesto per l'unmasking non è mascherato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**ERRORE \_ non può \_ passare a \_ runlevel**
</dt> <dd> <dl> <dt>

15400 (0x3C28)
</dt> <dt>



Non è possibile completare l'opzione del livello di esecuzione richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERRORE \_ \_ impostazione del runlevel non valida \_**
</dt> <dd> <dl> <dt>

15401 (0x3C29)
</dt> <dt>



L'impostazione del livello di esecuzione del servizio non è valida. Il livello di esecuzione per un servizio non deve essere maggiore del livello di esecuzione dei servizi dipendenti.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**\_ \_ timeout switch runlevel \_ errore**
</dt> <dd> <dl> <dt>

15402 (0x3C2A)
</dt> <dt>



Non è possibile completare l'opzione del livello di esecuzione richiesto perché uno o più servizi non verranno arrestati o riavviati entro il timeout specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**\_ \_ \_ timeout agente switch runlevel \_ errore**
</dt> <dd> <dl> <dt>

15403 (0x3C2B)
</dt> <dt>



Un agente di commutazione del livello di esecuzione non ha risposto entro il timeout specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**l' \_ opzione di errore runlevel è \_ \_ in \_ corso**
</dt> <dd> <dl> <dt>

15404 (0x3C2C)
</dt> <dt>



È attualmente in corso un'opzione del livello di esecuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**\_avvio automatico dei servizi di errore \_ non riuscito \_**
</dt> <dd> <dl> <dt>

15405 (0x3C2D)
</dt> <dt>



Non è stato possibile avviare uno o più servizi durante la fase di avvio del servizio di un Commuter del livello di esecuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERRORE \_ \_ interruzione attività \_ com \_ in sospeso**
</dt> <dd> <dl> <dt>

15501 (0x3C8D)
</dt> <dt>



Non è possibile completare la richiesta di arresto dell'attività immediatamente perché è necessario più tempo per l'arresto dell'attività.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERRORE di \_ installazione del \_ \_ pacchetto aperto \_ non riuscito**
</dt> <dd> <dl> <dt>

15600 (0x3CF0)
</dt> <dt>



Non è stato possibile aprire il pacchetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERRORE di \_ installazione \_ pacchetto \_ non \_ trovato**
</dt> <dd> <dl> <dt>

15601 (0x3CF1)
</dt> <dt>



Il pacchetto non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**errore durante l' \_ installazione del \_ pacchetto non valido \_**
</dt> <dd> <dl> <dt>

15602 (0x3CF2)
</dt> <dt>



I dati del pacchetto non sono validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**ERRORE di \_ installazione della \_ dipendenza di risoluzione \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

15603 (0x3CF3)
</dt> <dt>



Aggiornamenti del pacchetto non riusciti, dipendenza o convalida dei conflitti.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERRORE \_ \_ di installazione \_ \_ dello spazio su disco \_ insufficiente**
</dt> <dd> <dl> <dt>

15604 (0x3CF4)
</dt> <dt>



Spazio su disco insufficiente nel computer. Liberare spazio e riprovare.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERRORE di \_ installazione \_ rete non \_ riuscita**
</dt> <dd> <dl> <dt>

15605 (0x3CF5)
</dt> <dt>



Si è verificato un problema durante il download del prodotto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERRORE \_ di \_ registrazione dell'installazione \_**
</dt> <dd> <dl> <dt>

15606 (0x3CF6)
</dt> <dt>



Non è stato possibile registrare il pacchetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERRORE \_ di \_ annullamento della registrazione dell'installazione \_**
</dt> <dd> <dl> <dt>

15607 (0x3CF7)
</dt> <dt>



Non è stato possibile annullare la registrazione del pacchetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**errore durante l' \_ installazione dell' \_ annullamento**
</dt> <dd> <dl> <dt>

15608 (0x3CF8)
</dt> <dt>



L'utente ha annullato la richiesta di installazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**ERRORE di \_ installazione \_**
</dt> <dd> <dl> <dt>

15609 (0x3CF9)
</dt> <dt>



Installazione non riuscita. Contattare il fornitore del software.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**\_rimozione errore \_ non riuscita**
</dt> <dd> <dl> <dt>

15610 (0x3CFA)
</dt> <dt>



Rimozione non riuscita. Contattare il fornitore del software.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**il \_ pacchetto degli errori \_ \_ esiste già**
</dt> <dd> <dl> <dt>

15611 (0x3CFB)
</dt> <dt>



Il pacchetto specificato è già installato e la reinstallazione del pacchetto è stata bloccata. Per informazioni dettagliate, vedere il registro eventi AppXDeployment-Server.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**ERRORE \_ necessario \_ correzione**
</dt> <dd> <dl> <dt>

15612 (0x3CFC)
</dt> <dt>



Impossibile avviare l'applicazione. Provare a reinstallare l'applicazione per risolvere il problema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERRORE di \_ installazione \_ prerequisiti \_ non riuscito**
</dt> <dd> <dl> <dt>

15613 (0x3CFD)
</dt> <dt>



Non è stato possibile soddisfare un prerequisito per un'installazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**REPOSITORY del pacchetto di errore \_ \_ \_ danneggiato**
</dt> <dd> <dl> <dt>

15614 (0x3CFE)
</dt> <dt>



Il repository del pacchetto è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERRORE di \_ installazione dei \_ criteri \_**
</dt> <dd> <dl> <dt>

15615 (0x3CFF)
</dt> <dt>



Per installare questa applicazione, è necessario disporre di una licenza per sviluppatori Windows o di un sistema abilitato per sideload.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**\_aggiornamento del pacchetto di errori \_**
</dt> <dd> <dl> <dt>

15616 (0x3D00)
</dt> <dt>



Non è possibile avviare l'applicazione perché è attualmente in fase di aggiornamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**\_distribuzione \_ degli errori bloccata \_ dai \_ criteri**
</dt> <dd> <dl> <dt>

15617 (0x3D01)
</dt> <dt>



L'operazione di distribuzione del pacchetto è bloccata dai criteri. Contattare l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**\_pacchetti \_ di errore in \_ uso**
</dt> <dd> <dl> <dt>

15618 (0x3D02)
</dt> <dt>



Non è stato possibile installare il pacchetto perché le risorse modificate sono attualmente in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**\_file di ripristino errori \_ \_ danneggiato**
</dt> <dd> <dl> <dt>

15619 (0x3D03)
</dt> <dt>



Non è stato possibile recuperare il pacchetto perché i dati necessari per il ripristino sono stati danneggiati.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERRORE \_ di \_ firma temporanea non valida \_**
</dt> <dd> <dl> <dt>

15620 (0x3D04)
</dt> <dt>



La firma non è valida. Per eseguire la registrazione in modalità sviluppatore, AppxSignature. p7x e AppxBlockMap.xml devono essere validi o non devono essere presenti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**errore durante l' \_ eliminazione dell' \_ \_ Archivio APPLICATIONDATA esistente \_ \_ non riuscito**
</dt> <dd> <dl> <dt>

15621 (0x3D05)
</dt> <dt>



Si è verificato un errore durante l'eliminazione dei dati dell'applicazione precedentemente esistenti del pacchetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERRORE di \_ installazione del \_ downgrade del pacchetto \_**
</dt> <dd> <dl> <dt>

15622 (0x3D06)
</dt> <dt>



Non è stato possibile installare il pacchetto perché è già installata una versione più recente del pacchetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**il \_ sistema di errori \_ richiede la \_ correzione**
</dt> <dd> <dl> <dt>

15623 (0x3D07)
</dt> <dt>



È stato rilevato un errore in un file binario di sistema. Provare ad aggiornare il PC per risolvere il problema.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**errore errore di \_ \_ integrità appx \_ \_ CLR \_ NGen**
</dt> <dd> <dl> <dt>

15624 (0x3D08)
</dt> <dt>



Rilevato un file binario NGEN CLR danneggiato nel sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**\_file di resilienza degli errori \_ \_ danneggiato**
</dt> <dd> <dl> <dt>

15625 (0x3D09)
</dt> <dt>



Non è stato possibile riprendere l'operazione perché i dati necessari per il ripristino sono stati danneggiati.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**errore durante l' \_ installazione del \_ \_ servizio firewall \_ non \_ in esecuzione**
</dt> <dd> <dl> <dt>

15626 (0x3D0A)
</dt> <dt>



Non è stato possibile installare il pacchetto perché il servizio Windows Firewall non è in esecuzione. Abilitare il servizio Windows Firewall e riprovare.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**\_errore APPMODEL \_ nessun \_ pacchetto**
</dt> <dd> <dl> <dt>

15700 (0x3D54)
</dt> <dt>



Il processo non ha un'identità del pacchetto.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**\_runtime del \_ pacchetto errori APPMODEL \_ \_ danneggiato**
</dt> <dd> <dl> <dt>

15701 (0x3D55)
</dt> <dt>



Le informazioni di runtime del pacchetto sono danneggiate.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**\_identità del \_ pacchetto errori APPMODEL \_ \_ danneggiata**
</dt> <dd> <dl> <dt>

15702 (0x3D56)
</dt> <dt>



L'identità del pacchetto è danneggiata.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**\_errore APPMODEL \_ Nessuna \_ applicazione**
</dt> <dd> <dl> <dt>

15703 (0x3D57)
</dt> <dt>



Il processo non ha un'identità dell'applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**\_Archivio di caricamento stato di errore \_ \_ \_ non riuscito**
</dt> <dd> <dl> <dt>

15800 (0x3DB8)
</dt> <dt>



Il caricamento dell'archivio Stati non è riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**\_ \_ Impossibile ottenere la \_ versione dello stato di \_ errore**
</dt> <dd> <dl> <dt>

15801 (0x3DB9)
</dt> <dt>



Il recupero della versione dello stato per l'applicazione non è riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**versione del set di Stati di errore \_ \_ \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

15802 (0x3DBA)
</dt> <dt>



Impossibile impostare la versione dello stato per l'applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**\_ripristino strutturato dello stato di errore \_ \_ \_ non riuscito**
</dt> <dd> <dl> <dt>

15803 (0x3DBB)
</dt> <dt>



Reimpostazione dello stato strutturato dell'applicazione non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**ERRORE \_ di \_ apertura del \_ contenitore di \_ stato di errore**
</dt> <dd> <dl> <dt>

15804 (0x3DBC)
</dt> <dt>



Il gestore degli Stati non è riuscito ad aprire il contenitore.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**ERRORE \_ di \_ creazione del \_ contenitore di \_ stato di errore**
</dt> <dd> <dl> <dt>

15805 (0x3DBD)
</dt> <dt>



Gestione stato non è riuscito a creare il contenitore.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**eliminazione del contenitore di stato di errore \_ \_ \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

15806 (0x3DBE)
</dt> <dt>



Il gestore degli Stati non è riuscito a eliminare il contenitore.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**\_impostazione di \_ lettura stato errore \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

15807 (0x3DBF)
</dt> <dt>



Il gestore degli Stati non è riuscito a leggere l'impostazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**\_ \_ impostazione scrittura stato \_ errore \_ non riuscita**
</dt> <dd> <dl> <dt>

15808 (0x3DC0)
</dt> <dt>



Il gestore degli Stati non è riuscito a scrivere l'impostazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**\_ \_ impostazione eliminazione stato \_ errore \_ non riuscita**
</dt> <dd> <dl> <dt>

15809 (0x3DC1)
</dt> <dt>



Il gestore degli Stati non è riuscito a eliminare l'impostazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**\_impostazione della query sullo stato di errore \_ \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

15810 (0x3DC2)
</dt> <dt>



Gestione stato non è riuscito a eseguire una query sull'impostazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**\_ \_ \_ Impossibile impostare l'impostazione composita di lettura stato \_ errore \_**
</dt> <dd> <dl> <dt>

15811 (0x3DC3)
</dt> <dt>



Il gestore degli Stati non è riuscito a leggere l'impostazione composita.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**errore durante la \_ \_ scrittura dell' \_ impostazione composita \_ \_**
</dt> <dd> <dl> <dt>

15812 (0x3DC4)
</dt> <dt>



Il gestore degli Stati non è riuscito a scrivere l'impostazione composita.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**ERRORE \_ di \_ enumerazione del \_ contenitore di \_ stato di errore**
</dt> <dd> <dl> <dt>

15813 (0x3DC5)
</dt> <dt>



Il gestore degli Stati non è riuscito a enumerare i contenitori.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**\_ \_ Impossibile enumerare \_ le impostazioni di stato di errore \_**
</dt> <dd> <dl> <dt>

15814 (0x3DC6)
</dt> <dt>



Gestione stato non è riuscito a enumerare le impostazioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**\_ \_ limite dimensioni del valore dell'impostazione composita dello stato di errore \_ \_ \_ \_ \_ superato**
</dt> <dd> <dl> <dt>

15815 (0x3DC7)
</dt> <dt>



La dimensione del valore dell'impostazione composita di gestione stati ha superato il limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**\_ \_ \_ limite dimensioni valore impostazione stato errore \_ \_ \_ superato**
</dt> <dd> <dl> <dt>

15816 (0x3DC8)
</dt> <dt>



La dimensione del valore dell'impostazione di gestione stati ha superato il limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**\_ \_ \_ limite dimensioni nome impostazione stato errore \_ \_ \_ superato**
</dt> <dd> <dl> <dt>

15817 (0x3DC9)
</dt> <dt>



La lunghezza del nome dell'impostazione del gestore dello stato ha superato il limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**\_ \_ \_ limite dimensioni nome contenitore stato errore \_ \_ \_ superato**
</dt> <dd> <dl> <dt>

15818 (0x3DCA)
</dt> <dt>



La lunghezza del nome del contenitore di gestione stati ha superato il limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**API di errore non \_ \_ disponibile**
</dt> <dd> <dl> <dt>

15841 (0x3DE1)
</dt> <dt>



Questa API non può essere usata nel contesto del tipo di applicazione del chiamante.


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

 

 
