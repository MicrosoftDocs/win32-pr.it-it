---
title: Messaggio WM_ASKCBFORMATNAME (winuser. h)
description: Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti per richiedere il nome di un \_ formato degli Appunti di OWNERDISPLAY CF.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- Scambio di dati del messaggio WM_ASKCBFORMATNAME
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
ms.openlocfilehash: b14a7f2fc2ff57076d6b694061466fd60e09dce0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119358"
---
# <a name="wm_askcbformatname-message"></a>\_Messaggio ASKCBFORMATNAME WM

Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti per richiedere il nome di un formato degli Appunti di [**\_ OWNERDISPLAY CF**](standard-clipboard-formats.md) .

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Dimensione, in caratteri, del buffer a cui punta il parametro *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che deve ricevere il nome del formato degli Appunti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

In risposta a questo messaggio, il proprietario degli Appunti deve copiare il nome del formato di visualizzazione del proprietario nel buffer specificato, non superando la dimensione del buffer specificata dal parametro *wParam* .

Una finestra del visualizzatore degli Appunti Invia questo messaggio al proprietario degli Appunti per determinare il nome del formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) , ad esempio, per inizializzare un menu che elenca i formati disponibili.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Cenni preliminari sugli Appunti](clipboard.md)
</dt> </dl>

 

