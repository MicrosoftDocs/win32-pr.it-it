---
description: Descrive i codici di errore 0-499 definiti nel file di intestazione WinError.h ed è destinato agli sviluppatori.
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: Codici di errore di sistema (0-499) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: a9eddec2baf098f62bb1c0ad88e632360807e7f3fd0ea045f2565587f13e93a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405650"
---
# <a name="system-error-codes-0-499"></a>Codici di errore di sistema (0-499)

> [!NOTE]
> Queste informazioni sono destinate agli sviluppatori che ese tracciano errori di sistema. Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella [pagina Codici di](system-error-codes.md) errore.

L'elenco seguente descrive i [codici di errore di sistema](system-error-codes.md) (errori da 0 a 499). Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la [**funzione FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il flag **FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_SUCCESS"></span><span id="error_success"></span>**ERRORE \_ RIUSCITO**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Operazione riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**ERRORE \_ FUNZIONE NON \_ VALIDA**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Funzione non corretta.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**FILE \_ DEGLI ERRORI NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Non è possibile trovare il file specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**PERCORSO \_ ERRORE \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



impossibile trovare il percorso specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERRORE \_ TROPPI \_ FILE \_ \_ APERTI**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Il sistema non è in grado di aprire il file.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERRORE \_ DI \_ ACCESSO NEGATO**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



Accesso negato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERRORE \_ HANDLE NON \_ VALIDO**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



Handle non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**ERROR \_ PIÙ \_ CESTINO**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



I blocchi di controllo di archiviazione sono stati distrutti.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERRORE \_ MEMORIA \_ \_ INSUFFICIENTE**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Risorse di memoria insufficienti per elaborare il comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**ERRORE \_ BLOCCO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



L'indirizzo del blocco di controllo di archiviazione non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERRORE \_ AMBIENTE \_ NON GESTITO**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



L'ambiente non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**ERRORE \_ NEL FORMATO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



Tentativo di caricare un programma con un formato non corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERRORE ACCESSO \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



Il codice di accesso non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERRORE \_ DATI NON \_ VALIDI**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



I dati non sono validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERRORE \_ OUTOFMEMORY**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



Spazio di archiviazione insufficiente per completare questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERRORE UNITÀ \_ NON \_ VALIDA**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



Impossibile trovare l'unità specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERRORE \_ NELLA \_ DIRECTORY CORRENTE**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Impossibile rimuovere la directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERRORE \_ NON LO STESSO \_ \_ DISPOSITIVO**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



Il sistema non è in grado di spostare il file in un'altra unità disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERRORE \_ NESSUN \_ ALTRO \_ FILE**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



Non sono presenti altri file.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**PROTEZIONE \_ DA ERRORI DI \_ SCRITTURA**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



Il supporto è protetto da scrittura.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**UNITÀ \_ NON \_ ERTA DI ERRORE**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



Il sistema non riesce a trovare il dispositivo specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERRORE \_ NON \_ PRONTO**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



Il dispositivo non è pronto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERROR \_ BAD \_ COMMAND**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



Il dispositivo non riconosce il comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRC"></span><span id="error_crc"></span>**ERRORE \_ CRC**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



Errore dei dati (controllo di ridondanza ciclico).


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERRORE \_ LUNGHEZZA \_ NON VALIDA**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



Il programma ha eseguito un comando ma la lunghezza del comando non è corretta.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK"></span><span id="error_seek"></span>**ERROR \_ SEEK**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



L'unità non è in grado di individuare un'area o una traccia specifica sul disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERRORE \_ NON \_ DOS \_ DISK**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



Impossibile accedere al disco o al dischetto specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**SETTORE \_ DEGLI ERRORI NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



L'unità non è in grado di trovare il settore richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERRORE \_ \_ OUT OF \_ PAPER**
</dt> <dd> <dl> <dt>

28 (0x1C)
</dt> <dt>



La stampante è senza carta.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**ERRORE \_ DI SCRITTURA \_ ERRORE**
</dt> <dd> <dl> <dt>

29 (0x1D)
</dt> <dt>



Il sistema non è in grado di scrivere nel dispositivo specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**ERRORE \_ DI \_ LETTURA ERRORE**
</dt> <dd> <dl> <dt>

30 (0x1E)
</dt> <dt>



Il sistema non è in grado di leggere dal dispositivo specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**ERRORE \_ GEN \_ ERRORE**
</dt> <dd> <dl> <dt>

31 (0x1F)
</dt> <dt>



Un dispositivo collegato al sistema non funziona.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**VIOLAZIONE \_ DI CONDIVISIONE \_ DEGLI ERRORI**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Il processo non può accedere al file perché è in uso da un altro processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**VIOLAZIONE \_ DEL BLOCCO \_ DEGLI ERRORI**
</dt> <dd> <dl> <dt>

33 (0x21)
</dt> <dt>



Il processo non può accedere al file perché un altro processo ne ha bloccato una parte.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERRORE \_ DISCO \_ ERRATO**
</dt> <dd> <dl> <dt>

34 (0x22)
</dt> <dt>



Il dischetto errato si trova nell'unità. Inserire %2 (numero di serie del volume: %3) nell'unità %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**BUFFER \_ DI CONDIVISIONE DEGLI ERRORI \_ \_ SUPERATO**
</dt> <dd> <dl> <dt>

36 (0x24)
</dt> <dt>



Troppi file aperti per la condivisione.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**GESTIONE \_ DEGLI \_ ERRORI EOF**
</dt> <dd> <dl> <dt>

38 (0x26)
</dt> <dt>



Raggiunto la fine del file.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**DISCO \_ DI GESTIONE DEGLI ERRORI \_ \_ PIENO**
</dt> <dd> <dl> <dt>

39 (0x27)
</dt> <dt>



Disco pieno.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERRORE \_ NON \_ SUPPORTATO**
</dt> <dd> <dl> <dt>

50 (0x32)
</dt> <dt>



La richiesta non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERRORE \_ REM \_ NOT \_ LIST**
</dt> <dd> <dl> <dt>

51 (0x33)
</dt> <dt>



Windows impossibile trovare il percorso di rete. Verificare che il percorso di rete sia corretto e che il computer di destinazione non sia occupato o spento. Se Windows il percorso di rete, contattare l'amministratore di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**ERRORE \_ NOME DUP \_**
</dt> <dd> <dl> <dt>

