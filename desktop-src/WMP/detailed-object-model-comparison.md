---
title: Confronto dettagliato del modello a oggetti
description: Confronto dettagliato del modello a oggetti
ms.assetid: 8f08e2a6-1944-4814-b3b7-680a3722e1a0
keywords:
- Windows Media Player, modello a oggetti
- Modello a oggetti di Windows Media Player, differenze di versione
- modello a oggetti, differenze di versione
- Controllo ActiveX di Windows Media Player, differenze di versione
- Controllo ActiveX, differenze di versione
- Controllo ActiveX Windows Media Player Mobile, differenze di versione
- Windows Media Player Mobile, modello a oggetti
- Guida alla migrazione, differenze di versione
- versioni di Windows Media Player, modello a oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086607a9d367f42479e155e3273c30d88425a457
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104046253"
---
# <a name="detailed-object-model-comparison"></a>Confronto dettagliato del modello a oggetti

Nella tabella seguente vengono confrontate le proprietà del modello a oggetti di Windows Media Player 6,4 con il modello a oggetti di Windows Media Player 7 o versione successiva.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Proprietà di Windows Media Player 6,4</th>
<th>Equivalente a Windows Media Player 7 o versione successiva</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AllowChangeDisplaySize</strong></td>
<td>La visualizzazione di Windows Media Player 7 o versioni successive viene ridimensionata automaticamente per adattarsi ai supporti. È possibile impostare le proprietà Height e Width nel <OBJECT> tag o nello script.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AllowScan</strong></td>
<td><em>Controlli</em>. <strong>fastForward</strong> e <em>controlli</em>. <strong>fastReverse</strong> sono abilitati automaticamente per i tipi di file che supportano questi metodi.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AnglesAvailable</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AnimationAtStart</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AudioStream</strong></td>
<td>Usare i <em>controlli</em>. <strong>currentAudioLanguageIndex</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AudioStreamsAvailable</strong></td>
<td>Usare i <em>controlli</em>. <strong>audioLanguageCount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Riavvolgimento rapido</strong></td>
<td>Usare i <em>controlli</em>. <strong>currentPosition</strong> nello script per specificare o recuperare la posizione corrente. In alternativa, usare i marcatori e il <em>lettore</em>. evento <strong>markerHit</strong> .</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Ridimensiona automaticamente</strong></td>
<td>Il ridimensionamento automatico è il comportamento predefinito. Per eseguire l'override del ridimensionamento automatico, impostare le proprietà Height e Width nel <OBJECT> tag o nello script.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Avvio automatico</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>avvio automatico</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Bilancia</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>saldo</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Larghezza di banda</strong></td>
<td>Utilizzare la <em>rete</em>. <strong>larghezza di banda</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BaseUrl</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>BaseUrl</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingCount</strong></td>
<td>Utilizzare la <em>rete.</em> <strong>bufferingCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BufferingProgress</strong></td>
<td>Utilizzare la <em>rete</em>. <strong>bufferingProgress</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingTime</strong></td>
<td>Utilizzare la <em>rete</em>. <strong>bufferingTime</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ButtonsAvailable</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanPreview</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CANSCAN</strong></td>
<td>Usare i <em>controlli</em>. i controlli e sono <strong>disponibili</strong>( &quot; FastForward &quot; ). <em></em><strong> Disponibile</strong>( &quot; FastReverse &quot; ).</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanSeek</strong></td>
<td>Usare i <em>controlli</em>. è <strong>disponibile</strong> per verificare se è possibile eseguire un particolare metodo Seek.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CanSeekToMarkers</strong></td>
<td>Usare i <em>controlli</em>. <strong>disponibile</strong>( &quot; CurrentMarker &quot; ). Utilizzare <em>supporti</em>. <strong>markerCount</strong> per recuperare il numero di marcatori in un particolare elemento multimediale. Usare i <em>controlli</em>. <strong>currentMarker</strong> per specificare o recuperare il numero di marcatore corrente.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CaptioningID</strong></td>
<td>Usare <em>ClosedCaption</em>. <strong>captioningID</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CCActive</strong></td>
<td>Non disponibile. Per informazioni sul modo in cui la didascalia chiusa è cambiata in Windows Media Player, vedere <a href="closed-captioning.md">sottotitoli codificati</a> .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChannelDescription</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Canalename</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChannelURL</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ClickToPlay</strong></td>
<td>Non disponibile. È necessario fornire i controlli nell'interfaccia utente per avviare la riproduzione. In alternativa, l'utente può fare clic con il pulsante destro del mouse sull'immagine del video per aprire un menu a comparsa che contiene una selezione <strong>riproduzione/sospensione</strong> se <em>Player</em>. <strong>enableContextMenu</strong> è uguale a true.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ClientID</strong></td>
<td>Non disponibile. Windows Media Player 9 Series o versioni successive consente all'utente di selezionare se un ID giocatore univoco viene trasmesso ai provider di contenuti.<br/> Se l'utente seleziona questa opzione, il lettore invia un ID univoco al server Windows Media. L'ID viene registrato nel file di log del server, che si trova in. cartella <em>system32\logfiles</em> per impostazione predefinita. Il nome del campo di log è &quot; c-playerid &quot; . La registrazione del server non è abilitata per impostazione predefinita in Servizi Windows Media.<br/> Se l'utente non seleziona questa opzione, il server genera un ID di sessione casuale, che è univoco per ogni client per una determinata sessione.<br/> Per ulteriori informazioni, vedere la documentazione della serie Windows Media Services 9.<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CodecCount</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ColorKey</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ConnectionSpeed</strong></td>
<td>Non disponibile. Utilizzare la <em>rete</em>. <strong>bitrate</strong> per determinare la velocità in bit corrente.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ContactAddress</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ContactEmail</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ContactPhone</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CreationDate</strong></td>
<td>Usare <em>mediacollection</em>. <strong>getMediaAtom</strong>( &quot; CreationDate &quot; ) per recuperare l'indice della data Atom di creazione. Utilizzare <em>supporti</em>. <strong>getItemInfoByAtom</strong> per recuperare i metadati.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentAngle</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentAudioStream</strong></td>
<td>Usare i <em>controlli</em>. <strong>currentAudioLanguageIndex</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentButton</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentCCService</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentChapter</strong></td>
<td>Recuperare la playlist corrente. Se la playlist corrente non è uguale a quella restituita da <em>CDROM</em>. <strong>playlist</strong>, quindi non esiste alcun capitolo corrente. In caso contrario, il numero del capitolo corrente è l'indice del supporto corrente nella playlist corrente.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentDiscSide</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentDomain</strong></td>
<td>Usare il <em>DVD</em>. <strong>dominio</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentMarker</strong></td>
<td>Usare i <em>controlli</em>. <strong>currentMarker</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentPosition</strong></td>
<td>Usare i <em>controlli</em>. <strong>currentPosition</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentSubpictureStream</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentTime</strong></td>
<td>Usare i <em>controlli</em>. <strong>currentPositionTimeCode</strong>, <em>controlli</em>. <strong>currentPositionString</strong>o <em>controlli</em>. <strong>CurrentPosition.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentTitle</strong></td>
<td>Recuperare la playlist corrente. Se la playlist corrente corrisponde alla playlist restituita dal <em>CDROM</em>. <strong>playlist</strong>, il numero del titolo è l'indice del supporto corrente nella playlist corrente.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentVolume</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CursorType</strong></td>
<td>Non disponibile. Usare invece gli stili di Internet Explorer.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DefaultFrame</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>DefaultFrame</strong>oppure usare un <PARAM> attributo nell' <OBJECT> elemento: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>DisplayBackColor</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DisplayForeColor</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>DisplayMode</strong></td>
<td>La posizione corrente può essere recuperata in pochi secondi dall'inizio come <strong>numero</strong> usando i <em>controlli</em>. <strong>currentPosition</strong>, sotto forma di <strong>stringa</strong> in formato HH: mm: SS (hours, minutes, seconds) utilizzando i <em>controlli</em>. <strong>currentPositionString</strong>o nel formato del codice temporale utilizzando i <em>controlli</em>. <strong>currentPositionTimeCode</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DisplaySize</strong></td>
<td>La visualizzazione predefinita viene ridimensionata automaticamente per adattarsi ai supporti. È possibile impostare le proprietà Height e Width nel <OBJECT> tag o nello script. Usare <em>Player</em>. <strong>schermo</strong> intero per passare alla modalità schermo intero.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Durata</strong></td>
<td>Utilizzare <em>supporti</em>. <strong>durata</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DVD</strong> di</td>
<td>Usare <em>Player</em>. <strong>DVD</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableContextMenu</strong></td>
<td>Usare <em>Player</em>. <strong>enableContextMenu</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Abilitato</strong></td>
<td>Usare <em>Player</em>. <strong>abilitata</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableFullScreenControls</strong></td>
<td>Quando si usa Windows Media Player 9 Series o versioni successive, i controlli a schermo intero vengono abilitati automaticamente a meno che non sia il <em>lettore</em>. <strong></strong>  =  uiMode &quot; nessuno &quot; .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EnablePositionControls</strong></td>
<td>Non disponibile. È possibile fornire controlli personalizzati o utilizzare <em>Player</em>. <strong>uiMode</strong> per scegliere una configurazione predefinita.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableTracker</strong></td>
<td>Non disponibile. È possibile fornire un controllo personalizzato o usare un <em>lettore</em>. <strong>uiMode</strong> per scegliere una configurazione predefinita.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EntryCount</strong></td>
<td>Usare <em>playlist</em>. <strong>numero</strong> di</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong></strong> Codice errore</td>
<td>Usare <em>ErrorItem</em>. <strong>ErrorCode</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ErrorCorrection</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ErrorDescription</strong></td>
<td>Usare <em>ErrorItem</em>. <strong>errorDescription</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Nome file</strong></td>
<td>Usare <em>Player</em>. <strong>URL</strong> o <em>lettore</em>. <strong>currentMedia</strong>. Usare i <em>controlli</em>. <strong>CurrentItem</strong> quando si lavora all'interno di una playlist.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FramesPerSecond</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>HasError</strong></td>
<td>Usare l' <em>errore</em>. <strong>ErrorCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>HasMultipleItems</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ImageSourceHeight</strong></td>
<td>Utilizzare <em>supporti</em>. <strong>imageSourceHeight</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ImageSourceWidth</strong></td>
<td>Utilizzare <em>supporti</em>. <strong>imageSourceWidth</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>InvokeURLs</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>invokeURLs</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Trasmissione</strong></td>
<td>Utilizzare la <em>rete</em>. <strong>sourceProtocol</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>IsDurationValid</strong></td>
<td>Non disponibile. <em>Supporti</em>. <strong>Duration</strong> contiene un valore valido se utilizzato con l'oggetto multimediale corrente.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Lingua</strong> di</td>
<td>Usare i <em>controlli</em>. <strong>currentAudioLanguage</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>LostPackets</strong></td>
<td>Utilizzare la <em>rete</em>. <strong>lostPackets</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>MarkerCount</strong></td>
<td>Utilizzare <em>supporti</em>. <strong>markerCount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Disattiva</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>Disattiva</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>OpenState</strong></td>
<td>Usare <em>Player</em>. <strong>openState</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PlayCount</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>playCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Riproduzione</strong></td>
<td>Usare <em>Player</em>. <strong>riproduzione</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PreviewMode</strong></td>
<td>Non disponibile. Usare una struttura del ciclo di script con un timer HTML per duplicare questa funzionalità.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Frequenza</strong> di</td>
<td>Usare <em>Impostazioni</em>. <strong>frequenza</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReadyState</strong></td>
<td>Usare <em>Player</em>. <strong>openState</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ReceivedPackets</strong></td>
<td>Utilizzare la <em>rete</em>. <strong>receivedPackets</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReceptionQuality</strong></td>
<td>Utilizzare la <em>rete</em>. <strong>receptionQuality</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>RecoveredPackets</strong></td>
<td>Utilizzare la <em>rete</em>. <strong>recoveredPackets</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Radice</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SAMIFileName</strong></td>
<td>Usare <em>ClosedCaption</em>. <strong>SAMIFileName</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SAMILang</strong></td>
<td>Usare <em>ClosedCaption</em>. <strong>SAMILang</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SAMIStyle</strong></td>
<td>Usare <em>ClosedCaption</em>. <strong>SAMIStyle</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SelectionEnd</strong></td>
<td>Utilizzare <em>supporti</em>. <strong>durata</strong> per determinare la lunghezza di un oggetto <strong>multimediale</strong> . Usare un marcatore con i <em>controlli</em>. <strong>currentMarker</strong> per specificare una posizione finale personalizzata.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SelectionStart</strong></td>
<td>Usare i <em>controlli</em>. <strong>currentPosition</strong> avviare la riproduzione da una posizione specifica o utilizzare un marcatore con i <em>controlli</em>. <strong>currentMarker</strong> per specificare una posizione iniziale personalizzata.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendErrorEvents</strong></td>
<td>Gli errori vengono accodati. Usare l'oggetto <strong>Error</strong> e l'oggetto <strong>ErrorItem</strong> per recuperare le informazioni sull'errore.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SendKeyboardEvents</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendMouseClickEvents</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SendMouseMoveEvents</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendOpenStateChangeEvents</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SendPlayStateChangeEvents</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendWarningEvents</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowAudioControls</strong></td>
<td>Non disponibile. È possibile fornire controlli personalizzati o utilizzare <em>Player</em>. <strong>uiMode</strong> per scegliere una configurazione predefinita.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowCaptioning</strong></td>
<td>Non disponibile. È possibile fornire una visualizzazione didascalia personalizzata chiusa.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowControls</strong></td>
<td>Non disponibile. È possibile fornire controlli personalizzati o utilizzare <em>Player</em>. <strong>uiMode</strong> per scegliere una configurazione predefinita.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDisplay</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowGotoBar</strong></td>
<td>Non disponibile. È possibile fornire funzionalità personalizzate utilizzando l'oggetto multimediale</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowPositionControls</strong></td>
<td>Non disponibile. È possibile fornire controlli personalizzati o utilizzare <em>Player</em>. <strong>uiMode</strong> per scegliere una configurazione predefinita.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowStatusBar</strong></td>
<td>Non disponibile. È possibile fornire controlli personalizzati o utilizzare <em>Player</em>. <strong>uiMode</strong> per scegliere una configurazione predefinita.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowTracker</strong></td>
<td>Non disponibile. È possibile fornire controlli personalizzati o utilizzare <em>Player</em>. <strong>uiMode</strong> per scegliere una configurazione predefinita.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SourceLink</strong></td>
<td>Utilizzare <em>supporti</em>. <strong>sourceURL</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SourceProtocol</strong></td>
<td>Utilizzare la <em>rete</em>. <strong>sourceProtocol</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamCount</strong></td>
<td>Non disponibile. Usare i <em>controlli</em>. <strong>audioLanguageCount</strong> per recuperare il numero di flussi di lingua audio.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SubpictureOn</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SubpictureStreamsAvailable</strong></td>
<td>Non disponibile</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TitlesAvailable</strong></td>
<td>Usare il codice seguente:<code>Player.Cdrom.playlist.count - 1</code><br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TotalTitleTime</strong></td>
<td>Usare <em>currentMedia</em>. <strong>Duration</strong> o <em>currentMedia</em>. <strong>durationstring</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TransparentAtStart</strong></td>
<td>Usare lo script per specificare i valori di altezza e larghezza per rendere il lettore visibile o invisibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>UniqueId</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VideoBorder3D</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>VideoBorderColor</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VideoBorderWidth</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Volume</strong> di</td>
<td>Usare <em>Impostazioni</em>. <strong>Volume</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VolumesAvailable</strong></td>
<td>Non disponibile.</td>
</tr>
</tbody>
</table>



 

