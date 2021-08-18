---
description: La struttura PRINTPROCESSOR \_ INFO \_ 1 specifica il nome di un processore di stampa installato.
ms.assetid: 49b272c8-156b-4996-b3fd-92cde831f4ae
title: PRINTPROCESSOR_INFO_1 struttura (Winspool.h)
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
ms.openlocfilehash: 0aa94a2df1c44b53ec9fb8211f7eaed8c955f9f2c1cd824cd4634c754f8c337e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824740"
---
# <a name="printprocessor_info_1-structure"></a>Struttura PRINTPROCESSOR \_ INFO \_ 1

La **struttura PRINTPROCESSOR \_ INFO \_ 1** specifica il nome di un processore di stampa installato.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTPROCESSOR_INFO_1 {
  LPTSTR pName;
} PRINTPROCESSOR_INFO_1, *PPRINTPROCESSOR_INFO_1;
```



## <a name="members"></a>Members

<dl> <dt>

**Pname**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome di un processore di stampa installato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PRINTPROCESSOR \_ INFO \_ 1W** (Unicode) e **\_ PRINTPROCESSOR \_ INFO \_ 1A** (ANSI)<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> </dl>

 

 




