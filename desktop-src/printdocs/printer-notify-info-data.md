---
description: La \_ struttura di \_ dati notifica informazioni stampante \_ identifica un campo informazioni sul processo o sulla stampante e fornisce i dati correnti per quel campo.
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: Struttura PRINTER_NOTIFY_INFO_DATA (winspool. h)
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
ms.openlocfilehash: 4c76ffe70a8388e920b5f8576830e31ed23edc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231948"
---
# <a name="printer_notify_info_data-structure"></a>\_ \_ \_ Struttura dei dati di notifica della stampante

La struttura di **\_ \_ \_ dati notifica informazioni stampante** identifica un campo informazioni sul processo o sulla stampante e fornisce i dati correnti per quel campo.

La funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) restituisce una struttura di [**\_ \_ informazioni di notifica della stampante**](printer-notify-info.md) , che contiene una matrice di strutture di **\_ \_ \_ dati di notifica della stampante** .

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

Indica il tipo di informazioni fornite. Il membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                      | Significato                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**Processo \_ di Invia notifica al \_ tipo**</dt> <dt>0x01</dt> </dl>             | Indica che il membro del **campo** specifica una \_ costante di campo Notify di processo \_ \_ \* .<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**Stampante \_ NOTIFICA \_ tipo**</dt> <dt>0x00</dt> </dl> | Indica che il membro del **campo** specifica una \_ costante di campo Notify della stampante \_ \_ \* .<br/> |



 

</dd> <dt>

**Campo**
</dt> <dd>

Indica il campo modificato. Per un elenco di valori possibili, vedere la sezione Osservazioni.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> <dt>

**Id**
</dt> <dd>

Indica l'identificatore del processo se il membro del **tipo** specifica il tipo di notifica del processo \_ \_ . Se il membro del **tipo** specifica il \_ tipo di notifica della stampante \_ , questo membro non è definito.

</dd> <dt>

**NotifyData**
</dt> <dd>

Unione di informazioni sui dati basate sui membri del **tipo** e del **campo** . Per una descrizione del tipo di dati associato a ogni campo, vedere la sezione Osservazioni.

<dl> <dt>

**adwData \[ 2\]**
</dt> <dd>

Matrice di due valori **DWORD** . Per i campi di informazioni che usano solo un singolo **valore DWORD**, i dati sono in **adwData** \[ 0 \] .

</dd> <dt>

**Dati**
</dt> <dd> <dl> <dt>

**cbBuf**
</dt> <dd>

Indica la dimensione, in byte, del buffer a cui punta **pbuf**.

</dd> <dt>

**pBuf**
</dt> <dd>

