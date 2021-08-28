---
description: Nell'elenco seguente sono elencati gli eventi supportati dai log WMI in Windows Vista e sistemi operativi successivi.
ms.assetid: ad8891cc-0b76-404d-81fc-961bcdbfae32
ms.tgt_platform: multiple
title: Messaggi di evento WMI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bb2b0a732d79c8b8c11e8bd14a217ef1ee81eb29bead4a885003ea98f82898
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120711"
---
# <a name="wmi-event-messages"></a>Messaggi di evento WMI

Nell'elenco seguente sono elencati gli eventi supportati dai log WMI in Windows Vista e sistemi operativi successivi.

> [!Note]  
> La documentazione seguente è progettata per sviluppatori e amministratori IT. Se si sta tentando di risolvere un messaggio di errore WMI nel sistema home, vedere il sito [Web Supporto tecnico Microsoft.](https://support.microsoft.com/)

 

<dl> <dt>

<span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**WBEM \_ MC \_ REPOSITORY \_ INCONSISTENT**
</dt> <dd> <dl> <dt>

1073747424 (0x400015E0)
</dt> <dt>



Il servizio Windows Management Instrumentation ha rilevato un'incoerenza con il repository WMI nella directory *%windir% \\ system32 \\ wbem \\ repository* e non è stato in grado di ripristinarlo. Il repository WMI verrà ora eliminato. Verrà creato un nuovo repository basato sul meccanismo di ripristino automatico.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**WBEM \_ MC \_ PROVIDER \_ SUBSYSTEM \_ LOCALSYSTEM \_ PROVIDER \_ LOAD**
</dt> <dd> <dl> <dt>

2147483711 (0x8000003F)
</dt> <dt>



Nello spazio dei nomi di Strumentazione gestione Windows %2 è stato registrato un provider %1 per l'utilizzo dell'account LocalSystem. Questo account dispone di privilegi e il provider può causare una violazione della sicurezza se non rappresenta correttamente le richieste utente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**WBEM \_ MC \_ MOF NON CARICATO AL \_ \_ \_ \_ RIPRISTINO**
</dt> <dd> <dl> <dt>

3221225476 (0xC0000004)
</dt> <dt>



Errore %1 durante il tentativo di caricamento del file MOF %2 durante il ripristino di . File MOF contrassegnato con autorecover.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM \_ MC \_ CANNOT \_ ACTIVATE \_ FILTER**
</dt> <dd> <dl> <dt>

3221225482 (0xC000000A)
</dt> <dt>



Impossibile riattivare il filtro eventi con query "%2" nello spazio dei nomi "%1" a causa dell'errore %3. Gli eventi non possono essere recapitati tramite questo filtro fino a quando il problema non viene corretto.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**QUERY DEL PROVIDER DI \_ EVENTI WBEM MC NON \_ \_ \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

3221225493 (0xC0000015)
</dt> <dt>



Il provider di eventi %1 ha tentato di registrare una query sintatticamente non valida "%2". La query verrà ignorata. La query può essere corretta esaminando il repository WMI con CIM Studio e aggiornando le sottoscrizioni permanenti per il provider e la query elencati. Se la sottoscrizione permanente viene creata con il file MOF in arrivo con un prodotto installato, è necessario contattare il fornitore dell'applicazione per correggere la registrazione non corretta.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**QUERY INTRINSECA DEL PROVIDER DI \_ EVENTI WBEM MC NON \_ \_ \_ \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

3221225494 (0xC0000016)
</dt> <dt>



Il provider di eventi %1 ha tentato di registrare una query di eventi intrinseca "%2" nello spazio dei nomi %3 per cui non è stato possibile determinare il set di classi di oggetti di destinazione. La query verrà ignorata.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**QUERY DEL PROVIDER DI EVENTI WBEM \_ MC \_ TROPPO \_ \_ \_ \_ AMPIA**
</dt> <dd> <dl> <dt>

3221225495 (0xC0000017)
</dt> <dt>



Il provider di eventi %1 ha tentato di registrare la query "%2" nello spazio dei nomi %3 che è troppo ampia. I provider di eventi non possono fornire eventi forniti dal sistema. La query verrà ignorata. Contattare il fornitore dell'applicazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**QUERY DEL \_ PROVIDER DI EVENTI WBEM MC NON \_ \_ \_ \_ \_ TROVATA**
</dt> <dd> <dl> <dt>

3221225496 (0xC0000018)
</dt> <dt>



Il provider di eventi %1 ha tentato di registrare la query "%2" la cui classe di destinazione "%3" nello spazio dei nomi %4 non esiste. La query verrà ignorata.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**QUERY DEL PROVIDER DI EVENTI WBEM \_ MC \_ NON \_ \_ \_ \_ EVENTO**
</dt> <dd> <dl> <dt>

3221225497 (0xC0000019)
</dt> <dt>



Il provider di eventi %1 ha tentato di registrare la query &quot; %2 &quot; la cui classe di destinazione &quot; %3 &quot; non è una classe di evento. La query verrà ignorata. Contattare il fornitore dell'applicazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**ERRORE WBEM \_ MC \_ WBEM \_ CORE \_**
</dt> <dd> <dl> <dt>

3221225500 (0xC000001C)
</dt> <dt>



Impossibile inizializzare il sottosistema WMI Core o provider o il sottosistema eventi con numero di errore %1. Ciò potrebbe essere dovuto a una versione di WMI installata in modo non riuscito, a un errore di aggiornamento del repository WMI, a spazio su disco insufficiente o a memoria insufficiente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**ERRORE DI CONNESSIONE \_ WBEM MC \_ \_ \_ ADAP**
</dt> <dd> <dl> <dt>

3221225515 (0xC000002B)
</dt> <dt>



Windows La strumentazione di gestione ADAP non è riuscita a connettersi allo spazio dei nomi %1 con l'errore seguente %2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**ERRORE \_ PUTCLASS DI WBEM MC \_ \_ ADAP PERFLIB \_ \_**
</dt> <dd> <dl> <dt>

3221225520 (0xC0000030)
</dt> <dt>



Windows ADAP di Strumentazione gestione non è riuscito a salvare l'oggetto %1 nello spazio dei nomi %2 a causa dell'errore %3 seguente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ ADAP NON È IN GRADO \_ DI AGGIUNGERE \_ \_ \_ WIN32PERF**
</dt> <dd> <dl> <dt>

3221225530 (0xC000003A)
</dt> <dt>



Windows Strumentazione gestione ADAP non è riuscito a creare la classe \_ di base Win32 Perf in %1:Result=%2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ ADAP NON È IN GRADO \_ DI AGGIUNGERE \_ \_ \_ WIN32PERFRAWDATA**
</dt> <dd> <dl> <dt>

3221225531 (0xC000003B)
</dt> <dt>



Windows Strumentazione gestione ADAP: impossibile creare la classe di \_ base Win32 PerfRawData %1.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**IMPOSSIBILE AVVIARE \_ IL REPOSITORY WBEM MC \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

3221231073 (0xC00015E1)
</dt> <dt>



Il servizio Windows Management Instrumentation non è riuscito a caricare i file del repository nella directory *%windir% \\ system32 \\ wbem \\ repository*. Ciò può essere causato da un danneggiamento nei file del repository, dalle impostazioni di sicurezza in questa directory, dalla mancanza di spazio su disco o da altri problemi relativi alle risorse di sistema, ad esempio la mancanza di memoria. Se questo errore si verifica ogni volta che il computer viene riavviato, l'amministratore del computer potrebbe dover arrestare il servizio WMI, esaminare l'impostazione di sicurezza in questa cartella e i file in questa cartella ed eseguire WMIDiag per convalidare l'integrità di Strumentazione gestione Windows.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM \_ MC \_ WBEM \_ RICHIEDE LA CRITTOGRAFIA \_ \_ NEGATA**
</dt> <dd> <dl> <dt>

3221231077 (0xC00015E5)
</dt> <dt>



L'accesso allo spazio dei nomi %1 è stato negato perché lo spazio dei nomi è contrassegnato con RequiresEncryption, ma lo script o l'applicazione ha tentato di connettersi a questo spazio dei nomi con un livello di autenticazione inferiore a **Pkt \_ Privacy.** Modificare il livello di autenticazione in **Pkt \_ Privacy** ed eseguire di nuovo lo script o l'applicazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM \_ MC \_ WBEM \_ RICHIEDE CRITTOGRAFIA \_ \_ ASINCRONA \_ NEGATA**
</dt> <dd> <dl> <dt>

3221231078 (0xC00015E6)
</dt> <dt>



Windows Il servizio Strumentazione gestione non è stato in grado di recapitare i risultati in modo asincrono per lo spazio dei nomi %1. Lo spazio dei nomi è contrassegnato con RequiresEncryption, ma WinMgmt non è stato in grado di stabilire una connessione protetta al computer client. Verificare che sia presente una relazione di trust tra i computer client e server in modo che il client riconosca l'account del computer server.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**HOST WBEM \_ MC \_ WBEM \_ NON PIÙ IN \_ FUNZIONE**
</dt> <dd> <dl> <dt>

3221231084 (0xC00015EC)
</dt> <dt>



Windows Strumentazione gestione è stata arrestata WMIPRVSE.EXE perché una quota ha raggiunto un valore di avviso. Quota: %1 Valore: %2 Valore massimo: %3 WMIPRVSE PID: %4.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM \_ MC \_ WBEM \_ REPFILESNOTFOUND**
</dt> <dd> <dl> <dt>

3221231086 (0xC00015EE)
</dt> <dt>



Durante l'avvio del servizio, il Windows Management Instrumentation non è riuscito a individuare i file del repository. Verrà creato un nuovo repository basato sul meccanismo di ripristino automatico.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM \_ MC \_ WBEM \_ AVVIATO \_ CORRETTAMENTE**
</dt> <dd> <dl> <dt>

3221231087 (0xC00015EF)
</dt> <dt>



Windows Il servizio Strumentazione gestione è stato avviato correttamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM \_ MC \_ WBEM \_ CORE \_ PSS \_ ESS \_ INIZIALIZZATO**
</dt> <dd> <dl> <dt>

3221231089 (0xC00015F1)
</dt> <dt>



Windows Inizializzazione dei sottosistemi del servizio Strumentazione gestione completata.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**ERRORE INIT DEL SERVIZIO \_ \_ WBEM MC WBEM \_ \_ \_**
</dt> <dd> <dl> <dt>

3221225501 (0xC000001D)
</dt> <dt>



È stato restituito il numero di errore %1 durante il tentativo di inizializzazione Windows servizio Strumentazione gestione. Ciò potrebbe essere dovuto a una versione di WMI installata in modo non riuscito, a un errore di aggiornamento del repository WMI, a spazio su disco insufficiente o a memoria insufficiente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**REPOSITORY WBEM \_ MC \_ WBEM \_ \_ RICREATO**
</dt> <dd> <dl> <dt>

3221231088 (0xC00015F0)
</dt> <dt>



Windows Il repository di Strumentazione gestione è stato ricreato usando il meccanismo di salvataggio automatico.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi WMI](wmi-events.md)
</dt> <dt>

[Risoluzione dei problemi wmi](wmi-troubleshooting.md)
</dt> </dl>

 

 




