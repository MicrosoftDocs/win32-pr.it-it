---
description: Descrive i codici di errore 4000-5999 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: 1d2f7160-6322-4c75-abbc-4a882bbdf7ce
title: Codici di errore di sistema (4000-5999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: bfd39042489f2a92ff2eb13df92a22e392c5405e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126891"
---
# <a name="system-error-codes-4000-5999"></a>Codici di errore di sistema (4000-5999)

> [!NOTE]
> Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema. Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .

Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) per gli errori da 4000 a 5999. Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .

<dl> <dt>

<span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**ERRORE \_ \_ interno WINS**
</dt> <dd> <dl> <dt>

4000 (0xFA0)
</dt> <dt>



WINS ha rilevato un errore durante l'elaborazione del comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**l'errore \_ non può essere il \_ \_ del \_ \_ WINS locale**
</dt> <dd> <dl> <dt>

4001 (0xFA1)
</dt> <dt>



Non è possibile eliminare la WINS locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**ERRORE \_ \_ init statico**
</dt> <dd> <dl> <dt>

4002 (0xFA2)
</dt> <dt>



L'importazione dal file non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**ERRORE \_ di \_ backup Inc**
</dt> <dd> <dl> <dt>

4003 (0xFA3)
</dt> <dt>



Il backup non è riuscito. È stato eseguito un backup completo prima?


</dt> </dl> </dd> <dt>

<span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**ERRORE \_ \_ backup completo**
</dt> <dd> <dl> <dt>

4004 (0xFA4)
</dt> <dt>



Il backup non è riuscito. Controllare la directory in cui si sta eseguendo il backup del database.


</dt> </dl> </dd> <dt>

<span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**ERRORE \_ REC \_ non \_ esistente**
</dt> <dd> <dl> <dt>

4005 (0xFA5)
</dt> <dt>



Il nome non esiste nel database WINS.


</dt> </dl> </dd> <dt>

<span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**ERRORE \_ RPL \_ non \_ consentito**
</dt> <dd> <dl> <dt>

4006 (0xFA6)
</dt> <dt>



La replica con un partner non configurato non è consentita.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**\_errore PEERDIST \_ versione CONTENTINFO non \_ \_ supportata**
</dt> <dd> <dl> <dt>

4050 (0xFD2)
</dt> <dt>



La versione delle informazioni sul contenuto fornite non è supportata.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**\_errore PEERDIST \_ non è possibile \_ analizzare \_ CONTENTINFO**
</dt> <dd> <dl> <dt>

4051 (0xFD3)
</dt> <dt>



Le informazioni sul contenuto fornite non sono valide.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**\_ \_ mancano i dati nell'errore PEERDIST \_**
</dt> <dd> <dl> <dt>

4052 (0xFD4)
</dt> <dt>



I dati richiesti non sono stati trovati nelle cache locali o peer.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**\_errore PEERDIST \_ \_**
</dt> <dd> <dl> <dt>

4053 (0xFD5)
</dt> <dt>



Nessun altro dato disponibile o richiesto.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**\_errore PEERDIST \_ non \_ inizializzato**
</dt> <dd> <dl> <dt>

4054 (0xFD6)
</dt> <dt>



L'oggetto fornito non è stato inizializzato.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**\_errore PEERDIST \_ già \_ inizializzato**
</dt> <dd> <dl> <dt>

4055 (0xFD7)
</dt> <dt>



L'oggetto fornito è già stato inizializzato.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**\_arresto errore \_ PEERDIST \_ in \_ corso**
</dt> <dd> <dl> <dt>

4056 (0xFD8)
</dt> <dt>



È già in corso un'operazione di arresto.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**\_errore PEERDIST \_ invalidato**
</dt> <dd> <dl> <dt>

4057 (0xFD9)
</dt> <dt>



L'oggetto fornito è già stato invalidato.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**l' \_ errore \_ PEERDIST \_ esiste già**
</dt> <dd> <dl> <dt>

4058 (0xFDA)
</dt> <dt>



Un elemento esiste già e non è stato sostituito.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**\_operazione di errore PEERDIST \_ \_ NotFound**
</dt> <dd> <dl> <dt>

4059 (0xFDB)
</dt> <dt>



Non è possibile annullare l'operazione richiesta perché è già stata completata.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**\_errore PEERDIST \_ già \_ completato**
</dt> <dd> <dl> <dt>

4060 (0xFDC)
</dt> <dt>



Non è possibile eseguire l'operazione variante richiesta perché è già stata eseguita.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**\_errore PEERDIST \_ fuori \_ \_ limite**
</dt> <dd> <dl> <dt>

4061 (0xFDD)
</dt> <dt>



Un'operazione ha eseguito l'accesso ai dati oltre i limiti dei dati validi.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**versione dell'errore PEERDIST non \_ \_ \_ supportata**
</dt> <dd> <dl> <dt>

4062 (0xFDE)
</dt> <dt>



La versione richiesta non è supportata.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**\_configurazione errore PEERDIST \_ non valida \_**
</dt> <dd> <dl> <dt>

4063 (0xFDF)
</dt> <dt>



Valore di configurazione non valido.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**\_errore PEERDIST \_ non \_ concesso in licenza**
</dt> <dd> <dl> <dt>

4064 (0xFE0)
</dt> <dt>



Lo SKU non è concesso in licenza.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**\_servizio errori PEERDIST non \_ \_ disponibile**
</dt> <dd> <dl> <dt>

4065 (0xFE1)
</dt> <dt>



Il servizio PeerDist è ancora in fase di inizializzazione e sarà disponibile a breve.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**\_errore di \_ ATTENDIBILità PEERDIST \_**
</dt> <dd> <dl> <dt>

4066 (0xFE2)
</dt> <dt>



La comunicazione con uno o più computer verrà temporaneamente bloccata a causa di errori recenti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**ERRORE \_ in \_ conflitto di indirizzi DHCP \_**
</dt> <dd> <dl> <dt>

4100 (0x1004)
</dt> <dt>



Il client DHCP ha ottenuto un indirizzo IP già in uso nella rete. L'interfaccia locale verrà disabilitata fino a quando il client DHCP non potrà ottenere un nuovo indirizzo.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**ERRORE \_ \_ GUID WMI \_ non \_ trovato**
</dt> <dd> <dl> <dt>

4200 (0x1068)
</dt> <dt>



Il GUID passato non è stato riconosciuto come valido da un provider di dati WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**ERRORE \_ dell' \_ istanza WMI \_ non \_ trovata**
</dt> <dd> <dl> <dt>

4201 (0x1069)
</dt> <dt>



Il nome dell'istanza passato non è stato riconosciuto come valido da un provider di dati WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ERRORE \_ ID elemento WMI \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

4202 (0x106A)
</dt> <dt>



L'ID dell'elemento dati passato non è stato riconosciuto come valido da un provider di dati WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**ERRORE \_ WMI \_ Riprova \_**
</dt> <dd> <dl> <dt>

4203 (0x106B)
</dt> <dt>



Non è stato possibile completare la richiesta WMI ed è necessario riprovare.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**ERRORE \_ WMI \_ DP \_ non \_ trovato**
</dt> <dd> <dl> <dt>

4204 (0x106C)
</dt> <dt>



Impossibile trovare il provider di dati WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**ERRORE \_ di \_ riferimento dell'istanza non risolta WMI \_ \_**
</dt> <dd> <dl> <dt>

4205 (0x106D)
</dt> <dt>



Il provider di dati WMI fa riferimento a un set di istanze che non è stato registrato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**ERRORE \_ WMI \_ già \_ abilitato**
</dt> <dd> <dl> <dt>

4206 (0x106E)
</dt> <dt>



Il blocco di dati WMI o la notifica degli eventi è già stata abilitata.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**ERRORE \_ \_ GUID WMI \_ disconnesso**
</dt> <dd> <dl> <dt>

4207 (0x106F)
</dt> <dt>



Il blocco di dati WMI non è più disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**ERRORE \_ server WMI non \_ \_ disponibile**
</dt> <dd> <dl> <dt>

4208 (0x1070)
</dt> <dt>



Il servizio dati WMI non è disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**ERRORE \_ WMI \_ DP \_ non riuscito**
</dt> <dd> <dl> <dt>

4209 (0x1071)
</dt> <dt>



Il provider di dati WMI non è riuscito a eseguire la richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**ERRORE \_ \_ MOF WMI non valido \_**
</dt> <dd> <dl> <dt>

