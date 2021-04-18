---
title: Struttura MENUHELPID
description: Contiene i dati finali scritti nella risorsa di \_ menu RT per un menu o un sottomenu se il membro resInfo della struttura POPUPMENUITEM è impostato su un \_ popup fabbisogno.
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- Menu struttura MENUHELPID e altre risorse
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b90b5a4745433c92a859a168611aa1c14f1fa45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302527"
---
# <a name="menuhelpid-structure"></a>Struttura MENUHELPID

Contiene i dati finali scritti nella risorsa [**di \_ menu RT**](/windows/desktop/menurc/resource-types) per un menu o un sottomenu se il membro **resInfo** della struttura [**POPUPMENUITEM**](popupmenuitem.md) è impostato su **un \_ popup fabbisogno**. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.

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

Identificatore usato per identificare il menu durante l'elaborazione della [**\_ Guida di WM**](/windows/desktop/shell/wm-help) .

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

 

