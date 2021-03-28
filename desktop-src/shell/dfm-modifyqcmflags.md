---
description: 'Consente al callback di modificare i \_ valori cfm xxx passati a IContextMenu:: QueryContextMenu.'
title: Messaggio DFM_MODIFYQCMFLAGS (Shlobj. h)
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
ms.openlocfilehash: ff90cfb0e0297e7d3276f00f314fce865920663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878766"
---
# <a name="dfm_modifyqcmflags-message"></a>\_Messaggio DFM MODIFYQCMFLAGS

Consente al callback di modificare i \_ valori cfm xxx passati a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*puNewFlags* \[ in\]
</dt> <dd>

Puntatore ai nuovi valori del flag.

</dd> <dt>

*uFlags* \[ in\]
</dt> <dd>

Flag che specificano il modo in cui il menu di scelta rapida può essere modificato. Questo parametro usa i \_ valori di CMF xxx descritti in [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                          |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




