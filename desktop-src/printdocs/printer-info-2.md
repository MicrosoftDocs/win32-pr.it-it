---
description: La \_ struttura Printer Info \_ 2 specifica informazioni dettagliate sulla stampante.
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: Struttura PRINTER_INFO_2 (winspool. h)
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
ms.openlocfilehash: b299cb1bbdd3ac2475b7a9f2b600bcd9652246d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529755"
---
# <a name="printer_info_2-structure"></a>\_Struttura Info stampante \_ 2

La struttura **Printer \_ info \_ 2** specifica informazioni dettagliate sulla stampante.

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

Puntatore a una stringa con terminazione null che identifica il server che controlla la stampante. Se la stringa è **null**, la stampante viene controllata localmente.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome della stampante.

</dd> <dt>

**pShareName**
</dt> <dd>

Puntatore a una stringa con terminazione null che identifica il punto di condivisione per la stampante. Questa stringa viene utilizzata solo se la stampante \_ \_Per il membro **Attributes** è stata impostata la costante condivisa dell'attributo.

</dd> <dt>

**pPortName**
</dt> <dd>

Puntatore a una stringa con terminazione null che identifica la porta o le porte utilizzate per trasmettere i dati alla stampante. Se una stampante è connessa a più di una porta, i nomi di ogni porta devono essere separati da virgole (ad esempio, "LPT1:, LPT2:, LPT3:").

</dd> <dt>

**pDriverName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del driver della stampante.

</dd> <dt>

**pComment**
</dt> <dd>

Puntatore a una stringa con terminazione null che fornisce una breve descrizione della stampante.

</dd> <dt>

**pLocation**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica la posizione fisica della stampante, ad esempio "Bldg. 38, stanza 1164 ").

</dd> <dt>

**pDevMode**
</dt> <dd>

Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che definisce i dati predefiniti della stampante, ad esempio l'orientamento della carta e la risoluzione.

</dd> <dt>

**pSepFile**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del file utilizzato per creare la pagina separatore. Questa pagina viene utilizzata per separare i processi di stampa inviati alla stampante.

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del processore di stampa utilizzato dalla stampante. È possibile utilizzare la funzione [**EnumPrintProcessors**](enumprintprocessors.md) per ottenere un elenco dei processori di stampa installati in un server.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il tipo di dati utilizzato per registrare il processo di stampa. È possibile utilizzare la funzione [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) per ottenere un elenco dei tipi di dati supportati da uno specifico processore di stampa.

</dd> <dt>

**pParameters**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica i parametri predefiniti del processore di stampa.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

Puntatore a una struttura [**di \_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) per la stampante. Questo membro può essere **null**.

</dd> <dt>

**Attributes (Attributi)**
</dt> <dd>

Attributi della stampante. Questo membro può essere qualsiasi combinazione ragionevole dei valori seguenti.

| Valore                                   | Significato                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_attributo stampante \_ diretto              | Il processo viene inviato direttamente alla stampante, ovvero non è stato eseguito lo spooling.                                                                                                                                |
| \_prima operazione di attributo stampante \_ \_ completata \_ | Se set e Printer sono impostati per lo spooling di stampa, tutti i processi che hanno completato lo spooling sono pianificati per la stampa prima dei processi che non hanno completato lo spooling.                          |
| \_attributo stampante \_ Abilita \_ DEVQ        | Se impostato, viene chiamato **DevQueryPrint** . **DevQueryPrint** può avere esito negativo se le configurazioni di documento e stampante non corrispondono. Impostando questo flag, i documenti non corrispondenti verranno mantenuti nella coda. |
| attributo della stampante \_ \_ nascosto              | Riservato.                                                                                                                                                                               |
| \_KEEPPRINTEDJOBS attributo \_ stampante     | Se impostata, i processi vengono conservati dopo la stampa. Se non impostata, i processi vengono eliminati.                                                                                                               |
| \_attributo stampante \_ locale               | La stampante è una stampante locale.                                                                                                                                                             |
| \_rete attributi \_ stampante             | La stampante è una connessione alla stampante di rete.                                                                                                                                                |
| \_attributo Printer \_ pubblicato           | Indica se la stampante è pubblicata nel servizio directory.                                                                                                                    |
| attributo stampante in \_ \_ coda              | Se impostato, lo spooler della stampante e la stampa viene avviata dopo lo spooling dell'ultima pagina. Se non è impostato e \_ l'attributo della stampante \_ Direct non è impostato, la stampante esegue lo spooling e la stampa durante lo spooling.      |
| \_attributo stampante \_ \_ solo RAW           | Indica che è possibile spoolare solo i processi di stampa con tipi di dati non elaborati.                                                                                                                            |
| \_attributo stampante \_ condiviso              | La stampante è condivisa.                                                                                                                                                                      |



 

In Windows XP e nelle versioni successive di Windows è possibile utilizzare anche il valore seguente.