Puntatore a un buffer che contiene i dati correnti del campo.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Se il membro del **tipo** specifica il \_ tipo di notifica della stampante \_ , il membro del **campo** può essere uno dei valori seguenti.



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
<td><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che contiene il nome della stampante.</td>
<td>0x01</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SHARE_NAME</td>
<td><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che identifica il punto di condivisione per la stampante.</td>
<td>0x02</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PORT_NAME</td>
<td><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che contiene il nome della porta in cui verranno stampati i processi di stampa. Se &quot; &quot; si seleziona pool di stampanti, si tratta di un elenco delimitato da virgole di porte.</td>
<td>0x03</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_DRIVER_NAME</td>
<td><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che contiene il nome del driver della stampante.</td>
<td>0x04</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_COMMENT</td>
<td><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che contiene la nuova stringa di commento, che in genere è una breve descrizione della stampante.</td>
<td>0x05</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_LOCATION</td>
<td><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che contiene la nuova posizione fisica della stampante, ad esempio &quot; Bldg. 38, stanza 1164 &quot; ).</td>
<td>0x06</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEVMODE</td>
<td><strong>pbuf</strong> è un puntatore a una struttura <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> che definisce i dati predefiniti della stampante, ad esempio l'orientamento della carta e la risoluzione.</td>
<td>0x07</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SEPFILE</td>
<td><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che specifica il nome del file utilizzato per creare la pagina separatore. Questa pagina viene utilizzata per separare i processi di stampa inviati alla stampante.</td>
<td>0x08</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</td>
<td><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che specifica il nome del processore di stampa utilizzato dalla stampante.</td>
<td>0x09</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PARAMETERS</td>
<td><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che specifica i parametri predefiniti del processore di stampa.</td>
<td>0x0A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DATATYPE</td>
<td><strong>pbuf</strong> è un puntatore a una stringa con terminazione null che specifica il tipo di dati utilizzato per registrare il processo di stampa.</td>
<td>0x0B</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</td>
<td><strong>pbuf</strong> è un puntatore a una struttura <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> per la stampante. Il puntatore può essere <strong>null</strong> se non è presente alcun descrittore di sicurezza.</td>
<td>0x0C</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_ATTRIBUTES</td>
<td><strong>adwData</strong> [0] specifica gli attributi della stampante. i possibili valori sono i seguenti:<dl> PRINTER_ATTRIBUTE_QUEUED<br />
PRINTER_ATTRIBUTE_DIRECT<br />
PRINTER_ATTRIBUTE_DEFAULT<br />
PRINTER_ATTRIBUTE_SHARED<br />
</dl></td>
<td>0x0D</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PRIORITY</td>
<td><strong>adwData</strong> [0] specifica un valore di priorità utilizzato dallo spooler per instradare i processi di stampa.</td>
<td>0x0E</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</td>
<td><strong>adwData</strong> [0] specifica il valore di priorità predefinito assegnato a ogni processo di stampa.</td>
<td>0x0F</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_START_TIME</td>
<td><strong>adwData</strong> [0] specifica la prima ora di stampa di un processo da parte della stampante. (Questo valore viene specificato in minuti trascorsi dalle ore 12:00)</td>
<td>0x10</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_UNTIL_TIME</td>
<td><strong>adwData</strong> [0] specifica l'ora più recente in cui la stampante stampa un processo. (Questo valore viene specificato in minuti trascorsi dalle ore 12:00)</td>
<td>0x11</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_STATUS</td>
<td><strong>adwData</strong> [0] specifica lo stato della stampante. Per un elenco di valori possibili, vedere la struttura <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> .</td>
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
<td>Questa impostazione viene impostata se il GUID dell'oggetto viene modificato.</td>
<td>0x1A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</td>
<td>Questa impostazione viene impostata se la connessione alla stampante viene rinominata.</td>
<td>0x1B</td>
</tr>
</tbody>
</table>



 

Se il membro del **tipo** specifica il \_ tipo di notifica del processo \_ , il membro del **campo** può essere uno dei valori seguenti.



