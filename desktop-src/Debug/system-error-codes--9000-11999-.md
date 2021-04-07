---
description: Descrive i codici di errore 9000-11999 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: 27fe3fee-4ae3-43f1-a1f2-91c935e9851b
title: Codici di errore di sistema (9000-11999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 01eb071962d8d0f5beb801067ce1d72adc796bad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748378"
---
# <a name="system-error-codes-9000-11999"></a>Codici di errore di sistema (9000-11999)

> [!NOTE]
> Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema. Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .

Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) (errori da 9000 a 11999). Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .

<dl> <dt>

<span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**errore \_ di \_ formato RCODE errore \_ DNS \_**
</dt> <dd> <dl> <dt>

9001 (0x2329)
</dt> <dt>



Il server DNS non riesce a interpretare il formato.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**\_errore del \_ \_ Server RCODE errore DNS \_**
</dt> <dd> <dl> <dt>

9002 (0x232A)
</dt> <dt>



Errore del server DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**errore \_ DNS \_ RCODE \_ nome \_ errore**
</dt> <dd> <dl> <dt>

9003 (0x232B)
</dt> <dt>



Nome DNS inesistente.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**\_errore DNS \_ RCODE \_ non \_ implementato**
</dt> <dd> <dl> <dt>

9004 (0x232C)
</dt> <dt>



Richiesta DNS non supportata dal server dei nomi.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**\_errore DNS \_ RCODE \_ rifiutato**
</dt> <dd> <dl> <dt>

9005 (0x232D)
</dt> <dt>



Operazione DNS rifiutata.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**\_errore DNS \_ RCODE \_ YXDOMAIN**
</dt> <dd> <dl> <dt>

9006 (0x232E)
</dt> <dt>



Il nome DNS che non esiste, esiste.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**\_errore DNS \_ RCODE \_ YXRRSET**
</dt> <dd> <dl> <dt>

9007 (0x232F)
</dt> <dt>



Il set di RR DNS che non esiste, esiste.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**\_errore DNS \_ RCODE \_ NXRRSET**
</dt> <dd> <dl> <dt>

9008 (0x2330)
</dt> <dt>



Il set di RR DNS che deve esistere non esiste.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**\_errore DNS \_ RCODE \_ NOTAUTH**
</dt> <dd> <dl> <dt>

9009 (0x2331)
</dt> <dt>



Server DNS non autorevole per la zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**\_errore DNS \_ RCODE \_ NOTZONE**
</dt> <dd> <dl> <dt>

9010 (0x2332)
</dt> <dt>



Il nome DNS in Update o prereq non è nell'area.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**\_errore DNS \_ RCODE \_ BADSIG**
</dt> <dd> <dl> <dt>

9016 (0x2338)
</dt> <dt>



Impossibile verificare la firma DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**\_errore DNS \_ RCODE \_ BADKEY**
</dt> <dd> <dl> <dt>

9017 (0x2339)
</dt> <dt>



Chiave DNS non valida.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**\_errore DNS \_ RCODE \_ BADTIME**
</dt> <dd> <dl> <dt>

9018 (0x233A)
</dt> <dt>



Validità della firma DNS scaduta.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**errore DNS necessario per il \_ \_ master \_**
</dt> <dd> <dl> <dt>

9101 (0x238D)
</dt> <dt>



Questa operazione può essere eseguita solo dal server DNS che funge da Master chiavi per la zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**\_errore DNS \_ non \_ consentito \_ nell' \_ area firmata \_**
</dt> <dd> <dl> <dt>

9102 (0x238E)
</dt> <dt>



Questa operazione non è consentita in una zona firmata o con chiavi di firma.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**\_Errore DNS \_ NSEC3 \_ incompatibile \_ con \_ RSA \_ SHA1**
</dt> <dd> <dl> <dt>

9103 (0x238F)
</dt> <dt>



NSEC3 non è compatibile con l'algoritmo RSA-SHA-1. Scegliere un algoritmo diverso o usare NSEC.

Questo valore è stato anche **denominato \_ errore \_ DNS \_ \_ parametri NSEC3 non validi**


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**\_errore DNS \_ non sufficiente per i \_ \_ \_ \_ descrittori chiave di firma**
</dt> <dd> <dl> <dt>

9104 (0x2390)
</dt> <dt>



Il numero di chiavi di firma non è sufficiente per la zona. Deve essere presente almeno una chiave di firma della chiave (KSK) e almeno una chiave di firma della zona (ZSK).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**\_errore DNS \_ algoritmo non supportato \_**
</dt> <dd> <dl> <dt>

9105 (0x2391)
</dt> <dt>



L'algoritmo specificato non è supportato.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**\_errore DNS \_ \_ dimensione chiave non valida \_**
</dt> <dd> <dl> <dt>

9106 (0x2392)
</dt> <dt>



La dimensione della chiave specificata non è supportata.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**\_chiave di firma degli errori DNS \_ \_ \_ non \_ accessibile**
</dt> <dd> <dl> <dt>

9107 (0x2393)
</dt> <dt>



Una o più chiavi di firma per una zona non sono accessibili al server DNS. La firma della zona non sarà operativa fino a quando l'errore non viene risolto.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**\_il KSP dell'errore DNS non \_ \_ \_ supporta la \_ \_ protezione**
</dt> <dd> <dl> <dt>

9108 (0x2394)
</dt> <dt>



Il provider di archiviazione chiavi specificato non supporta la protezione dei dati DPAPI + +. La firma della zona non sarà operativa fino a quando l'errore non viene risolto.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**errore DNS \_ errore di \_ \_ \_ protezione \_ dati imprevisto**
</dt> <dd> <dl> <dt>

9109 (0x2395)
</dt> <dt>



Si è verificato un errore di DPAPI + + imprevisto. La firma della zona non sarà operativa fino a quando l'errore non viene risolto.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**errore \_ errore \_ CNG imprevisto del \_ DNS \_**
</dt> <dd> <dl> <dt>

9110 (0x2396)
</dt> <dt>



Si è verificato un errore di crittografia imprevisto. La firma della zona potrebbe non essere operativa fino a quando l'errore non viene risolto.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**\_versione del \_ \_ parametro di firma sconosciuta con errore \_ DNS \_**
</dt> <dd> <dl> <dt>

9111 (0x2397)
</dt> <dt>



