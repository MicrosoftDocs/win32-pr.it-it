---
title: Messaggio WM_QUERYUISTATE (winuser. h)
description: Un'applicazione invia il \_ messaggio WM QUERYUISTATE per recuperare lo stato dell'interfaccia utente per una finestra.
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- Menu del messaggio WM_QUERYUISTATE e altre risorse
topic_type:
- apiref
api_name:
- WM_QUERYUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1574fe0dab2a0885c8012bf19eed50facfd6cce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302726"
---
# <a name="wm_queryuistate-message"></a>\_Messaggio QUERYUISTATE WM

Un'applicazione invia il messaggio **WM \_ QUERYUISTATE** per recuperare lo stato dell'interfaccia utente per una finestra.


```C++
#define WM_QUERYUISTATE                 0x0129
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere 0.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **null** se gli indicatori di stato attivo e i tasti di scelta rapida sono visibili. In caso contrario, il valore restituito può essere uno o più dei valori seguenti.



| Codice/valore restituito                                                                                                                                       | Descrizione                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**UISF \_**</dt> <dt>0x4</dt> attivo </dl>    | Un controllo deve essere disegnato nello stile usato per i controlli attivi.<br/> |
| <dl> <dt>**UISF \_**</dt> <dt>0x2</dt> HIDEACCEL </dl> | Gli acceleratori tastiera sono nascosti.<br/>                                |
| <dl> <dt>**UISF \_**</dt> <dt>0x1</dt> hideFocus </dl> | Gli indicatori di stato attivo sono nascosti.<br/>                                     |



 

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

[**\_CHANGEUISTATE WM**](wm-changeuistate.md)
</dt> <dt>

[**\_UPDATEUISTATE WM**](wm-updateuistate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

 

 





