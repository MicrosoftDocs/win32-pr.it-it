---
title: Messaggio WM_RENDERFORMAT (winuser. h)
description: Inviato al proprietario degli Appunti se è stato posticipato il rendering di un formato degli Appunti specifico e se un'applicazione ha richiesto dati in tale formato.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- Scambio di dati del messaggio WM_RENDERFORMAT
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
ms.openlocfilehash: ab9d0e8539dc666c7a791a24c9ba7ac772c3c2c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340712"
---
# <a name="wm_renderformat-message"></a>\_Messaggio RENDERFORMAT WM

Inviato al proprietario degli Appunti se è stato posticipato il rendering di un formato degli Appunti specifico e se un'applicazione ha richiesto dati in tale formato. Il proprietario degli Appunti deve eseguire il rendering dei dati nel formato specificato e posizionarli negli Appunti chiamando la funzione [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[Formato degli Appunti](standard-clipboard-formats.md) di cui eseguire il rendering.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Quando si risponde a un messaggio **WM \_ RENDERFORMAT** , il proprietario degli Appunti non deve aprire gli Appunti prima di chiamare [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata). Non è necessario aprire gli Appunti prima di inserire i dati in risposta a **WM \_ RENDERFORMAT** e qualsiasi tentativo di aprire gli appunti avrà esito negativo perché gli Appunti sono attualmente mantenuti aperti dall'applicazione che ha richiesto il rendering del formato.

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

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**\_RENDERALLFORMATS WM**](wm-renderallformats.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> </dl>

 

 