Il server DNS ha rilevato una chiave di firma con una versione sconosciuta. La firma della zona non sarà operativa fino a quando l'errore non viene risolto.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**\_errore DNS \_ KSP \_ non \_ accessibile**
</dt> <dd> <dl> <dt>

9112 (0x2398)
</dt> <dt>



Il provider di servizi chiave specificato non può essere aperto dal server DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**\_errore DNS \_ troppi \_ \_ SKDS**
</dt> <dd> <dl> <dt>

9113 (0x2399)
</dt> <dt>



Il server DNS non è in grado di accettare altre chiavi di firma con l'algoritmo e il valore del flag KSK specificati per questa zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**errore DNS- \_ \_ periodo di rollover non valido \_ \_**
</dt> <dd> <dl> <dt>

9114 (0x239A)
</dt> <dt>



Il periodo di rollover specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**errore DNS con \_ \_ \_ offset di rollover iniziale non valido \_ \_**
</dt> <dd> <dl> <dt>

9115 (0x239B)
</dt> <dt>



L'offset di rollover iniziale specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**\_rollover degli errori DNS \_ \_ in \_ corso**
</dt> <dd> <dl> <dt>

9116 (0x239C)
</dt> <dt>



La chiave di firma specificata è già in corso di rollup delle chiavi.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**\_ \_ chiave standby errore \_ DNS \_ non \_ presente**
</dt> <dd> <dl> <dt>

9117 (0x239D)
</dt> <dt>



La chiave di firma specificata non dispone di una chiave standby da revocare.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**\_errore DNS \_ non \_ consentito \_ in \_ ZSK**
</dt> <dd> <dl> <dt>

9118 (0x239E)
</dt> <dt>



Questa operazione non è consentita in una chiave di firma della zona (ZSK).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**\_errore DNS \_ non \_ consentito \_ in \_ \_ SKD attivo**
</dt> <dd> <dl> <dt>

9119 (0x239F)
</dt> <dt>



Questa operazione non è consentita su una chiave di firma attiva.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**\_rollover degli errori DNS \_ \_ già \_ accodato**
</dt> <dd> <dl> <dt>

9120 (0x23A0)
</dt> <dt>



La chiave di firma specificata è già accodata per il rollover.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**\_errore DNS \_ non \_ consentito \_ in una \_ zona non firmata \_**
</dt> <dd> <dl> <dt>

9121 (0x23A1)
</dt> <dt>



Questa operazione non è consentita in una zona non firmata.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**\_errore DNS \_ errore \_ Master**
</dt> <dd> <dl> <dt>

9122 (0x23A2)
</dt> <dt>



Non è stato possibile completare l'operazione perché il server DNS elencato come Master chiavi corrente per questa zona è inattivo o non è configurato correttamente. Risolvere il problema nel Master chiavi corrente per questa zona oppure utilizzare un altro server DNS per requisire il ruolo di Master chiavi.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**\_errore DNS \_ \_ periodo di validità della firma non valido \_ \_**
</dt> <dd> <dl> <dt>

9123 (0x23A3)
</dt> <dt>



Il periodo di validità della firma specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**Errore DNS il \_ \_ \_ numero di \_ iterazioni NSEC3 non è valido \_**
</dt> <dd> <dl> <dt>

9124 (0x23A4)
</dt> <dt>



Il numero di iterazioni NSEC3 specificato è superiore a quello consentito dalla lunghezza minima della chiave usata nella zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**\_errore DNS \_ DNSSEC \_ \_ disabilitato**
</dt> <dd> <dl> <dt>

9125 (0x23A5)
</dt> <dt>



Non è stato possibile completare l'operazione perché il server DNS è stato configurato con le funzionalità DNSSEC disabilitate. Abilitare DNSSEC sul server DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**\_errore DNS \_ XML non valido \_**
</dt> <dd> <dl> <dt>

9126 (0x23A6)
</dt> <dt>



Non è stato possibile completare l'operazione perché il flusso XML ricevuto è vuoto o sintatticamente non valido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**\_errore DNS \_ nessun \_ \_ trust \_ Anchor valido**
</dt> <dd> <dl> <dt>

9127 (0x23A7)
</dt> <dt>



Questa operazione è stata completata, ma non sono stati aggiunti Trust Anchor perché tutti i trust anchor ricevuti non sono validi, non sono supportati, sono scaduti o non diventano validi in meno di 30 giorni.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**\_rollover degli errori DNS \_ \_ non \_ pokeable**
</dt> <dd> <dl> <dt>

9128 (0x23A8)
</dt> <dt>



La chiave di firma specificata non è in attesa dell'aggiornamento DS padre.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**\_ \_ \_ Conflitto nome NSEC3 errore \_ DNS**
</dt> <dd> <dl> <dt>

9129 (0x23A9)
</dt> <dt>



Collisione hash rilevata durante la firma NSEC3. Specificare un Salt fornito dall'utente diverso o usare un salt generato in modo casuale e tentare nuovamente di firmare la zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**\_Errore DNS \_ nsec \_ incompatibile \_ con \_ NSEC3 \_ RSA \_ SHA1**
</dt> <dd> <dl> <dt>

9130 (0x23AA)
</dt> <dt>



NSEC non è compatibile con l'algoritmo NSEC3-RSA-SHA-1. Scegliere un algoritmo diverso o usare NSEC3.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**\_informazioni DNS \_ nessun \_ record**
</dt> <dd> <dl> <dt>

9501 (0x251D)
</dt> <dt>



Nessun record trovato per la query DNS specificata.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**\_errore DNS \_ \_ pacchetto errato**
</dt> <dd> <dl> <dt>

9502 (0x251E)
</dt> <dt>



Pacchetto DNS non valido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**\_errore DNS \_ senza \_ pacchetti**
</dt> <dd> <dl> <dt>

9503 (0x251F)
</dt> <dt>



Nessun pacchetto DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**\_errore DNS \_ RCODE**
</dt> <dd> <dl> <dt>

9504 (0x2520)
</dt> <dt>



Errore DNS, controllare RCODE.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**errore DNS non \_ \_ protetto \_ pacchetto**
</dt> <dd> <dl> <dt>

9505 (0x2521)
</dt> <dt>



Pacchetto DNS non protetto.


</dt> </dl> </dd> <dt>

<span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**\_richiesta DNS \_ in sospeso**
</dt> <dd> <dl> <dt>

9506 (0x2522)
</dt> <dt>



La richiesta di query DNS è in sospeso.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**\_tipo di errore DNS \_ non valido \_**
</dt> <dd> <dl> <dt>

