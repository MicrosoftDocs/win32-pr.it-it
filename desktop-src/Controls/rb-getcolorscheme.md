---
title: RB_GETCOLORSCHEME messaggio (Commctrl.h)
description: Recupera le informazioni sulla combinazione di colori dal controllo Rebar.
ms.assetid: 01f81c4b-bbc9-43ae-a1f5-1e289c6fa278
keywords:
- RB_GETCOLORSCHEME controlli Windows messaggio
topic_type:
- apiref
api_name:
- RB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b918b46d1077c0074584be2d609d486097cc2e40f7a5c62a03db914fce58e320
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169621"
---
# <a name="rb_getcolorscheme-message"></a>Messaggio RB \_ GETCOLORSCHEME

Recupera le informazioni sulla combinazione di colori dal controllo Rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) che riceverà le informazioni sulla combinazione di colori. È necessario impostare il **membro dwSize** di questa struttura su **sizeof**(COLORSCHEME) prima di inviare questo messaggio.

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

[**RB \_ SETCOLORSCHEME**](rb-setcolorscheme.md)
</dt> </dl>

 

 





