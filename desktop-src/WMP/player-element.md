---
title: Elemento PLAYER
description: Elemento PLAYER
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Windows Media Player, elemento PLAYER
- skins,PLAYER - elemento
- PLAYER - elemento
- riferimento per le interfaccia, elemento PLAYER
- elementi, PLAYER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bef2e7758a0146ae6197d17dc3790011a758f9d2fa4e3d54af9461a8b870c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338117"
---
# <a name="player-element"></a>Elemento PLAYER

**L'elemento PLAYER** consente di definire i gestori eventi e specificare la proprietà **URL** dell'oggetto **Player** in fase di progettazione all'interno di un file di definizione dell'interfaccia. All'interno del codice di script, l'accesso all'oggetto **Player** viene eseguito tramite l'attributo globale del lettore anziché tramite un nome specificato da un **attributo id,** che non è supportato dall'elemento **PLAYER.** 

**L'elemento PLAYER** supporta l'attributo seguente.



| Attributo             | Descrizione                                          |
|-----------------------|------------------------------------------------------|
| [URL](player-url.md) | Specifica o recupera il nome del file da riprodurre. |



 

**L'elemento PLAYER** può implementare gestori eventi per gli eventi seguenti generati dall'oggetto **Player.**



| Event                                                                                            | Descrizione                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Si verifica quando cambia la lingua audio corrente.                                  |
| [responseBuffering](player-player-buffering.md)                                                         | Si verifica quando Windows Media Player inizia o termina la memorizzazione nel buffer.                       |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | Si verifica quando il supporto CD viene modificato.                                                |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Si verifica quando l'elemento corrente viene modificato.                                            |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Si verifica quando l'elemento multimediale corrente diventa disponibile.                            |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Si verifica quando cambia la playlist corrente.                                        |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Si verifica quando l'elemento della playlist corrente diventa disponibile.                         |
| [DomainChange](player-player-domainchange.md)                                                   | Si verifica quando il dominio DVD viene modificato.                                              |
| [Error (Errore) (Error (Errore)e)](player-player-error.md)                                                                 | Si verifica quando il Windows Media Player controllo presenta una condizione di errore.             |
| [MarkerHit](player-player-markerhit.md)                                                         | Si verifica Windows Media Player rileva un marcatore nella clip.                |
| [MediaChange](player-player-mediachange.md)                                                     | Si verifica quando viene modificato un elemento multimediale.                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | Si verifica quando un valore di attributo viene aggiunto alla libreria.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Si verifica quando viene modificato un valore di attributo nella libreria.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Si verifica quando un valore di attributo viene rimosso dalla libreria.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Si verifica quando **l'oggetto MediaCollection** viene modificato.                              |
| [MediaError](player-player-mediaerror.md)                                                       | Si verifica quando **l'oggetto Media** presenta una condizione di errore.                         |
| [ModeChange](player-player-modechange.md)                                                       | Si verifica quando si passa dalla modalità casuale alla modalità normale.                           |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Si verifica quando inizia la riproduzione di un titolo in un DVD.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Si verifica quando il *lettore*. **Modifiche di openState.**                                      |
| [Modifica playlist](player-player-playlistchange.md)                                               | Si verifica quando viene modificata una playlist.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Si verifica quando viene modificato un elemento nell'insieme di playlist.                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | Si verifica quando una playlist viene aggiunta all'insieme di playlist.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Si verifica quando una playlist viene rimossa dall'insieme di playlist.                  |
| [PlayStateChange](player-player-playstatechange.md)                                             | Si verifica quando il *lettore*. **Modifiche di playState.**                                      |
| [PositionChange](player-player-positionchange.md)                                               | Si verifica quando il *lettore*. *controlla*. **CurrentPosition** cambia.                     |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Si verifica Windows Media Player rileva un comando script incorporato in un file. |
| [StatusChange](player-player-statuschange.md)                                                   | Si verifica quando il **valore della proprietà** di stato viene modificato.                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




