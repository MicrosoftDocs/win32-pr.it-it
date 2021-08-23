---
title: LVM_GETSTRINGWIDTH messaggio (Commctrl.h)
description: Determina la larghezza di una stringa specificata usando il tipo di carattere corrente del controllo visualizzazione elenco specificato. Puoi inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetStringWidth.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- LVM_GETSTRINGWIDTH controlli Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETSTRINGWIDTH
- LVM_GETSTRINGWIDTHA
- LVM_GETSTRINGWIDTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9024cab94f59e543351e06d49ec058435ae369b6b746b1dc3fb2cd0472e3d57e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019309"
---
# <a name="lvm_getstringwidth-message"></a>Messaggio LVM \_ GETSTRINGWIDTH

Determina la larghezza di una stringa specificata usando il tipo di carattere corrente del controllo visualizzazione elenco specificato. Puoi inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetStringWidth.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una stringa con terminazione Null.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la larghezza della stringa in caso di esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Il messaggio LVM \_ GETSTRINGWIDTH restituisce la larghezza esatta, in pixel, della stringa specificata. Se si usa la larghezza della stringa restituita come larghezza di colonna nel messaggio [**LVM \_ SETCOLUMNWIDTH,**](lvm-setcolumnwidth.md) la stringa verrà troncata. Per recuperare la larghezza della colonna che può contenere la stringa senza troncarla, è necessario aggiungere spaziatura interna alla larghezza della stringa restituita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ GETSTRINGWIDTHW** (Unicode) e **LVM \_ GETSTRINGWIDTHA** (ANSI)<br/>     |



 

 





