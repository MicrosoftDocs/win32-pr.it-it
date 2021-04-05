---
title: Valori restituiti
description: Le costanti seguenti rappresentano i valori restituiti che generano l'ottimizzazione del recapito e i valori restituiti HTTP che eseguono l'acquisizione.
ms.assetid: 68AC4581-C748-49AB-A588-15816E534756
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e58d66587061cc44fc441249407b73653153322
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047103"
---
# <a name="do-return-values"></a>Valori restituiti

Le costanti seguenti rappresentano i valori restituiti che generano l'ottimizzazione del recapito e i valori restituiti HTTP che eseguono l'acquisizione. Tutti gli altri valori restituiti che è possibile ricevere sono i valori restituiti di Windows COM, RPC o convertiti (usare la macro [HRESULT_FROM_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) per convertire i valori restituiti di Windows in valori HRESULT).

<dl> <dt>

<span id="DO_E_NO_SERVICE__0x80d01001_"></span><span id="do_e_no_service__0x80d01001_"></span><span id="DO_E_NO_SERVICE__0X80D01001_"></span>DO_E_NO_SERVICE (0x80d01001)
</dt> <dd>

Ottimizzazione recapito non è in grado di fornire il servizio.

</dd> <dt>

<span id="DO_E_DOWNLOAD_NO_PROGRESS__0x80d02002_"></span><span id="do_e_download_no_progress__0x80d02002_"></span><span id="DO_E_DOWNLOAD_NO_PROGRESS__0X80D02002_"></span>DO_E_DOWNLOAD_NO_PROGRESS (0x80d02002)
</dt> <dd>

Il download di un file non è stato rilevato entro il periodo definito.

</dd> <dt>

<span id="DO_E_JOB_NOT_FOUND__0x80d02003_"></span><span id="do_e_job_not_found__0x80d02003_"></span><span id="DO_E_JOB_NOT_FOUND__0X80D02003_"></span>DO_E_JOB_NOT_FOUND (0x80d02003)
</dt> <dd>

Il processo non è stato trovato, aspettando che sia presente un processo.

</dd> <dt>

<span id="DO_E_JOB_EMPTY__0x80d02004_"></span><span id="do_e_job_empty__0x80d02004_"></span><span id="DO_E_JOB_EMPTY__0X80D02004_"></span>DO_E_JOB_EMPTY (0x80d02004)
</dt> <dd>

Nessun file nel processo. previsto almeno un file.

</dd> <dt>

<span id="DO_E_LOCALPATH_NOT_SET__0x80d0200d_"></span><span id="do_e_localpath_not_set__0x80d0200d_"></span><span id="DO_E_LOCALPATH_NOT_SET__0X80D0200D_"></span>DO_E_LOCALPATH_NOT_SET (0x80d0200d)
</dt> <dd>

Nessun percorso di file locale specificato per il download.

</dd> <dt>

<span id="DO_E_FILE_NOT_AVAILABLE__0x80d02010_"></span><span id="do_e_file_not_available__0x80d02010_"></span><span id="DO_E_FILE_NOT_AVAILABLE__0X80D02010_"></span>DO_E_FILE_NOT_AVAILABLE (0x80d02010)
</dt> <dd>

Nessun file disponibile perché nessun URL ha generato un errore.

</dd> <dt>

<span id="DO_E_UNKNOWN_PROPERTY_ID__0x80d02011_"></span><span id="do_e_unknown_property_id__0x80d02011_"></span><span id="DO_E_UNKNOWN_PROPERTY_ID__0X80D02011_"></span>DO_E_UNKNOWN_PROPERTY_ID (0x80d02011)
</dt> <dd>

SetProperty () o GetProperty () chiamato con un ID di proprietà sconosciuto.

</dd> <dt>

<span id="DO_E_READ_ONLY_PROPERTY__0x80d02012_"></span><span id="do_e_read_only_property__0x80d02012_"></span><span id="DO_E_READ_ONLY_PROPERTY__0X80D02012_"></span>DO_E_READ_ONLY_PROPERTY (0x80d02012)
</dt> <dd>

Impossibile chiamare SetProperty () su una proprietà di sola lettura.

</dd> <dt>

<span id="DO_E_INVALID_STATE__0x80d02013_"></span><span id="do_e_invalid_state__0x80d02013_"></span><span id="DO_E_INVALID_STATE__0X80D02013_"></span>DO_E_INVALID_STATE (0x80d02013)
</dt> <dd>

L'azione richiesta non è consentita nello stato del processo corrente. È possibile che il processo sia stato annullato o completato.

</dd> <dt>

