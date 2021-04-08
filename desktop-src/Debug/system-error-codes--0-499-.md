---
description: Descrive i codici di errore 0-499 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: Codici di errore di sistema (0-499) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 413d9674f511bd49df12267b60d6c6c3dac366aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877849"
---
# <a name="system-error-codes-0-499"></a>Codici di errore di sistema (0-499)

> [!NOTE]
> Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema. Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .

Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) (errori da 0 a 499). Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .

<dl> <dt>

<span id="ERROR_SUCCESS"></span><span id="error_success"></span>**ERRORE \_ riuscito**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Operazione riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**ERRORE \_ funzione non valida \_**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Funzione non corretta.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**FILE di errore \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Non è possibile trovare il file specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**il percorso dell'errore non è stato \_ \_ \_ trovato**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



impossibile trovare il percorso specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERRORE di \_ troppi \_ \_ \_ file aperti**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Il sistema non è in grado di aprire il file.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERRORE di \_ accesso \_ negato**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



Accesso negato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERRORE \_ handle non valido \_**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



Handle non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**ERRORE nell' \_ Arena \_**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



I blocchi di controllo dell'archiviazione sono stati eliminati definitivamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERRORE \_ di \_ memoria insufficiente \_**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Risorse di memoria insufficienti per elaborare il comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**ERRORE \_ blocco non valido \_**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



L'indirizzo del blocco di controllo dell'archiviazione non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERRORE \_ ambiente non valido \_**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



L'ambiente non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**\_formato errore errato \_**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



Tentativo di caricare un programma con un formato non corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERRORE \_ di \_ accesso non valido**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



Il codice di accesso non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERRORE \_ dati non validi \_**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



I dati non sono validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERRORE \_ OutOfMemory**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



Lo spazio di archiviazione disponibile non è sufficiente per completare questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERRORE \_ unità non valida \_**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



Il sistema non è in grado di trovare l'unità specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERRORE \_ \_ directory corrente**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



La directory non può essere rimossa.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERRORE \_ non \_ stesso \_ dispositivo**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



Il sistema non è in grado di spostare il file in un'unità disco diversa.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERRORE \_ nessun \_ altro \_ file**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



Non sono presenti altri file.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**\_protezione scrittura \_ errore**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



Il supporto è protetto da scrittura.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERRORE \_ unità non valida \_**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



Il sistema non è in grado di trovare il dispositivo specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERRORE \_ non \_ pronto**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



Il dispositivo non è pronto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERRORE \_ \_ comando errato**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



Il dispositivo non riconosce il comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRC"></span><span id="error_crc"></span>**ERRORE \_ CRC**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



Errore dei dati (controllo della ridondanza ciclica).


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERRORE \_ di \_ lunghezza errata**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



Il programma ha emesso un comando ma la lunghezza del comando non è corretta.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK"></span><span id="error_seek"></span>**\_ricerca errori**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



L'unità non è in grado di individuare un'area o una traccia specifica sul disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERRORE \_ non \_ \_ disco DOS**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



Non è possibile accedere al disco o al dischetto specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**\_ \_ Impossibile trovare il settore degli errori \_**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



L'unità non è in grado di trovare il settore richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERRORE \_ \_ di \_ carta esaurita**
</dt> <dd> <dl> <dt>

28 (0x1C)
</dt> <dt>



La stampante ha esaurito la carta.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**errore di \_ scrittura errore \_**
</dt> <dd> <dl> <dt>

29 (0x1D)
</dt> <dt>



Il sistema non è in grado di scrivere sul dispositivo specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**errore di \_ lettura errore \_**
</dt> <dd> <dl> <dt>

30 (0x1E)
</dt> <dt>



Il sistema non è in grado di leggere dal dispositivo specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**ERRORE \_ gen \_ errore**
</dt> <dd> <dl> <dt>

31 (0x1F)
</dt> <dt>



Un dispositivo collegato al sistema non funziona.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**\_violazione di condivisione degli errori \_**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Il processo non può accedere al file perché è in uso da un altro processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**\_violazione blocco \_ errori**
</dt> <dd> <dl> <dt>

33 (0x21)
</dt> <dt>



Il processo non può accedere al file perché un altro processo ne ha bloccato una parte.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERRORE \_ \_ disco errato**
</dt> <dd> <dl> <dt>

34 (0x22)
</dt> <dt>



Il dischetto errato si trova nell'unità. Inserisci %2 (numero di serie volume: %3) nell'unità %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**è \_ stato \_ superato il buffer di condivisione errori \_**
</dt> <dd> <dl> <dt>

36 (0x24)
</dt> <dt>



Troppi file aperti per la condivisione.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**HANDLE di errore \_ \_ EOF**
</dt> <dd> <dl> <dt>

38 (0x26)
</dt> <dt>



È stata raggiunta la fine del file.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**ERRORE di \_ gestione del \_ disco \_ completo**
</dt> <dd> <dl> <dt>

39 (0x27)
</dt> <dt>



Disco pieno.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERRORE \_ non \_ supportato**
</dt> <dd> <dl> <dt>

50 (0x32)
</dt> <dt>



La richiesta non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERRORE \_ REM \_ non \_ elenco**
</dt> <dd> <dl> <dt>

51 (0x33)
</dt> <dt>



Impossibile trovare il percorso di rete. Verificare che il percorso di rete sia corretto e che il computer di destinazione non sia occupato o disattivato. Se Windows non è ancora in grado di trovare il percorso di rete, contattare l'amministratore di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**\_nome duplicato errore \_**
</dt> <dd> <dl> <dt>

52 (0x34)
</dt> <dt>



La connessione non è stata stabilita perché nella rete è presente un nome duplicato. Se si aggiunge un dominio, passare a sistema nel pannello di controllo per modificare il nome del computer e riprovare. Se si aggiunge un gruppo di lavoro, scegliere un altro nome del gruppo di lavoro.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERRORE \_ \_ NETPATH errato**
</dt> <dd> <dl> <dt>

