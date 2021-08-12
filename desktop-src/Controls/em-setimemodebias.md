---
title: EM_SETIMEMODEBIAS messaggio (Richedit.h)
description: Impostare la distorsione della modalità IME (Input Method Editor) per un controllo Rich Edit.
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- EM_SETIMEMODEBIAS di controllo Windows messaggio
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
ms.openlocfilehash: b4812c21558fba07be2709c0fd1a011f31d79fad17e0b4146fa0c7d65843a087
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672671"
---
# <a name="em_setimemodebias-message"></a>Messaggio EM \_ SETIMEMODEBIAS

Impostare la distorsione della modalità IME (Input Method Editor) per un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore di distorsione della modalità IME. Può essere uno dei seguenti.



| Valore                                                                                                                                                                                        | Significato                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <dt>**IMF \_ SMODE \_ PLAURALCLAUSE**</dt> </dl> | Imposta la distorsione della modalità IME su Nome.<br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <dt>**IMF \_ SMODE \_ NONE**</dt> </dl>                            | Nessuna distorsione.<br/>                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere lo stesso valore di *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce la nuova impostazione di distorsione della modalità IME.

## <a name="remarks"></a>Commenti

Quando l'IME genera un elenco di scelte alternative per un set di caratteri, questo messaggio imposta i criteri in base ai quali alcune scelte verranno visualizzate all'inizio dell'elenco.

Per impostare la distorsione Framework servizi di testo (TSF), usare [**EM \_ SETCTFMODEBIAS.**](em-setctfmodebias.md)

L'applicazione deve [**chiamare \_ l'ISIME EM**](em-isime.md) prima di chiamare questa funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con \[ app desktop SP1\]<br/>                                  |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

[**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md)
</dt> </dl>

 

 