<span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0x80d02014_"></span><span id="do_e_error_information_unavailable__0x80d02014_"></span><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0X80D02014_"></span>DO_E_ERROR_INFORMATION_UNAVAILABLE (0x80d02014)
</dt> <dd>

Non si sono verificati errori.

</dd> <dt>

<span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0x80d03002_"></span><span id="do_e_no_download_extsettings__0x80d03002_"></span><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0X80D03002_"></span>DO_E_NO_DOWNLOAD_EXTSETTINGS (0x80d03002)
</dt> <dd>

Il processo di download non è consentito a causa delle impostazioni utente/amministratore.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0x80d03801_"></span><span id="do_e_blocked_by_cost_transfer_policy__0x80d03801_"></span><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0X80D03801_"></span>DO_E_BLOCKED_BY_COST_TRANSFER_POLICY (0x80d03801)
</dt> <dd>

Sospendere il processo a causa di restrizioni relative ai criteri di costo.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0x80d03803_"></span><span id="do_e_blocked_by_cellular_policy__0x80d03803_"></span><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0X80D03803_"></span>DO_E_BLOCKED_BY_CELLULAR_POLICY (0x80d03803)
</dt> <dd>

Sospendere il processo a causa del rilevamento delle restrizioni relative alla rete cellulare e ai criteri.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_POWER_STATE__0x80d03804_"></span><span id="do_e_blocked_by_power_state__0x80d03804_"></span><span id="DO_E_BLOCKED_BY_POWER_STATE__0X80D03804_"></span>DO_E_BLOCKED_BY_POWER_STATE (0x80d03804)
</dt> <dd>

Sospendere il processo a causa del rilevamento della modifica dello stato di alimentazione in modalità non AC.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_NO_NETWORK__0x80d03805_"></span><span id="do_e_blocked_by_no_network__0x80d03805_"></span><span id="DO_E_BLOCKED_BY_NO_NETWORK__0X80D03805_"></span>DO_E_BLOCKED_BY_NO_NETWORK (0x80d03805)
</dt> <dd>

Sospendere il processo a causa della perdita della connettività di rete.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_VPN_POLICY__0x80d03807_"></span><span id="do_e_blocked_by_vpn_policy__0x80d03807_"></span><span id="DO_E_BLOCKED_BY_VPN_POLICY__0X80D03807_"></span>DO_E_BLOCKED_BY_VPN_POLICY (0x80d03807)
</dt> <dd>

Sospendere il processo completato a causa del rilevamento della rete VPN.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0x80d03808_"></span><span id="do_e_blocked_by_critical_memory_usage__0x80d03808_"></span><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0X80D03808_"></span>DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE (0x80d03808)
</dt> <dd>

Sospendere il processo completato a causa del rilevamento dell'utilizzo di memoria critico nel sistema.

</dd> <dt>

<span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0x80d05001_"></span><span id="do_e_http_blocksize_mismatch__0x80d05001_"></span><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0X80D05001_"></span>DO_E_HTTP_BLOCKSIZE_MISMATCH (0x80d05001)
</dt> <dd>

Il server HTTP ha restituito una risposta con dimensione dei dati diversa da quella richiesta.

</dd> <dt>

<span id="DO_E_INVALID_RANGE__0x80d05010_"></span><span id="do_e_invalid_range__0x80d05010_"></span><span id="DO_E_INVALID_RANGE__0X80D05010_"></span>DO_E_INVALID_RANGE (0x80d05010)
</dt> <dd>

L'intervallo di byte specificato non è valido.

</dd> <dt>

<span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0x80d05011_"></span><span id="do_e_insufficient_range_support__0x80d05011_"></span><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0X80D05011_"></span>DO_E_INSUFFICIENT_RANGE_SUPPORT (0x80d05011)
</dt> <dd>

Il server non supporta il protocollo HTTP necessario. Per ottimizzazione recapito è necessario che il server supporti l'intestazione del protocollo di intervallo.

</dd> <dt>

<span id="DO_E_OVERLAPPING_RANGES__0x80d05012_"></span><span id="do_e_overlapping_ranges__0x80d05012_"></span><span id="DO_E_OVERLAPPING_RANGES__0X80D05012_"></span>DO_E_OVERLAPPING_RANGES (0x80d05012)
</dt> <dd>

L'elenco di intervalli di byte contiene alcuni intervalli sovrapposti, che non sono supportati.

</dd> <dt>

<span id="DO_E_FATAL_CORE_ERROR__0x80d06802_"></span><span id="do_e_fatal_core_error__0x80d06802_"></span><span id="DO_E_FATAL_CORE_ERROR__0X80D06802_"></span>DO_E_FATAL_CORE_ERROR (0x80d06802)
</dt> <dd>

Si è verificato un errore irreversibile in core.

</dd> </dl>

 

 