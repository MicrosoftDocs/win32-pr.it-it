---
title: Messaggio TBM_SETUNICODEFORMAT (COMmctrl. h)
description: Imposta il flag di formato carattere Unicode per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo.
ms.assetid: c50a49e8-6042-490d-bb7b-baf917d5c30a
keywords:
- Controlli di Windows Message TBM_SETUNICODEFORMAT
topic_type:
- apiref
api_name:
- TBM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adb64c8fcb3464067e9522695930f4f9d0771357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301274"
---
# <a name="tbm_setunicodeformat-message"></a>\_Messaggio SETUNICODEFORMAT TBM

Imposta il flag di formato carattere Unicode per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo.

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

[**TBM \_ GETUNICODEFORMAT**](tbm-getunicodeformat.md)
</dt> </dl>

 

 





