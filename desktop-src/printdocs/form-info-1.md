---
description: La struttura FORM_INFO_1 contiene informazioni su un modulo di stampa. Le informazioni includono l'origine dei form di stampa, il nome, le dimensioni e le dimensioni dell'area stampabile.
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: Struttura FORM_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_1
- _FORM_INFO_1A
- _FORM_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 516f646d664a034f81a76eb2262b3ea8c950a87e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314017"
---
# <a name="form_info_1-structure"></a>Struttura FORM_INFO_1

La struttura **FORM_INFO_1** contiene informazioni su un modulo di stampa. Le informazioni includono l'origine del modulo di stampa, il nome, le dimensioni e le dimensioni dell'area stampabile.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _FORM_INFO_1 {
  DWORD  Flags;
  LPTSTR pName;
  SIZEL  Size;
  RECTL  ImageableArea;
} FORM_INFO_1, *PFORM_INFO_1;
```



## <a name="members"></a>Members

<dl> <dt>

**Flag**
</dt> <dd>

Proprietà del form. Vengono definiti i valori seguenti.



| Valore         | Significato                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| FORM_USER    | Se viene impostato questo flag di bit, il form è stato definito dall'utente. I form con questo set di flag sono definiti nel registro di sistema.        |
| FORM_BUILTIN | Se viene impostato questo flag di bit, il form fa parte dello spooler. Le definizioni dei moduli con questo set di flag non vengono visualizzate nel registro di sistema. |
| FORM_PRINTER | Se viene impostato questo flag di bit, il form è associato a una determinata stampante e la relativa definizione viene visualizzata nel registro di sistema.          |



 

</dd> <dt>

**pName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del form. Il nome del modulo non può superare i 31 caratteri.

</dd> <dt>

**Dimensioni**
</dt> <dd>

Larghezza e altezza, in millesimi di millimetri, del form.

</dd> <dt>

**ImageableArea**
</dt> <dd>

Larghezza e altezza, in millesimi di millimetri, del form.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **_FORM_INFO_1W** (Unicode) e **_FORM_INFO_1A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**Diformi**](setform.md)
</dt> </dl>

 

 




