---
title: Elemento PLAYER
description: Elemento PLAYER
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Windows Media Player Skin, elemento PLAYER
- Skin, elemento PLAYER
- Elemento PLAYER
- riferimento per Skin, elemento PLAYER
- elementi, lettore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50eb4383eab279c28b75467a9ed803501e7720b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116873"
---
# <a name="player-element"></a>Elemento PLAYER

L'elemento **Player** consente di definire i gestori eventi e di specificare la proprietà **URL** dell'oggetto **Player** in fase di progettazione all'interno di un file di definizione dell'interfaccia. All'interno del codice di script, l'oggetto **Player** è accessibile tramite l'attributo globale **Player** anziché tramite un nome specificato da un attributo **ID** , che non è supportato dall'elemento **Player** .

L'elemento **Player** supporta l'attributo seguente.



| Attributo             | Descrizione                                          |
|-----------------------|------------------------------------------------------|
| [URL](player-url.md) | Specifica o Recupera il nome del file da riprodurre. |



 

L'elemento **Player** può implementare i gestori eventi per gli eventi seguenti generati dall'oggetto **Player** .



| Event                                                                                            | Descrizione                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Si verifica in seguito alla modifica della lingua audio corrente.                                  |
| [responseBuffering](player-player-buffering.md)                                                         | Si verifica all'inizio o alla fine del buffering di Windows Media Player.                       |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | Si verifica in seguito alla modifica del supporto CD.                                                |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Si verifica quando l'elemento corrente viene modificato.                                            |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Si verifica quando l'elemento multimediale corrente diventa disponibile.                            |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Si verifica quando cambia la playlist corrente.                                        |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Si verifica quando l'elemento della playlist corrente diventa disponibile.                         |
| [DomainChange](player-player-domainchange.md)                                                   | Si verifica in seguito alla modifica del dominio DVD.                                              |
| [Error (Errore) (Error (Errore)e)](player-player-error.md)                                                                 | Si verifica quando il controllo Media Player Windows presenta una condizione di errore.             |
| [MarkerHit](player-player-markerhit.md)                                                         | Si verifica quando Windows Media Player rileva un marcatore nella clip.                |
| [MediaChange](player-player-mediachange.md)                                                     | Si verifica quando un elemento multimediale viene modificato.                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | Si verifica quando un valore di attributo viene aggiunto alla libreria.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Si verifica quando viene modificato un valore di attributo nella libreria.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Si verifica quando un valore di attributo viene rimosso dalla libreria.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Si verifica quando l'oggetto **mediacollection** viene modificato.                              |
| [Errore MediaError](player-player-mediaerror.md)                                                       | Si verifica quando l'oggetto **multimediale** presenta una condizione di errore.                         |
| [ModeChange](player-player-modechange.md)                                                       | Si verifica quando si passa dalla modalità casuale alla modalità normale.                           |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Si verifica quando viene avviata la riproduzione di un titolo in un DVD.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Si verifica quando il *lettore*. **openState** modifiche.                                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | Si verifica in seguito alla modifica di una playlist.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Si verifica quando viene apportata una modifica alla raccolta di playlist.                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | Si verifica quando viene aggiunta una playlist alla raccolta di playlist.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Si verifica quando una playlist viene rimossa dalla raccolta di playlist.                  |
| [PlayStateChange](player-player-playstatechange.md)                                             | Si verifica quando il *lettore*. **riproduzione** modifiche.                                      |
| [PositionChange](player-player-positionchange.md)                                               | Si verifica quando il *lettore*. *controlli*. **currentPosition** modifiche.                     |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Si verifica quando Windows Media Player rileva un comando script incorporato in un file. |
| [StatusChange](player-player-statuschange.md)                                                   | Si verifica in seguito alla modifica del valore della proprietà **status** .                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




