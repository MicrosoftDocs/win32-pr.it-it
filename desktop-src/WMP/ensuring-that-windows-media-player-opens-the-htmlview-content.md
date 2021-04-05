---
title: Verifica che Windows Media Player Apra il contenuto di HTMLView
description: Verifica che Windows Media Player Apra il contenuto di HTMLView
ms.assetid: 4ec4e027-4f9c-4a86-9f70-b4014971c070
keywords:
- Playlist Windows Media Metafile, Windows Media Player apertura di contenuto HTMLView
- playlist, Windows Media Player apertura di contenuto HTMLView
- playlist di metafile, Windows Media Player apertura di contenuto HTMLView
- Playlist Windows Media Metafile, apertura del contenuto di HTMLView
- playlist, apertura del contenuto di HTMLView
- playlist di metafile, apertura del contenuto di HTMLView
- apertura del contenuto di HTMLView
- Windows Media Player, apertura del contenuto di HTMLView
- Windows Media Player, contenuto HTMLView
- HTMLView, apertura del contenuto
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3d3220be44fcc33b3657fb115b0bb57d07d1b928
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710975"
---
# <a name="ensuring-that-windows-media-player-opens-the-htmlview-content"></a>Verifica che Windows Media Player Apra il contenuto di HTMLView

Attualmente, le serie Windows Media Player 9 e Windows Media Player 10 sono gli unici lettori che supportano il parametro *HtmlView* nei file con estensione asx. Ciò significa che è necessario eseguire i passaggi per assicurarsi che il contenuto di HTMLView riproduca in queste versioni di Windows Media Player.

È necessario innanzitutto determinare se Windows Media Player 9 o Windows Media Player 10 è installato nel computer dell'utente. Windows Media Player SDK include un esempio completo in cui viene illustrato come rilevare versioni diverse di Windows Media Player in Web browser diversi. Sebbene un'analisi completa dell'esempio di rilevamento esula dall'ambito di questa sezione, è possibile eseguire alcuni passaggi di base per determinare quale versione di Windows Media Player computer dell'utente è in esecuzione.

Nella sua forma più semplice, il rilevamento di Windows Media Player comporta l'incorporamento del controllo lettore nella pagina Web che si collega al contenuto di HTMLView e quindi controlla il valore recuperato dal *lettore*. proprietà **VERSIONINFO** . Dopo aver verificato che l'utente dispone di Windows Media Player 9 serie o Windows Media Player 10 installato, è possibile usare il metodo [Player. openPlayer](player-openplayer.md) per aprire il contenuto nel lettore in modalità piena. Il metodo **openPlayer** garantisce che il contenuto venga inizialmente visualizzato nella funzionalità di **riproduzione** del lettore in modalità completa, anziché in un'interfaccia, in modalità Mini Player o in un altro lettore registrato come programma predefinito per i file con estensione asx, ma non supporta htmlview. Una volta visualizzato il contenuto, tuttavia, l'utente ha il controllo completo di Windows Media Player, vale a dire che può scegliere di visualizzare una funzionalità diversa da **Now**, passare alla modalità Skin o addirittura uscire dal lettore.

Il codice di esempio seguente consente di creare una pagina Web per Internet Explorer. Questa pagina apre un file con estensione asx, che specifica una pagina Web HTMLView che viene visualizzata nel lettore in modalità completa quando è installato Windows Media Player 9 Series o versione successiva.


```XML
<HTML>
<BODY>

<!-- This code embeds the Player object in invisible mode. -->
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6" height = 0 width = 0> 
        <PARAM Name = "AutoStart"  Value = "True">
        <PARAM Name = "uiMode" Value = "invisible">
</OBJECT>

<!-- Create a button to open the content. -->
<INPUT Type = "Button"  ID = "btnPlay"  Value = "Play ASX"  onClick = "PlayASX();"/>

<SCRIPT Language = "JScript">

// This function tests the Player version. If it is Windows Media 
// Player 9 Series or later, the script opens the .asx file in the full-mode 
// Player. Otherwise, the script makes the embedded control visible to 
// the user and opens the .asx file in the webpage. 

function PlayASX()
{
    if(parseInt(Player.versionInfo) >= 9)
        {
            // Open the full-mode Player to show HTMLView.
            Player.openPlayer("https://www.proseware.com/MyHTMLView.asx");
        }
        else
        {
            // Open the .asx file in the embedded Player.
            Player.uiMode = "full";
            Player.height = 200;
            Player.width = 200;
            Player.URL = "https://www.proseware.com/MyHTMLView.asx";
        }
}
</SCRIPT>

</BODY>
</HTML>

```



Il codice nell'esempio precedente incorpora il controllo Windows Media Player con la proprietà **uiMode** impostata su "invisibile" e gli attributi Height e Width del lettore impostati su zero. Ciò è dovuto al fatto che la pagina Web non richiede la visualizzazione iniziale dell'interfaccia utente del controllo del lettore, ma richiede solo l'accesso al modello a oggetti del lettore. La pagina Visualizza anche un pulsante di input che consente all'utente di riprodurre il file con estensione asx.

Quando l'utente fa clic sul pulsante Riproduci ASX, viene eseguita la funzione PlayASX di Microsoft JScript. Questa funzione recupera innanzitutto il valore per la proprietà Player **VERSIONINFO** , usando il metodo JScript **parseInt** per esaminare il valore numerico della stringa recuperata. Se il valore numerico è maggiore o uguale a 9 (vale a dire che l'utente ha installato Windows Media Player 9 Series), il codice di script chiama il metodo **openPlayer** , passando l'URL del file con estensione asx contenente il parametro htmlview. Questo metodo apre il file con estensione asx usando Windows Media Player in modalità completa, riproduce il contenuto multimediale digitale nella playlist. asx e visualizza il contenuto basato sul Web HTMLView nella funzionalità **Now Playing** .

Se il valore numerico della stringa di versione non è maggiore o uguale a 9 (ovvero se per l'utente non è installato Windows Media Player 9 o versione successiva nel computer in uso), il codice di script modifica **uiMode** del controllo Player in "full", imposta una nuova larghezza e altezza per il controllo e quindi apre il file con estensione asx nel lettore incorporato specificando un valore per la proprietà **URL** . In questo caso, il contenuto multimediale digitale viene riprodotto nella pagina Web, ma tutti i valori di HTMLView specificati nel file con estensione ASX vengono ignorati.

Il modo in cui il contenuto viene riprodotto quando l'utente non dispone di Windows Media Player 9 serie o Windows Media Player 10 installato dipende dall'utente. Nell'esempio precedente viene illustrato come specificare che il contenuto viene riprodotto nella pagina Web invece che nel lettore in modalità completa, ignorando qualsiasi contenuto HTMLView nel processo. È possibile adottare altri approcci. Ad esempio, è possibile richiedere all'utente di installare una versione più recente di Windows Media Player, rendendo tale versione del lettore un requisito per la riproduzione del contenuto multimediale digitale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Visualizzazione di pagine Web in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. uiMode**](player-uimode.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 




