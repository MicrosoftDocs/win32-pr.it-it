---
title: Messaggio TCM_SETCURFOCUS (COMmctrl. h)
description: Imposta lo stato attivo su una scheda specificata in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl SetCurFocus.
ms.assetid: bcbd5f26-b54e-492b-aff3-357b8ae23969
keywords:
- Controlli di Windows Message TCM_SETCURFOCUS
topic_type:
- apiref
api_name:
- TCM_SETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe566d1e1b3cc7d257c4756fe123423fc344a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964249"
---
# <a name="tcm_setcurfocus-message"></a>\_Messaggio TCM SETCURFOCUS

Imposta lo stato attivo su una scheda specificata in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della scheda che ottiene lo stato attivo.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se il controllo struttura a schede ha lo stile dei [**\_ pulsanti TCS**](tab-control-styles.md) (modalità pulsante), la scheda con lo stato attivo potrebbe essere diversa dalla scheda selezionata. Ad esempio, quando si seleziona una scheda, l'utente può premere i tasti di direzione per impostare lo stato attivo su una scheda diversa senza modificare la scheda selezionata. In modalità pulsante, **TCM \_ SETCURFOCUS** imposta lo stato attivo per l'input sul pulsante associato alla scheda specificata, ma non modifica la scheda selezionata.

Se il controllo struttura a schede non ha lo stile dei [**\_ pulsanti TCS**](tab-control-styles.md) , la modifica dello stato attivo cambia anche la scheda selezionata. In questo caso, il controllo struttura a schede invia i codici di notifica [TCN \_ SELCHANGING](tcn-selchanging.md) e [TCN \_ selChange](tcn-selchange.md) alla relativa finestra padre.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TCM \_ GETCURFOCUS**](tcm-getcurfocus.md)
</dt> </dl>

 

 





