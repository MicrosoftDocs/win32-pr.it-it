---
title: Messaggio EM_GETENDOFLINE (COMmctrl. h)
description: Recupera il carattere di fine riga utilizzato quando viene inserito un LineBreak. Inviare questo messaggio in modo esplicito o usando la \_ macro Edit GetEndOfLine.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Controlli di Windows Message EM_GETENDOFLINE
topic_type:
- apiref
api_name:
- EM_GETENDOFLINE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 98d537d2ea4239ab3f511666aeba46be93a2b881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475574"
---
# <a name="em_getendofline-message"></a>\_Messaggio GETENDOFLINE em

Recupera il carattere di fine riga per un controllo di modifica. Inviare questo messaggio in modo esplicito o usando la macro [**Edit \_ GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il carattere di fine riga utilizzato dal controllo di modifica. Può corrispondere a uno dei valori seguenti.

| Valore                                                                                                                                                   | Significato                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**EC \_ ENDOFLINE \_ CRLF**</dt> </dl> | Il carattere di fine riga utilizzato per il nuovo interruzioni è il ritorno a capo seguito da avanzamento riga (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ENDOFLINE \_ CR**</dt> </dl>       | Il carattere di fine riga utilizzato per il nuovo interruzioni è il ritorno a capo (CR).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ENDOFLINE \_ LF**</dt> </dl>       | Il carattere di fine riga utilizzato per il nuovo interruzioni è avanzamento riga (LF).<br/>                               |

## <a name="remarks"></a>Commenti

Quando il carattere di fine riga utilizzato viene impostato su **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** mediante [**Edit \_ SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), questo messaggio restituisce il carattere di fine riga rilevato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1809 \[\]<br/>                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2019\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETENDOFLINE em*](em-setendofline.md)
</dt> </dl>
 

 





