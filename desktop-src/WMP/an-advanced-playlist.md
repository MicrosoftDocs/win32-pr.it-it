---
title: Una playlist avanzata
description: Una playlist avanzata
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
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
- Playlist Windows Media Metafile, esempio di playlist avanzato
- playlist, esempio di playlist avanzato
- playlist di metafile, esempio di playlist avanzato
- Windows Media Player, esempi di playlist
- Media Player di Windows, playlist di esempio
- Windows Media Player, playlist di esempio
- Esempio di Windows Media Player, playlist avanzata
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
ms.openlocfilehash: f52251fedb13d41be5c94706bee4460c3f13c1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044504"
---
# <a name="an-advanced-playlist"></a>Una playlist avanzata

Nell'esempio di playlist seguente viene illustrato come usare un set più completo di elementi della playlist. Quando si scrive codice personalizzato, è necessario modificare tutti gli URL e i nomi di file in nomi di file validi accessibili al Media Player di Windows.

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



La tabella seguente descrive la playlist avanzata precedente.



| Linea                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | L'elemento [ASX](asx-element.md) identifica per il client (Windows Media Player) che si tratta di una playlist Windows Media Metafile. L'attributo **Version** specifica il numero di versione degli elementi del metafile.                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | L'elemento [title](title-element--metafile.md) identifica il titolo della playlist nel suo complesso. Windows Media Player visualizza questi metadati come titolo di visualizzazione.                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | L'elemento [astratto](abstract-element.md) fornisce la descrizione comando per il titolo di visualizzazione.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | L'elemento [moreinfo](moreinfo-element.md) collega il titolo show a un URL. La sospensione del puntatore del mouse sul titolo Show accede alla descrizione comando, se definita. Selezionando Mostra titolo verrà aperto l'URL designato.                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | L'elemento [banner](banner-element.md) crea un banner pubblicitario in Windows Media Player. L'attributo **href** specifica l'icona del banner (che deve essere 194 pixel di larghezza per 32 pixel di altezza).                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | L'elemento [astratto](abstract-element.md) fornisce la descrizione comando per l' **intestazione**.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | L'elemento [moreinfo](moreinfo-element.md) collega l'icona del **banner** a un URL. Il puntatore del mouse sul **banner** accede a una descrizione comando, se definita. Se si seleziona il **banner** , viene aperto l'URL designato.                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | L'elemento [param](param-element.md) definisce un parametro personalizzato. L'attributo **Name** definisce il nome del parametro personalizzato come "Track". L'attributo **value** definisce il valore di "Track" come "1".                                                                                                                          |
| `</BANNER>`                                                                                 | Chiude l'elemento **banner**                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | Inizia il blocco dell'elemento [entry](entry-element.md) . Questo elemento definisce una clip in una playlist specificando un collegamento nell'elemento **ref** . Impostando **ClientSkip** su "No" si indica che l'utente non può eseguire rapidamente l'avanzamento o passare alla clip successiva                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | Crea un banner pubblicitario. **Href** è la rappresentazione grafica del banner (194x32 pixel).                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | Fornisce la descrizione comando per l'intestazione.                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Fornisce un collegamento all'URL per il banner. La selezione del banner si connette all'URL.                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | Chiude l'elemento **banner**                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Fornisce un collegamento all'URL per il testo del **titolo** della clip.                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | Un commento. I [Commenti](comments.md) sono visibili solo quando viene visualizzato il codice.                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | Fornisce la descrizione comando per il testo del **titolo** della clip.                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | Identifica il titolo della clip. Si tratta del **titolo** della clip perché è annidato all'interno di un elemento **entry** . Windows Media Player visualizza questi metadati come titolo della clip.                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | Identifica l'autore del clip multimediale. Questi metadati vengono visualizzati come **autore** della clip da Windows Media Player.                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | L'elemento [Copyright](copyright-element.md) specifica i copyright associati al clip multimediale. Windows Media Player visualizza questi metadati come clip COPYRIGHT.                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Commento, nello stesso formato dei commenti **XML** .                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | URL per il contenuto multimediale. L'elemento [ref](ref-element.md) identifica la riga come puntatore al contenuto multimediale. L'attributo **href** è l'URL del file. Si noti l'uso della chiusura di tipo XML dell'elemento "/>" invece di " &lt; /ref &gt; ". Poiché questo elemento non ha elementi figlio, si chiude.<br/> |
| `</ENTRY>`                                                                                  | Specifica la fine dell'elemento del primo elemento **entry** .                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | Inizia il secondo elemento **entry** .                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | Identifica il titolo del secondo clip.                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | Identifica l'autore del secondo clip multimediale.                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | Un commento. Sarà visibile solo quando viene visualizzato il codice.                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | Testo della descrizione comando per il testo del **titolo** della clip.                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Un commento. Sarà visibile solo quando viene visualizzato il codice.                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | Identifica la riga come puntatore al contenuto multimediale. L'attributo **href** è l'URL del file.                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | Specifica la fine del secondo elemento **entry** .                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | Specifica la fine della playlist.                                                                                                                                                                                                                                                                                                      |



 

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

 

 





