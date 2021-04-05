---
title: Problemi di pagina Web
description: Problemi di pagina Web
ms.assetid: fd97540e-21e9-443e-99ec-ed29f4a2570a
keywords:
- Playlist Windows Media Metafile, pagine Web
- playlist, pagine Web
- playlist di metafile, pagine Web
- Playlist Windows Media Metafile, personalizzazione di HTMLView
- playlist, personalizzazione di HTMLView
- playlist di metafile, personalizzazione di HTMLView
- Playlist Windows Media Metafile, personalizzazione HTMLView
- playlist, personalizzazione di HTMLView
- playlist di metafile, personalizzazione di HTMLView
- personalizzazione di HTMLView
- Windows Media Player, pagine Web
- Windows Media Player, personalizzazione di HTMLView
- Media Player di Windows, personalizzazione di HTMLView
- HTMLView, personalizzazione
- HTMLView, pagine Web
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 882d8993ba3690cf8c4a068f9861ccf39cd1a95c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713402"
---
# <a name="web-page-issues"></a>Problemi di pagina Web

Quando si crea una pagina Web da visualizzare nella funzionalità Windows Media Player **Now Playing** , è necessario prendere in considerazione alcuni aspetti. In questa sezione vengono illustrati alcuni dei problemi che possono verificarsi durante la creazione del contenuto basato sul Web.

## <a name="customizing-htmlview"></a>Personalizzazione di HTMLView

