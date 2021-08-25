---
description: Le costanti seguenti formano il set di comandi del dispositivo hardware WIA (Windows Image Acquisition) validi.
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: Comandi del dispositivo WIA (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CMD_SYNCHRONIZE
- WIA_CMD_TAKE_PICTURE
- WIA_CMD_DELETE_ALL_ITEMS
- WIA_CMD_CHANGE_DOCUMENT
- WIA_CMD_UNLOAD_DOCUMENT
- WIA_CMD_START_FEEDER
- WIA_CMD_STOP_FEEDER
- WIA_CMD_PAUSE_FEEDER
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 08aeb26502686d2550d872bcfa845e3c68230ac4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467108"
---
# <a name="wia-device-commands"></a>Comandi del dispositivo WIA

Le costanti seguenti formano il set di comandi del dispositivo hardware WIA (Windows Image Acquisition) validi.




| Costante | Descrizione | 
|----------|-------------|
| <span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt></dl> | Determina la sincronizzazione degli elementi memorizzati nella cache con il dispositivo hardware da parte del minidriver del dispositivo. Se il dispositivo supporta il metodo <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem::AnalyzeItem,</strong></a> l'esecuzione di questo comando comporta la rimozione dei risultati dell'analisi da parte del minidriver e il ripristino dello stato iniziale dell'elemento. Tutti i driver devono supportare questo comando.<br /> | 
| <span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt></dl> | Determina l'acquisizione di un'immagine da parte di un dispositivo WIA.<br /> | 
| <span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt></dl> | Indica al dispositivo di eliminare tutti gli elementi che possono essere eliminati dall'albero degli oggetti <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> che rappresentano il dispositivo. L'eliminazione dell'elemento viene impedita impostando le proprietà dell'elemento. Per informazioni dettagliate, vedere <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage::SetPropertyStream</strong></a> e <a href="-wia-property-attributes.md">Attributi delle proprietà</a>.<br /> | 
| <span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt></dl> | Usato per gli scanner di documenti. Fa sì che lo scanner carichi la pagina successiva nel gestore del documento.<br /> | 
| <span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt></dl> | Usato per gli scanner di documenti. Indica al dispositivo di scaricare tutte le pagine rimanenti nel gestore del documento. <br /> | 
| <span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl><dt><strong>WIA_CMD_START_FEEDER</strong></dt></dl> | Usato per gli scanner di documenti con un alimentatore di pagine. Indica al dispositivo di avviare il motore dell'alimentatore. Questa funzionalità è disponibile a partire da Windows 8.<br /><blockquote>[!Note]<br />Il minidriver WIA deve rifiutare questo comando e restituire WIA_ERROR_INVALID_COMMAND <strong>quando</strong> la proprietà <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> non è supportata o è impostata su WIA_FEEDER_CONTROL_AUTO.</blockquote><br /> | 
| <span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt></dl> | Usato per gli scanner di documenti con un alimentatore di pagine. Indica al dispositivo di arrestare il motore dell'alimentatore. Questa funzionalità è disponibile a partire da Windows 8.<br /><blockquote>[!Note]<br />Il minidriver WIA deve rifiutare questo comando e restituire WIA_ERROR_INVALID_COMMAND <strong>quando</strong> la proprietà <strong>WIA_IPS_FEEDER_CONTROL</strong> non è supportata o è impostata su WIA_FEEDER_CONTROL_AUTO.</blockquote><br /> | 
| <span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt></dl> | Usato per gli scanner di documenti con un alimentatore di pagine. Indica al dispositivo di sospendere il motore dell'alimentatore. Questa funzionalità è disponibile a partire da Windows 8.<br /><blockquote>[!Note]<br />Il minidriver WIA deve rifiutare questo comando e restituire WIA_ERROR_INVALID_COMMAND <strong>quando</strong> la proprietà <strong>WIA_IPS_FEEDER_CONTROL</strong> non è supportata o è impostata su WIA_FEEDER_CONTROL_AUTO.</blockquote><br /> | 




## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 
