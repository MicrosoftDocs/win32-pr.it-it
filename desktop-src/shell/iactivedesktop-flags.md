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
# <a name="iactivedesktop-flags"></a>Flag IActiveDesktop

In questa sezione vengono descritti i flag utilizzati dai metodi dell'interfaccia [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .

<dl> <dt>

<span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD \_ apply \_ All**
</dt> <dd> <dl> <dt>



Aggregazione di * * * * AD \_ apply \_ Save * * * *, * * * * ad \_ apply \_ HTMLGEN * * * * e * * * * ad \_ apply \_ Refresh * * * * values.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD \_ applicare l' \_ aggiornamento memorizzato nel buffer \_**
</dt> <dd> <dl> <dt>



Avvia un timer e aggrega tutte le richieste di aggiornamento effettuate con questo flag durante tale intervallo di tempo in un singolo aggiornamento. Questo intervallo è impostato su cinque secondi. Alla fine dell'intervallo o se viene richiesto un aggiornamento durante l'intervallo senza un flag * * * * AD \_ apply \_ buffered \_ Refresh * * * *, l'aggiornamento viene eseguito e il timer viene arrestato. Questo flag deve essere combinato con il flag * * * * AD \_ apply \_ Refresh * * * *.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD \_ apply \_ DYNAMICREFRESH**
</dt> <dd> <dl> <dt>



[Versione 5,0](versions.md). Usare il codice HTML dinamico per aggiornare solo gli elementi che sono stati modificati dopo l'ultimo aggiornamento, non l'intero desktop.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**AD \_ apply \_ Force**
</dt> <dd> <dl> <dt>



Forzare una modifica del desktop attivo.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD \_ apply \_ HTMLGEN**
</dt> <dd> <dl> <dt>



Rigenerare il file HTML del desktop.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**AD \_ apply \_ Refresh**
</dt> <dd> <dl> <dt>



Aggiornare l'elemento del desktop.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD \_ apply \_ Save**
</dt> <dd> <dl> <dt>



Salvare l'elemento del desktop.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP \_ elem \_ All**
</dt> <dd> <dl> <dt>



Aggregazione dei valori di COMP \_ elem \_ \* .


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**\_Verifica elem \_ comp**
</dt> <dd> <dl> <dt>



L'elemento è stato selezionato.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**\_CURITEMSTATE comp elem \_**
</dt> <dd> <dl> <dt>



Stato corrente dell'elemento del desktop.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMPy \_ elem \_ FriendlyName**
</dt> <dd> <dl> <dt>



Nome descrittivo dell'elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP \_ elem \_ NoScroll**
</dt> <dd> <dl> <dt>



L'elemento non è scorrevole.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP \_ elem \_ Original \_ CSI**
</dt> <dd> <dl> <dt>



Informazioni sullo stato dell'elemento desktop originale.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**\_ \_ sinistra POS comp \_ elem**
</dt> <dd> <dl> <dt>



Posizione orizzontale dell'elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP \_ elem \_ POS \_ Top**
</dt> <dd> <dl> <dt>



Posizione verticale dell'elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**\_ZINDEX comp elem \_ POS \_**
</dt> <dd> <dl> <dt>



Indice z dell'elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP \_ elem \_ restorted \_ CSI**
</dt> <dd> <dl> <dt>



Informazioni sullo stato dell'elemento desktop ripristinato.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**\_ \_ Altezza dimensione comp \_ elem**
</dt> <dd> <dl> <dt>



Altezza dell'elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**\_ \_ lunghezza dimensioni elem \_ comp**
</dt> <dd> <dl> <dt>



Larghezza dell'elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**\_origine elem \_ comp**
</dt> <dd> <dl> <dt>



Origine originale dell'elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**tipo di COMP \_ elem \_**
</dt> <dd> <dl> <dt>



Tipo di elemento.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**\_CFHTML di tipo Comp \_**
</dt> <dd> <dl> <dt>



Formato HTML compresso.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**\_controllo tipo \_ comp**
</dt> <dd> <dl> <dt>



L'elemento è un controllo.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**\_htmldoc di tipo Comp \_**
</dt> <dd> <dl> <dt>



L'elemento è un documento HTML. Questo flag deve essere usato solo quando è strettamente necessario. In questo modo, un documento HTML viene inserito Verbatim nel file desktop. htt utilizzato per controllare il layout del desktop. Per la maggior parte dei casi, è consigliabile usare il flag * * * * COMP \_ Type \_ website * * * * per aggiungere elementi al desktop.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**tipo di COMP \_ \_ Max**
</dt> <dd> <dl> <dt>



Valore massimo di un flag di \_ tipo Comp \_ \* .


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**\_immagine del tipo di comp \_**
</dt> <dd> <dl> <dt>



L'elemento è un'immagine.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**\_sito Web del tipo di comp \_**
</dt> <dd> <dl> <dt>



L'elemento è un sito Web.


</dt> </dl> </dd> <dt>

<span id="COMPONENT_TOP"></span><span id="component_top"></span>**COMPONENTE \_ superiore**
</dt> <dd> <dl> <dt>



Valore dell'ordine z che indica che l'elemento si trova nella parte superiore.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**\_centro WPSTYLE**
</dt> <dd> <dl> <dt>



Lo sfondo è centrato.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE \_ Max**
</dt> <dd> <dl> <dt>



Valore massimo di un flag WPSTYLE \_ \* .


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**\_estensione WPSTYLE**
</dt> <dd> <dl> <dt>



Lo sfondo viene allungato per adattarsi all'intero schermo.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**\_riquadro WPSTYLE**
</dt> <dd> <dl> <dt>



Lo sfondo è affiancato.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**WPSTYLE \_ span**
</dt> <dd> <dl> <dt>



**Windows 8 e versioni successive**: lo sfondo si estende su più monitor.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
