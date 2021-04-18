---
title: Messaggio BM_SETSTATE (winuser. h)
description: Imposta lo stato di evidenziazione di un pulsante. Lo stato di evidenziazione indica se il pulsante è evidenziato come se l'utente avesse eseguito il push. È possibile inviare questo messaggio in modo esplicito o usare la macro di stato del pulsante \_ .
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- Controlli di Windows Message BM_SETSTATE
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9b60231980f406b0aeb499d724dc6aa7025513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301276"
---
# <a name="bm_setstate-message"></a>\_Messaggio di SESTATO BM

Imposta lo stato di evidenziazione di un pulsante. Lo stato di evidenziazione indica se il pulsante è evidenziato come se l'utente avesse eseguito il push. È possibile inviare questo messaggio in modo esplicito o usare la macro di [**\_ stato del pulsante**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore **booleano** che specifica se il pulsante è evidenziato. Il valore **true** evidenzia il pulsante. Il valore **false** consente di rimuovere tutte le evidenziazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce sempre zero.

## <a name="remarks"></a>Commenti

L'evidenziazione influiscono solo sull'aspetto di un pulsante. Non ha alcun effetto sullo stato di selezione di un pulsante di opzione o di una casella di controllo.

Un pulsante viene evidenziato automaticamente quando l'utente posiziona il cursore su di esso e preme e tiene premuto il pulsante sinistro del mouse. L'evidenziazione viene rimossa quando l'utente rilascia il pulsante del mouse.

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

[**BM \_ GETstate**](bm-getstate.md)
</dt> <dt>

[**\_controllo BM**](bm-setcheck.md)
</dt> </dl>

 

 





