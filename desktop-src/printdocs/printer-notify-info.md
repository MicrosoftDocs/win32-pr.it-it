---
description: La \_ struttura delle \_ informazioni di notifica della stampante contiene informazioni sulle stampanti restituite dalla funzione FindNextPrinterChangeNotification. La funzione restituisce queste informazioni dopo che è stata soddisfatta un'operazione di attesa su un oggetto notifica di modifica della stampante.
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: Struttura PRINTER_NOTIFY_INFO (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 631169cfcdabd6a87459ebb777adb6842d09089b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313543"
---
# <a name="printer_notify_info-structure"></a>\_ \_ Struttura info notifica stampanti

La struttura delle **\_ \_ informazioni di notifica della stampante** contiene informazioni sulle stampanti restituite dalla funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) . La funzione restituisce queste informazioni dopo che è stata soddisfatta un'operazione di attesa su un oggetto notifica di modifica della stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_NOTIFY_INFO {
  DWORD                    Version;
  DWORD                    Flags;
  DWORD                    Count;
  PRINTER_NOTIFY_INFO_DATA aData[1];
} PRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Versione**
</dt> <dd>

Versione della struttura. Impostare questo membro su 2.

</dd> <dt>

**Flag**
</dt> <dd>

Flag di bit che indica lo stato della struttura di notifica. Se il bit delle informazioni di notifica della stampante \_ \_ \_ non è impostato, viene indicato che alcune notifiche devono essere eliminate.

</dd> <dt>

**Count**
</dt> <dd>

Il numero di [**elementi \_ \_ \_ dati relativi alle informazioni di notifica della stampante**](printer-notify-info-data.md) nella matrice **ADATA** .

</dd> <dt>

**aData**
</dt> <dd>

Matrice di strutture [**di \_ \_ \_ dati**](printer-notify-info-data.md) per le informazioni di notifica delle stampanti. Ogni elemento della matrice identifica un singolo campo di informazioni relative a processi o stampanti e fornisce i dati correnti per quel campo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se il membro **Flags** dispone del \_ set di bit della stampante Notify \_ info \_ scartato, indica che si è verificato un overflow o un errore e le notifiche potrebbero essere andate perse. In questo caso, è necessario chiamare [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) e specificare il \_ \_ flag di aggiornamento delle opzioni di notifica della stampante \_ per recuperare tutte le informazioni correnti. Fino a quando non verrà richiesta questa operazione di aggiornamento, il sistema non invierà altre notifiche per questo oggetto notifica di modifica.

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

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**\_dati delle \_ informazioni di notifica della stampante \_**](printer-notify-info-data.md)
</dt> </dl>

 

 




