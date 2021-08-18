---
title: Struttura MENUHELPID
description: Contiene i dati finali scritti nella risorsa RT MENU per un menu o un sottomenu se il membro resInfo della struttura \_ POPUPMENUITEM è impostato su MFR \_ POPUP.
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- Struttura MENUHELPID Menu e altre risorse
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4831074d5e7b663210f880bf6684cbc6484ad3487a0c6c9e5be308aebc66291a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825951"
---
# <a name="menuhelpid-structure"></a>Struttura MENUHELPID

Contiene i dati finali scritti nella risorsa [**RT \_ MENU**](/windows/desktop/menurc/resource-types) per un menu o un sottomenu se il membro **resInfo** della struttura [**POPUPMENUITEM**](popupmenuitem.md) è impostato su **MFR \_ POPUP**. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD helpID;
} MENUHELPID;
```



## <a name="members"></a>Members

<dl> <dt>

**helpID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificatore utilizzato per identificare il menu durante [**l'elaborazione di WM \_ HELP.**](/windows/desktop/shell/wm-help)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**MENUHEADER**](menuheader.md)
</dt> <dt>

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Risorse](resources.md)
</dt> </dl>

 

