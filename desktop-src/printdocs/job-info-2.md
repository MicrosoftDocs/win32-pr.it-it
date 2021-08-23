---
description: La struttura \_ JOB INFO \_ 2 descrive un set completo di valori associati a un processo.
ms.assetid: 0cc61e35-4ac9-47bd-bb0d-ff43854bdee5
title: JOB_INFO_2 struttura (Winspool.h)
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
ms.openlocfilehash: 2c41ea46f9226990fc28b5c629f3b36785d4bf4b0ee6ecd6e39477251f765b3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971320"
---
# <a name="job_info_2-structure"></a>Struttura JOB \_ INFO \_ 2

La **struttura JOB INFO \_ \_ 2** descrive un set completo di valori associati a un processo.

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

**Jobid**
</dt> <dd>

Valore dell'identificatore del processo.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome della stampante per cui viene spooling il processo.

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

Puntatore a una stringa con terminazione Null che specifica il nome del processo di stampa, ad esempio "MS-WORD: Review.doc".

</dd> <dt>

**pNotifyName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome dell'utente che deve ricevere una notifica quando il processo è stato stampato o quando si verifica un errore durante la stampa del processo.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il tipo di dati utilizzato per registrare il processo di stampa.

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del processore di stampa da utilizzare per stampare il processo.

</dd> <dt>

**pParameters**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica i parametri del processore di stampa.

</dd> <dt>

**pDriverName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del driver della stampante da utilizzare per elaborare il processo di stampa.

</dd> <dt>

**pDevMode**
</dt> <dd>

Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che contiene i dati di inizializzazione del dispositivo e dell'ambiente per il driver della stampante.

</dd> <dt>

**pStatus**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica lo stato del processo di stampa. Questo membro deve essere controllato prima di **Status** e, se **pStatus** è **NULL,** lo stato è definito dal contenuto del membro Status.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

Il valore di questo membro è **NULL.** Il recupero e l'impostazione dei descrittori di sicurezza dei documenti non sono supportati in questa versione.

</dd> <dt>

**Status**
</dt> <dd>

Stato del processo. Questo membro può essere uno o più dei valori seguenti.

| Valore                           | Significato                                                      |
|---------------------------------|--------------------------------------------------------------|
| STATO \_ PROCESSO \_ BLOCCATO \_ DEVQ      | Il driver non può stampare il processo.                             |
| STATO \_ PROCESSO \_ ELIMINATO            | Il processo è stato eliminato.                                        |
| ELIMINAZIONE DELLO \_ STATO DEL \_ PROCESSO           | È in corso l'eliminazione del processo.                                        |
| ERRORE \_ DI STATO DEL \_ PROCESSO              | Al processo è associato un errore.                         |
| STATO \_ DEL PROCESSO \_ OFFLINE            | La stampante è offline.                                          |
| DOCUMENTO \_ SULLO STATO DEL \_ PROCESSO           | La stampante è senza carta.                                     |
| STATO \_ DEL PROCESSO \_ SOSPESO             | Il processo è in pausa.                                               |
| STATO \_ DEL \_ PROCESSO STAMPATO            | Il processo è stato stampato.                                             |
| STAMPA \_ DELLO STATO DEL \_ PROCESSO           | Il processo è in corso di stampa.                                             |
| RIAVVIO \_ STATO \_ PROCESSO            | Il processo è stato riavviato.                                      |
| \_ \_ SPOOLING DELLO STATO DEL PROCESSO           | È in esecuzione lo spooling del processo.                                             |
| INTERVENTO \_ \_ DELL'UTENTE SULLO STATO DEL \_ PROCESSO | La stampante presenta un errore che richiede all'utente di eseguire un'operazione. |



 

In Windows XP e versioni successive di Windows, è anche possibile usare i valori seguenti:

| Valore                 | Significato                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| STATO \_ PROCESSO \_ COMPLETATO | Il processo viene inviato alla stampante, ma potrebbe non essere ancora stampato. Per ulteriori informazioni, vedere la sezione Osservazioni. |
| STATO \_ DEL \_ PROCESSO MANTENUTO | Il processo è stato mantenuto nella coda di stampa dopo la stampa.                              |



 

</dd> <dt>

**Priorità**
</dt> <dd>

Priorità del processo. Questo membro può essere uno dei valori seguenti o compreso nell'intervallo compreso tra 1 e 99 (da MIN \_ PRIORITY a MAX \_ PRIORITY).



| Valore         | Significato           |
|---------------|-------------------|
| MIN \_ PRIORITY | Priorità minima. |
| MAX \_ PRIORITY | Priorità massima. |
| DEF \_ PRIORITY | Priorità predefinita. |



 

</dd> <dt>

**Position**
</dt> <dd>

Posizione del processo nella coda di stampa.

</dd> <dt>

**StartTime**
</dt> <dd>

La prima volta in cui è possibile stampare il processo.

</dd> <dt>

**UntilTime**
</dt> <dd>

Ora dell'ultima stampa del processo.

</dd> <dt>

**TotalPages**
</dt> <dd>

Numero di pagine necessarie per il processo. Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione della pagina.

</dd> <dt>

**Dimensioni**
</dt> <dd>

Dimensione, in byte, del processo.

</dd> <dt>

**Inviata**
</dt> <dd>

Struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che specifica l'ora di invio del processo.

Questo valore di ora è in formato UTC (Universal Time Coordinate). È consigliabile convertirlo in un valore di ora locale prima di visualizzarlo. È possibile usare la [**funzione FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) per eseguire la conversione.

</dd> <dt>

**Time**
</dt> <dd>

Tempo totale, in millisecondi, trascorso dall'inizio della stampa del processo.

</dd> <dt>

**Pagine stampate**
</dt> <dd>

Numero di pagine stampate. Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione della pagina.

</dd> </dl>

## <a name="remarks"></a>Commenti

I monitoraggi delle porte che non supportano TrueEndOfJob impostano il processo come JOB STATUS PRINTED subito dopo l'invio \_ \_ del processo alla stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ JOB \_ INFO \_ 2W** (Unicode) e **\_ JOB INFO \_ \_ 2A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

