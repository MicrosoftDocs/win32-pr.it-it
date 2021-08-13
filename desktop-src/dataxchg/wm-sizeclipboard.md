---
title: WM_SIZECLIPBOARD messaggio (Winuser.h)
description: Inviato al proprietario degli Appunti da una finestra del Visualizzatore Appunti quando gli Appunti contengono dati nel formato CF OWNERDISPLAY e le dimensioni dell'area client del visualizzatore appunti \_ sono cambiate.
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- WM_SIZECLIPBOARD messaggio Data Exchange
topic_type:
- apiref
api_name:
- WM_SIZECLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 778caa6538992d927a0451518fcb28b82891773563614ba97c9d9df121fb69f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545320"
---
# <a name="wm_sizeclipboard-message"></a>Messaggio \_ WM SIZECLIPBOARD

Inviato al proprietario degli Appunti da una finestra del Visualizzatore Appunti quando gli Appunti contengono dati nel formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) e le dimensioni dell'area client del visualizzatore appunti sono cambiate.


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra del visualizzatore Appunti.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per un oggetto memoria globale che contiene una [**struttura RECT.**](/previous-versions//dd162897(v=vs.85)) La struttura specifica le nuove dimensioni dell'area client del visualizzatore Appunti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Quando la finestra del visualizzatore Appunti sta per essere distrutta o ridimensionata, viene inviato un messaggio **\_ WM SIZECLIPBOARD** con un rettangolo Null (0, 0, 0, 0) come nuova dimensione. In questo modo il proprietario degli Appunti può liberare le risorse di visualizzazione.

Il proprietario degli Appunti deve usare la [**funzione GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) per bloccare l'oggetto memoria che contiene [**RECT.**](/previous-versions//dd162897(v=vs.85)) Prima della restituzione, il proprietario degli Appunti deve sbloccare l'oggetto usando la [**funzione GlobalUnlock.**](/windows/desktop/api/winbase/nf-winbase-globalunlock)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> </dl>

 

