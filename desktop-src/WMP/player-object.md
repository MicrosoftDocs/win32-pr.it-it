---
title: Oggetto Player
description: L'oggetto Player è l'oggetto radice per il controllo Media Player di Windows. Supporta le proprietà, i metodi e gli eventi elencati nelle tabelle seguenti.
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
ms.openlocfilehash: 0bdf6443557477c15497a36d4976b13d0cfea2fc
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104516396"
---
# <a name="player-object"></a>Oggetto Player

L'oggetto Player è l'oggetto radice per il controllo Media Player di Windows. Supporta le proprietà, i metodi e gli eventi elencati nelle tabelle seguenti.

L'oggetto Player supporta le proprietà seguenti. Le proprietà contrassegnate con un asterisco ( \* ) non sono accessibili alle interfacce.



| Proprietà                                             | Descrizione                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [cdromcollection](player-cdromcollection.md)        | Recupera l'oggetto [cdromcollection](cdromcollection-object.md) .                                                                          |
| [closedCaption](player-closedcaption.md)            | Recupera l'oggetto [ClosedCaption](closedcaption-object.md) .                                                                              |
| [controlli](player-controls.md)                      | Recupera l'oggetto [Controls](controls-object.md) .                                                                                        |
| [currentMedia](player-currentmedia.md)              | Specifica o recupera l'oggetto [multimediale](media-object.md) corrente.                                                                         |
| [currentPlaylist](player-currentplaylist.md)        | Specifica o recupera l'oggetto [playlist](playlist-object.md) corrente.                                                                   |
| [DVD](player-dvd.md)                                | Recupera l'oggetto [DVD](dvd-object.md) .                                                                                                  |
| [enableContextMenu](player-enablecontextmenu.md)\* | Specifica o recupera un valore che indica se abilitare il menu di scelta rapida che viene visualizzato quando si fa clic con il pulsante destro del mouse.          |
| [abilitato](player-enabled.md)\*                     | Specifica o recupera un valore che indica se il controllo Media Player Windows è abilitato.                                               |
| [error](player-error.md)                            | Recupera l'oggetto [Error](error-object.md) .                                                                                              |
| a [schermo intero](player-fullscreen.md)\*               | Specifica o recupera un valore che indica se il contenuto video viene riprodotto in modalità schermo intero.                                          |
| [isOnline](player-isonline.md)                      | Recupera un valore che indica se l'utente è connesso a una rete.                                                                     |
| [Remote](player-isremote.md)\*                   | Recupera un valore che indica se il controllo Media Player di Windows è in esecuzione in modalità remota.                                             |
| [mediacollection](player-mediacollection.md)        | Recupera l'oggetto [mediacollection](mediacollection-object.md) .                                                                          |
| [network](player-network.md)                        | Recupera l'oggetto di [rete](network-object.md) .                                                                                          |
| [openState](player-openstate.md)                    | Recupera un valore che indica lo stato dell'origine del contenuto.                                                                                |
| [playerApplication](player-playerapplication.md)\* | Recupera l'oggetto [PlayerApplication](playerapplication-object.md) quando è in esecuzione un controllo Media Player Windows remoto.               |
| [playlistCollection](player-playlistcollection.md)  | Recupera l'oggetto [PlaylistCollection](playlistcollection-object.md) .                                                                    |
| [Riproduzione](player-playstate.md)                    | Recupera un valore che indica lo stato dell'operazione di Media Player di Windows.                                                                |
| [impostazioni](player-settings.md)                      | Recupera l'oggetto [Impostazioni](settings-object.md) .                                                                                        |
| [Stato](player-status.md)                          | Recupera un valore che indica lo stato corrente di Windows Media Player.                                                                     |
| [stretchToFit](player-stretchtofit.md)\*           | Specifica o recupera un valore che indica se il video si adatta alla dimensione della visualizzazione video del controllo Media Player di Windows.          |
| [uiMode](player-uimode.md)\*                       | Specifica o recupera un valore che indica quali controlli vengono visualizzati nell'interfaccia utente quando Windows Media Player viene incorporato in una pagina Web. |
| [URL](player-url.md)                                | Specifica o Recupera il nome della clip da riprodurre.                                                                                         |
| [versionInfo](player-versioninfo.md)                | Recupera un valore stringa che specifica la versione di Windows Media Player.                                                                 |
| [windowlessVideo](player-windowlessvideo.md)\*     | Specifica o recupera un valore che indica se il controllo di Windows Media Player esegue il rendering del video in modalità senza finestra.                         |



 

\* Non accessibile alle interfacce.

L'oggetto Player supporta i metodi seguenti.



| Metodo                                | Descrizione                                               |
|---------------------------------------|-----------------------------------------------------------|
| [close](player-close.md)             | Rilascia le risorse di Windows Media Player.                  |
| [launchURL](player-launchurl.md)     | Invia un URL al browser predefinito dell'utente di cui eseguire il rendering. |
| [newMedia](player-newmedia.md)       | Crea un nuovo oggetto [multimediale](media-object.md) .           |
| [Nuova playlist](player-newplaylist.md) | Crea un nuovo oggetto [playlist](playlist-object.md) .     |
| [openPlayer](player-openplayer.md)   | Apre Windows Media Player utilizzando l'URL specificato.       |



 

L'oggetto Player supporta gli eventi seguenti. Gli eventi contrassegnati con un asterisco ( \* ) non sono accessibili alle interfacce. Per informazioni sulla gestione degli eventi di mouse e tastiera nelle interfacce, vedere [eventi esterni](external-events.md).



