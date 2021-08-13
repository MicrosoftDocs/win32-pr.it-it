---
title: Supporto tag ID3
description: Supporto tag ID3
ms.assetid: 57119b88-5901-4bea-abf6-a67fe71afd1b
keywords:
- Windows MEDIA Format SDK,attributi
- Advanced Systems Format (ASF), attributi
- ASF (Advanced Systems Format), attributi
- attributi,tag ID3
- Id3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28fd65ffadb952e9370af609e336c08fc07c9b96f50d09d95c78492bef2163db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118703026"
---
# <a name="id3-tag-support"></a>Supporto tag ID3

Nella tabella seguente sono elencati tutti gli attributi che corrispondono ai tag ID3. Se si vogliono usare i tag ID3 come attributi anziché usare i nomi degli attributi standard, aggiungere il prefisso "ID3/" al nome del tag. Ad esempio, "ID3/TPE2" equivale a **Author**.



| Attributo                      | ID3v1.x | ID3v2.2 | ID3v2.3/v2.4 |
|--------------------------------|---------|---------|--------------|
| **Autore**                     | Artista  | TP1     | TPE1         |
| **Copyright**                  |         | Tcr     | TCOP         |
| **CopyrightURL**               |         | Wcp     | WCOP         |
| **Descrizione**                | Commento | COM     | COMM         |
| **Duration**                   |         | Tle     | TLEN         |
| **Dimensione**                   |         |         | TSIZ         |
| **Title**                      | Title   | TT2     | TIT2         |
| **WM/AlbumArtist**             |         | TP2     | TPE2         |
| **WM/AlbumSortOrder**          |         |         | TSOA         |
| **WM/AlbumTitle**              | Album   | TAL     | TALB         |
| **WM/ArtistSortOrder**         |         |         | Tsop         |
| **WM/AudioFileURL**            |         | WAF     | WOAF         |
| **WM/AudioSourceURL**          |         | WAS     | WOAS         |
| **WM/AuthorURL**               |         | WAR     | WOAR         |
| **WM/BeatsPerMinute**          |         |         | TBPM         |
| **WM/Binary**                  |         | Geo     | GEOB         |
| **WM/Comments**                |         | COM     | COMM         |
| **WM/Composer**                |         | TCM     | TCOM         |
| **WM/Conductor**               |         | TP3     | TPE3         |
| **WM/ContentGroupDescription** |         | TT1     | TIT1         |
| **WM/EncodedBy**               |         | Dieci     | TENC         |
| **WM/EncodingSettings**        |         | Tss     | TSSE         |
| **WM/EncodingTime**            |         |         | TDEN         |
| **WM/GenreID**                 | GenreID | Costo totale di proprietà     | Tcon         |
| **WM/InitialKey**              |         |         | Tkey         |
| **WM/ISRC**                    |         |         | TSRC         |
| **WM/Language**                |         | Tla     | Tlan         |
| **WM/Lyrics \_ Synchronised**    |         | Slt     | Sylt         |
| **WM/MCDI**                    |         |         | MCDI         |
| **WM/ModifiedBy**              |         |         | TPE4         |
| **WM/Wm/Wm**                    |         |         | TMOO         |
| **WM/OriginalAlbumTitle**      |         | Tot     | TOAL         |
| **WM/OriginalArtist**          |         | Toa     | Tope         |
| **WM/OriginalFilename**        |         | Tof     | TOFN         |
| **WM/OriginalLyricist**        |         | Tol     | TOLY         |
| **WM/OriginalReleaseYear**     |         | Tor     | Tory         |
| **WM/PartOfSet**               |         | Tpa     | TPOS         |
| **WM/Picture**                 |         | Pic     | APIC         |
| **WM/PlaylistDelay**           |         |         | TDLY         |
| **WM/Publisher**               |         | Tpb     | TPUB         |
| **WM/RadioStationName**        |         | Trn     | TRSN         |
| **WM/RadioStationOwner**       |         | TRO     | TRSO         |
| **WM/SetSubTitle**             |         |         | Tsst         |
| **WM/SubTitle**                |         | TT3     | TIT3         |
| **WM/Text**                    |         | TXX     | TXXX         |
| **WM/TitleSortOrder**          |         |         | TSOT         |
| **WM/TrackNumber**             | Track   | TRK     | TRCK         |
| **WM/UniqueFileIdentifier**    |         | Ufi     | UFID         |
| **WM/UserWebURL**              |         | WXX     | WXXX         |
| **WM/Writer**                  |         | TXT     | TEXT         |
| **WM/Year**                    | Year    | Tye     | TYER         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi**](attributes.md)
</dt> </dl>

 

 




