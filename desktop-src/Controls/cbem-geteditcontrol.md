---
title: CBEM_GETEDITCONTROL messaggio (Commctrl.h)
description: Ottiene l'handle per la parte del controllo di modifica di un controllo ComboBoxEx. Un controllo ComboBoxEx usa una casella di modifica quando è impostato sullo stile elenco a discesa \_ CBS.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- CBEM_GETEDITCONTROL di controllo Windows messaggio
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
ms.openlocfilehash: 885a90a1b37fab7cd8e4a492bd00ad349f96202e13ee25a404f7f4aa41f623e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414071"
---
# <a name="cbem_geteditcontrol-message"></a>Messaggio CBEM \_ GETEDITCONTROL

Ottiene l'handle per la parte del controllo di modifica di un controllo ComboBoxEx. Un controllo ComboBoxEx usa una casella di modifica quando è impostato sullo stile elenco a discesa [**CBS. \_**](combo-box-styles.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il controllo di modifica all'interno del controllo ComboBoxEx se usa lo stile [**DROPDOWN di \_ CBS.**](combo-box-styles.md) In caso contrario, il messaggio restituisce **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





