---
title: EM_SETCTFMODEBIAS messaggio (Richedit.h)
description: Imposta la distorsione Framework servizi di testo modalità avanzata (TSF) per un controllo Rich Edit.
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- EM_SETCTFMODEBIAS di controllo Windows messaggio
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
ms.openlocfilehash: fd6aa0f10b07092d9637d9e5a993848671ab6aa7e7eb610eca48c3df353c4a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019509"
---
# <a name="em_setctfmodebias-message"></a>Messaggio EM \_ SETCTFMODEBIAS

Imposta la distorsione Framework servizi di testo modalità avanzata (TSF) per un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore di distorsione della modalità. Può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                     | Significato                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <dt>**CTFMODEBIAS \_ PREDEFINITO**</dt> </dl>                                           | Non è presente alcuna distorsione della modalità.<br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <dt>**NOME FILE CTFMODEBIAS \_**</dt> </dl>                                        | La distorsione è per un nome file.<br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <dt>**NOME CTFMODEBIAS \_**</dt> </dl>                                                    | La distorsione è per un nome.<br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <dt>**CTFMODEBIAS \_ READING**</dt> </dl>                                           | La distorsione è per la lettura.<br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <dt>**CTFMODEBIAS \_ DATETIME**</dt> </dl>                                        | La distorsione è a una data o a un'ora.<br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <dt>**CONVERSAZIONE DI CTFMODEBIAS \_**</dt> </dl>                            | La distorsione è per una conversazione.<br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <dt>**CTFMODEBIAS \_ NUMERIC**</dt> </dl>                                           | La distorsione è per un numero.<br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <dt>**CTFMODEBIAS \_ HIRAGANA**</dt> </dl>                                        | La distorsione è per le stringhe hiragana.<br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <dt>**CTFMODEBIAS \_ KATAKANA**</dt> </dl>                                        | La differenza è per le stringhe katakana.<br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <dt>**CTFMODEBIAS \_ HANGUL**</dt> </dl>                                              | La differenza è per i caratteri Hangul.<br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <dt>**CTFMODEBIAS \_ HALFWIDTHKATAKANA**</dt> </dl>             | La distorsione è alle stringhe katakana a metà larghezza.<br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <dt>**CTFMODEBIAS \_ FULLWIDTHALPHANUMERIC**</dt> </dl> | La distorsione è ai caratteri alfanumerici a larghezza intera.<br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <dt>**CTFMODEBIAS \_ HALFWIDTHALPHANUMERIC**</dt> </dl> | La distorsione è ai caratteri alfanumerici a metà larghezza.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, il valore restituito è il nuovo valore di distorsione della modalità TSF. Se ha esito negativo, il valore restituito è il valore di distorsione della modalità TSF precedente.

## <a name="remarks"></a>Commenti

Quando un'applicazione Microsoft Rich Edit usa TSF, può selezionare la distorsione della modalità TSF. Questo messaggio imposta i criteri in base ai quali viene visualizzata una scelta alternativa nella parte superiore dell'elenco per la selezione.

Per impostare la distorsione della modalità per Input Method Editor (IME), usare [**EM \_ SETIMEMODEBIAS**](em-setimemodebias.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP1 \[\]<br/>                                  |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ GETCTFMODEBIAS**](em-getctfmodebias.md)
</dt> <dt>

[**EM \_ SETIMEMODEBIAS**](em-setimemodebias.md)
</dt> </dl>

 

 





