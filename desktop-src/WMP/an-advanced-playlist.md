---
title: Playlist avanzata
description: Playlist avanzata
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
keywords:
- Windows playlist di metafile multimediali, esempi di playlist
- playlist, esempi di playlist
- playlist di metafile, esempi di playlist
- Windows playlist di metafile multimediali, playlist di esempio
- playlist, playlist di esempio
- playlist di metafile, playlist di esempio
- Windows playlist di metafile multimediali, playlist di esempio
- playlist, playlist di esempio
- playlist di metafile, playlist di esempio
- Windows Playlist di metafile multimediali, esempio di codice
- playlist, esempio di codice
- playlist di metafile, esempio di codice
- Windows Playlist di metafile multimediali, esempio di playlist avanzate
- playlist, esempio di playlist avanzata
- playlist di metafile, esempio di playlist avanzate
- Windows Media Player,esempi di playlist
- Windows Media Player,playlist di esempio
- Windows Media Player, playlist di esempio
- Windows Media Player, esempio di playlist avanzata
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
ms.openlocfilehash: 6573d5bef05c8af943368a12d03677526a9783915d6915b6cc5f1516bc9942f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583258"
---
# <a name="an-advanced-playlist"></a>Playlist avanzata

L'esempio di playlist seguente illustra come usare un set più completo di elementi playlist. Quando si scrive codice personalizzato, è necessario modificare tutti gli URL e i nomi di file in nomi di file validi accessibili al Windows Media Player.

Codice di esempio


``` XML
<ASX version = "3.0">
    <TITLE>Advanced Playlist Demo</TITLE>
    <ABSTRACT>More Information at this website</ABSTRACT>
    <MOREINFO HREF="https://www.microsoft.com/windows/windowsmedia" />
    <BANNER HREF = "..\samples\home.gif">
        <ABSTRACT>MSN website</ABSTRACT>
        <MOREINFO HREF = "https://www.msn.com" />
    </BANNER>
    <PARAM name="track" value="1"/>
    <ENTRY ClientSkip="no">
        <BANNER HREF = "..\sample\contact.gif">
            <ABSTRACT>Visit Our website</ABSTRACT>
            <MOREINFO HREF = "https://www.msn.com" />
        </BANNER>
        <MOREINFO HREF = "https://www.msn.com" />
        <!-- This is the ToolTip text for Title/Author/Copyright text -->
        <ABSTRACT>Visit the YourImage website</ABSTRACT>
        <TITLE>The first entry in an advanced playlist</TITLE>
        <AUTHOR>YourImage</AUTHOR>
        <COPYRIGHT>(c)2000 YourImage</COPYRIGHT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
         <REF HREF = "..\media\laure.wma" />
    </ENTRY>

    <ENTRY>
        <TITLE>The second entry in the advanced playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <!-- This is the ToolTip text for Title text -->
        <ABSTRACT>This is where you can include your tool tips</ABSTRACT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
        <REF HREF = "..\media\mellow.wma" />
    </ENTRY>
</ASX>

```



Nella tabella seguente viene descritta la playlist avanzata precedente.



| A linee                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | [L'elemento ASX](asx-element.md) identifica per il client (Windows Media Player) che si tratta di una playlist Windows metafile multimediale. **L'attributo** version specifica il numero di versione degli elementi del metafile.                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | [L'elemento TITLE](title-element--metafile.md) identifica il titolo della playlist nel suo complesso. Windows Media Player visualizza questi metadati come titolo di visualizzazione.                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | [L'elemento ABSTRACT](abstract-element.md) fornisce la descrizione comando per il titolo della visualizzazione.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | [L'elemento MOREINFO](moreinfo-element.md) collega il titolo di visualizzazione a un URL. Se si sosone il puntatore del mouse sul titolo di visualizzazione, si accede alla descrizione comando, se definita. Se si seleziona il titolo di visualizzazione, verrà aperto l'URL designato.                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | [L'elemento BANNER](banner-element.md) crea un banner pubblicitario in Windows Media Player. **L'attributo HREF** specifica l'immagine del banner (che deve avere una larghezza di 194 pixel per 32 pixel di altezza).                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | [L'elemento ABSTRACT](abstract-element.md) fornisce la descrizione comando per **banner.**                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | [L'elemento MOREINFO](moreinfo-element.md) collega **l'immagine BANNER** a un URL. Se si tiene premuto il puntatore del **mouse sull'intestazione,** si accede a una descrizione comando, se definita. Selezionando banner **verrà** aperto l'URL designato.                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | [L'elemento PARAM](param-element.md) definisce un parametro personalizzato. **L'attributo** name definisce il nome del parametro personalizzato come "track". **L'attributo** value definisce il valore di "track" come "1".                                                                                                                          |
| `</BANNER>`                                                                                 | Chiude **l'elemento BANNER**                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | Avvia il blocco di elementi [ENTRY.](entry-element.md) Questo elemento definisce un clip in una playlist specificando un collegamento **nell'elemento REF.** **L'impostazione di ClientSkip** su "no" significa che l'utente non può andare avanti o passare al clip successivo                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | Crea un banner pubblicitario. HREF **è** l'immagine del banner (194x32 pixel).                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | Fornisce la descrizione comando per il banner.                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Fornisce un collegamento all'URL per il banner. La selezione del banner consente di connettersi all'URL.                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | Chiude **l'elemento BANNER**                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Fornisce un collegamento all'URL per il testo del titolo **del** clip.                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | Un commento. [I commenti](comments.md) sono visibili solo quando viene visualizzato il codice.                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | Fornisce la descrizione comando per il testo del **titolo del** clip.                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | Identifica il titolo del clip. Si tratta del titolo del clip **perché** è annidato all'interno di un **elemento ENTRY.** Windows Media Player visualizza questi metadati come titolo del clip.                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | Identifica l'autore del clip multimediale. Questi metadati vengono visualizzati come **AUTHOR** di clip Windows Media Player.                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | [L'elemento COPYRIGHT](copyright-element.md) specifica i copyright associati al clip multimediale. Windows Media Player visualizza questi metadati come copyright della clip.                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Commento, nello stesso formato dei **commenti XML.**                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | URL per il contenuto multimediale. [L'elemento REF](ref-element.md) identifica la riga come puntatore al contenuto multimediale. **L'attributo HREF** è l'URL del file. Si noti l'uso della chiusura simile a XML dell'elemento , "/>" anziché " &lt; /REF &gt; ". Poiché questo elemento non dispone di elementi figlio, si chiude.<br/> |
| `</ENTRY>`                                                                                  | Specifica la fine dell'elemento del primo **elemento ENTRY.**                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | Inizia il secondo **elemento ENTRY.**                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | Identifica il titolo del secondo clip.                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | Identifica l'autore del secondo clip multimediale.                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | Un commento. Sarà visibile solo quando viene visualizzato il codice.                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | Si tratta del testo della descrizione comando per **il testo TITLE** del clip.                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Un commento. Sarà visibile solo quando viene visualizzato il codice.                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | Identifica la riga come puntatore al contenuto multimediale. **L'attributo HREF** è l'URL del file.                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | Specifica la fine del secondo **elemento ENTRY.**                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | Specifica la fine della playlist.                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist di metafile**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlist di esempio**](example-playlists.md)
</dt> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guida ai metafile multimediali**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





