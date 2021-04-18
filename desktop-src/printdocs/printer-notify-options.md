---
description: La \_ \_ struttura opzioni di notifica stampanti consente di specificare le opzioni per un oggetto notifica di modifica che monitora una stampante o un server di stampa.
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: Struttura PRINTER_NOTIFY_OPTIONS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: af1aeaa1138145c5df18ea4fd5babaa1a9e60416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313539"
---
# <a name="printer_notify_options-structure"></a>Struttura delle opzioni di \_ notifica stampanti \_

La **struttura \_ \_ Opzioni di notifica stampanti** consente di specificare le opzioni per un oggetto notifica di modifica che monitora una stampante o un server di stampa.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS {
  DWORD                        Version;
  DWORD                        Flags;
  DWORD                        Count;
  PPRINTER_NOTIFY_OPTIONS_TYPE pTypes;
} PRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS;
```



## <a name="members"></a>Members

<dl> <dt>

**Versione**
</dt> <dd>

Versione della struttura. Impostare questo membro su 2.

</dd> <dt>

**Flag**
</dt> <dd>

Flag di bit. Se si imposta il \_ flag di aggiornamento delle opzioni di notifica della stampante \_ \_ in una chiamata alla funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) , la funzione fornisce i dati correnti per tutti i campi delle informazioni sulla stampante monitorata. La funzione [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) ignora il membro dei **flag** .

</dd> <dt>

**Count**
</dt> <dd>

Numero di elementi nella matrice **pTypes** .

</dd> <dt>

**pTypes**
</dt> <dd>

Puntatore a una matrice di opzioni di notifica delle stampanti per le strutture dei [**\_ \_ \_ tipi**](printer-notify-options-type.md) . Usare un elemento di questa matrice per specificare i campi delle informazioni sulla stampante da monitorare e un elemento per specificare i campi di informazioni sui processi da monitorare. È possibile monitorare le informazioni sulle stampanti, le informazioni sui processi o entrambi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare questa struttura con la funzione [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) per specificare il set di campi delle informazioni sulla stampante o sul processo da monitorare per la modifica.

Usare questa struttura con la funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) per richiedere i dati correnti per tutti i campi di informazioni sui processi e le stampanti monitorati. In questo caso, il membro **Flags** specifica il \_ flag di aggiornamento delle opzioni di notifica della stampante \_ \_ e la funzione ignora gli altri membri della struttura.

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

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**\_tipo di \_ Opzioni di notifica stampanti \_**](printer-notify-options-type.md)
</dt> </dl>

 

 




