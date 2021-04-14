---
title: Messaggio EM_SETENDOFLINE (CommCtrl. h)
description: Imposta il carattere di fine riga utilizzato quando viene inserito un LineBreak.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- Controlli di Windows Message EM_SETENDOFLINE
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
ms.openlocfilehash: 5ee7c500ba3818cad0f5ee74e9994ed8af049ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478569"
---
# <a name="em_setendofline-message"></a>\_Messaggio SETENDOFLINE em

Imposta il carattere di fine riga utilizzato quando viene inserito un LineBreak.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il carattere di fine riga utilizzato quando viene inserito un LineBreak. Può corrispondere a uno dei valori seguenti.


| Valore                                                                                                                                                   | Significato                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <dt>**EC \_ ENDOFLINE \_ DETECTFROMCONTENT**</dt> </dl> | Imposta il carattere di fine riga utilizzato per il nuovo interruzioni sul carattere utilizzato dal documento corrente.<br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**EC \_ ENDOFLINE \_ CRLF**</dt> </dl>                                        | Imposta il carattere di fine riga utilizzato per il nuovo interruzioni per il ritorno a capo seguito da avanzamento riga (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**EC \_ ENDOFLINE \_ CR**</dt> </dl>                                              | Imposta il carattere di fine riga utilizzato per il nuovo interruzioni per il ritorno a capo (CR).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ENDOFLINE \_ LF**</dt> </dl>                                              | Imposta il carattere di fine riga utilizzato per il nuovo interruzioni di avanzamento riga (LF).<br/>                               |

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è diverso da zero.

Se l'operazione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Quando il set di caratteri di fine riga è **EC \_ ENDOFLINE \_ DETECTFROMCONTENT**, il controllo di modifica rileverà solo i caratteri di fine riga supportati in base allo stile della finestra estesa, vedere Modificare gli [stili estesi del controllo](edit-control-window-extended-styles.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10, 1809 \[\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2019\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETENDOFLINE em*](em-getendofline.md)
</dt> </dl>

 

 





