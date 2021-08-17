---
description: Contiene informazioni utilizzate da File Manager per aggiungere una stringa della Guida per un menu o una voce di comando della barra degli strumenti.
title: FMS_HELPSTRING (Wfext.h)
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
ms.openlocfilehash: 85c7c94f91cad962239745d5dffa82898ef4ad0539431122106f7d85fdaff1c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224120"
---
# <a name="fms_helpstring-structure"></a>Struttura \_ HELPSTRING FMS

Contiene informazioni utilizzate da File Manager per aggiungere una stringa della Guida per un menu o una voce di comando della barra degli strumenti.

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

Tipo: **INT**

</dd> <dd>

Identificatore dell'elemento di comando.

</dd> <dt>

**Hmenu**
</dt> <dd>

Tipo: **HMENU**

</dd> <dd>

Identificatore della barra dei menu.

</dd> <dt>

**szHelp**
</dt> <dd>

Tipo: **\_ \_ wchar \_ t \[ 128 \]**

</dd> <dd>

Stringa con terminazione Null che riceve il testo della Guida.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPMENUITEM**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




