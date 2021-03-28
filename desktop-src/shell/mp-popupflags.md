---
description: Rappresenta le opzioni disponibili quando si visualizza un menu di scelta rapida.
title: Costanti MP_POPUPFLAGS (ShObjIdl. h)
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
ms.openlocfilehash: 5d49f848df7749a732e9f0b849d44a9be56a5c3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130083"
---
# <a name="mp_popupflags-constants"></a>\_Costanti POPUPFLAGS MP

Rappresenta le opzioni disponibili quando si visualizza un menu di scelta rapida.



| Costante/valore                                                                                                                                                                                                                               | Descrizione                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <dt>**MPPF \_ SetFocus**</dt> <dt>0x00000001</dt> </dl>                | Assegnare al menu di scelta rapida lo stato attivo.<br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <dt>**MPPF \_**</dt> <dt>0x00000002</dt> INITIALSELECT </dl> | Selezionare il primo elemento nel menu a comparsa.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <dt>**MPPF \_ Noanimate**</dt> <dt>0x00000004</dt> </dl>             | Non usare le animazioni di sistema predefinite, ad esempio la dissolvenza, quando si Visualizza il menu.<br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <dt>**MPPF \_**</dt> <dt>0x00000010</dt> tastiera </dl>                | Attivare il menu tramite un tasto di scelta rapida.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <dt>**MPPF \_ Riposizionare**</dt> <dt>0x00000020</dt> </dl>          | Consente di visualizzare la barra in una posizione diversa, in base alle modifiche apportate al menu.<br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <dt>**MPPF \_**</dt> <dt>0x00000040</dt> FORCEZORDER </dl>       | Riservato. Non usare.<br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <dt>**MPPF \_**</dt> <dt>0x00000080</dt> FINALSELECT </dl>       | Selezionare l'ultimo elemento nel menu.<br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <dt>**MPPF \_ Allinea \_**</dt> <dt>0x02000000</dt> a sinistra </dl>         | **Windows Vista o versione successiva**: allineare il menu a comparsa a sinistra dell'area specificata nel parametro *prcExclude* di [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) o [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup). Si tratta dell'allineamento predefinito.<br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <dt>**MPPF \_ Allinea \_**</dt> <dt>0x04000000</dt> a destra </dl>      | **Windows Vista o versione successiva**: allineare il menu a comparsa a destra dell'area specificata nel parametro *prcExclude* di [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) o [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).<br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <dt>**MPPF \_ PRIMI**</dt> <dt>0x20000000</dt> </dl>                               | Posizionare il menu a comparsa sopra il punto iniziale specificato nel parametro *PPT* di [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) o [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).<br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <dt>**MPPF \_**</dt> <dt>0X40000000</dt> a sinistra </dl>                            | Posizionare il menu a comparsa a sinistra del punto iniziale.<br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <dt>**MPPF \_**</dt> <dt>0x60000000</dt> destro </dl>                         | Posizionare il menu a comparsa a destra del punto iniziale.<br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <dt>**MPPF \_ In basso**</dt> <dt>(int) 0x80000000</dt> </dl>                 | Posizionare il menu a comparsa sotto il punto iniziale.<br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <dt>**MPPF \_ POS \_ mask**</dt> <dt>(int) 0xE0000000</dt> </dl>          | Maschera della posizione dei menu.<br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a>Commenti

Queste costanti sono definite nel file ShObjIdl. h a partire da Windows XP Service Pack 1 (SP1) e Windows Server 2003

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP1 \[\]<br/>                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 




