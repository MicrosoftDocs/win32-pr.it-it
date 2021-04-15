---
title: Messaggio BCM_SETTEXTMARGIN (COMmctrl. h)
description: Il \_ messaggio BCM SETTEXTMARGIN imposta i margini per il disegno di testo in un controllo Button.
ms.assetid: 0798b1c5-7db4-46c6-8881-4c847abc7460
keywords:
- Controlli di Windows Message BCM_SETTEXTMARGIN
topic_type:
- apiref
api_name:
- BCM_SETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb6653007c155a508ce4da899a7be0d8ff2ab2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476660"
---
# <a name="bcm_settextmargin-message"></a>\_Messaggio SETTEXTMARGIN BCM

Il messaggio **BCM \_ SETTEXTMARGIN** imposta i margini per il disegno di testo in un controllo Button.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che specifica i margini da utilizzare per il disegno del testo.

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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Pulsante \_ SetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Pulsanti](buttons.md)
</dt> </dl>

 

