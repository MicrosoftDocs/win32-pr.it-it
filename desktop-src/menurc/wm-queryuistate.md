---
title: WM_QUERYUISTATE messaggio (Winuser.h)
description: Un'applicazione invia il messaggio \_ WM QUERYUISTATE per recuperare lo stato dell'interfaccia utente per una finestra.
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- WM_QUERYUISTATE menu e altre risorse del messaggio
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
ms.openlocfilehash: e62fc33fb79594f3e07c0d44d4b25fd16e980ef3a4a89b3079c69ef6eb5d1b89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119267911"
---
# <a name="wm_queryuistate-message"></a>Messaggio \_ WM QUERYUISTATE

Un'applicazione invia il **messaggio \_ WM QUERYUISTATE** per recuperare lo stato dell'interfaccia utente per una finestra.


```C++
#define WM_QUERYUISTATE                 0x0129
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere 0.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **NULL se** gli indicatori dello stato attivo e i tasti di scelta rapida sono visibili. In caso contrario, il valore restituito può essere uno o più dei valori seguenti.



| Codice/valore restituito                                                                                                                                       | Descrizione                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**UISF \_ Active**</dt> <dt>0x4</dt> </dl>    | Un controllo deve essere disegnato nello stile usato per i controlli attivi.<br/> |
| <dl> <dt>**UISF \_ HideACCEL**</dt> <dt>0x2</dt> </dl> | I tasti di scelta rapida sono nascosti.<br/>                                |
| <dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Gli indicatori di stato attivo sono nascosti.<br/>                                     |



 

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

[**WM \_ CHANGEUISTATE**](wm-changeuistate.md)
</dt> <dt>

[**WM \_ UPDATEUISTATE**](wm-updateuistate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

 

 





