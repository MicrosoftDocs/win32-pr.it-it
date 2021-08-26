---
title: EM_EMPTYUNDOBUFFER messaggio (Winuser.h)
description: Reimposta il flag di annullamento di un controllo di modifica. Il flag di annullamento viene impostato ogni volta che un'operazione all'interno del controllo di modifica può essere annullata. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- EM_EMPTYUNDOBUFFER dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- EM_EMPTYUNDOBUFFER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63d59dab38bca921e2125377889f8d18ddf6eb45c023badeead47f7e07b860fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915901"
---
# <a name="em_emptyundobuffer-message"></a>Messaggio EM \_ EMPTYUNDOBUFFER

Reimposta il flag di annullamento di un controllo di modifica. Il flag di annullamento viene impostato ogni volta che un'operazione all'interno del controllo di modifica può essere annullata. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

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

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Il flag di annullamento viene reimpostato automaticamente ogni volta che il controllo di modifica riceve un [**messaggio WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) [**o EM \_ SETHANDLE.**](em-sethandle.md)

**Controlli di modifica e Rich Edit 1.0:** Il controllo può solo annullare o ripetere l'operazione più recente.

**Rich Edit 2.0 e versioni successive:** Il **messaggio EM \_ EMPTYUNDOBUFFER** svuota tutti i buffer di annullamento e di annullamento. I controlli Rich Edit consentono all'utente di annullare o ripetere più operazioni.

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le diverse versioni del sistema, vedere [Informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ CANUNDO**](em-canundo.md)
</dt> <dt>

[**EM \_ SETHANDLE**](em-sethandle.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

