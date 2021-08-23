---
title: EM_SETREADONLY messaggio (Winuser.h)
description: Imposta o rimuove lo stile di sola lettura (ES \_ READONLY) di un controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETREADONLY di Windows di messaggi
topic_type:
- apiref
api_name:
- EM_SETREADONLY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d46726c1247f7ef93c00e495ca77ad3d337253705bd3018a0480fc9588c22f8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437511"
---
# <a name="em_setreadonly-message"></a>Messaggio EM \_ SETREADONLY

Imposta o rimuove lo stile di sola lettura ([**ES \_ READONLY**](edit-control-styles.md)) di un controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se impostare o rimuovere lo [**stile ES \_ READONLY.**](edit-control-styles.md) Il valore **TRUE imposta** lo stile **ES \_ READONLY.** Il valore **FALSE** rimuove lo **stile ES \_ READONLY.**

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è diverso da zero.

Se l'operazione non riesce, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Quando un controllo di modifica ha lo [**stile ES \_ READONLY,**](edit-control-styles.md) l'utente non può modificare il testo all'interno del controllo di modifica.

Per determinare se un controllo di modifica ha lo stile [**ES \_ READONLY,**](edit-control-styles.md) usare la [**funzione GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con il flag GWL \_ STYLE.

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le diverse versioni del sistema, vedere [Informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

