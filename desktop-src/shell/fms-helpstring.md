---
description: Contiene informazioni utilizzate da Gestione file per aggiungere una stringa della Guida per un elemento di comando di menu o barre degli strumenti.
title: Struttura FMS_HELPSTRING (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b3ae7f86-5d58-47fa-87bd-e4e6a3541a93
ms.openlocfilehash: c934409712ae740797eb3b5af0b55c50ff125342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994741"
---
# <a name="fms_helpstring-structure"></a>\_Struttura HELPSTRING FMS

Contiene informazioni utilizzate da Gestione file per aggiungere una stringa della Guida per un elemento di comando di menu o barre degli strumenti.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a>Members

<dl> <dt>

**idCommand**
</dt> <dd>

Tipo: **int**

</dd> <dd>

Identificatore dell'elemento di comando.

</dd> <dt>

**hMenu**
</dt> <dd>

Tipo: **HMENU**

</dd> <dd>

Identificatore della barra dei menu.

</dd> <dt>

**szHelp**
</dt> <dd>

Tipo: **\_ \_ WCHAR \_ t \[ 128 \]**

</dd> <dd>

Stringa con terminazione null che riceve il testo della guida.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**\_HELPMENUITEM FMEVENT**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




