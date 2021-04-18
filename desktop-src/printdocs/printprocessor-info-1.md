---
description: La \_ struttura PRINTPROCESSOR info \_ 1 specifica il nome di un processore di stampa installato.
ms.assetid: 49b272c8-156b-4996-b3fd-92cde831f4ae
title: Struttura PRINTPROCESSOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_INFO_1
- _PRINTPROCESSOR_INFO_1A
- _PRINTPROCESSOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5ac35f85e904e9a80d9f244a1421b54fd0994a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315980"
---
# <a name="printprocessor_info_1-structure"></a>\_Struttura PRINTPROCESSOR info \_ 1

La struttura **PRINTPROCESSOR \_ info \_ 1** specifica il nome di un processore di stampa installato.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTPROCESSOR_INFO_1 {
  LPTSTR pName;
} PRINTPROCESSOR_INFO_1, *PPRINTPROCESSOR_INFO_1;
```



## <a name="members"></a>Members

<dl> <dt>

**pName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome di un processore di stampa installato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PRINTPROCESSOR \_ info \_ 1W** (Unicode) e **\_ PRINTPROCESSOR \_ info \_ 1a** (ANSI)<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> </dl>

 

 