4210 (0x1072)
</dt> <dt>



Le informazioni MOF WMI non sono valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**ERRORE \_ WMI \_ REGINFO non valido \_**
</dt> <dd> <dl> <dt>

4211 (0x1073)
</dt> <dt>



Le informazioni di registrazione WMI non sono valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**ERRORE \_ WMI \_ già \_ disabilitato**
</dt> <dd> <dl> <dt>

4212 (0x1074)
</dt> <dt>



Il blocco di dati WMI o la notifica degli eventi è già stata disabilitata.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**ERRORE \_ WMI di sola \_ lettura \_**
</dt> <dd> <dl> <dt>

4213 (0x1075)
</dt> <dt>



Il blocco di dati o l'elemento di dati WMI è di sola lettura.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**ERRORE \_ set WMI Error \_ \_**
</dt> <dd> <dl> <dt>

4214 (0x1076)
</dt> <dt>



Impossibile modificare l'elemento di dati WMI o il blocco di dati.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**ERRORE \_ non \_ appcontainer**
</dt> <dd> <dl> <dt>

4250 (0x109A)
</dt> <dt>



Questa operazione è valida solo nel contesto di un contenitore di app.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**ERRORE \_ appcontainer \_ obbligatorio**
</dt> <dd> <dl> <dt>

4251 (0x109B)
</dt> <dt>



Questa applicazione può essere eseguita solo nel contesto di un contenitore di app.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**ERRORE \_ non \_ supportato \_ in \_ appcontainer**
</dt> <dd> <dl> <dt>

4252 (0x109C)
</dt> <dt>



Questa funzionalità non è supportata nel contesto di un contenitore di app.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**ERRORE \_ di \_ \_ lunghezza SID \_ pacchetto non valido**
</dt> <dd> <dl> <dt>

4253 (0x109D)
</dt> <dt>



La lunghezza del SID specificato non è una lunghezza valida per i SID del contenitore di app.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**ERRORE \_ supporto non valido \_**
</dt> <dd> <dl> <dt>

4300 (0x10CC)
</dt> <dt>



L'identificatore del supporto non rappresenta un supporto valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**ERRORE \_ di \_ libreria non valida**
</dt> <dd> <dl> <dt>

4301 (0x10CD)
</dt> <dt>



L'identificatore della libreria non rappresenta una libreria valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**ERRORE \_ nel \_ pool di supporti non valido \_**
</dt> <dd> <dl> <dt>

4302 (0x10CE)
</dt> <dt>



L'identificatore del pool di supporti non rappresenta un pool di supporti valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**supporto dell'unità di errore non \_ \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

4303 (0x10CF)
</dt> <dt>



L'unità e il supporto non sono compatibili o sono presenti in librerie diverse.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**\_supporto errori \_ offline**
</dt> <dd> <dl> <dt>

4304 (0x10D0)
</dt> <dt>



Il supporto attualmente esiste in una libreria offline e deve essere online per eseguire questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**\_libreria errori \_ offline**
</dt> <dd> <dl> <dt>

4305 (0x10D1)
</dt> <dt>



Impossibile eseguire l'operazione su una libreria offline.


</dt> </dl> </dd> <dt>

<span id="ERROR_EMPTY"></span><span id="error_empty"></span>**ERRORE \_ vuoto**
</dt> <dd> <dl> <dt>

4306 (0x10D2)
</dt> <dt>



La libreria, l'unità o il pool di supporti è vuoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**ERRORE \_ non \_ vuoto**
</dt> <dd> <dl> <dt>

4307 (0x10D3)
</dt> <dt>



Per eseguire questa operazione, è necessario che la libreria, l'unità o il pool di supporti sia vuoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**supporto errori non \_ \_ disponibile**
</dt> <dd> <dl> <dt>

4308 (0x10D4)
</dt> <dt>



Nessun supporto è attualmente disponibile in questo pool di supporti o nella libreria.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**\_risorsa errore \_ disabilitata**
</dt> <dd> <dl> <dt>

4309 (0x10D5)
</dt> <dt>



Una risorsa necessaria per questa operazione è disabilitata.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**ERRORE \_ di \_ pulizia non valido**
</dt> <dd> <dl> <dt>

4310 (0x10D6)
</dt> <dt>



L'identificatore del supporto non rappresenta una pulitura valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**ERRORE \_ \_ di \_ pulizia**
</dt> <dd> <dl> <dt>

4311 (0x10D7)
</dt> <dt>



L'unità non può essere pulita o non supporta la pulizia.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**\_ \_ Impossibile trovare l'oggetto errore \_**
</dt> <dd> <dl> <dt>

4312 (0x10D8)
</dt> <dt>



L'identificatore di oggetto non rappresenta un oggetto valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**ERRORE nel \_ database \_**
</dt> <dd> <dl> <dt>

4313 (0x10D9)
</dt> <dt>



Impossibile leggere o scrivere nel database.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**DATABASE con errori \_ \_ completo**
</dt> <dd> <dl> <dt>

4314 (0x10DA)
</dt> <dt>



Il database è pieno.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**\_supporti errori \_ incompatibili**
</dt> <dd> <dl> <dt>

4315 (0x10DB)
</dt> <dt>



Il supporto non è compatibile con il dispositivo o il pool di supporti.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**\_risorsa errore \_ non \_ presente**
</dt> <dd> <dl> <dt>

4316 (0x10DC)
</dt> <dt>



La risorsa necessaria per questa operazione non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**ERRORE \_ operazione non valida \_**
</dt> <dd> <dl> <dt>

4317 (0x10DD)
</dt> <dt>



Identificatore dell'operazione non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**\_supporto errori \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

4318 (0x10DE)
</dt> <dt>



Il supporto non è montato o pronto per l'uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**dispositivo di errore \_ \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

4319 (0x10DF)
</dt> <dt>



Il dispositivo non è pronto per l'uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**richiesta di errore \_ \_ rifiutata**
</dt> <dd> <dl> <dt>

4320 (0x10E0)
</dt> <dt>



L'operatore o l'amministratore ha rifiutato la richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**ERRORE \_ dell' \_ oggetto unità non valido \_**
</dt> <dd> <dl> <dt>

4321 (0x10E1)
</dt> <dt>



L'identificatore dell'unità non rappresenta un'unità valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**\_libreria errori \_ completa**
</dt> <dd> <dl> <dt>

4322 (0x10E2)
</dt> <dt>



La libreria è piena. Nessun slot disponibile per l'utilizzo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**ERRORE \_ medio \_ non \_ accessibile**
</dt> <dd> <dl> <dt>

4323 (0x10E3)
</dt> <dt>



Il trasporto non può accedere al supporto.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**ERRORE \_ non è possibile \_ \_ caricare il \_ supporto**
</dt> <dd> <dl> <dt>

4324 (0x10E4)
</dt> <dt>



Impossibile caricare il supporto nell'unità.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**ERRORE \_ \_ nell' \_ inventario dell' \_ unità**
</dt> <dd> <dl> <dt>

4325 (0x10E5)
</dt> <dt>



Impossibile recuperare lo stato dell'unità.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**ERRORE \_ \_ di \_ inventario dello \_ slot**
</dt> <dd> <dl> <dt>

4326 (0x10E6)
</dt> <dt>



Non è possibile recuperare lo stato dello slot.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**ERRORE \_ non è possibile \_ eseguire l' \_ inventario del \_ trasporto**
</dt> <dd> <dl> <dt>

4327 (0x10E7)
</dt> <dt>



Impossibile recuperare lo stato del trasporto.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**\_trasporto errori \_ completo**
</dt> <dd> <dl> <dt>

4328 (0x10E8)
</dt> <dt>



Impossibile utilizzare il trasporto perché è già in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**errore durante il \_ controllo di \_ inserimento/espulsione**
</dt> <dd> <dl> <dt>

4329 (0x10E9)
</dt> <dt>



Non è possibile aprire o chiudere la porta di inserimento/espulsione.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**ERRORE \_ non è possibile \_ \_ rimuovere il \_ \_ supporto montato**
</dt> <dd> <dl> <dt>

4330 (0x10EA)
</dt> <dt>



Impossibile estrarre il supporto perché si trova in un'unità.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**SET di slot per la pulizia degli errori \_ \_ \_**
</dt> <dd> <dl> <dt>

4331 (0x10EB)
</dt> <dt>



