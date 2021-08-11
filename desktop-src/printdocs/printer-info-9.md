---
description: La struttura PRINTER \_ INFO \_ 9 specifica le impostazioni predefinite della stampante per utente.
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: PRINTER_INFO_9 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_9
- _PRINTER_INFO_9A
- _PRINTER_INFO_9W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 684ffc6ccfc4f94c036bde42faec9458c8bb60911fc8c9398006f58631baa791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234236"
---
# <a name="printer_info_9-structure"></a>Struttura PRINTER \_ INFO \_ 9

La **struttura PRINTER INFO \_ \_ 9** specifica le impostazioni predefinite della stampante per utente.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_INFO_9 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_9, *PPRINTER_INFO_9;
```



## <a name="members"></a>Members

<dl> <dt>

**pDevMode**
</dt> <dd>

Puntatore a una [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che definisce i dati della stampante predefinita per utente, ad esempio l'orientamento della carta e la risoluzione. DevMODE **viene** archiviato nel registro dell'utente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le impostazioni predefinite per utente avranno effetto solo su un determinato utente o su chiunque usi il profilo. Al contrario, le impostazioni predefinite globali vengono impostate dall'amministratore di una stampante che può essere usata da chiunque. Per le impostazioni predefinite globali, usare [**PRINTER \_ INFO \_ 8**](printer-info-8.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PRINTER \_ INFO \_ 9W** (Unicode) e **\_ PRINTER INFO \_ \_ 9A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 8**](printer-info-8.md)
</dt> </dl>

 

 