Nella tabella seguente vengono confrontati i metodi del modello a oggetti di Windows Media Player versione 6,4 con il modello a oggetti di Windows Media Player 7 o versioni successive.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Metodo Windows Media Player 6,4</th>
<th>Equivalente a Windows Media Player 7 o versione successiva</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AboutBox</strong></td>
<td>Usare <em>Player</em>. <strong>VERSIONINFO</strong> per recuperare la versione di Windows Media Player.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BackwardScan</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>frequenza</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ButtonActivate</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ButtonSelectAndActivate</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Annulla</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChapterPlay</strong></td>
<td>Se si sta già eseguendo la playlist del titolo specificata, recuperare il capitolo desiderato come oggetto multimediale usando la sintassi seguente:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Quindi, specificare <em>Player</em>. <strong>currentMedia</strong> utilizzando l'oggetto multimediale restituito.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChapterPlayAutoStop</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChapterSearch</strong></td>
<td>Se si sta già eseguendo la playlist del titolo specificata, recuperare il capitolo desiderato come oggetto multimediale usando la sintassi seguente:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Quindi, specificare <em>Player</em>. <strong>currentMedia</strong> utilizzando l'oggetto multimediale restituito.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>FastForward</strong></td>
<td>Usare i <em>controlli</em>. <strong>fastForward</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FastReverse</strong></td>
<td>Usare i <em>controlli</em>. <strong>fastReverse</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ForwardScan</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>frequenza</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetAllGPRMs</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetAllSPRMs</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetAudioLanguage</strong></td>
<td>Usare i <em>controlli</em>. <strong>currentAudioLanguage</strong> per recuperare l'LCID della lingua audio corrente.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetCodecDescription</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetCodecInstalled</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetCodecURL</strong></td>
<td>Usare <em>ErrorItem</em>. <strong>customUrl</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetCurrentEntry</strong></td>
<td>Usare script per scorrere in ciclo la playlist corrente. Utilizzare <em>supporti</em>. è <strong>identico</strong> per confrontare ogni voce della playlist con il <em>lettore</em>. oggetto <strong>currentMedia</strong> .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Getmarcatore</strong></td>
<td>Utilizzare <em>supporti</em>. <strong>Getmarkname</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMarkerTime</strong></td>
<td>Utilizzare <em>supporti</em>. <strong>getMarkerTime</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaInfoString</strong></td>
<td>Utilizzare <em>supporti</em>. <strong>GetItemInfo</strong>, <em>supporto</em>. <strong>getItemInfoByAtom</strong>e i metodi associati per recuperare i metadati.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMediaParameter</strong></td>
<td>Usare <em>playlist</em>. <strong>elemento</strong> per recuperare un elemento multimediale. Usare quindi i <em>supporti</em>. <strong>GetItemInfo</strong> per recuperare la stringa di parametro.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaParameterName</strong></td>
<td>Usare <em>playlist</em>. <strong>elemento</strong> per recuperare un elemento multimediale. Usare quindi i <em>supporti</em>. <strong>GetAttribute</strong> per recuperare la stringa di parametro.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMoreInfoURL</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetNumberOfChapters</strong></td>
<td>Se un titolo è attualmente in riproduzione, usare <em>currentPlaylist</em>. <strong>conteggio</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetStreamGroup</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetStreamName</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetStreamSelected</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetSubpictureLanguage</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Goup</strong></td>
<td>Usare il <em>DVD</em>. <strong>indietro</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>IsSoundCardEnabled</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>LeftButtonSelect</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>LowerButtonSelect</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>MenuCall</strong></td>
<td>Usare il <em>DVD</em>. <strong>titleMenu</strong> o <em>DVD</em>. <strong>menu di scelta rapida</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Avanti</strong></td>
<td>Usare i <em>controlli</em>. <strong>quindi</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>NextPGSearch</strong></td>
<td>Usare i <em>controlli</em>. <strong>quindi</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Apri</strong></td>
<td>Usare <em>Player</em>. <strong>URL</strong> o <em>lettore</em>. <strong>currentMedia</strong>. I file vengono sempre aperti in modo asincrono.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Sospendi</strong></td>
<td>Usare i <em>controlli</em>. <strong>Sospendi</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Esegui la riproduzione</strong></td>
<td>Usare i <em>controlli</em>. <strong>Riproduci</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Precedente</strong></td>
<td>Usare i <em>controlli</em>. <strong>precedente</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PrevPGSearch</strong></td>
<td>Usare i <em>controlli</em>. <strong>precedente</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ResumeFromMenu</strong></td>
<td>Usare il <em>DVD</em>. <strong>riprendere</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>RightButtonSelect</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SetCurrentEntry</strong></td>
<td>Recuperare un oggetto multimediale utilizzando <em>currentPlaylist</em>. <strong>elemento</strong>(<em>entryNumber</em>). Specificare quindi l'oggetto supporto recuperato utilizzando i <em>controlli</em>. <strong>CurrentItem</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDialog</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StillOff</strong></td>
<td>Usare i <em>controlli</em>. <strong>Riproduci</strong>. In alternativa, usare i <em>controlli</em>. A questo punto <strong>, se attualmente</strong> si trova in modalità continua.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Arresta</strong></td>
<td>Usare i <em>controlli</em>. <strong>arrestare</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamSelect</strong></td>
<td>Non disponibile. Usare i <em>controlli</em>. <strong>currentAudioLanguage</strong> per specificare un flusso di lingua audio.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TimePlay</strong></td>
<td>Dalla playlist radice usare <em>currentPlaylist</em>. <strong>elemento</strong>(<em>Indice</em>) per recuperare un oggetto multimediale. Impostare quindi l'oggetto supporto come quello corrente usando i <em>controlli</em>. <strong>CurrentItem</strong>. Specificare quindi i <em>controlli</em>. <strong>currentPosition</strong> che utilizza un valore di ora in secondi.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TimeSearch</strong></td>
<td>Usare i <em>controlli</em>. <strong>currentPosition</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TitlePlay</strong></td>
<td>Se si sta già eseguendo la playlist del titolo specificata, recuperare il capitolo desiderato come oggetto multimediale usando la sintassi seguente:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Quindi, specificare <em>Player</em>. <strong>currentMedia</strong> utilizzando l'oggetto multimediale restituito.<br/> In alternativa, usare <em>currentPlaylist</em>. <strong>elemento</strong> per recuperare un oggetto multimediale, quindi utilizzare l'oggetto multimediale restituito per specificare i <em>controlli</em>. <strong>CurrentItem</strong>.<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TopPGSearch</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>UOPValid</strong></td>
<td>Non disponibile</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>UpperButtonSelect</strong></td>
<td>Non disponibile.</td>
</tr>
</tbody>
</table>



 