52 (0x34)
</dt> <dt>



Non si è connessi perché esiste un nome duplicato nella rete. Se si partecipa a un dominio, passare a Sistema in Pannello di controllo per modificare il nome del computer e riprovare. Se si partecipa a un gruppo di lavoro, scegliere un altro nome di gruppo di lavoro.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERRORE \_ \_ NETPATH NON VALIDO**
</dt> <dd> <dl> <dt>

53 (0x35)
</dt> <dt>



Impossibile trovare il percorso di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERRORE \_ RETE \_ OCCUPATA**
</dt> <dd> <dl> <dt>

54 (0x36)
</dt> <dt>



La rete è occupata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**ERRORE \_ DEV \_ NON \_ ESISTENTE**
</dt> <dd> <dl> <dt>

55 (0x37)
</dt> <dt>



La risorsa o il dispositivo di rete specificato non è più disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERRORE \_ TROPPI \_ \_ COMANDI**
</dt> <dd> <dl> <dt>

56 (0x38)
</dt> <dt>



È stato raggiunto il limite di comandi del BIOS di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERRORE \_ ADAP \_ HDW \_ ERR**
</dt> <dd> <dl> <dt>

57 (0x39)
</dt> <dt>



Si è verificato un errore hardware della scheda di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERRORE \_ DI RETE \_ \_ RESP NON ERTA**
</dt> <dd> <dl> <dt>

58 (0x3A)
</dt> <dt>



Il server specificato non può effettuare l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERRORE \_ UNEXP \_ NET \_ ERR**
</dt> <dd> <dl> <dt>

59 (0x3B)
</dt> <dt>



Si è verificato un errore di rete imprevisto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERRORE \_ \_ REM \_ ADAP NON GRAVE**
</dt> <dd> <dl> <dt>

60 (0x3C)
</dt> <dt>



La scheda remota non è compatibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERRORE \_ PRINTQ \_ FULL**
</dt> <dd> <dl> <dt>

61 (0x3D)
</dt> <dt>



La coda della stampante è piena.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERRORE- \_ SPAZIO \_ DI \_ SPOOLING**
</dt> <dd> <dl> <dt>

62 (0x3E)
</dt> <dt>



Lo spazio per archiviare il file in attesa di stampa non è disponibile nel server.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**STAMPA \_ \_ DELL'ERRORE ANNULLATA**
</dt> <dd> <dl> <dt>

63 (0x3F)
</dt> <dt>



Il file in attesa di stampa è stato eliminato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**ERRORE \_ NETNAME \_ ELIMINATO**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Il nome di rete specificato non è più disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERRORE \_ ACCESSO ALLA RETE \_ \_ NEGATO**
</dt> <dd> <dl> <dt>

65 (0x41)
</dt> <dt>



Accesso alla rete negato.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERRORE \_ TIPO DI SVILUPPO NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

66 (0x42)
</dt> <dt>



Il tipo di risorsa di rete non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERRORE \_ NOME RETE NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

67 (0x43)
</dt> <dt>



Impossibile trovare il nome della rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERRORE \_ TROPPI \_ \_ NOMI**
</dt> <dd> <dl> <dt>

68 (0x44)
</dt> <dt>



È stato superato il limite di nomi per la scheda di rete del computer locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERRORE \_ TROPPI \_ \_ SESS**
</dt> <dd> <dl> <dt>

69 (0x45)
</dt> <dt>



È stato superato il limite di sessione del BIOS di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**CONDIVISIONE \_ DEGLI ERRORI \_ SOSPESA**
</dt> <dd> <dl> <dt>

70 (0x46)
</dt> <dt>



Il server remoto è stato sospeso o è in corso l'avvio.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**ERRORE \_ REQ \_ NOT \_ ACCEP**
</dt> <dd> <dl> <dt>

71 (0x47)
</dt> <dt>



Al momento non è possibile eseguire altre connessioni a questo computer remoto perché sono già presenti tutte le connessioni che il computer può accettare.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**INTERRUZIONE \_ \_ DELL'ERRORE**
</dt> <dd> <dl> <dt>

72 (0x48)
</dt> <dt>



La stampante o il dispositivo disco specificato è stato sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**FILE \_ DI ERRORE \_ ESISTENTE**
</dt> <dd> <dl> <dt>

80 (0x50)
</dt> <dt>



File esistente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**IMPOSSIBILE \_ ESEGUIRE \_ L'ERRORE**
</dt> <dd> <dl> <dt>

82 (0x52)
</dt> <dt>



Impossibile creare la directory o il file.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERRORE \_ NON \_ RIUSCITO I24**
</dt> <dd> <dl> <dt>

83 (0x53)
</dt> <dt>



Errore su INT 24.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**ERRORE \_ \_ \_ ALL'INTERNO DELLE STRUTTURE**
</dt> <dd> <dl> <dt>

84 (0x54)
</dt> <dt>



Archiviazione per elaborare questa richiesta non è disponibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERRORE \_ GIÀ \_ ASSEGNATO**
</dt> <dd> <dl> <dt>

85 (0x55)
</dt> <dt>



Il nome del dispositivo locale è già in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**ERRORE \_ PASSWORD NON \_ VALIDA**
</dt> <dd> <dl> <dt>

86 (0x56)
</dt> <dt>



La password di rete specificata non è corretta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**ERRORE \_ PARAMETRO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

87 (0x57)
</dt> <dt>



Parametro non corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**ERRORE \_ DI SCRITTURA DI \_ \_ RETE**
</dt> <dd> <dl> <dt>

88 (0x58)
</dt> <dt>



Si è verificato un errore di scrittura nella rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**ERRORE \_ SENZA \_ SLOT \_ PROC**
</dt> <dd> <dl> <dt>

89 (0x59)
</dt> <dt>



Il sistema non può avviare un altro processo in questo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERRORE \_ TROPPI \_ \_ SEMAFORI**
</dt> <dd> <dl> <dt>

100 (0x64)
</dt> <dt>



Impossibile creare un altro semaforo di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERRORE \_ EXCL \_ SEM \_ GIÀ DI \_ PROPRIETÀ**
</dt> <dd> <dl> <dt>

101 (0x65)
</dt> <dt>



Il semaforo esclusivo è di proprietà di un altro processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**ERRORE \_ SEM \_ \_ IMPOSTATO**
</dt> <dd> <dl> <dt>

