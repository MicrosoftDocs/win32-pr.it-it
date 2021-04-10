---
title: Mapping di feed RSS a Windows Media Gestione dispositivi proprietà
description: Mapping di feed RSS a Windows Media Gestione dispositivi proprietà
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Media Gestione dispositivi, feed RSS
- Gestione dispositivi, feed RSS
- Guida per programmatori, feed RSS
- applicazioni desktop, feed RSS
- creazione di applicazioni Windows Media Gestione dispositivi, feed RSS
- Feed RSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a81d52b4099d77542963d2e87ae5b7dc26b034
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855573"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a>Mapping di feed RSS a Windows Media Gestione dispositivi proprietà

Windows Media Player 11 fornisce una funzionalità di aggregatore RSS che consente agli utenti di archiviare contenuti ottenuti da podcast nei propri computer. In questo argomento vengono descritti gli elementi XML disponibili in un feed RSS. Inoltre, esegue il mapping di questi elementi RSS a Windows Media Gestione dispositivi proprietà.

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



La tabella seguente elenca gli elementi del canale in un feed RSS e le proprietà Windows Media Gestione dispositivi corrispondenti.



| Elemento Channel | Stato         | Proprietà Gestione dispositivi Windows Media corrispondente   |
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
| textInput       | Non applicabile | Non applicabile                                        |
| title           | Necessario       | [g \_ wszWMDMTitle](metadata-constants.md)             |
| ttl             | Facoltativo       | [g \_ wszWMDMTimeToLive](metadata-constants.md)        |
| webMaster       | Facoltativo       | [g \_ wszWMDMWebMaster](metadata-constants.md)         |



 

La tabella seguente elenca gli elementi immagine in un feed RSS e le proprietà WMDM corrispondenti.



| Elemento Image | Stato   | Proprietà Gestione dispositivi Windows Media corrispondente |
|---------------|----------|-----------------------------------------------------|
| description   | Facoltativo | [g \_ wszWMDMDescription](metadata-constants.md)     |
| altezza        | Facoltativo | [g \_ wszWMDMHeight](metadata-constants.md)          |
| link          | Facoltativo | [g \_ wszWMDMDestinationURL](metadata-constants.md)  |
| title         | Facoltativo | [g \_ wszWMDMTitle](metadata-constants.md)           |
| url           | Facoltativo | [g \_ wszWMDMSourceURL](metadata-constants.md)       |
| width         | Facoltativo | [g \_ wszWMDMWidth](metadata-constants.md)           |



 

Nella tabella seguente sono elencati gli elementi elemento in un feed RSS e le proprietà corrispondenti di Windows Media Gestione dispositivi.



| Elemento Item | Attributo   | Stato         | Proprietà Gestione dispositivi Windows Media corrispondente            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| author       |             | Facoltativo       | [g \_ wszWMDMAuthor](metadata-constants.md)                     |
| category     |             | Facoltativo       | [g \_ wszWMDMGenre](metadata-constants.md)                      |
|              | dominio      | Non applicabile | Non applicabile                                                 |
| description  |             | Facoltativo       | [g \_ wszWMDMDescription](metadata-constants.md)                |
| recinto    |             | Facoltativo       | Non applicabile                                                 |
|              | length      | Necessario       | [g \_ wszWMDMFileSize](metadata-constants.md)                   |
|              | type        | Obbligatoria       | (Il tipo MIME deve essere mappato al tipo di contenuto della proprietà). |
|              | url         | Necessario       | [g \_ wszWMDMSourceURL](metadata-constants.md)                  |
| guid         |             | Facoltativo       | [g \_ wszWMDMediaGuid](metadata-constants.md)                   |
|              | PermaLink | Non applicabile | Non applicabile                                                 |
| link         |             | Facoltativo       | [g \_ wszWMDMDestinationURL](metadata-constants.md)             |
| pubDate      |             | Facoltativo       | [g \_ wszWMDMYear](metadata-constants.md)                       |
| source       |             | Non applicabile | Non applicabile                                                 |
| title        |             | Facoltativo       | [g \_ wszWMDMTitle](metadata-constants.md)                      |



 

Esempio

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



Mapping di elementi del canale RSS a Windows Media Gestione dispositivi valori delle proprietà

Nella tabella seguente viene descritto in che modo i valori negli elementi del canale RSS nell'esempio precedente vengono mappati a specifiche proprietà di Windows Media Gestione dispositivi.