9551 (0x254F)
</dt> <dt>



Tipo DNS non valido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**\_errore DNS \_ \_ indirizzo IP non valido \_**
</dt> <dd> <dl> <dt>

9552 (0x2550)
</dt> <dt>



Indirizzo IP non valido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**\_Proprietà errore DNS \_ non valida \_**
</dt> <dd> <dl> <dt>

9553 (0x2551)
</dt> <dt>



Proprietà non valida.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**\_errore DNS \_ riprovare \_ \_ più tardi**
</dt> <dd> <dl> <dt>

9554 (0x2552)
</dt> <dt>



Ripetere l'operazione DNS in un secondo momento.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**\_errore DNS \_ non \_ univoco**
</dt> <dd> <dl> <dt>

9555 (0x2553)
</dt> <dt>



Il record per il nome e il tipo specificati non è univoco.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**\_ \_ \_ nome non RFC \_ dell'errore DNS**
</dt> <dd> <dl> <dt>

9556 (0x2554)
</dt> <dt>



Il nome DNS non è conforme alle specifiche RFC.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**\_FQDN stato \_ DNS**
</dt> <dd> <dl> <dt>

9557 (0x2555)
</dt> <dt>



Il nome DNS è un nome DNS completo.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**\_ \_ nome punteggiato stato \_ DNS**
</dt> <dd> <dl> <dt>

9558 (0x2556)
</dt> <dt>



Il nome DNS è punteggiato (più etichette).


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**\_ \_ \_ nome singola parte \_ stato DNS**
</dt> <dd> <dl> <dt>

9559 (0x2557)
</dt> <dt>



Il nome DNS è un nome in una sola parte.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**\_errore DNS \_ non valido \_ nome \_ Char**
</dt> <dd> <dl> <dt>

9560 (0x2558)
</dt> <dt>



Il nome DNS contiene un carattere non valido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**\_ \_ nome numerico errore \_ DNS**
</dt> <dd> <dl> <dt>

9561 (0x2559)
</dt> <dt>



Il nome DNS è interamente numerico.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**\_errore DNS \_ non \_ consentito \_ nel \_ \_ server radice**
</dt> <dd> <dl> <dt>

9562 (0x255A)
</dt> <dt>



L'operazione richiesta non è consentita in un server radice DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**\_errore DNS \_ non \_ consentito \_ nella \_ delega**
</dt> <dd> <dl> <dt>

9563 (0x255B)
</dt> <dt>



Non è stato possibile creare il record perché questa parte dello spazio dei nomi DNS è stata delegata a un altro server.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**\_errore DNS \_ non è in grado di \_ trovare i \_ \_ parametri radice**
</dt> <dd> <dl> <dt>

9564 (0x255C)
</dt> <dt>



Il server DNS non è riuscito a trovare un set di parametri radice.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**\_ \_ parametri radice incoerenti degli errori \_ DNS \_**
</dt> <dd> <dl> <dt>

9565 (0x255D)
</dt> <dt>



Il server DNS ha rilevato parametri radice ma non è coerente in tutte le schede.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**\_errore DNS \_ \_ valore DWORD \_ troppo \_ piccolo**
</dt> <dd> <dl> <dt>

9566 (0x255E)
</dt> <dt>



Il valore specificato è troppo piccolo per questo parametro.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**\_errore DNS \_ \_ valore DWORD \_ troppo \_ grande**
</dt> <dd> <dl> <dt>

9567 (0x255F)
</dt> <dt>



Il valore specificato è troppo grande per questo parametro.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**\_caricamento in \_ background degli errori DNS \_**
</dt> <dd> <dl> <dt>

9568 (0x2560)
</dt> <dt>



Questa operazione non è consentita mentre il server DNS carica le zone in background. Riprova più tardi.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**\_errore DNS \_ non \_ consentito \_ nel controller di dominio di \_ sola lettura**
</dt> <dd> <dl> <dt>

9569 (0x2561)
</dt> <dt>



L'operazione richiesta non è consentita su un server DNS in esecuzione in un controller di dominio di sola lettura.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**\_errore DNS \_ non \_ consentito \_ in \_ DNAME**
</dt> <dd> <dl> <dt>

9570 (0x2562)
</dt> <dt>



Nessun dato può esistere sotto un record DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**\_delega degli errori DNS \_ \_ obbligatoria**
</dt> <dd> <dl> <dt>

9571 (0x2563)
</dt> <dt>



Questa operazione richiede la delega delle credenziali.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**\_tabella dei \_ criteri non valida per errore \_ DNS \_**
</dt> <dd> <dl> <dt>

9572 (0x2564)
</dt> <dt>



La tabella dei criteri di risoluzione dei nomi è danneggiata. La risoluzione DNS non riuscirà fino a quando non sarà corretta. Contattare l'amministratore di rete.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**\_la zona di errore DNS non \_ \_ \_ \_ esiste**
</dt> <dd> <dl> <dt>

9601 (0x2581)
</dt> <dt>



La zona DNS non esiste.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**\_errore DNS \_ senza \_ informazioni sulla zona \_**
</dt> <dd> <dl> <dt>

9602 (0x2582)
</dt> <dt>



Informazioni sulla zona DNS non disponibili.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**\_operazione di \_ zona non valida nell'errore \_ DNS \_**
</dt> <dd> <dl> <dt>

9603 (0x2583)
</dt> <dt>



Operazione non valida per la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**\_errore di \_ configurazione della zona di errore DNS \_ \_**
</dt> <dd> <dl> <dt>

9604 (0x2584)
</dt> <dt>



Configurazione della zona DNS non valida.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**la \_ zona di errore DNS \_ \_ \_ non ha \_ \_ record SOA**
</dt> <dd> <dl> <dt>

9605 (0x2585)
</dt> <dt>



La zona DNS non dispone di un record di inizio di autorità (SOA).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**la \_ zona di errore DNS \_ \_ \_ non contiene \_ \_ record NS**
</dt> <dd> <dl> <dt>

9606 (0x2586)
</dt> <dt>



Per la zona DNS non è presente alcun record server nome (NS).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**\_zona di errore DNS \_ \_ bloccata**
</dt> <dd> <dl> <dt>

9607 (0x2587)
</dt> <dt>



La zona DNS è bloccata.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**\_creazione della zona di errore DNS \_ \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

9608 (0x2588)
</dt> <dt>



