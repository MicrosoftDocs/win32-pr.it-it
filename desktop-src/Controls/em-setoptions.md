---
title: EM_SETOPTIONS messaggio (Richedit.h)
description: Imposta le opzioni per un controllo Rich Edit.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- EM_SETOPTIONS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5d5c4b7fd9e92261cedaf0681523ad0a3e25a37aa2814f6c00d0d9460e94bb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672610"
---
# <a name="em_setoptions-message"></a>Messaggio \_ EM SETOPTIONS

Imposta le opzioni per un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'operazione, che può essere uno di questi valori.



| Valore                                                                                                                                             | Significato                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**ECOOP \_ SET**</dt> </dl> | Imposta le opzioni su quelle specificate da *lParam*.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ OR**</dt> </dl>    | Combina le opzioni specificate con le opzioni correnti.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ AND**</dt> </dl> | Mantiene solo le opzioni correnti specificate anche da *lParam*.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ECOOP \_ XOR**</dt> </dl> | OR esclusivo logicamente le opzioni correnti con quelle specificate da *lParam*.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica uno o più dei valori seguenti.



| Valore                                                                                                                                                                                 | Significato                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <dt>**ECO \_ AUTOWORDSELECTION**</dt> </dl> | Selezione automatica della parola al doppio clic.<br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <dt>**ECO \_ AUTOVSCROLL**</dt> </dl>                   | Uguale allo [**stile ES \_ AUTOVSCROLL.**](rich-edit-control-styles.md)<br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <dt>**ECO \_ AUTOHSCROLL**</dt> </dl>                   | Uguale allo [**stile ES \_ AUTOHSCROLL.**](rich-edit-control-styles.md)<br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <dt>**ECO \_ NOHIDESEL**</dt> </dl>                         | Uguale allo [**stile ES \_ NOHIDESEL.**](rich-edit-control-styles.md)<br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <dt>**ECO \_ READONLY**</dt> </dl>                            | Uguale allo [**stile ES \_ READONLY.**](rich-edit-control-styles.md)<br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <dt>**ECO \_ WANTRETURN**</dt> </dl>                      | Uguale allo [**stile ES \_ WANTRETURN.**](rich-edit-control-styles.md)<br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <dt>**ECO \_ SELECTIONBAR**</dt> </dl>                | Uguale allo [**stile ES \_ SELECTIONBAR.**](rich-edit-control-styles.md)<br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <dt>**ECO \_ VERTICAL**</dt> </dl>                            | Uguale allo [**stile ES \_ VERTICAL.**](rich-edit-control-styles.md) Disponibile solo nelle versioni in lingua asiatica.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce le opzioni correnti del controllo di modifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Stili del controllo Rich Edit**](rich-edit-control-styles.md)
</dt> </dl>

 

 





