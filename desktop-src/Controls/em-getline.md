---
title: Messaggio EM_GETLINE (winuser. h)
description: Copia una riga di testo da un controllo di modifica e la inserisce in un buffer specificato. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- Controlli di Windows Message EM_GETLINE
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e014eaccba65b4ea1fc96e26872954a9cfc06e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963837"
---
# <a name="em_getline-message-winuserh"></a>Messaggio EM_GETLINE (winuser. h)

Copia una riga di testo da un controllo di modifica e la inserisce in un buffer specificato. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della riga da recuperare da un controllo di modifica su più righe. Un valore pari a zero specifica la riga più in alto. Questo parametro viene ignorato da un controllo di modifica a riga singola.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che riceve una copia della riga. Prima di inviare il messaggio, impostare la prima parola di questo buffer sulle dimensioni, in **TCHAR** s, del buffer. Per testo ANSI, indica il numero di byte; per il testo Unicode, indica il numero di caratteri. La dimensione nella prima parola viene sovrascritta dalla riga copiata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il numero di **TCHAR** copiate. Il valore restituito è zero se il numero di riga specificato dal parametro *wParam* è maggiore del numero di righe nel controllo di modifica.

## <a name="remarks"></a>Commenti

**Controlli di modifica:** La riga copiata non contiene un carattere null di terminazione.

**Controlli Rich Edit:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. La riga copiata non contiene un carattere null di terminazione, a meno che non sia stato copiato alcun testo. Se non è stato copiato alcun testo, il messaggio inserisce un carattere null all'inizio del buffer. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_LINELENGTH em**](em-linelength.md)
</dt> <dt>

[**Modifica \_ getline**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**WM \_ GETtext**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

