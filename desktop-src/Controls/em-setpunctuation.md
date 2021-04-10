---
title: Messaggio di EM_SETPUNCTUATION (RichEdit. h)
description: Imposta i caratteri di punteggiatura per un controllo Rich Edit.
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- Controlli di Windows Message EM_SETPUNCTUATION
topic_type:
- apiref
api_name:
- EM_SETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710392cee7f7a1fb04fce59d6549134255499172
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121030"
---
# <a name="em_setpunctuation-message"></a>\_Messaggio di DEpunteggiatura em

Imposta i caratteri di punteggiatura per un controllo Rich Edit.

> [!Note]  
> Questo messaggio è supportato solo nelle versioni in lingua asiatica di Microsoft Rich Edit 1,0. Non è supportata nelle versioni successive.

 

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il tipo di punteggiatura. i possibili valori sono i seguenti.



| Valore                                                                                                                                                      | Significato                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**COMPUTER \_ leader**</dt> </dl>       | Caratteri di punteggiatura iniziali.<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**PC che \_ segue**</dt> </dl> | Caratteri di punteggiatura seguenti.<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**\_DElimitatore PC**</dt> </dl> | Delimitatore.<br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <dt>**Computer \_ OVERFLOW**</dt> </dl> | Non supportata.<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**punteggiatura**](/windows/desktop/api/Richedit/ns-richedit-punctuation) che contiene i caratteri di punteggiatura.

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

[**\_GETpunteggiatura em**](em-getpunctuation.md)
</dt> <dt>

[**PUNTEGGIATURA**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





