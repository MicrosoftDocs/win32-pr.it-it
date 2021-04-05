---
title: Messaggio di EM_GETPUNCTUATION (RichEdit. h)
description: Ottiene i caratteri di punteggiatura correnti per il controllo Rich Edit.
ms.assetid: 1c04967b-d75e-4f54-b35b-cd50bac9cdfa
keywords:
- Controlli di Windows Message EM_GETPUNCTUATION
topic_type:
- apiref
api_name:
- EM_GETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158c26deca3328d9cdbed7ffe7cf885b0582d1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120850"
---
# <a name="em_getpunctuation-message"></a>\_Messaggio GETpunteggiation em

Ottiene i caratteri di punteggiatura correnti per il controllo Rich Edit.

> [!Note]  
> Questo messaggio è supportato solo nelle versioni in lingua asiatica di Microsoft Rich Edit 1,0. Non è supportata nelle versioni successive di Rich Edit.

 

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Il tipo di punteggiatura può essere uno dei valori seguenti.



| Valore                                                                                                                                                      | Significato                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**COMPUTER \_ leader**</dt> </dl>       | Caratteri di punteggiatura iniziali<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**PC che \_ segue**</dt> </dl> | Caratteri di punteggiatura seguenti<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**\_DElimitatore PC**</dt> </dl> | Delimitatore<br/>                        |
| <span id="PC_OVERFLOW"></span><span id="pc_overflow"></span><dl> <dt>**OVERFLOW del PC \_**</dt> </dl>    | Non supportato<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**punteggiatura**](/windows/desktop/api/Richedit/ns-richedit-punctuation) che riceve i caratteri di punteggiatura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.

Se l'operazione ha esito negativo, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_punteggiatura em**](em-setpunctuation.md)
</dt> <dt>

[**PUNTEGGIATURA**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





