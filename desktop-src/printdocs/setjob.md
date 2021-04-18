---
description: La funzione SetJob sospende, riprende, Annulla o riavvia un processo di stampa su una stampante specificata. È inoltre possibile utilizzare la funzione SetJob per impostare i parametri del processo di stampa, ad esempio la priorità del processo di stampa e il nome del documento.
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: Funzione SetJob (WinSpool. h)
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
ms.openlocfilehash: 34dfc8c0239a10d7e7f036beed457d57329f4c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314979"
---
# <a name="setjob-function"></a>SetJob (funzione)

La funzione **SetJob** sospende, riprende, Annulla o riavvia un processo di stampa su una stampante specificata. È inoltre possibile utilizzare la funzione **SetJob** per impostare i parametri del processo di stampa, ad esempio la priorità del processo di stampa e il nome del documento.

È possibile utilizzare la funzione **SetJob** per fornire un comando a un processo di stampa o per impostare i parametri del processo di stampa oppure per eseguire entrambe le operazioni nella stessa chiamata. Il valore del parametro *Command* non influisce sul modo in cui la funzione usa i parametri *Level* e *pJob* . Inoltre, è possibile usare **SetJob** con [**informazioni sul processo \_ \_ 3**](job-info-3.md) per collegare insieme un set di processi di stampa. Per ulteriori informazioni, vedere la sezione Osservazioni.

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

*hPrinter* \[ in\]
</dt> <dd>

Handle per l'oggetto stampante di interesse. Utilizzare la funzione [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*JobID* \[ in\]
</dt> <dd>