| Valore                   | Significato                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Fax attributo \_ stampante | Se impostato, Printer è una stampante fax. Questo può essere impostato solo da [**AddPrinter**](addprinter.md), ma può essere recuperato da [**EnumPrinters**](enumprinters.md) e [**GetPrinter**](getprinter.md). |



 

In Windows Vista e nelle versioni successive di Windows è possibile utilizzare anche i valori seguenti.

| Valore                               | Significato                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| \_ \_ nome descrittivo dell'attributo Printer \_  | Un computer si è connesso a questa stampante e ne è stato assegnato un nome descrittivo.           |
| \_computer attributo \_ stampante         | La stampante è una connessione per computer.                                             |
| \_ \_ utente push attributo \_ stampante    | La stampante è stata installata usando i criteri utente per le connessioni push Printer.     |
| \_ \_ computer push degli attributi stampante \_ | La stampante è stata installata usando i criteri del computer connessioni stampante push. |



 

In Windows Server 2003 è possibile usare anche il valore seguente.

| Valore                  | Significato                                                                 |
|------------------------|-------------------------------------------------------------------------|
| \_attributo stampante \_ TS | Indica che la stampante è attualmente connessa tramite un server terminal. |



 

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

Data e ora della prima stampa di un processo da parte della stampante. Questo valore è espresso come minuti trascorsi dall'ora 12:00 GMT (Greenwich Mean Time).

</dd> <dt>

**UntilTime**
</dt> <dd>

Ora più recente in cui la stampante stampa un processo. Questo valore è espresso come minuti trascorsi dall'ora 12:00 GMT (Greenwich Mean Time).

</dd> <dt>

**Status**
</dt> <dd>

Stato della stampante. Questo membro può essere qualsiasi combinazione ragionevole dei valori seguenti.



| Valore                               | Significato                                                          |
|-------------------------------------|------------------------------------------------------------------|
| stato della stampante \_ \_ occupato               | La stampante è occupata.                                             |
| \_sportello dello stato della stampante \_ \_ aperto         | Lo sportello della stampante è aperto.                                        |
| \_errore di stato della stampante \_              | La stampante è in uno stato di errore.                                |
| \_inizializzazione dello stato della stampante \_       | È in corso l'inizializzazione della stampante.                                     |
| \_io stato \_ stampante \_ attivo         | La stampante è in uno stato di input/output attivo                   |
| \_feed manuale dello stato della stampante \_ \_       | La stampante è in uno stato di avanzamento manuale.                           |
| \_stato stampante \_ senza \_ toner          | La stampante ha esaurito il toner.                                     |
| stato della stampante \_ \_ non \_ disponibile     | La stampante non è disponibile per la stampa.                       |
| stato della stampante \_ \_ offline            | La stampante non è in linea.                                          |
| \_ \_ \_ \_ memoria insufficiente per lo stato della stampante    | Memoria esaurita per la stampante.                               |
| \_Cestino di \_ output stato stampante \_ \_ completo  | Il cassetto di uscita della stampante è pieno.                                |
| pagina di stato della stampante \_ \_ \_ Punt         | La stampante non è in grado di stampare la pagina corrente.                       |
| \_ \_ inceppamento carta stato stampante \_         | La carta è bloccata nella stampante                                   |
| \_carta dello stato della stampante in \_ \_ uscita         | La stampante ha esaurito la carta.                                     |
| \_ \_ problema relativo alla carta di stato della stampante \_     | La stampante presenta un problema relativo alla carta.                                 |
| stato della stampante \_ \_ sospeso             | La stampante è sospesa.                                           |
| \_stato stampante \_ in attesa di \_ eliminazione  | È in corso l'eliminazione della stampante.                                    |
| \_risparmio di stato della stampante \_ \_        | La stampante è in modalità risparmio energia.                               |
| \_stampa dello stato della stampante \_           | Viene stampata la stampante.                                         |
| \_elaborazione dello stato della stampante \_         | La stampante sta elaborando un processo di stampa.                           |
| \_Server stato \_ stampante \_ sconosciuto    | Lo stato della stampante è sconosciuto.                                   |
| \_ \_ toner stato stampante \_ basso         | Il toner della stampante è insufficiente.                                     |
| \_ \_ intervento dell'utente sullo stato della stampante \_ | La stampante presenta un errore che richiede all'utente di eseguire un'operazione. |
| stato della stampante \_ \_ in attesa            | La stampante è in attesa.                                          |
| \_stato della \_ stampante \_ attivo        | La stampante è in fase di riscaldamento.                                       |



 

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
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ \_ Info stampante \_ 2W** (Unicode) e **\_ \_ Info stampante \_ 2a** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**\_Informazioni stampante \_ 1**](printer-info-1.md)
</dt> <dt>

[**\_Informazioni stampante \_ 3**](printer-info-3.md)
</dt> <dt>

[**\_Informazioni stampante \_ 4**](printer-info-4.md)
</dt> <dt>

[**descrittore di sicurezza \_**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

