---
description: La struttura PRINTER \_ NOTIFY INFO contiene le informazioni sulla stampante \_ restituite dalla funzione FindNextPrinterChangeNotification. La funzione restituisce queste informazioni dopo che è stata soddisfatta un'operazione di attesa su un oggetto notifica di modifica della stampante.
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: PRINTER_NOTIFY_INFO (Winspool.h)
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
ms.openlocfilehash: 26c7fca07eda8638bf657055691d72c78bccdbec6ef2b9a8c76ee7cf830bc767
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091851"
---
# <a name="printer_notify_info-structure"></a>Struttura PRINTER \_ NOTIFY \_ INFO

La **struttura PRINTER NOTIFY \_ \_ INFO** contiene le informazioni sulla stampante restituite [**dalla funzione FindNextPrinterChangeNotification.**](findnextprinterchangenotification.md) La funzione restituisce queste informazioni dopo che è stata soddisfatta un'operazione di attesa su un oggetto notifica di modifica della stampante.

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

**Version**
</dt> <dd>

Versione di questa struttura . Impostare questo membro su 2.

</dd> <dt>

**Flag**
</dt> <dd>

Flag di bit che indica lo stato della struttura di notifica. Se il bit PRINTER NOTIFY INFO DISCARDED è impostato, significa che alcune notifiche \_ \_ devono essere \_ rimosse.

</dd> <dt>

**Count**
</dt> <dd>

Numero di [**elementi PRINTER NOTIFY INFO \_ \_ \_ DATA**](printer-notify-info-data.md) nella **matrice aData.**

</dd> <dt>

**Adata**
</dt> <dd>

Matrice di strutture [**PRINTER \_ NOTIFY INFO \_ \_ DATA.**](printer-notify-info-data.md) Ogni elemento della matrice identifica un singolo campo di informazioni su processo o stampante e fornisce i dati correnti per tale campo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se per **il membro Flags** è impostato il bit PRINTER NOTIFY INFO \_ \_ DISCARDED, significa che si è verificato un overflow o un errore e che le notifiche \_ potrebbero essere state perse. In questo caso, è necessario chiamare [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) e specificare il flag PRINTER \_ NOTIFY OPTIONS REFRESH per recuperare tutte le informazioni \_ \_ correnti. Fino a quando non si richiede questa operazione di aggiornamento, il sistema non invierà notifiche aggiuntive per questo oggetto notifica di modifica.

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

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**DATI \_ INFORMARE \_ LA \_ STAMPANTE**](printer-notify-info-data.md)
</dt> </dl>

 

 




