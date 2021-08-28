---
description: Nelle tabelle seguenti sono elencati i CLSID per le DirectShow di filtro.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Categorie di filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4e8c2b5e5f9e477633774cb24e707aa9d71060
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476327"
---
# <a name="filter-categories"></a>Categorie di filtro

Nelle tabelle seguenti sono elencati i CLSID per le DirectShow di filtro.

-   [DirectShow Categorie di filtro](#directshow-filter-categories)
-   [Altre categorie di filtro](#other-filter-categories)
-   [DirectShow Filtra metacate categorie](#directshow-filter-meta-category)
-   [DMO Categorie](#dmo-categories)
-   [Argomenti correlati](#related-topics)

## <a name="directshow-filter-categories"></a>DirectShow Categorie di filtro

Le categorie elencate di seguito vengono enumerate da [Filter Mapper](filter-mapper.md). Per impostazione predefinita, tuttavia, Il mapper di filtri ignora le categorie con i vantaggi di NON \_ \_ USARE o \_ meno. Per altre informazioni, vedere [**IFilterMapper2::EnumMatchingFilters.**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) Tutte le categorie elencate di seguito possono essere enumerate anche con System [Device Enumerator](system-device-enumerator.md).

Le categorie seguenti sono dichiarate in Uuids.h. Includere il file di intestazione Dshow.h.




| Nome descrittivo | CLSID | Merito | 
|---------------|-------|-------|
| Origini di acquisizione audio | <strong>CLSID_AudioInputDeviceCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Audio Compressors | <strong>CLSID_AudioCompressorCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Renderer audio | <strong>CLSID_AudioRendererCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Filtri di controllo dei dispositivi | <strong>CLSID_DeviceControlCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| DirectShow Filtri | <strong>CLSID_LegacyAmFilterCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Renderer esterni | <strong>CLSID_TransmitCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Renderer Midi | <strong>CLSID_MidiRendererCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Origini di acquisizione video | <strong>CLSID_VideoInputDeviceCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Video Concis | <strong>CLSID_VideoCompressorCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivi di decompressione del flusso WDM | <strong>CLSID_DVDHWDecodersCategory</strong><blockquote>[!Note]<br />Questa categoria contiene decodificatori DVD hardware.</blockquote><br /> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivi di acquisizione di streaming WDM | <strong>AM_KSCATEGORY_CAPTURE</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivi wdm streaming crossbar | <strong>AM_KSCATEGORY_CROSSBAR</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Dispositivi di rendering di streaming WDM | <strong>AM_KSCATEGORY_RENDER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM Streaming Tee/Splitter Devices | <strong>AM_KSCATEGORY_SPLITTER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM Streaming TV Audio Devices | <strong>AM_KSCATEGORY_TVAUDIO</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM Streaming TV Tuner Devices | <strong>AM_KSCATEGORY_TVTUNER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Codec VBI di streaming WDM | <strong>AM_KSCATEGORY_VBICODEC</strong> | <strong>MERIT_DO_NOT_USE</strong> | 




 

Le categorie seguenti vengono dichiarate nel file di intestazione Ks.h.



| Nome descrittivo                          | CLSID                                   | Merito                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| Trasformazioni delle comunicazioni di streaming WDM | **KSCATEGORY \_ COMMUNICATIONSTRANSFORM** | **NON \_ \_ USARE \_** |
| Trasformazioni dei dati di streaming WDM          | **KSCATEGORY \_ DATATRANSFORM**           | **NON \_ \_ USARE \_** |
| Trasformazioni dell'interfaccia di streaming WDM     | **KSCATEGORY \_ INTERFACETRANSFORM**      | **NON \_ \_ USARE \_** |
| WdM Streaming Mixer Devices            | **KSCATEGORY \_ MIXER**                   | **NON \_ \_ USARE \_** |



 

Le categorie seguenti vengono dichiarate nel file di intestazione Bdamedia.h. Includere i file di intestazione seguenti: ks.h, ksmedia.h e bdamedia.h.



| Nome descrittivo                       | CLSID                                       | Merito                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| Provider di rete BDA               | **PROVIDER DI RETE KSCATEGORY \_ BDA \_ \_**      | **MERIT \_ NORMAL**       |
| Componenti ricevitore BDA             | **COMPONENTE \_ RICEVITORE KSCATEGORY BDA \_ \_**    | **NON \_ \_ USARE \_** |
| Filtri di rendering BDA               | **KSCATEGORY \_ IP \_ SINK**                    | **NON \_ \_ USARE \_** |
| Filtri di origine BDA                  | **TUNER DI RETE KSCATEGORY \_ BDA \_ \_**         | **NON \_ \_ USARE \_** |
| Renderer di informazioni sul trasporto BDA | **INFORMAZIONI SUL TRASPORTO \_ KSCATEGORY BDA \_ \_** | **MERIT \_ NORMAL**       |



 

> [!Note]  
> I decodificatori vengono registrati nella categoria "filtri DirectShow" (CLSID \_ LegacyAmFilterCategory).

 

## <a name="other-filter-categories"></a>Altre categorie di filtro

Le categorie elencate di seguito possono essere enumerate con System Device Enumerator, ma non sono visibili a Filter Mapper e non vengono usate da [Intelligent Connessione](intelligent-connect.md).

Le categorie seguenti vengono dichiarate nel file di intestazione Qedit.h.



| Nome descrittivo            | CLID                             | Merito                   |
|--------------------------|----------------------------------|-------------------------|
| Effetti video (1 input)  | **CLSID \_ VideoEffects1Category** | **NON \_ \_ USARE \_** |
| Effetti video (2 input) | **CLSID \_ VideoEffects2Category** | **NON \_ \_ USARE \_** |



 

Queste categorie contengono effetti video e transizioni per i [DirectShow di modifica:](directshow-editing-services.md)

-   "Effetti video (1 input)" contiene effetti video.
-   "Effetti video (2 input)" contiene transizioni video.

Per altre informazioni, vedere [Enumerazione di effetti e transizioni.](enumerating-effects-and-transitions.md)

Le categorie seguenti vengono dichiarate nel file di intestazione Uuids.h. Includere il file di intestazione Dshow.h.



| Nome descrittivo       | CLID                                | Merito                   |
|---------------------|-------------------------------------|-------------------------|
| Codificatori EncAPI     | **CLSID \_ MediaEncoderCategory**     | **NON \_ \_ USARE \_** |
| Multiplexer EncAPI | **CLSID \_ MediaMultiplexerCategory** | **NON \_ \_ USARE \_** |



 

## <a name="directshow-filter-meta-category"></a>DirectShow Filtro Meta-Category



| Nome descrittivo                 | CLSID                            | Merito          |
|-------------------------------|----------------------------------|----------------|
| Categorie di filtri ActiveMovie | **CLSID \_ ActiveMovieCategories** | Non applicabile |



 

Questa metacate categorie contiene un elenco di categorie di filtri. Se una categoria di filtro non viene visualizzata all'interno di questo elenco, il [mapper](filter-mapper.md) di filtri la [ignora,](intelligent-connect.md)ovvero il filtro non è disponibile per l'Connessione .

Per enumerare l'elenco delle categorie di filtri, chiamare [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con il valore CLSID \_ ActiveMovieCategories. I moniker restituiti da questo metodo supportano le proprietà seguenti.



| Nome proprietà  | Descrizione                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| "FriendlyName" | Nome categoria (VT \_ BSTR).                                                              |
| "Merito"        | Categoria di vantaggi (VT \_ I4). Se questa proprietà è assente, considerare come **NON \_ \_ USARE \_ .** |
| "CLSID"        | CLSID di categoria (VT \_ BSTR).                                                             |



 

Per aggiungere una nuova categoria di filtro a questo elenco, chiamare [**IFilterMapper2::CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).

## <a name="dmo-categories"></a>DMO Categorie

Gli oggetti multimediali DirectX (DMO) usano un meccanismo di enumerazione diverso DirectShow filtri. Per altre informazioni, vedere [Registrazione di un DMO](registering-a-dmo.md). È tuttavia possibile usare System Device Enumerator per enumerare DMO categorie. I moniker vengono associati al filtro [wrapper DMO](dmo-wrapper-filter.md) e inizializzano automaticamente il filtro con il DMO.

Viene inoltre eseguito il mapping di DMO categorie di filtri DirectShow ai fini della connessione intelligente:



| DMO Categoria                    | DirectShow Equivalente              |
|---------------------------------|------------------------------------|
| **CODIFICATORE AUDIO DMOCATEGORY \_ \_** | **CLSID \_ AudioCompressorCategory** |
| **DECODIFICATORE AUDIO DMOCATEGORY \_ \_** | **CLSID \_ LegacyAmFilterCategory**  |
| **CODIFICATORE \_ VIDEO \_ DMOCATEGORY** | **CLSID \_ VideoCompressorCategory** |
| **DECODIFICATORE VIDEO DMOCATEGORY \_ \_** | **CLSID \_ LegacyAmFilterCategory**  |



 

Si noti che le categorie di effetti video e audio non vengono mappate ad alcuna DirectShow categorie.

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

[Uso del mapper di filtri](using-the-filter-mapper.md)
</dt> <dt>

[Utilizzo dell'enumeratore dispositivo di sistema](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