Uno slot di pulitura è già riservato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**lo slot per la pulizia degli errori \_ \_ non è \_ \_ impostato**
</dt> <dd> <dl> <dt>

4332 (0x10EC)
</dt> <dt>



Uno slot di pulitura non è riservato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**\_pulitura della \_ cartuccia di \_ errore**
</dt> <dd> <dl> <dt>

4333 (0x10ED)
</dt> <dt>



La cartuccia Cleaner ha eseguito il numero massimo di operazioni di pulizia delle unità.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**errore di un errore \_ imprevisto. \_**
</dt> <dd> <dl> <dt>

4334 (0x10EE)
</dt> <dt>



Identificatore medio imprevisto.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**errore \_ durante \_ l'eliminazione dell' \_ ultimo \_ elemento**
</dt> <dd> <dl> <dt>

4335 (0x10EF)
</dt> <dt>



L'ultimo elemento rimanente in questo gruppo o risorsa non può essere eliminato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**il \_ messaggio di errore \_ supera le \_ dimensioni massime \_**
</dt> <dd> <dl> <dt>

4336 (0x10F0)
</dt> <dt>



Il messaggio specificato supera la dimensione massima consentita per questo parametro.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**il \_ volume degli errori \_ contiene \_ \_ i file sys**
</dt> <dd> <dl> <dt>

4337 (0x10F1)
</dt> <dt>



Il volume contiene file di sistema o di paging.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**tipo di errore \_ nativo \_**
</dt> <dd> <dl> <dt>

4338 (0x10F2)
</dt> <dt>



Non è possibile rimuovere il tipo di supporto da questa libreria perché almeno un'unità nella libreria segnala che è in grado di supportare questo tipo di supporto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**ERRORE \_ senza \_ unità di supporto \_**
</dt> <dd> <dl> <dt>

4339 (0x10F3)
</dt> <dt>



Non è possibile montare questo supporto offline sul sistema perché non sono presenti unità abilitate che possono essere usate.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**\_cartuccia di pulitura errori \_ \_ installata**
</dt> <dd> <dl> <dt>

4340 (0x10F4)
</dt> <dt>



Nella libreria di nastri è presente una cartuccia di pulitura.


</dt> </dl> </dd> <dt>

<span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**ERRORE \_ inserimento/espulsione \_ completo**
</dt> <dd> <dl> <dt>

4341 (0x10F5)
</dt> <dt>



Impossibile utilizzare la porta di inserimento/espulsione perché non è vuota.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**FILE degli errori \_ \_ offline**
</dt> <dd> <dl> <dt>

4350 (0x10FE)
</dt> <dt>



Il file non è attualmente disponibile per l'utilizzo in questo computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**ERRORE \_ di \_ archiviazione remota \_ non \_ attivo**
</dt> <dd> <dl> <dt>

4351 (0x10FF)
</dt> <dt>



Il servizio di archiviazione remoto non è operativo in questo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**errore \_ del \_ supporto di archiviazione remota \_ errore \_**
</dt> <dd> <dl> <dt>

4352 (0x1100)
</dt> <dt>



Il servizio di archiviazione remota ha rilevato un errore del supporto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**ERRORE \_ non è \_ un punto di \_ analisi \_**
</dt> <dd> <dl> <dt>

4390 (0x1126)
</dt> <dt>



Il file o la directory non è un punto di analisi.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**ERRORE di \_ RIanalisi dell' \_ attributo \_**
</dt> <dd> <dl> <dt>

4391 (0x1127)
</dt> <dt>



Non è possibile impostare l'attributo reparse point perché è in conflitto con un attributo esistente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**ERRORE \_ di \_ analisi \_ dei dati non validi**
</dt> <dd> <dl> <dt>

4392 (0x1128)
</dt> <dt>



I dati presenti nel buffer del reparse point non sono validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**ERRORE di \_ reparse \_ tag \_ non valido**
</dt> <dd> <dl> <dt>

4393 (0x1129)
</dt> <dt>



Il tag presente nel buffer del reparse point non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**ERRORE di \_ reparse \_ tag non \_ corrispondente**
</dt> <dd> <dl> <dt>

4394 (0x112A)
</dt> <dt>



Mancata corrispondenza tra il tag specificato nella richiesta e il tag presente nel reparse point.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**ERRORE \_ \_ dati app \_ non \_ trovati**
</dt> <dd> <dl> <dt>

4400 (0x1130)
</dt> <dt>



Dati della cache veloce non trovati.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**ERRORE \_ \_ dati app \_ scaduti**
</dt> <dd> <dl> <dt>

4401 (0x1131)
</dt> <dt>



I dati della cache veloce sono scaduti.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**ERRORE \_ \_ dati app \_ danneggiati**
</dt> <dd> <dl> <dt>

4402 (0x1132)
</dt> <dt>



Dati della cache veloce danneggiati.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**ERRORE \_ \_ limite dati \_ app \_ superato**
</dt> <dd> <dl> <dt>

4403 (0x1133)
</dt> <dt>



I dati della cache veloce hanno superato le dimensioni massime e non possono essere aggiornati.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**ERRORE \_ è \_ \_ necessario riavviare i dati dell'app \_**
</dt> <dd> <dl> <dt>

4404 (0x1134)
</dt> <dt>



La cache veloce è stata riarmata e richiede un riavvio fino a quando non può essere aggiornata.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**ERRORE \_ \_ rilevato rollback \_ SECUREBOOT**
</dt> <dd> <dl> <dt>

4420 (0x1144)
</dt> <dt>



L'avvio protetto ha rilevato un tentativo di rollback dei dati protetti.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**ERRORE \_ di \_ violazione dei criteri di SECUREBOOT \_**
</dt> <dd> <dl> <dt>

4421 (0x1145)
</dt> <dt>



Il valore è protetto da criteri di avvio protetto e non può essere modificato o eliminato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**ERRORE \_ SECUREBOOT \_ criterio non valido \_**
</dt> <dd> <dl> <dt>

4422 (0x1146)
</dt> <dt>



Il criterio di avvio protetto non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**ERRORE \_ SECUREBOOT di \_ pubblicazione del criterio \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

4423 (0x1147)
</dt> <dt>



Un nuovo criterio di avvio protetto non contiene il server di pubblicazione corrente nell'elenco di aggiornamenti.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**ERRORE \_ SECUREBOOT \_ criterio \_ non \_ firmato**
</dt> <dd> <dl> <dt>

4424 (0x1148)
</dt> <dt>



I criteri di avvio protetto non sono firmati o sono firmati da un firmatario non attendibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**ERRORE \_ SECUREBOOT \_ non \_ abilitato**
</dt> <dd> <dl> <dt>

4425 (0x1149)
</dt> <dt>



L'avvio protetto non è abilitato in questo computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**ERRORE \_ SECUREBOOT \_ file \_ sostituito**
</dt> <dd> <dl> <dt>

4426 (0x114A)
</dt> <dt>



Per l'avvio protetto è necessario che determinati file e driver non vengano sostituiti da altri file o driver.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**ERRORE di \_ OFFLOAD \_ Read \_ flt \_ non \_ supportato**
</dt> <dd> <dl> <dt>

4440 (0x1158)
</dt> <dt>



L'operazione di lettura dell'offload di copia non è supportata da un filtro.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**ERRORE di \_ OFFLOAD \_ scrittura \_ flt \_ non \_ supportato**
</dt> <dd> <dl> <dt>

4441 (0x1159)
</dt> <dt>



L'operazione di scrittura dell'offload di copia non è supportata da un filtro.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**ERRORE di \_ OFFLOAD \_ file di lettura \_ \_ non \_ supportato**
</dt> <dd> <dl> <dt>

4442 (0x115A)
</dt> <dt>



L'operazione di lettura dell'offload di copia non è supportata per il file.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**errore durante l' \_ OFFLOAD del \_ file di scrittura \_ \_ non \_ supportato**
</dt> <dd> <dl> <dt>

4443 (0x115B)
</dt> <dt>



L'operazione di scrittura dell'offload di copia non è supportata per il file.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**VOLUME di errore \_ \_ non \_ abilitato per SIS \_**
</dt> <dd> <dl> <dt>

4500 (0x1194)
</dt> <dt>



L'archiviazione a istanza singola non è disponibile in questo volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**\_risorsa dipendente dall'errore \_ \_ esistente**
</dt> <dd> <dl> <dt>

