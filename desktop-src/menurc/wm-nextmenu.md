---
title: WM_NEXTMENU messaggio (Winuser.h)
description: Inviato a un'applicazione quando si usa il tasto freccia DESTRA o SINISTRA per passare dalla barra dei menu al menu di sistema.
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- WM_NEXTMENU messaggio Menu e altre risorse
topic_type:
- apiref
api_name:
- WM_NEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 635ce19efbcfdfd8451f929affbbe0fe2b2c000bc4912977062f3fba2c54e9c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952081"
---
# <a name="wm_nextmenu-message"></a>Messaggio \_ WM NEXTMENU

Inviato a un'applicazione quando si usa il tasto freccia DESTRA o SINISTRA per passare dalla barra dei menu al menu di sistema.


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice della chiave virtuale della chiave. Vedere [**Codici di chiave virtuale**](/windows/desktop/inputdev/virtual-key-codes).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) che contiene informazioni sul menu da attivare.

</dd> </dl>

## <a name="remarks"></a>Commenti

In risposta a questo messaggio, l'applicazione può specificare il menu a cui passare nel membro **hmenuNext** di [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) e nella finestra per ricevere i messaggi di notifica del menu nel membro **hwndNext** della struttura **MDINEXTMENU.** È necessario impostare entrambi i membri per l'applicazione delle modifiche (inizialmente **SONO NULL).**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Menu](menus.md)
</dt> </dl>

 

