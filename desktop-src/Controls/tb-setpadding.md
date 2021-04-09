---
title: Messaggio TB_SETPADDING (COMmctrl. h)
description: Imposta la spaziatura interna per un controllo Toolbar.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- Controlli di Windows Message TB_SETPADDING
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
ms.openlocfilehash: 65fae53f7e7702528915af7631bd675f11188b71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121151"
---
# <a name="tb_setpadding-message"></a>\_Messaggio di SEPADDING TB

Imposta la spaziatura interna per un controllo Toolbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la spaziatura interna orizzontale, in pixel. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la spaziatura interna verticale, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **DWORD** che contiene la spaziatura orizzontale precedente in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e la spaziatura verticale precedente in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))in pixel.

## <a name="remarks"></a>Commenti

I valori di riempimento vengono usati per creare un'area vuota tra il bordo del pulsante e l'immagine del pulsante e/o il testo. La posizione e la quantità di riempimento effettivamente applicate variano a seconda del tipo di pulsante e della presenza di un'immagine. La spaziatura interna orizzontale viene applicata sia a destra che a sinistra del pulsante e la spaziatura interna verticale viene applicata sia alla parte superiore che alla parte inferiore del pulsante. La spaziatura interna viene applicata solo ai pulsanti con stile [**\_ AUTOSIZE TBSTYLE**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TB \_ GETpadding**](tb-getpadding.md)
</dt> </dl>

 