5001 (0X1389)
</dt> <dt>



Non è possibile completare l'operazione perché altre risorse dipendono da questa risorsa.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**\_dipendenza errore \_ non \_ trovata**
</dt> <dd> <dl> <dt>

5002 (0x138A)
</dt> <dt>



Impossibile trovare la dipendenza della risorsa cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**dipendenza di errore \_ \_ già \_ esistente**
</dt> <dd> <dl> <dt>

5003 (0x138B)
</dt> <dt>



La risorsa cluster non può essere resa dipendente dalla risorsa specificata perché è già dipendente.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**\_risorsa errore \_ non in \_ linea**
</dt> <dd> <dl> <dt>

5004 (0x138C)
</dt> <dt>



La risorsa cluster non è online.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**\_nodo host di errore \_ \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

5005 (0x138D)
</dt> <dt>



Un nodo del cluster non è disponibile per questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**\_risorsa errore \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

5006 (0x138E)
</dt> <dt>



La risorsa cluster non è disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**\_risorsa errore \_ non \_ trovata**
</dt> <dd> <dl> <dt>

5007 (0x138F)
</dt> <dt>



Impossibile trovare la risorsa cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**ERRORE di \_ arresto del \_ cluster**
</dt> <dd> <dl> <dt>

5008 (0x1390)
</dt> <dt>



È in corso l'arresto del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**errore durante la \_ \_ rimozione del \_ \_ nodo attivo**
</dt> <dd> <dl> <dt>

5009 (0x1391)
</dt> <dt>



Un nodo del cluster non può essere rimosso dal cluster, a meno che il nodo non sia attivo o sia l'ultimo nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**l' \_ oggetto \_ Error \_ esiste già**
</dt> <dd> <dl> <dt>

5010 (0x1392)
</dt> <dt>



L'oggetto esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**\_oggetto Error \_ nell' \_ elenco**
</dt> <dd> <dl> <dt>

5011 (0x1393)
</dt> <dt>



L'oggetto è già presente nell'elenco.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**\_gruppo errori \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

5012 (0x1394)
</dt> <dt>



Il gruppo cluster non è disponibile per le nuove richieste.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**\_ \_ Impossibile trovare il gruppo di errori \_**
</dt> <dd> <dl> <dt>

5013 (0x1395)
</dt> <dt>



Impossibile trovare il gruppo cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**\_gruppo errori \_ non in \_ linea**
</dt> <dd> <dl> <dt>

5014 (0x1396)
</dt> <dt>



Non è stato possibile completare l'operazione perché il gruppo cluster non è online.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**\_nodo host \_ errore \_ non \_ \_ proprietario risorsa**
</dt> <dd> <dl> <dt>

5015 (0x1397)
</dt> <dt>



L'operazione non è riuscita perché il nodo del cluster specificato non è il proprietario della risorsa o il nodo non è un possibile proprietario della risorsa.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**ERRORE \_ del \_ nodo \_ host \_ non \_ proprietario del gruppo**
</dt> <dd> <dl> <dt>

5016 (0x1398)
</dt> <dt>



Operazione non riuscita. Il gruppo non è di proprietà del nodo di cluster specificato o il nodo non è un possibile proprietario del gruppo.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**ERRORE \_ di \_ creazione resmon \_ non riuscita**
</dt> <dd> <dl> <dt>

5017 (0x1399)
</dt> <dt>



Impossibile creare la risorsa cluster nel monitoraggio risorse specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**ERRORE \_ resmon \_ online \_ non riuscito**
</dt> <dd> <dl> <dt>

5018 (0x139A)
</dt> <dt>



Impossibile portare in linea la risorsa cluster dal monitoraggio risorse.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**\_risorsa errore \_ online**
</dt> <dd> <dl> <dt>

5019 (0x139B)
</dt> <dt>



Non è stato possibile completare l'operazione perché la risorsa cluster è online.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**ERRORE \_ di \_ risorsa quorum**
</dt> <dd> <dl> <dt>

5020 (0x139C)
</dt> <dt>



Non è stato possibile eliminare o portare offline la risorsa cluster perché è la risorsa quorum.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**ERRORE \_ non \_ idoneo per il quorum \_**
</dt> <dd> <dl> <dt>

5021 (0x139D)
</dt> <dt>



Il cluster non è riuscito a rendere la risorsa specificata una risorsa quorum perché non è in grado di essere una risorsa quorum.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**ERRORE \_ di \_ arresto del \_ cluster**
</dt> <dd> <dl> <dt>

5022 (0x139E)
</dt> <dt>



È in corso l'arresto del software del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**ERRORE \_ di \_ stato non valido**
</dt> <dd> <dl> <dt>

5023 (0x139F)
</dt> <dt>



Il gruppo o la risorsa non si trova nello stato corretto per eseguire l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**\_proprietà delle risorse di errore \_ \_ archiviate**
</dt> <dd> <dl> <dt>

5024 (0x13A0)
</dt> <dt>



Le proprietà sono state archiviate, ma non tutte le modifiche saranno effettive fino alla successiva porta online della risorsa.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**ERRORE \_ di \_ classe del quorum \_**
</dt> <dd> <dl> <dt>

5025 (0x13A1)
</dt> <dt>



Il cluster non è riuscito a rendere la risorsa specificata una risorsa quorum perché non appartiene a una classe di archiviazione condivisa.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**\_risorsa principale \_ errore**
</dt> <dd> <dl> <dt>

5026 (0x13A2)
</dt> <dt>



Non è stato possibile eliminare la risorsa cluster perché è una risorsa principale.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**ERRORE \_ di \_ risorsa quorum \_ online \_ non riuscito**
</dt> <dd> <dl> <dt>

5027 (0x13A3)
</dt> <dt>



La risorsa quorum non è riuscita a tornare in linea.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**ERRORE \_ QUORUMLOG \_ apertura \_ non riuscita**
</dt> <dd> <dl> <dt>

5028 (0x13A4)
</dt> <dt>



Impossibile creare o montare correttamente il registro quorum.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**ERRORE \_ CLUSTERLOG \_ danneggiato**
</dt> <dd> <dl> <dt>

5029 (0x13A5)
</dt> <dt>



Il log del cluster è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**ERRORE \_ \_ record CLUSTERLOG \_ superiore a \_ MaxSize**
</dt> <dd> <dl> <dt>

5030 (0x13A6)
</dt> <dt>



Impossibile scrivere il record nel log del cluster perché supera le dimensioni massime.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**ERRORE \_ CLUSTERLOG \_ superiore a \_ MaxSize**
</dt> <dd> <dl> <dt>

5031 (0x13A7)
</dt> <dt>



Il log del cluster supera le dimensioni massime.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**ERRORE \_ CLUSTERLOG \_ CHKPOINT \_ non \_ trovato**
</dt> <dd> <dl> <dt>

5032 (0x13A8)
</dt> <dt>



Nessun record del checkpoint trovato nel log del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**ERRORE \_ CLUSTERLOG \_ \_ spazio insufficiente \_**
</dt> <dd> <dl> <dt>

5033 (0x13A9)
</dt> <dt>



Lo spazio su disco minimo necessario per la registrazione non è disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**ERRORE \_ \_ proprietario quorum \_ attivo**
</dt> <dd> <dl> <dt>

5034 (0x13AA)
</dt> <dt>



Il nodo del cluster non è riuscito a assumere il controllo della risorsa quorum perché la risorsa è di proprietà di un altro nodo attivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**ERRORE di \_ rete \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

5035 (0x13AB)
</dt> <dt>



Una rete cluster non è disponibile per questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**\_nodo errore \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

5036 (0x13AC)
</dt> <dt>



Un nodo del cluster non è disponibile per questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**ERRORE \_ tutti i \_ nodi \_ non \_ disponibili**
</dt> <dd> <dl> <dt>

5037 (0x13AD)
</dt> <dt>



Per eseguire questa operazione, è necessario che tutti i nodi del cluster siano in esecuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**ERRORE di \_ risorsa \_ non riuscita**
</dt> <dd> <dl> <dt>

5038 (0x13AE)
</dt> <dt>



Errore di una risorsa cluster


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**nodo del cluster di errore \_ \_ non valido \_**
</dt> <dd> <dl> <dt>

5039 (0x13AF)
</dt> <dt>



Il nodo del cluster non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**nodo del cluster di errore \_ \_ \_ esistente**
</dt> <dd> <dl> <dt>