53 (0x35)
</dt> <dt>



Impossibile trovare il percorso di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERRORE \_ rete \_ occupato**
</dt> <dd> <dl> <dt>

54 (0x36)
</dt> <dt>



La rete è occupata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**ERRORE \_ dev \_ non \_ esiste**
</dt> <dd> <dl> <dt>

55 (0x37)
</dt> <dt>



La risorsa o il dispositivo di rete specificato non è più disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERRORE di un \_ numero eccessivo di \_ \_ cmds**
</dt> <dd> <dl> <dt>

56 (0x38)
</dt> <dt>



È stato raggiunto il limite di comandi BIOS di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERRORE di \_ adattamento \_ HDW \_ Err**
</dt> <dd> <dl> <dt>

57 (0x39)
</dt> <dt>



Si è verificato un errore hardware della scheda di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERRORE \_ \_ net \_ resp errato**
</dt> <dd> <dl> <dt>

58 (0x3A)
</dt> <dt>



Il server specificato non può effettuare l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERRORE \_ UNEXP \_ net \_ Err**
</dt> <dd> <dl> <dt>

59 (0x3B)
</dt> <dt>



Si è verificato un errore di rete imprevisto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERRORE \_ di \_ adattamento REM errato \_**
</dt> <dd> <dl> <dt>

60 (0x3C)
</dt> <dt>



La scheda remota non è compatibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERRORE \_ printq \_ completo**
</dt> <dd> <dl> <dt>

61 (0x3D)
</dt> <dt>



Coda della stampante piena.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERRORE \_ senza \_ \_ spazio dello spooler**
</dt> <dd> <dl> <dt>

62 (0x3E)
</dt> <dt>



Lo spazio per archiviare il file in attesa di stampa non è disponibile nel server.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERRORE di \_ stampa \_ annullato**
</dt> <dd> <dl> <dt>

63 (0x3F)
</dt> <dt>



Il file in attesa di stampa è stato eliminato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**ERRORE \_ NETNAME \_ eliminato**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Il nome di rete specificato non è più disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERRORE \_ di \_ accesso alla rete \_ negato**
</dt> <dd> <dl> <dt>

65 (0x41)
</dt> <dt>



Accesso alla rete negato.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERRORE \_ di \_ tipo dev errato \_**
</dt> <dd> <dl> <dt>

66 (0x42)
</dt> <dt>



Il tipo di risorsa di rete non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERRORE \_ \_ nome rete non valido \_**
</dt> <dd> <dl> <dt>

67 (0x43)
</dt> <dt>



Impossibile trovare il nome della rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERRORE di un \_ numero eccessivo di \_ \_ nomi**
</dt> <dd> <dl> <dt>

68 (0x44)
</dt> <dt>



È stato superato il limite del nome per la scheda della scheda di rete del computer locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERRORE di un \_ numero eccessivo di \_ \_ sess**
</dt> <dd> <dl> <dt>

69 (0x45)
</dt> <dt>



È stato superato il limite della sessione BIOS di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**condivisione degli errori \_ \_ sospesa**
</dt> <dd> <dl> <dt>

70 (0x46)
</dt> <dt>



Il server remoto è stato sospeso o è in fase di avvio.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**ERRORE \_ req \_ non \_ definit**
</dt> <dd> <dl> <dt>

71 (0x47)
</dt> <dt>



Al momento non è possibile eseguire altre connessioni a questo computer remoto perché sono già presenti tutte le connessioni che il computer può accettare.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**ERRORE \_ redir in \_ pausa**
</dt> <dd> <dl> <dt>

72 (0x48)
</dt> <dt>



La stampante o il dispositivo disco specificato è stato sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**il \_ file degli errori \_ esiste**
</dt> <dd> <dl> <dt>

80 (0x50)
</dt> <dt>



File esistente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**l'errore \_ non può \_ essere**
</dt> <dd> <dl> <dt>

82 (0x52)
</dt> <dt>



Impossibile creare la directory o il file.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERRORE \_ \_ I24**
</dt> <dd> <dl> <dt>

83 (0x53)
</dt> <dt>



Errore in INT 24.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**ERRORE \_ \_ di \_ strutture**
</dt> <dd> <dl> <dt>

84 (0x54)
</dt> <dt>



Lo spazio di archiviazione per elaborare la richiesta non è disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERRORE \_ già \_ assegnato**
</dt> <dd> <dl> <dt>

85 (0x55)
</dt> <dt>



Il nome del dispositivo locale è già in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**ERRORE \_ di \_ password non valida**
</dt> <dd> <dl> <dt>

86 (0x56)
</dt> <dt>



La password di rete specificata non è corretta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**ERRORE \_ parametro non valido \_**
</dt> <dd> <dl> <dt>

87 (0x57)
</dt> <dt>



Parametro non corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**errore errore di \_ scrittura in rete \_ \_**
</dt> <dd> <dl> <dt>

88 (0x58)
</dt> <dt>



Si è verificato un errore di scrittura sulla rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**ERRORE \_ nessun \_ \_ slot proc**
</dt> <dd> <dl> <dt>

89 (0x59)
</dt> <dt>



Il sistema non può avviare un altro processo in questo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERRORE di un \_ numero eccessivo di \_ \_ semafori**
</dt> <dd> <dl> <dt>

100 (0x64)
</dt> <dt>



Non è possibile creare un altro semaforo di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERRORE \_ escl. \_ SEM è \_ già \_ proprietario**
</dt> <dd> <dl> <dt>

101 (0x65)
</dt> <dt>



Il semaforo esclusivo è di proprietà di un altro processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**ERRORE \_ sem \_ \_ impostato**
</dt> <dd> <dl> <dt>

102 (0x66)
</dt> <dt>



Il semaforo è impostato e non può essere chiuso.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERRORE di un \_ numero eccessivo di \_ \_ \_ richieste SEM**
</dt> <dd> <dl> <dt>

