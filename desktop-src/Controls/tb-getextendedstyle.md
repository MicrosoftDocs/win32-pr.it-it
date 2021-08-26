---
title: TB_GETEXTENDEDSTYLE messaggio (Commctrl.h)
description: Recupera gli stili estesi per un controllo barra degli strumenti.
ms.assetid: d9e31a8e-5e5a-4d2d-bc3b-65ac40e8592f
keywords:
- TB_GETEXTENDEDSTYLE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab059933c2019009ebc746cc59df6affb840f09c40a201a4ee4048dc2498a17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918861"
---
# <a name="tb_getextendedstyle-message"></a>TB \_ GETEXTENDEDSTYLE message

Recupera gli stili estesi per un controllo barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD che** rappresenta gli stili attualmente in uso per il controllo barra degli strumenti. Questo valore può essere una combinazione [di stili estesi.](toolbar-extended-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TB \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md)
</dt> </dl>

 

 