Creazione della zona DNS non riuscita.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**la \_ zona di errore DNS \_ \_ \_ esiste già**
</dt> <dd> <dl> <dt>

9609 (0x2589)
</dt> <dt>



Zona DNS già esistente.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**la \_ zona di errore DNS è \_ \_ già \_ esistente**
</dt> <dd> <dl> <dt>

9610 (0x258A)
</dt> <dt>



La zona DNS automatica esiste già.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**\_tipo di \_ zona non valido per l'errore DNS \_ \_**
</dt> <dd> <dl> <dt>

9611 (0x258B)
</dt> <dt>



Tipo di zona DNS non valido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**l' \_ errore DNS \_ secondario \_ richiede l' \_ \_ indirizzo IP master**
</dt> <dd> <dl> <dt>

9612 (0x258C)
</dt> <dt>



La zona DNS secondaria richiede l'indirizzo IP master.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**\_zona di errore DNS \_ \_ non \_ secondaria**
</dt> <dd> <dl> <dt>

9613 (0x258D)
</dt> <dt>



Zona DNS non secondaria.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**\_errore DNS \_ necessario \_ per \_ gli indirizzi secondari**
</dt> <dd> <dl> <dt>

9614 (0x258E)
</dt> <dt>



Sono necessari indirizzi IP secondari.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**\_errore DNS \_ WINS \_ inizializzazione \_ non riuscito**
</dt> <dd> <dl> <dt>

9615 (0x258F)
</dt> <dt>



Inizializzazione WINS non riuscita.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**errore DNS necessario per i \_ \_ \_ \_ server WINS**
</dt> <dd> <dl> <dt>

9616 (0x2590)
</dt> <dt>



Sono necessari server WINS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**\_errore DNS \_ NBSTAT \_ init \_ non riuscita**
</dt> <dd> <dl> <dt>

9617 (0x2591)
</dt> <dt>



Chiamata di inizializzazione NBTSTAT non riuscita.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**errore DNS- \_ \_ \_ eliminazione SOA \_ non valida**
</dt> <dd> <dl> <dt>

9618 (0x2592)
</dt> <dt>



Eliminazione dell'inizio dell'autorità (SOA) non valida.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**il \_ server d'invio degli errori DNS \_ \_ \_ esiste già**
</dt> <dd> <dl> <dt>

9619 (0x2593)
</dt> <dt>



Esiste già un'area di trasmissione condizionale per quel nome.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**la \_ zona di errore DNS \_ richiede l' \_ \_ \_ indirizzo IP master**
</dt> <dd> <dl> <dt>

9620 (0x2594)
</dt> <dt>



Questa zona deve essere configurata con uno o più indirizzi IP del server DNS master.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**\_la zona di errore DNS \_ è stata \_ \_ arrestata**
</dt> <dd> <dl> <dt>

9621 (0x2595)
</dt> <dt>



Non è possibile eseguire l'operazione perché questa zona è stata arrestata.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**\_ \_ zona di errore DNS \_ bloccata \_ per la \_ firma**
</dt> <dd> <dl> <dt>

9622 (0x2596)
</dt> <dt>



Impossibile eseguire l'operazione perché la zona è attualmente in fase di firma. Riprova più tardi.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**l' \_ errore DNS \_ primario \_ richiede \_ un file di file**
</dt> <dd> <dl> <dt>

9651 (0x25B3)
</dt> <dt>



La zona DNS primaria richiede DataFile.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**\_ \_ \_ nome DataFile non valido \_ per l'errore DNS**
</dt> <dd> <dl> <dt>

9652 (0x25B4)
</dt> <dt>



Nome di file di DataFile non valido per la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**errore di apertura del file di \_ errore DNS \_ \_ \_**
</dt> <dd> <dl> <dt>

9653 (0x25B5)
</dt> <dt>



Non è stato possibile aprire il file DataFile per la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**il \_ WRITEBACK del file degli errori DNS \_ \_ \_ non è riuscito**
</dt> <dd> <dl> <dt>

9654 (0x25B6)
</dt> <dt>



Non è stato possibile scrivere DataFile per la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**analisi dei file di \_ errore DNS \_ \_**
</dt> <dd> <dl> <dt>

9655 (0x25B7)
</dt> <dt>



Errore durante la lettura di DataFile per la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**\_il record di errore DNS non \_ \_ \_ \_ esiste**
</dt> <dd> <dl> <dt>

9701 (0x25E5)
</dt> <dt>



Il record DNS non esiste.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**\_ \_ formato record degli errori DNS \_**
</dt> <dd> <dl> <dt>

9702 (0x25E6)
</dt> <dt>



Errore di formato del record DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**\_ \_ creazione nodo errore \_ DNS \_ non riuscita**
</dt> <dd> <dl> <dt>

9703 (0x25E7)
</dt> <dt>



Errore di creazione del nodo in DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**\_tipo di \_ \_ record sconosciuto di errore \_ DNS**
</dt> <dd> <dl> <dt>

9704 (0x25E8)
</dt> <dt>



Tipo di record DNS sconosciuto.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**\_timeout del \_ record di errore \_ DNS \_**
</dt> <dd> <dl> <dt>

9705 (0x25E9)
</dt> <dt>



Timeout del record DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**\_nome errore \_ DNS \_ non \_ nella \_ zona**
</dt> <dd> <dl> <dt>

9706 (0x25EA)
</dt> <dt>



Nome non nella zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**\_errore DNS \_ \_ ciclo CNAME**
</dt> <dd> <dl> <dt>

9707 (0x25EB)
</dt> <dt>



Rilevato ciclo CNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**il \_ nodo errore DNS \_ \_ è \_ CNAME**
</dt> <dd> <dl> <dt>

9708 (0x25EC)
</dt> <dt>



Node è un record DNS CNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**\_ \_ collisione CNAME errore DNS \_**
</dt> <dd> <dl> <dt>

9709 (0x25ED)
</dt> <dt>



Un record CNAME esiste già per il nome specificato.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**\_record degli errori DNS \_ \_ solo \_ nella \_ radice della zona \_**
</dt> <dd> <dl> <dt>

9710 (0x25EE)
</dt> <dt>



Registra solo nella radice della zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**il \_ record di errore DNS \_ \_ \_ esiste già**
</dt> <dd> <dl> <dt>

9711 (0x25EF)
</dt> <dt>



Il record DNS esiste già.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**\_ \_ dati secondari degli errori DNS \_**
</dt> <dd> <dl> <dt>

