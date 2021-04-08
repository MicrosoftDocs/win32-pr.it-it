---
title: Supporto tag ID3
description: Supporto tag ID3
ms.assetid: 57119b88-5901-4bea-abf6-a67fe71afd1b
keywords:
- Windows Media Format SDK, attributi
- ASF (Advanced Systems Format), attributi
- ASF (formato avanzato dei sistemi), attributi
- attributi, tag ID3
- Tag ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f3dd91119aedf2983e654b4925231b8fd9e4b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045135"
---
# <a name="id3-tag-support"></a>Supporto tag ID3

La tabella seguente elenca tutti gli attributi che corrispondono ai tag ID3. Se si vogliono usare i tag ID3 come attributi anziché usare i nomi di attributo standard, aggiungere il prefisso "ID3/" al nome del tag. Ad esempio, "ID3/TPE2" equivale a **Author**.



| Attributo                      | ID3v1. x | ID3v 2.2 | ID3v 2.3/v 2.4 |
|--------------------------------|---------|---------|--------------|
| **Autore**                     | Artista  | TP1     | TPE1         |
| **Copyright**                  |         | TCR     | TCOP         |
| **CopyrightURL**               |         | WCP     | WCOP         |
| **Descrizione**                | Commento | COM     | COMM         |
| **Duration**                   |         | TLE     | TLEN         |
| **FileSize**                   |         |         | TSIZ         |
| **Title**                      | Titolo   | TT2     | TIT2         |
| **WM/AlbumArtist**             |         | TP2     | TPE2         |
| **WM/AlbumSortOrder**          |         |         | TSOA         |
| **WM/AlbumTitle**              | Album   | MI     | TALB         |
| **WM/ArtistSortOrder**         |         |         | TSOP         |
| **WM/AudioFileURL**            |         | WAF     | WOAF         |
| **WM/AudioSourceURL**          |         | WAS     | WOAS         |
| **WM/AuthorURL**               |         | WAR     | WOAR         |
| **WM/BeatsPerMinute**          |         |         | TBPM         |
| **WM/binario**                  |         | GEOGRAFICA     | GEOB         |
| **WM/Commenti**                |         | COM     | COMM         |
| **WM/Composer**                |         | TCM     | TCOM         |
| **WM/conduttore**               |         | TP3     | TPE3         |
| **WM/ContentGroupDescription** |         | TT1     | TIT1         |
| **WM/EncodedBy**               |         | DIECI     | TENC         |
| **WM/EncodingSettings**        |         | TSS     | TSSE         |
| **WM/EncodingTime**            |         |         | TDEN         |
| **WM/GenreID**                 | GenreID | Costo totale di proprietà     | TCON         |
| **WM/InitialKey**              |         |         | TKEY         |
| **WM/ISRC**                    |         |         | TSRC         |
| **WM/lingua**                |         | TLA     | TLAN         |
| **WM/lyrics \_ sincronizzati**    |         | SLT     | SYLT         |
| **WM/MCDI**                    |         |         | MCDI         |
| **WM/ModifiedBy**              |         |         | TPE4         |
| **WM/umore**                    |         |         | TMOO         |
| **WM/OriginalAlbumTitle**      |         | TOTALE     | TOAL         |
| **WM/OriginalArtist**          |         | TOA     | TOPE         |
| **WM/OriginalFilename**        |         | TOF     | TOFN         |
| **WM/OriginalLyricist**        |         | DI     | TOLY         |
| **WM/OriginalReleaseYear**     |         | TOR     | TORY         |
| **WM/PartOfSet**               |         | TPA     | TPOS         |
| **WM/immagine**                 |         | PIC     | APIC         |
| **WM/PlaylistDelay**           |         |         | TDLY         |
| **WM/Publisher**               |         | TPB     | TPUB         |
| **WM/radiostationname**        |         | TRN     | TRSN         |
| **WM/RadioStationOwner**       |         | TRO     | TRSO         |
| **WM/SetSubTitle**             |         |         | TSST         |
| **WM/sottotitolo**                |         | TT3     | TIT3         |
| **WM/testo**                    |         | TXX     | TXXX         |
| **WM/TitleSortOrder**          |         |         | TSOT         |
| **WM/numero**             | Track   | TRK     | TRCK         |
| **WM/UniqueFileIdentifier**    |         | UFI     | UFID         |
| **WM/UserWebURL**              |         | WXX     | WXXX         |
| **WM/writer**                  |         | TXT     | TEXT         |
| **WM/anno**                    | Year    | TYE     | TYER         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi**](attributes.md)
</dt> </dl>

 

 




