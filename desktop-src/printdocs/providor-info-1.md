---
description: La \_ struttura PROVIDOR info \_ 1 identifica un provider di stampa.
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: Struttura PROVIDOR_INFO_1 (winspool. h)
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
ms.openlocfilehash: 2eabc00009b76247af71b06ea877ca0bf738c1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347486"
---
# <a name="providor_info_1-structure"></a>\_Struttura PROVIDOR info \_ 1

La struttura **PROVIDOR \_ info \_ 1** identifica un provider di stampa.

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

**pName**
</dt> <dd>

Puntatore a una stringa con terminazione null che rappresenta il nome del provider di stampa.

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntatore a una stringa di ambiente con terminazione null che specifica l'ambiente in cui è progettata la libreria di collegamento dinamico (DLL) del provider.

</dd> <dt>

**pDLLName**
</dt> <dd>

Puntatore a una stringa con terminazione null che rappresenta il nome del provider. dll.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PROVIDOR \_ info \_ 1W** (Unicode) e **\_ PROVIDOR \_ info \_ 1a** (ANSI)<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




