---
title: Messaggio ACM_PLAY (COMmctrl. h)
description: Riproduce un clip AVI in un controllo dell'animazione. Il controllo riproduce il clip in background mentre il thread continua l'esecuzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro animazione.
ms.assetid: 738b7305-bb77-441d-a198-17daf3b76039
keywords:
- Controlli di Windows Message ACM_PLAY
topic_type:
- apiref
api_name:
- ACM_PLAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e501f3718e1b8172e2b7b16566f992c26346b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475760"
---
# <a name="acm_play-message"></a>\_Messaggio di riproduzione ACM

Riproduce un clip AVI in un controllo dell'animazione. Il controllo riproduce il clip in background mentre il thread continua l'esecuzione. È possibile inviare questo messaggio in modo esplicito o utilizzando [**\_ la macro animazione**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**Uint** che specifica il numero di volte in cui riprodurre il clip AVI. Il valore-1 indica la riproduzione illimitata del clip.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è l'indice in base zero del frame in cui inizia la riproduzione. Il valore deve essere minore di 65.536. Il valore zero indica che iniziano con il primo fotogramma del clip AVI.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è l'indice in base zero del frame in cui termina la riproduzione. Il valore deve essere minore di 65.536. Il valore-1 indica che termina con l'ultimo frame del clip AVI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

È possibile usare [**animate \_ Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) per indirizzare il controllo dell'animazione in modo da visualizzare un particolare frame del clip AVI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

