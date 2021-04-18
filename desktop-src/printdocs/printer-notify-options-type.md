---
description: La \_ struttura del \_ tipo di opzioni di notifica stampanti consente di \_ specificare il set di campi delle informazioni sulla stampante o sul processo da monitorare tramite un oggetto notifica di modifica della stampante. Una chiamata alla funzione FindFirstPrinterChangeNotification specifica una \_ \_ struttura di opzioni di notifica della stampante, che contiene una matrice di \_ strutture di tipi di opzioni di notifica stampanti \_ \_ .
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: Struttura PRINTER_NOTIFY_OPTIONS_TYPE (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS_TYPE
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4a82d0bc0481533a65fc90d32a992c51116b4595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313542"
---
# <a name="printer_notify_options_type-structure"></a>\_Struttura del \_ tipo di opzioni di notifica stampanti \_

La struttura del **\_ tipo di \_ Opzioni \_ di notifica stampanti** consente di specificare il set di campi delle informazioni sulla stampante o sul processo da monitorare tramite un oggetto notifica di modifica della stampante.

Una chiamata alla funzione [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) specifica una struttura [**di \_ \_ Opzioni di notifica della stampante**](printer-notify-options.md) , che contiene una matrice di strutture di **\_ \_ \_ tipi di opzioni di notifica stampanti** .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS_TYPE {
  WORD  Type;
  WORD  Reserved0;
  DWORD Reserved1;
  DWORD Reserved2;
  DWORD Count;
  PWORD pFields;
} PRINTER_NOTIFY_OPTIONS_TYPE, *PPRINTER_NOTIFY_OPTIONS_TYPE;
```



## <a name="members"></a>Members

<dl> <dt>

**Tipo**
</dt> <dd>

Tipo da guardare. Il membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                      | Significato                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**Processo \_ di Invia notifica al \_ tipo**</dt> <dt>0x01</dt> </dl>             | Indica che i campi specificati nella matrice **pFields** sono costanti di \_ campo Notify di processo \_ \_ \* .<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**Stampante \_ NOTIFICA \_ tipo**</dt> <dt>0x00</dt> </dl> | Indica che i campi specificati nella matrice **pFields** sono costanti di \_ campo notifica stampanti \_ \_ \* .<br/> |



 

</dd> <dt>

**Reserved0**
</dt> <dd>

Riservato.

</dd> <dt>

**Reserved1**
</dt> <dd>

Riservato.

</dd> <dt>

**Reserved2**
</dt> <dd>

Riservato.

</dd> <dt>

**Count**
</dt> <dd>

Numero di elementi nella matrice **pFields** .

</dd> <dt>

**pFields**
</dt> <dd>

Puntatore a una matrice di valori. Ogni elemento della matrice specifica un campo di informazioni su processo o stampante di interesse. Per un elenco dei campi di informazioni sulle stampanti e sui processi supportati, vedere la pagina relativa alla struttura dei [**\_ \_ \_ dati di notifica della stampante**](printer-notify-info-data.md) .

</dd> </dl>

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

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**\_dati delle \_ informazioni di notifica della stampante \_**](printer-notify-info-data.md)
</dt> <dt>

[**\_Opzioni di notifica stampanti \_**](printer-notify-options.md)
</dt> </dl>

 

 




