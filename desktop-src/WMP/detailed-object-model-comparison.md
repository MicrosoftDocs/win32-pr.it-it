---
title: Confronto dettagliato del modello a oggetti
description: Confronto dettagliato del modello a oggetti
ms.assetid: 8f08e2a6-1944-4814-b3b7-680a3722e1a0
keywords:
- Windows Media Player,modello a oggetti
- Windows Media Player a oggetti, differenze di versione
- modello a oggetti,differenze di versione
- Windows Media Player ActiveX controllo, differenze di versione
- ActiveX controllo, differenze di versione
- Windows Media Player Controllo ActiveX per dispositivi mobili, differenze di versione
- Windows Media Player Mobile, modello a oggetti
- guida alla migrazione, differenze di versione
- versioni di Windows Media Player,modello a oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5fb048042fcbaa064fd3a322b90b3ce90a676e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623537"
---
# <a name="detailed-object-model-comparison"></a>Confronto dettagliato del modello a oggetti

Nella tabella seguente vengono confrontate le Windows Media Player del modello a oggetti 6.4 con il modello a oggetti Windows Media Player 7 o versione successiva.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Windows Media Player 6.4</th>
<th>Windows Media Player 7 o versione successiva equivalente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AllowChangeDisplaySize</strong></td>
<td>La visualizzazione di Windows Media Player 7 o versioni successive viene ridimensionata automaticamente in base al supporto. È possibile impostare le proprietà height e width nel <OBJECT> tag o nello script.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AllowScan</strong></td>
<td><em>Controlla</em>. <strong>fastForward</strong> e <em>Controls</em>. <strong>fastReverse viene</strong> abilitato automaticamente per i tipi di file che supportano questi metodi.</td>
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
<td>Usare <em>i controlli</em>. <strong>currentAudioLanguageIndex</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AudioStreamsAvailable</strong></td>
<td>Usare <em>i controlli</em>. <strong>audioLanguageCount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Riavvolgimento automatico</strong></td>
<td>Usare <em>i controlli</em>. <strong>currentPosition</strong> nello script per specificare o recuperare la posizione corrente. In alternativa, usare i marcatori e <em>player</em>. <strong>evento markerHit.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AutoSize</strong></td>
<td>Il ridimensionamento automatico è il comportamento predefinito. Per eseguire l'override del ridimensionamento automatico, impostare le proprietà height e width nel <OBJECT> tag o nello script.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Avvio automatico</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>autoStart</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Saldo</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>bilanciare</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Larghezza di banda</strong></td>
<td>Usare <em>Rete</em>. <strong>bandWidth</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BaseURL</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>baseURL</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingCount</strong></td>
<td>Usare <em>Rete.</em> <strong>bufferingCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BufferingProgress</strong></td>
<td>Usare <em>Rete</em>. <strong>bufferingProgress</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingTime</strong></td>
<td>Usare <em>Rete</em>. <strong>bufferingTime</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>PulsantiDisponibili</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanPreview</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CanScan</strong></td>
<td>Usare <em>i controlli</em>. <strong>isAvailable</strong>( &quot; FastForward &quot; ) e <em>Controls</em>.<strong> isAvailable</strong>( &quot; FastReverse &quot; ).</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanSeek</strong></td>
<td>Usare <em>i controlli</em>. <strong>isAvailable per</strong> verificare se è possibile eseguire un determinato metodo seek.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CanSeekToMarkers</strong></td>
<td>Usare <em>i controlli</em>. <strong>isAvailable</strong>( &quot; CurrentMarker &quot; ). Usare <em>Media</em>. <strong>markerCount</strong> per recuperare il conteggio dei marcatori in un particolare elemento multimediale. Usare <em>i controlli</em>. <strong>currentMarker per</strong> specificare o recuperare il numero del marcatore corrente.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CaptioningID</strong></td>
<td>Usare <em>ClosedCaption</em>. <strong>captioningID</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CCActive</strong></td>
<td>Non disponibile. Vedere <a href="closed-captioning.md">Sottotitoli codificati</a> per informazioni sulla modifica dei sottotitoli codificati in Windows Media Player.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChannelDescription</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChannelName</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChannelURL</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ClickToPlay</strong></td>
<td>Non disponibile. È necessario fornire controlli nell'interfaccia utente per avviare la riproduzione. In alternativa, l'utente può fare clic con il pulsante destro del mouse sull'immagine video per aprire un menu a comparsa contenente una selezione <strong>Riproduci/Sospendi</strong> se <em>Lettore</em>. <strong>enableContextMenu</strong> è uguale a true.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ClientID</strong></td>
<td>Non disponibile. Windows Media Player serie 9 o successive consente all'utente di selezionare se un ID lettore univoco viene trasmesso ai provider di contenuti.<br/> Se l'utente seleziona questa opzione, il lettore invia un ID univoco al server Windows Media. L'ID viene registrato nel file di log del server, che si trova in . <em>cartella system32\logfiles</em> per impostazione predefinita. Il nome del campo del log &quot; è c-playerid &quot; . La registrazione del server non è abilitata per impostazione predefinita in Servizi Windows Media.<br/> Se l'utente non seleziona questa opzione, il server genera un ID sessione casuale, univoco per ogni client per una determinata sessione.<br/> Per altre informazioni, vedere la documentazione Servizi Windows Media serie 9.<br/></td>
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
<td>Non disponibile. Usare <em>Rete</em>. <strong>bitRate</strong> per determinare la velocità in bit corrente.</td>
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
<td>Usare <em>MediaCollection</em>. <strong>getMediaAtom</strong>( &quot; CreationDate &quot; ) per recuperare l'indice dell'atom della data di creazione. Usare <em>Media</em>. <strong>getItemInfoByAtom per</strong> recuperare i metadati.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentAngle</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentAudioStream</strong></td>
<td>Usare <em>i controlli</em>. <strong>currentAudioLanguageIndex</strong>.</td>
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
<td>Recupera la playlist corrente. Se la playlist corrente non è la stessa della playlist restituita da <em>Cdrom</em>. <strong>playlist</strong>, quindi non è presente alcun capitolo corrente. In caso contrario, il numero del capitolo corrente è l'indice del contenuto multimediale corrente nella playlist corrente.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentDiscSide</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentDomain</strong></td>
<td>Usare <em>DVD</em>. <strong>dominio</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentMarker</strong></td>
<td>Usare <em>i controlli</em>. <strong>currentMarker</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentPosition</strong></td>
<td>Usare <em>i controlli</em>. <strong>currentPosition</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentSubpictureStream</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentTime</strong></td>
<td>Usare <em>i controlli</em>. <strong>currentPositionTimeCode</strong>, <em>controlla</em>. <strong>currentPositionString</strong>o <em>Controls</em>. <strong>CurrentPosition.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentTitle</strong></td>
<td>Recupera la playlist corrente. Se la playlist corrente è la stessa della playlist restituita da <em>Cdrom.</em> <strong>playlist</strong>, quindi il numero del titolo è l'indice del contenuto multimediale corrente nella playlist corrente.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentVolume</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Tipo di cursore</strong></td>
<td>Non disponibile. Usare Internet Explorer stili.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DefaultFrame</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>defaultFrame</strong>o usare un oggetto <PARAM> Attributo <OBJECT> nell'elemento : <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></td>
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
<td><em>Player6</em>. <strong>Modalità di visualizzazione</strong></td>
<td>La posizione corrente può essere recuperata in secondi dall'inizio come <strong>numero usando</strong> <em>i controlli</em>. <strong>currentPosition</strong>, come <strong>stringa</strong> formattata come HH:MM:SS (ore, minuti, secondi) usando <em>i controlli</em>. <strong>currentPositionString</strong>o in time code usando <em>Controls</em>. <strong>currentPositionTimeCode</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DisplaySize</strong></td>
<td>La visualizzazione predefinita viene ridimensionata automaticamente in base al supporto. È possibile impostare le proprietà di altezza e larghezza nel <OBJECT> tag o nello script. Usare <em>Player</em>. <strong>fullScreen</strong> per passare alla modalità schermo intero.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Durata</strong></td>
<td>Usare <em>l'oggetto multimediale</em>. <strong>duration</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DVD</strong></td>
<td>Usare <em>Player</em>. <strong>DVD</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableContextMenu</strong></td>
<td>Usare <em>Player</em>. <strong>enableContextMenu</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Abilitato</strong></td>
<td>Usare <em>Player</em>. <strong>abilitato.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableFullScreenControls</strong></td>
<td>Quando si usa Windows Media Player 9 o versioni successive, i controlli a schermo intero vengono abilitati automaticamente a meno che Player non <em>sia</em>. <strong>uiMode</strong>  =  &quot; none &quot; .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EnablePositionControls</strong></td>
<td>Non disponibile. È possibile fornire controlli personalizzati o usare <em>Player.</em> <strong>uimode</strong> per scegliere una configurazione predefinita.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableTracker</strong></td>
<td>Non disponibile. È possibile fornire un controllo personalizzato o usare <em>Player.</em> <strong>uimode</strong> per scegliere una configurazione predefinita.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EntryCount</strong></td>
<td>Usare <em>playlist</em>. <strong>count</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ErrorCode</strong></td>
<td>Usare <em>ErrorItem</em>. <strong>errorCode</strong>.</td>
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
<td><em>Player6</em>. <strong>FileName</strong></td>
<td>Usare <em>Player</em>. <strong>URL o</strong> <em>Player</em>. <strong>currentMedia.</strong> Usare <em>i controlli</em>. <strong>currentItem quando</strong> si lavora all'interno di una playlist.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FramePerSecond</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>HasError</strong></td>
<td>Usare <em>Error</em>. <strong>errorCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>HasMultipleItems</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ImageSourceHeight</strong></td>
<td>Usare <em>l'oggetto multimediale</em>. <strong>imageSourceHeight</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ImageSourceWidth</strong></td>
<td>Usare <em>l'oggetto multimediale</em>. <strong>imageSourceWidth</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>InvokeURLs</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>invokeURLs</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>IsBroadcast</strong></td>
<td>Usare <em>rete</em>. <strong>sourceProtocol</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>IsDurationValid</strong></td>
<td>Non disponibile. <em>Oggetto multimediale.</em> <strong>duration</strong> contiene un valore valido se usato con l'oggetto multimediale corrente.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Lingua</strong></td>
<td>Usare <em>i controlli</em>. <strong>currentAudioLanguage</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Oggetti LostPackets</strong></td>
<td>Usare <em>rete</em>. <strong>lostPackets</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>MarkerCount</strong></td>
<td>Usare <em>l'oggetto multimediale</em>. <strong>markerCount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Disattiva audio</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>Disattivare l'audio</strong>di .</td>
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
<td><em>Player6</em>. <strong>PlayState</strong></td>
<td>Usare <em>Player</em>. <strong>playState</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PreviewMode</strong></td>
<td>Non disponibile. Usare una struttura del ciclo di script con un timer HTML per duplicare questa funzionalità.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Frequenza</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>rate</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReadyState</strong></td>
<td>Usare <em>Player</em>. <strong>openState</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ReceivedPackets</strong></td>
<td>Usare <em>Rete</em>. <strong>receivedPackets</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReceptionQuality</strong></td>
<td>Usare <em>Rete</em>. <strong>receptionQuality</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>RecoveredPackets</strong></td>
<td>Usare <em>Rete</em>. <strong>recoveredPackets</strong>.</td>
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
<td>Usare <em>Media</em>. <strong>duration</strong> per determinare la lunghezza di un <strong>oggetto Media.</strong> Usare un marcatore con <em>i controlli</em>. <strong>currentMarker per</strong> specificare una posizione finale personalizzata.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SelectionStart</strong></td>
<td>Usare <em>i controlli</em>. <strong>currentPosition per</strong> avviare la riproduzione da una posizione specifica o usare un marcatore con <em>Controls</em>. <strong>currentMarker per</strong> specificare una posizione iniziale personalizzata.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendErrorEvents</strong></td>
<td>Gli errori vengono accodati. Usare <strong>l'oggetto Error</strong> e <strong>l'oggetto ErrorItem</strong> per recuperare le informazioni sull'errore.</td>
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
<td>Non disponibile. È possibile fornire controlli personalizzati o usare <em>Player</em>. <strong>uimode</strong> per scegliere una configurazione predefinita.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowCaptioning</strong></td>
<td>Non disponibile. È possibile fornire una visualizzazione di sottotitoli codificati personalizzata.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowControls</strong></td>
<td>Non disponibile. È possibile fornire controlli personalizzati o usare <em>Player</em>. <strong>uimode</strong> per scegliere una configurazione predefinita.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDisplay</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowGotoBar</strong></td>
<td>Non disponibile. È possibile fornire funzionalità personalizzate usando l'oggetto Media</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowPositionControls</strong></td>
<td>Non disponibile. È possibile fornire controlli personalizzati o usare <em>Player</em>. <strong>uimode</strong> per scegliere una configurazione predefinita.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowStatusBar</strong></td>
<td>Non disponibile. È possibile fornire controlli personalizzati o usare <em>Player</em>. <strong>uimode</strong> per scegliere una configurazione predefinita.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowTracker</strong></td>
<td>Non disponibile. È possibile fornire controlli personalizzati o usare <em>Player</em>. <strong>uimode</strong> per scegliere una configurazione predefinita.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SourceLink</strong></td>
<td>Usare <em>Media</em>. <strong>sourceURL</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SourceProtocol</strong></td>
<td>Usare <em>Rete</em>. <strong>sourceProtocol</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamCount</strong></td>
<td>Non disponibile. Usare <em>i controlli</em>. <strong>audioLanguageCount per</strong> recuperare il numero di flussi della lingua audio.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SottopictureOn</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SubpictureStreamsAvailable</strong></td>
<td>Non disponibile</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TitlesAvailable</strong></td>
<td>Usare quanto segue:<code>Player.Cdrom.playlist.count - 1</code><br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TotalTitleTime</strong></td>
<td>Usare <em>currentMedia</em>. <strong>duration</strong> o <em>currentMedia</em>. <strong>durationString</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TransparentAtStart</strong></td>
<td>Usare lo script per specificare i valori di altezza e larghezza per rendere visibile o invisibile il lettore.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>UniqueID</strong></td>
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
<td><em>Player6</em>. <strong>Volume</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>Volume</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VolumiDisponibili</strong></td>
<td>Non disponibile.</td>
</tr>
</tbody>
</table>



 

