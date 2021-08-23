---
title: EM_GETENDOFLINE messaggio (Commctrl.h)
description: Recupera il carattere di fine riga utilizzato quando viene inserita un'interruzione di riga. Inviare questo messaggio in modo esplicito o tramite la \_ macro Edit GetEndOfLine.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETENDOFLINE controlli Windows messaggio
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
ms.openlocfilehash: 64ddb55ce592b71c7abaa8c35b1bf14a004b324586094f27a3b418a67e5b24e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019689"
---
# <a name="em_getendofline-message"></a>Messaggio \_ EM GETENDOFLINE

Recupera il carattere di fine riga per un controllo di modifica. Inviare questo messaggio in modo esplicito o tramite la macro [**\_ Edit GetEndOfLine.**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il carattere di fine riga utilizzato dal controllo di modifica. Può essere uno dei valori seguenti.

| Valore                                                                                                                                                   | Significato                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**EC \_ ENDOFLINE \_ CRLF**</dt> </dl> | Il carattere di fine riga usato per le nuove interruzioni di riga è il ritorno a capo seguito da avanzamento riga (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ENDOFLINE \_ CR**</dt> </dl>       | Il carattere di fine riga usato per le nuove interruzioni di riga è il ritorno a capo (CR).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ENDOFLINE \_ LF**</dt> </dl>       | Il carattere di fine riga usato per le nuove interruzioni di riga è l'avanzamento riga (LF).<br/>                               |

## <a name="remarks"></a>Commenti

Quando il carattere di fine riga utilizzato è impostato su **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** usando [**Edit \_ SetEndOfLine,**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline)questo messaggio restituirà il carattere di fine riga rilevato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10, versione 1809 solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2019 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ SETENDOFLINE*](em-setendofline.md)
</dt> </dl>
 

 





