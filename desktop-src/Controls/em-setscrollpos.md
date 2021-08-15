---
title: EM_SETSCROLLPOS messaggio (Richedit.h)
description: Scorre il contenuto di un controllo Rich Edit fino al punto specificato.
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- EM_SETSCROLLPOS controlli di Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d86609c1b3f4b04ade24e5ea2f3343c367bbad0a52b8e07be7c18b2282536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412336"
---
# <a name="em_setscrollpos-message"></a>Messaggio \_ EM SETSCROLLPOS

Scorre il contenuto di un controllo Rich Edit fino al punto specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura POINT**](/previous-versions//dd162805(v=vs.85)) che specifica un punto nello spazio di testo virtuale del documento, espresso in pixel. Verrà fatto scorrere il documento fino a quando questo punto non si trova nell'angolo superiore sinistro della finestra di controllo di modifica. Se si vuole modificare la visualizzazione in modo che l'angolo superiore sinistro della visualizzazione sia di due righe verso il basso e un carattere in dal bordo sinistro. Si passerebbe un punto di (7, 22).

Il controllo Rich Edit controlla le coordinate x e y e, se necessario, le regola, in modo che nella parte superiore sia visualizzata una riga completa. Garantisce inoltre che il testo non sia mai completamente scorrendo dal rettangolo di visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce sempre 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Componente ridistribuibile<br/>          | Rich Edit 3.0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETSCROLLPOS**](em-getscrollpos.md)
</dt> </dl>

 

