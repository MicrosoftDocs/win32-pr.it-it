---
title: DM_SETDEFID messaggio (Winuser.h)
description: Modifica l'identificatore del pulsante di comando predefinito per una finestra di dialogo.
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- DM_SETDEFID finestre di dialogo del messaggio
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
ms.openlocfilehash: 92749cc7eca569b57d239a36bb6559e59a6a7ebc31c63787a93d0720b334d1ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741751"
---
# <a name="dm_setdefid-message"></a>Dm \_ SETDEFID message

Modifica l'identificatore del pulsante di comando predefinito per una finestra di dialogo.


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore di un controllo pulsante di comando che diventerà l'impostazione predefinita.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è sempre **TRUE.**

## <a name="remarks"></a>Commenti

Questo messaggio viene elaborato dalla [**funzione DefDlgProc.**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) Per impostare il pulsante di comando predefinito, la funzione può inviare messaggi [**WM \_ GETDLGCODE**](wm-getdlgcode.md) e [**BM \_ SETSTYLE**](../controls/bm-setstyle.md) al controllo specificato e al pulsante di comando predefinito corrente.

**L'uso del messaggio DM \_ SETDEFID** può comportare la visualizzazione dello stato predefinito di più pulsanti. Quando il sistema apre una finestra di dialogo, disegna il primo pulsante di comando nel modello di finestra di dialogo con il bordo di stato predefinito. L'invio di un messaggio **\_ DM SETDEFID** per modificare il pulsante predefinito non rimuoverà sempre il bordo dello stato predefinito dal primo pulsante. In questi casi, l'applicazione deve inviare un [**messaggio \_ SETSTYLE BM**](../controls/bm-setstyle.md) per modificare lo stile del bordo del primo pulsante di comando.

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

[**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DM \_ GETDEFID**](dm-getdefid.md)
</dt> <dt>

[**WM \_ GETDLGCODE**](wm-getdlgcode.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**BM \_ SETSTYLE**](../controls/bm-setstyle.md)
</dt> <dt>

[**EM \_ SETLIMITTEXT**](../controls/em-setlimittext.md)
</dt> </dl>

 

