---
title: EM_SETENDOFLINE messaggio (CommCtrl.h)
description: Imposta il carattere di fine riga utilizzato quando viene inserita un'interruzione di riga.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETENDOFLINE dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- EM_SETENDOFLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 5990b247757fc8e3cd39ab38edf5b88ca8ac62f74e402aac3899d51e3156231f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437591"
---
# <a name="em_setendofline-message"></a>Messaggio EM \_ SETENDOFLINE

Imposta il carattere di fine riga utilizzato quando viene inserita un'interruzione di riga.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il carattere di fine riga utilizzato quando viene inserita un'interruzione di riga. Può essere uno dei valori seguenti.


| Valore                                                                                                                                                   | Significato                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <dt>**EC \_ ENDOFLINE \_ DETECTFROMCONTENT**</dt> </dl> | Imposta il carattere di fine riga utilizzato per le nuove interruzioni di riga sul carattere usato dal documento corrente.<br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**EC \_ ENDOFLINE \_ CRLF**</dt> </dl>                                        | Imposta il carattere di fine riga utilizzato per le nuove interruzioni di riga sul ritorno a capo seguito da avanzamento riga (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ENDOFLINE \_ CR**</dt> </dl>                                              | Imposta il carattere di fine riga utilizzato per le nuove interruzioni di riga sul ritorno a capo (CR).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ENDOFLINE \_ LF**</dt> </dl>                                              | Imposta il carattere di fine riga utilizzato per le nuove interruzioni di riga su avanzamento riga (LF).<br/>                               |

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è diverso da zero.

Se l'operazione non riesce, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Quando il set di caratteri di fine riga è **EC \_ ENDOFLINE \_ DETECTFROMCONTENT,** il controllo di modifica rileverà solo i caratteri di fine riga supportati in base allo stile della finestra estesa, vedere Modifica [degli](edit-control-window-extended-styles.md)stili estesi del controllo .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop 1809 \[\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2019 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETENDOFLINE*](em-getendofline.md)
</dt> </dl>

 

 





