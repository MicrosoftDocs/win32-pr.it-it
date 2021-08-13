---
title: EM_SETHYPHENATEINFO messaggio (Richedit.h)
description: Imposta il modo in cui un controllo Rich Edit esegue la sillabazione.
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- EM_SETHYPHENATEINFO di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5551aace3ab054c1c6fa322242ae06386ff19f5a44775bd6dcc6887d19c65c62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437561"
---
# <a name="em_sethyphenateinfo-message"></a>Messaggio EM \_ SETHYPHENATEINFO

Imposta il modo in cui un controllo Rich Edit esegue la sillabazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Puntatore a una [**struttura HYPHENATEINFO.**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo)

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato, deve essere zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> Per abilitare la sillabazione, il client deve [**chiamare EM \_ SETTYPOGRAPHYOPTIONS,**](em-settypographyoptions.md)specificando TO \_ ADVANCEDTYPOGRAPHY.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP1 \[\]<br/>                                  |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETHYPHENATEINFO**](em-gethyphenateinfo.md)
</dt> </dl>

 

 





