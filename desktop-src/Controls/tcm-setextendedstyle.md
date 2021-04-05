---
title: Messaggio TCM_SETEXTENDEDSTYLE (COMmctrl. h)
description: Imposta gli stili estesi che il controllo struttura a schede utilizzerà. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl SetExtendedStyle.
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- Controlli di Windows Message TCM_SETEXTENDEDSTYLE
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
ms.openlocfilehash: f4c789b45eaae6cb3b1bc4fed6f216ec5010b463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048386"
---
# <a name="tcm_setextendedstyle-message"></a>\_Messaggio TCM SETEXTENDEDSTYLE

Imposta gli stili estesi che il controllo struttura a schede utilizzerà. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore **DWORD** che indica quali stili in *lParam* devono essere interessati. Solo gli stili estesi in *wParam* verranno modificati. Tutti gli altri stili verranno mantenuti così come sono. Se questo parametro è zero, saranno interessati tutti gli stili in *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Valore che specifica gli stili del controllo scheda esteso. Questo valore è una combinazione di [stili estesi](tab-control-extended-styles.md)del controllo scheda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **DWORD** che contiene gli stili estesi del controllo tab precedente.

## <a name="remarks"></a>Commenti

Il parametro *wParam* consente di modificare uno o più stili estesi senza dover prima recuperare gli stili esistenti. Se, ad esempio, si [**passa TCS \_ ex \_ FLATSEPARATORS**](tab-control-extended-styles.md) per *wParam* e 0 per *lParam*, lo stile **\_ \_ FLATSEPARATORS di TC ex** verrà cancellato, ma tutti gli altri stili rimarranno invariati.

Per motivi di compatibilità con le versioni precedenti, la macro [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) non è stata aggiornata per l'uso di *dwExMask*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md)
</dt> </dl>

 

 





