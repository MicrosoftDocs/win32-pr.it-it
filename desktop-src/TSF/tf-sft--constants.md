---
title: Costanti TF_SFT_ (Ctfutb. h)
description: Le \_ costanti TF SFT \_ \ specificano le impostazioni di visualizzazione di una barra di lingua mobile.
ms.assetid: 628e1d85-9614-4327-b89b-723f6eeb0718
topic_type:
- apiref
api_name:
- TF_SFT_SHOWNORMAL
- TF_SFT_DOCK
- TF_SFT_MINIMIZED
- TF_SFT_HIDDEN
- TF_SFT_NOTRANSPARENCY
- TF_SFT_LOWTRANSPARENCY
- TF_SFT_HIGHTRANSPARENCY
- TF_SFT_LABELS
- TF_SFT_NOLABELS
- TF_SFT_EXTRAICONSONMINIMIZED
- TF_SFT_NOEXTRAICONSONMINIMIZED
- TF_SFT_DESKBAND
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a947960bfbe67585dc02a37de2da3dc6737540
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301789"
---
# <a name="tf_sft_-constants"></a>\_Costanti TF SFT \_ \*

Le costanti ** \_ tf \_ \* SFT* _ specificano le impostazioni di visualizzazione di una barra di lingua mobile.



| Costante/valore                                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_SFT_SHOWNORMAL"></span><span id="tf_sft_shownormal"></span><dl> <dt>_ * TF \_ SFT \_ SHOWNORMAL * *</dt> <dt>0x00000001</dt> </dl>                                        | Visualizza la barra della lingua come finestra mobile. Questa costante non può essere combinata con le \_ costanti TF SFT \_ Dock, TF \_ SFT \_ ridotto, TF \_ SFT \_ Hidden o TF \_ SFT \_ DESKBAND.<br/>                                                                                                 |
| <span id="TF_SFT_DOCK"></span><span id="tf_sft_dock"></span><dl> <dt>**Tf \_ 0x00000002 \_ Dock SFT**</dt> <dt></dt> </dl>                                                          | Ancorare la barra della lingua nel relativo riquadro attività. Questa costante non può essere combinata con le \_ costanti SHOWNORMAL TF SFT, \_ tf \_ SFT \_ ridotta, TF \_ SFT \_ Hidden o TF \_ SFT \_ DESKBAND. Disponibile solo in Windows XP.<br/>                                                                |
| <span id="TF_SFT_MINIMIZED"></span><span id="tf_sft_minimized"></span><dl> <dt>**Tf \_ 0x00000004 \_ ridotto al minimo SFT**</dt> <dt></dt> </dl>                                           | Visualizza la barra della lingua come icona singola nell'area di notifica. Questa costante non può essere combinata con le \_ costanti TF SFT \_ SHOWNORMAL, TF \_ SFT \_ Dock, TF \_ SFT \_ Hidden o TF \_ SFT \_ DESKBAND. In Windows XP, utilizzare TF \_ SFT \_ DESKBAND in alternativa.<br/>                                   |
| <span id="TF_SFT_HIDDEN"></span><span id="tf_sft_hidden"></span><dl> <dt>**Tf \_ 0x00000008 \_ nascosto SFT**</dt> <dt></dt> </dl>                                                    | Nascondere la barra della lingua. Questa costante non può essere combinata con le \_ costanti TF SFT \_ SHOWNORMAL, TF \_ SFT \_ Dock, TF \_ SFT \_ ridotta o TF \_ SFT \_ DESKBAND.<br/>                                                                                                                     |
| <span id="TF_SFT_NOTRANSPARENCY"></span><span id="tf_sft_notransparency"></span><dl> <dt>**Tf \_ SFT \_ notransparency**</dt> <dt>0x00000010</dt> </dl>                            | Rendere opaca la barra della lingua.<br/>                                                                                                                                                                                                                                                |
| <span id="TF_SFT_LOWTRANSPARENCY"></span><span id="tf_sft_lowtransparency"></span><dl> <dt>**Tf \_ SFT \_ LOWTRANSPARENCY**</dt> <dt>0x00000020</dt> </dl>                         | Rendere la barra del linguaggio parzialmente trasparente. Disponibile solo in Windows 2000 o versioni successive.<br/>                                                                                                                                                                                        |
| <span id="TF_SFT_HIGHTRANSPARENCY"></span><span id="tf_sft_hightransparency"></span><dl> <dt>**Tf \_ SFT \_ HIGHTRANSPARENCY**</dt> <dt>0x00000040</dt> </dl>                      | Rendere la barra della lingua altamente trasparente. Disponibile solo in Windows 2000 o versioni successive.<br/>                                                                                                                                                                                           |
| <span id="TF_SFT_LABELS"></span><span id="tf_sft_labels"></span><dl> <dt>**Tf \_ \_Etichette SFT**</dt> <dt>0x00000080</dt> </dl>                                                    | Visualizzare le etichette di testo accanto alle icone della barra della lingua.<br/>                                                                                                                                                                                                                              |
| <span id="TF_SFT_NOLABELS"></span><span id="tf_sft_nolabels"></span><dl> <dt>**Tf \_ SFT \_ NOlabels**</dt> <dt>0x00000100</dt> </dl>                                              | Nasconde le etichette di testo dell'icona della barra della lingua.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_SFT_EXTRAICONSONMINIMIZED"></span><span id="tf_sft_extraiconsonminimized"></span><dl> <dt>**Tf \_ SFT \_ EXTRAICONSONMINIMIZED**</dt> <dt>0x00000200</dt> </dl>       | Visualizza le icone del servizio di testo sulla barra delle applicazioni quando la barra della lingua è ridotta a icona.<br/>                                                                                                                                                                                                |
| <span id="TF_SFT_NOEXTRAICONSONMINIMIZED"></span><span id="tf_sft_noextraiconsonminimized"></span><dl> <dt>**Tf \_ SFT \_ NOEXTRAICONSONMINIMIZED**</dt> <dt>0x00000400</dt> </dl> | Nascondere le icone del servizio di testo sulla barra delle applicazioni quando la barra della lingua è ridotta a icona.<br/>                                                                                                                                                                                                   |
| <span id="TF_SFT_DESKBAND"></span><span id="tf_sft_deskband"></span><dl> <dt>**Tf \_ SFT \_ DESKBAND**</dt> <dt>0x00000800</dt> </dl>                                              | Ancorare la barra della lingua nell'estremità destra della barra delle applicazioni di sistema (immediatamente a sinistra del vassoio/orologio di sistema). Questa costante non può essere combinata con le \_ \_ costanti nascoste TF SFT SHOWNORMAL, TF \_ SFT \_ Dock, TF \_ SFT \_ ridotta o TF \_ SFT \_ . Disponibile solo in Windows XP.<br/> |



## <a name="remarks"></a>Commenti

Il metodo [ITfLangBarMgr:: ShowFloating](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating) imposta il risultato di un'operazione **or** logica su una o più di queste costanti per specificare gli attributi dell'elemento della barra della lingua.

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

[ITfLangBarMgr::ShowFloating](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating)
</dt> </dl>

 

 





