---
description: Nell'elenco seguente sono elencati gli eventi supportati dai log WMI in Windows Vista e nei sistemi operativi successivi.
ms.assetid: ad8891cc-0b76-404d-81fc-961bcdbfae32
ms.tgt_platform: multiple
title: Messaggi di evento WMI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 543e7131ac0c73a9f1e0f111dafe90197989a33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310339"
---
# <a name="wmi-event-messages"></a>Messaggi di evento WMI

Nell'elenco seguente sono elencati gli eventi supportati dai log WMI in Windows Vista e nei sistemi operativi successivi.

> [!Note]  
> La documentazione seguente è progettata per gli sviluppatori e gli amministratori IT. Se si sta tentando di risolvere un messaggio di errore WMI nel sistema principale, fare riferimento al sito Web [supporto tecnico Microsoft](https://support.microsoft.com/) .

 

<dl> <dt>

<span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**\_repository WBEM \_ MC \_ incoerente**
</dt> <dd> <dl> <dt>

1073747424 (0x400015E0)
</dt> <dt>



Il servizio Strumentazione gestione Windows ha rilevato un'incoerenza con il repository WMI nel repository di directory *% windir% \\ system32 \\ WBEM \\* e non è stato in grado di recuperarlo. Il repository WMI verrà ora eliminato. verrà creato un nuovo repository basato sul meccanismo di recupero automatico.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**\_caricamento del \_ \_ \_ provider LocalSystem del sottosistema del provider \_ di WBEM MC \_**
</dt> <dd> <dl> <dt>

2147483711 (0x8000003F)
</dt> <dt>



Un provider %1 è stato registrato nello spazio dei nomi Strumentazione gestione Windows %2 per l'utilizzo dell'account LocalSystem. Questo account è con privilegi e il provider può causare una violazione della sicurezza se non rappresenta correttamente le richieste degli utenti.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**\_MOF MC \_ MOF \_ non \_ caricato \_ al \_ ripristino**
</dt> <dd> <dl> <dt>

3221225476 (0xC0000004)
</dt> <dt>



Si è verificato l'errore %1 durante il tentativo di caricare il file MOF %2 durante il ripristino. File MOF contrassegnato con autocover.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM \_ MC \_ non è in grado di \_ attivare il \_ filtro**
</dt> <dd> <dl> <dt>

3221225482 (0xC000000A)
</dt> <dt>



Impossibile riattivare il filtro eventi con query "%2" nello spazio dei nomi "%1" a causa dell'errore %3. Non è possibile recapitare gli eventi tramite questo filtro fino a quando il problema non viene risolto.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**\_query del provider di eventi WBEM MC \_ non valida \_ \_ \_**
</dt> <dd> <dl> <dt>

3221225493 (0xC0000015)
</dt> <dt>



Il provider di eventi %1 ha tentato di registrare una query sintatticamente non valida "%2". La query verrà ignorata. È possibile correggere la query esaminando il repository WMI con CIM Studio e aggiornando le sottoscrizioni permanenti per il provider e la query elencati. Se la sottoscrizione permanente viene creata con un file MOF in arrivo con un prodotto installato, è necessario contattare il fornitore dell'applicazione per correggere la registrazione non funzionante.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**\_ \_ \_ \_ \_ query intrinseca del provider di eventi WBEM MC non valida \_**
</dt> <dd> <dl> <dt>

3221225494 (0xC0000016)
</dt> <dt>



Il provider di eventi %1 ha tentato di registrare una query di eventi intrinseca "%2" nello spazio dei nomi %3 per il quale non è stato possibile determinare il set di classi di oggetti di destinazione. La query verrà ignorata.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**\_query del provider di eventi WBEM MC \_ \_ \_ \_ troppo \_ ampia**
</dt> <dd> <dl> <dt>

3221225495 (0xC0000017)
</dt> <dt>



Il provider di eventi %1 ha tentato di registrare la query "%2" nello spazio dei nomi %3 troppo ampio. I provider di eventi non possono fornire eventi forniti dal sistema. La query verrà ignorata. Contattare il fornitore dell'applicazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**\_query del provider di eventi WBEM MC \_ \_ \_ \_ non \_ trovata**
</dt> <dd> <dl> <dt>

3221225496 (0xC0000018)
</dt> <dt>



Il provider di eventi %1 ha tentato di registrare la query "%2" la cui classe di destinazione "%3" nello spazio dei nomi %4 non esiste. La query verrà ignorata.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**\_evento di \_ query del provider di eventi WBEM MC \_ \_ \_ non \_**
</dt> <dd> <dl> <dt>

3221225497 (0xC0000019)
</dt> <dt>



Il provider di eventi %1 ha tentato di registrare &quot; la query %2 &quot; la cui classe &quot; di destinazione %3 &quot; non è una classe di evento. La query verrà ignorata. Contattare il fornitore dell'applicazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**\_errore di \_ \_ Core WBEM MC WBEM \_**
</dt> <dd> <dl> <dt>

3221225500 (0xC000001C)
</dt> <dt>



Non è stato possibile inizializzare il sottosistema o il sottosistema WMI o il sottosistema di eventi con numero di errore %1. Il problema potrebbe essere dovuto a una versione non installata di WMI, a un errore di aggiornamento del repository WMI, a spazio su disco insufficiente o a memoria insufficiente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**\_errore di connessione WBEM MC \_ ADAP \_ \_**
</dt> <dd> <dl> <dt>

3221225515 (0xC000002B)
</dt> <dt>



Strumentazione gestione Windows ADAP non è riuscito a connettersi allo spazio dei nomi %1 con l'errore seguente %2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**\_ \_ \_ \_ errore Perflib PUTCLASS \_ di WBEM MC ADAP**
</dt> <dd> <dl> <dt>

3221225520 (0xC0000030)
</dt> <dt>



Strumentazione gestione Windows ADAP non è stato in grado di salvare l'oggetto %1 nello spazio dei nomi %2 a causa del seguente errore %3.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ ADAP \_ non è \_ in grado di \_ aggiungere \_ WIN32PERF**
</dt> <dd> <dl> <dt>

3221225530 (0xC000003A)
</dt> <dt>



Strumentazione gestione Windows ADAP non è stato in grado di creare la \_ classe base delle prestazioni Win32 in %1: risultato = %2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ ADAP \_ non è \_ in grado di \_ aggiungere \_ WIN32PERFRAWDATA**
</dt> <dd> <dl> <dt>

3221225531 (0xC000003B)
</dt> <dt>



Strumentazione gestione Windows ADAP non è stato in grado di creare la \_ classe di base Win32 PerfRawData %1.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**\_ \_ \_ non è stato \_ possibile \_ avviare il repository WBEM MC**
</dt> <dd> <dl> <dt>

3221231073 (0xC00015E1)
</dt> <dt>



Il servizio Strumentazione gestione Windows non è riuscito a caricare i file del repository nel repository di directory *% windir% \\ system32 \\ WBEM \\*. Questo problema può essere causato da un danneggiamento nei file del repository, dalle impostazioni di sicurezza di questa directory, dalla mancanza di spazio su disco o da altri problemi di risorse di sistema, ad esempio la mancanza di memoria. Se questo errore si verifica ogni volta che il computer viene riavviato, l'amministratore di questo computer potrebbe dover arrestare il servizio WMI, verificare l'impostazione di sicurezza sulla cartella e i file in questa cartella ed eseguire WMIDiag per convalidare l'integrità del Strumentazione gestione Windows.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM \_ MC \_ WBEM \_ richiede la \_ crittografia \_ negata**
</dt> <dd> <dl> <dt>

3221231077 (0xC00015E5)
</dt> <dt>



Accesso allo spazio dei nomi %1 negato perché lo spazio dei nomi è contrassegnato con RequiresEncryption, ma lo script o l'applicazione ha tentato di connettersi a questo spazio dei nomi con un livello di autenticazione inferiore alla **\_ privacy di PKT**. Modificare il livello di autenticazione in **PKT \_ privacy** , quindi eseguire di nuovo lo script o l'applicazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM \_ MC \_ WBEM \_ richiede la \_ crittografia \_ asincrona \_ negata**
</dt> <dd> <dl> <dt>

3221231078 (0xC00015E6)
</dt> <dt>



Impossibile recapitare i risultati in modo asincrono per lo spazio dei nomi %1. Strumentazione gestione Windows Lo spazio dei nomi è contrassegnato con RequiresEncryption, ma WinMgmt non è riuscito a stabilire una connessione sicura al computer client. Verificare che sia presente una relazione di trust tra i computer client e server in modo che il client riconosca l'account del computer server.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**l' \_ \_ host WBEM MC WBEM è stato \_ \_ ucciso**
</dt> <dd> <dl> <dt>

3221231084 (0xC00015EC)
</dt> <dt>



Il Strumentazione gestione Windows è stato interrotto WMIPRVSE.EXE perché una quota ha raggiunto un valore di avviso. Quota: %1 valore: %2 valore massimo: %3 WMIPRVSE PID: %4.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM \_ MC \_ WBEM \_ REPFILESNOTFOUND**
</dt> <dd> <dl> <dt>

3221231086 (0xC00015EE)
</dt> <dt>



Durante l'avvio del servizio, il servizio Strumentazione gestione Windows non è stato in grado di individuare i file del repository. Verrà creato un nuovo repository basato sul meccanismo di recupero automatico.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM \_ MC \_ WBEM \_ ha avviato \_ è stata**
</dt> <dd> <dl> <dt>

3221231087 (0xC00015EF)
</dt> <dt>



Il servizio Strumentazione gestione Windows è stato avviato correttamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**si \_ è \_ \_ \_ \_ inizializzato l'ESS \_ di WBEM MC WBEM Core PSS**
</dt> <dd> <dl> <dt>

3221231089 (0xC00015F1)
</dt> <dt>



Strumentazione gestione Windows sottosistemi di servizio inizializzati correttamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**\_errore di \_ \_ \_ inizializzazione del \_ servizio WBEM MC WBEM**
</dt> <dd> <dl> <dt>

3221225501 (0xC000001D)
</dt> <dt>



Il numero di errore %1 è stato restituito durante il tentativo di inizializzare Strumentazione gestione Windows servizio. Il problema potrebbe essere dovuto a una versione non installata di WMI, a un errore di aggiornamento del repository WMI, a spazio su disco insufficiente o a memoria insufficiente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**\_repository WBEM \_ MC \_ WBEM \_ ricreato**
</dt> <dd> <dl> <dt>

3221231088 (0xC00015F0)
</dt> <dt>



Strumentazione gestione Windows repository è stato ricreato con il meccanismo di recupero automatico.


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

[Risoluzione dei problemi WMI](wmi-troubleshooting.md)
</dt> </dl>

 

 




