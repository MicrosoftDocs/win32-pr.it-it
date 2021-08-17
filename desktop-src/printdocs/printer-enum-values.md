---
description: La struttura PRINTER ENUM VALUES specifica il nome del valore, il tipo e i dati per un valore di configurazione della stampante restituito \_ \_ dalla funzione EnumPrinterDataEx.
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: PRINTER_ENUM_VALUES struttura (Winspool.h)
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
ms.openlocfilehash: a2b6fd8e548353dbede634d7b3bbaa08023d5e7bc2c8bc4cefbe37f7aba494ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470578"
---
# <a name="printer_enum_values-structure"></a>Struttura PRINTER \_ ENUM \_ VALUES

La **struttura PRINTER \_ ENUM \_ VALUES** specifica il nome del valore, il tipo e i dati per un valore di configurazione della stampante restituito dalla [**funzione EnumPrinterDataEx.**](enumprinterdataex.md)

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

Puntatore a una stringa con terminazione Null che specifica il nome del valore recuperato.

</dd> <dt>

**cbValueName**
</dt> <dd>

Numero di byte nel membro **pValueName,** incluso il carattere NULL di terminazione.

</dd> <dt>

**dwType**
</dt> <dd>

Codice che indica il tipo di dati a cui punta il **membro pData.** Per un elenco dei codici di tipo possibili, vedere Tipi [di valori del Registro di sistema](/windows/desktop/SysInfo/registry-value-types).

</dd> <dt>

**pData**
</dt> <dd>

Puntatore a un buffer contenente i dati per il valore recuperato.

</dd> <dt>

**cbData**
</dt> <dd>

Numero di byte recuperati nel buffer **pData.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PRINTER \_ ENUM \_ VALUESW** (Unicode) e **\_ PRINTER \_ ENUM \_ VALUESA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> </dl>

 

