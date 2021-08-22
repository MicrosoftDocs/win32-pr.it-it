---
description: La struttura PRINTER NOTIFY INFO DATA identifica un campo di informazioni sul processo o sulla stampante \_ e fornisce i dati correnti per tale \_ \_ campo.
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: PRINTER_NOTIFY_INFO_DATA struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO_DATA,
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e26f7ed7f002801d3bbdf60708d83234231fe3333675a1c211488431868a4236
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731195"
---
# <a name="printer_notify_info_data-structure"></a>Struttura PRINTER \_ NOTIFY \_ INFO \_ DATA

La **struttura PRINTER NOTIFY INFO \_ \_ \_ DATA** identifica un campo di informazioni sul processo o sulla stampante e fornisce i dati correnti per tale campo.

La [**funzione FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) restituisce una struttura [**PRINTER NOTIFY \_ \_ INFO**](printer-notify-info.md) che contiene una matrice di **strutture PRINTER NOTIFY \_ \_ INFO \_** DATA.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_NOTIFY_INFO_DATA {
  WORD  Type;
  WORD  Field;
  DWORD Reserved;
  DWORD Id;
  union {
    DWORD  adwData[2];
    struct {
      DWORD  cbBuf;
      LPVOID pBuf;
    } Data;
  } NotifyData;
} PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA; ;
```



## <a name="members"></a>Members

<dl> <dt>

**Tipo**
</dt> <dd>

Indica il tipo di informazioni fornite. Questo membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                      | Significato                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**PROCESSO \_ TIPO \_ DI**</dt> <dt>NOTIFICA 0x01</dt> </dl>             | Indica che il membro **Field** specifica una costante JOB \_ NOTIFY \_ \_ \* FIELD.<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**STAMPANTE \_ TIPO \_ DI**</dt> <dt>NOTIFICA 0x00</dt> </dl> | Indica che il **membro Field** specifica una costante PRINTER \_ NOTIFY \_ \_ \* FIELD.<br/> |



 

</dd> <dt>

**Campo**
</dt> <dd>

Indica il campo modificato. Per un elenco dei valori possibili, vedere la sezione Osservazioni.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> <dt>

**Id**
</dt> <dd>

Indica l'identificatore del processo se il **membro Type** specifica JOB \_ NOTIFY \_ TYPE. Se il **membro Type** specifica PRINTER \_ NOTIFY \_ TYPE, questo membro non è definito.

</dd> <dt>

**NotifyData**
</dt> <dd>

Unione di informazioni sui dati in base ai **membri Type** **e Field.** Per una descrizione del tipo di dati associati a ogni campo, vedere la sezione Osservazioni.

<dl> <dt>

**adwData \[ 2\]**
</dt> <dd>

Matrice di due **valori DWORD.** Per i campi di informazioni che usano una sola **DWORD,** i dati si trova in **adwData** \[ \] 0.

</dd> <dt>

**Dati**
</dt> <dd> <dl> <dt>

**cbBuf**
</dt> <dd>

Indica le dimensioni, in byte, del buffer a cui punta **pBuf.**

</dd> <dt>

**pBuf**
</dt> <dd>

Puntatore a un buffer che contiene i dati correnti del campo.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Se il **membro Type** specifica PRINTER \_ NOTIFY \_ TYPE, il membro **Field** può essere uno dei valori seguenti.



<table>
<thead>
<tr class="header">
<th>Campo</th>
<th>Tipo di dati</th>
<th>Valore</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SERVER_NAME</td>
<td>Non supportata.</td>
<td>0x00</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINTER_NAME</td>
<td><strong>pBuf</strong> è un puntatore a una stringa con terminazione Null contenente il nome della stampante.</td>
<td>0x01</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SHARE_NAME</td>
<td><strong>pBuf</strong> è un puntatore a una stringa con terminazione Null che identifica il punto di condivisione per la stampante.</td>
<td>0x02</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PORT_NAME</td>
<td><strong>pBuf</strong> è un puntatore a una stringa con terminazione Null contenente il nome della porta in cui verranno stampati i processi di stampa. Se &quot; è selezionato Pool di &quot; stampanti, si tratta di un elenco delimitato da virgole di porte.</td>
<td>0x03</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_DRIVER_NAME</td>
<td><strong>pBuf</strong> è un puntatore a una stringa con terminazione Null contenente il nome del driver della stampante.</td>
<td>0x04</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_COMMENT</td>
<td><strong>pBuf</strong> è un puntatore a una stringa con terminazione Null contenente la nuova stringa di commento, che in genere è una breve descrizione della stampante.</td>
<td>0x05</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_LOCATION</td>
<td><strong>pBuf</strong> è un puntatore a una stringa con terminazione Null contenente la nuova posizione fisica della stampante, ad esempio &quot; Bldg. 38, Stanza 1164 &quot; ).</td>
<td>0x06</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEVMODE</td>
<td><strong>pBuf è</strong> un puntatore a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>una struttura DEVMODE</strong></a> che definisce i dati predefiniti della stampante, ad esempio l'orientamento della carta e la risoluzione.</td>
<td>0x07</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SEPFILE</td>
<td><strong>pBuf</strong> è un puntatore a una stringa con terminazione Null che specifica il nome del file usato per creare la pagina separatore. Questa pagina viene usata per separare i processi di stampa inviati alla stampante.</td>
<td>0x08</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</td>
<td><strong>pBuf</strong> è un puntatore a una stringa con terminazione Null che specifica il nome del processore di stampa utilizzato dalla stampante.</td>
<td>0x09</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PARAMETERS</td>
<td><strong>pBuf</strong> è un puntatore a una stringa con terminazione Null che specifica i parametri predefiniti del processore di stampa.</td>
<td>0x0A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DATATYPE</td>
<td><strong>pBuf</strong> è un puntatore a una stringa con terminazione Null che specifica il tipo di dati usato per registrare il processo di stampa.</td>
<td>0x0B</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</td>
<td><strong>pBuf</strong> è un puntatore a una <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> per la stampante. Il puntatore può essere <strong>NULL</strong> se non è presente alcun descrittore di sicurezza.</td>
<td>0x0C</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_ATTRIBUTES</td>
<td><strong>adwData</strong> [0] specifica gli attributi della stampante, che possono essere uno dei valori seguenti:<dl> PRINTER_ATTRIBUTE_QUEUED<br />
PRINTER_ATTRIBUTE_DIRECT<br />
PRINTER_ATTRIBUTE_DEFAULT<br />
PRINTER_ATTRIBUTE_SHARED<br />
</dl></td>
<td>0x0d</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PRIORITY</td>
<td><strong>adwData</strong> [0] specifica un valore di priorità che lo spooler usa per instradare i processi di stampa.</td>
<td>0x0E</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</td>
<td><strong>adwData</strong> [0] specifica il valore di priorità predefinito assegnato a ogni processo di stampa.</td>
<td>0x0F</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_START_TIME</td>
<td><strong>adwData</strong> [0] specifica la prima ora in cui la stampante stamperà un processo. Questo valore è specificato in minuti trascorsi dalle 12:00.</td>
<td>0x10</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_UNTIL_TIME</td>
<td><strong>adwData</strong> [0] specifica l'ora più recente in cui la stampante stamperà un processo. Questo valore è specificato in minuti trascorsi dalle 12:00.</td>
<td>0x11</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_STATUS</td>
<td><strong>adwData</strong> [0] specifica lo stato della stampante. Per un elenco dei valori possibili, vedere la <a href="printer-info-2.md"><strong>struttura PRINTER_INFO_2</strong></a> dati.</td>
<td>0x12</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_STATUS_STRING</td>
<td>Non supportata.</td>
<td>0x13</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_CJOBS</td>
<td><strong>adwData</strong> [0] specifica il numero di processi di stampa accodati per la stampante.</td>
<td>0x14</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_AVERAGE_PPM</td>
<td><strong>adwData</strong> [0] specifica il numero medio di pagine al minuto stampate sulla stampante.</td>
<td>0x15</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_TOTAL_PAGES</td>
<td>Non supportata.</td>
<td>0x16</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PAGES_PRINTED</td>
<td>Non supportata.</td>
<td>0x17</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_TOTAL_BYTES</td>
<td>Non supportata.</td>
<td>0x18</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_BYTES_PRINTED</td>
<td>Non supportata.</td>
<td>0x19</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_OBJECT_GUID</td>
<td>Questa proprietà viene impostata se il GUID dell'oggetto viene modificato.</td>
<td>0x1A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</td>
<td>Questa impostazione viene impostata se la connessione della stampante viene rinominata.</td>
<td>0x1B</td>
</tr>
</tbody>
</table>



 

Se il **membro Type** specifica JOB \_ NOTIFY \_ TYPE, il membro **Field** può essere uno dei valori seguenti.



| Campo                                    | Tipo di dati                                                                                                                                                                                                                                            | Valore |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| NOME DELLA STAMPANTE DEL CAMPO DI \_ \_ NOTIFICA DEL \_ \_ PROCESSO        | **pBuf** è un puntatore a una stringa con terminazione Null contenente il nome della stampante per cui viene spooling del processo.                                                                                                                                      | 0x00  |
| JOB \_ NOTIFY \_ FIELD \_ MACHINE \_ NAME        | **pBuf** è un puntatore a una stringa con terminazione Null che specifica il nome del computer che ha creato il processo di stampa.                                                                                                                                    | 0x01  |
| NOME \_ DELLA PORTA DEL CAMPO DI NOTIFICA DEL \_ \_ \_ PROCESSO           | **pBuf** è un puntatore a una stringa con terminazione Null che identifica le porte usate per trasmettere i dati alla stampante. Se una stampante è connessa a più porte, i nomi delle porte sono separati da virgole (ad esempio, "LPT1:,LPT2:,LPT3:"). | 0x02  |
| NOME \_ UTENTE DEL CAMPO \_ \_ JOB NOTIFY \_           | **pBuf** è un puntatore a una stringa con terminazione Null che specifica il nome dell'utente che ha inviato il processo di stampa.                                                                                                                                           | 0x03  |
| NOME \_ DI NOTIFICA DEL CAMPO DI NOTIFICA DEL \_ \_ \_ PROCESSO         | **pBuf** è un puntatore a una stringa con terminazione Null che specifica il nome dell'utente che deve ricevere una notifica quando il processo è stato stampato o quando si verifica un errore durante la stampa del processo.                                                              | 0x04  |
| TIPO DI \_ DATI DEL CAMPO DI NOTIFICA DEL \_ \_ PROCESSO             | **pBuf** è un puntatore a una stringa con terminazione Null che specifica il tipo di dati utilizzato per registrare il processo di stampa.                                                                                                                                         | 0x05  |
| PROCESSORE \_ DI STAMPA PER LA NOTIFICA DEI \_ \_ \_ PROCESSI     | **pBuf** è un puntatore a una stringa con terminazione Null che specifica il nome del processore di stampa da usare per stampare il processore.                                                                                                                           | 0x06  |
| PARAMETRI DEI \_ CAMPI DI NOTIFICA DEL \_ \_ PROCESSO           | **pBuf** è un puntatore a una stringa con terminazione Null che specifica i parametri del processore di stampa.                                                                                                                                                            | 0x07  |
| NOME \_ DEL DRIVER DI CAMPO DI NOTIFICA DEL \_ \_ \_ PROCESSO         | **pBuf** è un puntatore a una stringa con terminazione Null che specifica il nome del driver della stampante da usare per elaborare il processo di stampa.                                                                                                           | 0x08  |
| DEVMODE \_ DEL CAMPO DI NOTIFICA DEL \_ \_ PROCESSO              | **pBuf è** un puntatore a [**una struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che contiene i dati di inizializzazione del dispositivo e dell'ambiente per il driver della stampante.                                                                                                        | 0x09  |
| STATO \_ DEL CAMPO NOTIFICA \_ \_ PROCESSO               | **adwData** \[ 0 \] specifica lo stato del processo. Per un elenco dei valori possibili, vedere la [**struttura JOB \_ INFO \_ 2.**](job-info-2.md)                                                                                                                        | 0x0A  |
| STRINGA DI \_ STATO DEL CAMPO DI NOTIFICA DEL \_ \_ \_ PROCESSO       | **pBuf** è un puntatore a una stringa con terminazione Null che specifica lo stato del processo di stampa.                                                                                                                                                           | 0x0B  |
| DESCRITTORE \_ DI SICUREZZA DEI CAMPI DI NOTIFICA DEL \_ \_ \_ PROCESSO | Non supportata.                                                                                                                                                                                                                                          | 0x0C  |
| DOCUMENTO \_ SUL CAMPO DI NOTIFICA DEL \_ \_ PROCESSO             | **pBuf** è un puntatore a una stringa con terminazione Null che specifica il nome del processo di stampa, ad esempio "MS-WORD: Review.doc").                                                                                                                        | 0x0d  |
| PRIORITÀ \_ DEI CAMPI DI NOTIFICA DEL \_ \_ PROCESSO             | **adwData** \[ 0 \] specifica la priorità del processo.                                                                                                                                                                                                           | 0x0E  |
| POSIZIONE \_ DEL CAMPO DI NOTIFICA DEL \_ \_ PROCESSO             | **adwData** \[ 0 \] specifica la posizione del processo nella coda di stampa.                                                                                                                                                                                      | 0x0F  |
| CAMPO \_ DI NOTIFICA DEL PROCESSO \_ \_ INVIATO            | **pBuf** è un puntatore a [**una struttura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che specifica l'ora di invio del processo.                                                                                                                          | 0x10  |
| ORA DI \_ INIZIO DEL CAMPO NOTIFICA \_ \_ \_ PROCESSO          | **adwData** \[ 0 \] specifica la prima ora in cui è possibile stampare il processo. Questo valore è specificato in minuti trascorsi dalle 12:00.                                                                                                                | 0x11  |
| CAMPO \_ NOTIFICA PROCESSO FINO \_ \_ \_ ALL'ORA          | **adwData** \[ 0 \] specifica l'ora più recente in cui è possibile stampare il processo. Questo valore è specificato in minuti trascorsi dalle 12:00.                                                                                                                  | 0x12  |
| ORA \_ DEL CAMPO NOTIFICA \_ \_ PROCESSO                 | **adwData** \[ 0 \] specifica il tempo totale, in secondi, trascorso dall'inizio della stampa del processo.                                                                                                                                                  | 0x13  |
| PAGINE TOTALI \_ \_ DEL CAMPO NOTIFICA \_ \_ PROCESSO         | **adwData** \[ 0 \] specifica le dimensioni, in pagine, del processo.                                                                                                                                                                                             | 0x14  |
| PAGINE \_ DEI CAMPI DI NOTIFICA DEL PROCESSO \_ \_ \_ STAMPATE       | **adwData** \[ 0 \] specifica il numero di pagine stampate.                                                                                                                                                                                      | 0x15  |
| BYTE \_ TOTALI CAMPO NOTIFICA \_ \_ \_ PROCESSO         | **adwData** \[ 0 \] specifica le dimensioni, in byte, del processo.                                                                                                                                                                                             | 0x16  |
| BYTE \_ DEI CAMPI DI NOTIFICA PROCESSO \_ \_ \_ STAMPATI       | **adwData** \[ 0 \] specifica il numero di byte stampati in questo processo. Per questo campo, l'oggetto notifica di modifica viene segnalato quando i byte vengono inviati alla stampante.                                                                      | 0x17  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL PROCESSO \_ 2**](job-info-2.md)
</dt> <dt>

[**INFORMAZIONI \_ STAMPANTE \_ 2**](printer-info-2.md)
</dt> <dt>

[**INFORMAZIONI DI \_ NOTIFICA \_ DELLA STAMPANTE**](printer-notify-info.md)
</dt> <dt>

[**DESCRITTORE \_ DI SICUREZZA**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**Systemtime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