9712 (0x25F0)
</dt> <dt>



Errore dati zona DNS secondaria.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**\_errore DNS \_ senza \_ creare \_ dati della cache \_**
</dt> <dd> <dl> <dt>

9713 (0x25F1)
</dt> <dt>



Non è stato possibile creare i dati della cache DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**\_il nome dell'errore DNS non \_ \_ \_ \_ esiste**
</dt> <dd> <dl> <dt>

9714 (0x25F2)
</dt> <dt>



Nome DNS inesistente.


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**\_errore di \_ creazione PTR avviso DNS \_ \_ non riuscito**
</dt> <dd> <dl> <dt>

9715 (0x25F3)
</dt> <dt>



Non è stato possibile creare il record puntatore (PTR).


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**dominio di avviso DNS non \_ \_ \_ eliminato**
</dt> <dd> <dl> <dt>

9716 (0x25F4)
</dt> <dt>



Il dominio DNS non è stato eliminato.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**\_errore DNS \_ DS non \_ disponibile**
</dt> <dd> <dl> <dt>

9717 (0x25F5)
</dt> <dt>



Il servizio directory non è disponibile.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**la \_ zona DS per gli errori DNS \_ \_ \_ \_ esiste già**
</dt> <dd> <dl> <dt>

9718 (0x25F6)
</dt> <dt>



La zona DNS esiste già nel servizio directory.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**\_errore DNS \_ senza \_ BOOTFILE \_ se \_ la \_ zona DS**
</dt> <dd> <dl> <dt>

9719 (0x25F7)
</dt> <dt>



Il server DNS non sta creando o leggendo il file di avvio per la zona DNS integrata del servizio directory.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**il \_ nodo di errore DNS \_ \_ è \_ DNAME**
</dt> <dd> <dl> <dt>

9720 (0x25F8)
</dt> <dt>



Il nodo è un record DNS DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**\_ \_ conflitto DNAME errore \_ DNS**
</dt> <dd> <dl> <dt>

9721 (0x25F9)
</dt> <dt>



Un record DNAME esiste già per il nome specificato.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**\_ciclo di \_ alias degli errori DNS \_**
</dt> <dd> <dl> <dt>

9722 (0x25FA)
</dt> <dt>



È stato rilevato un ciclo alias con record CNAME o DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**\_informazioni DNS \_ AXFR \_ completate**
</dt> <dd> <dl> <dt>

9751 (0x2617)
</dt> <dt>



AXFR DNS (trasferimento di zona) completato.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**\_errore DNS \_ AXFR**
</dt> <dd> <dl> <dt>

9752 (0x2618)
</dt> <dt>



Trasferimento di zona DNS non riuscito.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**le \_ informazioni DNS hanno \_ aggiunto \_ \_ WINS locale**
</dt> <dd> <dl> <dt>

9753 (0x2619)
</dt> <dt>



Aggiunto server WINS locale.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**\_stato DNS \_ continua \_ necessario**
</dt> <dd> <dl> <dt>

9801 (0x2649)
</dt> <dt>



Per la chiamata di aggiornamento sicuro è necessario continuare la richiesta di aggiornamento.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**\_errore DNS \_ senza \_ Tcpip**
</dt> <dd> <dl> <dt>

9851 (0x267B)
</dt> <dt>



Il protocollo di rete TCP/IP non è installato.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**\_errore DNS \_ nessun \_ \_ server DNS**
</dt> <dd> <dl> <dt>

9852 (0x267C)
</dt> <dt>



Nessun server DNS configurato per il sistema locale.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**\_il DP di errore DNS non \_ \_ \_ \_ esiste**
</dt> <dd> <dl> <dt>

9901 (0x26AD)
</dt> <dt>



La partizione di directory specificata non esiste.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**il \_ DP degli errori DNS \_ \_ \_ esiste già**
</dt> <dd> <dl> <dt>

9902 (0x26AE)
</dt> <dt>



La partizione di directory specificata esiste già.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**\_errore DNS \_ DP \_ non \_ integrato**
</dt> <dd> <dl> <dt>

9903 (0x26AF)
</dt> <dt>



Questo server DNS non è integrato nella partizione di directory specificata.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**il \_ DP degli errori DNS è \_ \_ già \_ integrato**
</dt> <dd> <dl> <dt>

9904 (0x26B0)
</dt> <dt>



Questo server DNS è già integrato nella partizione di directory specificata.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**\_errore DNS \_ DP \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

9905 (0x26B1)
</dt> <dt>



La partizione di directory non è disponibile in questo momento. Attendere qualche minuto e riprovare più tardi.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**\_ \_ \_ errore FSMO DP errore \_ DNS**
</dt> <dd> <dl> <dt>

9906 (0x26B2)
</dt> <dt>



Operazione non riuscita perché non è stato possibile raggiungere il ruolo FSMO master per la denominazione dei domini. Il controller di dominio che contiene il ruolo FSMO master per la denominazione dei domini non è attivo o non è in grado di gestire la richiesta o non è in esecuzione Windows Server 2003 o versione successiva.


</dt> </dl> </dd> <dt>

<span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**
</dt> <dd> <dl> <dt>

10004 (0x2714)
</dt> <dt>



Un'operazione di blocco è stata interrotta da una chiamata a WSACancelBlockingCall.


</dt> </dl> </dd> <dt>

<span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**
</dt> <dd> <dl> <dt>

10009 (0x2719)
</dt> <dt>



L'handle di file specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**
</dt> <dd> <dl> <dt>

10013 (0x271D)
</dt> <dt>



È stato effettuato un tentativo di accesso a un socket in modo non consentito dalle autorizzazioni di accesso.


</dt> </dl> </dd> <dt>

<span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**
</dt> <dd> <dl> <dt>

10014 (0x271E)
</dt> <dt>



Il sistema ha rilevato un indirizzo puntatore non valido durante il tentativo di usare un argomento puntatore in una chiamata.


</dt> </dl> </dd> <dt>

<span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**
</dt> <dd> <dl> <dt>

10022 (0x2726)
</dt> <dt>



Argomento fornito non valido.


</dt> </dl> </dd> <dt>

<span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**
</dt> <dd> <dl> <dt>

10024 (0x2728)
</dt> <dt>



Troppi socket aperti.


</dt> </dl> </dd> <dt>

<span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**
</dt> <dd> <dl> <dt>

10035 (0x2733)
</dt> <dt>