La pagina Web di HTMLView può essere semplice o complessa. È possibile includere gli elementi utilizzati in genere nel contenuto basato sul Web. Se si incorpora il controllo Media Player di Windows, è possibile visualizzare una delle interfacce utente fornite dal controllo, creare una propria interfaccia utente utilizzando codice HTML e script o non fornire alcuna interfaccia utente (il che significa che l'utente può utilizzare i controlli di trasporto del lettore in modalità completa).

Le dimensioni consigliate per le pagine Web visualizzate con la funzionalità HTMLView sono 575 x 345 pixel. L'utente, tuttavia, ha la possibilità di ridimensionare Media Player di Windows e scegliere la risoluzione dello schermo. Se la pagina Web HTMLView è più grande delle dimensioni configurate dalla funzionalità **Now Playing** , il lettore Visualizza barre di scorrimento orizzontali e verticali che consentono all'utente di visualizzare l'intera pagina. È necessario testare il contenuto di HTMLView usando un'ampia gamma di risoluzioni dello schermo e dimensioni dei lettori per determinare le dimensioni migliori per la pagina Web.

Windows Media Player non fornisce un metodo che consente di specificare una dimensione per il lettore in modalità completa.

## <a name="web-page-navigation"></a>Navigazione di pagine Web

Windows Media Player non fornisce una barra degli strumenti di navigazione per le pagine Web visualizzate nella funzionalità **Now Playing** . Ciò significa che è possibile controllare completamente se gli utenti possono uscire dalla pagina Web di HTMLView. Se si desidera consentire agli utenti di passare ad altre pagine Web, è necessario includere elementi nel codice HTML per fornire tale funzionalità.

## <a name="retrieving-the-parent-window"></a>Recupero della finestra padre

Se il codice di script esistente usa **Window. Parent** per recuperare l'oggetto finestra padre, il codice non funzionerà nella pagina Web htmlview. Quando si usa HTMLView, non è presente alcun oggetto finestra padre; Pertanto, questa funzionalità di scripting non è disponibile.

## <a name="about-the-embedded-browser"></a>Informazioni sul browser incorporato

Poiché Windows Media Player utilizza un'istanza incorporata di Internet Explorer per visualizzare il contenuto di HTMLView, le impostazioni utente e i criteri per Internet Explorer si applicano a tutte le pagine Web visualizzate nel lettore. Se, ad esempio, l'utente ha configurato Internet Explorer per impedire che le pagine Web scarichino i cookie nel computer, non è possibile eseguire questa operazione nella pagina Web HTMLView.

Le pagine Web aperte con la funzionalità HTMLView vengono sempre eseguite nell'area di sicurezza **Internet** di Internet Explorer.

Il controllo Web browser incorporato usa le stesse regole per memorizzare nella cache le pagine Web come la versione autonoma di Internet Explorer. È consigliabile usare Active Server Pages (ASP) quando si crea il contenuto per garantire che il contenuto venga distribuito dal server Web ogni volta che Windows Media Player accede alla pagina Web HTMLView. L'utilizzo di pagine ASP può essere semplice quanto la ridenominazione della pagina Web per l'utilizzo di un'estensione del nome di file ASP.

## <a name="about-local-web-content"></a>Informazioni sul contenuto Web locale

La funzionalità HTMLView non consente di aprire le pagine Web archiviate nel computer dell'utente.

## <a name="prompting-the-user"></a>Invio di una richiesta all'utente

È possibile utilizzare **Window. prompt** per richiedere informazioni all'utente. Tuttavia, **Window. Alert** e **Window. Confirm** non sono disponibili quando si usa htmlview.

## <a name="timing-issues"></a>Problemi di temporizzazione

È possibile che si verifichino problemi temporali quando si usa un controllo di Windows Media Player incorporato nella pagina Web HTMLView. In HTMLView, un controllo lettore incorporato condivide il motore di riproduzione con le Media Player Windows autonome. È possibile che il lettore autonomo possa aprire e iniziare a riprodurre la prima voce della playlist prima che la pagina Web (e, pertanto, il controllo Player) finisca il caricamento. Ciò significa che se si gestiscono gli eventi **OpenStateChange** o **PlayStateChange** , il codice di script non riceverà le notifiche degli eventi per questi eventi fino a quando non verrà caricato il controllo del lettore e gli oggetti associati.

È possibile eseguire le operazioni nel codice per ritardare la riproduzione fino a quando non viene creata un'istanza del controllo Windows Media Player. A questo scopo, è possibile fare in modo che la prima voce nella playlist del metafile punti a un file di immagine e impostare la durata del file su un periodo di tempo che consenta il caricamento del controllo lettore. Nell'esempio di codice seguente viene illustrata questa opzione:


```XML
<ASX version="3.0">
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>

<ENTRY>
   <REF href="https://www.proseware.com/blank.jpg"/>
   <DURATION  VALUE = "1:00"/>
</ENTRY>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



Quando si apre la playlist precedente, Windows Media Player attende la prima voce nella playlist per un massimo di un minuto mentre il giocatore carica la pagina Web HTMLView.

Quindi, nella pagina Web di HTMLView, scrivere codice script per gestire l'evento **OnLoad** per l'elemento **Body** . Nella funzione del gestore eventi chiamare il metodo Player **Controls. Next** per iniziare la riproduzione della seconda voce nella playlist.


```XML
<HTML>
<!-- Define the event handler function. -->
<BODY  onload = "OnLoad();">

<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">

</OBJECT>

<!-- Handle the BODY onload event. -->
<SCRIPT>
function OnLoad()
{
   // Advance to the second entry in the playlist.
   Player.controls.next();
}
</SCRIPT>

</BODY>
</HTML>

```



Quando la pagina Web nell'esempio precedente termina il caricamento, Windows Media Player avanza immediatamente alla seconda voce della playlist. Questa operazione sostituisce la durata specificata per il primo elemento nella playlist, ovvero l'utente non deve attendere il completamento di un minuto prima di visualizzare il contenuto desiderato; deve attendere il completamento del caricamento della pagina Web. Poiché a questo punto viene creata completamente un'istanza del controllo Player, gli eventi **OpenStateChange** e **PlayStateChange** possono essere gestiti nel modo consueto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Visualizzazione di pagine Web in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Evento Player. PlayStateChange**](player-player-playstatechange.md)
</dt> <dt>

[**Evento Player. OpenStateChange**](player-player-openstatechange.md)
</dt> </dl>

 

 




