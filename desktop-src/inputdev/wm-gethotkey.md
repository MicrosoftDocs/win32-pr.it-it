---
title: Messaggio WM_GETHOTKEY (winuser. h)
description: Inviato per determinare il tasto di scelta rapida associato a una finestra.
ms.assetid: 6f527758-e713-47a8-a571-3bf3270f0b33
keywords:
- Input della tastiera e del mouse WM_GETHOTKEY messaggio
topic_type:
- apiref
api_name:
- WM_GETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045ceefaf33c8d8edba0cb69e062ad589cfd833
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476157"
---
# <a name="wm_gethotkey-message"></a>\_Messaggio WM GEThotkey

Inviato per determinare il tasto di scelta rapida associato a una finestra.


```C++
#define WM_GETHOTKEY                    0x0033
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il codice della chiave virtuale e i modificatori per il tasto di scelta o **null** se alla finestra non è associato alcun tasto di scelta. Il codice della chiave virtuale si trova nel byte minimo del valore restituito e i modificatori sono nel byte massimo. I modificatori possono essere una combinazione dei flag seguenti di CommCtrl. h.



| Codice/valore restituito                                                                                                                                         | Descrizione             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt> </dl>     | ALT (tasto)<br/>      |
| <dl> <dt>**HOTKEYF \_**</dt> <dt>0x02</dt> di controllo </dl> | Tasto CTRL<br/>     |
| <dl> <dt>**HOTKEYF \_**</dt> <dt>0x08</dt> EXT </dl>     | Chiave estesa<br/> |
| <dl> <dt>**HOTKEYF \_ MAIUSC**</dt> <dt>0x01</dt> </dl>   | Tasto MAIUSC<br/>    |



 

## <a name="remarks"></a>Commenti

Questi tasti di scelta rapida non sono correlati ai tasti di scelta rapida impostati dalla funzione [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) .

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

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**sehotkey WM \_**](wm-sethotkey.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

