---
title: EM_SETWORDWRAPMODE messaggio (Richedit.h)
description: Imposta le opzioni di ritorno a capo automatico e di interruzione delle parole per un controllo Rich Edit.
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- EM_SETWORDWRAPMODE del messaggio Windows controlli
topic_type:
- apiref
api_name:
- EM_SETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b5c750bb83f4f3fb0c1acfc82b67677c36094df461d10787186177fc891df2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047981"
---
# <a name="em_setwordwrapmode-message"></a>Messaggio \_ EM SETWORDWRAPMODE

Imposta le opzioni di ritorno a capo automatico e di interruzione delle parole per un controllo Rich Edit.

> [!Note]  
> Questo messaggio è supportato solo nelle versioni in lingua Asia di Microsoft Rich Edit 1.0. Non è supportato nelle versioni successive.

 

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica uno o più dei valori seguenti.



| Valore                                                                                                                                                         | Significato                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <dt>**WBF \_ WORDWRAP**</dt> </dl>    | Abilita operazioni di ritorno a capo automatico specifiche dell'Asia, ad esempio kinsoku in giapponese. <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <dt>**WBF \_ WORDBREAK**</dt> </dl> | Abilita le operazioni di word breaking in inglese in giapponese e cinese. Abilita l'operazione di word breaking Hangeul.<br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <dt>**WBF \_ OVERFLOW**</dt> </dl>    | Riconosce la punteggiatura di overflow. Attualmente non è supportato.<br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <dt>**WBF \_ LEVEL1**</dt> </dl>          | Imposta la tabella di punteggiatura di livello 1 come predefinita.<br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <dt>**WBF \_ LEVEL2**</dt> </dl>          | Imposta la tabella di punteggiatura di livello 2 come predefinita.<br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <dt>**WBF \_ CUSTOM**</dt> </dl>          | Imposta la tabella di punteggiatura definita dall'applicazione.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce le opzioni correnti per il ritorno a capo automatico e il word breaking.

## <a name="remarks"></a>Commenti

Questo messaggio non deve essere inviato dalla procedura di word breaking definita dall'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





