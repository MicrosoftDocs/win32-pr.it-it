---
title: Messaggio WM_MENUGETOBJECT (winuser. h)
description: Inviato al proprietario di un menu a trascinamento quando il cursore del mouse entra in una voce di menu o viene spostato dal centro dell'elemento alla parte superiore o inferiore dell'elemento.
ms.assetid: 08348e43-3d21-4543-b624-5504575efced
keywords:
- Menu del messaggio WM_MENUGETOBJECT e altre risorse
topic_type:
- apiref
api_name:
- WM_MENUGETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e124c7f2757a0d6d1d2ac0904052b6d3c255ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519205"
---
# <a name="wm_menugetobject-message"></a>\_Messaggio MENUGETOBJECT WM

Inviato al proprietario di un menu a trascinamento quando il cursore del mouse entra in una voce di menu o viene spostato dal centro dell'elemento alla parte superiore o inferiore dell'elemento.


```C++
#define WM_MENUGETOBJECT                0x0124
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'applicazione deve restituire uno dei valori seguenti.



| Codice/valore restituito                                                                                                                                                | Descrizione                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNGO \_ NOERROR**</dt> <dt>0x00000001</dt> </dl>     | Puntatore di interfaccia restituito nel membro **pvObj** di [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)<br/> |
| <dl> <dt>**MNGO \_ Nointerface**</dt> <dt>0x00000000</dt> </dl> | L'interfaccia non è supportata.<br/>                                                                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica sui menu](menus.md)
</dt> </dl>

 

 





