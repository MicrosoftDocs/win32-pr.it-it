---
description: La struttura PRINTER NOTIFY OPTIONS TYPE specifica il set di campi relativi alle informazioni sulla stampante o sul processo che devono essere monitorati da \_ un oggetto notifica di modifica della \_ \_ stampante. Una chiamata alla funzione FindFirstPrinterChangeNotification specifica una struttura PRINTER NOTIFY OPTIONS che contiene una matrice di strutture \_ \_ PRINTER NOTIFY OPTIONS \_ \_ \_ TYPE.
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: PRINTER_NOTIFY_OPTIONS_TYPE (Winspool.h)
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
ms.openlocfilehash: 2b593a502a668345cdd0206b4f1363cf160074b6c9aa26696427b5b42a0fbdc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118056278"
---
# <a name="printer_notify_options_type-structure"></a>Struttura PRINTER \_ NOTIFY \_ OPTIONS \_ TYPE

La **struttura PRINTER NOTIFY OPTIONS \_ \_ \_ TYPE** specifica il set di campi relativi alle informazioni sulla stampante o sul processo che devono essere monitorati da un oggetto notifica di modifica della stampante.

Una chiamata alla funzione [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) specifica una struttura [**PRINTER NOTIFY \_ \_ OPTIONS**](printer-notify-options.md) che contiene una matrice di strutture **PRINTER NOTIFY OPTIONS \_ \_ \_ TYPE.**

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

Tipo da controllare. Questo membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                      | Significato                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**PROCESSO \_ TIPO \_ DI NOTIFICA**</dt> <dt>0x01</dt> </dl>             | Indica che i campi specificati nella matrice **pFields** sono costanti JOB \_ NOTIFY \_ \_ \* FIELD.<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**PRINTER \_ TIPO \_ DI NOTIFICA**</dt> <dt>0x00</dt> </dl> | Indica che i campi specificati nella matrice **pFields** sono costanti PRINTER \_ NOTIFY \_ \_ \* FIELD.<br/> |



 

</dd> <dt>

**Riservato0**
</dt> <dd>

Riservato.

</dd> <dt>

**Reserved1**
</dt> <dd>

Riservato.

</dd> <dt>

**Riservato2**
</dt> <dd>

Riservato.

</dd> <dt>

**Count**
</dt> <dd>

Numero di elementi nella **matrice pFields.**

</dd> <dt>

**pFields**
</dt> <dd>

Puntatore a una matrice di valori. Ogni elemento della matrice specifica un campo di informazioni sul processo o sulla stampante di interesse. Per un elenco dei campi di informazioni sulle stampanti e sui processi supportati, vedere la [**struttura PRINTER \_ NOTIFY \_ INFO \_**](printer-notify-info-data.md) DATA.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**DATI \_ INFORMARE \_ LA \_ STAMPANTE**](printer-notify-info-data.md)
</dt> <dt>

[**OPZIONI DI \_ NOTIFICA \_ DELLA STAMPANTE**](printer-notify-options.md)
</dt> </dl>

 

 




