---
description: La \_ struttura Printer Info \_ 8 specifica le impostazioni della stampante predefinite globali.
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: Struttura PRINTER_INFO_8 (winspool. h)
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
ms.openlocfilehash: e17780dc2f39dc3041e690de1ef7b5728c8743e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884985"
---
# <a name="printer_info_8-structure"></a>\_Struttura Info stampante \_ 8

La struttura **Printer \_ info \_ 8** specifica le impostazioni della stampante predefinite globali.

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

Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che definisce i dati globali della stampante predefiniti, ad esempio l'orientamento della carta e la risoluzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le impostazioni predefinite globali vengono impostate dall'amministratore di una stampante che può essere usata da chiunque. Al contrario, le impostazioni predefinite per singolo utente influiranno su un utente specifico o su qualsiasi altro utente che utilizza il profilo. Per le impostazioni predefinite per utente, usare [**le \_ informazioni \_ sulla stampante 9**](printer-info-9.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ Informazioni sulle stampanti \_ \_ 8W** (Unicode) e **\_ informazioni sulla stampante \_ \_ 8a** (ANSI)<br/>                           |



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

[**Informazioni sulla stampante \_ \_ 9**](printer-info-9.md)
</dt> </dl>

 

 




