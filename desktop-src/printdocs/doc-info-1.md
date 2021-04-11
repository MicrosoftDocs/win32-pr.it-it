---
description: La \_ struttura doc info \_ 1 descrive un documento che verrà stampato.
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: Struttura DOC_INFO_1 (winspool. h)
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
ms.openlocfilehash: 6f905a89163b46743a92c8616ee0fa3d0564590c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227354"
---
# <a name="doc_info_1-structure"></a>Struttura del documento \_ info \_ 1

La struttura **doc \_ info \_ 1** descrive un documento che verrà stampato.

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

Puntatore a una stringa con terminazione null che specifica il nome del documento.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome di un file di output. Per stampare su una stampante, impostarla su **null**.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntatore a una stringa con terminazione null che identifica il tipo di dati utilizzati per registrare il documento.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ \_ Info doc \_ 1W** (Unicode) e **\_ doc \_ info \_ 1a** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

 




