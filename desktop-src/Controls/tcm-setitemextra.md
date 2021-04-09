---
title: Messaggio TCM_SETITEMEXTRA (COMmctrl. h)
description: Imposta il numero di byte per tabulazione riservata ai dati definiti dall'applicazione in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl SetItemExtra.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- Controlli di Windows Message TCM_SETITEMEXTRA
topic_type:
- apiref
api_name:
- TCM_SETITEMEXTRA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6c7fdb47483ae0ddc841ae5f79b8f913e6a4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118962"
---
# <a name="tcm_setitemextra-message"></a>\_Messaggio TCM SETITEMEXTRA

Imposta il numero di byte per tabulazione riservata ai dati definiti dall'applicazione in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di byte aggiuntivi.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il numero di byte aggiuntivi è quattro. Un'applicazione che modifica il numero di byte aggiuntivi non può utilizzare la struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) per recuperare e impostare i dati definiti dall'applicazione per una scheda. È invece necessario definire una nuova struttura costituita dalla struttura [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) seguita da membri definiti dall'applicazione.

Un'applicazione deve modificare solo il numero di byte aggiuntivi quando un controllo struttura a schede non contiene alcuna tabulazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