Non è stato possibile completare immediatamente un'operazione socket non bloccante.


</dt> </dl> </dd> <dt>

<span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**
</dt> <dd> <dl> <dt>

10036 (0x2734)
</dt> <dt>



È in corso un'operazione di blocco.


</dt> </dl> </dd> <dt>

<span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**
</dt> <dd> <dl> <dt>

10037 (0x2735)
</dt> <dt>



Si è tentato di eseguire un'operazione su un socket non bloccato sul quale era già in corso un'operazione.


</dt> </dl> </dd> <dt>

<span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**
</dt> <dd> <dl> <dt>

10038 (0x2736)
</dt> <dt>



Si è tentato di eseguire un'operazione su un elemento che non è un socket.


</dt> </dl> </dd> <dt>

<span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**
</dt> <dd> <dl> <dt>

10039 (0x2737)
</dt> <dt>



Un indirizzo obbligatorio è stato omesso da un'operazione su un socket.


</dt> </dl> </dd> <dt>

<span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**
</dt> <dd> <dl> <dt>

10040 (0x2738)
</dt> <dt>



Le dimensioni di un messaggio inviato su un socket di datagramma erano maggiori del buffer del messaggio interno, erano presenti altri limiti di rete oppure le dimensioni del buffer utilizzato per ricevere un datagramma erano inferiori al datagramma stesso.


</dt> </dl> </dd> <dt>

<span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**
</dt> <dd> <dl> <dt>

10041 (0x2739)
</dt> <dt>



Un protocollo è stato specificato nella chiamata di funzione socket che non supporta la semantica del tipo di socket richiesto.


</dt> </dl> </dd> <dt>

<span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**
</dt> <dd> <dl> <dt>

10042 (0x273A)
</dt> <dt>



È stata specificata un'opzione o un livello sconosciuto, non valido o non supportato in una chiamata a getsockopt o setsockopt.


</dt> </dl> </dd> <dt>

<span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**
</dt> <dd> <dl> <dt>

10043 (0x273B)
</dt> <dt>



Il protocollo richiesto non è stato configurato nel sistema o non ne esiste alcuna implementazione.


</dt> </dl> </dd> <dt>

<span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**
</dt> <dd> <dl> <dt>

10044 (0x273C)
</dt> <dt>



Il supporto per il tipo di socket specificato non esiste in questa famiglia di indirizzi.


</dt> </dl> </dd> <dt>

<span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**ILWSAEOPNOTSUPP**
</dt> <dd> <dl> <dt>

10045 (0x273D)
</dt> <dt>



L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento.


</dt> </dl> </dd> <dt>

<span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**
</dt> <dd> <dl> <dt>

10046 (0x273E)
</dt> <dt>



La famiglia di protocolli non è stata configurata nel sistema o non ne esiste alcuna implementazione.


</dt> </dl> </dd> <dt>

<span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**
</dt> <dd> <dl> <dt>

10047 (0x273F)
</dt> <dt>



È stato usato un indirizzo incompatibile con il protocollo richiesto.


</dt> </dl> </dd> <dt>

<span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**
</dt> <dd> <dl> <dt>

10048 (0x2740)
</dt> <dt>



Only one usage of each socket address (protocol/network address/port) is normally permitted.


</dt> </dl> </dd> <dt>

<span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**
</dt> <dd> <dl> <dt>

10049 (0x2741)
</dt> <dt>



L'indirizzo richiesto non è valido nel contesto.


</dt> </dl> </dd> <dt>

<span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**
</dt> <dd> <dl> <dt>

10050 (0x2742)
</dt> <dt>



Rete inattiva rilevata durante l'operazione del socket.


</dt> </dl> </dd> <dt>

<span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**
</dt> <dd> <dl> <dt>

10051 (0x2743)
</dt> <dt>



Si è tentato di eseguire un'operazione socket in una rete irraggiungibile.


</dt> </dl> </dd> <dt>

<span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**
</dt> <dd> <dl> <dt>

10052 (0x2744)
</dt> <dt>



La connessione è stata interrotta a causa di un'attività keep-alive che rileva un errore durante l'esecuzione dell'operazione.


</dt> </dl> </dd> <dt>

<span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**
</dt> <dd> <dl> <dt>

10053 (0x2745)
</dt> <dt>



Connessione interrotta dal software del computer host.


</dt> </dl> </dd> <dt>

<span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**
</dt> <dd> <dl> <dt>

10054 (0x2746)
</dt> <dt>



Connessione in corso interrotta forzatamente dall'host remoto.


</dt> </dl> </dd> <dt>

<span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**
</dt> <dd> <dl> <dt>

10055 (0x2747)
</dt> <dt>



Non è stato possibile eseguire un'operazione su un socket perché il sistema non dispone di spazio sufficiente per il buffer o perché una coda era piena.


</dt> </dl> </dd> <dt>

<span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**
</dt> <dd> <dl> <dt>

10056 (0x2748)
</dt> <dt>



È stata effettuata una richiesta di connessione su un socket già connesso.


</dt> </dl> </dd> <dt>

<span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**
</dt> <dd> <dl> <dt>

10057 (0x2749)
</dt> <dt>



Socket non connesso e indirizzo non fornito durante l'invio su un socket di datagramma che utilizza una chiamata sendto. Richiesta di invio o ricezione di dati annullata.


</dt> </dl> </dd> <dt>

<span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**
</dt> <dd> <dl> <dt>

10058 (0x274A)
</dt> <dt>



Socket chiuso nella direzione specificata da una precedente chiamata di arresto. Richiesta di invio o ricezione dati annullata.


</dt> </dl> </dd> <dt>

<span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**
</dt> <dd> <dl> <dt>

10059 (0x274B)
</dt> <dt>



Troppi riferimenti a un oggetto kernel.


</dt> </dl> </dd> <dt>

<span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**
</dt> <dd> <dl> <dt>

10060 (0x274C)
</dt> <dt>



Tentativo di connessione non riuscito perché l'entità connessa non ha risposto correttamente dopo un periodo di tempo o la connessione stabilita non è riuscita perché l'host connesso non ha risposto.


</dt> </dl> </dd> <dt>

<span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**
</dt> <dd> <dl> <dt>

10061 (0x274D)
</dt> <dt>



Non è stato possibile connettersi perché il computer di destinazione lo ha rifiutato attivamente.


</dt> </dl> </dd> <dt>

<span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**
</dt> <dd> <dl> <dt>

10062 (0x274E)
</dt> <dt>