| Campo                                    | Tipo di dati                                                                                                                                                                                                                                            | Valore |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| \_ \_ \_ nome stampante campo notifica \_ processo        | **pbuf** è un puntatore a una stringa con terminazione null che contiene il nome della stampante per cui viene eseguito lo spooling del processo.                                                                                                                                      | 0x00  |
| \_ \_ \_ nome computer campo notifica \_ processo        | **pbuf** è un puntatore a una stringa con terminazione null che specifica il nome del computer in cui è stato creato il processo di stampa.                                                                                                                                    | 0x01  |
| \_ \_ \_ nome porta campo notifica \_ processo           | **pbuf** è un puntatore a una stringa con terminazione null che identifica la porta o le porte utilizzate per trasmettere i dati alla stampante. Se una stampante è connessa a più di una porta, i nomi delle porte sono separati da virgole (ad esempio, "LPT1:, LPT2:, LPT3:"). | 0x02  |
| \_ \_ \_ nome utente campo notifica \_ processo           | **pbuf** è un puntatore a una stringa con terminazione null che specifica il nome dell'utente che ha inviato il processo di stampa.                                                                                                                                           | 0x03  |
| \_ \_ \_ nome notifica campo \_ notifica processo         | **pbuf** è un puntatore a una stringa con terminazione null che specifica il nome dell'utente a cui deve essere inviata una notifica quando il processo è stato stampato o quando si verifica un errore durante la stampa del processo.                                                              | 0x04  |
| tipo di dati del \_ campo Notify processo \_ \_             | **pbuf** è un puntatore a una stringa con terminazione null che specifica il tipo di dati utilizzati per registrare il processo di stampa.                                                                                                                                         | 0x05  |
| \_processore di \_ \_ Stampa campo notifica processo \_     | **pbuf** è un puntatore a una stringa con terminazione null che specifica il nome del processore di stampa da utilizzare per stampare il processo.                                                                                                                           | 0x06  |
| \_ \_ parametri Campo notifica \_ processi           | **pbuf** è un puntatore a una stringa con terminazione null che specifica i parametri del processore di stampa.                                                                                                                                                            | 0x07  |
| \_ \_ \_ nome driver campo notifica \_ processo         | **pbuf** è un puntatore a una stringa con terminazione null che specifica il nome del driver della stampante da usare per elaborare il processo di stampa.                                                                                                           | 0x08  |
| area di notifica del processo \_ \_ \_ DEVMODE              | **pbuf** è un puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che contiene i dati dell'ambiente e dell'inizializzazione del dispositivo per il driver della stampante.                                                                                                        | 0x09  |
| \_ \_ stato campo notifica \_ processo               | **adwData** \[ 0 \] specifica lo stato del processo. Per un elenco di valori possibili, vedere la struttura di [**informazioni sul processo \_ \_ 2**](job-info-2.md) .                                                                                                                        | 0x0A  |
| \_stringa di \_ \_ stato campo notifica processo \_       | **pbuf** è un puntatore a una stringa con terminazione null che specifica lo stato del processo di stampa.                                                                                                                                                           | 0x0B  |
| \_ \_ \_ descrittore di sicurezza campo notifica processo \_ | Non supportata.                                                                                                                                                                                                                                          | 0x0C  |
| \_documento di \_ campo \_ Notify processo             | **pbuf** è un puntatore a una stringa con terminazione null che specifica il nome del processo di stampa, ad esempio "MS-WORD: Review.doc".                                                                                                                        | 0x0D  |
| \_ \_ priorità campo notifica \_ processi             | **adwData** \[ 0 \] specifica la priorità del processo.                                                                                                                                                                                                           | 0x0E  |
| \_ \_ posizione campo notifica \_ processo             | **adwData** \[ 0 \] specifica la posizione del processo nella coda di stampa.                                                                                                                                                                                      | 0x0F  |
| \_campo notifica \_ processi \_ inviato            | **pbuf** è un puntatore a una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che specifica l'ora in cui è stato inviato il processo.                                                                                                                          | 0x10  |
| \_ora di \_ \_ inizio campo notifica processo \_          | **adwData** \[ 0 \] specifica la prima volta che il processo può essere stampato. (Questo valore viene specificato in minuti trascorsi dalle ore 12:00)                                                                                                                | 0x11  |
| \_campo notifica \_ processo \_ fino al \_ momento          | **adwData** \[ 0 \] specifica l'ora più recente in cui è possibile stampare il processo. (Questo valore viene specificato in minuti trascorsi dalle ore 12:00)                                                                                                                  | 0x12  |
| \_ \_ tempo campo notifica \_ processo                 | **adwData** \[ 0 \] specifica il tempo totale, in secondi, trascorso dall'inizio della stampa del processo.                                                                                                                                                  | 0x13  |
| \_ \_ \_ pagine totali campo notifica \_ processo         | **adwData** \[ 0 \] specifica le dimensioni, in pagine, del processo.                                                                                                                                                                                             | 0x14  |
| pagine di campo di notifica del processo \_ \_ \_ \_ stampate       | **adwData** \[ 0 \] specifica il numero di pagine stampate.                                                                                                                                                                                      | 0x15  |
| \_ \_ \_ byte totali campo notifica \_ processo         | **adwData** \[ 0 \] specifica la dimensione, in byte, del processo.                                                                                                                                                                                             | 0x16  |
| \_ \_ byte campo notifica \_ processi \_ stampati       | **adwData** \[ 0 \] specifica il numero di byte che sono stati stampati in questo processo. Per questo campo, l'oggetto notifica di modifica viene segnalato quando i byte vengono inviati alla stampante.                                                                      | 0x17  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**Informazioni sul processo \_ \_ 2**](job-info-2.md)
</dt> <dt>

[**\_Informazioni stampante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_informazioni notifica \_ stampante**](printer-notify-info.md)
</dt> <dt>

[**descrittore di sicurezza \_**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

