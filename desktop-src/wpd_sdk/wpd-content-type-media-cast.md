---
description: CAST MULTIMEDIALE \_ DEL TIPO DI \_ \_ CONTENUTO \_ WPD
ms.assetid: 368e7381-8978-421a-b450-59915f8e70e2
title: WPD_CONTENT_TYPE_MEDIA_CAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4454053400c783b53437dd025e5adc8e845ea08c1b95b8d9b1fd358f39e326f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083315"
---
# <a name="wpd_content_type_media_cast"></a>CAST MULTIMEDIALE \_ DEL TIPO DI \_ \_ CONTENUTO \_ WPD

Un oggetto che descrive il tipo come WPD \_ CONTENT TYPE MEDIA CAST rappresenta una raccolta di contenuto \_ \_ \_ correlato.

Un oggetto Mediacast può essere pensato come un oggetto contenitore che raggruppa il contenuto correlato, proprio come un gruppo di playlist. Spesso, un oggetto Mediacast viene usato per raggruppare il contenuto multimediale pubblicato online. Ad esempio, un canale RSS può essere rappresentato come oggetto Mediacast i cui riferimenti all'oggetto puntano a oggetti contenuto che rappresentano ogni elemento nel canale.

Questo tipo di oggetto supporta le proprietà seguenti.



