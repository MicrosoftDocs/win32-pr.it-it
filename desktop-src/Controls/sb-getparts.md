---
title: SB_GETPARTS messaggio (Commctrl.h)
description: Recupera un conteggio delle parti in una finestra di stato. Il messaggio recupera anche la coordinata del bordo destro del numero specificato di parti.
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- SB_GETPARTS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- SB_GETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4318579b67adda9ab55a9dad4ad73949214758443c5e2151ce40cbb996fd90cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168757"
---
# <a name="sb_getparts-message"></a>Messaggio \_ GETPARTS SB

Recupera un conteggio delle parti in una finestra di stato. Il messaggio recupera anche la coordinata del bordo destro del numero specificato di parti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di parti per le quali recuperare le coordinate. Se questo parametro è maggiore del numero di parti nella finestra, il messaggio recupera le coordinate solo per le parti esistenti.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di interi con lo stesso numero di elementi delle parti specificate da *wParam*. Ogni elemento nella matrice riceve la coordinata client del bordo destro della parte corrispondente. Se un elemento è impostato su -1, la posizione del bordo destro per tale parte si estende al bordo destro della finestra. Per recuperare il numero corrente di parti, impostare questo parametro su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di parti nella finestra.

## <a name="remarks"></a>Commenti

Questo messaggio restituisce sempre il numero di parti nella barra di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





