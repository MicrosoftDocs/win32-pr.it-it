---
title: Messaggio LVM_GETSTRINGWIDTH (COMmctrl. h)
description: Determina la larghezza di una stringa specificata usando il tipo di carattere corrente del controllo visualizzazione elenco specificato. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetStringWidth di ListView.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- Controlli di Windows Message LVM_GETSTRINGWIDTH
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
ms.openlocfilehash: 71e27512eb7a2a260976356ed2a128b48975f9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518652"
---
# <a name="lvm_getstringwidth-message"></a>\_Messaggio GETSTRINGWIDTH LVM

Determina la larghezza di una stringa specificata usando il tipo di carattere corrente del controllo visualizzazione elenco specificato. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetStringWidth di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una stringa con terminazione null.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la larghezza della stringa in caso di esito positivo; in caso contrario, zero.

## <a name="remarks"></a>Commenti

Il \_ messaggio LVM GETSTRINGWIDTH restituisce la larghezza esatta, in pixel, della stringa specificata. Se si usa la larghezza della stringa restituita come larghezza della colonna nel messaggio [**LVM \_ SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) , la stringa verrà troncata. Per recuperare la larghezza della colonna che può contenere la stringa senza troncarla, è necessario aggiungere la spaziatura interna alla lunghezza della stringa restituita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ GETSTRINGWIDTHW** (Unicode) e **LVM \_ GETSTRINGWIDTHA** (ANSI)<br/>     |



 

 





