---
title: Oggetto esterno per i negozi online di tipo 1
description: Oggetto esterno per i negozi online di tipo 1
ms.assetid: 5c42e1a9-c5c6-4725-8528-de2839d84e77
keywords:
- Windows Media Player online, oggetti esterni
- negozi online, oggetti esterni
- tipo 1 negozi online, oggetti esterni
- oggetti esterni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7d95d2ca332b88edea73da2238374aeffc52e520d7bc0346eab9f4eb7a05f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649001"
---
# <a name="external-object-for-type-1-online-stores"></a>Oggetto esterno per i negozi online di tipo 1

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di un negozio online non è supportato.

 

**L'oggetto** External fornisce funzionalità alle pagine Web, fornite da uno store online, ospitate in Windows Media Player.

**L'oggetto** External espone le proprietà seguenti per i negozi online di tipo 1.



| Proprietà                                                                                  | Descrizione                                                                                                                              |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [accountType](external-accounttype.md)                                                   | Recupera il tipo di account dell'utente corrente.                                                                                          |
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md)                           | Recupera il colore di evidenziazione del pulsante corrente per l Windows Media Player'interfaccia utente.                                                |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md)                           | Recupera il colore corrente al passaggio del mouse del pulsante per Windows Media Player'interfaccia utente.                                                    |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)                                 | Recupera il colore dell'ombreggiatura del pulsante corrente per Windows Media Player'interfaccia utente.                                                   |
| [appColorDark](external-appcolordark.md)                                                 | Recupera il colore ombreggiato scuro corrente dell'Windows Media Player utente.                                                      |
| [appColorLight](external-appcolorlight.md)                                               | Recupera il colore ombreggiato chiaro corrente dell'Windows Media Player utente.                                                     |
| [appColorMedium](external-appcolormedium.md)                                             | Recupera il colore medio ombreggiato corrente dell'Windows Media Player utente.                                                    |
| [basketTitle](external-baskettitle.md)                                                   | Recupera il titolo del pulsante nel riquadro elenco (detto anche carrello) in Windows Media Player.                                     |
| [filter](external-filter.md)                                                             | Recupera il filtro di ricerca attualmente in uso da Windows Media Player.                                                                    |
| [ignoreIEHistory](external-ignoreiehistory.md)                                           | Specifica se Windows Media Player deve ignorare Internet Explorer cronologia.                                                          |
| [libraryLocationID](external-librarylocationid.md)                                       | Recupera l'identificatore di un elemento multimediale specifico attualmente visualizzato nella visualizzazione del lettore.                                      |
| [libraryLocationType](external-librarylocationtype.md)                                   | Recupera una costante [del percorso della](library-location-constants.md) libreria che indica il tipo della visualizzazione corrente in Windows Media Player. |
| [pluginRunning](external-pluginrunning.md)                                               | Recupera un valore che indica se il plug-in dello store online è in esecuzione.                                                          |
| [selectedItemID](external-selecteditemid.md)                                             | Recupera l'identificatore dell'elemento multimediale attualmente selezionato in Windows Media Player.                                           |
| [selectedItemType](external-selecteditemtype.md)                                         | Recupera il tipo di elemento multimediale attualmente selezionato in Windows Media Player.                                                 |
| [Attività](external-task.md)                                                                 | Recupera il nome del riquadro attività corrente.                                                                                             |
| [templateBeingDisplayedInLocalLibrary](external-templatebeingdisplayedinlocallibrary.md) | Indica se il feed rappresentato dalla pagina di individuazione corrente viene visualizzato nel controllo di visualizzazione albero della libreria locale.          |
| [userLoggedIn](external-userloggedin.md)                                                 | Recupera un valore che indica se l'utente è connesso al negozio online.                                                          |
| [version](external-version.md)                                                           | Recupera la versione corrente di Windows Media Player.                                                                                   |
| [viewParameters](external-viewparameters.md)                                             | Recupera i parametri associati alla visualizzazione corrente in Windows Media Player.                                                           |



 

**L'oggetto** External espone i metodi seguenti per i negozi online di tipo 1.



| Metodo                                                            | Descrizione                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [addToBasket](external-addtobasket.md)                           | Aggiunge elementi multimediali al riquadro elenco (detto anche carrello) in Windows Media Player.                                          |
| [attemptLogin](external-attemptlogin.md)                         | Visualizza una finestra di dialogo in cui l'utente può tentare di accedere al negozio online.                                                 |
| [authenticate](external-authenticate.md)                         | Avvia un tentativo di autenticazione dell'utente.                                                                               |
| [acquistare](external-buy.md)                                           | Avvia l'acquisto di un set di elementi multimediali.                                                                              |
| [cancelNavigate](external-cancelnavigate.md)                     | Informa Windows Media Player che non deve visualizzare una nuova pagina di individuazione anche se la visualizzazione è stata modificata nel lettore. |
| [changeView](external-changeview.md)                             | Modifica la visualizzazione in Windows Media Player.                                                                                    |
| [changeViewOnlineList](external-changeviewonlinelist.md)         | Modifica la visualizzazione in Windows Media Player per visualizzare un elenco generato dinamicamente dallo store online.                        |
| [download](external-download.md)                                 | Avvia il download di un set di elementi multimediali.                                                                              |
| [Giocare](external-play.md)                                         | Indica Windows Media Player riprodurre un set di elementi multimediali.                                                                 |
| [saveCurrentViewToLibrary](external-savecurrentviewtolibrary.md) | Crea una playlist dagli elementi multimediali nella visualizzazione corrente e la salva nella libreria locale.                     |
| [Sendmessage](external-sendmessage.md)                           | Invia un messaggio al plug-in dello store online.                                                                               |
| [showPopup](external-showpopup.md)                               | Indica Windows Media Player visualizzare una pagina Web popup. una pagina Web visualizzata in una finestra separata.            |



 

**L'oggetto** External espone gli eventi seguenti per i negozi online di tipo 1.



| Event                                                                         | Descrizione                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [OnChangeViewError](external-onchangeviewerror-event.md)                     | Si verifica quando una chiamata al **metodo External.ChangeView** restituisce un errore.           |
| [OnChangeViewOnlineListError](external-onchangeviewonlinelisterror-event.md) | Si verifica quando una chiamata al **metodo External.ChangeViewOnlineList** restituisce un errore. |
| [OnColorChange](external-oncolorchange-event.md)                             | Si verifica quando viene modificato il colore Windows Media Player'interfaccia utente.               |
| [OnLoginChange](external-onloginchange-event.md)                             | Si verifica quando lo stato di accesso dell'utente cambia o quando un tentativo di accesso non riesce.        |
| [OnSendMessageComplete](external-onsendmessagecomplete-event.md)             | Si verifica al termine dell'elaborazione di un messaggio da parte dello store online.                         |
| [OnViewChange](external-onviewchange-event.md)                               | Si verifica quando la visualizzazione cambia in Windows Media Player.                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento per negozi online di tipo 1**](reference-for-type-1-online-stores.md)
</dt> <dt>

[**Gestione remota del controllo di Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




