---
title: WM_ASKCBFORMATNAME messaggio (Winuser.h)
description: Inviato al proprietario degli Appunti da una finestra del visualizzatore Appunti per richiedere il nome di un formato degli Appunti CF \_ OWNERDISPLAY.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- WM_ASKCBFORMATNAME messaggio Dati Exchange
topic_type:
- apiref
api_name:
- WM_ASKCBFORMATNAME
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe96a2ddf4e6767c083ec2e3f4e3fc61bdde902ff93ce9a162ec7e93eb5bef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991241"
---
# <a name="wm_askcbformatname-message"></a>Messaggio WM \_ ASKCBFORMATNAME

Inviato al proprietario degli Appunti da una finestra del visualizzatore Appunti per richiedere il nome di un formato degli Appunti [**CF \_ OWNERDISPLAY.**](standard-clipboard-formats.md)

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Dimensione, in caratteri, del buffer a cui punta il *parametro lParam.*

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che deve ricevere il nome del formato degli Appunti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

In risposta a questo messaggio, il proprietario degli Appunti deve copiare il nome del formato di visualizzazione del proprietario nel buffer specificato, senza superare le dimensioni del buffer specificate dal *parametro wParam.*

Una finestra del visualizzatore appunti invia questo messaggio al proprietario degli Appunti per determinare il nome del formato [**CF \_ OWNERDISPLAY,**](standard-clipboard-formats.md) ad esempio, per inizializzare un elenco di menu nei formati disponibili.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica degli Appunti](clipboard.md)
</dt> </dl>

 