Nella tabella seguente vengono confrontati i Windows Media Player del modello a oggetti della versione 6.4 con il modello a oggetti Windows Media Player 7 o versione successiva.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Windows Media Player 6.4</th>
<th>Windows Media Player 7 o versione successiva equivalente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AboutBox</strong></td>
<td>Usare <em>Player</em>. <strong>versionInfo</strong> per recuperare la versione di Windows Media Player.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BackwardScan</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>rate</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PulsanteAttiva</strong></td>
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
<td>Se la playlist del titolo specificata è già in riproduzione, recuperare il capitolo desiderato come oggetto multimediale usando la sintassi seguente:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Specificare quindi <em>Player</em>. <strong>currentMedia con</strong> l'oggetto multimediale restituito.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChapterPlayAutoStop</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChapterSearch</strong></td>
<td>Se la playlist del titolo specificata è già in riproduzione, recuperare il capitolo desiderato come oggetto multimediale usando la sintassi seguente:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Specificare quindi <em>Player</em>. <strong>currentMedia con</strong> l'oggetto multimediale restituito.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>FastForward</strong></td>
<td>Usare <em>i controlli</em>. <strong>fastForward</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FastReverse</strong></td>
<td>Usare <em>i controlli</em>. <strong>fastReverse</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ForwardScan</strong></td>
<td>Usare <em>Impostazioni</em>. <strong>rate</strong>.</td>
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
<td>Usare <em>i controlli</em>. <strong>currentAudioLanguage</strong> per recuperare l'LCID della lingua audio corrente.</td>
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
<td>Usare lo script per scorrere la playlist corrente. Usare <em>l'oggetto multimediale</em>. <strong>isIdentical per</strong> confrontare ogni voce nella playlist con <em>player.</em> <strong>Oggetto currentMedia.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMarkerName</strong></td>
<td>Usare <em>l'oggetto multimediale</em>. <strong>getMarkerName</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMarkerTime</strong></td>
<td>Usare <em>l'oggetto multimediale</em>. <strong>getMarkerTime</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaInfoString</strong></td>
<td>Usare <em>l'oggetto multimediale</em>. <strong>getItemInfo</strong>, <em>Media</em>. <strong>getItemInfoByAtom</strong>e i relativi metodi associati per recuperare i metadati.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMediaParameter</strong></td>
<td>Usare <em>playlist</em>. <strong>elemento</strong> per recuperare un elemento multimediale. Usare quindi <em>Media</em>. <strong>getItemInfo per</strong> recuperare la stringa del parametro.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaParameterName</strong></td>
<td>Usare <em>playlist</em>. <strong>elemento</strong> per recuperare un elemento multimediale. Usare quindi <em>Media</em>. <strong>getAttributeName per</strong> recuperare la stringa del parametro.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMoreInfoURL</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetNumberOfChapters</strong></td>
<td>Se è in corso la riproduzione di un titolo, <em>usare currentPlaylist.</em> <strong>count</strong>.</td>
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
<td><em>Player6</em>. <strong>GoUp</strong></td>
<td>Usare <em>DVD</em>. <strong>torna a</strong>.</td>
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
<td><em>Player6</em>. <strong>Chiamata di menu</strong></td>
<td>Usare <em>DVD</em>. <strong>titleMenu</strong> o <em>DVD.</em> <strong>topMenu</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Avanti</strong></td>
<td>Usare <em>i controlli</em>. <strong>next</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>NextPGSearch</strong></td>
<td>Usare <em>i controlli</em>. <strong>next</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Apri</strong></td>
<td>Usare <em>Player</em>. <strong>URL o</strong> <em>Player</em>. <strong>currentMedia.</strong> I file vengono sempre aperti in modo asincrono.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Sospendi</strong></td>
<td>Usare <em>i controlli</em>. <strong>sospendere</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Riproduci</strong></td>
<td>Usare <em>i controlli</em>. <strong>riprodurre</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Precedente</strong></td>
<td>Usare <em>i controlli</em>. <strong>precedente.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PrevPGSearch</strong></td>
<td>Usare <em>i controlli</em>. <strong>precedente.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ResumeFromMenu</strong></td>
<td>Usare <em>DVD</em>. <strong>riprendere</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>RightButtonSelect</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SetCurrentEntry</strong></td>
<td>Recuperare un oggetto multimediale usando <em>currentPlaylist.</em> <strong>item</strong>(<em>entryNumber</em>). Specificare quindi l'oggetto multimediale recuperato usando <em>Controls.</em> <strong>currentItem</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDialog</strong></td>
<td>Non disponibile.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StillOff</strong></td>
<td>Usare <em>i controlli</em>. <strong>riprodurre</strong>. In alternativa, usare <em>Controls.</em> <strong>Avanti</strong> se la modalità è ancora attiva.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Arresta</strong></td>
<td>Usare <em>i controlli</em>. <strong>arrestare</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamSelect</strong></td>
<td>Non disponibile. Usare <em>i controlli</em>. <strong>currentAudioLanguage</strong> per specificare un flusso della lingua audio.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TimePlay</strong></td>
<td>Dalla playlist radice usare <em>currentPlaylist</em>. <strong>item</strong>(<em>index</em>) per recuperare un oggetto multimediale. Impostare quindi l'oggetto multimediale come corrente usando <em>Controls</em>. <strong>currentItem</strong>. Specificare quindi <em>Controls</em>. <strong>currentPosition</strong> usando un valore di tempo in secondi.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TimeSearch</strong></td>
<td>Usare <em>i controlli</em>. <strong>currentPosition</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TitlePlay</strong></td>
<td>Se si sta già riproducendo la playlist del titolo specificata, recuperare il capitolo desiderato come oggetto multimediale usando la sintassi seguente:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Specificare quindi <em>Player</em>. <strong>currentMedia usando</strong> l'oggetto multimediale restituito.<br/> In alternativa, usare <em>currentPlaylist</em>. <strong>elemento</strong> per recuperare un oggetto multimediale e quindi usare l'oggetto multimediale restituito per specificare <em>Controls</em>. <strong>currentItem</strong>.<br/></td>
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



 

