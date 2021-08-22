---
description: La struttura JOB INFO 1 specifica informazioni sul processo di stampa, ad esempio il valore dell'identificatore del processo, il nome della stampante per cui viene spoolato il processo, il nome del computer che ha creato il processo di stampa, il nome dell'utente proprietario del processo di stampa e \_ \_ così via.
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: JOB_INFO_1 struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_1
- _JOB_INFO_1A
- _JOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c6e8d5900a0f2d0a2dce5c12d2629abfc80776cdc0ada1354070005e28fbcd37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971330"
---
# <a name="job_info_1-structure"></a>Struttura JOB \_ INFO \_ 1

La struttura **JOB \_ INFO \_ 1** specifica informazioni sul processo di stampa, ad esempio il valore dell'identificatore del processo, il nome della stampante per cui viene spoolato il processo, il nome del computer che ha creato il processo di stampa, il nome dell'utente proprietario del processo di stampa e così via.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _JOB_INFO_1 {
  DWORD      JobId;
  LPTSTR     pPrinterName;
  LPTSTR     pMachineName;
  LPTSTR     pUserName;
  LPTSTR     pDocument;
  LPTSTR     pDatatype;
  LPTSTR     pStatus;
  DWORD      Status;
  DWORD      Priority;
  DWORD      Position;
  DWORD      TotalPages;
  DWORD      PagesPrinted;
  SYSTEMTIME Submitted;
} JOB_INFO_1, *PJOB_INFO_1;
```



## <a name="members"></a>Members

<dl> <dt>

**Jobid**
</dt> <dd>

Identificatore del processo.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome della stampante per cui viene spoolato il processo.

</dd> <dt>

**pMachineName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del computer che ha creato il processo di stampa.

</dd> <dt>

**pUserName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome dell'utente proprietario del processo di stampa.

</dd> <dt>

**pDocument**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del processo di stampa, ad esempio "MS-WORD: Review.doc").

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il tipo di dati utilizzato per registrare il processo di stampa.

</dd> <dt>

**pStatus**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica lo stato del processo di stampa. Questo membro deve essere controllato prima di *Status* e, se *pStatus* è **NULL,** lo stato viene definito dal contenuto del membro Status.

</dd> <dt>

**Status**
</dt> <dd>

Stato del processo. Il valore di questo membro può essere zero o una combinazione di uno o più dei valori seguenti. Il valore zero indica che la coda di stampa è stata sospesa al termine dello spooling del documento.



| Valore                           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| STATO \_ DEL PROCESSO BLOCCATO \_ \_ DEVQ      | Il driver non può stampare il processo.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| STATO \_ DEL \_ PROCESSO COMPLETATO           | **Windows XP e versioni successive:** Il processo viene inviato alla stampante, ma il processo potrebbe non essere ancora stampato.<br/> Per ulteriori informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                                                                                                                                                           |
| STATO \_ PROCESSO \_ ELIMINATO            | Il processo è stato eliminato.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ELIMINAZIONE DELLO \_ STATO DEL \_ PROCESSO           | È in corso l'eliminazione del processo.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ERRORE \_ DI STATO DEL \_ PROCESSO              | Al processo è associato un errore.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| STATO \_ DEL PROCESSO \_ OFFLINE            | La stampante è offline.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| DOCUMENTO \_ SULLO STATO DEL \_ PROCESSO           | La stampante non è cartacea.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| STATO \_ DEL PROCESSO \_ SOSPESO             | Il processo è sospeso.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| STATO \_ PROCESSO \_ STAMPATO            | Il processo è stato stampato.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| STAMPA \_ DELLO STATO DEL \_ PROCESSO           | Il processo è in corso di stampa.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| RIAVVIO \_ DELLO STATO \_ DEL PROCESSO            | Il processo è stato riavviato.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| STATO \_ DEL \_ PROCESSO MANTENUTO           | **Windows Vista e versioni successive:** Il processo è stato mantenuto nella coda di stampa e non può essere eliminato. Ciò può essere causato dai seguenti problemi:<br/> 1) Il processo è stato mantenuto manualmente da una chiamata a SetJob e lo spooler è in attesa del rilascio del processo.<br/> 2) Il processo non ha completato la stampa e deve terminare la stampa prima di poter essere eliminato automaticamente.<br/> Per altre informazioni sui comandi del processo di stampa, vedere [**SetJob.**](setjob.md)<br/> |
| \_ \_ SPOOLING DELLO STATO DEL PROCESSO           | Il processo è in spooling.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| INTERVENTO \_ DELL'UTENTE \_ SULLO STATO DEL \_ PROCESSO | La stampante presenta un errore che richiede all'utente di eseguire un'operazione.                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

**Priorità**
</dt> <dd>

Priorità del processo. Questo membro può essere uno dei valori seguenti o compreso nell'intervallo compreso tra 1 e 99 (MIN \_ PRIORITY fino a MAX \_ PRIORITY).



| Valore         | Significato           |
|---------------|-------------------|
| PRIORITÀ \_ MINIMA | Priorità minima. |
| PRIORITÀ \_ MASSIMA | Priorità massima. |
| PRIORITÀ \_ DEF | Priorità predefinita. |



 

</dd> <dt>

**Position**
</dt> <dd>

Posizione del processo nella coda di stampa.

</dd> <dt>

**TotalPages**
</dt> <dd>

Numero totale di pagine contenute nel documento. Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione della pagina.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

Numero di pagine stampate. Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione della pagina.

</dd> <dt>

**Inviata**
</dt> <dd>

Struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che specifica l'ora di spooling del documento.

Questo valore di ora è in formato UTC (Universal Time Coordinate). È necessario convertirlo in un valore di ora locale prima di visualizzarlo. È possibile usare la [**funzione FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) per eseguire la conversione.

</dd> </dl>

## <a name="remarks"></a>Commenti

I monitoraggi delle porte che non supportano TrueEndOfJob impostano il processo come JOB STATUS PRINTED subito dopo l'invio \_ \_ del processo alla stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ JOB \_ INFO \_ 1W** (Unicode) e **\_ JOB INFO \_ \_ 1A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