| Event                                                                                            | Descrizione                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Si verifica in seguito alla modifica della lingua audio corrente.                                  |
| [responseBuffering](player-player-buffering.md)                                                         | Si verifica quando il controllo Media Player di Windows inizia o termina il buffering.           |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | Si verifica quando si inserisce o si espelle un CD o un DVD da un'unità CD o DVD.      |
| [Clic](player-player-click.md) \*                                                              | Si verifica quando l'utente fa clic su un pulsante del mouse.                                      |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Si verifica quando i *controlli*. **CurrentItem** modifiche.                                  |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Si verifica quando diventa disponibile un elemento di metadati grafici nell'elemento multimediale corrente. |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Si verifica quando viene apportata una modifica all'interno della playlist corrente.                       |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Si verifica quando l'elemento della playlist corrente diventa disponibile.                         |
| **Disconnetti**                                                                                   | Riservato per utilizzi futuri.                                                         |
| [DomainChange](player-player-domainchange.md)                                                   | Si verifica in seguito alla modifica del dominio DVD.                                              |
| [DoubleClick](player-player-doubleclick.md)\*                                                  | Si verifica quando l'utente fa doppio clic su un pulsante del mouse.                               |
| **DurationUnitChange**                                                                           | Riservato per utilizzi futuri.                                                         |
| **EndOfStream**                                                                                  | Riservato per utilizzi futuri.                                                         |
| [Error (Errore) (Error (Errore)e)](player-player-error.md)                                                                 | Si verifica quando il controllo Media Player Windows presenta una condizione di errore.             |
| [KeyDown](player-player-keydown.md) \*                                                          | Si verifica quando un tasto viene premuto.                                                    |
| [Pressione](player-player-keypress.md) del tasto \*                                                        | Si verifica quando si preme e si rilascia un tasto.                                  |
| [KeyUp](player-player-keyup.md) \*                                                              | Si verifica quando si rilascia un tasto.                                                   |
| [MarkerHit](player-player-markerhit.md)                                                         | Si verifica quando viene raggiunto un marcatore.                                                 |
| [MediaChange](player-player-mediachange.md)                                                     | Si verifica quando un elemento multimediale viene modificato.                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | Si verifica quando un valore di attributo viene aggiunto alla libreria.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Si verifica quando viene modificato un valore di attributo nella libreria.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Si verifica quando un valore di attributo viene rimosso dalla libreria.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Si verifica in seguito alla modifica dell'insieme di supporti.                                        |
| [MediaCollectionMediaAdded](player-player-mediacollectionmediaadded.md)                         | Si verifica quando un elemento multimediale viene aggiunto alla libreria locale.                          |
| [MediaCollectionMediaRemoved](player-player-mediacollectionmediaremoved.md)                     | Si verifica quando un elemento multimediale viene rimosso dalla libreria locale.                      |
| [Errore MediaError](player-player-mediaerror.md)                                                       | Si verifica quando l'oggetto **multimediale** presenta una condizione di errore.                         |
| [ModeChange](player-player-modechange.md)                                                       | Si verifica quando viene modificata una modalità di Windows Media Player.                           |
| [MouseDown](player-player-mousedown.md)\*                                                      | Si verifica quando viene premuto un pulsante del mouse.                                           |
| [MouseMove](player-player-mousemove.md)\*                                                      | Si verifica quando il puntatore del mouse viene spostato.                                          |
| [MouseUp](player-player-mouseup.md)\*                                                          | Si verifica quando viene rilasciato un pulsante del mouse.                                          |
| **NewStream**                                                                                    | Riservato per utilizzi futuri.                                                         |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Si verifica quando viene avviata la riproduzione di un titolo in un DVD.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Si verifica in seguito alla modifica dello stato del controllo Media Player di Windows.                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | Si verifica in seguito alla modifica di una playlist.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Si verifica quando viene apportata una modifica alla raccolta di playlist.                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | Si verifica quando viene aggiunta una playlist alla raccolta di playlist.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Si verifica quando una playlist viene rimossa dalla raccolta di playlist.                  |
| **PlaylistCollectionPlaylistSetAsDeleted**                                                       | Riservato per utilizzi futuri.                                                         |
| [PlayStateChange](player-player-playstatechange.md)                                             | Si verifica in seguito alla modifica dello stato di riproduzione del controllo Media Player di Windows.          |
| [PositionChange](player-player-positionchange.md)                                               | Si verifica quando la posizione corrente dell'elemento multimediale è stata modificata.             |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Si verifica quando viene ricevuto un comando o un URL sincronizzato.                           |
| [StatusChange](player-player-statuschange.md)                                                   | Si verifica in seguito alla modifica del valore della proprietà **status** .                               |
| [StringCollectionChange](player-player-stringcollectionchange.md)                               | Si verifica in seguito alla modifica di una raccolta di stringhe.                                         |
| **Avviso**                                                                                      | Riservato per utilizzi futuri.                                                         |



 

\* Non accessibile alle interfacce. Per informazioni sulla gestione degli eventi di mouse e tastiera nelle interfacce, vedere [gestori eventi di ambiente](ambient-event-handlers.md).

Quando viene incorporato in una pagina Web, è possibile accedere all'oggetto **Player** usando il valore ID specificato nel tag Object. All'interno di un file di definizione dell'interfaccia, è possibile accedervi usando l'attributo globale **Player** . A scopo illustrativo, il **lettore** verrà usato come ID oggetto nelle sezioni della sintassi di riferimento.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




