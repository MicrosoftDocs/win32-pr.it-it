---
title: TB_SETBUTTONWIDTH messaggio (Commctrl.h)
description: Imposta le larghezze minime e massime dei pulsanti nel controllo barra degli strumenti.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- TB_SETBUTTONWIDTH dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TB_SETBUTTONWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 145ae1459b76fba60dd76b34e36d222cf62b93af071f2b430321d86956a3a871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167596"
---
# <a name="tb_setbuttonwidth-message"></a>TB \_ SETBUTTONWIDTH message

Imposta le larghezze minime e massime dei pulsanti nel controllo barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la larghezza minima del pulsante, in pixel. I pulsanti della barra degli strumenti non saranno mai più ristretti di questo valore.

HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la larghezza massima del pulsante, in pixel. Se il testo del pulsante è troppo ampio, il controllo lo visualizza con puntini di sospensione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Usare **TB \_ SETBUTTONWIDTH** per impostare le larghezze massime e minime consentite per i pulsanti prima che siano aggiunti. Usare [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) per impostare le dimensioni effettive dei pulsanti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

