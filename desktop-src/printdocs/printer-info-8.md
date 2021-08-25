---
description: La struttura PRINTER \_ INFO \_ 8 specifica le impostazioni predefinite globali della stampante.
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: PRINTER_INFO_8 struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_8
- _PRINTER_INFO_8A
- _PRINTER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0aa5d516dd099caeba5699a8328fa52add64f14ea970e6ccec28ea8bfbe87271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947671"
---
# <a name="printer_info_8-structure"></a>Struttura PRINTER \_ INFO \_ 8

La **struttura PRINTER INFO \_ \_ 8** specifica le impostazioni predefinite globali della stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_INFO_8 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_8, *PPRINTER_INFO_8;
```



## <a name="members"></a>Members

<dl> <dt>

**pDevMode**
</dt> <dd>

Puntatore a una [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che definisce i dati della stampante predefiniti globali, ad esempio l'orientamento della carta e la risoluzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le impostazioni predefinite globali vengono impostate dall'amministratore di una stampante che può essere usata da chiunque. Al contrario, le impostazioni predefinite per utente influiranno su un determinato utente o su qualsiasi altro utente che usa il profilo. Per le impostazioni predefinite per utente, usare [**PRINTER \_ INFO \_ 9**](printer-info-9.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PRINTER \_ INFO \_ 8W** (Unicode) e **\_ PRINTER INFO \_ \_ 8A** (ANSI)<br/>                           |



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

[**PRINTER \_ INFO \_ 9**](printer-info-9.md)
</dt> </dl>

 

 




