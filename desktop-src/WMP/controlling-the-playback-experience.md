---
title: Controllo dell'esperienza di riproduzione
description: Controllo dell'esperienza di riproduzione
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Playlist Windows Media Metafile, controllo della riproduzione
- playlist, controllo della riproduzione
- playlist di metafile, controllo della riproduzione
- Playlist Windows Media Metafile, problemi di riproduzione
- playlist, problemi di riproduzione
- playlist di metafile, problemi di riproduzione
- controllo della riproduzione
- Windows Media Player, controllo della riproduzione
- Media Player di Windows, problemi di riproduzione
- HTMLView, problemi di riproduzione
- HTMLView, controllo della riproduzione
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6877b869be8ca38ef9266aedf9318103d0e547ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298519"
---
# <a name="controlling-the-playback-experience"></a>Controllo dell'esperienza di riproduzione

In questa sezione vengono illustrati alcuni dei problemi di riproduzione che possono verificarsi quando si usa la funzionalità HTMLView.

## <a name="requiring-the-user-to-view-web-based-content"></a>Richiedere all'utente di visualizzare il contenuto basato sul Web

Si può decidere di consentire agli utenti di usare il contenuto multimediale digitale solo quando viene visualizzato anche il contenuto basato sul Web HTMLView. È possibile includere codice di script nella pagina Web di HTMLView che interrompe la riproduzione del contenuto multimediale digitale se l'utente passa dalla funzionalità **ora in gioco** . A tale scopo, è possibile specificare un gestore eventi per l'evento **unload** come parte dell'elemento **Body** , come illustrato nel codice HTML seguente:


```XML
<BODY onunload = "UnloadMe();">

```



È quindi possibile includere il codice di script nella funzione del gestore eventi per chiudere il file nel lettore. Il codice di esempio seguente esegue questa operazione:


```XML
function UnloadMe()
{
   Player.close();
}

```



Quando l'utente passa dall' **ora alla riproduzione** facendo clic su un pulsante per aprire un'altra funzionalità di Windows Media Player, ad esempio la libreria, il lettore chiude il browser incorporato. In questo modo si verifica l'evento **OnUnload** , eseguendo lo script nella funzione denominata **UnloadMe**. Il metodo [Player. Close](player-close.md) interrompe la riproduzione e Scarica il file multimediale digitale corrente. Per visualizzare nuovamente il contenuto, è necessario che l'utente riapra il file. asx originale. Questa tecnica interrompe anche la riproduzione quando l'utente si sposta dalla pagina Web HTMLView. Si noti che questa tecnica non può impedire all'utente di visualizzare il contenuto multimediale digitale quando passa alla modalità personalizzata.

Si ricorda che il parametro HTMLView può essere applicato a ogni elemento **entry** in un file con estensione asx. È possibile sfruttare questa funzionalità per garantire che il contenuto di HTMLView venga visualizzato ogni volta che viene avviato un nuovo file multimediale digitale. A tale scopo, associare un elemento **param** per HtmlView a ogni voce della playlist. asx. Quando ogni voce viene riprodotta, il lettore torna alla modalità Full e visualizza il contenuto HTMLView specificato nella playlist.

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a>I tipi di comando per script di FILE e URL sono disabilitati per impostazione predefinita

Windows Media Player 9 Series o versioni successive fornisce impostazioni che consentono all'utente di specificare se è possibile eseguire i comandi di script di tipo URL e FILE. Per impostazione predefinita, entrambi i tipi di comando per script non vengono eseguiti. Se si usano tipi di comando per script personalizzati, continueranno a essere eseguiti, indipendentemente dall'impostazione dell'utente. Se è necessario usare i comandi di script di tipo FILE e URL, è necessario richiedere all'utente di modificare le impostazioni. Per modificare le impostazioni, fare clic su **strumenti**, quindi su **Opzioni** e infine su **sicurezza**.

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a>La riapertura di un HTMLView non consente di ricaricare la pagina Web

Quando l'utente apre un file con estensione asx che include un parametro HTMLView e successivamente riapre lo stesso file, Windows Media Player non aggiorna la pagina Web HTMLView. Ciò significa anche che se gli utenti sono autorizzati a uscire dalla pagina Web di HTMLView, il lettore non restituisce il browser incorporato alla pagina Web HTMLView iniziale.

## <a name="hiding-the-content-location"></a>Nascondere il percorso del contenuto

Si potrebbe decidere di non volere che Windows Media Player visualizzi il percorso del contenuto multimediale digitale mentre sta eseguendo un file con estensione asx. In genere, Windows Media Player Visualizza solo le informazioni sulla playlist stessa quando si esegue lo streaming del contenuto da Internet. Tuttavia, è possibile eseguire altri passaggi per impedire agli utenti di determinare la posizione del contenuto. Ad esempio, un modo per assicurarsi che il lettore non visualizzi il percorso del contenuto è quello di trasmettere il contenuto tramite playlist lato server di servizi Windows Media. In questo modo, quando l'utente visualizza le proprietà per il contenuto, vede l'URL del server e non l'URL del contenuto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Visualizzazione di pagine Web in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**PARAM (elemento)**](param-element.md)
</dt> </dl>

 

 




