---
title: TB_SETPADDING messaggio (Commctrl.h)
description: Imposta la spaziatura interna per un controllo barra degli strumenti.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- TB_SETPADDING di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da488c7aab3a6856fd1bd8db6911336eb52881da396e287937678600158d9655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078165"
---
# <a name="tb_setpadding-message"></a>TB \_ SETPADDING message

Imposta la spaziatura interna per un controllo barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

LoWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) la spaziatura interna orizzontale, in pixel. La [**parola chiave HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la spaziatura interna verticale, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che contiene la spaziatura interna orizzontale precedente in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e la spaziatura interna verticale precedente in [**HIWORD,**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))in pixel.

## <a name="remarks"></a>Commenti

I valori di riempimento vengono usati per creare un'area vuota tra il bordo del pulsante e l'immagine e/o il testo del pulsante. La posizione e la quantità di spaziatura interna effettivamente applicata dipendono dal tipo di pulsante e dal fatto che abbia un'immagine. La spaziatura interna orizzontale viene applicata sia a destra che a sinistra del pulsante e la spaziatura interna verticale viene applicata sia alla parte superiore che alla parte inferiore del pulsante. La spaziatura interna viene applicata solo ai pulsanti con [**stile TBSTYLE \_ AUTOSIZE.**](toolbar-control-and-button-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TB \_ GETPADDING**](tb-getpadding.md)
</dt> </dl>

 

