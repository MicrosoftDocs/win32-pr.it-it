---
description: La \_ struttura PROVIDOR info \_ 2 aggiunge un provider di stampa all'elenco di ordini del provider di stampa.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: Struttura PROVIDOR_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_2
- _PROVIDOR_INFO_2A
- _PROVIDOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d40f5843bf68254b92e3d814d9f308ba4f058889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316417"
---
# <a name="providor_info_2-structure"></a>\_Struttura PROVIDOR info \_ 2

La struttura **PROVIDOR \_ info \_ 2** aggiunge un provider di stampa all'elenco di ordini del provider di stampa.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a>Members

<dl> <dt>

**pOrder**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del provider di stampa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata quando si chiama [**AddPrintProvidor**](addprintprovidor.md), Level 2, per aggiungere il provider di stampa specificato alla fine dell'elenco di ordini del provider di stampa. Il provider viene utilizzato immediatamente per il routing se la chiamata ha esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PROVIDOR \_ info \_ 2W** (Unicode) e **\_ PROVIDOR \_ info \_ 2a** (ANSI)<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




