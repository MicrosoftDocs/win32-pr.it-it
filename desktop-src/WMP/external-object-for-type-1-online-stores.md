---
title: Oggetto esterno per i negozi di tipo 1 online
description: Oggetto esterno per i negozi di tipo 1 online
ms.assetid: 5c42e1a9-c5c6-4725-8528-de2839d84e77
keywords:
- Windows Media Player Online Stores, oggetti esterni
- archivi online, oggetti esterni
- digitare 1 archivi online, oggetti esterni
- oggetti esterni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f50e5e6bfc98ea3669996b06fa4a4defb52452fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955782"
---
# <a name="external-object-for-type-1-online-stores"></a>Oggetto esterno per i negozi di tipo 1 online

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'oggetto **esterno** fornisce funzionalità alle pagine Web, fornite da uno Store online, ospitato in Windows Media Player.

L'oggetto **esterno** espone le proprietà seguenti per gli archivi online di tipo 1.



| Proprietà                                                                                  | Descrizione                                                                                                                              |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [accountType](external-accounttype.md)                                                   | Recupera il tipo di account dell'utente corrente.                                                                                          |
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md)                           | Recupera il colore di evidenziazione del pulsante corrente per l'interfaccia utente di Windows Media Player.                                                |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md)                           | Recupera il colore corrente del pulsante al passaggio del mouse per l'interfaccia utente di Windows Media Player.                                                    |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)                                 | Recupera il colore dell'ombreggiatura del pulsante corrente per l'interfaccia utente di Windows Media Player.                                                   |
| [appColorDark](external-appcolordark.md)                                                 | Recupera il colore ombreggiato scuro corrente dell'interfaccia utente di Windows Media Player.                                                      |
| [appColorLight](external-appcolorlight.md)                                               | Recupera il colore ombreggiato chiaro corrente dell'interfaccia utente di Windows Media Player.                                                     |
| [appColorMedium](external-appcolormedium.md)                                             | Recupera il colore medio ombreggiato corrente dell'interfaccia utente di Windows Media Player.                                                    |
| [basketTitle](external-baskettitle.md)                                                   | Recupera il titolo del pulsante nel riquadro dell'elenco (chiamato anche basket) in Windows Media Player.                                     |
| [filter](external-filter.md)                                                             | Recupera il filtro di ricerca attualmente utilizzato da Windows Media Player.                                                                    |
| [ignoreIEHistory](external-ignoreiehistory.md)                                           | Specifica se Windows Media Player deve ignorare la cronologia di Internet Explorer.                                                          |
| [libraryLocationID](external-librarylocationid.md)                                       | Recupera l'identificatore di un elemento multimediale specifico attualmente visualizzato nella visualizzazione del lettore.                                      |
| [libraryLocationType](external-librarylocationtype.md)                                   | Recupera una [costante del percorso della libreria](library-location-constants.md) che indica il tipo della visualizzazione corrente in Windows Media Player. |
| [pluginRunning](external-pluginrunning.md)                                               | Recupera un valore che indica se il plug-in del negozio online è in esecuzione.                                                          |
| [selectedItemID](external-selecteditemid.md)                                             | Recupera l'identificatore dell'elemento multimediale attualmente selezionato in Windows Media Player.                                           |
| [selectedItemType](external-selecteditemtype.md)                                         | Recupera il tipo dell'elemento multimediale attualmente selezionato in Windows Media Player.                                                 |
| [attività](external-task.md)                                                                 | Recupera il nome del riquadro attività corrente.                                                                                             |
| [templateBeingDisplayedInLocalLibrary](external-templatebeingdisplayedinlocallibrary.md) | Indica se il feed rappresentato dalla pagina di individuazione corrente viene visualizzato nel controllo di visualizzazione ad albero della libreria locale.          |
| [userLoggedIn](external-userloggedin.md)                                                 | Recupera un valore che indica se l'utente è connesso al negozio online.                                                          |
| [version](external-version.md)                                                           | Recupera la versione corrente di Windows Media Player.                                                                                   |
| [viewParameters](external-viewparameters.md)                                             | Recupera i parametri associati alla visualizzazione corrente in Windows Media Player.                                                           |



 

L'oggetto **esterno** espone i metodi seguenti per gli archivi online di tipo 1.



| Metodo                                                            | Descrizione                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [addToBasket](external-addtobasket.md)                           | Aggiunge elementi multimediali al riquadro elenco (chiamato anche basket) in Windows Media Player.                                          |
| [attemptLogin](external-attemptlogin.md)                         | Visualizza una finestra di dialogo in modo che l'utente possa tentare di accedere allo Store online.                                                 |
| [authenticate](external-authenticate.md)                         | Avvia un tentativo di autenticazione dell'utente.                                                                               |
| [acquistare](external-buy.md)                                           | Avvia l'acquisto di un set di elementi multimediali.                                                                              |
| [cancelNavigate](external-cancelnavigate.md)                     | Informa Windows Media Player che non dovrebbe visualizzare una nuova pagina di individuazione anche se la visualizzazione è cambiata nel lettore. |
| [changeView](external-changeview.md)                             | Modifica la visualizzazione in Windows Media Player.                                                                                    |
| [changeViewOnlineList](external-changeviewonlinelist.md)         | Modifica la visualizzazione in Windows Media Player per visualizzare un elenco generato dinamicamente dallo Store online.                        |
| [download](external-download.md)                                 | Avvia il download di un set di elementi multimediali.                                                                              |
| [Play](external-play.md)                                         | Indica a Windows Media Player di riprodurre un set di elementi multimediali.                                                                 |
| [saveCurrentViewToLibrary](external-savecurrentviewtolibrary.md) | Crea una playlist dagli elementi multimediali nella visualizzazione corrente e salva la playlist nella libreria locale.                     |
| [sendMessage](external-sendmessage.md)                           | Invia un messaggio al plug-in del negozio online.                                                                               |
| [showPopup](external-showpopup.md)                               | Indica a Windows Media Player di visualizzare una pagina Web popup; ovvero una pagina Web visualizzata in una finestra separata.            |



 

L'oggetto **esterno** espone gli eventi seguenti per gli archivi online di tipo 1.



| Event                                                                         | Descrizione                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [OnChangeViewError](external-onchangeviewerror-event.md)                     | Si verifica quando una chiamata al metodo **External. ChangeView** genera un errore.           |
| [OnChangeViewOnlineListError](external-onchangeviewonlinelisterror-event.md) | Si verifica quando una chiamata al metodo **External. ChangeViewOnlineList** genera un errore. |
| [OnColorChange](external-oncolorchange-event.md)                             | Si verifica quando cambia il colore dell'interfaccia utente di Windows Media Player.               |
| [OnLoginChange](external-onloginchange-event.md)                             | Si verifica quando lo stato di accesso dell'utente cambia o quando un tentativo di accesso non riesce.        |
| [OnSendMessageComplete](external-onsendmessagecomplete-event.md)             | Si verifica al termine dell'elaborazione di un messaggio da parte dell'archivio online.                         |
| [OnViewChange](external-onviewchange-event.md)                               | Si verifica quando la visualizzazione cambia in Windows Media Player.                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento per negozi online di tipo 1**](reference-for-type-1-online-stores.md)
</dt> <dt>

[**Gestione remota del controllo di Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




