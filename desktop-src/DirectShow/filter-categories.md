---
description: Nelle tabelle seguenti sono elencati i CLSID per le DirectShow filtro.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Filtrare le categorie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf3fec6c2d05e1ac82dc116dbcf2d2b1d51437747bbbd45c63f7b56440d003ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639521"
---
# <a name="filter-categories"></a>Filtrare le categorie

Nelle tabelle seguenti sono elencati i CLSID per le DirectShow filtro.

-   [DirectShow Filtrare le categorie](#directshow-filter-categories)
-   [Altre categorie di filtri](#other-filter-categories)
-   [DirectShow Filtra metacate categorie](#directshow-filter-meta-category)
-   [DMO Categorie](#dmo-categories)
-   [Argomenti correlati](#related-topics)

## <a name="directshow-filter-categories"></a>DirectShow Filtrare le categorie

Le categorie elencate di seguito vengono enumerate da [Filter Mapper.](filter-mapper.md) Per impostazione predefinita, tuttavia, il filtro mapper ignora le categorie con meriti di MERITO \_ NON \_ USARE o \_ meno. Per altre informazioni, vedere [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters). Tutte le categorie elencate qui possono essere enumerate anche con [l'enumeratore dispositivo di sistema](system-device-enumerator.md).

Le categorie seguenti sono dichiarate in Uuids.h. Includere il file di intestazione Dshow.h.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome descrittivo</th>
<th>CLSID</th>
<th>Merito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Origini di acquisizione audio</td>
<td><strong>CLSID_AudioInputDeviceCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Compresse audio</td>
<td><strong>CLSID_AudioCompressorCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Renderer audio</td>
<td><strong>CLSID_AudioRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Filtri di controllo dispositivo</td>
<td><strong>CLSID_DeviceControlCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>DirectShow Filtri</td>
<td><strong>CLSID_LegacyAmFilterCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Renderer esterni</td>
<td><strong>CLSID_TransmitCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Renderer Midi</td>
<td><strong>CLSID_MidiRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Origini di acquisizione video</td>
<td><strong>CLSID_VideoInputDeviceCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Compresse video</td>
<td><strong>CLSID_VideoCompressorCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Dispositivi di decompressione dei flussi WDM</td>
<td><strong>CLSID_DVDHWDecodersCategory</strong>
<blockquote>
[!Note]<br />
Questa categoria contiene decodificatori DVD hardware.
</blockquote>
<br/></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Dispositivi di acquisizione di streaming WDM</td>
<td><strong>AM_KSCATEGORY_CAPTURE</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Dispositivi crossbar di streaming WDM</td>
<td><strong>AM_KSCATEGORY_CROSSBAR</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Dispositivi di rendering di streaming WDM</td>
<td><strong>AM_KSCATEGORY_RENDER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Dispositivi WDM Streaming Tee/Splitter</td>
<td><strong>AM_KSCATEGORY_SPLITTER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Dispositivi audio WDM Streaming TV</td>
<td><strong>AM_KSCATEGORY_TVAUDIO</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Dispositivi di siner TV di streaming WDM</td>
<td><strong>AM_KSCATEGORY_TVTUNER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Codec VBI di streaming WDM</td>
<td><strong>AM_KSCATEGORY_VBICODEC</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
</tbody>
</table>



 

Le categorie seguenti sono dichiarate nel file di intestazione Ks.h.



| Nome descrittivo                          | CLSID                                   | Merito                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| Trasformazioni di comunicazione in streaming WDM | **KSCATEGORY \_ COMMUNICATIONSTRANSFORM** | **MERITO \_ NON \_ \_ USARE** |
| Trasformazioni dei dati di streaming WDM          | **KSCATEGORY \_ DATATRANSFORM**           | **MERITO \_ NON \_ \_ USARE** |
| Trasformazioni dell'interfaccia di streaming WDM     | **KSCATEGORY \_ INTERFACETRANSFORM**      | **MERITO \_ NON \_ \_ USARE** |
| Dispositivi di streaming WDM Mixer dispositivi            | **KSCATEGORY \_ MIXER**                   | **MERITO \_ NON \_ \_ USARE** |



 

Le categorie seguenti sono dichiarate nel file di intestazione Bdamedia.h. Includere i file di intestazione seguenti: ks.h, ksmedia.h e bdamedia.h.



| Nome descrittivo                       | CLSID                                       | Merito                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| Provider di rete BDA               | **PROVIDER DI RETE \_ KSCATEGORY BDA \_ \_**      | **MERITO \_ NORMALE**       |
| Componenti ricevitore BDA             | **COMPONENTE \_ RICEVITORE KSCATEGORY BDA \_ \_**    | **MERITO \_ NON \_ \_ USARE** |
| Filtri di rendering BDA               | **KSCATEGORY \_ IP \_ SINK**                    | **MERITO \_ NON \_ \_ USARE** |
| Filtri di origine BDA                  | **SINER DI RETE \_ KSCATEGORY BDA \_ \_**         | **MERITO \_ NON \_ \_ USARE** |
| Renderer di informazioni sul trasporto BDA | **INFORMAZIONI SUL TRASPORTO DI KSCATEGORY \_ BDA \_ \_** | **MERITO \_ NORMALE**       |



 

> [!Note]  
> I decodificatori vengono registrati nella categoria "filtri DirectShow" (CLSID \_ LegacyAmFilterCategory).

 

## <a name="other-filter-categories"></a>Altre categorie di filtri

Le categorie elencate di seguito possono essere enumerate con l'enumeratore dispositivo di sistema, ma non sono visibili a Filter Mapper e non vengono usate da [Intelligent Connessione](intelligent-connect.md).

Le categorie seguenti vengono dichiarate nel file di intestazione Qedit.h.



| Nome descrittivo            | Interfaccia della riga di comando                             | Merito                   |
|--------------------------|----------------------------------|-------------------------|
| Effetti video (1 input)  | **CLSID \_ VideoEffects1Category** | **MERITO \_ NON \_ \_ USARE** |
| Effetti video (2 input) | **CLSID \_ VideoEffects2Category** | **MERITO \_ NON \_ \_ USARE** |



 

Queste categorie contengono effetti video e transizioni per [i DirectShow di modifica:](directshow-editing-services.md)

-   "Effetti video (1 input)" contiene effetti video.
-   "Effetti video (2 input)" contiene transizioni video.

Per altre informazioni, vedere [Enumerazione di effetti e transizioni](enumerating-effects-and-transitions.md).

Le categorie seguenti sono dichiarate nel file di intestazione Uuids.h. Includere il file di intestazione Dshow.h.



| Nome descrittivo       | Interfaccia della riga di comando                                | Merito                   |
|---------------------|-------------------------------------|-------------------------|
| Codificatori EncAPI     | **CLSID \_ MediaEncoderCategory**     | **MERITO \_ NON \_ \_ USARE** |
| Multiplexer EncAPI | **CLSID \_ MediaMultiplexerCategory** | **MERITO \_ NON \_ \_ USARE** |



 

## <a name="directshow-filter-meta-category"></a>DirectShow Filtrare Meta-Category



| Nome descrittivo                 | CLSID                            | Merito          |
|-------------------------------|----------------------------------|----------------|
| Categorie di filtri ActiveMovie | **CLSID \_ ActiveMovieCategories** | Non applicabile |



 

Questa metacatema contiene un elenco di categorie di filtri. Se all'interno di questo elenco non viene visualizzata una categoria di [filtri,](intelligent-connect.md)il [mapper](filter-mapper.md) dei filtri ignora la categoria, ovvero il filtro non è disponibile per Intelligent Connessione .

Per enumerare l'elenco di categorie di filtri, chiamare [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con il valore CLSID \_ ActiveMovieCategories. I moniker restituiti da questo metodo supportano le proprietà seguenti.



| Nome proprietà  | Descrizione                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| "FriendlyName" | Nome categoria (VT \_ BSTR).                                                              |
| "Merito"        | Merito della categoria (VT \_ I4). Se questa proprietà è assente, considerare come **MERIT \_ DO NOT \_ \_ USE**. |
| "CLSID"        | CLSID di categoria (VT \_ BSTR).                                                             |



 

Per aggiungere una nuova categoria di filtro a questo elenco, chiamare [**IFilterMapper2::CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).

## <a name="dmo-categories"></a>DMO Categorie

DirectX Media Objects (DMO) usa un meccanismo di enumerazione diverso da DirectShow filtri. Per altre informazioni, vedere [Registrazione di un DMO](registering-a-dmo.md). Tuttavia, è possibile usare l'enumeratore del dispositivo di sistema per enumerare DMO categorie. I moniker vengono associati al filtro [wrapper DMO](dmo-wrapper-filter.md) e inizializzano automaticamente il filtro con il DMO.

Inoltre, alcune delle categorie DMO vengono mappate DirectShow categorie di filtro ai fini della connessione intelligente:



| DMO Categoria                    | DirectShow Equivalente              |
|---------------------------------|------------------------------------|
| **CODIFICATORE AUDIO DMOCATEGORY \_ \_** | **CLSID \_ AudioCompressorCategory** |
| **DECODIFICATORE AUDIO DMOCATEGORY \_ \_** | **CLSID \_ LegacyAmFilterCategory**  |
| **CODIFICATORE VIDEO DMOCATEGORY \_ \_** | **CLSID \_ VideoCompressorCategory** |
| **DECODIFICATORE VIDEO DMOCATEGORY \_ \_** | **CLSID \_ LegacyAmFilterCategory**  |



 

Si noti che l'effetto video e le categorie di effetti audio non vengono mappati ad alcuna DirectShow categorie.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti e GUID](constants-and-guids.md)
</dt> <dt>

[Enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md)
</dt> <dt>

[Gestione Connessione](intelligent-connect.md)
</dt> <dt>

[Layout delle chiavi del Registro di sistema](layout-of-the-registry-keys.md)
</dt> <dt>

[Uso di Filter Mapper](using-the-filter-mapper.md)
</dt> <dt>

[Uso dell'enumeratore del dispositivo di sistema](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




