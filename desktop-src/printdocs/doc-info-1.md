---
description: La struttura DOC \_ INFO \_ 1 descrive un documento che verrà stampato.
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: DOC_INFO_1 struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_1
- _DOC_INFO_1A
- _DOC_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: f534031da1c8f8f50309d4a2db0bfa39fe272ac34f59d1b490c24026d8fee261
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950001"
---
# <a name="doc_info_1-structure"></a>Struttura DOC \_ INFO \_ 1

La **struttura DOC INFO \_ \_ 1** descrive un documento che verrà stampato.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DOC_INFO_1 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
} DOC_INFO_1;
```



## <a name="members"></a>Members

<dl> <dt>

**pDocName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del documento.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome di un file di output. Per stampare su una stampante, impostare questo valore su **NULL.**

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica il tipo di dati utilizzato per registrare il documento.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ DOC \_ INFO \_ 1W** (Unicode) e **\_ DOC INFO \_ \_ 1A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

 




