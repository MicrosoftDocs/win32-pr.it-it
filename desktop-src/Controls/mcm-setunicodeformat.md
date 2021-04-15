---
title: Messaggio MCM_SETUNICODEFORMAT (COMmctrl. h)
description: Imposta il flag di formato carattere Unicode per il controllo.
ms.assetid: 250789b5-694b-4502-9cc0-3bc260ea06e7
keywords:
- Controlli di Windows Message MCM_SETUNICODEFORMAT
topic_type:
- apiref
api_name:
- MCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0aee3318479f4e94b4d85f15fe7c58e4417a1bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476966"
---
# <a name="mcm_setunicodeformat-message"></a>\_Messaggio SETUNICODEFORMAT MCM

Imposta il flag di formato carattere Unicode per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetUnicodeFormat di MonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat) .

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

[**\_GETUNICODEFORMAT MCM**](mcm-getunicodeformat.md)
</dt> </dl>

 

 





