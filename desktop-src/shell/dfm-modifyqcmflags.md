---
description: Consente al callback di modificare i valori CFM \_ XXX passati a IContextMenu::QueryContextMenu.
title: DFM_MODIFYQCMFLAGS messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2c87e14d-4cf4-425d-a5fe-9dc7530f0e59
api_name:
- DFM_MODIFYQCMFLAGS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 62ce86426b31abfb6dec67d7ee45b01a8bc47ba10c40ce9ed00051dd414a0ffd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223591"
---
# <a name="dfm_modifyqcmflags-message"></a>Messaggio DFM \_ MODIFYQCMFLAGS

Consente al callback di modificare i valori CFM \_ XXX passati a [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*puNewFlags* \[ Pollici\]
</dt> <dd>

Puntatore ai nuovi valori del flag.

</dd> <dt>

*uFlags* \[ Pollici\]
</dt> <dd>

Flag che specificano la modalità di modifica del menu di scelta rapida. Questo parametro usa i valori CMF \_ XXX descritti in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




