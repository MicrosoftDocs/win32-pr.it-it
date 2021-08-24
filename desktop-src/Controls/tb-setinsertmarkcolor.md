---
title: TB_SETINSERTMARKCOLOR messaggio (Commctrl.h)
description: Imposta il colore utilizzato per disegnare il segno di inserimento per la barra degli strumenti.
ms.assetid: 09a04449-9a1f-4f9a-b09f-9f22f930d735
keywords:
- TB_SETINSERTMARKCOLOR dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TB_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 466c9bfe27462b11cc0c6cf3a183328ddedb1b422b4d0c07b4496c7a90f83890
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540041"
---
# <a name="tb_setinsertmarkcolor-message"></a>TB \_ MESSAGGIO SETINSERTMARKCOLOR

Imposta il colore utilizzato per disegnare il segno di inserimento per la barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

**Valore COLORREF** che contiene il nuovo colore del segno di inserimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore COLORREF** che contiene il colore del segno di inserimento precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TB \_ GETINSERTMARKCOLOR**](tb-getinsertmarkcolor.md)
</dt> </dl>

 

 