Nella tabella seguente vengono confrontati gli eventi del modello a oggetti di Windows Media Player versione 6,4 con il modello a oggetti di Windows Media Player 7 o versioni successive.



| Evento Windows Media Player 6,4  | Equivalente a Windows Media Player 7 o versione successiva                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Player6*. **Memorizzazione nel buffer**         | Usare *Player*. **Memorizzazione nel buffer**.                                                                                                                                                                                              |
| *Player6*. **Fare clic su**             | Usare *Player*. **Fare clic su**                                                                                                                                                                                                   |
| *Player6*. **DblClick**          | Usare *Player*. **DoubleClick**                                                                                                                                                                                             |
| *Player6*. **Disconnetti**        | Non disponibile.                                                                                                                                                                                                           |
| *Player6*. **DisplayModeChange** | Non disponibile.                                                                                                                                                                                                           |
| *Player6*. **DVDNotify**         | *Player*. **DomainChange** e *Player*. **OpenPlaylistSwitch** sono eventi specifici del DVD. Potrebbero essere applicati anche altri eventi relativi a playlist, supporti multimediali e CD-ROM, a seconda dell'applicazione.                        |
| *Player6*. **EndOfStream**       | Usare *Player*. **Riproduzione**.                                                                                                                                                                                              |
| *Player6*. **Errore**             | L'evento è invariato. Gli errori, tuttavia, vengono accodati. Usare l'oggetto **Error** con l'oggetto **ErrorItem** per recuperare le informazioni sull'errore dalla coda. Vedere il codice di esempio nella sezione precedente, gestione degli errori. |
| *Player6*. **KeyDown**           | Usare *Player*. **KeyDown**                                                                                                                                                                                                 |
| *Player6*. **Pressione** del tasto          | Usare *Player*. **Pressione** del tasto                                                                                                                                                                                                |
| *Player6*. **Evento KeyUp**             | Usare *Player*. **Evento KeyUp**                                                                                                                                                                                                   |
| *Player6*. **MarkerHit**         | Usare *Player*. **MarkerHit**.                                                                                                                                                                                              |
| *Player6*. **MouseDown**         | Usare *Player*. **MouseDown**                                                                                                                                                                                               |
| *Player6*. **MouseMove**         | Usare *Player*. **MouseMove**                                                                                                                                                                                               |
| *Player6*. **MouseUp**           | Usare *Player*. **MouseUp**                                                                                                                                                                                                 |
| *Player6*. **NewStream**         | Usare *Player*. **OpenStateChange**                                                                                                                                                                                         |
| *Player6*. **OpenStateChange**   | Usare *Player*. **OpenStateChange**.                                                                                                                                                                                        |
| *Player6*. **PlayStateChange**   | Usare *Player*. **PlayStateChange**.                                                                                                                                                                                        |
| *Player6*. **PositionChange**    | Usare *Player*. **PositionChange**.                                                                                                                                                                                         |
| *Player6*. **ReadyStateChange**  | Usare *Player*. **PlayStateChange**.                                                                                                                                                                                        |
| *Player6*. **ScriptCommand**     | Usare *Player*. **ScriptCommand**.                                                                                                                                                                                          |
| *Player6*. **Avviso** di           | Non disponibile.                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla migrazione del modello a oggetti**](object-model-migration-guide.md)
</dt> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





