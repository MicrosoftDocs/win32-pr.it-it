---
title: Messaggio TCM_SETCURSEL (COMmctrl. h)
description: Seleziona una scheda in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl.
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- Controlli di Windows Message TCM_SETCURSEL
topic_type:
- apiref
api_name:
- TCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90033c5a19b0eb7b73f9ed886e8dad8d1ca4c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964248"
---
# <a name="tcm_setcursel-message"></a>\_Messaggio di DEcursel TCM

Seleziona una scheda in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della scheda da selezionare.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice della scheda selezionata in precedenza, se ha esito positivo, oppure-1 in caso contrario.

## <a name="remarks"></a>Commenti

Un controllo struttura a schede non invia un codice di notifica [TCN \_ SELCHANGING](tcn-selchanging.md) o [TCN \_ selChange](tcn-selchange.md) quando viene selezionata una scheda utilizzando questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