102 (0x66)
</dt> <dt>



Il semaforo è impostato e non può essere chiuso.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERRORE \_ TROPPE \_ RICHIESTE \_ \_ SEM**
</dt> <dd> <dl> <dt>

103 (0x67)
</dt> <dt>



Il semaforo non può essere impostato di nuovo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERRORE \_ NON VALIDO IN FASE DI \_ \_ \_ INTERRUZIONE**
</dt> <dd> <dl> <dt>

104 (0x68)
</dt> <dt>



Impossibile richiedere semafori esclusivi in fase di interruzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERRORE \_ DI SEM \_ OWNER \_ DIED**
</dt> <dd> <dl> <dt>

105 (0x69)
</dt> <dt>



La proprietà precedente di questo semaforo è terminata.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**ERRORE \_ SEM \_ USER \_ LIMIT**
</dt> <dd> <dl> <dt>

106 (0x6A)
</dt> <dt>



Inserire il dischetto per l'unità %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**MODIFICA \_ DEL DISCO DI \_ ERRORE**
</dt> <dd> <dl> <dt>

107 (0x6B)
</dt> <dt>



Il programma è stato arrestato perché non è stato inserito un dischetto alternativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**UNITÀ \_ DI ERRORE \_ BLOCCATA**
</dt> <dd> <dl> <dt>

108 (0x6C)
</dt> <dt>



Il disco è in uso o bloccato da un altro processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERRORE \_ DELLA \_ PIPE INTERROTTA**
</dt> <dd> <dl> <dt>

109 (0x6D)
</dt> <dt>



La pipe è stata terminata.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**ERRORE \_ DI APERTURA NON \_ RIUSCITA**
</dt> <dd> <dl> <dt>

110 (0x6E)
</dt> <dt>



Il sistema non può aprire il dispositivo o il file specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**OVERFLOW \_ DEL BUFFER DEGLI \_ ERRORI**
</dt> <dd> <dl> <dt>

111 (0x6F)
</dt> <dt>



Il nome del file è troppo lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**DISCO \_ DI ERRORE \_ PIENO**
</dt> <dd> <dl> <dt>

112 (0x70)
</dt> <dt>



Lo spazio su disco è insufficiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERRORE \_ NON PIÙ HANDLE DI \_ \_ \_ RICERCA**
</dt> <dd> <dl> <dt>

113 (0x71)
</dt> <dt>



Non sono disponibili altri identificatori di file interni.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERRORE HANDLE \_ DI \_ DESTINAZIONE NON \_ VALIDO**
</dt> <dd> <dl> <dt>

114 (0x72)
</dt> <dt>



L'identificatore di file interno di destinazione non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**ERRORE \_ CATEGORIA NON \_ VALIDA**
</dt> <dd> <dl> <dt>

117 (0x75)
</dt> <dt>



La chiamata IOCTL effettuata dal programma dell'applicazione non è corretta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERRORE - \_ OPZIONE DI VERIFICA NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

118 (0x76)
</dt> <dt>



Il valore del parametro dell'opzione verify-on-write non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERRORE \_ LIVELLO DRIVER NON \_ \_ CORRETTO**
</dt> <dd> <dl> <dt>

119 (0x77)
</dt> <dt>



Il sistema non supporta il comando richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**CHIAMATA \_ DI ERRORE NON \_ \_ IMPLEMENTATA**
</dt> <dd> <dl> <dt>

120 (0x78)
</dt> <dt>



Questa funzione non è supportata in questo sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**ERRORE \_ SEM \_ TIMEOUT**
</dt> <dd> <dl> <dt>

121 (0x79)
</dt> <dt>



Il periodo di timeout del semaforo è scaduto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERRORE \_ BUFFER \_ INSUFFICIENTE**
</dt> <dd> <dl> <dt>

122 (0x7A)
</dt> <dt>



L'area dati passata a una chiamata di sistema è troppo piccola.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**ERRORE \_ NOME NON \_ VALIDO**
</dt> <dd> <dl> <dt>

123 (0x7B)
</dt> <dt>



La sintassi del nome file, del nome della directory o dell'etichetta di volume non è corretta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**LIVELLO \_ DI ERRORE NON \_ VALIDO**
</dt> <dd> <dl> <dt>

124 (0x7C)
</dt> <dt>



Il livello di chiamata di sistema non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERRORE \_ NESSUNA ETICHETTA DI \_ \_ VOLUME**
</dt> <dd> <dl> <dt>

125 (0x7D)
</dt> <dt>



Il disco non ha un'etichetta di volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**ERRORE \_ MOD \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

126 (0x7E)
</dt> <dt>



