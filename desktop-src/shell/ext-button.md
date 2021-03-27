---
description: Contiene informazioni su un pulsante aggiunto da una DLL di estensione di file Manager alla barra degli strumenti di gestione file.
title: Struttura EXT_BUTTON (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXT_BUTTON
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8cd29a06-0f38-4285-9092-647a391b72d7
ms.openlocfilehash: 5eabb9f5e958b1e0bd15a6412dfbfa276d23f255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751015"
---
# <a name="ext_button-structure"></a>\_Struttura pulsante EXT

Contiene informazioni su un pulsante aggiunto da una DLL di estensione di file Manager alla barra degli strumenti di gestione file.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a>Members

<dl> <dt>

**idCommand**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Identificatore di comando per il pulsante.

</dd> <dt>

**idsHelp**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Identificatore della stringa della Guida per il pulsante.

</dd> <dt>

**fsStyle**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Stile del pulsante.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TOOLBARLOAD FMEVENT**](fmevent-toolbarload.md)
</dt> <dt>

[**\_TOOLBARLOAD FMS**](fms-toolbarload.md)
</dt> </dl>

 

 




