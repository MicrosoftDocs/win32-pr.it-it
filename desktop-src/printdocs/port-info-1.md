---
description: La struttura PORT \_ INFO \_ 1 identifica una porta della stampante supportata.
ms.assetid: e474fe9c-e554-406a-a5bf-de07f9a72b32
title: PORT_INFO_1 struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_1
- _PORT_INFO_1A
- _PORT_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ff6e4c3a43c35118772aede2e329a2e1e761fc0f147b5a3a9ceeef97bbf8fb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947811"
---
# <a name="port_info_1-structure"></a>Struttura PORT \_ INFO \_ 1

La **struttura PORT INFO \_ \_ 1** identifica una porta della stampante supportata.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PORT_INFO_1 {
  LPTSTR pName;
} PORT_INFO_1, *PPORT_INFO_1;
```



## <a name="members"></a>Members

<dl> <dt>

**Pname**
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica una porta della stampante supportata, ad esempio "LPT1:".

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PORT \_ INFO \_ 1W** (Unicode) e **\_ PORT INFO \_ \_ 1A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




