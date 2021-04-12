---
description: Nelle tabelle seguenti sono elencati i CLSID per le categorie di filtro DirectShow.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Filtra categorie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4ccb9443c405abcbd0b9afbd406d6faf2558a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401079"
---
# <a name="filter-categories"></a>Filtra categorie

Nelle tabelle seguenti sono elencati i CLSID per le categorie di filtro DirectShow.

-   [Categorie filtro DirectShow](#directshow-filter-categories)
-   [Altre categorie di filtro](#other-filter-categories)
-   [Meta-categoria del filtro DirectShow](#directshow-filter-meta-category)
-   [Categorie DMO](#dmo-categories)
-   [Argomenti correlati](#related-topics)

## <a name="directshow-filter-categories"></a>Categorie filtro DirectShow

Le categorie elencate di seguito vengono enumerate dal [mapper dei filtri](filter-mapper.md). Per impostazione predefinita, tuttavia, il mapper dei filtri ignora le categorie con meriti di \_ merito \_ non \_ usare o meno. Per ulteriori informazioni, vedere [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters). Tutte le categorie elencate di seguito possono essere enumerate anche con l' [enumeratore di dispositivo di sistema](system-device-enumerator.md).

Le categorie seguenti sono dichiarate in UUIDs. h. Includere il file di intestazione dshow. h.



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
<td>Commediatori audio</td>
<td><strong>CLSID_AudioCompressorCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Renderer audio</td>
<td><strong>CLSID_AudioRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Filtri di controllo del dispositivo</td>
<td><strong>CLSID_DeviceControlCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Filtri DirectShow</td>
<td><strong>CLSID_LegacyAmFilterCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Renderer esterni</td>
<td><strong>CLSID_TransmitCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Renderer MIDI</td>
<td><strong>CLSID_MidiRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Origini acquisizione video</td>
<td><strong>CLSID_VideoInputDeviceCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Compressione video</td>
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
<td>Dispositivi traversa di streaming WDM</td>
<td><strong>AM_KSCATEGORY_CROSSBAR</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Dispositivi di rendering di streaming WDM</td>
<td><strong>AM_KSCATEGORY_RENDER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Dispositivi t/Splitter streaming WDM</td>
<td><strong>AM_KSCATEGORY_SPLITTER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Dispositivi audio WDM Streaming TV</td>
<td><strong>AM_KSCATEGORY_TVAUDIO</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Dispositivi sintonizzatore streaming TV WDM</td>
<td><strong>AM_KSCATEGORY_TVTUNER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Codec VBI per flussi WDM</td>
<td><strong>AM_KSCATEGORY_VBICODEC</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
</tbody>
</table>



 

Le seguenti categorie sono dichiarate nel file di intestazione KS. h.



| Nome descrittivo                          | CLSID                                   | Merito                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| Trasformazioni di comunicazione WDM Streaming | **\_COMMUNICATIONSTRANSFORM KSCATEGORY** | **il merito non viene \_ \_ \_ utilizzato** |
| Trasformazioni di dati di streaming WDM          | **KSCATEGORY \_ DATAtransform**           | **il merito non viene \_ \_ \_ utilizzato** |
| Trasformazioni dell'interfaccia di streaming WDM     | **\_INTERFACETRANSFORM KSCATEGORY**      | **il merito non viene \_ \_ \_ utilizzato** |
| Dispositivi mixer di streaming WDM            | **\_mixer KSCATEGORY**                   | **il merito non viene \_ \_ \_ utilizzato** |



 

Le seguenti categorie sono dichiarate nel file di intestazione Bdamedia. h. Includere i file di intestazione seguenti: KS. h, ksmedia. h e bdamedia. h.



| Nome descrittivo                       | CLSID                                       | Merito                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| Provider di rete BDA               | **\_provider di \_ rete \_ BDA KSCATEGORY**      | **VALORE \_ normale**       |
| Componenti ricevitore BDA             | **\_ \_ componente ricevitore BDA \_ KSCATEGORY**    | **il merito non viene \_ \_ \_ utilizzato** |
| Filtri per il rendering BDA               | **\_sink IP \_ KSCATEGORY**                    | **il merito non viene \_ \_ \_ utilizzato** |
| Filtri origine BDA                  | **\_Tuner di \_ rete \_ BDA KSCATEGORY**         | **il merito non viene \_ \_ \_ utilizzato** |
| Renderer delle informazioni di trasporto BDA | **\_ \_ informazioni sul trasporto BDA KSCATEGORY \_** | **VALORE \_ normale**       |



 

> [!Note]  
> I decodificatori sono registrati nella categoria "filtri DirectShow" (CLSID \_ LegacyAmFilterCategory).

 

## <a name="other-filter-categories"></a>Altre categorie di filtro

Le categorie elencate di seguito possono essere enumerate con l'enumeratore del dispositivo di sistema, ma non sono visibili al mapper dei filtri e non vengono usate da [Intelligent Connect](intelligent-connect.md).

Le seguenti categorie sono dichiarate nel file di intestazione qedit. h.



| Nome descrittivo            | CLID                             | Merito                   |
|--------------------------|----------------------------------|-------------------------|
| Effetti video (1 input)  | **\_VIDEOEFFECTS1CATEGORY CLSID** | **il merito non viene \_ \_ \_ utilizzato** |
| Effetti video (2 input) | **\_VIDEOEFFECTS2CATEGORY CLSID** | **il merito non viene \_ \_ \_ utilizzato** |



 

Queste categorie contengono effetti video e transizioni per i [servizi di modifica DirectShow](directshow-editing-services.md):

-   "Effetti video (1 input)" contiene effetti video.
-   "Video Effects (2 input)" contiene transizioni video.

Per ulteriori informazioni, vedere [enumerazione degli effetti e delle transizioni](enumerating-effects-and-transitions.md).

Le seguenti categorie sono dichiarate nel file di intestazione UUIDs. h. Includere il file di intestazione dshow. h.



| Nome descrittivo       | CLID                                | Merito                   |
|---------------------|-------------------------------------|-------------------------|
| Codificatori     | **\_MEDIAENCODERCATEGORY CLSID**     | **il merito non viene \_ \_ \_ utilizzato** |
| Multiplexer | **\_MEDIAMULTIPLEXERCATEGORY CLSID** | **il merito non viene \_ \_ \_ utilizzato** |



 

## <a name="directshow-filter-meta-category"></a>Meta-Category filtro DirectShow



| Nome descrittivo                 | CLSID                            | Merito          |
|-------------------------------|----------------------------------|----------------|
| Categorie filtro ActiveMovie | **\_ACTIVEMOVIECATEGORIES CLSID** | Non applicabile |



 

Questa meta-categoria contiene un elenco di categorie di filtro. Se una categoria di filtri non viene visualizzata in questo elenco, il [mapper dei filtri](filter-mapper.md) ignora la categoria, il che significa che il filtro non è disponibile per la [connessione intelligente](intelligent-connect.md).

Per enumerare l'elenco di categorie di filtro, chiamare [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con il valore CLSID \_ ActiveMovieCategories. I moniker restituiti da questo metodo supportano le seguenti proprietà.



| Nome proprietà  | Descrizione                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| FriendlyName | Nome della categoria (VT \_ BSTR).                                                              |
| Merito        | Merit categoria (VT \_ I4). Se questa proprietà è assente, considerare come **Merit non \_ \_ \_ usare**. |
| CLSID        | Categoria CLSID (VT \_ BSTR).                                                             |



 

Per aggiungere una nuova categoria di filtri all'elenco, chiamare [**IFilterMapper2:: CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).

## <a name="dmo-categories"></a>Categorie DMO

Gli oggetti multimediali DirectX (DMOs) utilizzano un meccanismo di enumerazione diverso dai filtri DirectShow. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un DMO](registering-a-dmo.md). Tuttavia, è possibile usare l'enumeratore System Device per enumerare le categorie DMO. I moniker vengono associati al [filtro del wrapper DMO](dmo-wrapper-filter.md) e inizializzano automaticamente il filtro con DMO.

Inoltre, alcune categorie DMO sono mappate alle categorie di filtri DirectShow ai fini della connessione intelligente:



| Categoria DMO                    | Equivalente DirectShow              |
|---------------------------------|------------------------------------|
| **\_ \_ codificatore audio DMOCATEGORY** | **\_AUDIOCOMPRESSORCATEGORY CLSID** |
| **\_decodificatore audio DMOCATEGORY \_** | **\_LEGACYAMFILTERCATEGORY CLSID**  |
| **\_ \_ codificatore video DMOCATEGORY** | **\_VIDEOCOMPRESSORCATEGORY CLSID** |
| **\_decodificatore video DMOCATEGORY \_** | **\_LEGACYAMFILTERCATEGORY CLSID**  |



 

Si noti che le categorie effetto video e effetto audio non sono mappate ad alcuna categoria DirectShow.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti e GUID](constants-and-guids.md)
</dt> <dt>

[Enumerazione dei dispositivi e dei filtri](enumerating-devices-and-filters.md)
</dt> <dt>

[Connessione intelligente](intelligent-connect.md)
</dt> <dt>

[Layout delle chiavi del registro di sistema](layout-of-the-registry-keys.md)
</dt> <dt>

[Uso del mapper dei filtri](using-the-filter-mapper.md)
</dt> <dt>

[Uso di System Device Enumerator](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




