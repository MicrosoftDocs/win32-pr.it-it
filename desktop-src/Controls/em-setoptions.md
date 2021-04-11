---
title: Messaggio di EM_SETOPTIONS (RichEdit. h)
description: Imposta le opzioni per un controllo Rich Edit.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- Controlli di Windows Message EM_SETOPTIONS
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
ms.openlocfilehash: 0c43dda8268b42dc264a86600826d2a6b550e35c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119598"
---
# <a name="em_setoptions-message"></a>\_Messaggio SEoptions em

Imposta le opzioni per un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'operazione. i possibili valori sono i seguenti.



| Valore                                                                                                                                             | Significato                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**SET di ECOOP \_**</dt> </dl> | Imposta le opzioni su quelle specificate da *lParam*.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ o**</dt> </dl>    | Combina le opzioni specificate con le opzioni correnti.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ e**</dt> </dl> | Mantiene solo le opzioni correnti specificate anche da *lParam*.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**\_Xor ECOOP**</dt> </dl> | Logicamente esclusivo o opzioni correnti con quelle specificate da *lParam*.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica uno o più dei valori seguenti.



| Valore                                                                                                                                                                                 | Significato                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <dt>**\_AUTOWORDSELECTION eco**</dt> </dl> | Selezione automatica di Word con doppio clic.<br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <dt>**\_AUTOVSCROLL eco**</dt> </dl>                   | Uguale allo stile [**es \_ AUTOVSCROLL**](rich-edit-control-styles.md) .<br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <dt>**\_AUTOHSCROLL eco**</dt> </dl>                   | Uguale allo stile [**es \_ AUTOHSCROLL**](rich-edit-control-styles.md) .<br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <dt>**\_NOHIDESEL eco**</dt> </dl>                         | Uguale allo stile [**es \_ NOHIDESEL**](rich-edit-control-styles.md) .<br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <dt>**ECO \_ ReadOnly**</dt> </dl>                            | Uguale allo stile di sola [**\_ lettura di es**](rich-edit-control-styles.md) .<br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <dt>**\_WANTRETURN eco**</dt> </dl>                      | Uguale allo stile [**es \_ WANTRETURN**](rich-edit-control-styles.md) .<br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <dt>**\_SELECTIONBAR eco**</dt> </dl>                | Uguale allo stile [**es \_ SELECTIONBAR**](rich-edit-control-styles.md) .<br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <dt>**ECO \_ verticale**</dt> </dl>                            | Uguale allo [**stile \_ verticale es**](rich-edit-control-styles.md) . Disponibile solo nelle versioni in lingua asiatica.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce le opzioni correnti del controllo di modifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Stili del controllo Rich Edit**](rich-edit-control-styles.md)
</dt> </dl>

 

 





