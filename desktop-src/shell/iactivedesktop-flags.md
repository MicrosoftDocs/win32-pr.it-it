---
description: In questa sezione vengono descritti i flag utilizzati dai metodi dell'interfaccia IActiveDesktop.
title: Flag IActiveDesktop (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d1a2f69-0730-4805-8b50-071332ff7070
api_name:
- AD_APPLY_ALL
- AD_APPLY_BUFFERED_REFRESH
- AD_APPLY_DYNAMICREFRESH
- AD_APPLY_FORCE
- AD_APPLY_HTMLGEN
- AD_APPLY_REFRESH
- AD_APPLY_SAVE
- COMP_ELEM_ALL
- COMP_ELEM_CHECKED
- COMP_ELEM_CURITEMSTATE
- COMP_ELEM_FRIENDLYNAME
- COMP_ELEM_NOSCROLL
- COMP_ELEM_ORIGINAL_CSI
- COMP_ELEM_POS_LEFT
- COMP_ELEM_POS_TOP
- COMP_ELEM_POS_ZINDEX
- COMP_ELEM_RESTORED_CSI
- COMP_ELEM_SIZE_HEIGHT
- COMP_ELEM_SIZE_WIDTH
- COMP_ELEM_SOURCE
- COMP_ELEM_TYPE
- COMP_TYPE_CFHTML
- COMP_TYPE_CONTROL
- COMP_TYPE_HTMLDOC
- COMP_TYPE_MAX
- COMP_TYPE_PICTURE
- COMP_TYPE_WEBSITE
- COMPONENT_TOP
- WPSTYLE_CENTER
- WPSTYLE_MAX
- WPSTYLE_STRETCH
- WPSTYLE_TILE
- WPSTYLE_SPAN
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dae164c696ae54963f802a6ddd5cb1f6862b2f14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982931"
---
# <a name="iactivedesktop-flags"></a><span data-ttu-id="94ba8-103">Flag IActiveDesktop</span><span class="sxs-lookup"><span data-stu-id="94ba8-103">IActiveDesktop Flags</span></span>

<span data-ttu-id="94ba8-104">In questa sezione vengono descritti i flag utilizzati dai metodi dell'interfaccia [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .</span><span class="sxs-lookup"><span data-stu-id="94ba8-104">This section describes the flags used by [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface methods.</span></span>

<dl> <dt>

<span data-ttu-id="94ba8-105"><span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD \_ apply \_ All**</span><span class="sxs-lookup"><span data-stu-id="94ba8-105"><span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD\_APPLY\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-106">Aggregazione di \* \* \* \* AD \_ apply \_ Save \* \* \* \*, \* \* \* \* ad \_ apply \_ HTMLGEN \* \* \* \* e \* \* \* \* ad \_ apply \_ Refresh \* \* \* \* values.</span><span class="sxs-lookup"><span data-stu-id="94ba8-106">Aggregate of the \*\*\*\*AD\_APPLY\_SAVE\*\*\*\*, \*\*\*\*AD\_APPLY\_HTMLGEN\*\*\*\*, and \*\*\*\*AD\_APPLY\_REFRESH\*\*\*\* values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-107"><span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD \_ applicare l' \_ aggiornamento memorizzato nel buffer \_**</span><span class="sxs-lookup"><span data-stu-id="94ba8-107"><span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD\_APPLY\_BUFFERED\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-108">Avvia un timer e aggrega tutte le richieste di aggiornamento effettuate con questo flag durante tale intervallo di tempo in un singolo aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="94ba8-108">Starts a timer and aggregates all the refresh requests made with this flag during that time interval into a single refresh.</span></span> <span data-ttu-id="94ba8-109">Questo intervallo è impostato su cinque secondi.</span><span class="sxs-lookup"><span data-stu-id="94ba8-109">This interval is set at five seconds.</span></span> <span data-ttu-id="94ba8-110">Alla fine dell'intervallo o se viene richiesto un aggiornamento durante l'intervallo senza un flag \* \* \* \* AD \_ apply \_ buffered \_ Refresh \* \* \* \*, l'aggiornamento viene eseguito e il timer viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="94ba8-110">At the end of the interval, or if a refresh is requested during the interval without an \*\*\*\*AD\_APPLY\_BUFFERED\_REFRESH\*\*\*\* flag, the refresh is made and the timer is stopped.</span></span> <span data-ttu-id="94ba8-111">Questo flag deve essere combinato con il flag \* \* \* \* AD \_ apply \_ Refresh \* \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="94ba8-111">This flag must be combined with the \*\*\*\*AD\_APPLY\_REFRESH\*\*\*\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-112"><span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD \_ apply \_ DYNAMICREFRESH**</span><span class="sxs-lookup"><span data-stu-id="94ba8-112"><span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD\_APPLY\_DYNAMICREFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-113">[Versione 5,0](versions.md).</span><span class="sxs-lookup"><span data-stu-id="94ba8-113">[Version 5.0](versions.md).</span></span> <span data-ttu-id="94ba8-114">Usare il codice HTML dinamico per aggiornare solo gli elementi che sono stati modificati dopo l'ultimo aggiornamento, non l'intero desktop.</span><span class="sxs-lookup"><span data-stu-id="94ba8-114">Use dynamic HTML to refresh only those items that have changed since the last refresh, not the entire desktop.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-115"><span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**AD \_ apply \_ Force**</span><span class="sxs-lookup"><span data-stu-id="94ba8-115"><span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**AD\_APPLY\_FORCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-116">Forzare una modifica del desktop attivo.</span><span class="sxs-lookup"><span data-stu-id="94ba8-116">Force an Active Desktop change.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-117"><span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD \_ apply \_ HTMLGEN**</span><span class="sxs-lookup"><span data-stu-id="94ba8-117"><span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD\_APPLY\_HTMLGEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-118">Rigenerare il file HTML del desktop.</span><span class="sxs-lookup"><span data-stu-id="94ba8-118">Regenerate the desktop HTML file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-119"><span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**AD \_ apply \_ Refresh**</span><span class="sxs-lookup"><span data-stu-id="94ba8-119"><span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**AD\_APPLY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-120">Aggiornare l'elemento del desktop.</span><span class="sxs-lookup"><span data-stu-id="94ba8-120">Refresh the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-121"><span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD \_ apply \_ Save**</span><span class="sxs-lookup"><span data-stu-id="94ba8-121"><span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD\_APPLY\_SAVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-122">Salvare l'elemento del desktop.</span><span class="sxs-lookup"><span data-stu-id="94ba8-122">Save the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-123"><span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP \_ elem \_ All**</span><span class="sxs-lookup"><span data-stu-id="94ba8-123"><span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP\_ELEM\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-124">Aggregazione dei valori di COMP \_ elem \_ \* .</span><span class="sxs-lookup"><span data-stu-id="94ba8-124">Aggregate of the COMP\_ELEM\_\* values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-125"><span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**\_Verifica elem \_ comp**</span><span class="sxs-lookup"><span data-stu-id="94ba8-125"><span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**COMP\_ELEM\_CHECKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-126">L'elemento è stato selezionato.</span><span class="sxs-lookup"><span data-stu-id="94ba8-126">The item has been checked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-127"><span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**\_CURITEMSTATE comp elem \_**</span><span class="sxs-lookup"><span data-stu-id="94ba8-127"><span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP\_ELEM\_CURITEMSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-128">Stato corrente dell'elemento del desktop.</span><span class="sxs-lookup"><span data-stu-id="94ba8-128">The current state of the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-129"><span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMPy \_ elem \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="94ba8-129"><span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP\_ELEM\_FRIENDLYNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-130">Nome descrittivo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="94ba8-130">The friendly name of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-131"><span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP \_ elem \_ NoScroll**</span><span class="sxs-lookup"><span data-stu-id="94ba8-131"><span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP\_ELEM\_NOSCROLL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-132">L'elemento non è scorrevole.</span><span class="sxs-lookup"><span data-stu-id="94ba8-132">The item is not scrollable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-133"><span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP \_ elem \_ Original \_ CSI**</span><span class="sxs-lookup"><span data-stu-id="94ba8-133"><span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP\_ELEM\_ORIGINAL\_CSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-134">Informazioni sullo stato dell'elemento desktop originale.</span><span class="sxs-lookup"><span data-stu-id="94ba8-134">The original desktop item state information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-135"><span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**\_ \_ sinistra POS comp \_ elem**</span><span class="sxs-lookup"><span data-stu-id="94ba8-135"><span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP\_ELEM\_POS\_LEFT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-136">Posizione orizzontale dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="94ba8-136">The horizontal position of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-137"><span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP \_ elem \_ POS \_ Top**</span><span class="sxs-lookup"><span data-stu-id="94ba8-137"><span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP\_ELEM\_POS\_TOP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-138">Posizione verticale dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="94ba8-138">The vertical position of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-139"><span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**\_ZINDEX comp elem \_ POS \_**</span><span class="sxs-lookup"><span data-stu-id="94ba8-139"><span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP\_ELEM\_POS\_ZINDEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-140">Indice z dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="94ba8-140">The z-index of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-141"><span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP \_ elem \_ restorted \_ CSI**</span><span class="sxs-lookup"><span data-stu-id="94ba8-141"><span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP\_ELEM\_RESTORED\_CSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-142">Informazioni sullo stato dell'elemento desktop ripristinato.</span><span class="sxs-lookup"><span data-stu-id="94ba8-142">The restored desktop item state information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-143"><span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**\_ \_ Altezza dimensione comp \_ elem**</span><span class="sxs-lookup"><span data-stu-id="94ba8-143"><span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**COMP\_ELEM\_SIZE\_HEIGHT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-144">Altezza dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="94ba8-144">The height of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-145"><span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**\_ \_ lunghezza dimensioni elem \_ comp**</span><span class="sxs-lookup"><span data-stu-id="94ba8-145"><span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**COMP\_ELEM\_SIZE\_WIDTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-146">Larghezza dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="94ba8-146">The width of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-147"><span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**\_origine elem \_ comp**</span><span class="sxs-lookup"><span data-stu-id="94ba8-147"><span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**COMP\_ELEM\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-148">Origine originale dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="94ba8-148">The original source of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-149"><span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**tipo di COMP \_ elem \_**</span><span class="sxs-lookup"><span data-stu-id="94ba8-149"><span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**COMP\_ELEM\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-150">Tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="94ba8-150">The item type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-151"><span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**\_CFHTML di tipo Comp \_**</span><span class="sxs-lookup"><span data-stu-id="94ba8-151"><span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**COMP\_TYPE\_CFHTML**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-152">Formato HTML compresso.</span><span class="sxs-lookup"><span data-stu-id="94ba8-152">Compressed format HTML.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-153"><span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**\_controllo tipo \_ comp**</span><span class="sxs-lookup"><span data-stu-id="94ba8-153"><span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**COMP\_TYPE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-154">L'elemento è un controllo.</span><span class="sxs-lookup"><span data-stu-id="94ba8-154">The item is a control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-155"><span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**\_htmldoc di tipo Comp \_**</span><span class="sxs-lookup"><span data-stu-id="94ba8-155"><span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**COMP\_TYPE\_HTMLDOC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-156">L'elemento è un documento HTML.</span><span class="sxs-lookup"><span data-stu-id="94ba8-156">The item is an HTML document.</span></span> <span data-ttu-id="94ba8-157">Questo flag deve essere usato solo quando è strettamente necessario.</span><span class="sxs-lookup"><span data-stu-id="94ba8-157">This flag should only be used when absolutely necessary.</span></span> <span data-ttu-id="94ba8-158">In questo modo, un documento HTML viene inserito Verbatim nel file desktop. htt utilizzato per controllare il layout del desktop.</span><span class="sxs-lookup"><span data-stu-id="94ba8-158">It causes an HTML document to be inserted verbatim into the Desktop.htt file used to control layout of the desktop.</span></span> <span data-ttu-id="94ba8-159">Per la maggior parte dei casi, è consigliabile usare il flag \* \* \* \* COMP \_ Type \_ website \* \* \* \* per aggiungere elementi al desktop.</span><span class="sxs-lookup"><span data-stu-id="94ba8-159">For most cases, you should use the \*\*\*\*COMP\_TYPE\_WEBSITE\*\*\*\* flag to add items to the desktop.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-160"><span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**tipo di COMP \_ \_ Max**</span><span class="sxs-lookup"><span data-stu-id="94ba8-160"><span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**COMP\_TYPE\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-161">Valore massimo di un flag di \_ tipo Comp \_ \* .</span><span class="sxs-lookup"><span data-stu-id="94ba8-161">The maximum value of a COMP\_TYPE\_\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-162"><span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**\_immagine del tipo di comp \_**</span><span class="sxs-lookup"><span data-stu-id="94ba8-162"><span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**COMP\_TYPE\_PICTURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-163">L'elemento è un'immagine.</span><span class="sxs-lookup"><span data-stu-id="94ba8-163">The item is a picture.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-164"><span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**\_sito Web del tipo di comp \_**</span><span class="sxs-lookup"><span data-stu-id="94ba8-164"><span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**COMP\_TYPE\_WEBSITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-165">L'elemento è un sito Web.</span><span class="sxs-lookup"><span data-stu-id="94ba8-165">The item is a website.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-166"><span id="COMPONENT_TOP"></span><span id="component_top"></span>**COMPONENTE \_ superiore**</span><span class="sxs-lookup"><span data-stu-id="94ba8-166"><span id="COMPONENT_TOP"></span><span id="component_top"></span>**COMPONENT\_TOP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-167">Valore dell'ordine z che indica che l'elemento si trova nella parte superiore.</span><span class="sxs-lookup"><span data-stu-id="94ba8-167">A z-order value meaning the item is at the top.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-168"><span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**\_centro WPSTYLE**</span><span class="sxs-lookup"><span data-stu-id="94ba8-168"><span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**WPSTYLE\_CENTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-169">Lo sfondo è centrato.</span><span class="sxs-lookup"><span data-stu-id="94ba8-169">The wallpaper is centered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-170"><span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE \_ Max**</span><span class="sxs-lookup"><span data-stu-id="94ba8-170"><span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-171">Valore massimo di un flag WPSTYLE \_ \* .</span><span class="sxs-lookup"><span data-stu-id="94ba8-171">The maximum value of a WPSTYLE\_\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-172"><span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**\_estensione WPSTYLE**</span><span class="sxs-lookup"><span data-stu-id="94ba8-172"><span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE\_STRETCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-173">Lo sfondo viene allungato per adattarsi all'intero schermo.</span><span class="sxs-lookup"><span data-stu-id="94ba8-173">The wallpaper is stretched to fit the entire screen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-174"><span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**\_riquadro WPSTYLE**</span><span class="sxs-lookup"><span data-stu-id="94ba8-174"><span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**WPSTYLE\_TILE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-175">Lo sfondo è affiancato.</span><span class="sxs-lookup"><span data-stu-id="94ba8-175">The wallpaper is tiled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94ba8-176"><span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**WPSTYLE \_ span**</span><span class="sxs-lookup"><span data-stu-id="94ba8-176"><span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**WPSTYLE\_SPAN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94ba8-177">**Windows 8 e versioni successive**: lo sfondo si estende su più monitor.</span><span class="sxs-lookup"><span data-stu-id="94ba8-177">**Windows 8 and later**: The wallpaper spans multiple monitors.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94ba8-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94ba8-178">Requirements</span></span>



| <span data-ttu-id="94ba8-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="94ba8-179">Requirement</span></span> | <span data-ttu-id="94ba8-180">Valore</span><span class="sxs-lookup"><span data-stu-id="94ba8-180">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="94ba8-181">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94ba8-181">Header</span></span><br/> | <dl> <span data-ttu-id="94ba8-182"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="94ba8-182"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
