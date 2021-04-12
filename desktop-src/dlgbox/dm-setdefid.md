---
title: Messaggio DM_SETDEFID (winuser. h)
description: Modifica l'identificatore del pulsante di push predefinito per una finestra di dialogo.
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- Finestre di dialogo DM_SETDEFID messaggio
topic_type:
- apiref
api_name:
- DM_SETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ceda9ac9e8fd399604e9c55431b8fcd74646f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518879"
---
# <a name="dm_setdefid-message"></a>\_Messaggio DM SETDEFID

Modifica l'identificatore del pulsante di push predefinito per una finestra di dialogo.


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore di un controllo pulsante di comando che diventerà il valore predefinito.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è sempre **true**.

## <a name="remarks"></a>Commenti

Questo messaggio viene elaborato dalla funzione [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) . Per impostare il pulsante di push predefinito, la funzione può inviare i messaggi [**di \_ tipo**](../controls/bm-setstyle.md) " [**WM \_ GETDLGCODE**](wm-getdlgcode.md) " e "BM" al controllo specificato e al pulsante di push predefinito corrente.

L'uso del messaggio **DM \_ SETDEFID** può comportare la visualizzazione di più di un pulsante con lo stato predefinito del pulsante di push. Quando il sistema Visualizza una finestra di dialogo, disegna il primo pulsante di push nel modello di finestra di dialogo con il bordo dello stato predefinito. L'invio di un messaggio **DM \_ SETDEFID** per modificare il pulsante predefinito non ridurrà sempre il bordo di stato predefinito dal primo pulsante di push. In questi casi, l'applicazione deve inviare un messaggio di [**\_ tipo BM**](../controls/bm-setstyle.md) per modificare il primo stile del bordo del pulsante di push.

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

[**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**\_GETDEFID DM**](dm-getdefid.md)
</dt> <dt>

[**\_GETDLGCODE WM**](wm-getdlgcode.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**distile BM \_**](../controls/bm-setstyle.md)
</dt> <dt>

[**\_SETLIMITTEXT em**](../controls/em-setlimittext.md)
</dt> </dl>

 

