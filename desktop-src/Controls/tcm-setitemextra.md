---
title: TCM_SETITEMEXTRA messaggio (Commctrl.h)
description: Imposta il numero di byte per scheda riservato ai dati definiti dall'applicazione in un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TabCtrl SetItemExtra.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- TCM_SETITEMEXTRA di controllo Windows messaggio
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
ms.openlocfilehash: f92fb85f7133053392bee39119c91b55240f84f0a51c8acc7dc9c732b596526c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104761"
---
# <a name="tcm_setitemextra-message"></a>Messaggio \_ TCM SETITEMEXTRA

Imposta il numero di byte per scheda riservato ai dati definiti dall'applicazione in un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TabCtrl SetItemExtra.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di byte aggiuntivi.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il numero di byte aggiuntivi è quattro. Un'applicazione che modifica il numero di byte aggiuntivi non può usare la struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) per recuperare e impostare i dati definiti dall'applicazione per una scheda. È invece necessario definire una nuova struttura costituita dalla struttura [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) seguita dai membri definiti dall'applicazione.

Un'applicazione deve modificare il numero di byte aggiuntivi solo quando un controllo Struttura a schede non contiene schede.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





