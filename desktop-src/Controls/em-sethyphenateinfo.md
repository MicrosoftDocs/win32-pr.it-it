---
title: Messaggio di EM_SETHYPHENATEINFO (RichEdit. h)
description: Imposta il modo in cui un controllo Rich Edit esegue la sillabazione.
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- Controlli di Windows Message EM_SETHYPHENATEINFO
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
ms.openlocfilehash: b8369d463ae03e9410347ab58a50346625e3de47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874357"
---
# <a name="em_sethyphenateinfo-message"></a>\_Messaggio SETHYPHENATEINFO em

Imposta il modo in cui un controllo Rich Edit esegue la sillabazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Puntatore a una struttura [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) .

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato, deve essere zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> Per abilitare la sillabazione, il client deve chiamare [**em \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md), specificando \_ ADVANCEDTYPOGRAPHY.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP1 \[\]<br/>                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETHYPHENATEINFO em**](em-gethyphenateinfo.md)
</dt> </dl>

 

 





