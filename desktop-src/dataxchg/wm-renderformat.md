---
title: WM_RENDERFORMAT messaggio (Winuser.h)
description: Inviato al proprietario degli Appunti se ha ritardato il rendering di un formato degli Appunti specifico e se un'applicazione ha richiesto dati in tale formato.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- WM_RENDERFORMAT messaggio Dati Exchange
topic_type:
- apiref
api_name:
- WM_RENDERFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2885e056577656d6cabb8ea78f48a02a19f3c3c40bb3c30b1e5ca25c72cdf39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545310"
---
# <a name="wm_renderformat-message"></a>Messaggio WM \_ RENDERFORMAT

Inviato al proprietario degli Appunti se ha ritardato il rendering di un formato degli Appunti specifico e se un'applicazione ha richiesto dati in tale formato. Il proprietario degli Appunti deve eseguire il rendering dei dati nel formato specificato e posizionarlo negli Appunti chiamando la [**funzione SetClipboardData.**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Formato [degli Appunti di](standard-clipboard-formats.md) cui eseguire il rendering.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Quando risponde a un **messaggio WM \_ RENDERFORMAT,** il proprietario degli Appunti non deve aprire gli Appunti prima di [**chiamare SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata). L'apertura degli Appunti non è necessaria prima di inserire i dati in risposta a **WM \_ RENDERFORMAT** e qualsiasi tentativo di apertura degli Appunti avrà esito negativo perché gli Appunti sono attualmente mantenuti aperti dall'applicazione che ha richiesto il rendering del formato.

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

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**WM \_ RENDERALLFORMATS**](wm-renderallformats.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> </dl>

 

 





