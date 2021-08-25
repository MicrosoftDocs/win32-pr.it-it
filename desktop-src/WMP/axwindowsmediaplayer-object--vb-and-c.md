---
title: Oggetto AxWindowsMediaPlayer (VB e C )
description: Oggetto AxWindowsMediaPlayer (VB e C\ )
ms.assetid: d7eeac20-1afa-4e73-9af6-9772fbb65516
keywords:
- Windows Media Player,Oggetto AxWindowsMediaPlayer
- Windows Media Player Oggetto Mobile,AxWindowsMediaPlayer
- Windows Media Player a oggetti, oggetto AxWindowsMediaPlayer
- modello a oggetti,oggetto AxWindowsMediaPlayer
- ActiveX, oggetto AxWindowsMediaPlayer
- Windows Media Player ActiveX, oggetto AxWindowsMediaPlayer
- Windows Media Player Controllo ActiveX mobile,oggetto AxWindowsMediaPlayer
- informazioni di riferimento per il modello a oggetti, oggetto AxWindowsMediaPlayer
- Oggetto AxWindowsMediaPlayer
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1d0c66360e80ea293795442472ce163292c38152baa859889086a5687f03764f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765281"
---
# <a name="axwindowsmediaplayer-object-vb-and-c"></a>Oggetto AxWindowsMediaPlayer (VB e C#)

L'oggetto AxWindowsMediaPlayer è l'oggetto radice per il Windows Media Player controllo. Supporta le proprietà, i metodi e gli eventi elencati nelle tabelle seguenti.

L'oggetto AxWindowsMediaPlayer supporta le proprietà seguenti.



| Proprietà                                                                             | Descrizione                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [cdromCollection](axwmplib-axwindowsmediaplayer-cdromcollection--vb-and-c.md)       | Ottiene **un'interfaccia IWMPCdromCollection.**                                                                                         |
| [closedCaption](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md)           | Ottiene un'interfaccia IWMPClosedCaption.                                                                                               |
| [Ctlcontrols](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md)               | Ottiene un'interfaccia IWMPControls.                                                                                                    |
| [Ctlenabled](axwmplib-axwindowsmediaplayer-ctlenabled--vb-and-c.md)                 | Ottiene o imposta un valore che indica se il controllo Windows Media Player è abilitato.                                               |
| [currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)             | Ottiene o imposta l'interfaccia IWMPMedia che corrisponde all'elemento multimediale corrente.                                                   |
| [currentPlaylist](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)       | Ottiene o imposta **l'interfaccia IWMPPlaylist** corrente.                                                                               |
| [Dvd](axwmplib-axwindowsmediaplayer-dvd--vb-and-c.md)                               | Ottiene un'interfaccia IWMPDVD.                                                                                                         |
| [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)   | Ottiene o imposta un valore che indica se abilitare il menu di scelta rapida, che viene visualizzato quando si fa clic con il pulsante destro del mouse.          |
| [Error (Errore) (Error (Errore)e)](axwmplib-axwindowsmediaplayer-error--vb-and-c.md)                           | Ottiene un'interfaccia IWMPError.                                                                                                       |
| [Fullscreen](axwmplib-axwindowsmediaplayer-fullscreen--vb-and-c.md)                 | Ottiene o imposta un valore che indica se il contenuto video viene riprodotto in modalità schermo intero.                                          |
| [isOnline](axwmplib-axwindowsmediaplayer-isonline--vb-and-c.md)                     | Ottiene un valore che indica se l'utente è connesso a una rete.                                                                |
| isRemote                                                                             | Non supportato per la programmazione .NET.                                                                                                |
| [mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)       | Ottiene un'interfaccia IWMPMediaCollection.                                                                                             |
| [Rete](axwmplib-axwindowsmediaplayer-network--vb-and-c.md)                       | Ottiene un'interfaccia IWMPNetwork.                                                                                                     |
| [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)                   | Ottiene un valore che indica lo stato dell'origine di contenuto.                                                                           |
| playerApplication                                                                    | Non supportato per la programmazione .NET.                                                                                                |
| [playlistCollection](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) | Ottiene un'interfaccia IWMPPlaylistCollection.                                                                                          |
| [playState](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)                   | Ottiene un valore che indica lo stato dell'Windows Media Player operazione.                                                           |
| [impostazioni](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)                     | Ottiene un'interfaccia IWMPSettings.                                                                                                    |
| [Stato](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)                         | Ottiene un valore che indica lo stato corrente di Windows Media Player.                                                                |
| [stretchToFit](axwmplib-axwindowsmediaplayer-stretchtofit--vb-and-c.md)             | Ottiene o imposta un valore che indica se il video verrà adattato alle dimensioni della Windows Media Player video del controllo.          |
| [uiMode](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)                         | Ottiene o imposta un valore che indica quali controlli vengono visualizzati nell'interfaccia utente quando Windows Media Player è incorporato in una pagina Web. |
| [URL](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)                               | Ottiene o imposta il nome del clip da riprodurre.                                                                                         |
| [versionInfo](axwmplib-axwindowsmediaplayer-versioninfo--vb-and-c.md)               | Ottiene un valore che specifica la versione del Windows Media Player.                                                               |
| [windowlessVideo](axwmplib-axwindowsmediaplayer-windowlessvideo--vb-and-c.md)       | Ottiene o imposta un valore che indica se il controllo Windows Media Player esegue il rendering del video in modalità senza finestra.                         |



 

