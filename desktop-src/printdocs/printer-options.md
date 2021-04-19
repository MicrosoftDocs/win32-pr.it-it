---
description: Rappresenta le opzioni della stampante.
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
title: Struttura PRINTER_OPTIONS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 37c45277f0a7e30bc94b2d23ffa27de0092a7164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313540"
---
# <a name="printer_options-structure"></a>\_Struttura opzioni stampante

Rappresenta le opzioni della stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_OPTIONS {
  UINT  cbSize;
  DWORD dwFlags;
} PRINTER_OPTIONS, *PPRINTER_OPTIONS;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione della struttura delle **\_ Opzioni di stampa** .

</dd> <dt>

**dwFlags**
</dt> <dd>

Set di [**flag di \_ Opzioni \_ della stampante**](printer-option-flags.md) che specifica il modo in cui l'handle per una stampante restituita da [**OpenPrinter2**](openprinter2.md) verrà usato da altre funzioni.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**\_flag di opzione stampante \_**](printer-option-flags.md)
</dt> </dl>

 

 




