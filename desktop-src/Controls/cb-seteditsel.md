---
title: Messaggio CB_SETEDITSEL (winuser. h)
description: Un'applicazione invia un \_ messaggio CB SETEDITSEL per selezionare i caratteri nel controllo di modifica di una casella combinata.
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- Controlli di Windows Message CB_SETEDITSEL
topic_type:
- apiref
api_name:
- CB_SETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54e09697e266b4e0c4260104e90f454a5e3edfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476631"
---
# <a name="cb_seteditsel-message"></a>\_Messaggio SETEDITSEL CB

Un'applicazione invia un messaggio **CB \_ SETEDITSEL** per selezionare i caratteri nel controllo di modifica di una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) di *lParam* specifica la posizione iniziale. Se **LOWORD** è-1, la selezione, se presente, viene rimossa.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) di *lParam* specifica la posizione finale. Se **HIWORD** è-1, viene selezionato tutto il testo della posizione iniziale fino all'ultimo carattere del controllo di modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è **true**. Se il messaggio viene inviato a una casella combinata con lo stile di [**\_ DropDownList CBS**](combo-box-styles.md) , è CB \_ Err.

## <a name="remarks"></a>Commenti

Le posizioni sono in base zero. Il primo carattere del controllo di modifica è nella posizione zero. Il primo carattere dopo l'ultimo carattere selezionato è nella posizione finale. Per selezionare, ad esempio, i primi quattro caratteri del controllo di modifica, utilizzare una posizione iniziale pari a 0 e una posizione finale pari a 4.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CB \_ GETEDITSEL**](cb-geteditsel.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