5040 (0x13B0)
</dt> <dt>



Il nodo del cluster esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**ERRORE \_ \_ di join \_ del cluster in \_ corso**
</dt> <dd> <dl> <dt>

5041 (0x13B1)
</dt> <dt>



Un nodo è in corso di aggiunta al cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**nodo del cluster di errore \_ \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

5042 (0x13B2)
</dt> <dt>



Impossibile trovare il nodo del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**\_ \_ nodo locale del cluster di errore \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

5043 (0x13B3)
</dt> <dt>



Impossibile trovare le informazioni sul nodo locale del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**ERRORE \_ \_ rete cluster \_ esistente**
</dt> <dd> <dl> <dt>

5044 (0x13B4)
</dt> <dt>



La rete cluster esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**ERRORE \_ di \_ rete cluster \_ non \_ trovato**
</dt> <dd> <dl> <dt>

5045 (0x13B5)
</dt> <dt>



Impossibile trovare la rete cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**ERRORE del \_ cluster \_ NETINTERFACE \_ esistente**
</dt> <dd> <dl> <dt>

5046 (0x13B6)
</dt> <dt>



L'interfaccia di rete del cluster esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**ERRORE \_ cluster \_ NETINTERFACE \_ non \_ trovato**
</dt> <dd> <dl> <dt>

5047 (0x13B7)
</dt> <dt>



Impossibile trovare l'interfaccia di rete cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**\_ \_ richiesta non valida del cluster di errori \_**
</dt> <dd> <dl> <dt>

5048 (0x13B8)
</dt> <dt>



La richiesta del cluster non è valida per questo oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**ERRORE \_ cluster \_ \_ provider di rete non valido \_**
</dt> <dd> <dl> <dt>

5049 (0x13B9)
</dt> <dt>



Il provider di rete cluster non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**nodo del cluster di errore \_ \_ \_ inattivo**
</dt> <dd> <dl> <dt>

5050 (0x13BA)
</dt> <dt>



Il nodo del cluster è inattivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**ERRORE del \_ nodo del cluster non \_ \_ raggiungibile**
</dt> <dd> <dl> <dt>

5051 (0x13BB)
</dt> <dt>



Il nodo del cluster non è raggiungibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**nodo del cluster di errore \_ \_ \_ non \_ membro**
</dt> <dd> <dl> <dt>

5052 (0x13BC)
</dt> <dt>



Il nodo del cluster non è un membro del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**ERRORE \_ \_ di join \_ del cluster non \_ in \_ corso**
</dt> <dd> <dl> <dt>

5053 (0x13BD)
</dt> <dt>



Un'operazione di join del cluster non è in corso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**ERRORE \_ cluster \_ rete non valida \_**
</dt> <dd> <dl> <dt>

5054 (0x13BE)
</dt> <dt>



Rete cluster non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**nodo del cluster di errore \_ \_ \_ attivo**
</dt> <dd> <dl> <dt>

5056 (0x13C0)
</dt> <dt>



Il nodo del cluster è attivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**ERRORE \_ \_ del cluster IPADDR \_ in \_ uso**
</dt> <dd> <dl> <dt>

5057 (0x13C1)
</dt> <dt>



L'indirizzo IP del cluster è già in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**nodo del cluster di errore \_ \_ \_ non \_ sospeso**
</dt> <dd> <dl> <dt>

5058 (0x13C2)
</dt> <dt>



Il nodo del cluster non è sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**ERRORE \_ nel \_ cluster \_ senza \_ contesto di sicurezza**
</dt> <dd> <dl> <dt>

5059 (0x13C3)
</dt> <dt>



Non è disponibile alcun contesto di sicurezza del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**ERRORE \_ di \_ rete del cluster \_ non \_ interno**
</dt> <dd> <dl> <dt>

5060 (0x13C4)
</dt> <dt>



La rete cluster non è configurata per la comunicazione interna del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**nodo del cluster di errore \_ \_ \_ già \_ attivo**
</dt> <dd> <dl> <dt>

5061 (0x13C5)
</dt> <dt>



Il nodo del cluster è già attivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**nodo del cluster di errore \_ \_ \_ già \_ attivo**
</dt> <dd> <dl> <dt>

5062 (0x13C6)
</dt> <dt>



Il nodo del cluster è già inattivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**\_rete cluster di errore \_ \_ già \_ online**
</dt> <dd> <dl> <dt>

5063 (0x13C7)
</dt> <dt>



La rete cluster è già online.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**\_rete cluster di errore \_ \_ già \_ offline**
</dt> <dd> <dl> <dt>

5064 (0x13C8)
</dt> <dt>



La rete cluster è già offline.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**nodo del cluster di errore \_ \_ \_ già \_ membro**
</dt> <dd> <dl> <dt>

5065 (0x13C9)
</dt> <dt>



Il nodo del cluster è già membro del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**\_ \_ Ultima \_ rete interna cluster \_ errori**
</dt> <dd> <dl> <dt>

5066 (0x13CA)
</dt> <dt>



La rete cluster è l'unico configurato per la comunicazione interna del cluster tra due o più nodi del cluster attivi. Impossibile rimuovere dalla rete la funzionalità di comunicazione interna.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**ERRORE \_ della \_ rete cluster \_ con \_ dipendenti**
</dt> <dd> <dl> <dt>

5067 (0x13CB)
</dt> <dt>



Una o più risorse cluster dipendono dalla rete per fornire il servizio ai client. Non è possibile rimuovere la funzionalità di accesso client dalla rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**ERRORE \_ operazione non valida \_ \_ sul \_ quorum**
</dt> <dd> <dl> <dt>

5068 (0x13CC)
</dt> <dt>



Questa operazione non può essere eseguita sulla risorsa cluster come risorsa quorum. Non è possibile portare offline la risorsa quorum o modificare il relativo elenco di proprietari.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**\_dipendenza errore \_ non \_ consentita**
</dt> <dd> <dl> <dt>

5069 (0x13CD)
</dt> <dt>



La risorsa quorum del cluster non può avere alcuna dipendenza.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**nodo del cluster di errore \_ \_ \_ sospeso**
</dt> <dd> <dl> <dt>

5070 (0x13CE)
</dt> <dt>



Il nodo del cluster è sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**\_ \_ \_ risorsa host cant del nodo errore \_**
</dt> <dd> <dl> <dt>

5071 (0x13CF)
</dt> <dt>



Impossibile portare in linea la risorsa cluster. Il nodo proprietario non è in grado di eseguire questa risorsa.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**nodo del cluster di errore \_ \_ \_ non \_ pronto**
</dt> <dd> <dl> <dt>

5072 (0x13D0)
</dt> <dt>



Il nodo del cluster non è pronto per eseguire l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**ERRORE \_ di \_ arresto del nodo cluster \_ \_**
</dt> <dd> <dl> <dt>

5073 (0x13D1)
</dt> <dt>



È in corso l'arresto del nodo del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**ERRORE \_ di \_ join del cluster \_ interrotto**
</dt> <dd> <dl> <dt>

5074 (0x13D2)
</dt> <dt>



L'operazione di join del cluster è stata interrotta.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**\_ \_ versioni incompatibili del cluster di errori \_**
</dt> <dd> <dl> <dt>

5075 (0x13D3)
</dt> <dt>



L'operazione di join del cluster non è riuscita a causa di versioni software incompatibili tra il nodo di join e il relativo sponsor.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**\_ \_ MAXNUM del cluster \_ di errore delle \_ risorse \_ superato**
</dt> <dd> <dl> <dt>

5076 (0x13D4)
</dt> <dt>



Non è possibile creare questa risorsa perché il cluster ha raggiunto il limite al numero di risorse che può monitorare.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**ERRORE \_ di \_ configurazione del sistema cluster \_ \_ modificato**
</dt> <dd> <dl> <dt>

5077 (0x13D5)
</dt> <dt>



La configurazione di sistema è stata modificata durante l'operazione di join o modulo del cluster. L'operazione di join o modulo è stata interrotta.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**\_ \_ \_ \_ Impossibile trovare il tipo di risorsa cluster di errore \_**
</dt> <dd> <dl> <dt>

5078 (0x13D6)
</dt> <dt>



Il tipo di risorsa specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**ERRORE del \_ cluster \_ restype \_ non \_ supportato**
</dt> <dd> <dl> <dt>

5079 (0x13D7)
</dt> <dt>



