---
description: La funzione SetJob sospende, riprende, annulla o riavvia un processo di stampa su una stampante specificata. È anche possibile usare la funzione SetJob per impostare i parametri del processo di stampa, ad esempio la priorità del processo di stampa e il nome del documento.
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: Funzione SetJob (WinSpool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetJob
- SetJobA
- SetJobW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 9259429a7696e832bbbe6d0dd4bbb6fb46e7bce2bf7157122c10ca47656af346
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060021"
---
# <a name="setjob-function"></a>Funzione SetJob

La **funzione SetJob** sospende, riprende, annulla o riavvia un processo di stampa su una stampante specificata. È anche possibile usare la **funzione SetJob** per impostare i parametri del processo di stampa, ad esempio la priorità del processo di stampa e il nome del documento.

È possibile usare la **funzione SetJob** per assegnare un comando a un processo di stampa o per impostare i parametri del processo di stampa o per eseguire entrambe le operazioni nella stessa chiamata. Il valore del *parametro Command* non influisce sul modo in cui la funzione usa i *parametri Level* *e pJob.* È anche possibile usare **SetJob** con [**JOB INFO \_ \_ 3**](job-info-3.md) per collegare un set di processi di stampa. Per ulteriori informazioni, vedere la sezione Osservazioni.

## <a name="syntax"></a>Sintassi


```C++
BOOL SetJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  JobId,
  _In_ DWORD  Level,
  _In_ LPBYTE pJob,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per l'oggetto stampante di interesse. Usare la [**funzione OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*JobId* \[ Pollici\]
</dt> <dd>

Identificatore che specifica il processo di stampa. Per ottenere un identificatore di processo di stampa, chiamare la [**funzione AddJob**](addjob.md) o [**La funzione StartDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)

Se il *parametro Level* è impostato su 3, il *parametro JobId* deve corrispondere al membro **JobId** della struttura [**JOB INFO \_ \_ 3**](job-info-3.md) a cui *punta pJob*

</dd> <dt>

*Livello* \[ Pollici\]
</dt> <dd>

Tipo di struttura di informazioni sul processo a cui punta il *parametro pJob.*

**Tutte le versioni Windows:** è possibile impostare il *parametro Level* su 0, 1 o 2. Quando si imposta *Level* su 0, *pJob* deve essere **NULL.** Usare questi valori quando non si impostano parametri del processo di stampa.

È anche possibile impostare il *parametro Level* su 3.

A partire **Windows Vista:** è anche possibile impostare il *parametro Level* su 4.

</dd> <dt>

*pJob* \[ Pollici\]
</dt> <dd>

Puntatore a una struttura che imposta i parametri del processo di stampa.

**Tutte le versioni Windows:** *pJob* può puntare a una struttura [**JOB INFO \_ \_ 1**](job-info-1.md) o [**JOB INFO \_ \_ 2.**](job-info-2.md)

*pJob* può anche puntare a una [**struttura JOB INFO \_ \_ 3.**](job-info-3.md) È necessario disporre **dell'autorizzazione di accesso JOB \_ ACCESS \_ ADMINISTER** per i processi specificati dai membri **JobId** e **NextJobId** della **struttura JOB INFO \_ \_ 3.**

A partire **Windows Vista**: *pJob* può anche puntare a una [**struttura JOB INFO \_ \_ 4.**](job-info-4.md)

Se il *parametro Level* è 0, *pJob* deve essere **NULL.**

</dd> <dt>

*Comando* \[ Pollici\]
</dt> <dd>

Operazione del processo di stampa da eseguire. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                            | Significato                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <dt>**ANNULLAMENTO \_ DEL CONTROLLO \_ DEL PROCESSO**</dt> </dl>                                    | Non usare. Per eliminare un processo di stampa, usare **JOB \_ CONTROL \_ DELETE**.<br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <dt>**SOSPENSIONE \_ DEL CONTROLLO DEL \_ PROCESSO**</dt> </dl>                                       | Sospendere il processo di stampa.<br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <dt>**RIAVVIO \_ DEL CONTROLLO \_ DEL PROCESSO**</dt> </dl>                                 | Riavviare il processo di stampa. Un processo può essere riavviato solo se è in corso di stampa.<br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <dt>**RIPRESA \_ DEL CONTROLLO DEI \_ PROCESSI**</dt> </dl>                                    | Riprendere un processo di stampa sospeso.<br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <dt>**ELIMINAZIONE \_ DEL CONTROLLO DEL \_ PROCESSO**</dt> </dl>                                    | Eliminare il processo di stampa.<br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <dt>**CONTROLLO \_ DEL PROCESSO INVIATO ALLA \_ \_ \_ STAMPANTE**</dt> </dl>       | Usato dai monitoraggi delle porte per terminare il processo di stampa.<br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <dt>**ULTIMA PAGINA DEL CONTROLLO \_ \_ PROCESSO \_ \_ ESPULSA**</dt> </dl> | Usato dai monitoraggi linguistici per terminare il processo di stampa.<br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <dt>**MANTENIMENTO \_ DEL CONTROLLO DEI \_ PROCESSI**</dt> </dl>                                    | **Windows Vista e versioni successive:** mantenere il processo nella coda dopo la stampa.<br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <dt>**VERSIONE \_ DI CONTROLLO DEL \_ PROCESSO**</dt> </dl>                                 | **Windows Vista e versioni successive:** rilasciare il processo di stampa.<br/>                     |



 

È possibile usare la stessa chiamata alla **funzione SetJob** per impostare i parametri del processo di stampa e assegnare un comando a un processo di stampa. Pertanto, *command* non deve essere 0 se si impostano i parametri del processo di stampa, anche se può essere .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

È possibile usare la **funzione SetJob** per impostare vari parametri del processo di stampa fornendo un puntatore a una struttura [**JOB INFO \_ \_ 1,**](job-info-1.md) [**JOB INFO \_ \_ 2,**](job-info-2.md) [**JOB INFO \_ \_ 3**](job-info-3.md)o [**JOB INFO \_ \_ 4**](job-info-4.md) che contiene i dati necessari.

Per rimuovere o eliminare tutti i processi di stampa per una determinata stampante, chiamare la [**funzione SetPrinter**](setprinter.md) con il parametro *Command* impostato su **PRINTER CONTROL \_ \_ PURGE**.

I membri seguenti di una struttura [**JOB \_ INFO \_ 1,**](job-info-1.md) [**JOB INFO \_ \_ 2**](job-info-2.md)o [**JOB INFO \_ \_ 4**](job-info-4.md) vengono ignorati in una chiamata a **SetJob**: **JobId**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **Size**, **Submitted,** **Time** e **TotalPages**.

Per modificare la posizione di un processo di stampa nella coda di stampa, è necessario disporre dell'autorizzazione di accesso **PRINTER \_ ACCESS \_ ADMINISTER** per una stampante.

Se non si vuole impostare la posizione di un processo di stampa nella coda di stampa, è necessario impostare il membro **Position** della struttura [**JOB INFO \_ \_ 1,**](job-info-1.md) [**JOB INFO \_ \_ 2**](job-info-2.md)o [**JOB INFO \_ \_ 4**](job-info-4.md) su **JOB POSITION \_ \_ UNSPECIFIED**.

Usare la **funzione SetJob** con la struttura [**JOB INFO \_ \_ 3**](job-info-3.md) per collegare insieme un set di processi di stampa (noti anche come catena). Ciò è utile in situazioni in cui un singolo documento è costituito da diverse parti di cui si vuole eseguire il rendering separatamente. Per stampare i processi A, B, C e D in ordine, chiamare **SetJob** con [**JOB INFO \_ \_ 4**](job-info-4.md) per collegare A a B, B a C e C a D.

Se si collegano processi di stampa, tenere presente quanto segue:

-   I processi possono essere aggiunti all'inizio o alla fine di una catena.
-   Tutti i processi nella catena devono avere lo stesso tipo di dati.
-   La catena deve essere completamente collegata prima dell'inizio dello spooling, in caso contrario lo spooler può stampare ed eliminare i processi di spooling prima di collegarli tutti. Esistono due modi per evitare la stampa prematura della catena:

    -   Sospendere il primo processo nella catena fino a quando la catena non è completamente collegata. Lo stato sospeso del primo processo determina lo stato di tutti i processi nella catena.
    -   Mantenere il primo processo incompleto, ad esempio non chiamare [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) o [**ScheduleJob**](schedulejob.md) per il primo processo. Tuttavia, se l'opzione "stampa durante lo spooling" è abilitata (impostazione predefinita), questo metodo blocca la porta durante la creazione della catena, impedendo anche la stampa di processi non correlati.

-   L'applicazione deve gestire il caso in cui l'utente elimina un processo nella catena prima che la catena finisca la stampa. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **INVALID \_ PARAMETER** quando un JobID non esiste.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>WinSpool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WinSpool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **SetJobW** (Unicode) e **SetJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL PROCESSO \_ 1**](job-info-1.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL PROCESSO \_ 2**](job-info-2.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL PROCESSO \_ 3**](job-info-3.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL PROCESSO \_ 4**](job-info-4.md)
</dt> </dl>

 

