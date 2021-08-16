---
description: La struttura PROVIDOR \_ INFO \_ 2 aggiunge un provider di stampa all'elenco degli ordini del provider di stampa.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: PROVIDOR_INFO_2 struttura (Winspool.h)
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
ms.openlocfilehash: 969af36fe0a64bb586fbf62912ca27c6ebba9ba0a627701e4bc57f6202bfe1b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091681"
---
# <a name="providor_info_2-structure"></a>Struttura PROVIDOR \_ INFO \_ 2

La **struttura PROVIDOR \_ INFO \_ 2** aggiunge un provider di stampa all'elenco degli ordini del provider di stampa.

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

Puntatore a una stringa con terminazione Null che specifica il nome del provider di stampa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata quando si chiama [**AddPrintProvidor**](addprintprovidor.md), livello 2, per aggiungere il provider di stampa specificato alla fine dell'elenco degli ordini del provider di stampa. Il provider viene immediatamente usato per il routing se la chiamata ha esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PROVIDOR \_ INFO \_ 2W** (Unicode) e **\_ PROVIDOR \_ INFO \_ 2A** (ANSI)<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




