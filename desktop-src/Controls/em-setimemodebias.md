---
title: Messaggio di EM_SETIMEMODEBIAS (RichEdit. h)
description: Impostare la distorsione della modalità IME (Input Method Editor) per un controllo Rich Edit.
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- Controlli di Windows Message EM_SETIMEMODEBIAS
topic_type:
- apiref
api_name:
- EM_SETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48fbd93971a57cffa3441c2a3db0816572f761d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477320"
---
# <a name="em_setimemodebias-message"></a>\_Messaggio SETIMEMODEBIAS em

Impostare la distorsione della modalità IME (Input Method Editor) per un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore di distorsione della modalità IME. Può essere uno dei seguenti.



| Valore                                                                                                                                                                                        | Significato                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <dt>**\_PLAURALCLAUSE SMODE \_ FMI**</dt> </dl> | Imposta la distorsione della modalità IME su Name.<br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <dt>**\_SMODE FMI \_**</dt> </dl>                            | Nessuna distorsione.<br/>                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Deve corrispondere al valore *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce la nuova impostazione di distorsione della modalità IME.

## <a name="remarks"></a>Commenti

Quando l'IME genera un elenco di scelte alternative per un set di caratteri, questo messaggio imposta i criteri in base ai quali verranno visualizzate alcune delle scelte nella parte superiore dell'elenco.

Per impostare la distorsione della modalità TSF (Text Services Framework), usare [**em \_ SETCTFMODEBIAS**](em-setctfmodebias.md).

Prima di chiamare questa funzione, l'applicazione deve chiamare [**em \_ ISIME**](em-isime.md) .

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

[**\_ISIME em**](em-isime.md)
</dt> <dt>

[**\_SETCTFMODEBIAS em**](em-setctfmodebias.md)
</dt> </dl>

 

 





