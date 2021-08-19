---
title: EM_SETSEL messaggio (Winuser.h)
description: Seleziona un intervallo di caratteri in un controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETSEL dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 190d8a62b874d3449e0a9bf5d334a515000fb0436ba73753a8657936363071b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062891"
---
# <a name="em_setsel-message"></a>Messaggio \_ EM SETSEL

Seleziona un intervallo di caratteri in un controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Posizione iniziale del carattere della selezione.

</dd> <dt>

*lParam* 
</dt> <dd>

Posizione del carattere finale della selezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Il valore iniziale può essere maggiore del valore finale. La parte inferiore dei due valori specifica la posizione del carattere del primo carattere nella selezione. Il valore più alto specifica la posizione del primo carattere oltre la selezione.

Il valore iniziale è il punto di ancoraggio della selezione e il valore finale è l'estremità attiva. Se l'utente usa MAIUSC per regolare le dimensioni della selezione, l'estremità attiva può spostarsi ma il punto di ancoraggio rimane invariato.

Se l'inizio è 0 e la fine è -1, tutto il testo nel controllo di modifica viene selezionato. Se l'inizio è -1, qualsiasi selezione corrente viene deselezionata.

**Controlli di modifica:** Il controllo visualizza un cursore lampeggiante nella posizione finale indipendentemente dai valori relativi di inizio e fine.

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le diverse versioni del sistema, vedere [Informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

Se il controllo di modifica ha lo stile [**ES \_ NOHIDESEL,**](edit-control-styles.md) il testo selezionato viene evidenziato indipendentemente dal fatto che il controllo abbia lo stato attivo. Senza lo **stile ES \_ NOHIDESEL,** il testo selezionato viene evidenziato solo quando il controllo di modifica ha lo stato attivo.

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

[**EM \_ GETSEL**](em-getsel.md)
</dt> <dt>

[**EM \_ REPLACESEL**](em-replacesel.md)
</dt> <dt>

[**EM \_ SCROLLCARET**](em-scrollcaret.md)
</dt> <dt>

[**EM \_ EXSETSEL**](em-exsetsel.md)
</dt> </dl>

 

 





