---
title: Gestione remota del controllo di Windows Media Player
description: Gestione remota del controllo di Windows Media Player
ms.assetid: d543b2a0-a2cb-47e2-b50e-4513fc061b46
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Windows Media Player, controllo ActiveX remoto
- Modello a oggetti di Windows Media Player, controllo ActiveX remoto
- modello a oggetti, controllo ActiveX remoto
- Windows Media Player Mobile, controllo ActiveX remoto
- Controllo ActiveX di Windows Media Player, comunicazione remota
- Controllo ActiveX Windows Media Player Mobile, comunicazione remota
- Controllo ActiveX, comunicazione remota
- controllo ActiveX di Windows Media Player remoto
- incorporamento, controllo ActiveX remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615d3d31535abea098939af65ea67c13acbf8f6c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046435"
---
# <a name="remoting-the-windows-media-player-control"></a>Gestione remota del controllo di Windows Media Player

Quando si incorpora il controllo Windows Media Player in un programma C++, è possibile usarlo come estensione remota della modalità completa del lettore. Questa funzionalità è denominata "comunicazione remota" del controllo Windows Media Player e consente di fornire tutte le funzionalità del lettore in modalità completa senza implementarle autonomamente.

Quando si esegue la modalità remota, il controllo condivide lo stesso motore di riproduzione della modalità completa del lettore e gli utenti possono passare dalla modalità incorporata (lo stato "ancorato") alla modalità completa (lo stato "non ancorato") mentre la riproduzione dei supporti digitali continua senza interruzioni.

## <a name="enabling-remote-embedding"></a>Abilitazione dell'incorporamento remoto

Per abilitare l'incorporamento remoto del controllo Media Player Windows, è necessario che il programma implementi le interfacce **IServiceProvider** e [IWMPRemoteMediaServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices) . **IServiceProvider** è un'interfaccia di Component Object Model standard (com) con un unico metodo denominato **QueryService**. Windows Media Player chiama questo metodo per recuperare un puntatore a un'interfaccia **IWMPRemoteMediaServices** .

**IWMPRemoteMediaServices** dispone di diversi metodi, ma solo due di essi sono direttamente rilevanti per la comunicazione remota. In [getApplicationName](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getapplicationname)si restituisce il nome del programma, che Windows Media Player aggiunge all'elenco **passa ad altro programma** dal menu **Visualizza** . In [GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype)è indicata la modalità di incorporamento del controllo restituendo un valore "Remote" o "local". Se una connessione remota viene stabilita correttamente, il metodo [get \_ Remote](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_isremote) dell'interfaccia [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4) restituisce true.

## <a name="specifying-an-exclusive-online-store"></a>Specifica di un negozio online esclusivo

Con Windows Media Player 11, un'applicazione che incorpora il controllo Player in modalità remota può specificare un negozio online esclusivo. In tal caso, il selettore di servizio in Windows Media Player è disabilitato e solo l'archivio online specificato è disponibile per l'utente. Per informazioni dettagliate su come specificare un negozio online esclusivo, vedere la pagina relativa ai [negozi online esclusivi](exclusive-online-stores.md).

## <a name="docking-and-undocking"></a>Ancoraggio e disancoraggio

L'interfaccia **IWMPPlayer4** fornisce anche l'accesso all'interfaccia [IWMPPlayerApplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication) tramite il metodo [get \_ playerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_playerapplication) . Usare **IWMPPlayerApplication** per spostarsi tra gli stati ancorati e non ancorati e per determinare lo stato ancorato corrente e la posizione del video o della visualizzazione.

Il metodo [IWMPPlayerApplication:: switchToPlayerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtoplayerapplication) Annulla l'ancoraggio del controllo aprendo la modalità completa di Windows Media Player e trasferendo il video o la visualizzazione nel riquadro **Now Playing** . Il metodo [IWMPPlayerApplication:: switchToControl](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtocontrol) ancora il controllo trasferendo la visualizzazione del video o della visualizzazione al programma e chiudendo la modalità completa del lettore, se è aperto. Il controllo può anche essere ancorato selezionando un programma dall'elenco **passa ad altro programma** o chiudendo la modalità completa del lettore. In entrambi i casi, i supporti digitali in riproduzione continuano senza interruzioni.

## <a name="transferring-the-video-or-visualization-display"></a>Trasferimento del video o della visualizzazione

Quando più programmi con controlli Windows Media Player incorporati e remoti vengono eseguiti simultaneamente, tutti i controlli condividono lo stesso motore di riproduzione. Condividono anche la stessa istanza della modalità completa del lettore nello stato non ancorato. Nello stato ancorato, tuttavia, solo un controllo può visualizzare il video o la visualizzazione. Nello stato non ancorato, solo la modalità completa del lettore Visualizza il video o la visualizzazione. Il metodo **switchToControl** funziona sia nello stato ancorato che in quello non ancorato e trasferisce la visualizzazione video o visualizzazione a qualsiasi programma che lo chiama.

