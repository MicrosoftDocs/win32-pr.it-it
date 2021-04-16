---
title: Messaggio SB_GETUNICODEFORMAT (COMmctrl. h)
description: Recupera il flag del formato carattere Unicode per il controllo.
ms.assetid: 0b2b543a-b1ef-452c-9b34-c5fbbac4aaa9
keywords:
- Controlli di Windows Message SB_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- SB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dbb639a04f0a40d9d5e11b938aaadbcc8b4c730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518442"
---
# <a name="sb_getunicodeformat-message"></a>\_Messaggio GETUNICODEFORMAT SB

Recupera il flag del formato carattere Unicode per il controllo.

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

[**\_SETUNICODEFORMAT SB**](sb-setunicodeformat.md)
</dt> </dl>

 

 





