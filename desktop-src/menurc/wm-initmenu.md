---
title: WM_INITMENU messaggio (Winuser.h)
description: Inviato quando un menu sta per diventare attivo.
ms.assetid: d0fcc6d8-f57c-4d04-b9e7-4cfab6add173
keywords:
- WM_INITMENU messaggio Menu e altre risorse
topic_type:
- apiref
api_name:
- WM_INITMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff775849abf6a7e3be4530ce893e1ae8821cb4be6e9fb2888ef9bb0ee6d67d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939571"
---
# <a name="wm_initmenu-message"></a>Messaggio \_ WM INITMENU

Inviato quando un menu sta per diventare attivo. Si verifica quando l'utente fa clic su una voce sulla barra dei menu o preme un tasto di menu. In questo modo l'applicazione può modificare il menu prima che venga visualizzato.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_INITMENU                     0x0116
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle del menu da inizializzare.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Un **messaggio WM \_ INITMENU** viene inviato solo quando si accede a un menu per la prima volta. Per ogni accesso viene generato un solo messaggio **WM \_ INITMENU.** Ad esempio, lo spostamento del mouse tra diverse voci di menu tenendo premuto il pulsante non genera nuovi messaggi. **WM \_ INITMENU** non fornisce informazioni sulle voci di menu.

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

[**WM \_ INITMENUPOPUP**](wm-initmenupopup.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

 