| Nome della proprietà             |  Obbligatorio o facoltativo         |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [ID OGGETTO WPD \_ \_](object-properties.md)                                                                | Obbligatorio.                                                             |
| [ID PADRE \_ DELL'OGGETTO WPD \_ \_](object-properties.md)                                                 | Obbligatorio.                                                             |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto rappresenta un file.                             |
| [\_ID UNIVOCO PERMANENTE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                          | Obbligatorio.                                                             |
| [FORMATO \_ DELL'OGGETTO WPD \_](object-properties.md)                                                        | Obbligatorio.                                                             |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                                           | Obbligatorio.                                                             |
| [\_ISHIDDEN DELL'OGGETTO \_ WPD](object-properties.md)                                                    | Obbligatorio se l'oggetto è nascosto.                                     |
| [ISSYSTEM \_ DELL'OGGETTO \_ WPD](object-properties.md)                                                    | Obbligatorio se l'oggetto è un oggetto di sistema (rappresenta un file di sistema). |
| [DIMENSIONI \_ DELL'OGGETTO WPD \_](object-properties.md)                                                            | Obbligatorio se l'oggetto dispone di almeno una risorsa.                     |
| [NOME FILE ORIGINALE \_ DELL'OGGETTO \_ \_ \_ WPD](object-properties.md)                              | Obbligatorio se l'oggetto rappresenta un file.                             |
| [OGGETTO WPD \_ \_ NON \_ CONSUMABILE](object-properties.md)                                       | Consigliato se l'oggetto non è destinato all'uso da parte del dispositivo. |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                                                | Obbligatorio se l'oggetto contiene riferimenti ad altri oggetti.               |
| [PAROLE CHIAVE DEGLI OGGETTI WPD \_ \_](object-properties.md)                                                    | facoltativo.                                                             |
| [ID SINCRONIZZAZIONE OGGETTO WPD \_ \_ \_](object-properties.md)                                                     | facoltativo.                                                             |
| [L'OGGETTO WPD \_ \_ È PROTETTO DA \_ \_ DRM](object-properties.md)                                  | Obbligatorio se l'oggetto è protetto dalla tecnologia DRM.                |
| [DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                           | facoltativo.                                                             |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                                         | Consigliato.                                                          |
| [DATA DELL'OGGETTO WPD \_ \_ \_ CREATO](object-properties.md)                                         | facoltativo.                                                             |
| [RIFERIMENTI INDIETRO DEGLI OGGETTI WPD \_ \_ \_](object-properties.md)                                     | Consigliato se all'oggetto viene fatto riferimento da un altro oggetto.            |
| [ID OGGETTO FUNZIONALE \_ DEL \_ CONTENITORE \_ DI \_ OGGETTI \_ WPD](object-properties.md)     | facoltativo.                                                             |
| [GENERAZIONE \_ DELL'ANTEPRIMA \_ \_ DELL'OGGETTO \_ WPD DALLA \_ RISORSA](object-properties.md) | facoltativo.                                                             |
| [L'OGGETTO WPD \_ \_ PUÒ ESSERE \_ ELIMINATO](object-properties.md)                                               | Obbligatorio se l'oggetto può essere eliminato.                                |
| [IMPOSTAZIONI LOCALI \_ DELLA LINGUA \_ DELL'OGGETTO WPD \_](object-properties.md)                                                                | Obbligatorio se l'oggetto non può essere eliminato.                             |
| [COPYRIGHT DEI SUPPORTI WPD \_ \_](media-properties.md)                                                     | facoltativo.                                                             |
| [CLASSIFICAZIONE DEI \_ GENITORI DEI CONTENUTI \_ MULTIMEDIALI \_ WPD](media-properties.md)                                        | facoltativo.                                                             |
| [META GENERE \_ \_ MULTIMEDIALE WPD \_](media-properties.md)                                                  | facoltativo.                                                             |
| [TITOLO \_ SECONDARIO \_ MULTIMEDIALE \_ WPD](media-properties.md)                                                    | facoltativo.                                                             |
| [DATA DI RILASCIO \_ DEI SUPPORTI WPD \_ \_](media-properties.md)                                              | Consigliato.                                                          |
| [TITOLO MULTIMEDIALE WPD \_ \_](media-properties.md)                                                             | Consigliato.                                                          |
| [PROPRIETARIO DEI SUPPORTI WPD \_ \_](media-properties.md)                                                             | Consigliato.                                                          |
| [EDITOR DI GESTIONE DEI SUPPORTI WPD \_ \_ \_](media-properties.md)                                        | Consigliato.                                                          |
| [WEBMASTER MULTIMEDIALE WPD \_ \_](media-properties.md)                                                     | Consigliato.                                                          |
| [URL ORIGINE SUPPORTO WPD \_ \_ \_](media-properties.md)                                                  | Consigliato.                                                          |
| [URL DESTINAZIONE SUPPORTI WPD \_ \_ \_](media-properties.md)                                        | Consigliato.                                                          |
| [DESCRIZIONE DEI SUPPORTI WPD \_ \_](media-properties.md)                                                 | facoltativo.                                                             |
| [GENERE MULTIMEDIALE WPD \_ \_](media-properties.md)                                                             | facoltativo.                                                             |
| [SEGNALIBRO \_ DELL'OGGETTO \_ MULTIMEDIALE WPD \_](media-properties.md)                                        | Consigliato                                                           |
| [DATA ULTIMA COMPILAZIONE \_ DEI \_ SUPPORTI \_ WPD \_](media-properties.md)                                       | Consigliato.                                                          |
| [TEMPO DI \_ VITA DEI \_ SUPPORTI \_ WPD \_](media-properties.md)                                             | facoltativo.                                                             |
| [DESCRIZIONE DELLA \_ SOTTOSOD MEDIA \_ \_ WPD](object-properties.md)                                                                 | facoltativo.                                                             |



 

## <a name="typical-resources"></a>Risorse tipiche

Questi oggetti includono in genere le risorse seguenti.



| Nome risorsa                                               | Obbligatorio o facoltativo | Descrizione                                                                                                                 |
|-------------------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**IMPOSTAZIONE PREDEFINITA DELLA RISORSA WPD \_ \_**](wpd-resource-default.md)      | facoltativo.            | Contiene i dati del file mediacast. Ad esempio, se questo mediacast rappresenta un canale RSS, potrebbe trattarsi del documento RSS. |
| [**ANTEPRIMA DELLA RISORSA WPD \_ \_**](wpd-resource-thumbnail.md)  | facoltativo.            | Contiene l'anteprima che rappresenta questo mediacast.                                                                         |
| [**WPD \_ RESOURCE \_ ALBUM \_ ART**](wpd-resource-album-art.md) | facoltativo.            | Contiene la grafica per questo mediacast.                                                                                    |



 

## <a name="mapping-of-rss-elements-and-mediacast-properties"></a>Mapping di elementi RSS e proprietà Mediacast

Un canale RSS può essere rappresentato come oggetto Mediacast i cui riferimenti puntano a oggetti contenuto che rappresentano ogni elemento in un canale specificato.

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



La tabella seguente elenca gli elementi del canale in un feed RSS e le proprietà MEDIA CAST WPD \_ CONTENT \_ TYPE \_ \_ corrispondenti.



| Elemento Channel | Requisito del feed RSS | Proprietà Mediacast corrispondente      |
|---------------------|--------------------------|---------------------------------------------------------------------------------|
| category            | facoltativo.                | [GENERE MULTIMEDIALE WPD \_ \_](media-properties.md)                       |
| cloud               | Non applicabile.          | Non applicabile.                                                                 |
| copyright           | facoltativo.                | [COPYRIGHT MULTIMEDIALE WPD \_ \_](media-properties.md)               |
| description         | Obbligatorio.                | [DESCRIZIONE DEI SUPPORTI WPD \_ \_](media-properties.md)           |
| docs                | Non applicabile.          | Non applicabile.                                                                 |
| generatore           | Non applicabile.          | Non applicabile.                                                                 |
| Linguaggio            | Non applicabile.          | Non applicabile.                                                                 |
| lastBuildDate       | facoltativo.                | [DATA ULTIMA COMPILAZIONE \_ \_ \_ SUPPORTI WPD \_](media-properties.md) |
| link                | Obbligatorio.                | [URL DESTINAZIONE SUPPORTO WPD \_ \_ \_](media-properties.md)  |
| gestioneeditor      | facoltativo.                | [WPD \_ MEDIA \_ MANAGING \_ EDITOR](media-properties.md)  |
| pubDate             | facoltativo.                | [DATA DI RILASCIO DEI FILE MULTIMEDIALI WPD \_ \_ \_](media-properties.md)        |
| rating              | Non applicabile.          | Non applicabile.                                                                 |
| skipDays            | Non applicabile.          | Non applicabile.                                                                 |
| skipHours           | Non applicabile.          | Non applicabile.                                                                 |
| Textinput           | Non applicabile.          | Non applicabile.                                                                 |
| title               | Obbligatorio.                | [NOME OGGETTO \_ WPD \_](object-properties.md)                      |
| ttl                 | facoltativo.                | [WPD \_ MEDIA \_ TIME \_ TO \_ LIVE](media-properties.md)       |
| Webmaster           | facoltativo.                | [WPD \_ MEDIA \_ WEBMASTER](media-properties.md)               |



 

La tabella seguente elenca gli elementi immagine in un feed RSS e le proprietà MEDIA CAST WPD \_ CONTENT \_ TYPE \_ \_ corrispondenti.



| Elemento immagine | Requisito del feed RSS | Proprietà Mediacast                     |
|-------------------|--------------------------|--------------------------------------------------------------------------------|
| description       | facoltativo.                | [DESCRIZIONE DEI SUPPORTI WPD \_ \_](media-properties.md)          |
| altezza            | facoltativo.                | [ALTEZZA SUPPORTO \_ WPD \_](media-properties.md)                    |
| link              | facoltativo.                | [URL DESTINAZIONE SUPPORTO WPD \_ \_ \_](media-properties.md) |
| title             | facoltativo.                | [NOME OGGETTO \_ WPD \_](object-properties.md)                     |
| url               | facoltativo.                | [URL ORIGINE MULTIMEDIALE WPD \_ \_ \_](media-properties.md)           |
| width             | facoltativo.                | [LARGHEZZA SUPPORTO \_ WPD \_](media-properties.md)                      |



 

La tabella seguente elenca gli elementi elemento in un feed RSS e le proprietà MEDIA CAST WPD \_ CONTENT \_ TYPE \_ \_ corrispondenti.



| Elemento Item | Attributo | Requisito del feed RSS | Proprietà Mediacast  |
|------------------|---------------|--------------------------|--------------------------------------------------------------------------------|
| author           |               | facoltativo.                | [WPD \_ MEDIA \_ ARTIST](media-properties.md)                    |
| category         |               | facoltativo.                | [GENERE MULTIMEDIALE WPD \_ \_](media-properties.md)                      |
|                  | dominio        | Non applicabile.          | Non applicabile.                                                                |
| description      |               | facoltativo.                | [DESCRIZIONE DEI SUPPORTI WPD \_ \_](media-properties.md)          |
| Recinto        |               | facoltativo.                |                                                                                |
|                  | url           | Obbligatorio.                | [URL ORIGINE SUPPORTO WPD \_ \_ \_](media-properties.md)           |
|                  | length        | Obbligatorio.                | [DIMENSIONI \_ DELL'OGGETTO WPD \_](object-properties.md)                     |
|                  | tipo          | Obbligatorio.                | Il tipo MIME deve essere mappato al tipo di contenuto della proprietà.                 |
| guid             |               | facoltativo.                | [GUID SUPPORTO WPD \_ \_](media-properties.md)                        |
|                  | isPermaLink   | Non applicabile.          | Non applicabile.                                                                |
| link             |               | facoltativo.                | [URL DESTINAZIONE SUPPORTI WPD \_ \_ \_](media-properties.md) |
| pubDate          |               | facoltativo.                | [DATA DI RILASCIO \_ DEI \_ SUPPORTI WPD \_](media-properties.md)       |
| source           |               | Non applicabile.          | Non applicabile.                                                                |
| title            |               | facoltativo.                | [NOME OGGETTO \_ WPD \_](object-properties.md)                     |



 

L'esempio seguente mostra un feed RSS completo per un podcast fittizio fornito dal CEO di una società di pubblicazione.


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

Nella tabella seguente viene descritto il mapping dei valori negli elementi del canale RSS nell'esempio precedente a determinate proprietà WPD.



| Proprietà WPD | Valore |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [COPYRIGHT DEI SUPPORTI WPD \_ \_](media-properties.md)                            | 2006 Lucerne Publishing LP, LLLP. All Rights Reserved.                                        |
| [DESCRIZIONE DEI SUPPORTI WPD \_ \_](media-properties.md)                        | Il CEO di Lucerne Publishing, Peter Bankov, osserva le ultime tendenze nelle pubblicazioni online. |
| [URL DESTINAZIONE SUPPORTI WPD \_ \_ \_](media-properties.md)               | https://www.lucernepublishing.com/services/podcasting                                          |
| [GENERE MULTIMEDIALE WPD \_ \_](media-properties.md)                                    | Notizie                                                                                          |
| [DATA ULTIMA COMPILAZIONE \_ DEI \_ SUPPORTI \_ WPD \_](media-properties.md)              | ven, 9 giugno 2006 14:00:28 EDT                                                                 |
| [EDITOR DI GESTIONE DEI SUPPORTI WPD \_ \_ \_](media-properties.md)               | someone@example.com                                                                           |
| [DATA DI RILASCIO \_ DEI \_ SUPPORTI WPD \_](media-properties.md)                     | ven, 9 giugno 2006 14:00:28 EDT                                                                 |
| [TEMPO DI \_ VITA DEI \_ SUPPORTI \_ WPD \_](media-properties.md)                    | 240                                                                                           |
| [TITOLO MULTIMEDIALE WPD \_ \_](media-properties.md)                                    | Pubblicazione digitale                                                                       |
| [URL ORIGINE SUPPORTO WPD \_ \_ \_](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publication/rss.xml                  |
| [WEBMASTER MULTIMEDIALE WPD \_ \_](media-properties.md)                            | someone@example.com                                                                           |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                  | CAST MULTIMEDIALE \_ DEL TIPO \_ DI \_ CONTENUTO \_ WPD                                                               |
| [DATA DELL'OGGETTO WPD \_ \_ \_ CREATO](object-properties.md)                | ven, 9 giugno 2006 14:00:28 EDT                                                                 |
| [DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                  | ven, 9 giugno 2006 14:00:28 EDT                                                                 |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                | ven, 9 giugno 2006 14:00:28 EDT                                                                 |
| [FORMATO \_ DELL'OGGETTO WPD \_](object-properties.md)                               | CAST MULTIMEDIALE \_ ASTRATTO IN \_ \_ FORMATO \_ \_ OGGETTO WPD                                                    |
| [ID OGGETTO WPD \_ \_](object-properties.md)                                       | Valore dipendente dalla sessione.                                                                      |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                   | Pubblicazione digitale                                                                       |
| [NOME FILE ORIGINALE \_ DELL'OGGETTO \_ \_ \_ WPD](object-properties.md)     | Pubblicazione digitale                                                                       |
| [ID PADRE \_ DELL'OGGETTO WPD \_ \_](object-properties.md)                        | MyPodcasts (una cartella fittizia di podcast nel dispositivo). Si supponga che "0A0" per questo esempio.        |
| [\_ID UNIVOCO PERMANENTE DELL'OGGETTO WPD \_ \_ \_](object-properties.md) | Valore indipendente dalla sessione. Si supponga che "0A1" per questo esempio.                                   |
| [RIFERIMENTI AGLI OGGETTI WPD \_ \_](object-properties.md)                       | 0A2 per N elementi<br/>                                                                   |
| [DIMENSIONI \_ DELL'OGGETTO WPD \_](object-properties.md)                                   | 13,790                                                                                        |



 

## <a name="mapping-rss-image-elements-to-wpd-property-values"></a>Mapping degli elementi immagine RSS ai valori delle proprietà WPD

Nella tabella seguente viene descritto il mapping dei valori negli elementi dell'immagine RSS nell'esempio precedente a determinate proprietà WPD.



| Proprietà WPD               |                         Valore                                           |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [DESCRIZIONE DEI SUPPORTI WPD \_ \_](media-properties.md)                                                   | Lucerne Logo                                        |
| [URL DESTINAZIONE SUPPORTI WPD \_ \_ \_](media-properties.md)                                          | https://www.lucernepublishing.com/community/podcasts |
| [ALTEZZA DEI SUPPORTI WPD \_ \_](media-properties.md)                                                             | 300                                                 |
| [URL ORIGINE SUPPORTO WPD \_ \_ \_](media-properties.md)                                                    | https://www.lucernepublishing.com/images/logo.gif    |
| [LARGHEZZA DEI SUPPORTI WPD \_ \_](media-properties.md)                                                               | 300                                                 |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                                              | Lucerne Publishing                                  |
| [L'ATTRIBUTO DELLA RISORSA WPD \_ \_ PUÒ ESSERE \_ \_ ELIMINATO](attributes.md)                               | VARIANT \_ TRUE                                       |
| [L'ATTRIBUTO DELLA RISORSA WPD \_ \_ PUÒ \_ \_ LEGGERE](attributes.md)                                   | VARIANT \_ TRUE                                       |
| [FORMATO DELL'ATTRIBUTO DELLA RISORSA WPD \_ \_ \_](resource-attribute-properties.md)                     | GIF FORMATO OGGETTO WPD \_ \_ \_                            |
| [DIMENSIONI OTTIMALI DEL \_ BUFFER DI \_ LETTURA \_ DELL'ATTRIBUTO DELLA \_ RISORSA \_ \_ WPD](attributes.md) | 1024                                                |
| [DIMENSIONI TOTALI \_ DELL'ATTRIBUTO DELLA RISORSA \_ \_ \_ WPD](resource-attribute-properties.md)            | 512                                                 |



 

## <a name="mapping-rss-item-elements-to-wpd-property-values"></a>Mapping di elementi elemento RSS a valori di proprietà WPD

Nella tabella seguente viene descritto il mapping dei valori negli elementi elemento RSS nell'esempio precedente a determinate proprietà WPD.



| Proprietà WPD  | Valore                   |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [TITOLO MULTIMEDIALE WPD \_ \_](media-properties.md)                                    | Pubblicazione digitale                                                                                                          |
| [DURATA DEI SUPPORTI WPD \_ \_](media-properties.md)                              | 10329011                                                                                                                         |
| [WPD \_ MEDIA \_ ARTIST](media-properties.md)                                  | Lucerna                                                                                                                          |
| [DESCRIZIONE DEI SUPPORTI WPD \_ \_](media-properties.md)                        | Le pubblicazioni online cambiano rapidamente. Un amministratore delegato della casa editrice esamina le tendenze degli ultimi 5 anni e le relative implicazioni. |
| [URL DESTINAZIONE SUPPORTI WPD \_ \_ \_](media-properties.md)               | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [GENERE MULTIMEDIALE WPD \_ \_](media-properties.md)                                    | Notizie                                                                                                                             |
| [GUID SUPPORTO WPD \_ \_](media-properties.md)                                      | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [DATA DI RILASCIO \_ DEI \_ SUPPORTI WPD \_](media-properties.md)                     | Thur, 1 giugno 2006 14:00:28 EDT                                                                                                   |
| [URL ORIGINE SUPPORTO WPD \_ \_ \_](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [RIFERIMENTI INDIETRO DEGLI OGGETTI WPD \_ \_ \_](object-properties.md)            | 0a1                                                                                                                              |
| [TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD](object-properties.md)                  | IMMAGINE MULTIMEDIALE \_ DEL TIPO DI CONTENUTO \_ WPD \_ \_                                                                                                 |
| [DATA DELL'OGGETTO WPD \_ \_ \_ CREATO](object-properties.md)                | Thur, 1 giugno 2006 14:00:28 EDT                                                                                                   |
| [DATA DI CREAZIONE DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                  | Thur, 1 giugno 2006 14:00:28 EDT                                                                                                   |
| [DATA DI MODIFICA DELL'OGGETTO WPD \_ \_ \_](object-properties.md)                | Thur, 1 giugno 2006 14:00:28 EDT                                                                                                   |
| [FORMATO \_ DELL'OGGETTO WPD \_](object-properties.md)                               | FORMATO OGGETTO WPD \_ \_ \_ MP3                                                                                                         |
| [ID OGGETTO WPD \_ \_](object-properties.md)                                       | Dipendente dalla sessione. Si supponga che "0A2" per questo esempio.                                                                              |
| [NOME OGGETTO \_ WPD \_](object-properties.md)                                   | Pubblicazione digitale                                                                                                          |
| [NOME FILE ORIGINALE \_ DELL'OGGETTO \_ \_ \_ WPD](object-properties.md)     | digital0601.mp3                                                                                                                  |
| [ID PADRE \_ DELL'OGGETTO WPD \_ \_](object-properties.md)                        | 0A0                                                                                                                              |
| [\_ID UNIVOCO PERMANENTE DELL'OGGETTO WPD \_ \_ \_](object-properties.md) | Indipendente dalla sessione.                                                                                                             |
| [DIMENSIONI \_ DELL'OGGETTO WPD \_](object-properties.md)                                   | 10329011                                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Requisiti per gli oggetti**](requirements-for-objects.md)
</dt> </dl>

 

 




