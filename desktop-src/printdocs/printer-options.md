---
description: Rappresenta le opzioni della stampante.
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
title: PRINTER_OPTIONS struttura (Winspool.h)
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
ms.openlocfilehash: d7eb7be8443c6a49c670e0573a79831a7aacfd88087f6ab19de632223b8588c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091751"
---
# <a name="printer_options-structure"></a>Struttura PRINTER \_ OPTIONS

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

Dimensioni della struttura **PRINTER \_ OPTIONS.**

</dd> <dt>

**dwFlags**
</dt> <dd>

Set di [**FLAG PRINTER OPTION \_ \_ che**](printer-option-flags.md) specifica come l'handle per una stampante restituita da [**OpenPrinter2**](openprinter2.md) verrà utilizzato da altre funzioni.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**FLAG DI \_ OPZIONE \_ DELLA STAMPANTE**](printer-option-flags.md)
</dt> </dl>

 

 