| Windows Media Gestione dispositivi proprietà                    | Valore                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthorDate](metadata-constants.md)           | Venerdì, 9 giugno 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMDESCRIPTION](metadata-constants.md)          | Il CEO della pubblicazione di Lucerne Peter Bankov esamina le tendenze più recenti nelle pubblicazioni online. |
| [\_URL wszWMDMDESTINATION \_ g](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [g \_ wszWMDMEDITOR](metadata-constants.md)               | someone@example.com                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md)     | Venerdì, 9 giugno 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMFileName](metadata-constants.md)             | Pubblicazione digitale                                                                       |
| [g \_ wszWMDMFileSize](metadata-constants.md)             | 13.790                                                                                        |
| [g \_ wszWMDMFormatCode](metadata-constants.md)           | \_ \_ cast multimediale WMDM \_ FORMATCODE                                                                 |
| [g \_ wszWMDMGENRE](metadata-constants.md)                | Notizie                                                                                          |
| [g \_ wszWMDMLAST \_ Data di modifica \_](metadata-constants.md) | Venerdì, 9 giugno 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md)     | Venerdì, 9 giugno 2006 14:00:28 EDT                                                                 |
| [g \_ wszWMDMProviderCopyright](metadata-constants.md)    | 2006 Lucerne Publishing LP, LLLP. All Rights Reserved.                                        |
| [g \_ wszWMDMTimeToLive](metadata-constants.md)           | 240                                                                                           |
| [g \_ wszWMDMTitle](metadata-constants.md)                | Pubblicazione digitale                                                                       |
| [g \_ wszWMDMWEBMASTER](metadata-constants.md)            | someone@example.com                                                                           |
| [g \_ wszWMDMYear](metadata-constants.md)                 | Venerdì, 9 giugno 2006 14:00:28 EDT                                                                 |



 

Mapping di elementi immagine RSS a Windows Media Gestione dispositivi valori delle proprietà

Nella tabella seguente viene descritto in che modo i valori negli elementi immagine RSS nell'esempio precedente vengono mappati a specifiche proprietà di Windows Media Gestione dispositivi.



| Windows Media Gestione dispositivi proprietà                | Valore                                            |
|------------------------------------------------------|--------------------------------------------------|
| [g \_ wszWMDMAlbumCoverFormat](metadata-constants.md) | \_ \_ GIF formato oggetto \_ WPD                         |
| [g \_ wszWMDMAlbumCoverSize](metadata-constants.md)   | 512                                              |
| [g \_ wszWMDMDescription](metadata-constants.md)      | Logo Lucerne                                     |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | www.lucernepublishing.com/community/podcasts   |
| [g \_ wszWMDMHeight](metadata-constants.md)           | 300                                              |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [g \_ wszWMDMTitle](metadata-constants.md)            | Pubblicazione di Lucerne                               |
| [g \_ wszWMDMWidth](metadata-constants.md)            | 300                                              |



 

Mapping di elementi elemento RSS a Windows Media Gestione dispositivi valori delle proprietà

Nella tabella seguente viene descritto in che modo i valori negli elementi RSS dell'esempio precedente vengono mappati a specifiche proprietà di Windows Media Gestione dispositivi.



| Windows Media Gestione dispositivi proprietà                | Valore                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [g \_ wszWMDMAuthor](metadata-constants.md)           | Lucerna                                                                                                                             |
| [g \_ wszWMDMAuthorDate](metadata-constants.md)       | Gio, 1 giugno 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMDescription](metadata-constants.md)      | Le pubblicazioni online sono in rapida evoluzione. Un CEO della casa di pubblicazione esamina le tendenze degli ultimi cinque anni e le loro implicazioni. |
| [g \_ wszWMDMDestinationURL](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMDuration](metadata-constants.md)         | 120325445                                                                                                                           |
| [g \_ wszWMDMFileCreationDate](metadata-constants.md) | Gio, 1 giugno 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMFileSize](metadata-constants.md)         | 10329011                                                                                                                            |
| [g \_ wszWMDMFormatCode](metadata-constants.md)       | WMDM \_ FORMATCODE \_ MP3                                                                                                               |
| [g \_ wszWMDMGenre](metadata-constants.md)            | Notizie                                                                                                                                |
| [g \_ wszWMDMLastModifiedDate](metadata-constants.md) | Gio, 1 giugno 2006 14:00:28 EDT                                                                                                      |
| [g \_ wszWMDMMediaGuid](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMSourceURL](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ wszWMDMTitle](metadata-constants.md)            | Pubblicazione digitale                                                                                                             |
| [g \_ wszWMDMYear](metadata-constants.md)             | Gio, 1 giugno 2006 14:00:28 EDT                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Costanti dei metadati**](metadata-constants.md)
</dt> </dl>

 

 




