---
title: Messaggio CBEM_GETUNICODEFORMAT (COMmctrl. h)
description: Ottiene il flag del formato carattere UNICODE per il controllo.
ms.assetid: 854ff8d5-6e2f-4918-a6c5-91356a4454af
keywords:
- Controlli di Windows Message CBEM_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- CBEM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b77bb0daabe6ef14d4be1b5e2de6bb1dd63248d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874578"
---
# <a name="cbem_getunicodeformat-message"></a>\_Messaggio CBEM GETUNICODEFORMAT

Ottiene il flag del formato carattere UNICODE per il controllo.

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

[**\_SETUNICODEFORMAT CBEM**](cbem-setunicodeformat.md)
</dt> </dl>

 

 