The specified module could not be found. (E_CSC_SYSTEM_INTERNAL: errore interno. Impossibile caricare il file o l'assembly 'ScopeEngineManaged.dll' o una delle sue dipendenze. Impossibile trovare il modulo specificato.)


</dt> </dl> </dd> <dt>

<span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**ERRORE \_ PROC \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

127 (0x7F)
</dt> <dt>



Impossibile trovare la procedura specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERROR \_ WAIT \_ NO \_ CHILDREN**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Non sono presenti processi figlio da attendere.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**ERRORE \_ FIGLIO \_ NON \_ COMPLETATO**
</dt> <dd> <dl> <dt>

129 (0x81)
</dt> <dt>



Impossibile eseguire l'applicazione %1 in modalità Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**HANDLE \_ DI ACCESSO DIRETTO \_ \_ ERRORI**
</dt> <dd> <dl> <dt>

130 (0x82)
</dt> <dt>



Provare a usare un handle di file per una partizione del disco aperto per un'operazione diversa dall'I/O su disco non elaborato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**ERROR \_ NEGATIVE \_ SEEK**
</dt> <dd> <dl> <dt>

131 (0x83)
</dt> <dt>



Si è tentato di spostare il puntatore del file prima dell'inizio del file.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**RICERCA \_ ERRORI \_ NEL \_ DISPOSITIVO**
</dt> <dd> <dl> <dt>

132 (0x84)
</dt> <dt>



Non è possibile impostare il puntatore del file nel dispositivo o nel file specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**ERRORE NELLA \_ \_ DESTINAZIONE DEL \_ JOIN**
</dt> <dd> <dl> <dt>

133 (0x85)
</dt> <dt>



Non è possibile usare un comando JOIN o SUBST per un'unità che contiene unità unite in precedenza.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**\_L'ERRORE È \_ STATO UNITO**
</dt> <dd> <dl> <dt>

134 (0x86)
</dt> <dt>



Si è tentato di usare un comando JOIN o SUBST in un'unità già unita in join.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**ERROR \_ IS \_ SUBSTED**
</dt> <dd> <dl> <dt>

135 (0x87)
</dt> <dt>



Si è tentato di usare un comando JOIN o SUBST in un'unità che è già stata sostituita.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERRORE \_ NON UNITO IN \_ JOIN**
</dt> <dd> <dl> <dt>

136 (0x88)
</dt> <dt>



Il sistema ha tentato di eliminare l'operazione JOIN di un'unità non unita in join.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERROR \_ NOT \_ SUBSTED**
</dt> <dd> <dl> <dt>

137 (0x89)
</dt> <dt>



Il sistema ha tentato di eliminare la sostituzione di un'unità che non è stata sostituita.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**ERROR \_ JOIN \_ TO \_ JOIN**
</dt> <dd> <dl> <dt>

138 (0x8A)
</dt> <dt>



Il sistema ha tentato di aggiungere un'unità a una directory in un'unità aggiunta.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERROR \_ SUBST \_ TO \_ SUBST**
</dt> <dd> <dl> <dt>

139 (0x8B)
</dt> <dt>



Il sistema ha tentato di sostituire un'unità con una directory in un'unità sostituita.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**ERROR \_ JOIN \_ TO \_ SUBST**
</dt> <dd> <dl> <dt>

140 (0x8C)
</dt> <dt>



Il sistema ha tentato di aggiungere un'unità a una directory in un'unità sostituita.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERROR \_ SUBST \_ TO \_ JOIN**
</dt> <dd> <dl> <dt>

141 (0x8D)
</dt> <dt>



Il sistema ha tentato di convertire un'unità in una directory in un'unità unita.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**UNITÀ \_ CON ERRORE \_ OCCUPATO**
</dt> <dd> <dl> <dt>

142 (0x8E)
</dt> <dt>



Il sistema non è in grado di eseguire un'operazione JOIN o SUBST in questo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERRORE \_ STESSA \_ UNITÀ**
</dt> <dd> <dl> <dt>

143 (0x8F)
</dt> <dt>



Il sistema non può aggiungere o sostituire un'unità a o per una directory nella stessa unità.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERRORE \_ DIR \_ NOT \_ ROOT**
</dt> <dd> <dl> <dt>

144 (0x90)
</dt> <dt>



La directory non è una sottodirectory della directory radice.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**ERRORE \_ DIR \_ NON \_ VUOTO**
</dt> <dd> <dl> <dt>

145 (0x91)
</dt> <dt>



La directory non è vuota.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**ERROR \_ IS \_ SUBST \_ PATH**
</dt> <dd> <dl> <dt>

146 (0x92)
</dt> <dt>



Il percorso specificato viene usato in sostituzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**ERRORE \_ È IL PERCORSO DI \_ \_ JOIN**
</dt> <dd> <dl> <dt>

147 (0x93)
</dt> <dt>



Non sono disponibili risorse sufficienti per elaborare questo comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**PERCORSO \_ ERRORE \_ OCCUPATO**
</dt> <dd> <dl> <dt>

148 (0x94)
</dt> <dt>



Il percorso specificato non può essere usato in questo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**ERROR \_ IS \_ SUBST \_ TARGET**
</dt> <dd> <dl> <dt>

149 (0x95)
</dt> <dt>



È stato effettuato un tentativo di aggiunta o sostituzione di un'unità per cui una directory nell'unità è la destinazione di un sostituzione precedente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**TRACCIA \_ DI SISTEMA DEGLI \_ ERRORI**
</dt> <dd> <dl> <dt>

150 (0x96)
</dt> <dt>



Le informazioni di traccia di sistema non sono specificate nel file CONFIG.SYS oppure la traccia non è consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**ERRORE \_ CONTEGGIO \_ EVENTI NON \_ VALIDI**
</dt> <dd> <dl> <dt>

151 (0x97)
</dt> <dt>



Il numero di eventi semafori specificati per DosMuxSemWait non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERRORE \_ TROPPI \_ \_ MUXWAITER**
</dt> <dd> <dl> <dt>

152 (0x98)
</dt> <dt>



DosMuxSemWait non è stato eseguito. troppi semafori già impostati.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**ERRORE FORMATO \_ ELENCO \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

153 (0x99)
</dt> <dt>



L'elenco DosMuxSemWait non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**ETICHETTA \_ DI ERRORE TROPPO \_ \_ LUNGA**
</dt> <dd> <dl> <dt>

154 (0x9A)
</dt> <dt>



L'etichetta di volume immessa supera il limite di caratteri dell'etichetta del file system.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERRORE \_ TROPPI \_ \_ TCBS**
</dt> <dd> <dl> <dt>

155 (0x9B)
</dt> <dt>



Impossibile creare un altro thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**IL SEGNALE \_ DI ERRORE È STATO \_ RIFIUTATO**
</dt> <dd> <dl> <dt>

156 (0x9C)
</dt> <dt>



Il processo del destinatario ha rifiutato il segnale.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERRORE \_ IGNORATO**
</dt> <dd> <dl> <dt>

157 (0x9D)
</dt> <dt>



Il segmento è già stato eliminato e non può essere bloccato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERRORE \_ NON \_ BLOCCATO**
</dt> <dd> <dl> <dt>

158 (0x9E)
</dt> <dt>



Il segmento è già sbloccato.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ERRORE \_ - \_ THREADID \_ ADDR NON VALIDO**
</dt> <dd> <dl> <dt>

159 (0x9F)
</dt> <dt>



L'indirizzo per l'ID thread non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERRORE \_ ARGOMENTI \_ NON VALIDI**
</dt> <dd> <dl> <dt>

160 (0xA0)
</dt> <dt>



Uno o più argomenti non sono corretti.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERRORE \_ \_ PATHNAME NON VALIDO**
</dt> <dd> <dl> <dt>

161 (0xA1)
</dt> <dt>



Il percorso specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**SEGNALE \_ DI ERRORE IN \_ SOSPESO**
</dt> <dd> <dl> <dt>

162 (0xA2)
</dt> <dt>



Un segnale è già in sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**È \_ STATO RAGGIUNTO IL NUMERO MASSIMO \_ DI ERRORI \_**
</dt> <dd> <dl> <dt>

164 (0xA4)
</dt> <dt>



Non è possibile creare altri thread nel sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**BLOCCO \_ DEGLI ERRORI NON \_ RIUSCITO**
</dt> <dd> <dl> <dt>

167 (0xA7)
</dt> <dt>



Impossibile bloccare un'area di un file.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERRORE \_ OCCUPATO**
</dt> <dd> <dl> <dt>

170 (0xAA)
</dt> <dt>



La risorsa richiesta è in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**ERRORE \_ SUPPORTO DISPOSITIVO IN \_ \_ \_ CORSO**
</dt> <dd> <dl> <dt>

171 (0xAB)
</dt> <dt>



È in corso il rilevamento del supporto dei comandi del dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**VIOLAZIONE \_ \_ DELL'ANNULLAMENTO DELL'ERRORE**
</dt> <dd> <dl> <dt>

173 (0xAD)
</dt> <dt>



Richiesta di blocco non in sospeso per l'area di annullamento fornita.


</dt> </dl> </dd> <dt>

<span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**BLOCCHI \_ \_ ATOMICI DI ERRORE \_ NON \_ SUPPORTATI**
</dt> <dd> <dl> <dt>

174 (0xAE)
</dt> <dt>



Il file system non supporta le modifiche atomiche al tipo di blocco.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**ERRORE \_ NUMERO DI SEGMENTO NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

180 (0xB4)
</dt> <dt>



Il sistema ha rilevato un numero di segmento non corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERRORE \_ \_ ORDINALE NON VALIDO**
</dt> <dd> <dl> <dt>

182 (0xB6)
</dt> <dt>



Il sistema operativo non può eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**\_L'ERRORE ESISTE \_ GIÀ**
</dt> <dd> <dl> <dt>

183 (0xB7)
</dt> <dt>



Impossibile creare un file, se il file esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERRORE \_ NUMERO DI FLAG NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

186 (0xBA)
</dt> <dt>



Il flag passato non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERRORE \_ SEM \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

187 (0xBB)
</dt> <dt>



Impossibile trovare il nome del semaforo di sistema specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**ERRORE \_ CODICI DI AVVIO NON \_ \_ VALIDIEG**
</dt> <dd> <dl> <dt>

188 (0xBC)
</dt> <dt>



Il sistema operativo non può eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERRORE \_ \_ STACKSEG NON VALIDO**
</dt> <dd> <dl> <dt>

189 (0xBD)
</dt> <dt>



Il sistema operativo non può eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERRORE \_ \_ MODULETYPE NON VALIDO**
</dt> <dd> <dl> <dt>

190 (0xBE)
</dt> <dt>



Il sistema operativo non può eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERRORE \_ FIRMA EXE NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

191 (0xBF)
</dt> <dt>



Impossibile eseguire %1 in modalità Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**EXE \_ \_ DELL'ERRORE CONTRASSEGNATO \_ COME NON VALIDO**
</dt> <dd> <dl> <dt>

192 (0xC0)
</dt> <dt>



Il sistema operativo non può eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERRORE \_ FORMATO EXE NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

193 (0xC1)
</dt> <dt>



%1 non è un'applicazione Win32 valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**I \_ DATI \_ ITERATI DI ERRORE \_ SUPERANO \_ 64.000**
</dt> <dd> <dl> <dt>

194 (0xC2)
</dt> <dt>



Il sistema operativo non può eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERRORE \_ \_ MINALLOCSIZE NON VALIDO**
</dt> <dd> <dl> <dt>

195 (0xC3)
</dt> <dt>



Il sistema operativo non può eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERRORE \_ DYNLINK \_ DA ANELLO NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

196 (0xC4)
</dt> <dt>



Il sistema operativo non può eseguire questo programma dell'applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERRORE \_ IOPL \_ NON \_ ABILITATO**
</dt> <dd> <dl> <dt>

197 (0xC5)
</dt> <dt>



Il sistema operativo non è attualmente configurato per eseguire questa applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERRORE \_ \_ SEGDPL NON VALIDO**
</dt> <dd> <dl> <dt>

198 (0xC6)
</dt> <dt>



Il sistema operativo non può eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**ERRORE \_ AUTODATASEG \_ SUPERA \_ 64K**
</dt> <dd> <dl> <dt>

199 (0xC7)
</dt> <dt>



Il sistema operativo non può eseguire questo programma dell'applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**\_L'ERRORE RING2SEG \_ DEVE ESSERE \_ \_ MOVABLE**
</dt> <dd> <dl> <dt>

200 (0xC8)
</dt> <dt>



Il segmento di codice non può essere maggiore o uguale a 64.000.


</dt> </dl> </dd> <dt>

<span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERRORE \_ RELOC \_ CHAIN \_ XEEDS \_ SEGLIM**
</dt> <dd> <dl> <dt>

201 (0xC9)
</dt> <dt>



Il sistema operativo non può eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERRORE \_ INFLOOP \_ NELLA CATENA \_ RELOC \_**
</dt> <dd> <dl> <dt>

202 (0xCA)
</dt> <dt>



Il sistema operativo non può eseguire %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERRORE \_ ENVVAR \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

203 (0xCB)
</dt> <dt>



Il sistema non è stato in grado di trovare l'opzione di ambiente immessa.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERRORE \_ NESSUN \_ SEGNALE \_ INVIATO**
</dt> <dd> <dl> <dt>

205 (0xCD)
</dt> <dt>



Nessun processo nel sottoalbero dei comandi ha un gestore del segnale.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERROR \_ FILENAME \_ EXCED \_ RANGE**
</dt> <dd> <dl> <dt>

206 (0xCE)
</dt> <dt>



Il nome file o l'estensione è troppo lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**STACK \_ RING2 \_ DI ERRORE IN \_ \_ USO**
</dt> <dd> <dl> <dt>

207 (0xCF)
</dt> <dt>



Lo stack dell'anello 2 è in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**ESPANSIONE \_ META ERRORE TROPPO \_ \_ \_ LUNGA**
</dt> <dd> <dl> <dt>

208 (0xD0)
</dt> <dt>



I caratteri globali del nome file, o ?, vengono immessi in modo non corretto o vengono specificati troppi \* caratteri di nome file globali.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**ERRORE \_ NUMERO DI SEGNALE NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

209 (0xD1)
</dt> <dt>



Il segnale inviato non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**THREAD \_ DI \_ ERRORE 1 \_ INATTIVO**
</dt> <dd> <dl> <dt>

210 (0xD2)
</dt> <dt>



Impossibile impostare il gestore del segnale.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERRORE \_ BLOCCATO**
</dt> <dd> <dl> <dt>

212 (0xD4)
</dt> <dt>



Il segmento è bloccato e non può essere riallocato.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERRORE \_ TROPPI \_ \_ MODULI**
</dt> <dd> <dl> <dt>

214 (0xD6)
</dt> <dt>



Troppi moduli a collegamento dinamico sono collegati a questo programma o modulo a collegamento dinamico.


</dt> </dl> </dd> <dt>

<span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**\_ANNIDAMENTO DEGLI ERRORI NON \_ \_ CONSENTITO**
</dt> <dd> <dl> <dt>

215 (0xD7)
</dt> <dt>



Impossibile annidare le chiamate a LoadModule.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**ERRORE \_ DI \_ MANCATA CORRISPONDENZA DEL TIPO DI COMPUTER \_ \_ EXE**
</dt> <dd> <dl> <dt>

216 (0xD8)
</dt> <dt>



Questa versione di %1 non è compatibile con la versione di Windows in esecuzione. Controllare le informazioni di sistema del computer e quindi contattare l'autore del software.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**\_L'EXE \_ DELL'ERRORE \_ NON PUÒ MODIFICARE IL FILE \_ BINARIO \_ FIRMATO**
</dt> <dd> <dl> <dt>

217 (0xD9)
</dt> <dt>



Il file di immagine %1 è firmato e non può essere modificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**IL \_ FILE EXE \_ DELL'ERRORE \_ NON PUÒ MODIFICARE IL FILE \_ \_ BINARIO CON FIRMA \_ FORTE**
</dt> <dd> <dl> <dt>

218 (0xDA)
</dt> <dt>



Il file di immagine %1 è con firma completa e non può essere modificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**FILE \_ DI ERRORE \_ \_ ESTRATTO**
</dt> <dd> <dl> <dt>

220 (0xDC)
</dt> <dt>



Questo file è estratto o bloccato per la modifica da un altro utente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**ESTRAZIONE \_ DEGLI \_ ERRORI NECESSARIA**
</dt> <dd> <dl> <dt>

221 (0xDD)
</dt> <dt>



Il file deve essere estratto prima di salvare le modifiche.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERRORE \_ TIPO DI FILE NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

222 (0xDE)
</dt> <dt>



Il tipo di file salvato o recuperato è stato bloccato.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**FILE \_ DI ERRORE TROPPO \_ \_ GRANDE**
</dt> <dd> <dl> <dt>

223 (0xDF)
</dt> <dt>



Le dimensioni del file superano il limite consentito e non possono essere salvate.


</dt> </dl> </dd> <dt>

<span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**RICHIESTA \_ AUTENTICAZIONE MODULI DI \_ \_ ERRORE**
</dt> <dd> <dl> <dt>

224 (0xE0)
</dt> <dt>



Accesso negato. Prima di aprire i file in questo percorso, è necessario aggiungere il sito Web all'elenco dei siti attendibili, passare al sito Web e selezionare l'opzione per l'accesso automatico.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**VIRUS \_ \_ DEGLI ERRORI INFETTATO**
</dt> <dd> <dl> <dt>

225 (0xE1)
</dt> <dt>



L'operazione non è stata completata correttamente perché il file contiene un virus o software potenzialmente indesiderato.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**VIRUS \_ DEGLI \_ ERRORI ELIMINATO**
</dt> <dd> <dl> <dt>

226 (0xE2)
</dt> <dt>



Questo file contiene un virus o software potenzialmente indesiderato e non può essere aperto. A causa della natura di questo virus o di software potenzialmente indesiderato, il file è stato rimosso da questo percorso.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**ERRORE \_ PIPE \_ LOCALE**
</dt> <dd> <dl> <dt>

229 (0xE5)
</dt> <dt>



La pipe è locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**ERRORE \_ PIPE \_ NON NEGATIVA**
</dt> <dd> <dl> <dt>

230 (0xE6)
</dt> <dt>



Lo stato della pipe non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**ERRORE \_ PIPE \_ OCCUPATA**
</dt> <dd> <dl> <dt>

231 (0xE7)
</dt> <dt>



Tutte le istanze di pipe sono occupate.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERRORE \_ NESSUN \_ DATO**
</dt> <dd> <dl> <dt>

232 (0xE8)
</dt> <dt>



La pipe è in fase di chiusura.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**PIPE \_ DI ERRORE NON \_ \_ CONNESSA**
</dt> <dd> <dl> <dt>

233 (0xE9)
</dt> <dt>



Nessun processo si trova nell'altra estremità della pipe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERRORE \_ - ALTRI \_ DATI**
</dt> <dd> <dl> <dt>

234 (0xEA)
</dt> <dt>



sono disponibili più dati.


</dt> </dl> </dd> <dt>

<span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERRORE \_ VC \_ DISCONNESSO**
</dt> <dd> <dl> <dt>

240 (0xF0)
</dt> <dt>



La sessione è stata annullata.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERRORE \_ NOME \_ EA NON \_ VALIDO**
</dt> <dd> <dl> <dt>

254 (0xFE)
</dt> <dt>



Il nome dell'attributo esteso specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**ERRORE \_ ELENCO EA \_ \_ INCOERENTE**
</dt> <dd> <dl> <dt>

255 (0xFF)
</dt> <dt>



Gli attributi estesi non sono coerenti.


</dt> </dl> </dd> <dt>

<span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**\_TIMEOUT DI ATTESA**
</dt> <dd> <dl> <dt>

258 (0x102)
</dt> <dt>



Tempo di attesa scaduto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERRORE \_ NESSUN \_ ALTRO \_ ELEMENTO**
</dt> <dd> <dl> <dt>

259 (0x103)
</dt> <dt>



Dati disponibili esauriti.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**ERRORE \_ IMPOSSIBILE \_ COPIARE**
</dt> <dd> <dl> <dt>

266 (0x10A)
</dt> <dt>



Non è possibile usare le funzioni di copia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**\_DIRECTORY DEGLI ERRORI**
</dt> <dd> <dl> <dt>

267 (0x10B)
</dt> <dt>



Il nome della directory non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERRORE \_ EAS \_ NON \_ IDONEO**
</dt> <dd> <dl> <dt>

275 (0x113)
</dt> <dt>



Gli attributi estesi non rientrano nel buffer.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**ERRORE \_ FILE EA \_ \_ DANNEGGIATO**
</dt> <dd> <dl> <dt>

276 (0x114)
</dt> <dt>



Il file di attributi estesi nel file system è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERRORE \_ EA \_ TABLE \_ FULL**
</dt> <dd> <dl> <dt>

277 (0x115)
</dt> <dt>



Il file della tabella degli attributi estesi è pieno.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERRORE \_ HANDLE \_ EA NON \_ VALIDO**
</dt> <dd> <dl> <dt>

278 (0x116)
</dt> <dt>



L'handle dell'attributo esteso specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**\_EAS DI ERRORE NON \_ \_ SUPPORTATI**
</dt> <dd> <dl> <dt>

282 (0x11A)
</dt> <dt>



L'file system non supporta gli attributi estesi.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ERRORE \_ NON \_ PROPRIETARIO**
</dt> <dd> <dl> <dt>

288 (0x120)
</dt> <dt>



Provare a rilasciare mutex non di proprietà del chiamante.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**TROPPI \_ \_ POST DI \_ ERRORE**
</dt> <dd> <dl> <dt>

298 (0x12A)
</dt> <dt>



Troppi post sono stati emersi in un semaforo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERRORE \_ DURANTE LA COPIA \_ PARZIALE**
</dt> <dd> <dl> <dt>

299 (0x12B)
</dt> <dt>



È stata completata solo una parte di una richiesta ReadProcessMemory o WriteProcessMemory.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERRORE \_ OPLOCK \_ NON \_ CONCESSO**
</dt> <dd> <dl> <dt>

300 (0x12C)
</dt> <dt>



La richiesta oplock è stata negata.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERRORE \_ DEL \_ PROTOCOLLO OPLOCK NON \_ VALIDO**
</dt> <dd> <dl> <dt>

301 (0x12D)
</dt> <dt>



Riconoscimento oplock non valido ricevuto dal sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**DISCO \_ DI ERRORE TROPPO \_ \_ FRAMMENTATO**
</dt> <dd> <dl> <dt>

302 (0x12E)
</dt> <dt>



Il volume è troppo frammentato per completare l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERRORE \_ DURANTE L'ELIMINAZIONE \_ IN SOSPESO**
</dt> <dd> <dl> <dt>

303 (0x12F)
</dt> <dt>



Impossibile aprire il file perché è in corso l'eliminazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERRORE \_ INCOMPATIBILE CON \_ \_ \_ L'IMPOSTAZIONE GLOBALE DEL REGISTRO DI SISTEMA DEI NOMI \_ \_ \_ BREVI**
</dt> <dd> <dl> <dt>

304 (0x130)
</dt> <dt>



Le impostazioni del nome breve non possono essere modificate in questo volume a causa dell'impostazione globale del Registro di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**NOMI \_ BREVI DI ERRORE NON \_ \_ \_ \_ ABILITATI NEL \_ VOLUME**
</dt> <dd> <dl> <dt>

305 (0x131)
</dt> <dt>



I nomi brevi non sono abilitati in questo volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**IL FLUSSO \_ DI SICUREZZA DEGLI ERRORI È \_ \_ \_ INCOERENTE**
</dt> <dd> <dl> <dt>

306 (0x132)
</dt> <dt>



Il flusso di sicurezza per il volume specificato è in uno stato incoerente. Eseguire CHKDSK nel volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERRORE INTERVALLO \_ \_ DI BLOCCO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

307 (0x133)
</dt> <dt>



Impossibile elaborare un'operazione di blocco file richiesta a causa di un intervallo di byte non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**\_ \_ SOTTOSISTEMA IMMAGINE ERRORE \_ NON \_ PRESENTE**
</dt> <dd> <dl> <dt>

308 (0x134)
</dt> <dt>



Il sottosistema necessario per supportare il tipo di immagine non è presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**GUID \_ DI NOTIFICA DEGLI ERRORI GIÀ \_ \_ \_ DEFINITO**
</dt> <dd> <dl> <dt>

309 (0x135)
</dt> <dt>



Al file specificato è già associato un GUID di notifica.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERRORE \_ GESTORE \_ ECCEZIONI NON \_ VALIDO**
</dt> <dd> <dl> <dt>

310 (0x136)
</dt> <dt>



È stata rilevata una routine del gestore eccezioni non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**ERRORE \_ \_ DUPLICA PRIVILEGI**
</dt> <dd> <dl> <dt>

311 (0x137)
</dt> <dt>



Sono stati specificati privilegi duplicati per il token.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERRORE \_ NESSUN \_ INTERVALLO \_ ELABORATO**
</dt> <dd> <dl> <dt>

312 (0x138)
</dt> <dt>



Non è stato possibile elaborare alcun intervallo per l'operazione specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERRORE \_ NON CONSENTITO NEL FILE DI \_ \_ \_ \_ SISTEMA**
</dt> <dd> <dl> <dt>

313 (0x139)
</dt> <dt>



L'operazione non è consentita in un file system file interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**RISORSE \_ DISCO DI ERRORE \_ \_ ESAURITE**
</dt> <dd> <dl> <dt>

314 (0x13A)
</dt> <dt>



Le risorse fisiche di questo disco sono state esaurite.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**ERRORE \_ TOKEN NON \_ VALIDO**
</dt> <dd> <dl> <dt>

315 (0x13B)
</dt> <dt>



Il token che rappresenta i dati non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**FUNZIONALITÀ \_ DEL DISPOSITIVO DI ERRORE NON \_ \_ \_ SUPPORTATA**
</dt> <dd> <dl> <dt>

316 (0x13C)
</dt> <dt>



Il dispositivo non supporta la funzionalità di comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**ERRORE \_ MR MID NON \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

317 (0x13D)
</dt> <dt>



Impossibile trovare il testo del messaggio per il numero di messaggio 0x%1 nel file di messaggio per %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**AMBITO \_ ERRORE \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

318 (0x13E)
</dt> <dt>



L'ambito specificato non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**ERRORE \_ AMBITO NON \_ DEFINITO**
</dt> <dd> <dl> <dt>

319 (0x13F)
</dt> <dt>



I criteri di accesso centrale specificati non sono definiti nel computer di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**ERRORE \_ LIMITE NON \_ VALIDO**
</dt> <dd> <dl> <dt>

320 (0x140)
</dt> <dt>



I criteri di accesso centrale ottenuti da Active Directory non sono validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**ERRORE \_ DISPOSITIVO \_ NON RAGGIUNGIBILE**
</dt> <dd> <dl> <dt>

321 (0x141)
</dt> <dt>



Il dispositivo non è raggiungibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**NESSUNA \_ \_ RISORSA DEL DISPOSITIVO DI \_ ERRORE**
</dt> <dd> <dl> <dt>

322 (0x142)
</dt> <dt>



Le risorse del dispositivo di destinazione non sono sufficienti per completare l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**ERRORE \_ DI \_ CHECKSUM DEI \_ DATI DEGLI ERRORI**
</dt> <dd> <dl> <dt>

323 (0x143)
</dt> <dt>



Si è verificato un errore di checksum di integrità dei dati. I dati nel flusso di file sono danneggiati.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERRORE \_ DURANTE L'OPERAZIONE \_ EA DEL KERNEL \_ INTERMIXED \_**
</dt> <dd> <dl> <dt>

324 (0x144)
</dt> <dt>



È stato effettuato un tentativo di modificare sia un KERNEL che un normale attributo esteso (EA) nella stessa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**L'OPERAZIONE DI \_ TAGLIO A LIVELLO DI FILE DI ERRORE NON È \_ \_ \_ \_ SUPPORTATA**
</dt> <dd> <dl> <dt>

326 (0x146)
</dt> <dt>



Il dispositivo non supporta TRIM a livello di file.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**VIOLAZIONE \_ \_ DELL'ALLINEAMENTO DELL'OFFSET \_ DEGLI ERRORI**
</dt> <dd> <dl> <dt>

327 (0x147)
</dt> <dt>



Il comando ha specificato un offset dei dati che non è allineato alla granularità/allineamento del dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**ERRORE \_ CAMPO NON VALIDO \_ \_ \_ NELL'ELENCO DI \_ PARAMETRI**
</dt> <dd> <dl> <dt>

328 (0x148)
</dt> <dt>



Il comando ha specificato un campo non valido nel relativo elenco di parametri.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**OPERAZIONE \_ DI ERRORE IN \_ \_ CORSO**
</dt> <dd> <dl> <dt>

329 (0x149)
</dt> <dt>



È in corso un'operazione con il dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERRORE \_ PERCORSO DEL DISPOSITIVO NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

330 (0x14A)
</dt> <dt>



Si è tentato di inviare il comando tramite un percorso non valido al dispositivo di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERRORE \_ DI \_ TROPPI \_ DESCRITTORI**
</dt> <dd> <dl> <dt>

331 (0x14B)
</dt> <dt>



Il comando ha specificato un numero di descrittori che ha superato il valore massimo supportato dal dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**ERROR \_ SCRUB \_ DATA \_ DISABLED**
</dt> <dd> <dl> <dt>

332 (0x14C)
</dt> <dt>



Lo scrubbing è disabilitato nel file specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**ERRORE DI \_ ARCHIVIAZIONE \_ NON \_ RIDONDANTE**
</dt> <dd> <dl> <dt>

333 (0x14D)
</dt> <dt>



Il dispositivo di archiviazione non fornisce ridondanza.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**ERRORE \_ FILE \_ RESIDENTE NON \_ \_ SUPPORTATO**
</dt> <dd> <dl> <dt>

334 (0x14E)
</dt> <dt>



Un'operazione non è supportata in un file residente.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**ERRORE \_ FILE \_ COMPRESSO NON \_ \_ SUPPORTATO**
</dt> <dd> <dl> <dt>

335 (0x14F)
</dt> <dt>



Un'operazione non è supportata in un file compresso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**\_DIRECTORY DEGLI ERRORI NON \_ \_ SUPPORTATA**
</dt> <dd> <dl> <dt>

336 (0x150)
</dt> <dt>



Un'operazione non è supportata in una directory.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**ERRORE \_ DURANTE LA LETTURA DALLA \_ \_ \_ COPIA**
</dt> <dd> <dl> <dt>

337 (0x151)
</dt> <dt>



Impossibile leggere la copia specificata dei dati richiesti.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**ERRORE FAIL \_ \_ NOACTION \_ REBOOT**
</dt> <dd> <dl> <dt>

350 (0x15E)
</dt> <dt>



Non è stata eseguita alcuna azione perché è necessario un riavvio del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**ERRORE DI \_ ARRESTO \_ NON RIUSCITO**
</dt> <dd> <dl> <dt>

351 (0x15F)
</dt> <dt>



L'operazione di arresto non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**ERRORE - \_ RIAVVIO \_ NON RIUSCITO**
</dt> <dd> <dl> <dt>

352 (0x160)
</dt> <dt>



L'operazione di riavvio non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**ERRORE \_ RAGGIUNTO NUMERO MASSIMO DI \_ \_ SESSIONI**
</dt> <dd> <dl> <dt>

353 (0x161)
</dt> <dt>



È stato raggiunto il numero massimo di sessioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**MODALITÀ \_ THREAD DI ERRORE GIÀ IN \_ \_ \_ BACKGROUND**
</dt> <dd> <dl> <dt>

400 (0x190)
</dt> <dt>



Il thread è già in modalità di elaborazione in background.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**MODALITÀ \_ THREAD DI ERRORE NON IN \_ \_ \_ BACKGROUND**
</dt> <dd> <dl> <dt>

401 (0x191)
</dt> <dt>



Il thread non è in modalità di elaborazione in background.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**MODALITÀ \_ DI ELABORAZIONE DEGLI ERRORI GIÀ IN \_ \_ \_ BACKGROUND**
</dt> <dd> <dl> <dt>

402 (0x192)
</dt> <dt>



Il processo è già in modalità di elaborazione in background.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**MODALITÀ \_ DI ELABORAZIONE DEGLI ERRORI NON IN \_ \_ \_ BACKGROUND**
</dt> <dd> <dl> <dt>

403 (0x193)
</dt> <dt>



Il processo non è in modalità di elaborazione in background.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERRORE INDIRIZZO \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

487 (0x1E7)
</dt> <dt>



Tentativo di accesso a un indirizzo non valido.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>WinError.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore di sistema](system-error-codes.md)
</dt> </dl>

 

 




