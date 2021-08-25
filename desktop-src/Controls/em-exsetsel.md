---
title: EM_EXSETSEL messaggio (Richedit.h)
description: Seleziona un intervallo di caratteri o Component Object Model (COM) in un controllo Microsoft Rich Edit.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- EM_EXSETSEL di Windows messaggi
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e35840e404f295b7d3ed6ddd5dddf4c77076c236eb3260f6f719b152cef207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915651"
---
# <a name="em_exsetsel-message"></a>Messaggio \_ EM EXSETSEL

Seleziona un intervallo di caratteri o Component Object Model (COM) in un controllo Microsoft Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) che specifica l'intervallo di selezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è la selezione effettivamente impostata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





