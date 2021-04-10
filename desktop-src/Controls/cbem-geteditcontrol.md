---
title: Messaggio CBEM_GETEDITCONTROL (COMmctrl. h)
description: Ottiene l'handle per la parte del controllo di modifica di un controllo ComboBoxEx. Un controllo ComboBoxEx usa una casella di modifica quando è impostata sullo stile a \_ discesa CBS.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- Controlli di Windows Message CBEM_GETEDITCONTROL
topic_type:
- apiref
api_name:
- CBEM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412d1183b29c8c89b5977d5f7f2a1b962d54dc01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121050"
---
# <a name="cbem_geteditcontrol-message"></a>\_Messaggio CBEM GETEDITCONTROL

Ottiene l'handle per la parte del controllo di modifica di un controllo ComboBoxEx. Un controllo ComboBoxEx usa una casella di modifica quando è impostata sullo stile [**a \_ discesa CBS**](combo-box-styles.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il controllo di modifica all'interno del controllo ComboBoxEx se usa lo stile a [**\_ discesa CBS**](combo-box-styles.md) . In caso contrario, il messaggio restituisce **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





