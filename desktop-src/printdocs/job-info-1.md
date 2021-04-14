---
description: La \_ struttura info processo \_ 1 specifica le informazioni sul processo di stampa, ad esempio il valore dell'identificatore del processo, il nome della stampante per cui viene eseguito lo spooling del processo, il nome del computer in cui è stato creato il processo di stampa, il nome dell'utente proprietario del processo di stampa e così via.
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: Struttura JOB_INFO_1 (winspool. h)
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
ms.openlocfilehash: d56d4d6bce15a661ce141d8e22d27a15837a9f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349081"
---
# <a name="job_info_1-structure"></a>Struttura di informazioni sul processo \_ \_ 1

La **struttura \_ info processo \_ 1** specifica le informazioni sul processo di stampa, ad esempio il valore dell'identificatore del processo, il nome della stampante per cui viene eseguito lo spooling del processo, il nome del computer in cui è stato creato il processo di stampa, il nome dell'utente proprietario del processo di stampa e così via.

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

**JobId**
</dt> <dd>

Identificatore di processo.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome della stampante per cui viene eseguito lo spooling del processo.

</dd> <dt>

**pMachineName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del computer in cui è stato creato il processo di stampa.

</dd> <dt>

**pUserName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome dell'utente proprietario del processo di stampa.

</dd> <dt>

**pDocument**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del processo di stampa, ad esempio "MS-WORD: Review.doc".

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il tipo di dati utilizzati per registrare il processo di stampa.

</dd> <dt>

**pStatus**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica lo stato del processo di stampa. Questo membro deve essere controllato prima *dello stato* e, se *pStatus* è **null**, lo stato viene definito dal contenuto del membro di stato.

</dd> <dt>

**Status**
</dt> <dd>

Stato del processo. Il valore di questo membro può essere zero o una combinazione di uno o più dei valori seguenti. Un valore pari a zero indica che la coda di stampa è stata sospesa al termine dello spooling del documento.



| Valore                           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_stato processo \_ bloccato \_ DEVQ      | Il driver non è in grado di stampare il processo.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_stato processo \_ completato           | **Windows XP e versioni successive:** Il processo viene inviato alla stampante, ma il processo potrebbe non essere ancora stampato.<br/> Per ulteriori informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                                                                                                                                                           |
| \_stato processo \_ eliminato            | Il processo è stato eliminato.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_eliminazione dello stato del processo \_           | È in corso l'eliminazione del processo.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_errore di stato del processo \_              | Un errore è associato al processo.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| stato del processo \_ \_ offline            | La stampante è offline.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \_carta dello stato del processo \_           | Stampante esaurita.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \_stato processo \_ sospeso             | Il processo è stato sospeso.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| stato del processo \_ \_ stampato            | Il processo è stato stampato.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_stampa dello stato del processo \_           | Il processo viene stampato.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_riavvio stato \_ processo            | Il processo è stato riavviato.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| stato del processo \_ \_ mantenuto           | **Windows Vista e versioni successive:** Il processo è stato mantenuto nella coda di stampa e non può essere eliminato. Ciò può essere causato dai seguenti problemi:<br/> 1) il processo è stato mantenuto manualmente da una chiamata a SetJob e lo spooler è in attesa del rilascio del processo.<br/> 2) il processo non ha completato la stampa e deve terminare la stampa prima di poter essere eliminato automaticamente.<br/> Per ulteriori informazioni sui comandi dei processi di stampa, vedere [**SetJob**](setjob.md) .<br/> |
| \_spooling dello stato del processo \_           | Il processo sta effettuando lo spooling.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_ \_ intervento dell'utente sullo stato del processo \_ | La stampante presenta un errore che richiede all'utente di eseguire un'operazione.                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

**Priorità**
</dt> <dd>

Priorità del processo. Questo membro può essere uno dei valori seguenti o compreso tra 1 e 99 ( \_ priorità minima tramite \_ priorità massima).



| Valore         | Significato           |
|---------------|-------------------|
| \_priorità minima | Priorità minima. |
| \_priorità massima | Priorità massima. |
| \_priorità def | Priorità predefinita. |



 

</dd> <dt>

**Position**
</dt> <dd>

Posizione del processo nella coda di stampa.

</dd> <dt>

**TotalPages**
</dt> <dd>

Numero totale di pagine contenute nel documento. Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione di pagina.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

Numero di pagine stampate. Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione di pagina.

</dd> <dt>

**Inviata**
</dt> <dd>

Struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che specifica l'ora in cui è stato eseguito lo spooling del documento.

Questo valore di ora è in formato UTC (Universal Time Coordinate). È necessario convertirlo in un valore di ora locale prima di visualizzarlo. Per eseguire la conversione, è possibile usare la funzione [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) .

</dd> </dl>

## <a name="remarks"></a>Commenti

I monitoraggi porta che non supportano TrueEndOfJob imposteranno il processo in modo che lo stato del processo \_ \_ venga stampato subito dopo l'invio del processo alla stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ \_ Info processo \_ 1W** (Unicode) e **\_ informazioni sul processo \_ \_ 1a** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

