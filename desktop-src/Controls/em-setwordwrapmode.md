---
title: Messaggio di EM_SETWORDWRAPMODE (RichEdit. h)
description: Imposta le opzioni di ritorno a capo automatico e di suddivisione in parole per un controllo Rich Edit.
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- Controlli di Windows Message EM_SETWORDWRAPMODE
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
ms.openlocfilehash: cf1dc6f064f52bf2a5f58c71db099f38b9350e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048477"
---
# <a name="em_setwordwrapmode-message"></a>\_Messaggio SETWORDWRAPMODE em

Imposta le opzioni di ritorno a capo automatico e di suddivisione in parole per un controllo Rich Edit.

> [!Note]  
> Questo messaggio è supportato solo nelle versioni in lingua asiatica di Microsoft Rich Edit 1,0. Non è supportata nelle versioni successive.

 

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica uno o più dei valori seguenti.



| Valore                                                                                                                                                         | Significato                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <dt>**\_WORDWRAP WBF**</dt> </dl>    | Abilita le operazioni a capo automatico specifiche per le lingue asiatiche, ad esempio Kinsoku in giapponese. <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <dt>**\_WordBreak WBF**</dt> </dl> | Abilita le operazioni di suddivisione in parole inglesi in giapponese e cinese. Abilita l'operazione di suddivisione in parole Hangeul.<br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <dt>**\_overflow WBF**</dt> </dl>    | Riconosce la punteggiatura dell'overflow. (Attualmente non supportata).<br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <dt>**\_Level1 WBF**</dt> </dl>          | Imposta come predefinita la tabella di punteggiatura di livello 1.<br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <dt>**\_Level2 WBF**</dt> </dl>          | Imposta la tabella di punteggiatura di livello 2 come valore predefinito.<br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <dt>**WBF \_ personalizzato**</dt> </dl>          | Imposta la tabella di punteggiatura definita dall'applicazione.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce le opzioni di ritorno a capo e di suddivisione in parole correnti.

## <a name="remarks"></a>Commenti

Questo messaggio non deve essere inviato dalla procedura di suddivisione delle parole definita dall'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





