---
title: Messaggio TB_SETBUTTONWIDTH (COMmctrl. h)
description: Imposta le larghezze minime e massime del pulsante nel controllo Toolbar.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- Controlli di Windows Message TB_SETBUTTONWIDTH
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
ms.openlocfilehash: 5e105770d72e90108b9c31311f77599520cecea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119823"
---
# <a name="tb_setbuttonwidth-message"></a>TB \_ SETBUTTONWIDTH messaggio

Imposta le larghezze minime e massime del pulsante nel controllo Toolbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la larghezza minima del pulsante in pixel. I pulsanti della barra degli strumenti non saranno mai più stretti di questo valore.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la larghezza massima del pulsante, in pixel. Se il testo del pulsante è troppo ampio, il controllo lo Visualizza con puntini di sospensione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Usare **TB \_ SETBUTTONWIDTH** per impostare le larghezze massime e minime consentite per i pulsanti prima di aggiungerli. Usare [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) per impostare le dimensioni effettive dei pulsanti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

