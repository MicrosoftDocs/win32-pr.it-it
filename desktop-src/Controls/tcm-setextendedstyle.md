---
title: TCM_SETEXTENDEDSTYLE messaggio (Commctrl.h)
description: Imposta gli stili estesi che verranno utilizzati dal controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TabCtrl SetExtendedStyle.
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- TCM_SETEXTENDEDSTYLE controlli Windows messaggio
topic_type:
- apiref
api_name:
- TCM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a4a28bcf4cffe9aa2559f96a990d23511ece9fbbfc65468f84a4a874dce678a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876451"
---
# <a name="tcm_setextendedstyle-message"></a>Messaggio TCM \_ SETEXTENDEDSTYLE

Imposta gli stili estesi che verranno utilizzati dal controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TabCtrl SetExtendedStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore **DWORD** che indica gli stili in *lParam* da modificare. Verranno modificati solo gli stili estesi in *wParam.* Tutti gli altri stili verranno mantenuti così come sono. Se questo parametro è zero, tutti gli stili in *lParam* saranno interessati.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore che specifica gli stili estesi del controllo Struttura a schede. Questo valore è una combinazione di stili estesi del [controllo Struttura a schede.](tab-control-extended-styles.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che contiene gli stili estesi del controllo Struttura a schede precedente.

## <a name="remarks"></a>Commenti

Il *parametro wParam* consente di modificare uno o più stili estesi senza dover prima recuperare gli stili esistenti. Ad esempio, se si passa [**TCS \_ EX \_ FLATSEPARATORS**](tab-control-extended-styles.md) per *wParam* e 0 per *lParam*, lo stile **TCS \_ EX \_ FLATSEPARATORS** verrà cancellato, ma tutti gli altri stili rimarranno invariati.

Per motivi di compatibilità con le versioni precedenti, la macro [**\_ TabCtrl SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) non è stata aggiornata per l'uso *di dwExMask*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md)
</dt> </dl>

 

 





