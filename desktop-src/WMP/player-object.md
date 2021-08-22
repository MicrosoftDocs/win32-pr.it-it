---
title: Oggetto Player
description: L'oggetto Player è l'oggetto radice per il Windows Media Player controllo . Supporta le proprietà, i metodi e gli eventi elencati nelle tabelle seguenti.
ms.assetid: 694bd6cc-c816-478a-87b9-1526e2d18869
keywords:
- Oggetto Player Windows Media Player
topic_type:
- apiref
api_name:
- Player Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ee314862aad1237036d5a7fa6a5627f42a6185d1ab6914f1e11ec19a831b755
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616701"
---
# <a name="player-object"></a>Oggetto Player

L'oggetto Player è l'oggetto radice per il Windows Media Player controllo . Supporta le proprietà, i metodi e gli eventi elencati nelle tabelle seguenti.

L'oggetto Player supporta le proprietà seguenti. Le proprietà contrassegnate con un asterisco ( \* ) non sono accessibili alle interfaccia.



| Proprietà                                             | Descrizione                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [CdromCollection](player-cdromcollection.md)        | Recupera [l'oggetto CdromCollection.](cdromcollection-object.md)                                                                          |
| [closedCaption](player-closedcaption.md)            | Recupera [l'oggetto ClosedCaption.](closedcaption-object.md)                                                                              |
| [Controlli](player-controls.md)                      | Recupera [l'oggetto Controls.](controls-object.md)                                                                                        |
| [currentMedia](player-currentmedia.md)              | Specifica o recupera l'oggetto [Media](media-object.md) corrente.                                                                         |
| [currentPlaylist](player-currentplaylist.md)        | Specifica o recupera l'oggetto [Playlist](playlist-object.md) corrente.                                                                   |
| [Dvd](player-dvd.md)                                | Recupera [l'oggetto DVD.](dvd-object.md)                                                                                                  |
| [enableContextMenu](player-enablecontextmenu.md)\* | Specifica o recupera un valore che indica se abilitare il menu di scelta rapida, che viene visualizzato quando si fa clic con il pulsante destro del mouse.          |
| [abilitata](player-enabled.md) \*                     | Specifica o recupera un valore che indica se il controllo Windows Media Player è abilitato.                                               |
| [error](player-error.md)                            | Recupera [l'oggetto Error.](error-object.md)                                                                                              |
| [fullScreen](player-fullscreen.md)\*               | Specifica o recupera un valore che indica se il contenuto video viene riprodotto in modalità schermo intero.                                          |
| [isOnline](player-isonline.md)                      | Recupera un valore che indica se l'utente è connesso a una rete.                                                                     |
| [isRemote](player-isremote.md)\*                   | Recupera un valore che indica se il controllo Windows Media Player è in esecuzione in modalità remota.                                             |
| [mediaCollection](player-mediacollection.md)        | Recupera [l'oggetto MediaCollection.](mediacollection-object.md)                                                                          |
| [Rete](player-network.md)                        | Recupera [l'oggetto Network.](network-object.md)                                                                                          |
| [openState](player-openstate.md)                    | Recupera un valore che indica lo stato dell'origine del contenuto.                                                                                |
| [playerApplication](player-playerapplication.md)\* | Recupera [l'oggetto PlayerApplication](playerapplication-object.md) quando è in esecuzione Windows Media Player remoto.               |
| [playlistCollection](player-playlistcollection.md)  | Recupera [l'oggetto PlaylistCollection.](playlistcollection-object.md)                                                                    |
| [playState](player-playstate.md)                    | Recupera un valore che indica lo stato dell'Windows Media Player'operazione.                                                                |
| [impostazioni](player-settings.md)                      | Recupera [l'Impostazioni](settings-object.md) corrente.                                                                                        |
| [Stato](player-status.md)                          | Recupera un valore che indica lo stato corrente di Windows Media Player.                                                                     |
| [stretchToFit](player-stretchtofit.md)\*           | Specifica o recupera un valore che indica se il video verrà adattato alle dimensioni della visualizzazione video Windows Media Player controllo video.          |
| [uiMode](player-uimode.md)\*                       | Specifica o recupera un valore che indica quali controlli vengono visualizzati nell'interfaccia utente quando Windows Media Player è incorporato in una pagina Web. |
| [URL](player-url.md)                                | Specifica o recupera il nome del clip da riprodurre.                                                                                         |
| [versionInfo](player-versioninfo.md)                | Recupera un valore String che specifica la versione del Windows Media Player.                                                                 |
| [windowlessVideo](player-windowlessvideo.md)\*     | Specifica o recupera un valore che indica se il controllo Windows Media Player esegue il rendering del video in modalità senza finestra.                         |



 

\* Non accessibile alle interfaccia.

L'oggetto Player supporta i metodi seguenti.



| Metodo                                | Descrizione                                               |
|---------------------------------------|-----------------------------------------------------------|
| [close](player-close.md)             | Rilascia Windows Media Player risorse.                  |
| [launchURL](player-launchurl.md)     | Invia un URL al browser predefinito dell'utente di cui eseguire il rendering. |
| [Newmedia](player-newmedia.md)       | Crea un nuovo [oggetto Media.](media-object.md)           |
| [newPlaylist](player-newplaylist.md) | Crea un nuovo [oggetto Playlist.](playlist-object.md)     |
| [openPlayer](player-openplayer.md)   | Apre Windows Media Player utilizzando l'URL specificato.       |



 

L'oggetto Player supporta gli eventi seguenti. Gli eventi contrassegnati con un asterisco ( \* ) non sono accessibili alle interfaccia. Per informazioni sulla gestione degli eventi del mouse e della tastiera nelle interfaccia, vedere [Eventi esterni.](external-events.md)



| Event                                                                                            | Descrizione                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Si verifica quando cambia la lingua audio corrente.                                  |
| [responseBuffering](player-player-buffering.md)                                                         | Si verifica quando il Windows Media Player inizia o termina la memorizzazione nel buffer.           |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | Si verifica quando un CD o DVD viene inserito o espulso da un'unità CD o DVD.      |
| [Clic](player-player-click.md) \*                                                              | Si verifica quando l'utente fa clic su un pulsante del mouse.                                      |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Si verifica quando *controlla*. **Modifiche a currentItem.**                                  |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Si verifica quando un elemento di metadati grafico nell'elemento multimediale corrente diventa disponibile. |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Si verifica quando un elemento viene modificato all'interno della playlist corrente.                       |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Si verifica quando l'elemento della playlist corrente diventa disponibile.                         |
| **Disconnetti**                                                                                   | Riservato per utilizzi futuri.                                                         |
| [DomainChange](player-player-domainchange.md)                                                   | Si verifica quando il dominio DVD viene modificato.                                              |
| [DoubleClick](player-player-doubleclick.md)\*                                                  | Si verifica quando l'utente fa doppio clic su un pulsante del mouse.                               |
| **DurationUnitChange**                                                                           | Riservato per utilizzi futuri.                                                         |
| **EndOfStream**                                                                                  | Riservato per utilizzi futuri.                                                         |
| [Error (Errore) (Error (Errore)e)](player-player-error.md)                                                                 | Si verifica quando il Windows Media Player controllo presenta una condizione di errore.             |
| [KeyDown](player-player-keydown.md) \*                                                          | Si verifica quando un tasto viene premuto.                                                    |
| [KeyPress](player-player-keypress.md)\*                                                        | Si verifica quando viene premuto e quindi rilasciato un tasto.                                  |
| [KeyUp](player-player-keyup.md) \*                                                              | Si verifica quando si rilascia un tasto.                                                   |
| [MarkerHit](player-player-markerhit.md)                                                         | Si verifica quando viene raggiunto un marcatore.                                                 |
| [MediaChange](player-player-mediachange.md)                                                     | Si verifica quando viene modificato un elemento multimediale.                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | Si verifica quando un valore di attributo viene aggiunto alla libreria.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Si verifica quando viene modificato un valore di attributo nella libreria.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Si verifica quando un valore di attributo viene rimosso dalla libreria.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Si verifica quando l'insieme di supporti viene modificato.                                        |
| [MediaCollectionMediaAdded](player-player-mediacollectionmediaadded.md)                         | Si verifica quando un elemento multimediale viene aggiunto alla libreria locale.                          |
| [MediaCollectionMediaRemoved](player-player-mediacollectionmediaremoved.md)                     | Si verifica quando un elemento multimediale viene rimosso dalla libreria locale.                      |
| [MediaError](player-player-mediaerror.md)                                                       | Si verifica quando **l'oggetto Media** presenta una condizione di errore.                         |
| [ModeChange](player-player-modechange.md)                                                       | Si verifica quando viene modificata una Windows Media Player di .                           |
| [MouseDown](player-player-mousedown.md)\*                                                      | Si verifica quando viene premuto un pulsante del mouse.                                           |
| [MouseMove](player-player-mousemove.md)\*                                                      | Si verifica quando il puntatore del mouse viene spostato.                                          |
| [MouseUp](player-player-mouseup.md)\*                                                          | Si verifica quando viene rilasciato un pulsante del mouse.                                          |
| **NewStream**                                                                                    | Riservato per utilizzi futuri.                                                         |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Si verifica quando inizia la riproduzione di un titolo in un DVD.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Si verifica quando il Windows Media Player cambia stato.                      |
| [Modifica playlist](player-player-playlistchange.md)                                               | Si verifica quando viene modificata una playlist.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Si verifica quando viene modificato un elemento nell'insieme di playlist.                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | Si verifica quando una playlist viene aggiunta all'insieme di playlist.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Si verifica quando una playlist viene rimossa dall'insieme di playlist.                  |
| **PlaylistCollectionPlaylistSetAsDeleted**                                                       | Riservato per utilizzi futuri.                                                         |
| [PlayStateChange](player-player-playstatechange.md)                                             | Si verifica quando lo stato di riproduzione del controllo Windows Media Player cambia.          |
| [PositionChange](player-player-positionchange.md)                                               | Si verifica quando la posizione corrente dell'elemento multimediale è stata modificata.             |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Si verifica quando viene ricevuto un COMANDO o un URL sincronizzato.                           |
| [StatusChange](player-player-statuschange.md)                                                   | Si verifica quando il **valore della proprietà** di stato viene modificato.                               |
| [StringCollectionChange](player-player-stringcollectionchange.md)                               | Si verifica quando viene modificata una raccolta di stringhe.                                         |
| **Avviso**                                                                                      | Riservato per utilizzi futuri.                                                         |



 

\* Non accessibile alle interfaccia. Per informazioni sulla gestione degli eventi del mouse e della tastiera nelle interfaccia, vedere [Gestori eventi di ambiente.](ambient-event-handlers.md)

Quando è incorporato in una pagina Web, è possibile accedere all'oggetto **Player** usando il valore ID specificato nel tag OBJECT. All'interno di un file di definizione dell'interfaccia, è possibile accedervi usando **l'attributo globale player.** A scopo illustrativo, **player** verrà usato come ID oggetto nelle sezioni della sintassi di riferimento.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento sul modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




