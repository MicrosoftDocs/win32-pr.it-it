---
title: Messaggio EM_GETLINECOUNT (winuser. h)
description: Ottiene il numero di righe in un controllo di modifica su più righe. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- Controlli di Windows Message EM_GETLINECOUNT
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
ms.openlocfilehash: 15ffbeafb13850317faccb4be44571d81b0d7e36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475569"
---
# <a name="em_getlinecount-message-winuserh"></a>Messaggio EM_GETLINECOUNT (winuser. h)

Ottiene il numero di righe in un controllo di modifica su più righe. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

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

Il valore restituito è un Integer che specifica il numero totale di righe di testo nel controllo di modifica su più righe o in un controllo Rich Edit. Se il controllo non ha testo, il valore restituito è 1. Il valore restituito non sarà mai minore di 1.

## <a name="remarks"></a>Commenti

Il **messaggio \_ GETLINECOUNT em** Recupera il numero totale di righe di testo, non solo il numero di righe attualmente visibili.

Se la funzionalità WordWrap è abilitata, il numero di righe può cambiare quando cambiano le dimensioni della finestra di modifica.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

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

[**\_riga em**](em-getline.md)
</dt> <dt>

[**\_LINELENGTH em**](em-linelength.md)
</dt> <dt>

[**Modifica \_ GetLineCount**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 





