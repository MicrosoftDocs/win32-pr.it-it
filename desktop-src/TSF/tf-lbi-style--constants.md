---
title: Costanti TF_LBI_STYLE_ (Ctfutb. h)
description: Le costanti di TF \_ LBI \_ Style \_ \ vengono usate nel membro DWSTYLE della \_ struttura TF LANGBARITEMINFO per specificare lo stile di un elemento della barra della lingua.
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
ms.openlocfilehash: 3b43ef805161afce6cb73bfaa26060308bc0aa5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476570"
---
# <a name="tf_lbi_style_-constants"></a>\_Costanti di \_ stile TF LBI \_ \*

Per specificare lo stile di un elemento della barra della lingua, [ \_](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo) **\_ \_ \_ \* *vengono usate le costanti _* LBI Style _ di TF** .

Se questo stile è combinato con il \_ \_ pulsante BTN stile TF LBI \_ \_ , verrà visualizzata una freccia a discesa per l'elemento oltre al testo. La freccia a discesa funziona come pulsante di menu e facendo clic su di essa si farà in modo che **ITfLangBarItemButton:: InitMenu** venga chiamato. Facendo clic sulla parte di testo del pulsante si farà in modo che **ITfLangBarItemButton:: OnClick** venga chiamato.



| Costante/valore                                                                                                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STYLE_HIDDENSTATUSCONTROL"></span><span id="tf_lbi_style_hiddenstatuscontrol"></span><dl> <dt>**Tf \_ \_Stile LBI \_ HIDDENSTATUSCONTROL**</dt> <dt>0x00000001</dt> </dl> | L'elemento può essere nascosto o visualizzato in modo dinamico usando il \_ \_ valore nascosto stato TF LBI \_ nel metodo [ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) . Se questo valore non è presente, l'elemento non può essere nascosto in questo modo.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_SHOWNINTRAY"></span><span id="tf_lbi_style_shownintray"></span><dl> <dt>**Tf \_ \_Stile LBI \_ SHOWNINTRAY**</dt> <dt>0x00000002</dt> </dl>                         | L'elemento verrà visualizzato nella barra delle icone di notifica oltre alla barra della lingua. Questo flag non è attualmente supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="TF_LBI_STYLE_HIDEONNOOTHERITEMS"></span><span id="tf_lbi_style_hideonnootheritems"></span><dl> <dt>**Tf \_ \_Stile LBI \_ HIDEONNOOTHERITEMS**</dt> <dt>0x00000004</dt> </dl>    | La barra della lingua è nascosta se tutti gli elementi nella barra della lingua contengono questo stile. Se un elemento nella barra della lingua non contiene questo stile, viene visualizzata la barra della lingua.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="TF_LBI_STYLE_SHOWNINTRAYONLY"></span><span id="tf_lbi_style_shownintrayonly"></span><dl> <dt>**Tf \_ \_Stile LBI \_ SHOWNINTRAYONLY**</dt> <dt>0x00000008</dt> </dl>             | L'elemento verrà visualizzato solo nella barra delle icone di notifica e non nella barra della lingua. Questo flag non è attualmente supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_HIDDENBYDEFAULT"></span><span id="tf_lbi_style_hiddenbydefault"></span><dl> <dt>**Tf \_ \_Stile LBI \_ HIDDENBYDEFAULT**</dt> <dt>0x00000010</dt> </dl>             | L'elemento non viene visualizzato nella barra degli strumenti fino a quando non viene selezionato dal menu delle opzioni della barra della lingua. Questo flag viene ignorato se \_ \_ è impostato lo stile TF LBI \_ HIDDENSTATUSCONTROL o se l'utente ha già modificato lo stato nascosto o visualizzato usando il menu delle opzioni della barra della lingua.<br/>                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_TEXTCOLORICON"></span><span id="tf_lbi_style_textcoloricon"></span><dl> <dt>**Tf \_ \_Stile LBI \_ TEXTCOLORICON**</dt> <dt>0x00000020</dt> </dl>                   | Qualsiasi pixel nero all'interno dell'icona verrà convertito nel colore del testo del tema selezionato. L'icona deve essere monocromatica.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="TF_LBI_STYLE_BTN_BUTTON"></span><span id="tf_lbi_style_btn_button"></span><dl> <dt>**Tf \_ \_ \_ \_ Pulsante BTN di LBI Style**</dt> <dt>0x00010000</dt> </dl>                           | L'elemento è un pulsante di push. [ITfLangBarItemButton:: OnClick](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onclick) viene chiamato quando viene premuto l'elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_BTN_MENU"></span><span id="tf_lbi_style_btn_menu"></span><dl> <dt>**Tf \_ \_ \_ \_ Menu BTN stile LBI**</dt> <dt>0x00020000</dt> </dl>                                 | L'elemento è un menu. [ITfLangBarItemButton:: InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) viene chiamato quando viene premuto l'elemento.<br/> Se questo stile è combinato con il \_ \_ pulsante BTN stile TF LBI \_ \_ , verrà visualizzata una freccia a discesa per l'elemento oltre al testo. La freccia a discesa funziona come pulsante di menu e facendo clic su di essa si farà in modo che **ITfLangBarItemButton:: InitMenu** venga chiamato. Facendo clic sulla parte di testo del pulsante si farà in modo che **ITfLangBarItemButton:: OnClick** venga chiamato.<br/> |
| <span id="TF_LBI_STYLE_BTN_TOGGLE"></span><span id="tf_lbi_style_btn_toggle"></span><dl> <dt>**Tf \_ LBI \_ Style \_ BTN \_ /Nascondi**</dt> <dt>0x00040000</dt> </dl>                           | L'elemento è un interruttore e funziona in modo analogo a una casella di controllo. **ITfLangBarItemButton:: OnClick** viene chiamato quando viene premuto l'elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                       |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Ctfutb. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ctfutb. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_LANGBARITEMINFO TF](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> <dt>

[ITfLangBarItem:: GetInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getinfo)
</dt> <dt>

[ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