Nella tabella seguente vengono confrontati gli Windows Media Player del modello a oggetti della versione 6.4 con il modello a oggetti Windows Media Player 7 o versione successiva.



| Windows Media Player 6.4  | Windows Media Player 7 o versione successiva equivalente                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Player6*. **Memorizzazione nel buffer**         | Usare *Player*. **Memorizzazione nel buffer di**.                                                                                                                                                                                              |
| *Player6*. **Fare clic su**             | Usare *Player*. **Fare clic su**                                                                                                                                                                                                   |
| *Player6*. **DblClick**          | Usare *Player*. **DoubleClick**                                                                                                                                                                                             |
| *Player6*. **Disconnetti**        | Non disponibile.                                                                                                                                                                                                           |
| *Player6*. **DisplayModeChange** | Non disponibile.                                                                                                                                                                                                           |
| *Player6*. **DVDNotify**         | *Lettore*. **DomainChange** e *Player*. **OpenPlaylistSwitch sono** eventi specifici di DVD. A seconda dell'applicazione, possono essere applicati anche altri eventi correlati a playlist, supporti multimediali e supporti CD-ROM.                        |
| *Player6*. **EndOfStream**       | Usare *Player*. **PlayState**.                                                                                                                                                                                              |
| *Player6*. **Errore**             | L'evento rimane invariato. Gli errori, tuttavia, vengono accodati. Usare **l'oggetto Error** con **l'oggetto ErrorItem** per recuperare le informazioni sull'errore dalla coda. Vedere il codice di esempio nella sezione precedente, Gestione degli errori. |
| *Player6*. **KeyDown**           | Usare *Player*. **Keydown**                                                                                                                                                                                                 |
| *Player6*. **KeyPress**          | Usare *Player*. **KeyPress**                                                                                                                                                                                                |
| *Player6*. **KeyUp**             | Usare *Player*. **KeyUp**                                                                                                                                                                                                   |
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
| *Player6*. **Avviso**           | Non disponibile.                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla migrazione del modello a oggetti**](object-model-migration-guide.md)
</dt> <dt>

[**Informazioni di riferimento sul modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





