---
title: Una playlist di base
description: Una playlist di base
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
keywords:
- Playlist Windows Media Metafile, esempi di playlist
- playlist, esempi di playlist
- playlist di metafile, esempi di playlist
- Playlist Windows Media Metafile, playlist di esempio
- playlist, playlist di esempio
- playlist di metafile, playlist di esempio
- Playlist Windows Media Metafile, playlist di esempio
- playlist, playlist di esempio
- playlist di metafile, playlist di esempio
- Playlist Windows Media Metafile, esempio di codice
- playlist, esempio di codice
- playlist di metafile, esempio di codice
- Playlist Windows Media Metafile, esempio di playlist di base
- playlist, esempio di playlist di base
- playlist di metafile, esempio di playlist di base
- Windows Media Player, esempi di playlist
- Media Player di Windows, playlist di esempio
- Windows Media Player, playlist di esempio
- Windows Media Player, esempio di playlist di base
- esempi di playlist
- playlist di esempio
- playlist di esempio
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 804bc69c9ab3b243030cd2c87545e6362ccfca79
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314784"
---
# <a name="a-basic-playlist"></a>Una playlist di base

Nell'esempio di playlist seguente viene illustrato un set di base di elementi della playlist. Quando si scrive codice personalizzato, è necessario modificare tutti gli URL e i nomi di file in nomi di file validi accessibili al Media Player di Windows.

**Esempio di codice**


```XML
<ASX version = "3.0">
<TITLE>Basic Playlist Demo</TITLE>
    <ENTRY>
        <TITLE>An Entry in a basic playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <REF HREF = "mms://proseware.com/path/Yourfile.wma" />
    </ENTRY>
</ASX>

```



La tabella seguente fornisce informazioni dettagliate sull'uso di ogni elemento nel codice di esempio.



| Linea                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<ASX version = "3.0">                                                                     | L'elemento [ASX](asx-element.md) identifica per il client (Windows Media Player) che si tratta di una playlist Windows Media Metafile. L'attributo **Version** specifica il numero di versione degli elementi del metafile.                                                                                                                                                                                                                                                                                                                                           |
| \<TITLE>Demo di base della playlist\</TITLE>                                                  | L'elemento [title](title-element--metafile.md) identifica il titolo della playlist nel suo complesso. Windows Media Player visualizza questi metadati come titolo di visualizzazione.                                                                                                                                                                                                                                                                                                                                                                                               |
| \<ENTRY>                                                                                   | Inizia l'elemento [entry](entry-element.md) . Un elemento **entry** è un modo per definire una clip specifica in una playlist                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<TITLE>Una voce in una playlist di base\</TITLE>                                         | Identifica il titolo del clip della playlist. È diverso dall'elemento **title** precedente, perché questo è annidato all'interno di un elemento **entry** . Windows Media Player visualizza questi metadati come titolo della clip.                                                                                                                                                                                                                                                                                                                                         |
| \<AUTHOR>Microsoft Corporation\</AUTHOR>                                              | L'elemento [Author](author-element.md) identifica l'autore del clip multimediale. Windows Media Player visualizza questi metadati come **autore** della clip.                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<!-- This is a comment. Change the following path to point to your Windows media file --> | Un commento. I [Commenti](comments.md) sono visibili solo quando viene visualizzato il codice e si trovano nello stesso formato dei commenti **XML** .                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \<REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | Puntatore effettivo al file multimediale. L'elemento [ref](ref-element.md) identifica la riga come puntatore al contenuto multimediale, mentre l'attributo **href** è l'URL del file multimediale. In questo caso, l'URL utilizza il protocollo MMS, in modo che punti a un server Windows Media. I file multimediali nel server multimediale non vengono in genere conservati nello stesso percorso dei documenti HTML.<br/> Si noti l'uso della chiusura di tipo XML dell'elemento "/>" invece di " &lt; /ref &gt; ". Poiché questo elemento non ha elementi figlio, si chiude.<br/> |
| \</ENTRY>                                                                                  | Specifica la fine dell'elemento **entry** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \</ASX>                                                                                    | Specifica la fine della playlist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist di metafile**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlist di esempio**](example-playlists.md)
</dt> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guida ai metafile di Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





