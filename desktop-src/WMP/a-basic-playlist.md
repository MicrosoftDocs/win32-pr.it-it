---
title: Elenco di riproduzione di base
description: Elenco di riproduzione di base
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
keywords:
- Windows playlist di metafile multimediali, esempi di playlist
- playlist, esempi di playlist
- playlist di metafile, esempi di playlist
- Windows Playlist di metafile multimediali, playlist di esempio
- playlist, playlist di esempio
- playlist di metafile, playlist di esempio
- Windows playlist di metafile multimediali, playlist di esempio
- playlist, playlist di esempio
- playlist di metafile, playlist di esempio
- Windows Playlist di metafile multimediali, esempio di codice
- playlist, esempio di codice
- playlist di metafile, esempio di codice
- Windows Playlist di metafile multimediali, esempio di playlist di base
- playlist, esempio di playlist di base
- playlist di metafile, esempio di playlist di base
- Windows Media Player,esempi di playlist
- Windows Media Player,playlist di esempio
- Windows Media Player,playlist di esempio
- Windows Media Player,esempio di playlist di base
- Esempi di playlist
- playlist di esempio
- playlist di esempio
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c8284acfe86cb204293902c0fb8664e74b12f3d2cc176d762f1aff079faac0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004581"
---
# <a name="a-basic-playlist"></a>Elenco di riproduzione di base

L'esempio di playlist seguente mostra un set di base di elementi della playlist. Quando si scrive codice personalizzato, è necessario modificare tutti gli URL e i nomi di file in nomi di file validi accessibili per l'Windows Media Player.

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



Nella tabella seguente vengono fornite informazioni dettagliate sull'uso di ogni elemento nel codice di esempio.



| A linee                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<ASX version = "3.0">                                                                     | [L'elemento ASX](asx-element.md) identifica per il client (Windows Media Player) che si tratta di una playlist Windows metafile multimediale. **L'attributo** version specifica il numero di versione degli elementi del metafile.                                                                                                                                                                                                                                                                                                                                           |
| \<TITLE>Demo playlist di base\</TITLE>                                                  | [L'elemento TITLE](title-element--metafile.md) identifica il titolo dell'intera playlist. Windows Media Player questi metadati vengono visualizzati come titolo della presentazione.                                                                                                                                                                                                                                                                                                                                                                                               |
| \<ENTRY>                                                                                   | Avvia [l'elemento ENTRY.](entry-element.md) Un **elemento ENTRY** è un modo per definire un clip specifico in una playlist                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<TITLE>Voce in una playlist di base\</TITLE>                                         | Identifica il titolo del clip della playlist. È diverso dall'elemento TITLE precedente **perché** è annidato all'interno di un **elemento ENTRY.** Windows Media Player questi metadati vengono visualizzati come titolo del clip.                                                                                                                                                                                                                                                                                                                                         |
| \<AUTHOR>Microsoft Corporation\</AUTHOR>                                              | [L'elemento AUTHOR](author-element.md) identifica l'autore del clip multimediale. Windows Media Player questi metadati vengono visualizzati come CLIP **AUTHOR.**                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<!-- This is a comment. Change the following path to point to your Windows media file --> | Un commento. [I commenti](comments.md) sono visibili solo quando il codice viene visualizzato e hanno lo stesso formato dei **commenti XML.**                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \<REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | Puntatore effettivo al file multimediale. [L'elemento REF](ref-element.md) identifica la riga come puntatore al contenuto multimediale, mentre l'attributo **HREF** è l'URL del file multimediale. In questo caso, l'URL usa il protocollo MMS, quindi punta a un server Windows Media. I file multimediali nel server multimediale non vengono in genere mantenuti nella stessa posizione dei documenti HTML.<br/> Si noti l'uso della chiusura simile a XML dell'elemento , "/>", anziché " &lt; /REF &gt; ". Poiché questo elemento non dispone di elementi figlio, si chiude.<br/> |
| \</ENTRY>                                                                                  | Specifica la fine **dell'elemento ENTRY.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \</ASX>                                                                                    | Specifica la fine della playlist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist metafile**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlist di esempio**](example-playlists.md)
</dt> <dt>

[**Playlist metafile**](metafile-playlists.md)
</dt> <dt>

[**Windows Informazioni di riferimento su elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guida al metafile multimediale**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





