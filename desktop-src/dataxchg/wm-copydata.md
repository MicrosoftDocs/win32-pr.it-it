---
title: Messaggio WM_COPYDATA (winuser. h)
description: Un'applicazione invia il \_ messaggio WM COPYDATA per passare i dati a un'altra applicazione.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- Scambio di dati del messaggio WM_COPYDATA
topic_type:
- apiref
api_name:
- WM_COPYDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8160c88b11fa109e8bbfaa06f0f6c45c9b7daed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477177"
---
# <a name="wm_copydata-message"></a>\_Messaggio COPYDATA WM

Un'applicazione invia il messaggio **WM \_ COPYDATA** per passare i dati a un'altra applicazione.


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra che passa i dati.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) che contiene i dati da passare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'applicazione ricevente elabora questo messaggio, deve restituire **true**; in caso contrario, deve restituire **false**.

## <a name="remarks"></a>Commenti

I dati passati non devono contenere puntatori o altri riferimenti a oggetti non accessibili all'applicazione che riceve i dati.

Durante l'invio di questo messaggio, i dati a cui si fa riferimento non devono essere modificati da un altro thread del processo di invio.

L'applicazione ricevente deve considerare i dati di sola lettura. Il parametro *lParam* è valido solo durante l'elaborazione del messaggio. L'applicazione ricevente non deve liberare la memoria a cui fa riferimento *lParam*. Se l'applicazione ricevente deve accedere ai dati dopo la restituzione di [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , deve copiare i dati in un buffer locale.

## <a name="examples"></a>Esempio

Per un esempio, vedere [uso della copia dei dati](using-data-copy.md).

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

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 

