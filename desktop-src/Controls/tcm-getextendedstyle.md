---
title: Messaggio TCM_GETEXTENDEDSTYLE (COMmctrl. h)
description: Recupera gli stili estesi attualmente in uso per il controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl GetExtendedStyle.
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- Controlli di Windows Message TCM_GETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- TCM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8280b7043591dd4fdd0b453c5baea5fe014bd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964791"
---
# <a name="tcm_getextendedstyle-message"></a>\_Messaggio TCM GETEXTENDEDSTYLE

Recupera gli stili estesi attualmente in uso per il controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **DWORD** che rappresenta gli stili estesi attualmente in uso per il controllo struttura a schede. Questo valore è una combinazione di [stili estesi](tab-control-extended-styles.md)del controllo scheda.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TCM \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md)
</dt> </dl>

 

 





