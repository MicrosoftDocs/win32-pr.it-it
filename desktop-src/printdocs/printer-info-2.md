---
description: La struttura PRINTER \_ INFO \_ 2 specifica informazioni dettagliate sulla stampante.
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: PRINTER_INFO_2 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_2
- _PRINTER_INFO_2A
- _PRINTER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1f7a2b871cc0181fbceab56e4ac14170bf46fa1b31081f4b4365ad7296ec2e85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600611"
---
# <a name="printer_info_2-structure"></a>Struttura PRINTER \_ INFO \_ 2

La **struttura PRINTER INFO \_ \_ 2** specifica informazioni dettagliate sulla stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_INFO_2 {
  LPTSTR               pServerName;
  LPTSTR               pPrinterName;
  LPTSTR               pShareName;
  LPTSTR               pPortName;
  LPTSTR               pDriverName;
  LPTSTR               pComment;
  LPTSTR               pLocation;
  LPDEVMODE            pDevMode;
  LPTSTR               pSepFile;
  LPTSTR               pPrintProcessor;
  LPTSTR               pDatatype;
  LPTSTR               pParameters;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Attributes;
  DWORD                Priority;
  DWORD                DefaultPriority;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                Status;
  DWORD                cJobs;
  DWORD                AveragePPM;
} PRINTER_INFO_2, *PPRINTER_INFO_2;
```



## <a name="members"></a>Members

<dl> <dt>

**pServerName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica il server che controlla la stampante. Se questa stringa è **NULL,** la stampante viene controllata in locale.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome della stampante.

</dd> <dt>

**pShareName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica il punto di condivisione per la stampante. Questa stringa viene usata solo se printer \_ La costante ATTRIBUTE \_ SHARED è stata impostata per il membro **Attributes.**

</dd> <dt>

**pPortName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica le porte utilizzate per trasmettere i dati alla stampante. Se una stampante è connessa a più di una porta, i nomi di ogni porta devono essere separati da virgole (ad esempio, "LPT1:,LPT2:,LPT3:").

</dd> <dt>

**pDriverName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del driver della stampante.

</dd> <dt>

**pComment**
</dt> <dd>

Puntatore a una stringa con terminazione Null che fornisce una breve descrizione della stampante.

</dd> <dt>

**pLocation**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica la posizione fisica della stampante, ad esempio "Bldg. 38, Room 1164").

</dd> <dt>

**pDevMode**
</dt> <dd>

Puntatore a una [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che definisce i dati predefiniti della stampante, ad esempio l'orientamento della carta e la risoluzione.

</dd> <dt>

**pSepFile**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del file utilizzato per creare la pagina del separatore. Questa pagina viene utilizzata per separare i processi di stampa inviati alla stampante.

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del processore di stampa utilizzato dalla stampante. È possibile usare la [**funzione EnumPrintProcessors**](enumprintprocessors.md) per ottenere un elenco dei processori di stampa installati in un server.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il tipo di dati utilizzato per registrare il processo di stampa. È possibile usare la [**funzione EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) per ottenere un elenco dei tipi di dati supportati da un processore di stampa specifico.

</dd> <dt>

**pParameters**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica i parametri predefiniti del processore di stampa.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

Puntatore a una [**struttura SECURITY \_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) per la stampante. Questo membro può essere **NULL.**

</dd> <dt>

**Attributes (Attributi)**
</dt> <dd>

Attributi della stampante. Questo membro può essere qualsiasi combinazione ragionevole dei valori seguenti.

| Valore                                   | Significato                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PRINTER \_ ATTRIBUTE \_ DIRECT              | Il processo viene inviato direttamente alla stampante (non è in stato di spooling).                                                                                                                                |
| ATTRIBUTO \_ PRINTER DO COMPLETE \_ \_ \_ FIRST | Se impostata e la stampante è impostata per lo spooling di stampa, tutti i processi che hanno completato lo spooling vengono pianificati per la stampa prima dei processi che non hanno completato lo spooling.                          |
| ATTRIBUTO \_ PRINTER \_ ENABLE \_ DEVQ        | Se impostato, **viene chiamato DevQueryPrint.** **DevQueryPrint potrebbe** non riuscire se le impostazioni del documento e della stampante non corrispondono. Se si imposta questo flag, i documenti non corrispondenti vengono mantenuti nella coda. |
| ATTRIBUTO \_ PRINTER \_ NASCOSTO              | Riservato.                                                                                                                                                                               |
| ATTRIBUTO \_ DELLA \_ STAMPANTE KEEPPRINTEDJOBS     | Se impostata, i processi vengono mantenuti dopo la stampa. Se non impostata, i processi vengono eliminati.                                                                                                               |
| ATTRIBUTO \_ PRINTER \_ LOCAL               | La stampante è una stampante locale.                                                                                                                                                             |
| PRINTER \_ ATTRIBUTE \_ NETWORK             | La stampante è una connessione alla stampante di rete.                                                                                                                                                |
| ATTRIBUTO \_ PRINTER \_ PUBBLICATO           | Indica se la stampante è pubblicata nel servizio directory.                                                                                                                    |
| ATTRIBUTO \_ STAMPANTE \_ IN CODA              | Se impostata, lo spooling della stampante viene avviato e la stampa viene avviata dopo lo spooling dell'ultima pagina. Se non è impostata e PRINTER ATTRIBUTE DIRECT non è impostata, la stampante viene \_ \_ spooling e stampa durante lo spooling.      |
| ATTRIBUTO \_ PRINTER \_ RAW \_ ONLY           | Indica che è possibile eseguire lo spooling solo dei processi di stampa con tipo di dati non elaborati.                                                                                                                            |
| ATTRIBUTO \_ STAMPANTE \_ CONDIVISO              | La stampante è condivisa.                                                                                                                                                                      |



 

In Windows XP e versioni successive di Windows, è anche possibile usare il valore seguente.

| Valore                   | Significato                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PRINTER \_ ATTRIBUTE \_ FAX | Se impostata, la stampante è una stampante fax. Questa proprietà può essere impostata solo [**da AddPrinter,**](addprinter.md)ma può essere recuperata da [**EnumPrinters**](enumprinters.md) e [**GetPrinter**](getprinter.md). |



 

In Windows Vista e versioni successive di Windows, è possibile usare anche i valori seguenti.

| Valore                               | Significato                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| NOME \_ DESCRITTIVO \_ DELL'ATTRIBUTO \_ PRINTER  | Un computer si è connesso a questa stampante e gli ha assegnato un nome descrittivo.           |
| PRINTER \_ ATTRIBUTE \_ MACHINE         | La stampante è una connessione per computer.                                             |
| UTENTE \_ DI CUI È STATO PUSH ATTRIBUTO \_ \_ STAMPANTE    | La stampante è stata installata usando i criteri utente Push Printer Connections.     |
| MACCHINA CON \_ PUSH \_ DELL'ATTRIBUTO \_ DELLA STAMPANTE | La stampante è stata installata utilizzando il criterio computer Push Printer Connections . |



 

In Windows Server 2003, è anche possibile usare il valore seguente.

| Valore                  | Significato                                                                 |
|------------------------|-------------------------------------------------------------------------|
| ATTRIBUTO \_ STAMPANTE \_ TS | Indica che la stampante è attualmente connessa tramite un server terminal. |



 

</dd> <dt>

**Priorità**
</dt> <dd>

Valore di priorità utilizzato dallo spooler per instradare i processi di stampa.

</dd> <dt>

**DefaultPriority**
</dt> <dd>

Valore di priorità predefinito assegnato a ogni processo di stampa.

</dd> <dt>

**StartTime**
</dt> <dd>

La prima ora in cui la stampante stamperà un processo. Questo valore è espresso come minuti trascorsi dalle 12:00 GMT (Ora di Greenwich).

</dd> <dt>

**UntilTime**
</dt> <dd>

Ora più recente in cui la stampante stamperà un processo. Questo valore è espresso come minuti trascorsi dalle 12:00 GMT (Ora di Greenwich).

</dd> <dt>

**Status**
</dt> <dd>

Stato della stampante. Questo membro può essere qualsiasi combinazione ragionevole dei valori seguenti.



| Valore                               | Significato                                                          |
|-------------------------------------|------------------------------------------------------------------|
| STATO \_ STAMPANTE \_ OCCUPATO               | La stampante è occupata.                                             |
| STATO \_ DELLA STAMPANTE PORTA \_ \_ APERTA         | La porta della stampante è aperta.                                        |
| ERRORE DI \_ STATO \_ DELLA STAMPANTE              | La stampante è in uno stato di errore.                                |
| INIZIALIZZAZIONE \_ \_ DELLO STATO DELLA STAMPANTE       | È in corso l'inizializzazione della stampante.                                     |
| STATO \_ DELLA STAMPANTE IO \_ \_ ACTIVE         | La stampante è in uno stato di input/output attivo                   |
| ALIMENTAZIONE \_ MANUALE DELLO STATO DELLA \_ \_ STAMPANTE       | La stampante è in uno stato di alimentazione manuale.                           |
| STATO \_ STAMPANTE \_ NESSUN \_ TONER          | La stampante ha esaurito il toner.                                     |
| STATO \_ STAMPANTE \_ NON \_ DISPONIBILE     | La stampante non è disponibile per la stampa.                       |
| STATO \_ DELLA STAMPANTE \_ OFFLINE            | La stampante non è in linea.                                          |
| MEMORIA \_ INSUFFICIENTE PER LO STATO DELLA \_ \_ \_ STAMPANTE    | Memoria insufficiente per la stampante.                               |
| BIN DI \_ OUTPUT DELLO STATO DELLA STAMPANTE \_ \_ \_ PIENO  | Il cassetto di uscita della stampante è pieno.                                |
| PAGINA \_ DI STATO DELLA STAMPANTE \_ \_ PUNT         | La stampante non può stampare la pagina corrente.                       |
| STATO DELLA \_ STAMPANTE \_ CARTA \_ INCEPPAMENTO         | La carta è inceppata nella stampante                                   |
| PRINTER \_ STATUS \_ PAPER \_ OUT         | La stampante è senza carta.                                     |
| PROBLEMA RELATIVO \_ ALLA CARTA DI STATO DELLA \_ \_ STAMPANTE     | La stampante presenta un problema di carta.                                 |
| STATO \_ DELLA STAMPANTE IN \_ PAUSA             | La stampante è in pausa.                                           |
| STATO DELLA \_ STAMPANTE IN ATTESA DI \_ \_ ELIMINAZIONE  | È in corso l'eliminazione della stampante.                                    |
| SALVATAGGIO ALIMENTAZIONE \_ STATO \_ \_ STAMPANTE        | La stampante è in modalità risparmio energia.                               |
| STAMPA DELLO \_ STATO DELLA \_ STAMPANTE           | La stampante sta stampando.                                         |
| ELABORAZIONE DELLO \_ STATO DELLA \_ STAMPANTE         | La stampante sta elaborando un processo di stampa.                           |
| SERVER DI \_ STATO \_ DELLA STAMPANTE \_ SCONOSCIUTO    | Lo stato della stampante è sconosciuto.                                   |
| TONER \_ STATO \_ STAMPANTE \_ BASSO         | Il toner della stampante è basso.                                     |
| INTERVENTO \_ DELL'UTENTE \_ SULLO STATO DELLA \_ STAMPANTE | La stampante presenta un errore che richiede all'utente di eseguire un'operazione. |
| STATO DELLA \_ STAMPANTE \_ IN ATTESA            | La stampante è in attesa.                                          |
| RISCALDAMENTO \_ DELLO STATO DELLA \_ \_ STAMPANTE        | La stampante è in fase di riscaldamento.                                       |



 

</dd> <dt>

**cJobs**
</dt> <dd>

Numero di processi di stampa accodati per la stampante.

</dd> <dt>

**AveragePPM**
</dt> <dd>

Numero medio di pagine al minuto stampate sulla stampante.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PRINTER \_ INFO \_ 2W** (Unicode) e **\_ PRINTER INFO \_ \_ 2A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**Enumprinters**](enumprinters.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 1**](printer-info-1.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 3**](printer-info-3.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 4**](printer-info-4.md)
</dt> <dt>

[**DESCRITTORE \_ DI SICUREZZA**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

