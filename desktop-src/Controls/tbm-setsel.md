---
title: Messaggio TBM_SETSEL (COMmctrl. h)
description: Imposta le posizioni iniziale e finale per l'intervallo di selezione disponibile in un TrackBar.
ms.assetid: 71f5b9f8-4850-44a8-8acf-adca9bda84c3
keywords:
- Controlli di Windows Message TBM_SETSEL
topic_type:
- apiref
api_name:
- TBM_SETSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edebc6b6dcf3b0b93e3047a39aac74c34d121bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739903"
---
# <a name="tbm_setsel-message"></a>\_Messaggio SETSEL TBM

Imposta le posizioni iniziale e finale per l'intervallo di selezione disponibile in un TrackBar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Ridisegni flag. Se questo parametro è **true**, il messaggio riestrae il TrackBar dopo l'impostazione dell'intervallo di selezione. Se questo parametro è **false**, il messaggio imposta l'intervallo di selezione senza ricreare il TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la posizione logica iniziale per l'intervallo di selezione e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la posizione logica finale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo messaggio viene ignorato se il TrackBar non ha lo stile [**\_ ENABLESELRANGE di TBS**](trackbar-control-styles.md) .

**TBM \_ SETSEL** consente di limitare il puntatore solo a una parte dell'intervallo disponibile per l'indicatore di stato.

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

[**TBM \_ GETselend**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ GETSELSTART**](tbm-getselstart.md)
</dt> <dt>

[**\_SEselend TBM**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