Impossibile tradurre il nome.


</dt> </dl> </dd> <dt>

<span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**
</dt> <dd> <dl> <dt>

10063 (0x274F)
</dt> <dt>



Il nome o il componente del nome è troppo lungo.


</dt> </dl> </dd> <dt>

<span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**
</dt> <dd> <dl> <dt>

10064 (0x2750)
</dt> <dt>



Un'operazione socket non è riuscita perché l'host di destinazione è inattivo.


</dt> </dl> </dd> <dt>

<span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**
</dt> <dd> <dl> <dt>

10065 (0x2751)
</dt> <dt>



Tentativo di operazione del socket verso un host non raggiungibile.


</dt> </dl> </dd> <dt>

<span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**
</dt> <dd> <dl> <dt>

10066 (0x2752)
</dt> <dt>



Non è possibile rimuovere una directory che non è vuota.


</dt> </dl> </dd> <dt>

<span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**
</dt> <dd> <dl> <dt>

10067 (0x2753)
</dt> <dt>



Un'implementazione di Windows Sockets può avere un limite al numero di applicazioni che possono utilizzarlo simultaneamente.


</dt> </dl> </dd> <dt>

<span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**
</dt> <dd> <dl> <dt>

10068 (0x2754)
</dt> <dt>



Quota esaurita.


</dt> </dl> </dd> <dt>

<span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**
</dt> <dd> <dl> <dt>

10069 (0x2755)
</dt> <dt>



Quota del disco esaurita.


</dt> </dl> </dd> <dt>

<span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**
</dt> <dd> <dl> <dt>

10070 (0x2756)
</dt> <dt>



Il riferimento all'handle di file non è più disponibile.


</dt> </dl> </dd> <dt>

<span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**
</dt> <dd> <dl> <dt>

10071 (0x2757)
</dt> <dt>



Elemento non disponibile localmente.


</dt> </dl> </dd> <dt>

<span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**
</dt> <dd> <dl> <dt>

10091 (0x276B)
</dt> <dt>



WSAStartup non può funzionare in questo momento perché il sistema sottostante usato per fornire servizi di rete non è attualmente disponibile.


</dt> </dl> </dd> <dt>

<span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**
</dt> <dd> <dl> <dt>

10092 (0x276C)
</dt> <dt>



La versione richiesta di Windows Sockets non è supportata.


</dt> </dl> </dd> <dt>

<span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**
</dt> <dd> <dl> <dt>

10093 (0x276D)
</dt> <dt>



L'applicazione non ha chiamato WSAStartup o WSAStartup non è riuscito.


</dt> </dl> </dd> <dt>

<span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON nativo**
</dt> <dd> <dl> <dt>

10101 (0x2775)
</dt> <dt>



Restituito da WSARecv o WSARecvFrom per indicare che la parte remota ha avviato una sequenza di arresto normale.


</dt> </dl> </dd> <dt>

<span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**
</dt> <dd> <dl> <dt>

10102 (0x2776)
</dt> <dt>



WSALookupServiceNext non può restituire altri risultati.


</dt> </dl> </dd> <dt>

<span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**
</dt> <dd> <dl> <dt>

10103 (0x2777)
</dt> <dt>



È stata effettuata una chiamata a WSALookupServiceEnd mentre la chiamata era ancora in fase di elaborazione. La chiamata è stata annullata.


</dt> </dl> </dd> <dt>

<span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**
</dt> <dd> <dl> <dt>

10104 (0x2778)
</dt> <dt>



La tabella delle chiamate di procedura non è valida.


</dt> </dl> </dd> <dt>

<span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**
</dt> <dd> <dl> <dt>

10105 (0x2779)
</dt> <dt>



Il provider di servizi richiesto non è valido.


</dt> </dl> </dd> <dt>

<span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**
</dt> <dd> <dl> <dt>

10106 (0x277A)
</dt> <dt>



Non è stato possibile caricare o inizializzare il provider di servizi richiesto.


</dt> </dl> </dd> <dt>

<span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**
</dt> <dd> <dl> <dt>

10107 (0x277B)
</dt> <dt>



Una chiamata di sistema non è riuscita.


</dt> </dl> </dd> <dt>

<span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**WSASERVICE \_ non \_ trovato**
</dt> <dd> <dl> <dt>

10108 (0x277C)
</dt> <dt>



Nessun servizio di questo tipo è noto. Il servizio non è stato trovato nello spazio dei nomi specificato.


</dt> </dl> </dd> <dt>

<span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**WSATYPE \_ non \_ trovato**
</dt> <dd> <dl> <dt>

10109 (0x277D)
</dt> <dt>



La classe specificata non è stata trovata.


</dt> </dl> </dd> <dt>

<span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA \_ E \_ nient' \_ altro**
</dt> <dd> <dl> <dt>

10110 (0x277E)
</dt> <dt>



WSALookupServiceNext non può restituire altri risultati.


</dt> </dl> </dd> <dt>

<span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA \_ E \_ annullato**
</dt> <dd> <dl> <dt>

10111 (0x277F)
</dt> <dt>



È stata effettuata una chiamata a WSALookupServiceEnd mentre la chiamata era ancora in fase di elaborazione. La chiamata è stata annullata.


</dt> </dl> </dd> <dt>

<span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**
</dt> <dd> <dl> <dt>

10112 (0x2780)
</dt> <dt>



Una query sul database non è riuscita perché è stata rifiutata attivamente.


</dt> </dl> </dd> <dt>

<span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**WSAHOST \_ non \_ trovato**
</dt> <dd> <dl> <dt>

11001 (0x2AF9)
</dt> <dt>



L'host è sconosciuto.


</dt> </dl> </dd> <dt>

<span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY di \_ nuovo**
</dt> <dd> <dl> <dt>

11002 (0x2AFA)
</dt> <dt>



Generalmente, questo è un errore temporaneo che si verifica durante la risoluzione dei nomi host e significa che il server locale non ha ricevuto una risposta da un server autorevole.


</dt> </dl> </dd> <dt>

<span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**\_ripristino WSANO**
</dt> <dd> <dl> <dt>

11003 (0x2AFB)
</dt> <dt>



Si è verificato un errore irreversibile durante la ricerca nel database.


</dt> </dl> </dd> <dt>

<span id="WSANO_DATA"></span><span id="wsano_data"></span>**\_dati WSANO**
</dt> <dd> <dl> <dt>

