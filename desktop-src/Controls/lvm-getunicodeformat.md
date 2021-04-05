---
title: Messaggio LVM_GETUNICODEFORMAT (COMmctrl. h)
description: Recupera il flag del formato carattere UNICODE per il controllo. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetUnicodeFormat di ListView.
ms.assetid: b0598b60-4d0e-4c68-b63a-e614c6268129
keywords:
- Controlli di Windows Message LVM_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- LVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720a65baab8ec9c1ec3b311e49fe3672c97a0fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874317"
---
# <a name="lvm_getunicodeformat-message"></a>\_Messaggio GETUNICODEFORMAT LVM

Recupera il flag del formato carattere UNICODE per il controllo. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetUnicodeFormat di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il flag di formato Unicode per il controllo. Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode. Se questo valore è zero, il controllo utilizza caratteri ANSI.

## <a name="remarks"></a>Commenti

Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETUNICODEFORMAT LVM**](lvm-setunicodeformat.md)
</dt> </dl>

 

 