Identificatore che specifica il processo di stampa. È possibile ottenere un identificatore del processo di stampa chiamando la funzione [**AddJob**](addjob.md) o [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .

Se il parametro *Level* è impostato su 3, il parametro *JobID* deve corrispondere al membro **JobID** della struttura [**Job \_ info \_ 3**](job-info-3.md) a cui punta *pJob*

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Tipo di struttura delle informazioni sul processo a cui punta il parametro *pJob* .

**Tutte le versioni di Windows**: è possibile impostare il parametro *Level* su 0, 1 o 2. Quando si imposta *Level* su 0, *PJob* deve essere **null**. Usare questi valori quando non si imposta alcun parametro del processo di stampa.

È anche possibile impostare il parametro *Level* su 3.

A partire da **Windows Vista**: è anche possibile impostare il parametro *Level* su 4.

</dd> <dt>

*pJob* \[ in\]
</dt> <dd>

Puntatore a una struttura che imposta i parametri del processo di stampa.

**Tutte le versioni di Windows**: *pJob* può puntare a una struttura di job info [**\_ \_ 1**](job-info-1.md) o [**Job \_ info \_ 2**](job-info-2.md) .

*pJob* può puntare anche a una struttura di [**informazioni sul processo \_ \_ 3**](job-info-3.md) . È necessario disporre dell'autorizzazione di accesso per l' **\_ \_ Amministrazione** dell'accesso ai processi specificati dai membri **JobID** e **NextJobId** della struttura di **informazioni sul processo \_ \_ 3** .

A partire da **Windows Vista**: *pJob* può puntare anche a una struttura di [**informazioni sul processo \_ \_ 4**](job-info-4.md) .

Se il parametro *Level* è 0, *PJob* deve essere **null**.

</dd> <dt>

*Comando* \[ in\]
</dt> <dd>

Operazione di stampa del processo da eseguire. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                            | Significato                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <dt>**\_annullamento controllo \_ processo**</dt> </dl>                                    | Non usare. Per eliminare un processo di stampa, utilizzare il **controllo del processo \_ \_ Delete**.<br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <dt>**\_pausa controllo \_ processo**</dt> </dl>                                       | Sospendere il processo di stampa.<br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <dt>**\_riavvio del controllo processo \_**</dt> </dl>                                 | Riavviare il processo di stampa. Un processo può essere riavviato solo se è stato stampato.<br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <dt>**\_ripresa controllo \_ processo**</dt> </dl>                                    | Riprendere un processo di stampa in pausa.<br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <dt>**\_eliminazione controllo \_ processo**</dt> </dl>                                    | Eliminare il processo di stampa.<br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <dt>**\_controllo processo \_ inviato \_ alla \_ stampante**</dt> </dl>       | Utilizzato dai monitoraggi porta per terminare il processo di stampa.<br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <dt>**\_ultima pagina di controllo processo \_ \_ \_ espellata**</dt> </dl> | Utilizzato dai monitoraggi della lingua per terminare il processo di stampa.<br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <dt>**\_mantenimento del controllo del processo \_**</dt> </dl>                                    | **Windows Vista e versioni successive**: Mantieni il processo nella coda dopo la stampa.<br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <dt>**\_versione controllo \_ processo**</dt> </dl>                                 | **Windows Vista e versioni successive**: rilasciare il processo di stampa.<br/>                     |



 

È possibile utilizzare la stessa chiamata alla funzione **SetJob** per impostare i parametri del processo di stampa e per fornire un comando a un processo di stampa. Pertanto, il *comando* non deve essere 0 se si imposta i parametri del processo di stampa, sebbene possa essere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

È possibile utilizzare la **funzione SetJob** per impostare vari parametri del processo di stampa fornendo un puntatore a un [**processo di \_ informazioni \_ 1**](job-info-1.md), informazioni sul processo [**\_ \_ 2**](job-info-2.md), informazioni sul [**processo \_ \_ 3**](job-info-3.md)o struttura di informazioni sul [**processo \_ \_ 4**](job-info-4.md) contenente i dati necessari.

Per rimuovere o eliminare tutti i processi di stampa per una particolare stampante, chiamare la funzione [**Seprinter**](setprinter.md) con il parametro *Command* impostato sul **controllo della stampante \_ \_ Purge**.

I membri seguenti di una struttura di informazioni sul processo [**\_ \_ 1**](job-info-1.md), [**informazioni sul processo \_ \_ 2**](job-info-2.md)o [**informazioni sul processo \_ \_ 4**](job-info-4.md) vengono ignorati in una chiamata a **SetJob**: **JobID**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **size**, **inviato**, **ora** e **TotalPages**.

Per modificare la posizione di un processo di stampa nella coda di stampa, è necessario disporre dell'autorizzazione di accesso per **la stampante. \_ \_**

Se non si desidera impostare la posizione di un processo di stampa nella coda di stampa, è necessario impostare il membro **position** della struttura [**Job \_ info \_ 1**](job-info-1.md), [**Job \_ info \_ 2**](job-info-2.md)o [**Job \_ info \_ 4**](job-info-4.md) sulla posizione del processo non **\_ \_ specificata**.

Usare la funzione **SetJob** con la struttura [**Job \_ info \_ 3**](job-info-3.md) per collegare un set di processi di stampa (noto anche come catena). Questa operazione è utile nelle situazioni in cui un singolo documento è costituito da diverse parti di cui si desidera eseguire il rendering separatamente. Per stampare i processi a, B, C e D in ordine, chiamare **SetJob** con [**informazioni sul processo \_ \_ 4**](job-info-4.md) per collegare da a a b, da b a c e da C a d.

Se si collegano i processi di stampa, tenere presente quanto segue:

-   I processi possono essere aggiunti all'inizio o alla fine di una catena.
-   Tutti i processi nella catena devono avere lo stesso tipo di dati.
-   La catena deve essere completamente collegata prima che lo spooling venga avviato. in caso contrario, lo spooler potrebbe stampare ed eliminare i processi di spooling prima di collegarli tutti. Esistono due modi per impedire la stampa della catena in modo anomalo:

    -   Sospende il primo processo nella catena finché la catena non è completamente collegata. Lo stato di sospensione del primo processo determina lo stato di tutti i processi nella catena.
    -   Lasciare incompleto il primo processo, ovvero non chiamare [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) o [**ScheduleJob**](schedulejob.md) per il primo processo. Tuttavia, se l'opzione ' stampa durante lo spooling ' è abilitata (impostazione predefinita), questo metodo blocca la porta mentre viene compilata la catena, che impedisce anche la stampa di processi non correlati.

-   L'applicazione deve gestire il caso in cui l'utente elimina un processo nella catena prima del completamento della stampa della catena. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **un \_ parametro non valido** quando JobID non esiste.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>WinSpool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WinSpool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |
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

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**\_Informazioni processo \_ 1**](job-info-1.md)
</dt> <dt>

[**Informazioni sul processo \_ \_ 2**](job-info-2.md)
</dt> <dt>

[**Informazioni sul processo \_ \_ 3**](job-info-3.md)
</dt> <dt>

[**Informazioni sul processo \_ \_ 4**](job-info-4.md)
</dt> </dl>

 

