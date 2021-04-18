---
title: Messaggio LVM_SETUNICODEFORMAT (COMmctrl. h)
description: Imposta il flag di formato carattere UNICODE per il controllo.
ms.assetid: e332ae88-821f-4341-a98d-59d8a01a126f
keywords:
- Controlli di Windows Message LVM_SETUNICODEFORMAT
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
ms.openlocfilehash: 18b1e29d933892a24d7bc2ab472c7d591375362a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302283"
---
# <a name="lvm_setunicodeformat-message"></a>\_Messaggio SETUNICODEFORMAT LVM

Imposta il flag di formato carattere UNICODE per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetUnicodeFormat di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setunicodeformat) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Determina il set di caratteri utilizzato dal controllo. Se questo valore è diverso da zero, il controllo utilizzerà caratteri Unicode. Se questo valore è zero, il controllo utilizzerà caratteri ANSI.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il flag di formato Unicode precedente per il controllo.

## <a name="remarks"></a>Commenti

Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETUNICODEFORMAT LVM**](lvm-getunicodeformat.md)
</dt> </dl>

 

 





