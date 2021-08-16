---
description: La struttura PROVIDOR \_ INFO \_ 1 identifica un provider di stampa.
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: PROVIDOR_INFO_1 struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_1
- _PROVIDOR_INFO_1A
- _PROVIDOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4f9e7015382ef34f4582c4772e148059c4ed01de9e81da5af71bc0849df26f15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091701"
---
# <a name="providor_info_1-structure"></a>Struttura PROVIDOR \_ INFO \_ 1

La **struttura PROVIDOR \_ INFO \_ 1** identifica un provider di stampa.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PROVIDOR_INFO_1 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} PROVIDOR_INFO_1, *PPROVIDOR_INFO_1;
```



## <a name="members"></a>Members

<dl> <dt>

**Pname**
</dt> <dd>

Puntatore a una stringa con terminazione Null che rappresenta il nome del provider di stampa.

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntatore a una stringa di ambiente con terminazione Null che specifica l'ambiente in cui è progettata la libreria a collegamento dinamico (DLL) del provider.

</dd> <dt>

**pDLLName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che rappresenta il nome del provider .dll.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PROVIDOR \_ INFO \_ 1W** (Unicode) e **\_ PROVIDOR \_ INFO \_ 1A** (ANSI)<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