Il nodo specificato non supporta una risorsa di questo tipo. Ciò può essere dovuto a incoerenze di versione o a causa dell'assenza della DLL di risorse in questo nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**ERRORE \_ cluster \_ RESNAME \_ non \_ trovato**
</dt> <dd> <dl> <dt>

5080 (0x13D8)
</dt> <dt>



Il nome di risorsa specificato non è supportato da questa DLL di risorse. Questo potrebbe essere dovuto a un nome non valido (o modificato) fornito alla DLL della risorsa.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**ERRORE \_ del \_ cluster \_ nessun \_ pacchetto RPC \_ registrato**
</dt> <dd> <dl> <dt>

5081 (0x13D9)
</dt> <dt>



Non è stato possibile registrare alcun pacchetto di autenticazione con il server RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**ERRORE \_ \_ del proprietario \_ del cluster non \_ in \_ PREFLIST**
</dt> <dd> <dl> <dt>

5082 (0x13DA)
</dt> <dt>



Non è possibile portare il gruppo online perché il proprietario del gruppo non è presente nell'elenco preferito per il gruppo. Per modificare il nodo proprietario per il gruppo, spostare il gruppo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**ERRORE \_ del \_ database cluster \_ SEQMISMATCH**
</dt> <dd> <dl> <dt>

5083 (0x13DB)
</dt> <dt>



L'operazione di join non è riuscita perché il numero di sequenza del database cluster è stato modificato o non è compatibile con il nodo del blocco. Questo problema può verificarsi durante un'operazione di join se il database del cluster è stato modificato durante il join.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**ERRORE \_ resmon \_ stato non valido \_**
</dt> <dd> <dl> <dt>

5084 (0x13DC)
</dt> <dt>



Il monitoraggio risorse non consentirà l'esecuzione dell'operazione di errore mentre la risorsa si trova nello stato corrente. Questo problema può verificarsi se la risorsa è in uno stato in sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**ERRORE \_ di \_ \_ blocco del \_ cluster**
</dt> <dd> <dl> <dt>

5085 (0x13DD)
</dt> <dt>



Un codice non di blocco ha ricevuto una richiesta di riservare il blocco per la creazione di aggiornamenti globali.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**\_disco quorum \_ errore \_ non \_ trovato**
</dt> <dd> <dl> <dt>

5086 (0x13DE)
</dt> <dt>



Il disco quorum non è stato trovato dal servizio cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**BACKUP del database di errore \_ \_ \_ danneggiato**
</dt> <dd> <dl> <dt>

5087 (0x13DF)
</dt> <dt>



È possibile che il database del cluster di cui è stato eseguito il backup sia danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**il \_ nodo del cluster di errore \_ dispone già di una \_ \_ \_ \_ radice DFS**
</dt> <dd> <dl> <dt>

5088 (0x13E0)
</dt> <dt>



Una radice DFS esiste già nel nodo del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**Proprietà della risorsa di errore non \_ \_ \_ modificabile**
</dt> <dd> <dl> <dt>

5089 (0x13E1)
</dt> <dt>



Il tentativo di modificare una proprietà della risorsa non è riuscito perché è in conflitto con un'altra proprietà esistente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**ERRORE \_ appartenenza cluster a \_ \_ stato non valido \_**
</dt> <dd> <dl> <dt>

5890 (0x1702)
</dt> <dt>



Si è tentato di eseguire un'operazione incompatibile con lo stato di appartenenza corrente del nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**ERRORE \_ cluster \_ QUORUMLOG \_ non \_ trovato**
</dt> <dd> <dl> <dt>

5891 (0x1703)
</dt> <dt>



La risorsa quorum non contiene il registro quorum.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**\_ \_ interruzione appartenenza cluster di errore \_**
</dt> <dd> <dl> <dt>

5892 (0x1704)
</dt> <dt>



Il motore di appartenenza ha richiesto l'arresto del servizio cluster in questo nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**\_ID istanza cluster di errore non \_ \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

5893 (0x1705)
</dt> <dt>



L'operazione di join non è riuscita perché l'ID istanza del cluster del nodo di join non corrisponde all'ID istanza del cluster del nodo sponsor.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**ERRORE \_ \_ di rete cluster \_ non \_ trovato per l' \_ \_ indirizzo IP**
</dt> <dd> <dl> <dt>

5894 (0x1706)
</dt> <dt>



Impossibile trovare una rete cluster corrispondente per l'indirizzo IP specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**ERRORE \_ del \_ tipo di dati della proprietà cluster non \_ \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

5895 (0x1707)
</dt> <dt>



Il tipo di dati effettivo della proprietà non corrisponde al tipo di dati previsto della proprietà.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**ERRORE \_ di \_ rimozione del cluster \_ senza \_ pulizia**
</dt> <dd> <dl> <dt>

5896 (0x1708)
</dt> <dt>



Il nodo del cluster è stato rimosso dal cluster, ma il nodo non è stato eliminato. Per determinare i passaggi di pulizia non riusciti e come eseguire il ripristino, vedere il registro eventi dell'applicazione clustering di failover con Visualizzatore eventi.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**ERRORE \_ parametro cluster non \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

5897 (0x1709)
</dt> <dt>



Due o più valori di parametro specificati per le proprietà di una risorsa sono in conflitto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**\_ \_ Impossibile \_ \_ RAGGRUPPAre il nodo errore**
</dt> <dd> <dl> <dt>

5898 (0x170A)
</dt> <dt>



Questo computer non può essere membro di un cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**ERRORE \_ del \_ cluster \_ versione del sistema operativo \_**
</dt> <dd> <dl> <dt>

5899 (0x170B)
</dt> <dt>



Il computer non può essere membro di un cluster perché non è installata la versione corretta di Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**\_ \_ Impossibile creare il \_ \_ \_ nome cluster DUPLICAto \_ del cluster di errori**
</dt> <dd> <dl> <dt>

5900 (0x170C)
</dt> <dt>



Non è possibile creare un cluster con il nome del cluster specificato perché il nome del cluster è già in uso. Specificare un nome diverso per il cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**ERRORE \_ CLUSCFG \_ già \_ eseguito**
</dt> <dd> <dl> <dt>

5901 (0x170D)
</dt> <dt>



È già stato eseguito il commit dell'azione di configurazione del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**ERRORE \_ \_ rollback CLUSCFG \_ non riuscito**
</dt> <dd> <dl> <dt>

5902 (0x170E)
</dt> <dt>



Non è stato possibile eseguire il rollback dell'azione di configurazione del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**ERRORE \_ nella \_ \_ lettera di \_ unità \_ disco \_ di sistema CLUSCFG**
</dt> <dd> <dl> <dt>

5903 (0x170F)
</dt> <dt>



La lettera di unità assegnata a un disco di sistema in un nodo è in conflitto con la lettera di unità assegnata a un disco in un altro nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**ERRORE \_ nella \_ versione precedente del cluster \_**
</dt> <dd> <dl> <dt>

5904 (0x1710)
</dt> <dt>



Uno o più nodi del cluster eseguono una versione di Windows che non supporta questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**ERRORE del cluster per il \_ \_ \_ \_ nome acct del computer non corrispondente \_**
</dt> <dd> <dl> <dt>

5905 (0x1711)
</dt> <dt>



Il nome dell'account computer corrispondente non corrisponde al nome di rete per la risorsa.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**ERRORE \_ cluster \_ nessun \_ \_ Adapter NET**
</dt> <dd> <dl> <dt>

5906 (0x1712)
</dt> <dt>



Non sono disponibili schede di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**ERRORE \_ cluster non \_ elaborabile**
</dt> <dd> <dl> <dt>

5907 (0x1713)
</dt> <dt>



Il nodo del cluster è stato danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**errore durante lo stato del \_ \_ gruppo cluster \_**
</dt> <dd> <dl> <dt>

5908 (0x1714)
</dt> <dt>



Il gruppo non è in grado di accettare la richiesta perché sta per essere spostato in un altro nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**\_tipo di risorsa cluster di errore \_ \_ \_ occupato**
</dt> <dd> <dl> <dt>

5909 (0x1715)
</dt> <dt>



Il tipo di risorsa non può accettare la richiesta perché è troppo occupato a eseguire un'altra operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**\_timeout della \_ chiamata alla risorsa \_ di errore \_**
</dt> <dd> <dl> <dt>

5910 (0x1716)
</dt> <dt>



