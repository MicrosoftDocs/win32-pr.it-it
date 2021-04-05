---
title: Messaggio WM_SIZECLIPBOARD (winuser. h)
description: Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti quando gli Appunti contengono dati nel \_ formato CF OWNERDISPLAY e le dimensioni dell'area client del Visualizzatore Appunti sono state modificate.
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- Scambio di dati del messaggio WM_SIZECLIPBOARD
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
ms.openlocfilehash: 235de630b20757a571b1917a975d1425bee06cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741863"
---
# <a name="wm_sizeclipboard-message"></a>\_Messaggio SIZECLIPBOARD WM

Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti quando gli Appunti contengono dati nel formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) e le dimensioni dell'area client del Visualizzatore Appunti sono state modificate.


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra del visualizzatore degli Appunti.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per un oggetto memoria globale che contiene una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) . La struttura specifica le nuove dimensioni dell'area client del visualizzatore degli Appunti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Quando la finestra Visualizzatore Appunti sta per essere distrutta o ridimensionata, viene inviato un messaggio **WM \_ SIZECLIPBOARD** con un rettangolo null (0, 0, 0, 0) come nuova dimensione. Ciò consente al proprietario degli Appunti di liberare le risorse di visualizzazione.

Il proprietario degli Appunti deve usare la funzione [**funzione GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) per bloccare l'oggetto Memory che contiene [**Rect**](/previous-versions//dd162897(v=vs.85)). Prima di restituire, il proprietario degli Appunti deve sbloccare l'oggetto utilizzando la funzione [**funzione GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> </dl>

 

