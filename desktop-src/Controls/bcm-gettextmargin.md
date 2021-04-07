---
title: Messaggio BCM_GETTEXTMARGIN (COMmctrl. h)
description: Ottiene i margini utilizzati per creare il testo in un controllo Button. È possibile inviare questo messaggio in modo esplicito o usare il pulsante \_ GetTextMargin macro.
ms.assetid: 6c141752-e636-41c4-9d05-df8b320ff59f
keywords:
- Controlli di Windows Message BCM_GETTEXTMARGIN
topic_type:
- apiref
api_name:
- BCM_GETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a7d809207c21c74a36c796a9035ed0e3772481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964121"
---
# <a name="bcm_gettextmargin-message"></a>\_Messaggio GETTEXTMARGIN BCM

Ottiene i margini utilizzati per creare il testo in un controllo Button. È possibile inviare questo messaggio in modo esplicito o usare il [**pulsante \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) macro.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene i margini da utilizzare per il disegno del testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, restituisce **true**. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

