---
title: CB_GETHORIZONTALEXTENT messaggio (Winuser.h)
description: Ottiene la larghezza, in pixel, che la casella di riepilogo può scorrere orizzontalmente (larghezza scorrevole). È applicabile solo se la casella di riepilogo ha una barra di scorrimento orizzontale.
ms.assetid: 7c9fff88-2750-4c94-b7f6-6bdd81c224e9
keywords:
- CB_GETHORIZONTALEXTENT controlli di Windows messaggio
topic_type:
- apiref
api_name:
- CB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 928561b812dd3a09909d8d89c7dda1dc67b63f9177769d80db2d16ac78cbbf72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089211"
---
# <a name="cb_gethorizontalextent-message"></a>CB \_ GETHORIZONTALEXTENT message

Ottiene la larghezza, in pixel, che la casella di riepilogo può scorrere orizzontalmente (larghezza scorrevole). È applicabile solo se la casella di riepilogo ha una barra di scorrimento orizzontale.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è la larghezza scorrevole, in pixel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CB \_ SETHORIZONTALEXTENT**](cb-sethorizontalextent.md)
</dt> </dl>

 

 