103 (0x67)
</dt> <dt>



Non è possibile impostare di nuovo il semaforo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERRORE \_ non valido \_ in fase di \_ interrupt \_**
</dt> <dd> <dl> <dt>

104 (0x68)
</dt> <dt>



Non è possibile richiedere semafori esclusivi in fase di interrupt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERRORE \_ \_ proprietario sem \_ morto**
</dt> <dd> <dl> <dt>

105 (0x69)
</dt> <dt>



La proprietà precedente di questo semaforo è terminata.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**\_ \_ limite utente sem \_ errore**
</dt> <dd> <dl> <dt>

106 (0x6A)
</dt> <dt>



Inserire il dischetto per l'unità %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**\_modifica disco \_ errore**
</dt> <dd> <dl> <dt>

107 (0x6B)
</dt> <dt>



Il programma è stato interrotto perché non è stato inserito un dischetto alternativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**unità di errore \_ \_ bloccata**
</dt> <dd> <dl> <dt>

108 (0x6C)
</dt> <dt>



Il disco è in uso o è bloccato da un altro processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERRORE \_ con \_ pipe interrotta**
</dt> <dd> <dl> <dt>

109 (0x6D)
</dt> <dt>



Pipe terminata.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**ERRORE di \_ apertura \_ non riuscito**
</dt> <dd> <dl> <dt>

110 (0x6E)
</dt> <dt>



Il sistema non è in grado di aprire il dispositivo o il file specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**\_overflow del buffer di errore \_**
</dt> <dd> <dl> <dt>

111 (0x6F)
</dt> <dt>



Il nome del file è troppo lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**\_disco errore \_ pieno**
</dt> <dd> <dl> <dt>

112 (0x70)
</dt> <dt>



Lo spazio su disco è insufficiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERRORE \_ nessun \_ altro \_ handle di ricerca \_**
</dt> <dd> <dl> <dt>

113 (0x71)
</dt> <dt>



Non sono disponibili altri identificatori di file interni.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERRORE \_ dell' \_ handle di destinazione non valido \_**
</dt> <dd> <dl> <dt>

114 (0x72)
</dt> <dt>



L'identificatore del file interno di destinazione non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**ERRORE \_ categoria non valida \_**
</dt> <dd> <dl> <dt>

117 (0x75)
</dt> <dt>



La chiamata IOCTL eseguita dal programma dell'applicazione non è corretta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERRORE \_ di \_ verifica \_ opzione non valida**
</dt> <dd> <dl> <dt>

118 (0x76)
</dt> <dt>



Il valore del parametro dell'opzione verify-on-Write non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERRORE \_ \_ livello driver non valido \_**
</dt> <dd> <dl> <dt>

119 (0x77)
</dt> <dt>



Il sistema non supporta il comando richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**chiamata di errore \_ \_ non \_ implementata**
</dt> <dd> <dl> <dt>

120 (0x78)
</dt> <dt>



Questa funzione non è supportata in questo sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**\_timeout sem \_ errore**
</dt> <dd> <dl> <dt>

121 (0x79)
</dt> <dt>



Il periodo di timeout del semaforo è scaduto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERRORE \_ buffer insufficiente \_**
</dt> <dd> <dl> <dt>

122 (0x7A)
</dt> <dt>



L'area dati passata a una chiamata di sistema è troppo piccola.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**ERRORE \_ nome non valido \_**
</dt> <dd> <dl> <dt>

123 (0x7B)
</dt> <dt>



La sintassi del nome file, della directory o dell'etichetta di volume non è corretta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**ERRORE \_ livello non valido \_**
</dt> <dd> <dl> <dt>

124 (0x7C)
</dt> <dt>



Il livello della chiamata di sistema non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERRORE \_ senza \_ \_ etichetta volume**
</dt> <dd> <dl> <dt>

125 (0x7D)
</dt> <dt>



Il disco non ha un'etichetta di volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**ERRORE \_ mod \_ non \_ trovato**
</dt> <dd> <dl> <dt>

126 (0x7E)
</dt> <dt>



