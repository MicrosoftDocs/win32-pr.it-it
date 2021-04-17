---
title: Messaggio HDM_SETUNICODEFORMAT (COMmctrl. h)
description: Imposta il flag di formato carattere UNICODE per il controllo.
ms.assetid: 18161fe5-c779-4be0-9e7a-1b5948e42b80
keywords:
- Controlli di Windows Message HDM_SETUNICODEFORMAT
topic_type:
- apiref
api_name:
- HDM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3fe3497413b265510426fab4ef2e71666f46312
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476972"
---
# <a name="hdm_setunicodeformat-message"></a>\_Messaggio HDM SETUNICODEFORMAT

Imposta il flag di formato carattere UNICODE per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetUnicodeFormat dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_setunicodeformat) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Set di caratteri utilizzato dal controllo. Se questo valore è diverso da zero, il controllo utilizzerà caratteri Unicode. Se questo valore è zero, il controllo utilizzerà caratteri ANSI.

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

[**\_GETUNICODEFORMAT HDM**](hdm-getunicodeformat.md)
</dt> </dl>

 

 





