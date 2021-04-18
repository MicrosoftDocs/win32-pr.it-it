---
title: Messaggio WM_PAINTCLIPBOARD (winuser. h)
description: Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti quando gli Appunti contengono dati nel \_ formato CF OWNERDISPLAY e l'area client del Visualizzatore Appunti deve essere ridisegnata.
ms.assetid: 85aeefa5-e3d9-4689-a068-47b59ec7b571
keywords:
- Scambio di dati del messaggio WM_PAINTCLIPBOARD
topic_type:
- apiref
api_name:
- WM_PAINTCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8148af6b513fd1fa956d48f22dc86e618544b073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301437"
---
# <a name="wm_paintclipboard-message"></a>\_Messaggio PAINTCLIPBOARD WM

Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti quando gli Appunti contengono dati nel formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) e l'area client del Visualizzatore Appunti deve essere ridisegnata.


```C++
#define WM_PAINTCLIPBOARD               0x0309
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra del visualizzatore degli Appunti.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per un oggetto memoria globale che contiene una struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) . La struttura definisce la parte dell'area client da disegnare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Per determinare se l'intera area client o solo una parte di essa debba essere ridisegnata, il proprietario degli Appunti deve confrontare le dimensioni dell'area di disegno specificata nel membro **rcPaint** di [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) con le dimensioni specificate nel messaggio [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md) più recente.

Il proprietario degli Appunti deve usare la funzione [**funzione GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) per bloccare la memoria che contiene la struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) . Prima di restituire, il proprietario degli Appunti deve sbloccare tale memoria utilizzando la funzione [**funzione GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .

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

[**\_SIZECLIPBOARD WM**](wm-sizeclipboard.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> </dl>

 

