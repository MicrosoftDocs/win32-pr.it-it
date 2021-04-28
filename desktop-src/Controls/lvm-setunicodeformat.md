---
title: LVM_SETUNICODEFORMAT messaggio (Commctrl.h)
description: 'LVM_SETUNICODEFORMAT messaggio: imposta il flag di formato carattere UNICODE per il controllo.'
ms.assetid: e332ae88-821f-4341-a98d-59d8a01a126f
keywords:
- LVM_SETUNICODEFORMAT messaggio Controlli Windows
topic_type:
- apiref
api_name:
- LVM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0f700cd057bc77eddc699404f37b19a6cc9c39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120149"
---
# <a name="lvm_setunicodeformat-message"></a>Messaggio LVM \_ SETUNICODEFORMAT

Imposta il flag di formato carattere UNICODE per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView SetUnicodeFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setunicodeformat)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Determina il set di caratteri utilizzato dal controllo . Se questo valore è diverso da zero, il controllo userà caratteri Unicode. Se questo valore è zero, il controllo userà caratteri ANSI.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il flag di formato Unicode precedente per il controllo.

## <a name="remarks"></a>Commenti

Per una descrizione di questo messaggio, vedere le osservazioni per [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LVM \_ GETUNICODEFORMAT**](lvm-getunicodeformat.md)
</dt> </dl>

 

 





