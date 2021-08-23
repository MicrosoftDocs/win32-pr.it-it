---
title: EM_GETRECT messaggio (Winuser.h)
description: Ottiene il rettangolo di formattazione di un controllo di modifica.
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- EM_GETRECT dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_GETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d4ad7dbab40a8d294d814e3524b54c5b11206c91608e9293bdf88df2a63f23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541041"
---
# <a name="em_getrect-message"></a>Messaggio \_ EM GETRECT

Ottiene il [rettangolo di formattazione](about-edit-controls.md) di un controllo di modifica. Il rettangolo di formattazione è il rettangolo di limitazione in cui il controllo disegna il testo. Il rettangolo di limitazione è indipendente dalle dimensioni della finestra di controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che riceve il rettangolo di formattazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non è significativo.

## <a name="remarks"></a>Commenti

È possibile modificare il rettangolo di formattazione di un controllo di modifica su più righe usando i messaggi [**EM \_ SETRECT**](em-setrect.md) ed [**EM \_ SETRECTNP.**](em-setrectnp.md)

In determinate **condizioni, EM \_ GETRECT** potrebbe non restituire i valori esatti impostati da [**EM \_ SETRECT**](em-setrect.md) o [**EM \_ SETRECTNP,**](em-setrectnp.md) ma può essere disattivato di pochi pixel.

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Il rettangolo di formattazione non include la barra di selezione, ovvero un'area non contrassegnata a sinistra di ogni paragrafo. Quando si fa clic, la barra di selezione seleziona la linea. Per informazioni sulla compatibilità delle versioni rich edit con le diverse versioni del sistema, vedere [Informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

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

[**EM \_ SETRECT**](em-setrect.md)
</dt> <dt>

[**EM \_ SETRECTNP**](em-setrectnp.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

