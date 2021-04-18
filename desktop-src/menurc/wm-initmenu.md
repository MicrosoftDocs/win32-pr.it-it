---
title: Messaggio WM_INITMENU (winuser. h)
description: Inviato quando un menu sta per diventare attivo.
ms.assetid: d0fcc6d8-f57c-4d04-b9e7-4cfab6add173
keywords:
- Menu del messaggio WM_INITMENU e altre risorse
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
ms.openlocfilehash: 94626b99a5016efaa9427d1ae8b3b3122e599965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302526"
---
# <a name="wm_initmenu-message"></a>\_Messaggio INITMENU WM

Inviato quando un menu sta per diventare attivo. Si verifica quando l'utente fa clic su un elemento nella barra dei menu o preme un tasto di menu. Questo consente all'applicazione di modificare il menu prima che venga visualizzato.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_INITMENU                     0x0116
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il menu da inizializzare.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Un messaggio **WM \_ INITMENU** viene inviato solo quando si accede per la prima volta a un menu. viene generato un solo messaggio **WM \_ INITMENU** per ogni accesso. Ad esempio, lo spostamento del mouse tra diverse voci di menu tenendo premuto il pulsante non genera nuovi messaggi. **WM \_ INITMENU** non fornisce informazioni sulle voci di menu.

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

[**\_INITMENUPOPUP WM**](wm-initmenupopup.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

 

