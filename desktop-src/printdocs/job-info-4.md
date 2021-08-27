---
description: Descrive un set completo di valori associati a un processo e supporta file di spooling di grandi dimensioni con dimensioni espresse con 64 bit.
ms.assetid: 90932ae2-ea9e-43bc-9a1d-c68223f6d0ee
title: JOB_INFO_4 struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_4
- _JOB_INFO_4A
- _JOB_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: dd338b4e6e486c59bfdac705b68c72c56eafb96c9f4e1899e9b4cb3b294791de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091921"
---
# <a name="job_info_4-structure"></a>Struttura JOB \_ INFO \_ 4

Descrive un set completo di valori associati a un processo e supporta file di spooling di grandi dimensioni con dimensioni espresse con 64 bit.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _JOB_INFO_4 {
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
  LONG                 SizeHigh;
} JOB_INFO_4, *PJOB_INFO_4;
```



## <a name="members"></a>Members

<dl> <dt>

**Jobid**
</dt> <dd>

Valore dell'identificatore del processo.

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

Puntatore a una [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che contiene i dati di inizializzazione del dispositivo e dell'ambiente per il driver della stampante.

</dd> <dt>

**pStatus**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica lo stato del processo di stampa. Questo membro deve essere controllato prima di **Status** e, se **pStatus** è **NULL,** lo stato viene definito dal contenuto del membro Status.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

Il valore di questo membro è **NULL.** Il recupero e l'impostazione dei descrittori di sicurezza dei documenti non sono supportati in questa versione.

</dd> <dt>

**Status**
</dt> <dd>

Stato del processo. Questo membro può essere uno o più dei valori seguenti:

| Valore                           | Significato                                                      |
|---------------------------------|--------------------------------------------------------------|
| STATO \_ DEL PROCESSO BLOCCATO \_ \_ DEVQ      | Il driver non può stampare il processo.                             |
| STATO \_ PROCESSO \_ ELIMINATO            | Il processo è stato eliminato.                                        |
| ELIMINAZIONE DELLO \_ STATO DEL \_ PROCESSO           | È in corso l'eliminazione del processo.                                        |
| ERRORE \_ DI STATO DEL \_ PROCESSO              | Al processo è associato un errore.                         |
| STATO \_ DEL PROCESSO \_ OFFLINE            | La stampante è offline.                                          |
| DOCUMENTO \_ SULLO STATO DEL \_ PROCESSO           | La stampante non è cartacea.                                     |
| STATO \_ DEL \_ PROCESSO SOSPESO             | Il processo è sospeso.                                               |
| STATO \_ DEL \_ PROCESSO STAMPATO            | Il processo è stato stampato.                                             |
| STAMPA \_ DELLO STATO DEL \_ PROCESSO           | Il processo è in corso di stampa.                                             |
| RIAVVIO \_ DELLO STATO \_ DEL PROCESSO            | Il processo è stato riavviato.                                      |
| \_ \_ SPOOLING DELLO STATO DEL PROCESSO           | È in esecuzione lo spooling del processo.                                             |
| INTERVENTO \_ DELL'UTENTE \_ SULLO STATO DEL \_ PROCESSO | La stampante presenta un errore che richiede all'utente di eseguire un'operazione. |



 

In Windows XP e versioni successive di Windows, è possibile usare anche i valori seguenti:

| Valore                 | Significato                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| STATO \_ DEL \_ PROCESSO COMPLETATO | Il processo viene inviato alla stampante, ma potrebbe non essere ancora stampato. Per ulteriori informazioni, vedere la sezione Osservazioni. |
| STATO \_ DEL \_ PROCESSO MANTENUTO | Il processo è stato mantenuto nella coda di stampa dopo la stampa.                              |



 

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

**StartTime**
</dt> <dd>

Data e ora meno recente in cui è possibile stampare il processo.

</dd> <dt>

**UntilTime**
</dt> <dd>

Ora più recente in cui è possibile stampare il processo.

</dd> <dt>

**TotalPages**
</dt> <dd>

Numero di pagine necessarie per il processo. Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione della pagina.

</dd> <dt>

**Dimensioni**
</dt> <dd>

Quattro byte inferiori delle dimensioni, in byte, del processo. Vedere anche il **membro SizeHigh** di seguito.

</dd> <dt>

**Inviata**
</dt> <dd>

Struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che specifica l'ora di invio del processo.

Questo valore di ora è in formato UTC (Universal Time Coordinate). È necessario convertirlo in un valore di ora locale prima di visualizzarlo. È possibile usare la [**funzione FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) per eseguire la conversione.

</dd> <dt>

**Time**
</dt> <dd>

Tempo totale, in millisecondi, trascorso dall'inizio della stampa del processo.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

Numero di pagine stampate. Questo valore può essere zero se il processo di stampa non contiene informazioni di delimitazione della pagina.

</dd> <dt>

**SizeHigh**
</dt> <dd>

Quattro byte superiori delle dimensioni, in byte, del processo. Vedere anche il **membro Size** precedente.

</dd> </dl>

## <a name="remarks"></a>Commenti

I monitoraggi delle porte che non supportano TrueEndOfJob impostano il processo come JOB STATUS PRINTED immediatamente dopo l'invio \_ \_ del processo alla stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Winspool.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ JOB \_ INFO \_ 4W** (Unicode) e **\_ JOB INFO \_ \_ 4A** (ANSI)<br/>               |



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

 

