---
title: TF_LBI_STYLE_ costanti (Ctfutb.h)
description: Le costanti STYLE \ TF LBI vengono usate nel membro dwStyle della struttura \_ \_ \_ LANGBARITEMINFO di TF per specificare lo stile di un elemento della \_ barra della lingua.
ms.assetid: 9180a666-774f-401b-bea3-68d5396fab30
topic_type:
- apiref
api_name:
- TF_LBI_STYLE_HIDDENSTATUSCONTROL
- TF_LBI_STYLE_SHOWNINTRAY
- TF_LBI_STYLE_HIDEONNOOTHERITEMS
- TF_LBI_STYLE_SHOWNINTRAYONLY
- TF_LBI_STYLE_HIDDENBYDEFAULT
- TF_LBI_STYLE_TEXTCOLORICON
- TF_LBI_STYLE_BTN_BUTTON
- TF_LBI_STYLE_BTN_MENU
- TF_LBI_STYLE_BTN_TOGGLE
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9954c416d9ad28f0ba0b2ddd6853b125039bf4db24adb3b3ff41f8722b2ba494
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950796"
---
# <a name="tf_lbi_style_-constants"></a>Costanti STYLE di TF \_ LBI \_ \_ \*

Le costanti STYLE di TF LBI vengono usate nel membro **\_ \_ \_ \* *_* dwStyle** della struttura [ \_ LANGBARITEMINFO di TF](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo) per specificare lo stile di un elemento della barra della lingua.

Se questo stile viene combinato con TF \_ LBI \_ STYLE \_ BTN BUTTON, verrà visualizzata una freccia a discesa per l'elemento \_ oltre al testo. La freccia a discesa funziona come pulsante di menu e facendo clic su di esso verrà chiamato **ITfLangBarItemButton::InitMenu.** Facendo clic sulla parte di testo del pulsante verrà chiamato **ITfLangBarItemButton::OnClick.**



| Costante/valore                                                                                                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STYLE_HIDDENSTATUSCONTROL"></span><span id="tf_lbi_style_hiddenstatuscontrol"></span><dl> <dt>**TF \_ STILE LBI \_ \_ HIDDENSTATUSCONTROL**</dt> <dt>0x00000001</dt> </dl> | L'elemento può essere nascosto o visualizzato dinamicamente usando il valore TF \_ LBI \_ STATUS HIDDEN nel \_ metodo [ITfLangBarItem::GetStatus.](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) Se questo valore non è presente, l'elemento non può essere nascosto in questo modo.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_SHOWNINTRAY"></span><span id="tf_lbi_style_shownintray"></span><dl> <dt>**TF \_ STILE LBI \_ \_ SHOWNINTRAY**</dt> <dt>0x00000002</dt> </dl>                         | L'elemento verrà visualizzato nella barra delle icone di notifica oltre alla barra della lingua. Questo flag non è attualmente supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="TF_LBI_STYLE_HIDEONNOOTHERITEMS"></span><span id="tf_lbi_style_hideonnootheritems"></span><dl> <dt>**TF \_ LBI \_ STYLE \_ HIDEONNOOTHERITEMS**</dt> <dt>0x00000004</dt> </dl>    | La barra della lingua è nascosta se tutti gli elementi nella barra della lingua contengono questo stile. Se un elemento della barra della lingua non contiene questo stile, viene visualizzata la barra della lingua.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="TF_LBI_STYLE_SHOWNINTRAYONLY"></span><span id="tf_lbi_style_shownintrayonly"></span><dl> <dt>**TF \_ STILE LBI \_ \_ SHOWNINTRAYONLY**</dt> <dt>0x00000008</dt> </dl>             | L'elemento verrà visualizzato solo nella barra delle icone di notifica e non nella barra della lingua. Questo flag non è attualmente supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_HIDDENBYDEFAULT"></span><span id="tf_lbi_style_hiddenbydefault"></span><dl> <dt>**TF \_ STILE LBI \_ \_ HIDDENBYDEFAULT**</dt> <dt>0x00000010</dt> </dl>             | L'elemento non viene visualizzato nella barra degli strumenti finché non viene selezionato dal menu delle opzioni della barra della lingua. Questo flag viene ignorato se l'opzione TF LBI STYLE HIDDENSTATUSCONTROL è impostata o se l'utente ha già modificato lo stato nascosto/visualizzato usando il menu delle opzioni della \_ \_ barra della \_ lingua.<br/>                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_TEXTCOLORICON"></span><span id="tf_lbi_style_textcoloricon"></span><dl> <dt>**TF \_ STILE LBI \_ \_ TEXTCOLORICON**</dt> <dt>0x00000020</dt> </dl>                   | Qualsiasi pixel nero all'interno dell'icona verrà convertito nel colore del testo del tema selezionato. L'icona deve essere monocromatica.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="TF_LBI_STYLE_BTN_BUTTON"></span><span id="tf_lbi_style_btn_button"></span><dl> <dt>**TF \_ PULSANTE \_ \_ BTN \_**</dt> STILE LBI <dt>0x00010000</dt> </dl>                           | L'elemento è un pulsante di comando. [ITfLangBarItemButton::OnClick](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onclick) viene chiamato quando viene premuto l'elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_BTN_MENU"></span><span id="tf_lbi_style_btn_menu"></span><dl> <dt>**TF \_ MENU \_ LBI STYLE \_ BTN \_ 0x00020000**</dt> <dt></dt> </dl>                                 | La voce è un menu. [ITfLangBarItemButton::InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) viene chiamato quando viene premuto l'elemento.<br/> Se questo stile viene combinato con TF \_ LBI \_ STYLE \_ BTN BUTTON, verrà visualizzata una freccia a discesa per l'elemento \_ oltre al testo. La freccia a discesa funziona come pulsante di menu e facendo clic su di esso verrà chiamato **ITfLangBarItemButton::InitMenu.** Facendo clic sulla parte di testo del pulsante verrà chiamato **ITfLangBarItemButton::OnClick.**<br/> |
| <span id="TF_LBI_STYLE_BTN_TOGGLE"></span><span id="tf_lbi_style_btn_toggle"></span><dl> <dt>**TF \_ INTERRUTTORE \_ \_ LBI STYLE BTN \_ 0x00040000**</dt> <dt></dt> </dl>                           | L'elemento è un interruttore e funziona in modo simile a una casella di controllo. **ITfLangBarItemButton::OnClick** viene chiamato quando viene premuto l'elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                       |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Componente ridistribuibile<br/>          | TSF 1.0 in Windows 2000 Professional<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Ctfutb.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Ctfutb.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[TF \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> <dt>

[ITfLangBarItem::GetInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getinfo)
</dt> <dt>

[ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





