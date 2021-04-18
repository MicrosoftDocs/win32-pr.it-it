---
description: La \_ struttura Info stampante \_ 5 specifica informazioni dettagliate sulla stampante.
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: Struttura PRINTER_INFO_5 (winspool. h)
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
ms.openlocfilehash: 2ec207b60eca8cc20f6f24e2bb08bb1e3b191fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314990"
---
# <a name="printer_info_5-structure"></a>\_Struttura Info stampante \_ 5

La **struttura \_ Info stampante \_ 5** specifica informazioni dettagliate sulla stampante.

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

Puntatore a una stringa con terminazione null che specifica il nome della stampante.

</dd> <dt>

**pPortName**
</dt> <dd>

Puntatore a una stringa con terminazione null che identifica la porta o le porte utilizzate per trasmettere i dati alla stampante. Se una stampante è connessa a più di una porta, i nomi di ogni porta devono essere separati da virgole (ad esempio, "LPT1:, LPT2:, LPT3:").

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
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ \_ Info stampante \_ 5W** (Unicode) e **\_ \_ Info stampante \_ 5a** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**\_Informazioni stampante \_ 1**](printer-info-1.md)
</dt> <dt>

[**\_Informazioni stampante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Informazioni stampante \_ 3**](printer-info-3.md)
</dt> <dt>

[**\_Informazioni stampante \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




