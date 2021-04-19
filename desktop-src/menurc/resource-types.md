---
title: Tipi di risorse (winuser. h)
description: Di seguito sono riportati i tipi di risorse predefiniti.
ms.assetid: 8d27f79a-8165-4565-a975-f25b2344efdc
topic_type:
- apiref
api_name:
- RT_ACCELERATOR
- RT_ANICURSOR
- RT_ANIICON
- RT_BITMAP
- RT_CURSOR
- RT_DIALOG
- RT_DLGINCLUDE
- RT_FONT
- RT_FONTDIR
- RT_GROUP_CURSOR
- RT_GROUP_ICON
- RT_HTML
- RT_ICON
- RT_MANIFEST
- RT_MENU
- RT_MESSAGETABLE
- RT_PLUGPLAY
- RT_RCDATA
- RT_STRING
- RT_VERSION
- RT_VXD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595f1d459f645d26014a644d0e2b7cb608f4c6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332379"
---
# <a name="resource-types"></a>Tipi di risorsa

Di seguito sono riportati i tipi di risorse predefiniti.



| Costante/valore                                                                                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RT_ACCELERATOR"></span><span id="rt_accelerator"></span><dl> <dt>**RT \_ ACCELERAtore**</dt> <dt>MAKEINTRESOURCE (9)</dt> </dl>                                 | Tabella dei tasti di scelta rapida.<br/>                                                                                                                                                                                                                                                                    |
| <span id="RT_ANICURSOR"></span><span id="rt_anicursor"></span><dl> <dt>**RT \_ ANICURSOR**</dt> <dt>MAKEINTRESOURCE (21)</dt> </dl>                                      | Cursore animato.<br/>                                                                                                                                                                                                                                                                      |
| <span id="RT_ANIICON"></span><span id="rt_aniicon"></span><dl> <dt>**RT \_ ANIICON**</dt> <dt>MAKEINTRESOURCE (22)</dt> </dl>                                            | Icona animata.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_BITMAP"></span><span id="rt_bitmap"></span><dl> <dt>**RT \_ BITMAP**</dt> <dt>MAKEINTRESOURCE (2)</dt> </dl>                                                | Risorsa bitmap.<br/>                                                                                                                                                                                                                                                                      |
| <span id="RT_CURSOR"></span><span id="rt_cursor"></span><dl> <dt>**RT \_ CURSORE**</dt> <dt>MAKEINTRESOURCE (1)</dt> </dl>                                                | Risorsa del cursore dipendente dall'hardware.<br/>                                                                                                                                                                                                                                                   |
| <span id="RT_DIALOG"></span><span id="rt_dialog"></span><dl> <dt>**RT \_ Finestra di dialogo**</dt> <dt>MAKEINTRESOURCE (5)</dt> </dl>                                                | Finestra di dialogo.<br/>                                                                                                                                                                                                                                                                           |
| <span id="RT_DLGINCLUDE"></span><span id="rt_dlginclude"></span><dl> <dt>**RT \_ DLGINCLUDE**</dt> <dt>MAKEINTRESOURCE (17)</dt> </dl>                                   | Consente a uno strumento di modifica delle risorse di associare una stringa a un file RC. In genere, la stringa è il nome del file di intestazione che fornisce i nomi simbolici. Il compilatore di risorse analizza la stringa, ma altrimenti ignora il valore. Ad esempio, <br/> `1 DLGINCLUDE "MyFile.h"`<br/> |
| <span id="RT_FONT"></span><span id="rt_font"></span><dl> <dt>**RT \_ CARATTERE**</dt> <dt>MAKEINTRESOURCE (8)</dt> </dl>                                                      | Risorsa del tipo di carattere.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_FONTDIR"></span><span id="rt_fontdir"></span><dl> <dt>**RT \_ FONTDIR**</dt> <dt>MAKEINTRESOURCE (7)</dt> </dl>                                             | Risorsa della directory dei tipi di carattere.<br/>                                                                                                                                                                                                                                                              |
| <span id="RT_GROUP_CURSOR"></span><span id="rt_group_cursor"></span><dl> <dt>**RT \_ \_Cursori del gruppo**</dt> <dt>MAKEINTRESOURCE ((ULONG \_ ptr) (RT \_ Cursor) + 11)</dt> </dl> | Risorsa Cursor indipendente dall'hardware.<br/>                                                                                                                                                                                                                                                 |
| <span id="RT_GROUP_ICON"></span><span id="rt_group_icon"></span><dl> <dt>**RT \_ \_Icona del gruppo**</dt> <dt>MAKEINTRESOURCE ((ULONG \_ ptr) ( \_ icona RT) + 11)</dt> </dl>         | Risorsa icona indipendente dall'hardware.<br/>                                                                                                                                                                                                                                                   |
| <span id="RT_HTML"></span><span id="rt_html"></span><dl> <dt>**RT \_ MAKEINTRESOURCE HTML**</dt> <dt>(23)</dt> </dl>                                                     | Risorsa HTML.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_ICON"></span><span id="rt_icon"></span><dl> <dt>**RT \_ ICONA**</dt> <dt>MAKEINTRESOURCE (3)</dt> </dl>                                                      | Risorsa icona dipendente dall'hardware.<br/>                                                                                                                                                                                                                                                     |
| <span id="RT_MANIFEST"></span><span id="rt_manifest"></span><dl> <dt>**RT \_ MANIFESTO**</dt> <dt>MAKEINTRESOURCE (24)</dt> </dl>                                         | Manifesto dell'assembly affiancato.<br/>                                                                                                                                                                                                                                                       |
| <span id="RT_MENU"></span><span id="rt_menu"></span><dl> <dt>**RT \_ MENU**</dt> <dt>MAKEINTRESOURCE (4)</dt> </dl>                                                      | Risorsa di menu.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_MESSAGETABLE"></span><span id="rt_messagetable"></span><dl> <dt>**RT \_ MESSAGETABLE**</dt> <dt>MAKEINTRESOURCE (11)</dt> </dl>                             | Voce della tabella messaggio.<br/>                                                                                                                                                                                                                                                                  |
| <span id="RT_PLUGPLAY"></span><span id="rt_plugplay"></span><dl> <dt>**RT \_ PLUGPLAY**</dt> <dt>MAKEINTRESOURCE (19)</dt> </dl>                                         | Risorsa Plug and Play.<br/>                                                                                                                                                                                                                                                               |
| <span id="RT_RCDATA"></span><span id="rt_rcdata"></span><dl> <dt>**RT \_ RCDATA**</dt> <dt>MAKEINTRESOURCE (10)</dt> </dl>                                               | Risorsa definita dall'applicazione (dati non elaborati).<br/>                                                                                                                                                                                                                                              |
| <span id="RT_STRING"></span><span id="rt_string"></span><dl> <dt>**RT \_ STRINGA**</dt> <dt>MAKEINTRESOURCE (6)</dt> </dl>                                                | Voce della tabella di stringhe.<br/>                                                                                                                                                                                                                                                                   |
| <span id="RT_VERSION"></span><span id="rt_version"></span><dl> <dt>**RT \_ VERSIONE**</dt> <dt>MAKEINTRESOURCE (16)</dt> </dl>                                            | Risorsa della versione.<br/>                                                                                                                                                                                                                                                                     |
| <span id="RT_VXD"></span><span id="rt_vxd"></span><dl> <dt>**RT \_ VXD**</dt> <dt>MAKEINTRESOURCE (20)</dt> </dl>                                                        | VXD.<br/>                                                                                                                                                                                                                                                                                  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

 





