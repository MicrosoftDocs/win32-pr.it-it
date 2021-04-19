---
description: La \_ struttura Printer Info \_ 9 specifica le impostazioni predefinite della stampante per singolo utente.
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: Struttura PRINTER_INFO_9 (winspool. h)
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
ms.openlocfilehash: c0ae3c099da17d7fc437a67035d8da2cd00136bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318028"
---
# <a name="printer_info_9-structure"></a>Struttura delle informazioni di stampa \_ \_ 9

La struttura **Printer \_ info \_ 9** specifica le impostazioni predefinite della stampante per singolo utente.

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

Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che definisce i dati della stampante predefiniti per ogni utente, ad esempio l'orientamento della carta e la risoluzione. **DEVMODE** viene archiviato nel registro di sistema dell'utente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le impostazioni predefinite per utente avranno effetto solo su un utente specifico o su chiunque utilizzi il profilo. Al contrario, le impostazioni predefinite globali vengono impostate dall'amministratore di una stampante che può essere utilizzata da chiunque. Per le impostazioni predefinite globali, usare le [**informazioni sulla stampante \_ \_ 8**](printer-info-8.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ Informazioni sulle stampanti \_ \_ 9W** (Unicode) e **\_ informazioni sulla stampante \_ \_ 9a** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**\_Informazioni stampante \_ 8**](printer-info-8.md)
</dt> </dl>

 

 




