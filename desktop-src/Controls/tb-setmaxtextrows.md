---
title: TB_SETMAXTEXTROWS messaggio (Commctrl.h)
description: Imposta il numero massimo di righe di testo visualizzate su un pulsante della barra degli strumenti.
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- TB_SETMAXTEXTROWS dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- TB_SETMAXTEXTROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a1e1a2cda7b3dced4cf538623578d48b41d38925629f2985a35974baed229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167481"
---
# <a name="tb_setmaxtextrows-message"></a>TB \_ SETMAXTEXTROWS message

Imposta il numero massimo di righe di testo visualizzate su un pulsante della barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero massimo di righe di testo che possono essere visualizzate.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Per fare in modo che il testo va a capo, è necessario impostare la larghezza massima del pulsante inviando un [**\_ messaggio SETBUTTONWIDTH DA TB.**](tb-setbuttonwidth.md) Il testo va a capo in corrispondenza di un'interruzione di parola; Le interruzioni di riga (" \\ n") nel testo vengono ignorate. Il testo nelle barre \_ degli strumenti TBSTYLE LIST viene sempre visualizzato su una singola riga.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





