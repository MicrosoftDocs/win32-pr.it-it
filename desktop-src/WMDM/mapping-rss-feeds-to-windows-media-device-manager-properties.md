---
title: Mapping dei feed RSS alle Windows di Gestione dispositivi multimediali
description: Mapping dei feed RSS alle Windows di Gestione dispositivi multimediali
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Gestione dispositivi multimediali, feed RSS
- Gestione dispositivi, feed RSS
- guida per programmatori,feed RSS
- applicazioni desktop, feed RSS
- creazione Windows applicazioni di Gestione dispositivi multimediali,feed RSS
- Feed RSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355515217db31740603d5c6323ef8455da4b29ee80bec508897d2d4df5d59bde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031681"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a>Mapping dei feed RSS alle Windows di Gestione dispositivi multimediali

Windows Media Player 11 offre una funzionalità di aggregatore RSS che consente agli utenti di archiviare il contenuto ottenuto dai podcast nei propri computer. Questo argomento descrive gli elementi XML presenti in un feed RSS. Esegue inoltre il mapping di questi elementi RSS Windows proprietà di Gestione dispositivi multimediali.

Gli elementi in un feed RSS hanno la gerarchia e gli attributi seguenti:


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



Nella tabella seguente sono elencati gli elementi del canale in un feed RSS e le proprietà Windows gestione dispositivi multimediali.



| Elemento Channel | Stato         | Proprietà Windows Gestione dispositivi multimediali corrispondente   |
|-----------------|----------------|-------------------------------------------------------|
| category        | Facoltativo       | [g \_ wszWMDMGenre](metadata-constants.md)             |
| cloud           | Non applicabile | Non applicabile                                        |
| copyright       | Facoltativo       | [g \_ wszWMDMProviderCopyright](metadata-constants.md) |
| description     | Necessario       | [g \_ wszWMDMDescription](metadata-constants.md)       |
| docs            | Non applicabile | Non applicabile                                        |
| generatore       | Non applicabile | Non applicabile                                        |
| Linguaggio        | Non applicabile | Non applicabile                                        |
| lastBuildDate   | Facoltativo       | [g \_ wszWMDMLastModifiedDate](metadata-constants.md)  |
| link            | Necessario       | [g \_ wszWMDMDestinationURL](metadata-constants.md)    |
| managingEditor  | Facoltativo       | [g \_ wszWMDMEditor](metadata-constants.md)            |
| pubDate         | Facoltativo       | [g \_ wszWMDMYear](metadata-constants.md)              |
| rating          | Non applicabile | Non applicabile                                        |
| skipDays        | Non applicabile | Non applicabile                                        |
| skipHours       | Non applicabile | Non applicabile                                        |
| Textinput       | Non applicabile | Non applicabile                                        |
| title           | Necessario       | [g \_ wszWMDMTitle](metadata-constants.md)             |
| ttl             | Facoltativo       | [g \_ wszWMDMTimeToLive](metadata-constants.md)        |
| Webmaster       | Facoltativo       | [g \_ wszWMDMWebMaster](metadata-constants.md)         |



 

Nella tabella seguente sono elencati gli elementi immagine in un feed RSS e le proprietà WMDM corrispondenti.



| Elemento Image | Stato   | Proprietà Windows Gestione dispositivi multimediali corrispondente |
|---------------|----------|-----------------------------------------------------|
| description   | Facoltativo | [g \_ wszWMDMDescription](metadata-constants.md)     |
| altezza        | Facoltativo | [g \_ wszWMDMMHeight](metadata-constants.md)          |
| link          | Facoltativo | [g \_ wszWMDMDestinationURL](metadata-constants.md)  |
| title         | Facoltativo | [g \_ wszWMDMTitle](metadata-constants.md)           |
| url           | Facoltativo | [g \_ wszWMDMSourceURL](metadata-constants.md)       |
| width         | Facoltativo | [g \_ wszWMDMWidth](metadata-constants.md)           |



 

Nella tabella seguente sono elencati gli elementi dell'elemento in un feed RSS e le proprietà Windows gestione dispositivi multimediali.



| Elemento Item | Attributo   | Stato         | Proprietà Windows Gestione dispositivi multimediali corrispondente            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| author       |             | Facoltativo       | [g \_ wszWMDMAuthor](metadata-constants.md)                     |
| category     |             | Facoltativo       | [g \_ wszWMDMGenre](metadata-constants.md)                      |
|              | dominio      | Non applicabile | Non applicabile                                                 |
| description  |             | Facoltativo       | [g \_ wszWMDMDescription](metadata-constants.md)                |
| Recinto    |             | Facoltativo       | Non applicabile                                                 |
|              | length      | Necessario       | [g \_ wszWMDMFileSize](metadata-constants.md)                   |
|              | type        | Obbligatoria       | Il tipo MIME deve essere mappato al tipo di contenuto della proprietà. |
|              | url         | Necessario       | [g \_ wszWMDMSourceURL](metadata-constants.md)                  |
| guid         |             | Facoltativo       | [g \_ wszWMDMediaGuid](metadata-constants.md)                   |
|              | isPermaLink | Non applicabile | Non applicabile                                                 |
| link         |             | Facoltativo       | [g \_ wszWMDMDestinationURL](metadata-constants.md)             |
| pubDate      |             | Facoltativo       | [g \_ wszWMDMYear](metadata-constants.md)                       |
| source       |             | Non applicabile | Non applicabile                                                 |
| title        |             | Facoltativo       | [g \_ wszWMDMTitle](metadata-constants.md)                      |



 

