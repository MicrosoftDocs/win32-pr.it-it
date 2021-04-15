---
title: Messaggio di EM_SETCTFMODEBIAS (RichEdit. h)
description: Imposta la distorsione della modalità TSF (Text Services Framework) per un controllo Rich Edit.
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- Controlli di Windows Message EM_SETCTFMODEBIAS
topic_type:
- apiref
api_name:
- EM_SETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b872fa5489c898ec4482ecdc094de7df6e3180be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518675"
---
# <a name="em_setctfmodebias-message"></a>\_Messaggio SETCTFMODEBIAS em

Imposta la distorsione della modalità TSF (Text Services Framework) per un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore di distorsione della modalità. Può corrispondere a uno dei valori seguenti.



| Valore                                                                                                                                                                                                                     | Significato                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <dt>**\_impostazione predefinita CTFMODEBIAS**</dt> </dl>                                           | Non esiste alcuna distorsione in modalità.<br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <dt>**\_nome file CTFMODEBIAS**</dt> </dl>                                        | La distorsione è a un nome di file.<br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <dt>**\_nome CTFMODEBIAS**</dt> </dl>                                                    | La distorsione è un nome.<br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <dt>**lettura di CTFMODEBIAS \_**</dt> </dl>                                           | La distorsione è la lettura.<br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <dt>**CTFMODEBIAS \_ DateTime**</dt> </dl>                                        | La distorsione è a una data o un'ora.<br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <dt>**\_conversazione CTFMODEBIAS**</dt> </dl>                            | La distorsione è a una conversazione.<br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <dt>**CTFMODEBIAS \_ numerico**</dt> </dl>                                           | La distorsione è un numero.<br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <dt>**\_Hiragana CTFMODEBIAS**</dt> </dl>                                        | La distorsione è per le stringhe hiragana.<br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <dt>**\_katakana CTFMODEBIAS**</dt> </dl>                                        | La distorsione è per le stringhe katakana.<br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <dt>**CTFMODEBIAS \_ hangul**</dt> </dl>                                              | La distorsione è di caratteri Hangul.<br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <dt>**\_HALFWIDTHKATAKANA CTFMODEBIAS**</dt> </dl>             | La distorsione è per le stringhe katakana a metà larghezza.<br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <dt>**\_FULLWIDTHALPHANUMERIC CTFMODEBIAS**</dt> </dl> | La distorsione è a caratteri alfanumerici a larghezza intera.<br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <dt>**\_HALFWIDTHALPHANUMERIC CTFMODEBIAS**</dt> </dl> | La distorsione è costituita da caratteri alfanumerici a metà larghezza.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, il valore restituito è il nuovo valore di distorsione della modalità TSF. Se ha esito negativo, il valore restituito è il valore di distorsione della modalità TSF precedente.

## <a name="remarks"></a>Commenti

Quando un'applicazione Microsoft Rich Edit USA TSF, può selezionare la distorsione della modalità TSF. Questo messaggio imposta i criteri in base ai quali una scelta alternativa viene visualizzata nella parte superiore dell'elenco per la selezione.

Per impostare la distorsione della modalità per input Method Editor (IME), usare [**em \_ SETIMEMODEBIAS**](em-setimemodebias.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP1 \[\]<br/>                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_GETCTFMODEBIAS em**](em-getctfmodebias.md)
</dt> <dt>

[**\_SETIMEMODEBIAS em**](em-setimemodebias.md)
</dt> </dl>

 

 





