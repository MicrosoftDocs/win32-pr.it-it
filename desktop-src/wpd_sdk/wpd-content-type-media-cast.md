---
description: '\_cast del \_ supporto del tipo di contenuto WPD \_ \_'
ms.assetid: 368e7381-8978-421a-b450-59915f8e70e2
title: WPD_CONTENT_TYPE_MEDIA_CAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2daafb381aac802b9add130aa97e9750f30e7847
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132202"
---
# <a name="wpd_content_type_media_cast"></a>\_cast del \_ supporto del tipo di contenuto WPD \_ \_

Un oggetto che descrive il tipo come \_ \_ \_ il cast multimediale del tipo di contenuto WPD \_ rappresenta una raccolta di contenuti correlati.

Un oggetto Mediacast può essere considerato come un oggetto contenitore che raggruppa il contenuto correlato, così come una playlist di gruppi di musica. Spesso, un oggetto Mediacast viene usato per raggruppare il contenuto multimediale pubblicato online. Un canale RSS, ad esempio, può essere rappresentato come un oggetto Mediacast i cui riferimenti a oggetti puntano a oggetti contenuto che rappresentano ogni elemento nel canale.

Questo tipo di oggetto supporta le proprietà seguenti.



|                                                                                                                       |                                                                       |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **Nome della proprietà**                                                                                                     | **Obbligatorio o facoltativo**                                              |
| [\_ID oggetto \_ WPD](object-properties.md)                                                                | Obbligatorio.                                                             |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                                                 | Obbligatorio.                                                             |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                             |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md)                          | Obbligatorio.                                                             |
| [\_formato oggetto \_ WPD](object-properties.md)                                                        | Obbligatorio.                                                             |
| [\_tipo di \_ contenuto dell'oggetto WPD \_](object-properties.md)                                           | Obbligatorio.                                                             |
| [\_oggetto WPD \_ nascosto](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                     |
| [\_oggetto WPD \_](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema). |
| [\_dimensioni dell'oggetto WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto ha almeno una risorsa.                     |
| [\_ \_ \_ nome file originale oggetto \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                             |
| [\_oggetto WPD \_ non utilizzabile \_](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'utilizzo da parte del dispositivo. |
| [\_riferimenti a oggetti WPD \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.               |
| [\_parole chiave dell'oggetto WPD \_](object-properties.md)                                                    | facoltativo.                                                             |
| [\_ \_ ID sincronizzazione oggetto \_ WPD](object-properties.md)                                                     | facoltativo.                                                             |
| [\_oggetto WPD \_ \_ protetto da DRM \_](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                |
| [\_data dell'oggetto WPD \_ \_ creata](object-properties.md)                                           | facoltativo.                                                             |
| [\_data dell'oggetto WPD \_ \_ modificata](object-properties.md)                                         | Consigliato.                                                          |
| [\_ \_ Data creazione oggetto \_ WPD](object-properties.md)                                         | facoltativo.                                                             |
| [\_riferimenti all'oggetto WPD \_ \_](object-properties.md)                                     | Consigliato se un altro oggetto fa riferimento all'oggetto.            |
| [\_ \_ \_ \_ ID oggetto funzionale contenitore oggetto \_ WPD](object-properties.md)     | facoltativo.                                                             |
| [oggetto WPD che \_ \_ genera l' \_ Anteprima \_ dalla \_ risorsa](object-properties.md) | facoltativo.                                                             |
| [l' \_ oggetto WPD \_ può essere \_ eliminato](object-properties.md)                                               | Obbligatorio se l'oggetto può essere eliminato.                                |
| [\_ \_ impostazioni locali della lingua dell'oggetto WPD \_](object-properties.md)                                                                | Obbligatorio se l'oggetto non può essere eliminato.                             |
| [\_copyright per supporti WPD \_](media-properties.md)                                                     | facoltativo.                                                             |
| [\_ \_ classificazione parentale media \_ WPD](media-properties.md)                                        | facoltativo.                                                             |
| [\_ \_ meta genere WPD \_ media](media-properties.md)                                                  | facoltativo.                                                             |
| [\_sottotitolo supporto WPD \_ \_](media-properties.md)                                                    | facoltativo.                                                             |
| [\_Data di \_ rilascio del supporto WPD \_](media-properties.md)                                              | Consigliato.                                                          |
| [\_titolo supporto \_ WPD](media-properties.md)                                                             | Consigliato.                                                          |
| [\_proprietario del supporto WPD \_](media-properties.md)                                                             | Consigliato.                                                          |
| [\_ \_ Editor gestione supporto \_ WPD](media-properties.md)                                        | Consigliato.                                                          |
| [Webmaster di WPD \_ media \_](media-properties.md)                                                     | Consigliato.                                                          |
| [\_URL dell' \_ origine \_ multimediale WPD](media-properties.md)                                                  | Consigliato.                                                          |
| [\_ \_ URL destinazione supporto \_ WPD](media-properties.md)                                        | Consigliato.                                                          |
| [\_Descrizione supporto \_ WPD](media-properties.md)                                                 | facoltativo.                                                             |
| [\_genere multimediale \_ WPD](media-properties.md)                                                             | facoltativo.                                                             |
| [\_ \_ segnalibro oggetto multimediale WPD \_](media-properties.md)                                        | Consigliato                                                           |
| [\_ \_ \_ Data Ultima compilazione \_ del supporto WPD](media-properties.md)                                       | Consigliato.                                                          |
| [\_durata media \_ WPD \_ \_](media-properties.md)                                             | facoltativo.                                                             |
| [\_ \_ Descrizione secondaria supporti \_ WPD](object-properties.md)                                                                 | facoltativo.                                                             |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                               | Obbligatorio o facoltativo | Descrizione                                                                                                                 |
|-------------------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**\_impostazione predefinita della risorsa WPD \_**](wpd-resource-default.md)      | facoltativo.            | Contiene i dati del file Mediacast. Ad esempio, se questo Mediacast rappresenta un canale RSS, potrebbe trattarsi del documento RSS. |
| [**\_anteprima della risorsa WPD \_**](wpd-resource-thumbnail.md)  | facoltativo.            | Contiene l'anteprima che rappresenta questo Mediacast.                                                                         |
| [**\_Art album delle risorse WPD \_ \_**](wpd-resource-album-art.md) | facoltativo.            | Contiene l'artwork per questo Mediacast.                                                                                    |



 

## <a name="mapping-of-rss-elements-and-mediacast-properties"></a>Mapping degli elementi RSS e delle proprietà Mediacast

Un canale RSS può essere rappresentato come un oggetto Mediacast i cui riferimenti puntano a oggetti contenuto che rappresentano ogni elemento in un canale specificato.

Gli elementi in un feed RSS hanno la gerarchia e gli attributi seguenti.


```C++
<channel>
    <title />
    <link />
    <description />
    <language />
    <copyright />
    <managingEditor />
    <webMaster />
    <pubDate />
    <lastBuildDate />
    <category />
    <generator />
    <docs />
    <cloud />
    <ttl />

    <image>
        <url />
        <title />
        <link />
        <width />
        <height />
        <description />
    </image>

    <rating />

    <textInput>
        <title />
        <description />
        <name />
        <link />
    </textInput>

    <skipHours />
    <skipDays />

    <item>
        <title />
        <link />
        <description />
        <author />
        <category domain = " "/>
        <comments />
        <enclousure url = " " length = " " type = " "/>
        <guid isPermaLink = " "/>
        <pubDate />
        <source url = " " />
    </item>
</channel>
```



Nella tabella seguente sono elencati gli elementi del canale in un feed RSS e le \_ proprietà del cast del tipo di contenuto WPD corrispondente \_ \_ \_ .



|                     |                          |                                                                                 |
|---------------------|--------------------------|---------------------------------------------------------------------------------|
| **Elemento Channel** | **Requisito del feed RSS** | **Proprietà Mediacast corrispondente**                                            |
| category            | facoltativo.                | [\_genere multimediale \_ WPD](media-properties.md)                       |
| cloud               | Non applicabile.          | Non applicabile.                                                                 |
| copyright           | facoltativo.                | [\_copyright per supporti WPD \_](media-properties.md)               |
| description         | Obbligatorio.                | [\_Descrizione supporto \_ WPD](media-properties.md)           |
| docs                | Non applicabile.          | Non applicabile.                                                                 |
| generatore           | Non applicabile.          | Non applicabile.                                                                 |
| Linguaggio            | Non applicabile.          | Non applicabile.                                                                 |
| lastBuildDate       | facoltativo.                | [\_ \_ \_ Data Ultima compilazione \_ del supporto WPD](media-properties.md) |
| link                | Obbligatorio.                | [\_ \_ URL destinazione supporto \_ WPD](media-properties.md)  |
| managingEditor      | facoltativo.                | [\_ \_ Editor gestione supporto \_ WPD](media-properties.md)  |
| pubDate             | facoltativo.                | [\_Data di \_ rilascio del supporto WPD \_](media-properties.md)        |
| rating              | Non applicabile.          | Non applicabile.                                                                 |
| skipDays            | Non applicabile.          | Non applicabile.                                                                 |
| skipHours           | Non applicabile.          | Non applicabile.                                                                 |
| textInput           | Non applicabile.          | Non applicabile.                                                                 |
| title               | Obbligatorio.                | [\_nome dell'oggetto WPD \_](object-properties.md)                      |
| ttl                 | facoltativo.                | [\_durata media \_ WPD \_ \_](media-properties.md)       |
| webMaster           | facoltativo.                | [Webmaster di WPD \_ media \_](media-properties.md)               |



 

La tabella seguente elenca gli elementi immagine in un feed RSS e le proprietà del \_ cast del tipo di contenuto WPD corrispondente \_ \_ \_ .



|                   |                          |                                                                                |
|-------------------|--------------------------|--------------------------------------------------------------------------------|
| **Elemento immagine** | **Requisito del feed RSS** | **Proprietà Mediacast**                                                         |
| description       | facoltativo.                | [\_Descrizione supporto \_ WPD](media-properties.md)          |
| altezza            | facoltativo.                | [\_altezza supporto \_ WPD](media-properties.md)                    |
| link              | facoltativo.                | [\_ \_ URL destinazione supporto \_ WPD](media-properties.md) |
| title             | facoltativo.                | [\_nome dell'oggetto WPD \_](object-properties.md)                     |
| url               | facoltativo.                | [\_URL dell' \_ origine \_ multimediale WPD](media-properties.md)           |
| width             | facoltativo.                | [\_Larghezza supporto \_ WPD](media-properties.md)                      |



 

La tabella seguente elenca gli elementi elemento in un feed RSS e le proprietà del \_ cast del tipo di contenuto WPD corrispondente \_ \_ \_ .



|                  |               |                          |                                                                                |
|------------------|---------------|--------------------------|--------------------------------------------------------------------------------|
| **Elemento Item** | **Attributo** | **Requisito del feed RSS** | **Proprietà Mediacast**                                                         |
| author           |               | facoltativo.                | [WPD \_ media \_ Artist](media-properties.md)                    |
| category         |               | facoltativo.                | [\_genere multimediale \_ WPD](media-properties.md)                      |
|                  | dominio        | Non applicabile.          | Non applicabile.                                                                |
| description      |               | facoltativo.                | [\_Descrizione supporto \_ WPD](media-properties.md)          |
| recinto        |               | facoltativo.                |                                                                                |
|                  | url           | Obbligatorio.                | [\_URL dell' \_ origine \_ multimediale WPD](media-properties.md)           |
|                  | length        | Obbligatorio.                | [\_dimensioni dell'oggetto WPD \_](object-properties.md)                     |
|                  | tipo          | Obbligatorio.                | (Il tipo MIME deve essere mappato al tipo di contenuto della proprietà).                 |
| guid             |               | facoltativo.                | [\_GUID del supporto WPD \_](media-properties.md)                        |
|                  | PermaLink   | Non applicabile.          | Non applicabile.                                                                |
| link             |               | facoltativo.                | [\_ \_ URL destinazione supporto \_ WPD](media-properties.md) |
| pubDate          |               | facoltativo.                | [\_Data di \_ rilascio del supporto WPD \_](media-properties.md)       |
| source           |               | Non applicabile.          | Non applicabile.                                                                |
| title            |               | facoltativo.                | [\_nome dell'oggetto WPD \_](object-properties.md)                     |



 

Nell'esempio seguente viene illustrato un feed RSS completo per un podcast fittizio fornito dal CEO di una società di pubblicazione.


```C++
<channel>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/podcasting</link>
    <description>Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</description>
    <language>en-us</language>
    <copyright>2006 Lucerne Publishing LP, LLLP. All Rights Reserved.</copyright>
    <managingEditor>someone@example.com</managingEditor>
    <webMaster>someone@example.com</webMaster>
    <pubDate>Fri, 9 June 2006 14:00:28 EDT</pubDate>
    <lastBuildDate Fri, 9 June 2006 14:00:28 EDT />
    <category>News</category>
    <generator>Podcaster version 1.0</generator>
    <docs>https://www.lucernepublishing.com/tech/rss</docs>
    <cloud />
    <ttl>240</ttl>
    <rating />
    <textInput />
    <skipHours />
    <skipDays />

<image>
     <url>https://www.lucernepublishing.com/images/logo.gif</url>
     <title>Lucerne Publishing</title>
     <link>https://www.lucernepublishing.com/community/podcasts</link>
     <width>300</width>
     <height>300</height>
     <description>Lucerne Logo</description>
</image>

<item>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past 5 years and their implications.</description>
    <author>Lucerne</author>
    <category>News</category>
    <comments />
    <enclosure url="https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3" length="10329011" type="audio/mpeg" />
    <guid>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</guid>
    <pubDate>Thur, 1 June 2006 14:00:28 EDT</pubDate>
    <source />
</item>

</channel>
```



## <a name="mapping-rss-channel-elements-to-wpd-property-values"></a>Mapping degli elementi del canale RSS ai valori delle proprietà WPD

Nella tabella seguente viene descritto in che modo i valori negli elementi del canale RSS nell'esempio precedente vengono mappati a determinate proprietà di WPD.



|                                                                                              |                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| **Proprietà WPD**                                                                             | **Valore**                                                                                     |
| [\_copyright per supporti WPD \_](media-properties.md)                            | 2006 Lucerne Publishing LP, LLLP. All Rights Reserved.                                        |
| [\_Descrizione supporto \_ WPD](media-properties.md)                        | Il CEO della pubblicazione di Lucerne Peter Bankov esamina le tendenze più recenti nelle pubblicazioni online. |
| [\_ \_ URL destinazione supporto \_ WPD](media-properties.md)               | https://www.lucernepublishing.com/services/podcasting                                          |
| [\_genere multimediale \_ WPD](media-properties.md)                                    | Notizie                                                                                          |
| [\_ \_ \_ Data Ultima compilazione \_ del supporto WPD](media-properties.md)              | Venerdì, 9 giugno 2006 14:00:28 EDT                                                                 |
| [\_ \_ Editor gestione supporto \_ WPD](media-properties.md)               | someone@example.com                                                                           |
| [\_Data di \_ rilascio del supporto WPD \_](media-properties.md)                     | Venerdì, 9 giugno 2006 14:00:28 EDT                                                                 |
| [\_durata media \_ WPD \_ \_](media-properties.md)                    | 240                                                                                           |
| [\_titolo supporto \_ WPD](media-properties.md)                                    | Pubblicazione digitale                                                                       |
| [\_URL dell' \_ origine \_ multimediale WPD](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publication/rss.xml                  |
| [Webmaster di WPD \_ media \_](media-properties.md)                            | someone@example.com                                                                           |
| [\_tipo di \_ contenuto dell'oggetto WPD \_](object-properties.md)                  | \_cast del \_ supporto del tipo di contenuto WPD \_ \_                                                               |
| [\_ \_ Data creazione oggetto \_ WPD](object-properties.md)                | Venerdì, 9 giugno 2006 14:00:28 EDT                                                                 |
| [\_data dell'oggetto WPD \_ \_ creata](object-properties.md)                  | Venerdì, 9 giugno 2006 14:00:28 EDT                                                                 |
| [\_data dell'oggetto WPD \_ \_ modificata](object-properties.md)                | Venerdì, 9 giugno 2006 14:00:28 EDT                                                                 |
| [\_formato oggetto \_ WPD](object-properties.md)                               | \_ \_ \_ \_ cast multimediale astratto formato oggetto \_ WPD                                                    |
| [\_ID oggetto \_ WPD](object-properties.md)                                       | Valore dipendente dalla sessione.                                                                      |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                   | Pubblicazione digitale                                                                       |
| [\_ \_ \_ nome file originale oggetto \_ WPD](object-properties.md)     | Pubblicazione digitale                                                                       |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                        | Podcast (una cartella Podcast fittizia sul dispositivo). Per questo esempio, si supponga "0A0".        |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md) | Valore indipendente dalla sessione. (Si supponga "notifica 0A1" per questo esempio).                                   |
| [\_riferimenti a oggetti WPD \_](object-properties.md)                       | 0A2 per N elementi<br/>                                                                   |
| [\_dimensioni dell'oggetto WPD \_](object-properties.md)                                   | 13.790                                                                                        |



 

## <a name="mapping-rss-image-elements-to-wpd-property-values"></a>Mapping di elementi dell'immagine RSS ai valori delle proprietà WPD

Nella tabella seguente viene descritto in che modo i valori negli elementi immagine RSS nell'esempio precedente vengono mappati a determinate proprietà WPD.



|                                                                                                                         |                                                     |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| **Proprietà WPD**                                                                                                        | **Valore**                                           |
| [\_Descrizione supporto \_ WPD](media-properties.md)                                                   | Logo Lucerne                                        |
| [\_ \_ URL destinazione supporto \_ WPD](media-properties.md)                                          | https://www.lucernepublishing.com/community/podcasts |
| [\_altezza supporto \_ WPD](media-properties.md)                                                             | 300                                                 |
| [\_URL dell' \_ origine \_ multimediale WPD](media-properties.md)                                                    | https://www.lucernepublishing.com/images/logo.gif    |
| [\_Larghezza supporto \_ WPD](media-properties.md)                                                               | 300                                                 |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                                              | Pubblicazione di Lucerne                                  |
| [l' \_ attributo della risorsa WPD \_ può essere \_ \_ eliminato](attributes.md)                               | VARIANT \_ true                                       |
| [l'attributo della risorsa WPD è in \_ \_ grado di \_ \_ leggere](attributes.md)                                   | VARIANT \_ true                                       |
| [\_formato dell' \_ attributo della risorsa WPD \_](resource-attribute-properties.md)                     | \_ \_ GIF formato oggetto \_ WPD                            |
| [\_dimensione del \_ \_ buffer di \_ lettura ottimale dell' \_ attributo \_ della risorsa WPD](attributes.md) | 1024                                                |
| [\_ \_ dimensioni totali dell'attributo della risorsa WPD \_ \_](resource-attribute-properties.md)            | 512                                                 |



 

## <a name="mapping-rss-item-elements-to-wpd-property-values"></a>Mapping di elementi elemento RSS a valori di proprietà WPD

Nella tabella seguente viene descritto il mapping tra i valori negli elementi RSS dell'esempio precedente e le proprietà WPD specifiche.



|                                                                                              |                                                                                                                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **Proprietà WPD**<br/>                                                                  | **Valore**                                                                                                                        |
| [\_titolo supporto \_ WPD](media-properties.md)                                    | Pubblicazione digitale                                                                                                          |
| [\_durata supporto \_ WPD](media-properties.md)                              | 10329011                                                                                                                         |
| [WPD \_ media \_ Artist](media-properties.md)                                  | Lucerna                                                                                                                          |
| [\_Descrizione supporto \_ WPD](media-properties.md)                        | Le pubblicazioni online sono in rapida evoluzione. Un CEO della casa di pubblicazione esamina le tendenze degli ultimi 5 anni e le relative implicazioni. |
| [\_ \_ URL destinazione supporto \_ WPD](media-properties.md)               | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_genere multimediale \_ WPD](media-properties.md)                                    | Notizie                                                                                                                             |
| [\_GUID del supporto WPD \_](media-properties.md)                                      | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_Data di \_ rilascio del supporto WPD \_](media-properties.md)                     | Gio, 1 giugno 2006 14:00:28 EDT                                                                                                   |
| [\_URL dell' \_ origine \_ multimediale WPD](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_riferimenti all'oggetto WPD \_ \_](object-properties.md)            | Notifica 0A1                                                                                                                              |
| [\_tipo di \_ contenuto dell'oggetto WPD \_](object-properties.md)                  | \_ \_ immagine multimediale del tipo di contenuto WPD \_ \_                                                                                                 |
| [\_ \_ Data creazione oggetto \_ WPD](object-properties.md)                | Gio, 1 giugno 2006 14:00:28 EDT                                                                                                   |
| [\_data dell'oggetto WPD \_ \_ creata](object-properties.md)                  | Gio, 1 giugno 2006 14:00:28 EDT                                                                                                   |
| [\_data dell'oggetto WPD \_ \_ modificata](object-properties.md)                | Gio, 1 giugno 2006 14:00:28 EDT                                                                                                   |
| [\_formato oggetto \_ WPD](object-properties.md)                               | \_Formato oggetto \_ WPD \_ MP3                                                                                                         |
| [\_ID oggetto \_ WPD](object-properties.md)                                       | Dipendente dalla sessione. (Si supponga "0A2" per questo esempio).                                                                              |
| [\_nome dell'oggetto WPD \_](object-properties.md)                                   | Pubblicazione digitale                                                                                                          |
| [\_ \_ \_ nome file originale oggetto \_ WPD](object-properties.md)     | digital0601.mp3                                                                                                                  |
| [\_ \_ ID padre dell'oggetto WPD \_](object-properties.md)                        | 0A0                                                                                                                              |
| [\_ \_ \_ ID univoco permanente dell'oggetto WPD \_](object-properties.md) | Indipendente dalla sessione.                                                                                                             |
| [\_dimensioni dell'oggetto WPD \_](object-properties.md)                                   | 10329011                                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 




