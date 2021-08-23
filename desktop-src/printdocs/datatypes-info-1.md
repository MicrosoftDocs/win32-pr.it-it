---
description: La struttura DATATYPES \_ INFO \_ 1 contiene informazioni sul tipo di dati usato per registrare un processo di stampa.
ms.assetid: 6169006c-12d4-4608-865c-732f04107f9f
title: DATATYPES_INFO_1 struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DATATYPES_INFO_1
- _DATATYPES_INFO_1A
- _DATATYPES_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 05defe3d8cc6cd66b15b2cacdd3d3d1d56c348e4946a43700278f100ea17da5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719671"
---
# <a name="datatypes_info_1-structure"></a>Struttura DATATYPES \_ INFO \_ 1

La **struttura DATATYPES \_ INFO \_ 1** contiene informazioni sul tipo di dati usato per registrare un processo di stampa.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DATATYPES_INFO_1 {
  LPTSTR pName;
} DATATYPES_INFO_1, *PDATATYPES_INFO_1;
```



## <a name="members"></a>Members

<dl> <dt>

**Pname**
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica il tipo di dati utilizzato per registrare un processo di stampa.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ DATATYPES \_ INFO \_ 1W** (Unicode) e **\_ DATATYPES \_ INFO \_ 1A** (ANSI)<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> </dl>

 

 




