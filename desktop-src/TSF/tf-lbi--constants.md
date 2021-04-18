---
title: Costanti TF_LBI_ (Ctfutb. h)
description: Le \_ costanti TF LBI \_ \ vengono usate con il metodo OnUpdate di ITfLangBarItemSink per indicare quali elementi della barra della lingua sono stati modificati.
ms.assetid: ed84012f-19ba-43b3-bbb5-7373ed174c33
topic_type:
- apiref
api_name:
- TF_LBI_ICON
- TF_LBI_TEXT
- TF_LBI_TOOLTIP
- TF_LBI_BITMAP
- TF_LBI_BALLOON
- TF_LBI_STATUS
- TF_LBI_BMPALL
- TF_LBI_BMPBTNALL
- TF_LBI_BTNALL
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72b69f1cb5a5b4a24e78a2bdc1ca0e7a9d79cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301345"
---
# <a name="tf_lbi_-constants"></a>\_Costanti LBI \_ \* TF

Le costanti ** \_ tf \_ \* LBI* _ vengono usate con il metodo [ITfLangBarItemSink:: OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) per indicare quali elementi della barra della lingua sono stati modificati.



| Costante/valore                                                                                                                                                                                                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_ICON"></span><span id="tf_lbi_icon"></span><dl> <dt>_ * TF \_ Icona di LBI \_ * *</dt> <dt>0x00000001</dt> </dl>                                                        | L'icona dell'elemento è stata modificata. La barra della lingua chiama [ITfLangBarItemButton:: GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) in risposta a questa notifica.<br/>                                                                                                                                             |
| <span id="TF_LBI_TEXT"></span><span id="tf_lbi_text"></span><dl> <dt>**Tf \_ 0x00000002 \_ testo LBI**</dt> <dt></dt> </dl>                                                        | Il testo di un pulsante o di un elemento del pulsante bitmap è stato modificato. La barra della lingua chiama [ITfLangBarItemButton:: GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) o [ITfLangBarItemBitmapButton:: GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext), a seconda del caso appropriato, in risposta a questa notifica.<br/>           |
| <span id="TF_LBI_TOOLTIP"></span><span id="tf_lbi_tooltip"></span><dl> <dt>**Tf \_ \_Descrizione comando LBI**</dt> <dt>0x00000004</dt> </dl>                                               | Testo della descrizione comando dell'elemento modificato. La barra della lingua chiama [ITfLangBarItem:: GetTooltipString](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) in risposta a questa notifica.<br/>                                                                                                                                   |
| <span id="TF_LBI_BITMAP"></span><span id="tf_lbi_bitmap"></span><dl> <dt>**Tf \_ 0x00000008 \_ bitmap LBI**</dt> <dt></dt> </dl>                                                  | Bitmap di una bitmap o di un elemento del pulsante bitmap modificato. La barra della lingua chiama [ITfLangBarItemBitmap::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) o [ITfLangBarItemBitmapButton::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), a seconda del caso appropriato, in risposta a questa notifica.<br/> |
| <span id="TF_LBI_BALLOON"></span><span id="tf_lbi_balloon"></span><dl> <dt>**Tf \_ 0x00000010 \_ Balloon LBI**</dt> <dt></dt> </dl>                                               | Le informazioni relative a un elemento del fumetto sono state modificate. La barra della lingua chiama [ITfLangBarItemBalloon:: GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) in risposta a questa notifica.<br/>                                                                                                                   |
| <span id="TF_LBI_STATUS"></span><span id="tf_lbi_status"></span><dl> <dt>**Tf \_ \_Stato LBI**</dt> <dt>0x00010000</dt> </dl>                                                  | Lo stato dell'elemento è stato modificato. La barra della lingua chiama [ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) in risposta a questa notifica.<br/>                                                                                                                                                              |
| <span id="TF_LBI_BMPALL"></span><span id="tf_lbi_bmpall"></span><dl> <dt>**Tf \_ LBI \_ BMPALL**</dt> <dt>tf \_ LBI \_ bitmap \| tf \_ LBI \_ TOOLTIP</dt> </dl>                          | Combina la \_ bitmap TF LBI \_ e \_ la \_ Descrizione comando tf LBI.<br/>                                                                                                                                                                                                                                                           |
| <span id="TF_LBI_BMPBTNALL"></span><span id="tf_lbi_bmpbtnall"></span><dl> <dt>**Tf \_ LBI \_ BMPBTNALL**</dt> <dt>tf \_ LBI \_ bitmap \| tf \_ LBI \_ Text \| tf \_ LBI \_ TOOLTIP</dt> </dl> | Combina la \_ bitmap TF LBI \_ , il \_ testo TF LBI e la \_ \_ \_ Descrizione comando tf LBI.<br/>                                                                                                                                                                                                                                            |
| <span id="TF_LBI_BTNALL"></span><span id="tf_lbi_btnall"></span><dl> <dt>**Tf \_ LBI \_ BTNALL**</dt> <dt>tf \_ LBI \_ Icon \| tf \_ LBI \_ Text \| tf \_ LBI \_ TOOLTIP</dt> </dl>            | Combina l' \_ icona TF LBI \_ , il \_ testo TF LBI e la \_ \_ \_ Descrizione comando tf LBI.<br/>                                                                                                                                                                                                                                              |



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

[ITfLangBarItemSink:: OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)
</dt> </dl>

 

 