Esempio

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
    <link>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past five years and their implications.</description>
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



Mapping degli elementi del canale RSS ai Windows proprietà di Gestione dispositivi multimediali

Nella tabella seguente viene descritto il mapping dei valori negli elementi del canale RSS nell'esempio precedente a determinate Windows di Gestione dispositivi multimediali.



| Windows Proprietà di Gestione dispositivi multimediali                    | Valore                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthorDate](metadata-constants.md)           | ven, 9 giugno 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMDESCRIPTION](metadata-constants.md)          | Il CEO di Lucerne Publishing, Peter Bankov, osserva le ultime tendenze nelle pubblicazioni online. |
| [g \_ wszWMDMDESTINATION \_ URL](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [g \_ wszWMDMEDITOR](metadata-constants.md)               | someone@example.com                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md)     | ven, 9 giugno 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMFileName](metadata-constants.md)             | Pubblicazione digitale                                                                       |
| [g \_ wszWMDMFileSize](metadata-constants.md)             | 13,790                                                                                        |
| [g \_ wszWMDMFormatCode](metadata-constants.md)           | WMDM \_ FORMATCODE \_ MEDIA \_ CAST                                                                 |
| [g \_ wszWMDMGENRE](metadata-constants.md)                | Notizie                                                                                          |
| [g \_ wszWMDMLAST \_ MODIFIED \_ DATE](metadata-constants.md) | ven, 9 giugno 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md)     | ven, 9 giugno 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMProviderCopyright](metadata-constants.md)    | 2006 Lucerne Publishing LP, LLLP. All Rights Reserved.                                        |
| [g \_ wszWMDMTimeToLive](metadata-constants.md)           | 240                                                                                           |
| [g \_ wszWMDMTitle](metadata-constants.md)                | Pubblicazione digitale                                                                       |
| [g \_ wszWMDMWEBMASTER](metadata-constants.md)            | someone@example.com                                                                           |
| [g \_ wszWMDMYear](metadata-constants.md)                 | ven, 9 giugno 2006 14:00:28 EDT                                                                 |



 

Mapping degli elementi immagine RSS ai Windows proprietà di Gestione dispositivi multimediali

Nella tabella seguente viene descritto il mapping dei valori negli elementi immagine RSS dell'esempio precedente a determinate Windows di Gestione dispositivi multimediali.



| Windows Proprietà di Gestione dispositivi multimediali                | Valore                                            |
|------------------------------------------------------|--------------------------------------------------|
| [g \_ wszWMDMAlbumCoverFormat](metadata-constants.md) | GIF FORMATO OGGETTO WPD \_ \_ \_                         |
| [g \_ wszWMDMAlbumCoverSize](metadata-constants.md)   | 512                                              |
| [g \_ wszWMDMDescription](metadata-constants.md)      | Lucerne Logo                                     |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | www.lucernepublishing.com/community/podcasts   |
| [g \_ wszWMDMMHeight](metadata-constants.md)           | 300                                              |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [g \_ wszWMDMTitle](metadata-constants.md)            | Lucerne Publishing                               |
| [g \_ wszWMDMMWidth](metadata-constants.md)            | 300                                              |



 

Mapping degli elementi elemento RSS ai Windows proprietà di Gestione dispositivi multimediali

Nella tabella seguente viene descritto il mapping dei valori negli elementi elemento RSS nell'esempio precedente a determinate Windows di Gestione dispositivi multimediali.



| Windows Proprietà di Gestione dispositivi multimediali                | Valore                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthor](metadata-constants.md)           | Lucerna                                                                                                                             |
| [g \_ wszWMDMAuthorDate](metadata-constants.md)       | Thur, 1 giugno 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMDescription](metadata-constants.md)      | Le pubblicazioni online cambiano rapidamente. Un amministratore delegato della casa editrice esamina le tendenze degli ultimi cinque anni e le relative implicazioni. |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMDuration](metadata-constants.md)         | 120325445                                                                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md) | Thur, 1 giugno 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMFileSize](metadata-constants.md)         | 10329011                                                                                                                            |
| [g \_ wszWMDMFormatCode](metadata-constants.md)       | WMDM \_ FORMATCODE \_ MP3                                                                                                               |
| [g \_ wszWMDMGenre](metadata-constants.md)            | Notizie                                                                                                                                |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md) | Thur, 1 giugno 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMMediaGuid](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMTitle](metadata-constants.md)            | Pubblicazione digitale                                                                                                             |
| [g \_ wszWMDMYear](metadata-constants.md)             | Thur, 1 giugno 2006 14:00:28 EDT                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Costanti dei metadati**](metadata-constants.md)
</dt> </dl>

 

 




