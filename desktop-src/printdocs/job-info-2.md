---
description: La \_ struttura di informazioni sul processo \_ 2 descrive un set completo di valori associati a un processo.
ms.assetid: 0cc61e35-4ac9-47bd-bb0d-ff43854bdee5
title: Struttura JOB_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_2
- _JOB_INFO_2A
- _JOB_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d6b582267afceb01fd7ced7d6d46144664bb9d2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233723"
---
# <a name="job_info_2-structure"></a>Struttura di informazioni sul processo \_ \_ 2

La struttura di **informazioni sul processo \_ \_ 2** descrive un set completo di valori associati a un processo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _JOB_INFO_2 {
  DWORD                JobId;
  LPTSTR               pPrinterName;
  LPTSTR               pMachineName;
  LPTSTR               pUserName;
  LPTSTR               pDocument;
  LPTSTR               pNotifyName;
  LPTSTR               pDatatype;
  LPTSTR               pPrintProcessor;
  LPTSTR               pParameters;
  LPTSTR               pDriverName;
  LPDEVMODE            pDevMode;
  LPTSTR               pStatus;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Status;
  DWORD                Priority;
  DWORD                Position;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                TotalPages;
  DWORD                Size;
  SYSTEMTIME           Submitted;
  DWORD                Time;
  DWORD                PagesPrinted;
} JOB_INFO_2, *PJOB_INFO_2;
```



## <a name="members"></a>Members

<dl> <dt>

**JobId**
</dt> <dd>

Valore dell'identificatore di processo.

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

**pNotifyName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome dell'utente che deve ricevere una notifica quando il processo è stato stampato o quando si verifica un errore durante la stampa del processo.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il tipo di dati utilizzati per registrare il processo di stampa.

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del processore di stampa da utilizzare per stampare il processo.

</dd> <dt>

**pParameters**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica i parametri del processore di stampa.

</dd> <dt>

**pDriverName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del driver della stampante da utilizzare per elaborare il processo di stampa.

</dd> <dt>

**pDevMode**
</dt> <dd>

Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che contiene i dati dell'ambiente e dell'inizializzazione del dispositivo per il driver della stampante.

</dd> <dt>

**pStatus**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica lo stato del processo di stampa. Questo membro deve essere controllato prima **dello stato** e, se **pStatus** è **null**, lo stato viene definito dal contenuto del membro di stato.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

Il valore di questo membro è **null**. Il recupero e l'impostazione dei descrittori di sicurezza del documento non sono supportati in questa versione.

</dd> <dt>

**Status**
</dt> <dd>

Stato del processo. Il membro può essere costituito da uno o più dei valori seguenti.

| Valore                           | Significato                                                      |
|---------------------------------|--------------------------------------------------------------|
| \_stato processo \_ bloccato \_ DEVQ      | Il driver non è in grado di stampare il processo.                             |
| \_stato processo \_ eliminato            | Il processo è stato eliminato.                                        |
| \_eliminazione dello stato del processo \_           | È in corso l'eliminazione del processo.                                        |
| \_errore di stato del processo \_              | Un errore è associato al processo.                         |
| stato del processo \_ \_ offline            | La stampante è offline.                                          |
| \_carta dello stato del processo \_           | Stampante esaurita.                                     |
| \_stato processo \_ sospeso             | Il processo è stato sospeso.                                               |
| stato del processo \_ \_ stampato            | Il processo è stato stampato.                                             |
| \_stampa dello stato del processo \_           | Il processo viene stampato.                                             |
| \_riavvio stato \_ processo            | Il processo è stato riavviato.                                      |
| \_spooling dello stato del processo \_           | Il processo sta effettuando lo spooling.                                             |
| \_ \_ intervento dell'utente sullo stato del processo \_ | La stampante presenta un errore che richiede all'utente di eseguire un'operazione. |



 

In Windows XP e nelle versioni successive di Windows è possibile utilizzare anche i valori seguenti:

| Valore                 | Significato                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| \_stato processo \_ completato | Il processo viene inviato alla stampante, ma potrebbe non essere ancora stampato. Per ulteriori informazioni, vedere la sezione Osservazioni. |
| stato del processo \_ \_ mantenuto | Il processo è stato mantenuto nella coda di stampa che segue la stampa.                              |



 

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

**StartTime**
</dt> <dd>

La prima volta che il processo può essere stampato.

</dd> <dt>

**UntilTime**
</dt> <dd>

Ora più recente in cui è possibile stampare il processo.

</dd> <dt>

**TotalPages**
</dt> <dd>

Numero di pagine necessarie per il processo. Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione di pagina.

</dd> <dt>

**Dimensioni**
</dt> <dd>

Dimensione, in byte, del processo.

</dd> <dt>

**Inviata**
</dt> <dd>

Struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che specifica l'ora in cui il processo è stato inviato.

Questo valore di ora è in formato UTC (Universal Time Coordinate). È necessario convertirlo in un valore di ora locale prima di visualizzarlo. Per eseguire la conversione, è possibile usare la funzione [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) .

</dd> <dt>

**Time**
</dt> <dd>

Tempo totale, in millisecondi, trascorso dall'inizio della stampa del processo.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

Numero di pagine stampate. Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione di pagina.

</dd> </dl>

## <a name="remarks"></a>Commenti

I monitoraggi porta che non supportano TrueEndOfJob imposteranno il processo in modo che lo stato del processo \_ \_ venga stampato subito dopo l'invio del processo alla stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ \_ Info processo \_ 2W** (Unicode) e **\_ informazioni sul processo \_ \_ 2a** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

