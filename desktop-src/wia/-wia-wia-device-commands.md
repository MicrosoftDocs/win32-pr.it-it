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
# <a name="wia-device-commands"></a><span data-ttu-id="55d8b-103">Comandi del dispositivo WIA</span><span class="sxs-lookup"><span data-stu-id="55d8b-103">WIA Device Commands</span></span>

<span data-ttu-id="55d8b-104">Le costanti seguenti costituiscono il set di comandi del dispositivo hardware di acquisizione di immagini Windows (WIA) validi.</span><span class="sxs-lookup"><span data-stu-id="55d8b-104">The following constants form the set of valid Windows Image Acquisition (WIA) hardware device commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="55d8b-105">Costante</span><span class="sxs-lookup"><span data-stu-id="55d8b-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="55d8b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55d8b-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl> <span data-ttu-id="55d8b-107"><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="55d8b-107"><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="55d8b-108">Causa la sincronizzazione degli elementi memorizzati nella cache con il dispositivo hardware da parte del minidriver del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55d8b-108">Causes the device's minidriver to synchronize cached items with the hardware device.</span></span> <span data-ttu-id="55d8b-109">Se il dispositivo supporta il metodo <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem:: AnalyzeItem</strong></a> , l'esecuzione di questo comando comporta l'eliminazione dei risultati dell'analisi da parte di minidriver e la reimpostazione dello stato iniziale dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="55d8b-109">If the device supports the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem::AnalyzeItem</strong></a> method, issuing this command causes the minidriver to discard the analysis results and reset the item to its initial state.</span></span> <span data-ttu-id="55d8b-110">Tutti i driver devono supportare questo comando.</span><span class="sxs-lookup"><span data-stu-id="55d8b-110">All drivers must support this command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl> <span data-ttu-id="55d8b-111"><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="55d8b-111"><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="55d8b-112">Determina l'acquisizione di un'immagine da un dispositivo WIA.</span><span class="sxs-lookup"><span data-stu-id="55d8b-112">Causes a WIA device to acquire an image.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl> <span data-ttu-id="55d8b-113"><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="55d8b-113"><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="55d8b-114">Indica al dispositivo di eliminare tutti gli elementi che possono essere eliminati dalla struttura ad albero degli oggetti <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> che rappresentano il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55d8b-114">Tells the device to delete all items that can be deleted from the tree of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> objects that represent the device.</span></span> <span data-ttu-id="55d8b-115">L'eliminazione degli elementi viene impedita impostando le proprietà dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="55d8b-115">Item deletion is prevented by setting the item's properties.</span></span> <span data-ttu-id="55d8b-116">Per informazioni dettagliate, vedere <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage:: SetPropertyStream</strong></a> e <a href="-wia-property-attributes.md">attributi della proprietà</a>.</span><span class="sxs-lookup"><span data-stu-id="55d8b-116">For details, see <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage::SetPropertyStream</strong></a> and <a href="-wia-property-attributes.md">Property Attributes</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl> <span data-ttu-id="55d8b-117"><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="55d8b-117"><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="55d8b-118">Usato per gli scanner di documenti.</span><span class="sxs-lookup"><span data-stu-id="55d8b-118">Used for document scanners.</span></span> <span data-ttu-id="55d8b-119">Determina il caricamento della pagina successiva nel gestore del documento da parte dello scanner.</span><span class="sxs-lookup"><span data-stu-id="55d8b-119">Causes the scanner to load the next page in its document handler.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl> <span data-ttu-id="55d8b-120"><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="55d8b-120"><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="55d8b-121">Usato per gli scanner di documenti.</span><span class="sxs-lookup"><span data-stu-id="55d8b-121">Used for document scanners.</span></span> <span data-ttu-id="55d8b-122">Indica al dispositivo di scaricare tutte le pagine rimanenti nel relativo gestore del documento.</span><span class="sxs-lookup"><span data-stu-id="55d8b-122">Tells the device to unload all remaining pages in its document handler.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl> <span data-ttu-id="55d8b-123"><dt><strong>WIA_CMD_START_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="55d8b-123"><dt><strong>WIA_CMD_START_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="55d8b-124">Usato per gli scanner di documenti con un feeder di pagine.</span><span class="sxs-lookup"><span data-stu-id="55d8b-124">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="55d8b-125">Indica al dispositivo di avviare il motore del feeder.</span><span class="sxs-lookup"><span data-stu-id="55d8b-125">Tells the device to start the feeder motor.</span></span> <span data-ttu-id="55d8b-126">Questa funzionalità è disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="55d8b-126">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="55d8b-127">Il minidriver WIA deve rifiutare questo comando e restituire <strong>WIA_ERROR_INVALID_COMMAND</strong> quando la proprietà <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> non è supportata oppure è impostata su WIA_FEEDER_CONTROL_AUTO.</span><span class="sxs-lookup"><span data-stu-id="55d8b-127">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl> <span data-ttu-id="55d8b-128"><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="55d8b-128"><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="55d8b-129">Usato per gli scanner di documenti con un feeder di pagine.</span><span class="sxs-lookup"><span data-stu-id="55d8b-129">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="55d8b-130">Indica al dispositivo di arrestare il motore del feeder.</span><span class="sxs-lookup"><span data-stu-id="55d8b-130">Tells the device to stop the feeder motor.</span></span> <span data-ttu-id="55d8b-131">Questa funzionalità è disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="55d8b-131">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="55d8b-132">Il minidriver WIA deve rifiutare questo comando e restituire <strong>WIA_ERROR_INVALID_COMMAND</strong> quando la proprietà <strong>WIA_IPS_FEEDER_CONTROL</strong> non è supportata oppure è impostata su WIA_FEEDER_CONTROL_AUTO.</span><span class="sxs-lookup"><span data-stu-id="55d8b-132">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <strong>WIA_IPS_FEEDER_CONTROL</strong> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl> <span data-ttu-id="55d8b-133"><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="55d8b-133"><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="55d8b-134">Usato per gli scanner di documenti con un feeder di pagine.</span><span class="sxs-lookup"><span data-stu-id="55d8b-134">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="55d8b-135">Indica al dispositivo di sospendere il motore del feeder.</span><span class="sxs-lookup"><span data-stu-id="55d8b-135">Tells the device to pause the feeder motor.</span></span> <span data-ttu-id="55d8b-136">Questa funzionalità è disponibile a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="55d8b-136">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="55d8b-137">Il minidriver WIA deve rifiutare questo comando e restituire <strong>WIA_ERROR_INVALID_COMMAND</strong> quando la proprietà <strong>WIA_IPS_FEEDER_CONTROL</strong> non è supportata oppure è impostata su WIA_FEEDER_CONTROL_AUTO.</span><span class="sxs-lookup"><span data-stu-id="55d8b-137">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <strong>WIA_IPS_FEEDER_CONTROL</strong> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="55d8b-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55d8b-138">Requirements</span></span>



| <span data-ttu-id="55d8b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="55d8b-139">Requirement</span></span> | <span data-ttu-id="55d8b-140">Valore</span><span class="sxs-lookup"><span data-stu-id="55d8b-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="55d8b-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55d8b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="55d8b-142">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="55d8b-142">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="55d8b-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55d8b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="55d8b-144">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="55d8b-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="55d8b-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55d8b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="55d8b-146"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="55d8b-146"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