The specified module could not be found. (E_CSC_SYSTEM_INTERNAL: errore interno. Impossibile caricare il file o l'assembly 'ScopeEngineManaged.dll' o una delle sue dipendenze. Impossibile trovare il modulo specificato.)


</dt> </dl> </dd> <dt>

<span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**ERRORE di \_ proc \_ non \_ trovato**
</dt> <dd> <dl> <dt>

127 (0x7F)
</dt> <dt>



Impossibile trovare la procedura specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERRORE di \_ attesa \_ senza \_ figli**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Nessun processo figlio da attendere.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**ERRORE \_ figlio \_ non \_ completato**
</dt> <dd> <dl> <dt>

129 (0x81)
</dt> <dt>



Impossibile eseguire l'applicazione %1 in modalità Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**\_handle di \_ accesso \_ diretto errore**
</dt> <dd> <dl> <dt>

130 (0x82)
</dt> <dt>



Tentativo di utilizzare un handle di file per una partizione del disco aperta per un'operazione diversa dall'I/O del disco non elaborato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**\_ricerca negativa \_ errore**
</dt> <dd> <dl> <dt>

131 (0x83)
</dt> <dt>



È stato effettuato un tentativo di spostare il puntatore del file prima dell'inizio del file.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**ERRORE \_ durante la ricerca \_ nel \_ dispositivo**
</dt> <dd> <dl> <dt>

132 (0x84)
</dt> <dt>



Il puntatore del file non può essere impostato sul dispositivo o sul file specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**ERRORE \_ di \_ \_ destinazione join**
</dt> <dd> <dl> <dt>

133 (0x85)
</dt> <dt>



Non è possibile usare un comando JOIN o SUBSt per un'unità che contiene unità precedentemente unite in join.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**ERRORE \_ \_ aggiunto**
</dt> <dd> <dl> <dt>

134 (0x86)
</dt> <dt>



È stato effettuato un tentativo di usare un comando JOIN o SUBSt in un'unità che è già stata unita in join.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**l'errore \_ è \_ SUBST**
</dt> <dd> <dl> <dt>

135 (0x87)
</dt> <dt>



È stato effettuato un tentativo di usare un comando JOIN o SUBSt in un'unità che è già stata sostituita.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERRORE \_ non \_ Unito in join**
</dt> <dd> <dl> <dt>

136 (0x88)
</dt> <dt>



Il sistema ha tentato di eliminare il JOIN di un'unità non unita in JOIN.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERRORE \_ non \_ subsd**
</dt> <dd> <dl> <dt>

137 (0x89)
</dt> <dt>



Il sistema ha tentato di eliminare la sostituzione di un'unità che non viene sostituita.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**errore \_ durante il join \_ \_**
</dt> <dd> <dl> <dt>

138 (0x8A)
</dt> <dt>



Il sistema ha tentato di aggiungere un'unità a una directory in un'unità unita in join.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERRORE \_ da SUBST \_ a \_ SUBST**
</dt> <dd> <dl> <dt>

139 (0x8B)
</dt> <dt>



Il sistema ha tentato di sostituire un'unità con una directory in un'unità sostituita.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**errore durante il \_ join \_ a \_ SUBST**
</dt> <dd> <dl> <dt>

140 (0x8C)
</dt> <dt>



Il sistema ha tentato di aggiungere un'unità a una directory in un'unità sostituita.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERRORE \_ SUBST \_ da \_ unire**
</dt> <dd> <dl> <dt>

141 (0x8D)
</dt> <dt>



Il sistema ha tentato di eseguire il SUBSt di un'unità in una directory in un'unità unita in join.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**ERRORE \_ nell' \_ unità occupata**
</dt> <dd> <dl> <dt>

142 (0x8E)
</dt> <dt>



Il sistema non è in grado di eseguire un JOIN o un oggetto Subs in questo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERRORE della \_ stessa \_ unità**
</dt> <dd> <dl> <dt>

143 (0x8F)
</dt> <dt>



Il sistema non è in grado di aggiungere o sostituire un'unità con o per una directory nella stessa unità.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERRORE \_ dir \_ non \_ radice**
</dt> <dd> <dl> <dt>

144 (0x90)
</dt> <dt>



La directory non è una sottodirectory della directory radice.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**\_dir errore \_ non \_ vuota**
</dt> <dd> <dl> <dt>

145 (0x91)
</dt> <dt>



La directory non è vuota.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**ERRORE \_ è \_ un \_ percorso SUBST**
</dt> <dd> <dl> <dt>

146 (0x92)
</dt> <dt>



Il percorso specificato è in uso in un sostituto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**ERRORE \_ nel \_ percorso di join \_**
</dt> <dd> <dl> <dt>

147 (0x93)
</dt> <dt>



Sono disponibili risorse insufficienti per elaborare il comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**\_percorso errore \_ occupato**
</dt> <dd> <dl> <dt>

148 (0x94)
</dt> <dt>



Impossibile utilizzare il percorso specificato in questo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**ERRORE \_ è \_ la \_ destinazione SUBST**
</dt> <dd> <dl> <dt>

149 (0x95)
</dt> <dt>



È stato effettuato un tentativo di aggiunta o sostituzione di un'unità per la quale una directory nell'unità è la destinazione di un sostituto precedente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**\_traccia di sistema degli errori \_**
</dt> <dd> <dl> <dt>

150 (0x96)
</dt> <dt>



Le informazioni di traccia di sistema non sono state specificate nel file di CONFIG.SYS o la traccia non è consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**ERRORE \_ \_ numero eventi non validi \_**
</dt> <dd> <dl> <dt>

151 (0x97)
</dt> <dt>



Il numero di eventi semaforo specificati per DosMuxSemWait non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERRORE di un \_ numero eccessivo di \_ \_ MUXWAITERS**
</dt> <dd> <dl> <dt>

152 (0x98)
</dt> <dt>



DosMuxSemWait non è stato eseguito; troppi semafori sono già impostati.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**ERRORE \_ di \_ formato elenco non valido \_**
</dt> <dd> <dl> <dt>

153 (0x99)
</dt> <dt>



L'elenco DosMuxSemWait non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**\_etichetta errore \_ troppo \_ lungo**
</dt> <dd> <dl> <dt>

154 (0x9A)
</dt> <dt>



L'etichetta di volume immessa supera il limite di caratteri dell'etichetta della file system di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERRORE di un \_ numero eccessivo di \_ \_ TCBs**
</dt> <dd> <dl> <dt>

155 (0x9B)
</dt> <dt>



Non è possibile creare un altro thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**\_segnalazione errori \_ rifiutata**
</dt> <dd> <dl> <dt>

156 (0x9C)
</dt> <dt>



Il processo del destinatario ha rifiutato il segnale.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERRORE \_ eliminato**
</dt> <dd> <dl> <dt>

157 (0x9D)
</dt> <dt>



Il segmento è già stato scartato e non può essere bloccato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERRORE \_ non \_ bloccato**
</dt> <dd> <dl> <dt>

158 (0x9E)
</dt> <dt>



Il segmento è già sbloccato.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ERRORE \_ \_ addr THREADID \_ errato**
</dt> <dd> <dl> <dt>

159 (0x9F)
</dt> <dt>



L'indirizzo per l'ID del thread non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERRORI \_ argomenti non validi \_**
</dt> <dd> <dl> <dt>

160 (messaggi 0XA0)
</dt> <dt>



Uno o più argomenti non sono corretti.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**\_ \_ nome percorso errato errore**
</dt> <dd> <dl> <dt>

161 (0xA1)
</dt> <dt>



Il percorso specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**\_segnalazione errori \_ in sospeso**
</dt> <dd> <dl> <dt>

162 (0xA2)
</dt> <dt>



Un segnale è già in sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERRORE \_ massimo \_ THRDS \_ raggiunto**
</dt> <dd> <dl> <dt>

164 (0xA4)
</dt> <dt>



Non è possibile creare altri thread nel sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**\_blocco errore \_ non riuscito**
</dt> <dd> <dl> <dt>

167 (0xA7)
</dt> <dt>



Non è possibile bloccare un'area di un file.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERRORE \_ occupato**
</dt> <dd> <dl> <dt>

170 (0xAA)
</dt> <dt>



La risorsa richiesta è in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**\_supporto dei dispositivi \_ con errori \_ in \_ corso**
</dt> <dd> <dl> <dt>

171 (0xAB)
</dt> <dt>



Il rilevamento del supporto del comando del dispositivo è in corso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERRORE di \_ annullamento della \_ violazione**
</dt> <dd> <dl> <dt>

173 (0xAD)
</dt> <dt>



Richiesta di blocco non in attesa per l'area di annullamento specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERRORE \_ blocchi atomici \_ \_ non \_ supportati**
</dt> <dd> <dl> <dt>

174 (0xAE)
</dt> <dt>



Il file system non supporta le modifiche atomiche al tipo di blocco.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**ERRORE \_ \_ numero di segmento non valido \_**
</dt> <dd> <dl> <dt>

180 (0xB4)
</dt> <dt>



Il sistema ha rilevato un numero di segmento non corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERRORE \_ \_ ordinale non valido**
</dt> <dd> <dl> <dt>

182 (0xB6)
</dt> <dt>



Il sistema operativo non è in grado di eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**ERRORE \_ già \_ esistente**
</dt> <dd> <dl> <dt>

183 (0xB7)
</dt> <dt>



Impossibile creare un file, se il file esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERRORE \_ \_ numero di flag non valido \_**
</dt> <dd> <dl> <dt>

186 (0xBA)
</dt> <dt>



Il flag passato non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERRORE \_ sem \_ non \_ trovato**
</dt> <dd> <dl> <dt>

187 (0xBB)
</dt> <dt>



Il nome del semaforo di sistema specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**ERRORE \_ di \_ avvio di CODESEG non valido \_**
</dt> <dd> <dl> <dt>

188 (0xBC)
</dt> <dt>



Il sistema operativo non è in grado di eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERRORE \_ STACKSEG non valido \_**
</dt> <dd> <dl> <dt>

189 (0xBD)
</dt> <dt>



Il sistema operativo non è in grado di eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERRORE \_ MODULETYPE non valido \_**
</dt> <dd> <dl> <dt>

190 (0xBE)
</dt> <dt>



Il sistema operativo non è in grado di eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERRORE \_ di \_ firma exe non valida \_**
</dt> <dd> <dl> <dt>

191 (0xBF)
</dt> <dt>



Impossibile eseguire %1 in modalità Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERRORE del file \_ exe \_ contrassegnato come \_ non valido**
</dt> <dd> <dl> <dt>

192 (0xC0)
</dt> <dt>



Il sistema operativo non è in grado di eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERRORE \_ nel \_ formato exe errato \_**
</dt> <dd> <dl> <dt>

193 (0xC1)
</dt> <dt>



%1 non è un'applicazione Win32 valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**Errore durante l' \_ iterazione \_ dei dati \_ supera \_ 64K**
</dt> <dd> <dl> <dt>

194 (0xC2)
</dt> <dt>



Il sistema operativo non è in grado di eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERRORE \_ MINALLOCSIZE non valido \_**
</dt> <dd> <dl> <dt>

195 (0xC3)
</dt> <dt>



Il sistema operativo non è in grado di eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERRORE \_ DYNLINK \_ dall' \_ anello non valido \_**
</dt> <dd> <dl> <dt>

196 (0xC4)
</dt> <dt>



Il sistema operativo non è in grado di eseguire questo programma applicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERRORE \_ IOPL \_ non \_ abilitato**
</dt> <dd> <dl> <dt>

197 (0xC5)
</dt> <dt>



Il sistema operativo non è attualmente configurato per l'esecuzione dell'applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERRORE \_ SEGDPL non valido \_**
</dt> <dd> <dl> <dt>

198 (0xC6)
</dt> <dt>



Il sistema operativo non è in grado di eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**ERRORE \_ AUTODATASEG \_ supera \_ 64K**
</dt> <dd> <dl> <dt>

199 (0xC7)
</dt> <dt>



Il sistema operativo non è in grado di eseguire questo programma applicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**Il \_ RING2SEG di errore \_ deve \_ essere \_ mobile**
</dt> <dd> <dl> <dt>

200 (0xC8)
</dt> <dt>



Il segmento di codice non può essere maggiore o uguale a 64K.


</dt> </dl> </dd> <dt>

<span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERRORE \_ \_ XEEDS catena \_ reloc \_ SEGLIM**
</dt> <dd> <dl> <dt>

201 (0xC9)
</dt> <dt>



Il sistema operativo non è in grado di eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERRORE \_ INFLOOP \_ nella \_ \_ catena reloc**
</dt> <dd> <dl> <dt>

202 (0xCA)
</dt> <dt>



Il sistema operativo non è in grado di eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERRORE \_ ENVVAR \_ non \_ trovato**
</dt> <dd> <dl> <dt>

203 (0xCB)
</dt> <dt>



Il sistema non è riuscito a trovare l'opzione di ambiente immessa.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERRORE \_ nessun \_ segnale \_ inviato**
</dt> <dd> <dl> <dt>

205 (0xCD)
</dt> <dt>



Nessun processo nel sottoalbero dei comandi dispone di un gestore di segnale.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERRORE del \_ nome file \_ EXCED \_ Range**
</dt> <dd> <dl> <dt>

206 (0xCE)
</dt> <dt>



Il nome file o l'estensione è troppo lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**ERRORE \_ RING2 \_ Stack \_ in \_ uso**
</dt> <dd> <dl> <dt>

207 (0xCF)
</dt> <dt>



Lo stack Ring 2 è in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**ERRORE \_ meta di \_ espansione \_ troppo \_ lungo**
</dt> <dd> <dl> <dt>

208 (0xD0)
</dt> <dt>



I caratteri di nome file globali, \* o?, vengono immessi in modo errato o sono stati specificati troppi caratteri di nome file globali.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**ERRORE \_ \_ numero segnale non valido \_**
</dt> <dd> <dl> <dt>

209 (0xD1)
</dt> <dt>



Il segnale inviato non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**THREAD di errore \_ \_ 1 \_ inattivo**
</dt> <dd> <dl> <dt>

210 (0xD2)
</dt> <dt>



Impossibile impostare il gestore del segnale.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERRORE \_ bloccato**
</dt> <dd> <dl> <dt>

212 (0xD4)
</dt> <dt>



Il segmento è bloccato e non può essere riallocato.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERRORE di un \_ numero eccessivo di \_ \_ moduli**
</dt> <dd> <dl> <dt>

214 (0xD6)
</dt> <dt>



Troppi moduli di collegamento dinamico collegati al programma o al modulo a collegamento dinamico.


</dt> </dl> </dd> <dt>

<span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**\_annidamento errori \_ non \_ consentito**
</dt> <dd> <dl> <dt>

215 (0xD7)
</dt> <dt>



Impossibile annidare le chiamate a LoadModule.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**\_tipo di computer exe errore non \_ \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

216 (0xD8)
</dt> <dt>



Questa versione di %1 non è compatibile con la versione di Windows in esecuzione. Controllare le informazioni di sistema del computer e contattare l'autore del software.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**ERRORE \_ exe \_ non è possibile \_ modificare il \_ \_ file binario firmato**
</dt> <dd> <dl> <dt>

217 (0xD9)
</dt> <dt>



Il file di immagine %1 è firmato. Impossibile modificarlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**ERRORE \_ exe \_ non è possibile \_ modificare il \_ \_ \_ file binario con firma complessa**
</dt> <dd> <dl> <dt>

218 (0xDA)
</dt> <dt>



Il file di immagine %1 è firmato con firma sicura, non è possibile modificarlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**FILE di errore \_ \_ Estratto \_**
</dt> <dd> <dl> <dt>

220 (0xDC)
</dt> <dt>



Il file è stato estratto o bloccato per la modifica da un altro utente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**ERRORE di \_ checkout \_ obbligatorio**
</dt> <dd> <dl> <dt>

221 (0xDD)
</dt> <dt>



Il file deve essere estratto prima di salvare le modifiche.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERRORE \_ \_ tipo di file non valido \_**
</dt> <dd> <dl> <dt>

222 (0xDE)
</dt> <dt>



Il tipo di file salvato o recuperato è stato bloccato.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**FILE di errore \_ \_ troppo \_ grande**
</dt> <dd> <dl> <dt>

223 (0xDF)
</dt> <dt>



Le dimensioni del file superano il limite consentito e non possono essere salvate.


</dt> </dl> </dd> <dt>

<span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**\_autorizzazione moduli di errore \_ \_ obbligatoria**
</dt> <dd> <dl> <dt>

224 (0xE0)
</dt> <dt>



Accesso negato. Prima di aprire i file in questo percorso, è necessario innanzitutto aggiungere il sito Web all'elenco siti attendibili, passare al sito Web e selezionare l'opzione per l'accesso automatico.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**ERRORE \_ virus \_ infetto**
</dt> <dd> <dl> <dt>

225 (0xE1)
</dt> <dt>



L'operazione non è stata completata perché il file contiene un virus o software potenzialmente indesiderato.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**ERRORE \_ virus \_ eliminato**
</dt> <dd> <dl> <dt>

226 (0xE2)
</dt> <dt>



Questo file contiene un virus o software potenzialmente indesiderato e non può essere aperto. A causa della natura di questo virus o di software potenzialmente indesiderato, il file è stato rimosso da questo percorso.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**PIPE di errore \_ \_ locale**
</dt> <dd> <dl> <dt>

229 (0xE5)
</dt> <dt>



La pipe è locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**PIPE errore non \_ valida \_**
</dt> <dd> <dl> <dt>

230 (0xE6)
</dt> <dt>



Lo stato della pipe non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**PIPE di errore \_ \_ occupata**
</dt> <dd> <dl> <dt>

231 (0xE7)
</dt> <dt>



Tutte le istanze di pipe sono occupate.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERRORE \_ nessun \_ dato**
</dt> <dd> <dl> <dt>

232 (0xE8)
</dt> <dt>



La pipe verrà chiusa.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**PIPE degli errori \_ \_ non \_ connessa**
</dt> <dd> <dl> <dt>

233 (0xE9)
</dt> <dt>



Nessun processo è sull'altra estremità della pipe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERRORE di \_ più \_ dati**
</dt> <dd> <dl> <dt>

234 (0xEA)
</dt> <dt>



sono disponibili più dati.


</dt> </dl> </dd> <dt>

<span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERRORE \_ VC \_ disconnesso**
</dt> <dd> <dl> <dt>

240 (0xF0)
</dt> <dt>



La sessione è stata annullata.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERRORE \_ \_ nome EA non valido \_**
</dt> <dd> <dl> <dt>

254 (0xFE)
</dt> <dt>



Il nome dell'attributo esteso specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**\_elenco EA \_ errore \_ incoerente**
</dt> <dd> <dl> <dt>

255 (0xFF)
</dt> <dt>



Gli attributi estesi sono incoerenti.


</dt> </dl> </dd> <dt>

<span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**TIMEOUT di attesa \_**
</dt> <dd> <dl> <dt>

258 (0x102)
</dt> <dt>



Tempo di attesa scaduto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERRORE \_ nessun \_ altro \_ elemento**
</dt> <dd> <dl> <dt>

259 (0x103)
</dt> <dt>



Dati disponibili esauriti.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**ERRORE \_ di \_ copia**
</dt> <dd> <dl> <dt>

266 (0x10A)
</dt> <dt>



Impossibile utilizzare le funzioni di copia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**Directory degli errori \_**
</dt> <dd> <dl> <dt>

267 (0x10B)
</dt> <dt>



Il nome della directory non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERRORE \_ EAS non \_ \_ adatto**
</dt> <dd> <dl> <dt>

275 (0x113)
</dt> <dt>



Gli attributi estesi non rientravano nel buffer.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**ERRORE \_ \_ file EA \_ danneggiato**
</dt> <dd> <dl> <dt>

276 (0x114)
</dt> <dt>



Il file di attributo esteso nel file system montato è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERRORE \_ \_ tabella EA \_ completa**
</dt> <dd> <dl> <dt>

277 (0x115)
</dt> <dt>



Il file di tabella dell'attributo esteso è pieno.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERRORE \_ \_ handle EA non valido \_**
</dt> <dd> <dl> <dt>

278 (0x116)
</dt> <dt>



L'handle di attributo esteso specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERRORE \_ EAS \_ non \_ supportato**
</dt> <dd> <dl> <dt>

282 (0x11A)
</dt> <dt>



Il file system montato non supporta gli attributi estesi.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ERRORE \_ non \_ proprietario**
</dt> <dd> <dl> <dt>

288 (0x120)
</dt> <dt>



Tentativo di rilascio di mutex non di proprietà del chiamante.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERRORE di un \_ numero eccessivo di \_ \_ post**
</dt> <dd> <dl> <dt>

298 (0x12A)
</dt> <dt>



Sono stati apportati troppi post a un semaforo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERRORE \_ di \_ copia parziale**
</dt> <dd> <dl> <dt>

299 (0x12B)
</dt> <dt>



Solo una parte di una richiesta ReadProcessMemory o WriteProcessMemory è stata completata.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERRORE \_ blocco opportunistico \_ non \_ concesso**
</dt> <dd> <dl> <dt>

300 (0x12C)
</dt> <dt>



La richiesta blocco opportunistico è stata negata.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERRORE \_ del \_ protocollo blocco opportunistico non valido \_**
</dt> <dd> <dl> <dt>

301 (0x12D)
</dt> <dt>



Il sistema ha ricevuto un riconoscimento blocco opportunistico non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**disco di errore \_ \_ troppo \_ frammentato**
</dt> <dd> <dl> <dt>

302 (0x12E)
</dt> <dt>



Il volume è troppo frammentato per completare questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERRORE di \_ eliminazione \_ in sospeso**
</dt> <dd> <dl> <dt>

303 (0x12F)
</dt> <dt>



Non è possibile aprire il file perché è in fase di eliminazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERRORE \_ incompatibile \_ con \_ l' \_ \_ \_ impostazione del registro di sistema nome breve globale \_**
</dt> <dd> <dl> <dt>

304 (0x130)
</dt> <dt>



Le impostazioni nome breve potrebbero non essere modificate in questo volume a causa dell'impostazione globale del registro di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**\_nomi brevi \_ \_ di errore non \_ abilitati \_ nel \_ volume**
</dt> <dd> <dl> <dt>

305 (0x131)
</dt> <dt>



I nomi brevi non sono abilitati in questo volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**il \_ flusso di sicurezza degli errori \_ \_ è \_ incoerente**
</dt> <dd> <dl> <dt>

306 (0x132)
</dt> <dt>



Il flusso di sicurezza per il volume specificato è in uno stato incoerente. Eseguire CHKDSK nel volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERRORE \_ di \_ intervallo di blocco non valido \_**
</dt> <dd> <dl> <dt>

307 (0x133)
</dt> <dt>



Impossibile elaborare un'operazione di blocco file richiesta a causa di un intervallo di byte non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**\_sottosistema immagine errore \_ \_ non \_ presente**
</dt> <dd> <dl> <dt>

308 (0x134)
</dt> <dt>



Il sottosistema necessario per supportare il tipo di immagine non è presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**GUID della notifica di errore \_ \_ \_ già \_ definito**
</dt> <dd> <dl> <dt>

309 (0x135)
</dt> <dt>



Al file specificato è già associato un GUID di notifica.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERRORE \_ del \_ gestore di eccezioni non valido \_**
</dt> <dd> <dl> <dt>

310 (0x136)
</dt> <dt>



È stata rilevata una routine del gestore di eccezioni non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**\_privilegi duplicati errore \_**
</dt> <dd> <dl> <dt>

311 (0x137)
</dt> <dt>



Sono stati specificati privilegi duplicati per il token.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERRORE \_ nessun \_ intervallo \_ elaborato**
</dt> <dd> <dl> <dt>

312 (0x138)
</dt> <dt>



Non è stato possibile elaborare intervalli per l'operazione specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERRORE \_ non \_ consentito \_ nel \_ file di sistema \_**
</dt> <dd> <dl> <dt>

313 (0x139)
</dt> <dt>



Operazione non consentita su un file interno file system.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**\_risorse disco di errore \_ \_ esaurite**
</dt> <dd> <dl> <dt>

314 (0x13A)
</dt> <dt>



Le risorse fisiche di questo disco sono esaurite.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**ERRORE \_ di \_ token non valido**
</dt> <dd> <dl> <dt>

315 (0x13B)
</dt> <dt>



Il token che rappresenta i dati non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**funzionalità del dispositivo di errore \_ \_ \_ non \_ supportata**
</dt> <dd> <dl> <dt>

316 (0x13C)
</dt> <dt>



Il dispositivo non supporta la funzionalità comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**ERRORE \_ il \_ Mid \_ non \_ trovato**
</dt> <dd> <dl> <dt>

317 (0x13D)
</dt> <dt>



Impossibile trovare il testo del messaggio per il numero di messaggio 0x %1 nel file di messaggio per %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**\_ambito errore \_ non \_ trovato**
</dt> <dd> <dl> <dt>

318 (0x13E)
</dt> <dt>



L'ambito specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**ERRORE \_ ambito non definito \_**
</dt> <dd> <dl> <dt>

319 (0x13F)
</dt> <dt>



Il criterio di accesso centrale specificato non è definito nel computer di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**ERRORE \_ limite non valido \_**
</dt> <dd> <dl> <dt>

320 (0x140)
</dt> <dt>



I criteri di accesso centrale ottenuti da Active Directory non sono validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**ERRORE \_ dispositivo non \_ raggiungibile**
</dt> <dd> <dl> <dt>

321 (0x141)
</dt> <dt>



Il dispositivo è irraggiungibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**ERRORE \_ dispositivo \_ Nessuna \_ risorsa**
</dt> <dd> <dl> <dt>

322 (0x142)
</dt> <dt>



Il dispositivo di destinazione non dispone di risorse sufficienti per completare l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**errore di \_ checksum dei dati errore \_ \_**
</dt> <dd> <dl> <dt>

323 (0x143)
</dt> <dt>



Si è verificato un errore di checksum di integrità dei dati. I dati nel flusso di file sono danneggiati.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERRORE \_ \_ \_ operazione EA kernel intermista \_**
</dt> <dd> <dl> <dt>

324 (0x144)
</dt> <dt>



È stato effettuato un tentativo di modificare un KERNEL e un attributo esteso normale (EA) nella stessa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**Trim a livello di file di errore \_ \_ \_ \_ non \_ supportato**
</dt> <dd> <dl> <dt>

326 (0x146)
</dt> <dt>



Il dispositivo non supporta il TRIM a livello di file.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**\_violazione di \_ allineamento \_ offset errori**
</dt> <dd> <dl> <dt>

327 (0x147)
</dt> <dt>



Il comando ha specificato un offset dei dati non allineato alla granularità/allineamento del dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**ERRORE \_ \_ nel campo \_ dell' \_ \_ elenco dei parametri**
</dt> <dd> <dl> <dt>

328 (0x148)
</dt> <dt>



Il comando ha specificato un campo non valido nell'elenco di parametri.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**\_operazione \_ di errore in \_ corso**
</dt> <dd> <dl> <dt>

329 (0x149)
</dt> <dt>



È attualmente in corso un'operazione con il dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERRORE \_ nel \_ percorso del dispositivo errato \_**
</dt> <dd> <dl> <dt>

330 (0x14A)
</dt> <dt>



È stato effettuato un tentativo di inviare il comando tramite un percorso non valido al dispositivo di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERRORE di un \_ numero eccessivo di \_ \_ descrittori**
</dt> <dd> <dl> <dt>

331 (0x14B)
</dt> <dt>



Il comando ha specificato un numero di descrittori che hanno superato il valore massimo supportato dal dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**ERRORE di \_ pulizia \_ dati \_ disabilitato**
</dt> <dd> <dl> <dt>

332 (0x14C)
</dt> <dt>



Lo scrub è disabilitato nel file specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**ERRORE \_ di \_ archiviazione non ridondante \_**
</dt> <dd> <dl> <dt>

333 (0x14D)
</dt> <dt>



Il dispositivo di archiviazione non fornisce ridondanza.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**il \_ file residente di errore \_ \_ non è \_ supportato**
</dt> <dd> <dl> <dt>

334 (0x14E)
</dt> <dt>



Un'operazione non è supportata in un file residente.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**ERRORE \_ \_ file compresso \_ non \_ supportato**
</dt> <dd> <dl> <dt>

335 (0x14F)
</dt> <dt>



Un'operazione non è supportata in un file compresso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**Directory degli errori \_ \_ non \_ supportata**
</dt> <dd> <dl> <dt>

336 (0x150)
</dt> <dt>



Un'operazione non è supportata in una directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**ERRORE \_ \_ di lettura \_ dalla \_ copia**
</dt> <dd> <dl> <dt>

337 (0x151)
</dt> <dt>



Impossibile leggere la copia specificata dei dati richiesti.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**errore durante il \_ \_ riavvio di NoAction \_**
</dt> <dd> <dl> <dt>

350 (0x15E)
</dt> <dt>



Non è stata eseguita alcuna azione perché è necessario riavviare il sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**ERRORE \_ di \_ arresto**
</dt> <dd> <dl> <dt>

351 (0x15F)
</dt> <dt>



L'operazione di arresto non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**errore durante il \_ \_ riavvio**
</dt> <dd> <dl> <dt>

352 (0x160)
</dt> <dt>



Operazione di riavvio non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**\_numero massimo di sessioni di errore \_ \_ raggiunto**
</dt> <dd> <dl> <dt>

353 (0x161)
</dt> <dt>



È stato raggiunto il numero massimo di sessioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**\_modalità thread di errore \_ già in \_ \_ background**
</dt> <dd> <dl> <dt>

400 (0x190)
</dt> <dt>



Il thread è già in modalità di elaborazione in background.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**\_modalità thread di errore \_ non in \_ \_ background**
</dt> <dd> <dl> <dt>

401 (0x191)
</dt> <dt>



Il thread non è in modalità di elaborazione in background.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**modalità di elaborazione degli errori \_ \_ già in \_ \_ background**
</dt> <dd> <dl> <dt>

402 (0x192)
</dt> <dt>



Il processo è già in modalità di elaborazione in background.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**\_modalità elaborazione \_ errori \_ non in \_ background**
</dt> <dd> <dl> <dt>

403 (0x193)
</dt> <dt>



Il processo non è in modalità di elaborazione in background.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERRORE \_ indirizzo non valido \_**
</dt> <dd> <dl> <dt>

487 (0x1E7)
</dt> <dt>



Tentativo di accedere a un indirizzo non valido.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>WinError. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore di sistema](system-error-codes.md)
</dt> </dl>

 

 