L'unica differenza tra gli stati ancorati e non ancorati è la presenza della modalità completa di Windows Media Player e della relativa proprietà della visualizzazione video o visualizzazione. Nello stato non ancorato tutti i controlli incorporati e remoti attualmente in esecuzione sono ancora visibili e le interfacce utente sono ancora completamente funzionanti. Se è presente una finestra video o visualizzazione, tuttavia, è vuota. Nello stato ancorato, solo uno dei controlli in remoto incorporati è proprietario della visualizzazione, ma tutte le interfacce utente continuano a funzionare.

## <a name="hiding-or-changing-the-control-in-the-undocked-state"></a>Nascondere o modificare il controllo nello stato non ancorato

È necessario fornire un'implementazione personalizzata se si desidera nascondere o modificare l'interfaccia utente di un controllo incorporato nello stato non ancorato o quando il programma non è proprietario della visualizzazione. Queste modifiche possono essere apportate quando si ancora e si annulla l'ancoraggio del controllo oppure è possibile modificarle in risposta a eventi di Windows Media Player. Poiché il lettore può essere ancorato tramite l'opzione **di menu passa ad altro programma** , tuttavia, in genere è preferibile fornire questa funzionalità in risposta agli eventi.

È possibile implementare i gestori eventi per gli eventi [SwitchedToPlayerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication) e [SwitchedToControl](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol) oppure è possibile implementare un singolo gestore eventi per l'evento [PlayerDockedStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange) . Nel secondo caso, è possibile determinare lo stato ancorato chiamando [IWMPPlayerApplication:: Get \_ playerDocked](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_playerdocked). In entrambi i casi, usare [IWMPPlayerApplication:: Get \_ hasDisplay](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_hasdisplay) per determinare se il programma è proprietario del video o della visualizzazione.

## <a name="re-establishing-a-remote-connection"></a>Ristabilimento di una connessione remota

In determinate circostanze, la connessione tra un controllo incorporato remoto e il lettore autonomo avrà esito negativo, invalidando i puntatori alle interfacce di Windows Media Player. Windows Media Player tenterà automaticamente di riconnettersi e genererà l'evento [PlayerReconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect) per segnalare questo tentativo. Sebbene la riconnessione sia automatica, è necessario fornire un gestore eventi per questo evento se si vuole rilasciare i puntatori non validi e recuperare quelli nuovi per poter accedere al lettore autonomo tramite la nuova connessione.

## <a name="controlling-the-undocked-player"></a>Controllo del lettore non ancorato

Tutte le istanze remote del controllo Media Player Windows possono modificare la modalità completa del lettore indipendentemente dallo stato ancorato. Le funzionalità che non hanno alcuna pertinenza per la modalità completa del lettore, tuttavia, vengono ignorate fino a quando il controllo Media Player Windows non è ancorato. Sono incluse le proprietà di [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) e le interfacce derivate, ad esempio **Enabled**, **enableContextMenu**, **uiMode** e **windowlessVideo**.

## <a name="error-dialog-boxes"></a>Finestre di dialogo di errore

Da un'istanza di controllo Media Player Windows remota, le *Impostazioni*. la proprietà **enableErrorDialogs** si comporta in modo specifico. Sono applicabili le regole seguenti:

-   Quando Windows Media Player non è ancorato (l'interfaccia utente di Windows Media Player è visibile), la proprietà **enableErrorDialogs** viene ignorata e le finestre di dialogo di errore vengono gestite dal lettore.
-   Quando Windows Media Player è ancorato, il valore specificato da ogni istanza remota del controllo per **enableErrorDialogs** si applica solo alla singola istanza del controllo. Ovvero, se una particolare istanza del controllo specifica il valore "true" per **enableErrorDialogs**, solo tale istanza visualizzerà una finestra di dialogo quando si verifica un errore se tutte le altre istanze del controllo hanno specificato un valore "false".

## <a name="remoting-in-the-background"></a>Comunicazione remota in background

È consigliabile evitare di mantenere un'istanza remota del lettore in esecuzione in background durante i periodi in cui il controllo non è in uso. Poiché l'istanza del controllo del lettore remoto condivide il motore di riproduzione con il lettore in modalità completa, il mantenimento di un'istanza in background può causare un comportamento imprevisto. È ad esempio possibile che l'utente chiuda il lettore in modalità completa mentre è in corso la riproduzione di un file. L'utente si aspetterebbe che la riproduzione dei file si arresti completamente quando il giocatore si chiude, ma l'audio potrebbe continuare a riprodurre perché il motore di riproduzione è ancora attivo.

## <a name="samples"></a>Esempi

Il pacchetto di installazione di Windows Media Player SDK consente di installare esempi che illustrano la comunicazione remota. Per ulteriori informazioni, vedere gli esempi di RemoteSkin e WMPML.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempi**](samples.md)
</dt> <dt>

[**Uso del controllo Media Player di Windows in un programma C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




