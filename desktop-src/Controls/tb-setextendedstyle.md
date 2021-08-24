---
title: TB_SETEXTENDEDSTYLE messaggio (Commctrl.h)
description: Imposta gli stili estesi per un controllo barra degli strumenti.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- TB_SETEXTENDEDSTYLE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 600e5904637215eeb052c85ec0203c9b86c75ed6b179be643dc9a213156b3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318881"
---
# <a name="tb_setextendedstyle-message"></a>TB \_ MESSAGGIO SETEXTENDEDSTYLE

Imposta gli stili estesi per un controllo barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore che specifica i nuovi stili estesi. Questo parametro può essere una combinazione [di stili estesi.](toolbar-extended-styles.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che rappresenta gli stili estesi precedenti. Questo valore può essere una combinazione [di stili estesi.](toolbar-extended-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TB \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md)
</dt> </dl>

 

 





