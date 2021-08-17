---
title: CB_SETEDITSEL messaggio (Winuser.h)
description: Un'applicazione invia un messaggio \_ CB SETEDITSEL per selezionare i caratteri nel controllo di modifica di una casella combinata.
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- CB_SETEDITSEL dei messaggi Windows
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
ms.openlocfilehash: 0e8deb133559332ea8f727758086e19cb17483b4c343f8b3f8f1a3694911eedd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832269"
---
# <a name="cb_seteditsel-message"></a>CB \_ SETEDITSEL message

Un'applicazione invia un **messaggio \_ CB SETEDITSEL** per selezionare i caratteri nel controllo di modifica di una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

LoWORD [**di**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) *lParam* specifica la posizione iniziale. Se **LOWORD è** -1, la selezione, se presente, viene rimossa.

La [**parola chiave HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) *di lParam* specifica la posizione finale. Se **HIWORD è** -1, viene selezionato tutto il testo dalla posizione iniziale all'ultimo carattere nel controllo di modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è **TRUE.** Se il messaggio viene inviato a una casella combinata con lo stile [**\_ DROPDOWNLIST di CBS,**](combo-box-styles.md) si tratta di CB \_ ERR.

## <a name="remarks"></a>Commenti

Le posizioni sono in base zero. Il primo carattere del controllo di modifica si trova nella posizione zero. Il primo carattere dopo l'ultimo carattere selezionato si trova nella posizione finale. Ad esempio, per selezionare i primi quattro caratteri del controllo di modifica, usare una posizione iniziale di 0 e una posizione finale di 4.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



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

 

