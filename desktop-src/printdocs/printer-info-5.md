---
description: La struttura PRINTER \_ INFO \_ 5 specifica informazioni dettagliate sulla stampante.
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: PRINTER_INFO_5 struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_5
- _PRINTER_INFO_5A
- _PRINTER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ef50f3bfd83a0c2dd49eb0a15cdae31f25588106926e606887292c705602dd44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731422"
---
# <a name="printer_info_5-structure"></a>Struttura PRINTER \_ INFO \_ 5

La **struttura PRINTER INFO \_ \_ 5** specifica informazioni dettagliate sulla stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_INFO_5 {
  LPTSTR pPrinterName;
  LPTSTR pPortName;
  DWORD  Attributes;
  DWORD  DeviceNotSelectedTimeout;
  DWORD  TransmissionRetryTimeout;
} PRINTER_INFO_5, *PPRINTER_INFO_5;
```



## <a name="members"></a>Members

<dl> <dt>

**pPrinterName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome della stampante.

</dd> <dt>

**pPortName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica le porte utilizzate per trasmettere i dati alla stampante. Se una stampante è connessa a più porte, i nomi di ogni porta devono essere separati da virgole (ad esempio, "LPT1:,LPT2:,LPT3:").

</dd> <dt>

**Attributes (Attributi)**
</dt> <dd>

Attributi della stampante. Questo membro può essere qualsiasi combinazione ragionevole dei valori seguenti.

| Valore                                   | Significato                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PRINTER \_ ATTRIBUTE \_ DIRECT              | Il processo viene inviato direttamente alla stampante (non è in spooling).                                                                                                                                |
| ATTRIBUTO \_ PRINTER DO COMPLETE \_ \_ \_ FIRST | Se impostata e la stampante è impostata per lo spooling di stampa, tutti i processi che hanno completato lo spooling vengono pianificati per la stampa prima dei processi che non hanno completato lo spooling.                          |
| ATTRIBUTO \_ PRINTER \_ ENABLE \_ DEVQ        | Se impostato, **viene chiamato DevQueryPrint.** **DevQueryPrint potrebbe** non riuscire se le impostazioni del documento e della stampante non corrispondono. Se si imposta questo flag, i documenti non corrispondenti vengono mantenuti nella coda. |
| ATTRIBUTO \_ PRINTER \_ HIDDEN              | Riservato.                                                                                                                                                                               |
| ATTRIBUTO \_ DELLA \_ STAMPANTE KEEPPRINTEDJOBS     | Se impostato, i processi vengono mantenuti dopo la stampa. Se non è impostata, i processi vengono eliminati.                                                                                                               |
| PRINTER \_ ATTRIBUTE \_ LOCAL               | La stampante è una stampante locale.                                                                                                                                                             |
| RETE \_ DEGLI ATTRIBUTI DELLA \_ STAMPANTE             | La stampante è una connessione stampante di rete.                                                                                                                                                |
| ATTRIBUTO \_ PRINTER \_ PUBBLICATO           | Indica se la stampante è pubblicata nel servizio directory.                                                                                                                    |
| ATTRIBUTO \_ PRINTER \_ IN CODA              | Se impostata, la stampante si spoolererà e inizierà la stampa dopo lo spooling dell'ultima pagina. Se non è impostato e PRINTER ATTRIBUTE DIRECT non è impostato, la stampante \_ viene \_ spooling e stampa durante lo spooling.      |
| SOLO \_ ATTRIBUTO \_ PRINTER RAW \_           | Indica che è possibile eseguire lo spooling solo dei processi di stampa con tipo di dati non elaborati.                                                                                                                            |
| ATTRIBUTO \_ PRINTER \_ CONDIVISO              | La stampante è condivisa.                                                                                                                                                                      |



 

In Windows XP e versioni successive di Windows, è possibile usare anche il valore seguente.

| Valore                   | Significato                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FAX \_ ATTRIBUTO \_ STAMPANTE | Se impostata, la stampante è una stampante fax. Questa proprietà può essere impostata solo [**da AddPrinter**](addprinter.md), ma può essere recuperata da [**EnumPrinters**](enumprinters.md) e [**GetPrinter**](getprinter.md). |



 

In Windows Vista e versioni successive di Windows, è possibile usare anche i valori seguenti.

| Valore                               | Significato                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| NOME \_ DESCRITTIVO \_ DELL'ATTRIBUTO \_ DELLA STAMPANTE  | Un computer è connesso a questa stampante e gli ha assegnato un nome descrittivo.           |
| PRINTER \_ ATTRIBUTE \_ MACHINE         | La stampante è una connessione per computer.                                             |
| UTENTE \_ CON \_ PUSH \_ DELL'ATTRIBUTO DELLA STAMPANTE    | La stampante è stata installata usando i criteri utente Push Printer Connections.     |
| MACCHINA CON \_ PUSH DEGLI ATTRIBUTI DELLA \_ \_ STAMPANTE | La stampante è stata installata usando i criteri del computer Push Printer Connections. |



 

</dd> <dt>

**DeviceNotSelectedTimeout**
</dt> <dd>

Questo valore non viene utilizzato.

</dd> <dt>

**TransmissionRetryTimeout**
</dt> <dd>

Questo valore non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PRINTER \_ INFO \_ 5W** (Unicode) e **\_ PRINTER INFO \_ \_ 5A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Enumprinters**](enumprinters.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> <dt>

[**INFORMAZIONI \_ STAMPANTE \_ 1**](printer-info-1.md)
</dt> <dt>

[**INFORMAZIONI \_ STAMPANTE \_ 2**](printer-info-2.md)
</dt> <dt>

[**INFORMAZIONI \_ STAMPANTE \_ 3**](printer-info-3.md)
</dt> <dt>

[**INFORMAZIONI \_ STAMPANTE \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