Timeout della chiamata alla DLL della risorsa cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**ERRORE \_ di \_ \_ indirizzo IPv6 del cluster non valido \_**
</dt> <dd> <dl> <dt>

5911 (0x1717)
</dt> <dt>



Indirizzo non valido per una risorsa indirizzo IPv6. Un indirizzo IPv6 globale è obbligatorio e deve corrispondere a una rete di cluster. Gli indirizzi di compatibilità non sono consentiti.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**\_funzione interna del cluster di errore \_ \_ non valida \_**
</dt> <dd> <dl> <dt>

5912 (0x1718)
</dt> <dt>



Si è verificato un errore interno del cluster. È stata tentata una chiamata a una funzione non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**\_ \_ parametro del cluster \_ di errore fuori \_ \_ limite**
</dt> <dd> <dl> <dt>

5913 (0x1719)
</dt> <dt>



Il valore di un parametro non è compreso nell'intervallo accettabile.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**ERRORE \_ di \_ invio parziale del cluster \_**
</dt> <dd> <dl> <dt>

5914 (0x171A)
</dt> <dt>



Si è verificato un errore di rete durante l'invio dei dati a un altro nodo del cluster. Il numero di byte trasmessi è inferiore al necessario.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**ERRORE \_ registro cluster- \_ \_ funzione non valida \_**
</dt> <dd> <dl> <dt>

5915 (0x171B)
</dt> <dt>



È stata tentata un'operazione del registro cluster non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**\_ \_ interruzione stringa non valida del cluster di errori \_ \_**
</dt> <dd> <dl> <dt>

5916 (0x171C)
</dt> <dt>



Una stringa di input di caratteri non è terminata correttamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**ERRORE del \_ cluster in \_ \_ formato stringa non valido \_**
</dt> <dd> <dl> <dt>

5917 (0x171D)
</dt> <dt>



Una stringa di input di caratteri non è in un formato valido per i dati rappresentati.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**ERRORE \_ \_ \_ di transazione database cluster \_ in \_ corso**
</dt> <dd> <dl> <dt>

5918 (0x171E)
</dt> <dt>



Si è verificato un errore interno del cluster. È stata tentata una transazione del database cluster mentre era già in corso una transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**ERRORE \_ \_ \_ di transazione database cluster \_ non \_ in \_ corso**
</dt> <dd> <dl> <dt>

5919 (0x171F)
</dt> <dt>



Si è verificato un errore interno del cluster. Si è verificato un tentativo di eseguire il commit di una transazione del database cluster mentre non è in corso alcuna transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**ERRORI \_ \_ dei dati null del cluster \_**
</dt> <dd> <dl> <dt>

5920 (0x1720)
</dt> <dt>



Si è verificato un errore interno del cluster. I dati non sono stati inizializzati correttamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**ERRORE \_ di \_ lettura parziale del cluster \_**
</dt> <dd> <dl> <dt>

5921 (0x1721)
</dt> <dt>



Si è verificato un errore durante la lettura da un flusso di dati. È stato restituito un numero imprevisto di byte.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**ERRORE \_ di \_ scrittura parziale del cluster \_**
</dt> <dd> <dl> <dt>

5922 (0x1722)
</dt> <dt>



Si è verificato un errore durante la scrittura in un flusso di dati. Impossibile scrivere il numero di byte richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**ERRORE del \_ cluster di \_ \_ deserializzazione \_ dei dati**
</dt> <dd> <dl> <dt>

5923 (0x1723)
</dt> <dt>



Si è verificato un errore durante la deserializzazione di un flusso di dati del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**\_ \_ \_ conflitto proprietà risorse dipendente dall'errore \_**
</dt> <dd> <dl> <dt>

5924 (0x1724)
</dt> <dt>



Uno o più valori di proprietà per questa risorsa sono in conflitto con uno o più valori di proprietà associati alle risorse dipendenti.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**ERRORE del \_ cluster \_ senza \_ quorum**
</dt> <dd> <dl> <dt>

5925 (0x1725)
</dt> <dt>



Un quorum di nodi del cluster non è presente per formare un cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**ERRORE \_ cluster \_ \_ rete IPv6 non valida \_**
</dt> <dd> <dl> <dt>

5926 (0x1726)
</dt> <dt>



La rete cluster non è valida per una risorsa indirizzo IPv6 o non corrisponde all'indirizzo configurato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**ERRORE \_ cluster \_ \_ \_ rete tunnel IPv6 non valida \_**
</dt> <dd> <dl> <dt>

5927 (0x1727)
</dt> <dt>



La rete cluster non è valida per una risorsa tunnel IPv6. Controllare la configurazione della risorsa indirizzo IP da cui dipende la risorsa tunnel IPv6.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**\_il quorum degli errori \_ non è \_ consentito \_ in \_ questo \_ gruppo**
</dt> <dd> <dl> <dt>

5928 (0x1728)
</dt> <dt>



La risorsa quorum non può trovarsi nel gruppo di archiviazione disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**\_albero delle dipendenze di errore \_ \_ troppo \_ complesso**
</dt> <dd> <dl> <dt>

5929 (0x1729)
</dt> <dt>



Le dipendenze per questa risorsa sono troppo profondamente nidificate.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**\_eccezione \_ di errore \_ nella \_ chiamata di risorsa**
</dt> <dd> <dl> <dt>

5930 (0x172A)
</dt> <dt>



La chiamata nella DLL della risorsa ha generato un'eccezione non gestita.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**\_inizializzazione del cluster di errore \_ RHS \_ non riuscita \_**
</dt> <dd> <dl> <dt>

5931 (0x172B)
</dt> <dt>



Impossibile inizializzare il processo RHS.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**ERRORE del \_ cluster \_ non \_ installato**
</dt> <dd> <dl> <dt>

5932 (0x172C)
</dt> <dt>



La funzionalità clustering di failover non è installata in questo nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**le \_ \_ risorse cluster \_ di errore devono \_ essere \_ online nello \_ \_ \_ stesso \_ nodo**
</dt> <dd> <dl> <dt>

5933 (0x172D)
</dt> <dt>



Le risorse devono essere online nello stesso nodo per questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**\_ \_ numero massimo \_ di nodi \_ del cluster di errore nel \_ cluster**
</dt> <dd> <dl> <dt>

5934 (0x172E)
</dt> <dt>



Non è possibile aggiungere un nuovo nodo perché questo cluster è già al numero massimo di nodi.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**ERRORE del \_ cluster di \_ troppi \_ \_ nodi**
</dt> <dd> <dl> <dt>

5935 (0x172F)
</dt> <dt>



Non è possibile creare il cluster perché il numero di nodi specificato supera il limite massimo consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**\_oggetto cluster di errore \_ già in \_ \_ uso**
</dt> <dd> <dl> <dt>

5936 (0x1730)
</dt> <dt>



Il tentativo di utilizzare il nome del cluster specificato non è riuscito perché nel dominio esiste già un oggetto computer abilitato con il nome specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**ERRORE di \_ gruppi non core \_ \_ trovati**
</dt> <dd> <dl> <dt>

5937 (0x1731)
</dt> <dt>



Questo cluster non può essere eliminato definitivamente. Contiene gruppi di applicazioni non core che devono essere eliminati prima che il cluster possa essere eliminato definitivamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**\_conflitto di \_ risorse di condivisione file \_ di errore \_**
</dt> <dd> <dl> <dt>

5938 (0x1732)
</dt> <dt>



La condivisione file associata alla risorsa di controllo di condivisione file non può essere ospitata da questo cluster o da uno dei relativi nodi.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**ERRORE del \_ cluster per \_ rimuovere la \_ richiesta non valida \_**
</dt> <dd> <dl> <dt>

5939 (0x1733)
</dt> <dt>



L'eliminazione di questo nodo non è valida in questo momento. A causa dell'eliminazione del nodo dei requisiti del quorum, il cluster viene arrestato. Se è l'ultimo nodo del cluster, usare il comando destroy cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**\_ \_ risorsa singleton del cluster di errore \_**
</dt> <dd> <dl> <dt>

5940 (0x1734)
</dt> <dt>



Nel cluster è consentita una sola istanza di questo tipo di risorsa.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**ERRORE \_ della \_ \_ risorsa singleton del gruppo cluster \_**
</dt> <dd> <dl> <dt>

5941 (0x1735)
</dt> <dt>



