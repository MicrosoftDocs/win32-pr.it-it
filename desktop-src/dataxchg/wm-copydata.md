---
title: WM_COPYDATA messaggio (Winuser.h)
description: Un'applicazione invia il messaggio WM \_ COPYDATA per passare i dati a un'altra applicazione.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- WM_COPYDATA messaggio Dati Exchange
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
ms.openlocfilehash: 4eb91b2544bf0ebf0e8767a611b422de9aaaf1d73161e47c7bf27768f4acecb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304486"
---
# <a name="wm_copydata-message"></a>Messaggio \_ WM COPYDATA

Un'applicazione invia il **messaggio WM \_ COPYDATA** per passare i dati a un'altra applicazione.


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

Puntatore a una [**struttura COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) che contiene i dati da passare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'applicazione ricevente elabora questo messaggio, deve restituire **TRUE**. in caso contrario, deve restituire **FALSE.**

## <a name="remarks"></a>Commenti

I dati passati non devono contenere puntatori o altri riferimenti a oggetti non accessibili all'applicazione che riceve i dati.

Durante l'invio di questo messaggio, i dati a cui si fa riferimento non devono essere modificati da un altro thread del processo di invio.

L'applicazione ricevente deve considerare i dati di sola lettura. Il *parametro lParam* è valido solo durante l'elaborazione del messaggio. L'applicazione ricevente non deve liberare la memoria a cui fa riferimento *lParam*. Se l'applicazione ricevente deve accedere ai dati dopo il ritorno di [**SendMessage,**](/windows/desktop/api/winuser/nf-winuser-sendmessage) deve copiare i dati in un buffer locale.

## <a name="examples"></a>Esempio

Per un esempio, vedere [Uso della copia dei dati](using-data-copy.md).

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

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 

