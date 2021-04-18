---
description: La \_ struttura Printer enum \_ values specifica il nome del valore, il tipo e i dati per un valore di configurazione della stampante restituito dalla funzione EnumPrinterDataEx.
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: Struttura PRINTER_ENUM_VALUES (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_ENUM_VALUES
- _PRINTER_ENUM_VALUESA
- _PRINTER_ENUM_VALUESW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ea73318db7a91fa4d422624b1c3c0c6f09d97cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314004"
---
# <a name="printer_enum_values-structure"></a>\_ \_ Struttura dei valori enum della stampante

La struttura **Printer \_ enum \_ values** specifica il nome del valore, il tipo e i dati per un valore di configurazione della stampante restituito dalla funzione [**EnumPrinterDataEx**](enumprinterdataex.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_ENUM_VALUES {
  LPTSTR pValueName;
  DWORD  cbValueName;
  DWORD  dwType;
  LPBYTE pData;
  DWORD  cbData;
} PRINTER_ENUM_VALUES, *PPRINTER_ENUM_VALUES;
```



## <a name="members"></a>Members

<dl> <dt>

**pValueName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del valore recuperato.

</dd> <dt>

**cbValueName**
</dt> <dd>

Numero di byte nel membro **pValueName** , incluso il carattere null di terminazione.

</dd> <dt>

**dwType**
</dt> <dd>

Codice che indica il tipo di dati a cui fa riferimento il membro **pData** . Per un elenco dei possibili codici di tipo, vedere [tipi di valore del registro di sistema](/windows/desktop/SysInfo/registry-value-types).

</dd> <dt>

**pData**
</dt> <dd>

Puntatore a un buffer contenente i dati per il valore recuperato.

</dd> <dt>

**cbData**
</dt> <dd>

Numero di byte recuperati nel buffer **pData** .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ Printer \_ enum \_ VALUESW** (Unicode) e **\_ Printer \_ enum \_ values** (ANSI)<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> </dl>

 

