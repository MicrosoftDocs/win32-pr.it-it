---
title: EM_GETLINECOUNT messaggio (Winuser.h)
description: Ottiene il numero di righe in un controllo di modifica su più righe. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETLINECOUNT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETLINECOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44487084da8df8edd463fc0683c9d27fcba19a2993465e5493edfd8bb7c3c6b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006684"
---
# <a name="em_getlinecount-message-winuserh"></a>EM_GETLINECOUNT messaggio (Winuser.h)

Ottiene il numero di righe in un controllo di modifica su più righe. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un numero intero che specifica il numero totale di righe di testo nel controllo di modifica su più righe o nel controllo Rich Edit. Se il controllo non contiene testo, il valore restituito è 1. Il valore restituito non sarà mai minore di 1.

## <a name="remarks"></a>Commenti

Il **messaggio EM \_ GETLINECOUNT** recupera il numero totale di righe di testo, non solo il numero di righe attualmente visibili.

Se la funzionalità Wordwrap è abilitata, il numero di righe può cambiare quando cambiano le dimensioni della finestra di modifica.

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ GETLINE**](em-getline.md)
</dt> <dt>

[**EM \_ LINELENGTH**](em-linelength.md)
</dt> <dt>

[**Modificare \_ GetLineCount**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 





