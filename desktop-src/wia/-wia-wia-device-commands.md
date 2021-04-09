---
description: Le costanti seguenti costituiscono il set di comandi del dispositivo hardware di acquisizione di immagini Windows (WIA) validi.
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: Comandi del dispositivo WIA (Wiadef. h)
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
ms.openlocfilehash: 6e9e732520a256519ebcb21da84eac7ca8d8b630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879310"
---
# <a name="wia-device-commands"></a>Comandi del dispositivo WIA

Le costanti seguenti costituiscono il set di comandi del dispositivo hardware di acquisizione di immagini Windows (WIA) validi.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl> <dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </dl></td>
<td style="text-align: left;">Causa la sincronizzazione degli elementi memorizzati nella cache con il dispositivo hardware da parte del minidriver del dispositivo. Se il dispositivo supporta il metodo <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem:: AnalyzeItem</strong></a> , l'esecuzione di questo comando comporta l'eliminazione dei risultati dell'analisi da parte di minidriver e la reimpostazione dello stato iniziale dell'elemento. Tutti i driver devono supportare questo comando.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl> <dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </dl></td>
<td style="text-align: left;">Determina l'acquisizione di un'immagine da un dispositivo WIA.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl> <dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </dl></td>
<td style="text-align: left;">Indica al dispositivo di eliminare tutti gli elementi che possono essere eliminati dalla struttura ad albero degli oggetti <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> che rappresentano il dispositivo. L'eliminazione degli elementi viene impedita impostando le proprietà dell'elemento. Per informazioni dettagliate, vedere <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage:: SetPropertyStream</strong></a> e <a href="-wia-property-attributes.md">attributi della proprietà</a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl> <dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">Usato per gli scanner di documenti. Determina il caricamento della pagina successiva nel gestore del documento da parte dello scanner.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl> <dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">Usato per gli scanner di documenti. Indica al dispositivo di scaricare tutte le pagine rimanenti nel relativo gestore del documento. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl> <dt><strong>WIA_CMD_START_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Usato per gli scanner di documenti con un feeder di pagine. Indica al dispositivo di avviare il motore del feeder. Questa funzionalità è disponibile a partire da Windows 8.<br/>
<blockquote>
[!Note]<br />
Il minidriver WIA deve rifiutare questo comando e restituire <strong>WIA_ERROR_INVALID_COMMAND</strong> quando la proprietà <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> non è supportata oppure è impostata su WIA_FEEDER_CONTROL_AUTO.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl> <dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Usato per gli scanner di documenti con un feeder di pagine. Indica al dispositivo di arrestare il motore del feeder. Questa funzionalità è disponibile a partire da Windows 8.<br/>
<blockquote>
[!Note]<br />
Il minidriver WIA deve rifiutare questo comando e restituire <strong>WIA_ERROR_INVALID_COMMAND</strong> quando la proprietà <strong>WIA_IPS_FEEDER_CONTROL</strong> non è supportata oppure è impostata su WIA_FEEDER_CONTROL_AUTO.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl> <dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Usato per gli scanner di documenti con un feeder di pagine. Indica al dispositivo di sospendere il motore del feeder. Questa funzionalità è disponibile a partire da Windows 8.<br/>
<blockquote>
[!Note]<br />
Il minidriver WIA deve rifiutare questo comando e restituire <strong>WIA_ERROR_INVALID_COMMAND</strong> quando la proprietà <strong>WIA_IPS_FEEDER_CONTROL</strong> non è supportata oppure è impostata su WIA_FEEDER_CONTROL_AUTO.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
