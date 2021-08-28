---
title: TB_GETCOLORSCHEME messaggio (Commctrl.h)
description: Recupera le informazioni sulla combinazione di colori dal controllo barra degli strumenti.
ms.assetid: af172631-309e-4181-a690-05946cd6e143
keywords:
- TB_GETCOLORSCHEME di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fca3a7a88fd108454c3838d646db311c9be19bf04163b4c8987db67f6c09c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918871"
---
# <a name="tb_getcolorscheme-message"></a>TB \_ GETCOLORSCHEME message

Recupera le informazioni sulla combinazione di colori dal controllo barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) che riceverà le informazioni sulla combinazione di colori. È necessario impostare il **membro cbSize** di questa struttura su **sizeof**(COLORSCHEME) prima di inviare questo messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TB \_ SETCOLORSCHEME**](tb-setcolorscheme.md)
</dt> </dl>

 

 





