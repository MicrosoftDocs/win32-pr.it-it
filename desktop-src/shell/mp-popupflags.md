---
description: Rappresenta le opzioni disponibili quando si visualizza un menu a comparsa.
title: MP_POPUPFLAGS costanti (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cc1d9ff0-a03b-4bd3-b481-9b78d20eb771
api_name:
- MPPF_SETFOCUS
- MPPF_INITIALSELECT
- MPPF_NOANIMATE
- MPPF_KEYBOARD
- MPPF_REPOSITION
- MPPF_FORCEZORDER
- MPPF_FINALSELECT
- MPPF_ALIGN_LEFT
- MPPF_ALIGN_RIGHT
- MPPF_TOP
- MPPF_LEFT
- MPPF_RIGHT
- MPPF_BOTTOM
- MPPF_POS_MASK
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a1f6211769eca021f76fcbef34625f705cd3bf3fed02ca548d2965f17de80af7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710011"
---
# <a name="mp_popupflags-constants"></a>Costanti \_ MP POPUPFLAGS

Rappresenta le opzioni disponibili quando si visualizza un menu a comparsa.



| Costante/valore                                                                                                                                                                                                                               | Descrizione                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <dt>**MPPF \_ SetFOCUS**</dt> <dt>0x00000001</dt> </dl>                | Assegnare lo stato attivo al menu a comparsa.<br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <dt>**MPPF \_ INITIALSELECT**</dt> <dt>0x00000002</dt> </dl> | Selezionare la prima voce nel menu a comparsa.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <dt>**MPPF \_ NoANIMATE**</dt> <dt>0x00000004</dt> </dl>             | Non usare le animazioni di sistema predefinite, ad esempio la dissolvenza in entrata, quando si visualizza il menu.<br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <dt>**MPPF \_ Tasti di**</dt> <dt>scelta 0x00000010</dt> </dl>                | Attivare il menu tramite un tasto di scelta rapida.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <dt>**MPPF \_ RIPOSIZIONA**</dt> <dt>0x00000020</dt> </dl>          | Visualizzare la barra in una posizione diversa, in base alle modifiche apportate al menu.<br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <dt>**MPPF \_ FORCEZORDER**</dt> <dt>0x00000040</dt> </dl>       | Riservato. Non usare.<br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <dt>**MPPF \_ FINALSELECT**</dt> <dt>0x00000080</dt> </dl>       | Selezionare l'ultima voce nel menu.<br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <dt>**MPPF \_ ALLINEA \_ A SINISTRA**</dt> <dt>0x02000000</dt> </dl>         | **Windows Vista** o versioni successive: allineare il menu a comparsa a sinistra dell'area specificata nel parametro *prcExclude* di [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) o [**IMenuPopup::P opup.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup) Questo è l'allineamento predefinito.<br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <dt>**MPPF \_ ALLINEA \_ A**</dt> <dt>DESTRA 0x04000000</dt> </dl>      | **Windows Vista** o versioni successive: allineare il menu a comparsa a destra dell'area specificata nel parametro *prcExclude* di [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) o [**IMenuPopup::P opup.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)<br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <dt>**MPPF \_ Top**</dt> <dt>0x20000000</dt> </dl>                               | Posizionare il menu a comparsa sopra il punto iniziale specificato nel parametro *ppt* di [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) o [**IMenuPopup::P opup.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)<br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <dt>**MPPF \_ Sinistra**</dt> <dt>0x40000000</dt> </dl>                            | Posizionare il menu a comparsa a sinistra del punto iniziale.<br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <dt>**MPPF \_ Right**</dt> <dt>0x60000000</dt> </dl>                         | Posizionare il menu a comparsa a destra del punto iniziale.<br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <dt>**MPPF \_ BOTTOM**</dt> <dt>(int)0x80000000</dt> </dl>                 | Posizionare il menu a comparsa sotto il punto iniziale.<br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <dt>**MPPF \_ POS \_ MASK**</dt> <dt>(int)0xE0000000</dt> </dl>          | Maschera della posizione del menu.<br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a>Commenti

Queste costanti sono definite nel file Shobjidl.h a partire da Windows XP Service Pack 1 (SP1) e Windows Server 2003

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con \[ app desktop SP1\]<br/>                                    |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 