È consentita una sola istanza di questo tipo di risorsa per gruppo di risorse.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**ERRORE \_ del \_ provider di risorse cluster \_ \_**
</dt> <dd> <dl> <dt>

5942 (0x1736)
</dt> <dt>



La risorsa non è riuscita a tornare in linea a causa di un errore di una o più risorse del provider.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**errore \_ di \_ configurazione della risorsa cluster \_ errore \_**
</dt> <dd> <dl> <dt>

5943 (0x1737)
</dt> <dt>



La risorsa ha indicato che non è possibile passare in linea su alcun nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**gruppo di cluster di errore \_ \_ \_ occupato**
</dt> <dd> <dl> <dt>

5944 (0x1738)
</dt> <dt>



Al momento non è possibile eseguire l'operazione corrente in questo gruppo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**ERRORE \_ del \_ \_ volume condiviso del cluster \_**
</dt> <dd> <dl> <dt>

5945 (0x1739)
</dt> <dt>



La directory o il file non si trova in un volume condiviso cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**\_ \_ \_ descrittore di sicurezza non valido del cluster di errori \_**
</dt> <dd> <dl> <dt>

5946 (0x173A)
</dt> <dt>



Il descrittore di sicurezza non soddisfa i requisiti per un cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**\_ \_ volumi condivisi cluster \_ \_ di errore in \_ uso**
</dt> <dd> <dl> <dt>

5947 (0x173B)
</dt> <dt>



Nel cluster sono configurate una o più risorse di volumi condivisi. Queste risorse devono essere spostate nello spazio di archiviazione disponibile affinché l'operazione abbia esito positivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**ERRORE del \_ cluster \_ usare l' \_ \_ API volumi condivisi \_**
</dt> <dd> <dl> <dt>

5948 (0x173C)
</dt> <dt>



Il gruppo o la risorsa non può essere modificato direttamente. Usare le API del volume condiviso per eseguire l'operazione desiderata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**\_ \_ backup del cluster \_ di errore in \_ corso**
</dt> <dd> <dl> <dt>

5949 (0x173D)
</dt> <dt>



Il backup è in corso. Attendere il completamento del backup prima di riprovare.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**ERRORE \_ non \_ CSV \_ percorso**
</dt> <dd> <dl> <dt>

5950 (0x173E)
</dt> <dt>



Il percorso non appartiene a un volume condiviso cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**\_volume CSV \_ errore \_ non \_ locale**
</dt> <dd> <dl> <dt>

5951 (0x173F)
</dt> <dt>



Il volume condiviso cluster non è installato localmente in questo nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**errore durante la chiusura del watchdog del \_ cluster \_ \_**
</dt> <dd> <dl> <dt>

5952 (0x1740)
</dt> <dt>



Il watchdog del cluster verrà terminato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**ERRORE \_ di \_ spostamento della risorsa cluster di \_ \_ \_ nodi incompatibili \_**
</dt> <dd> <dl> <dt>

5953 (0x1741)
</dt> <dt>



Una risorsa ha dato il veto a uno spostamento tra due nodi perché non sono compatibili.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**\_spessore nodo del cluster di errore \_ non valido \_ \_**
</dt> <dd> <dl> <dt>

5954 (0x1742)
</dt> <dt>



La richiesta non è valida perché non è possibile modificare il peso del nodo mentre il cluster si trova in modalità quorum solo disco oppure perché la modifica del peso del nodo viola i requisiti minimi del quorum del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**errore durante la chiamata alla \_ \_ risorsa cluster \_ \_**
</dt> <dd> <dl> <dt>

5955 (0x1743)
</dt> <dt>



La risorsa ha posto il veto alla chiamata.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**ERRORE \_ resmon \_ risorse di sistema \_ \_ mancanti**
</dt> <dd> <dl> <dt>

5956 (0x1744)
</dt> <dt>



Non è stato possibile avviare o eseguire la risorsa perché non è stato possibile riservare risorse di sistema sufficienti.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**la \_ \_ risorsa cluster \_ di errore \_ \_ non dispone \_ \_ di risorse sufficienti \_ per \_ spostare la destinazione**
</dt> <dd> <dl> <dt>

5957 (0x1745)
</dt> <dt>



Una risorsa ha bloccato uno spostamento tra due nodi perché la destinazione attualmente non dispone di risorse sufficienti per completare l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**la \_ \_ risorsa cluster \_ di errore \_ Sposta \_ \_ le risorse insufficienti \_ \_ nell' \_ origine**
</dt> <dd> <dl> <dt>

5958 (0x1746)
</dt> <dt>



Una risorsa ha causato il veto di uno spostamento tra due nodi perché l'origine attualmente non dispone di risorse sufficienti per completare l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**ERRORE del \_ gruppo di cluster in \_ \_ coda**
</dt> <dd> <dl> <dt>

5959 (0x1747)
</dt> <dt>



Non è possibile completare l'operazione richiesta perché il gruppo è in coda per un'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**ERRORE \_ \_ \_ stato blocco risorse \_ cluster**
</dt> <dd> <dl> <dt>

5960 (0x1748)
</dt> <dt>



L'operazione richiesta non può essere completata perché lo stato di una risorsa è bloccato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**ERRORE \_ \_ failover del \_ volume condiviso cluster \_ \_ non \_ consentito**
</dt> <dd> <dl> <dt>

5961 (0x1749)
</dt> <dt>



La risorsa non può essere spostata in un altro nodo perché il volume condiviso del cluster ha consentito l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**ERRORE \_ \_ \_ di svuotamento del nodo cluster \_ in \_ corso**
</dt> <dd> <dl> <dt>

5962 (0x174A)
</dt> <dt>



Uno svuotamento del nodo è già in corso.

Questo valore era denominato anche **errore \_ \_ \_ di evacuazione nodi cluster \_ in \_ corso**


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**ERRORE \_ del \_ disco del cluster \_ non \_ connesso**
</dt> <dd> <dl> <dt>

5963 (0x174B)
</dt> <dt>



L'archiviazione in cluster non è connessa al nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**\_disco errore \_ non \_ compatibile con CSV \_**
</dt> <dd> <dl> <dt>

5964 (0x174C)
</dt> <dt>



Il disco non è configurato in modo da essere utilizzato con CSV. I dischi CSV devono contenere almeno una partizione formattata con NTFS.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**\_risorsa \_ di errore non \_ \_ presente nell' \_ archiviazione disponibile**
</dt> <dd> <dl> <dt>

5965 (0x174D)
</dt> <dt>



Per completare questa azione, è necessario che la risorsa faccia parte del gruppo di archiviazione disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**ERRORE \_ del \_ volume condiviso del cluster \_ \_ reindirizzato**
</dt> <dd> <dl> <dt>

5966 (0x174E)
</dt> <dt>



L'operazione CSVFS non è riuscita perché il volume è in modalità reindirizzato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**ERRORE \_ del \_ volume condiviso cluster \_ \_ non \_ reindirizzato**
</dt> <dd> <dl> <dt>

5967 (0x174F)
</dt> <dt>



L'operazione CSVFS non è riuscita perché il volume non è in modalità reindirizzata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**il \_ cluster di errore \_ non può \_ restituire \_ Proprietà**
</dt> <dd> <dl> <dt>

5968 (0x1750)
</dt> <dt>



Non è possibile restituire le proprietà del cluster in questo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**\_ \_ la risorsa cluster \_ di errore contiene un' \_ \_ area diff non supportata \_ \_ per i \_ \_ volumi condivisi**
</dt> <dd> <dl> <dt>

5969 (0x1751)
</dt> <dt>



La risorsa disco del cluster contiene un'area di diff snapshot software non supportata per i volumi condivisi del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**ERRORE \_ \_ della risorsa \_ cluster \_ in \_ \_ modalità manutenzione**
</dt> <dd> <dl> <dt>

5970 (0x1752)
</dt> <dt>



Non è possibile completare l'operazione perché la risorsa è in modalità di manutenzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**\_conflitto di \_ affinità del cluster di errore \_**
</dt> <dd> <dl> <dt>

5971 (0x1753)
</dt> <dt>



Non è possibile completare l'operazione a causa di conflitti di affinità del cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**\_la risorsa cluster di errore \_ è una \_ \_ \_ macchina virtuale di replica \_**
</dt> <dd> <dl> <dt>

5972 (0x1754)
</dt> <dt>



Non è possibile completare l'operazione perché la risorsa è una macchina virtuale di replica.


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

 

 




