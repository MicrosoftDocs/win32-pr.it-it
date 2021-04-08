---
title: Messaggio WM_NEXTMENU (winuser. h)
description: Inviato a un'applicazione quando viene usato il tasto freccia destra o sinistra per passare dalla barra dei menu al menu di sistema e viceversa.
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- Menu del messaggio WM_NEXTMENU e altre risorse
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
ms.openlocfilehash: 3ecb8efe8c80a3355a30ab0abf28019f87b33963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964970"
---
# <a name="wm_nextmenu-message"></a>\_Messaggio NEXTMENU WM

Inviato a un'applicazione quando viene usato il tasto freccia destra o sinistra per passare dalla barra dei menu al menu di sistema e viceversa.


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice della chiave virtuale della chiave. Vedere [**codici chiave virtuale**](/windows/desktop/inputdev/virtual-key-codes).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) contenente informazioni sul menu da attivare.

</dd> </dl>

## <a name="remarks"></a>Commenti

In risposta a questo messaggio, l'applicazione può specificare il menu a cui passare nel membro **hmenuNext** di [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) e la finestra per ricevere i messaggi di notifica del menu nel membro **hwndNext** della struttura **MDINEXTMENU** . Per rendere effettive le modifiche, è necessario impostare entrambi i membri (inizialmente **null**).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



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

 

