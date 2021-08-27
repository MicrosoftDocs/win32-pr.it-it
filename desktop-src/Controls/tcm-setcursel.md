---
title: TCM_SETCURSEL messaggio (Commctrl.h)
description: Seleziona una scheda in un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TabCtrl SetCurSel.
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- TCM_SETCURSEL di controllo Windows messaggio
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
ms.openlocfilehash: 5bdfd0861f5249a823d9406b437fd0efbca64a757a4bcadd7991155a87ddbc59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104851"
---
# <a name="tcm_setcursel-message"></a>Messaggio \_ SETCURSEL TCM

Seleziona una scheda in un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TabCtrl SetCurSel.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della scheda da selezionare.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice della scheda selezionata in precedenza in caso di esito positivo oppure -1 in caso contrario.

## <a name="remarks"></a>Commenti

Un controllo Struttura a schede non invia un codice di notifica [TCN \_ SELCHANGING](tcn-selchanging.md) o [TCN \_ SELCHANGE](tcn-selchange.md) quando si seleziona una scheda usando questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