11004 (0x2AFC)
</dt> <dt>



Il nome richiesto è valido, ma non sono stati trovati dati del tipo richiesto.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**\_ricevitori QoS di WSA \_**
</dt> <dd> <dl> <dt>

11005 (0x2AFD)
</dt> <dt>



È arrivata almeno una riserva.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**\_mittenti QoS per WSA \_**
</dt> <dd> <dl> <dt>

11006 (0x2AFE)
</dt> <dt>



È arrivato almeno un percorso.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**\_QoS \_ non disponibile \_ per WSA**
</dt> <dd> <dl> <dt>

11007 (0x2AFF)
</dt> <dt>



Nessun mittenti.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**\_ \_ nessun ricevitore di QoS per WSA \_**
</dt> <dd> <dl> <dt>

11008 (0x2B00)
</dt> <dt>



Nessun ricevitore.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**\_richiesta QoS per WSA \_ \_ confermata**
</dt> <dd> <dl> <dt>

11009 (0x2B01)
</dt> <dt>



La riserva è stata confermata.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**\_errore di \_ ammissione \_ QoS di WSA**
</dt> <dd> <dl> <dt>

11010 (0x2B02)
</dt> <dt>



Errore dovuto a risorse insufficienti.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**\_errore dei \_ criteri \_ QoS di WSA**
</dt> <dd> <dl> <dt>

11011 (0x2B03)
</dt> <dt>



Rifiutato per motivi amministrativi: credenziali non valide.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**\_stile non \_ valido \_ QoS per WSA**
</dt> <dd> <dl> <dt>

11012 (0x2B04)
</dt> <dt>



Stile sconosciuto o in conflitto.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**\_oggetto non \_ valido \_ QoS di WSA**
</dt> <dd> <dl> <dt>

11013 (0x2B05)
</dt> <dt>



Problema con una parte del buffer filterspec o providerspecific in generale.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**\_errore di \_ traffico QoS WSA \_ CTRL \_**
</dt> <dd> <dl> <dt>

11014 (0x2B06)
</dt> <dt>



Problemi con alcune parti del flowspec.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**\_ \_ errore generico di QoS WSA \_**
</dt> <dd> <dl> <dt>

11015 (0x2B07)
</dt> <dt>



Errore QOS generale.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**\_ESERVICETYPE QoS per WSA \_**
</dt> <dd> <dl> <dt>

11016 (0x2B08)
</dt> <dt>



È stato trovato un tipo di servizio non valido o non riconosciuto in flowspec.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**\_EFLOWSPEC QoS per WSA \_**
</dt> <dd> <dl> <dt>

11017 (0x2B09)
</dt> <dt>



Flowspec non valido o incoerente trovato nella struttura QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**\_EPROVSPECBUF QoS per WSA \_**
</dt> <dd> <dl> <dt>

11018 (0x2B0A)
</dt> <dt>



Buffer specifico del provider QOS non valido.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**\_EFILTERSTYLE QoS per WSA \_**
</dt> <dd> <dl> <dt>

11019 (0x2B0B)
</dt> <dt>



È stato usato uno stile di filtro QOS non valido.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**\_EFILTERTYPE QoS per WSA \_**
</dt> <dd> <dl> <dt>

11020 (0x2B0C)
</dt> <dt>



È stato usato un tipo di filtro QOS non valido.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**\_EFILTERCOUNT QoS per WSA \_**
</dt> <dd> <dl> <dt>

11021 (0x2B0D)
</dt> <dt>



Nel FLOWDESCRIPTOR è stato specificato un numero non corretto di FILTERSPECs QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**\_EOBJLENGTH QoS per WSA \_**
</dt> <dd> <dl> <dt>

11022 (0x2B0E)
</dt> <dt>



In un buffer specifico del provider QOS è stato specificato un oggetto con un campo ObjectLength non valido.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**\_EFLOWCOUNT QoS per WSA \_**
</dt> <dd> <dl> <dt>

11023 (0x2B0F)
</dt> <dt>



Nella struttura QOS è stato specificato un numero errato di descrittori di flusso.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**\_EUNKOWNPSOBJ QoS per WSA \_**
</dt> <dd> <dl> <dt>

11024 (0x2B10)
</dt> <dt>



Trovato oggetto non riconosciuto nel buffer di QOS specifico del provider.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**\_EPOLICYOBJ QoS per WSA \_**
</dt> <dd> <dl> <dt>

11025 (0x2B11)
</dt> <dt>



Trovato oggetto criteri non valido nel buffer specifico del provider QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**\_EFLOWDESC QoS per WSA \_**
</dt> <dd> <dl> <dt>

11026 (0x2B12)
</dt> <dt>



Descrittore di flusso QOS non valido trovato nell'elenco dei descrittori di flusso.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**\_EPSFLOWSPEC QoS per WSA \_**
</dt> <dd> <dl> <dt>

11027 (0x2B13)
</dt> <dt>



Flowspec non valido o incoerente trovato nel buffer del provider QOS specifico.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**\_EPSFILTERSPEC QoS per WSA \_**
</dt> <dd> <dl> <dt>

11028 (0x2B14)
</dt> <dt>



Trovato FILTERSPEC non valido nel buffer specifico del provider QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**\_ESDMODEOBJ QoS per WSA \_**
</dt> <dd> <dl> <dt>

11029 (0x2B15)
</dt> <dt>



Trovato oggetto modalità di scarto di forma non valido nel buffer del provider QOS specifico.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**\_ESHAPERATEOBJ QoS per WSA \_**
</dt> <dd> <dl> <dt>

11030 (0x2B16)
</dt> <dt>



Trovato oggetto frequenza di shaping non valido nel buffer di QOS specifico del provider.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**\_ \_ PETYPE riservato WSA \_ QoS**
</dt> <dd> <dl> <dt>

11031 (0x2B17)
</dt> <dt>



Un elemento dei criteri riservato è stato trovato nel buffer specifico del provider QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**\_host sicuro \_ WSA \_ non \_ trovato**
</dt> <dd> <dl> <dt>

11032 (0x2B18)
</dt> <dt>



Questo host non è noto in modo sicuro.


</dt> </dl> </dd> <dt>

<span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**\_ \_ \_ errore criterio nome IPSec \_ WSA**
</dt> <dd> <dl> <dt>

11033 (0x2B19)
</dt> <dt>



Non è stato possibile aggiungere i criteri IPSEC basati su nome.


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

 

 




