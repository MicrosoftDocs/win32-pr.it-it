---
description: Contiene informazioni su un pulsante aggiunto da una DLL di estensione di File Manager alla barra degli strumenti di File Manager.
title: EXT_BUTTON struttura (Wfext.h)
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
ms.openlocfilehash: 6d1505ef7b330f0e935136eacaf808da3add8cd8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843152"
---
# <a name="ext_button-structure"></a>Struttura EXT \_ BUTTON

Contiene informazioni su un pulsante aggiunto da una DLL di estensione di File Manager alla barra degli strumenti di File Manager.

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

Tipo: **WORD**

</dd> <dd>

Identificatore di comando per il pulsante.

</dd> <dt>

**idsHelp**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Identificatore della stringa della Guida per il pulsante.

</dd> <dt>

**fsStyle**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Stile del pulsante.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BARRA DEGLI STRUMENTI \_ FMEVENTLOAD**](fmevent-toolbarload.md)
</dt> <dt>

[**BARRA DEGLI STRUMENTI \_ FMSCARICA**](fms-toolbarload.md)
</dt> </dl>

 

 




