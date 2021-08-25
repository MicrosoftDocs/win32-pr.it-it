---
description: La FORM_INFO_1 struttura contiene informazioni su un modulo di stampa. Le informazioni includono l'origine dei moduli di stampa, il nome, le dimensioni e le dimensioni della relativa area stampabile.
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: FORM_INFO_1 struttura (Winspool.h)
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
ms.openlocfilehash: b6f620d8bd2ed4ef39fc868c91068e10a7ff43f57d98510ecfbae1dbe2ae7c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949261"
---
# <a name="form_info_1-structure"></a>FORM_INFO_1 struttura

La **FORM_INFO_1** struttura contiene informazioni su un modulo di stampa. Le informazioni includono l'origine del modulo di stampa, il nome, le dimensioni e le dimensioni della relativa area stampabile.

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
| FORM_USER    | Se questo flag di bit è impostato, il modulo è stato definito dall'utente. I moduli con questo flag impostato vengono definiti nel Registro di sistema.        |
| FORM_BUILTIN | Se questo flag di bit è impostato, il modulo fa parte dello spooler. Le definizioni dei moduli con questo flag impostato non vengono visualizzate nel Registro di sistema. |
| FORM_PRINTER | Se questo flag di bit è impostato, il modulo è associato a una determinata stampante e la relativa definizione viene visualizzata nel Registro di sistema.          |



 

</dd> <dt>

**Pname**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del formato. Il nome del modulo non può superare i 31 caratteri.

</dd> <dt>

**Dimensioni**
</dt> <dd>

Larghezza e altezza, in migliaia di millimetri, del formato.

</dd> <dt>

**ImageableArea**
</dt> <dd>

Larghezza e altezza, in migliaia di millimetri, del formato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **_FORM_INFO_1W** (Unicode) e **_FORM_INFO_1A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

 