L'oggetto AxWindowsMediaPlayer supporta i metodi seguenti.



| Metodo                                                       | Descrizione                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| [close](axwmplib-axwindowsmediaplayer-close.md)             | Rilascia Windows Media Player risorse.                  |
| [launchURL](axwmplib-axwindowsmediaplayer-launchurl.md)     | Invia un URL al browser predefinito dell'utente di cui eseguire il rendering. |
| [Newmedia](axwmplib-axwindowsmediaplayer-newmedia.md)       | Restituisce un'interfaccia IWMPMedia per un nuovo elemento multimediale.      |
| [newPlaylist](axwmplib-axwindowsmediaplayer-newplaylist.md) | restituisce un'interfaccia IWMPPlaylist per una nuova playlist.     |
| [openPlayer](axwmplib-axwindowsmediaplayer-openplayer.md)   | Apre Windows Media Player utilizzando l'URL specificato.       |



 

L'oggetto AxWindowsMediaPlayer supporta gli eventi seguenti.



| Event                                                                                                              | Descrizione                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [AudioLanguageChange](axwmplib-axwindowsmediaplayer-audiolanguagechange.md)                                       | Si verifica quando cambia la lingua audio corrente.                                                            |
| [responseBuffering](axwmplib-axwindowsmediaplayer-buffering.md)                                                           | Si verifica quando il controllo Windows Media Player inizia o termina la memorizzazione nel buffer.                                     |
| [CdromBurnError](axwmplib-axwindowsmediaplayer-cdromburnerror.md)                                                 | Si verifica quando si verifica un errore generico durante un'operazione di masterizzazione cd.                                         |
| [CdromBurnMediaError](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)                                       | Si verifica quando si verifica un errore durante la masterizzazione di un singolo elemento multimediale in un CD.                               |
| [CdromBurnStateChange](axwmplib-axwindowsmediaplayer-cdromburnstatechange.md)                                     | Si verifica quando lo stato di un'operazione di masterizzazione cd cambia.                                                          |
| [CdromMediaChange](axwmplib-axwindowsmediaplayer-cdrommediachange.md)                                             | Si verifica quando un CD o DVD viene inserito o espulso da un'unità CD o DVD.                                |
| [CdromRipMediaError](axwmplib-axwindowsmediaplayer-cdromripmediaerror.md)                                         | Si verifica quando si verifica un errore durante la copia di una singola traccia da un CD.                                  |
| [CdromRipStateChange](axwmplib-axwindowsmediaplayer-cdromripstatechange.md)                                       | Si verifica quando lo stato di un'operazione di ripping cd cambia.                                                          |
| [Clic](axwmplib-axwindowsmediaplayer-click.md)                                                                   | Si verifica quando l'utente fa clic su un pulsante del mouse.                                                                |
| CreatePartnershipComplete                                                                                          | Non supportato per la programmazione .NET.                                                                        |
| [CurrentItemChange](axwmplib-axwindowsmediaplayer-currentitemchange.md)                                           | Si verifica [quando cambia IWMPControls.currentItem.](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md) |
| [CurrentMediaItemAvailable](axwmplib-axwindowsmediaplayer-currentmediaitemavailable.md)                           | Si verifica quando un elemento di metadati grafico nell'elemento multimediale corrente diventa disponibile.                           |
| [CurrentPlaylistChange](axwmplib-axwindowsmediaplayer-currentplaylistchange.md)                                   | Si verifica quando cambia qualcosa all'interno della playlist corrente.                                                 |
| [CurrentPlaylistItemAvailable](axwmplib-axwindowsmediaplayer-currentplaylistitemavailable.md)                     | Si verifica quando l'elemento della playlist corrente diventa disponibile.                                                   |
| DeviceConnect                                                                                                      | Non supportato per la programmazione .NET.                                                                        |
| DeviceDisconnect                                                                                                   | Non supportato per la programmazione .NET.                                                                        |
| DeviceStatusChange                                                                                                 | Non supportato per la programmazione .NET.                                                                        |
| DeviceSyncError                                                                                                    | Non supportato per la programmazione .NET.                                                                        |
| DeviceSyncStateChange                                                                                              | Non supportato per la programmazione .NET.                                                                        |
| [Disconnetti](axwmplib-axwindowsmediaplayer-disconnect.md)                                                         | Riservato per utilizzi futuri.                                                                                   |
| [DomainChange](axwmplib-axwindowsmediaplayer-domainchange.md)                                                     | Si verifica quando cambia il dominio DVD.                                                                        |
| [Doubleclick](axwmplib-axwindowsmediaplayer-doubleclick.md)                                                       | Si verifica quando l'utente fa doppio clic su un pulsante del mouse.                                                         |
| [DurationUnitChange](axwmplib-axwindowsmediaplayer-durationunitchange.md)                                         | Riservato per utilizzi futuri.                                                                                   |
| [EndOfStream](axwmplib-axwindowsmediaplayer-endofstream.md)                                                       | Riservato per utilizzi futuri.                                                                                   |
| [Error (Errore) (Error (Errore)e)](axwmplib-axwindowsmediaplayer-error.md)                                                                   | Si verifica quando il controllo Windows Media Player ha una condizione di errore.                                       |
| [FolderScanStateChange](axwmplib-axwindowsmediaplayer-folderscanstatechange.md)                                   | Si verifica quando lo stato di un'operazione di monitoraggio della cartella cambia.                                                   |
| [KeyDown](axwmplib-axwindowsmediaplayer-keydown.md)                                                               | Si verifica quando un tasto viene premuto.                                                                              |
| [Keypress](axwmplib-axwindowsmediaplayer-keypress.md)                                                             | Si verifica quando un tasto viene premuto e quindi rilasciato.                                                            |
| [KeyUp](axwmplib-axwindowsmediaplayer-keyup.md)                                                                   | Si verifica quando si rilascia un tasto.                                                                             |
| [LibreriaConnetti](axwmplib-axwindowsmediaplayer-libraryconnect.md)                                                 | Si verifica quando una libreria diventa disponibile.                                                                   |
| [LibreriaDisconnect](axwmplib-axwindowsmediaplayer-librarydisconnect.md)                                           | Si verifica quando una libreria non è più disponibile.                                                              |
| [MarkerHit](axwmplib-axwindowsmediaplayer-markerhit.md)                                                           | Si verifica quando viene raggiunto un marcatore.                                                                           |
| [MediaChange](axwmplib-axwindowsmediaplayer-mediachange.md)                                                       | Si verifica quando viene modificato un elemento multimediale.                                                                          |
| [MediaCollectionAttributeStringAdded](axwmplib-axwindowsmediaplayer-mediacollectionattributestringadded.md)       | Si verifica quando un valore di attributo viene aggiunto alla libreria.                                                    |
| [MediaCollectionAttributeStringChanged](axwmplib-axwindowsmediaplayer-mediacollectionattributestringchanged.md)   | Si verifica quando viene modificato il valore di un attributo nella libreria.                                                  |
| [MediaCollectionAttributeStringRemoved](axwmplib-axwindowsmediaplayer-mediacollectionattributestringremoved.md)   | Si verifica quando un valore di attributo viene rimosso dalla libreria.                                                |
| [MediaCollectionChange](axwmplib-axwindowsmediaplayer-mediacollectionchange.md)                                   | Si verifica quando cambia la raccolta di supporti.                                                                  |
| [MediaCollectionMediaAdded](axwmplib-axwindowsmediaplayer-mediacollectionmediaadded.md)                           | Si verifica quando un elemento multimediale viene aggiunto alla libreria locale.                                                    |
| [MediaCollectionMediaRemoved](axwmplib-axwindowsmediaplayer-mediacollectionmediaremoved.md)                       | Si verifica quando un elemento multimediale viene rimosso dalla libreria locale.                                                |
| [MediaError](axwmplib-axwindowsmediaplayer-mediaerror.md)                                                         | Si verifica quando **l'oggetto Media** presenta una condizione di errore.                                                   |
| [ModeChange](axwmplib-axwindowsmediaplayer-modechange.md)                                                         | Si verifica quando viene modificata una Windows Media Player modalità.                                                     |
| [Mousedown](axwmplib-axwindowsmediaplayer-mousedown.md)                                                           | Si verifica quando viene premuto un pulsante del mouse.                                                                     |
| [Mousemove](axwmplib-axwindowsmediaplayer-mousemove.md)                                                           | Si verifica quando il puntatore del mouse viene spostato.                                                                    |
| [Mouseup](axwmplib-axwindowsmediaplayer-mouseup.md)                                                               | Si verifica quando viene rilasciato un pulsante del mouse.                                                                    |
| [NewStream](axwmplib-axwindowsmediaplayer-newstream.md)                                                           | Riservato per utilizzi futuri.                                                                                   |
| [OpenPlaylistSwitch](axwmplib-axwindowsmediaplayer-openplaylistswitch.md)                                         | Si verifica quando inizia la riproduzione di un titolo in un DVD.                                                               |
| [OpenStateChange](axwmplib-axwindowsmediaplayer-openstatechange.md)                                               | Si verifica quando il controllo Windows Media Player cambia stato.                                                |
| PlayerDockedStateChange                                                                                            | Non supportato per la programmazione .NET.                                                                        |
| PlayerReconnect                                                                                                    | Non supportato per la programmazione .NET.                                                                        |
| [PlaylistChange](axwmplib-axwindowsmediaplayer-playlistchange.md)                                                 | Si verifica quando cambia una playlist.                                                                            |
| [PlaylistCollectionChange](axwmplib-axwindowsmediaplayer-playlistcollectionchange.md)                             | Si verifica quando cambia qualcosa nella raccolta di playlist.                                                  |
| [PlaylistCollectionPlaylistAdded](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistadded.md)               | Si verifica quando una playlist viene aggiunta alla raccolta di playlist.                                                |
| [PlaylistCollectionPlaylistRemoved](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistremoved.md)           | Si verifica quando una playlist viene rimossa dalla raccolta di playlist.                                            |
| [PlaylistCollectionPlaylistSetAsDeleted](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistsetasdeleted.md) | Riservato per utilizzi futuri.                                                                                   |
| [PlayStateChange](axwmplib-axwindowsmediaplayer-playstatechange.md)                                               | Si verifica quando lo stato di riproduzione del controllo Windows Media Player modifica.                                    |
| [PositionChange](axwmplib-axwindowsmediaplayer-positionchange.md)                                                 | Si verifica quando la posizione corrente dell'elemento multimediale è stata modificata.                                       |
| [ScriptCommand](axwmplib-axwindowsmediaplayer-scriptcommand.md)                                                   | Si verifica quando viene ricevuto un URL o un comando sincronizzato.                                                     |
| [StatusChange](axwmplib-axwindowsmediaplayer-statuschange.md)                                                     | Si verifica quando il **valore della proprietà** di stato cambia.                                                         |
| [StringCollectionChange](axwmplib-axwindowsmediaplayer-stringcollectionchange.md)                                 | Si verifica quando viene modificata una raccolta di stringhe.                                                                   |
| SwitchedToControl                                                                                                  | Non supportato per la programmazione .NET.                                                                        |
| SwitchedToPlayerApplication                                                                                        | Non supportato per la programmazione .NET.                                                                        |
| [Avviso](axwmplib-axwindowsmediaplayer-warning.md)                                                               | Riservato per utilizzi futuri.                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPCdromCollection (VB e C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPError (VB e C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylistCollection (VB e C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Informazioni di riferimento sul modello a oggetti Visual Basic .NET e C #**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> <dt>

[**WMPOpenState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> <dt>

[**WMPPlayState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 




