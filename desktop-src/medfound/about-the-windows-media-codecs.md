---
description: Informazioni sui codec Windows Media
ms.assetid: C0B0265C-AD20-433B-A554-112AEB0208B9
title: Informazioni sui codec Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2240176de22682451814609abc94f33a52300563
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234496"
---
# <a name="about-the-windows-media-codecs"></a>Informazioni sui codec Windows Media

-   [Codec Windows Media Audio](#windows-media-audio-codecs)
    -   [Windows Media Audio 9](#windows-media-audio-9)
    -   [Windows Media Audio 10 Professional](#windows-media-audio-10-professional)
    -   [Windows Media Audio 9 senza perdita di perdite](#windows-media-audio-9-lossless)
    -   [Windows Media Audio 9 Voice](#windows-media-audio-9-voice)
    -   [Compatibilità](#compatibility)
-   [Codec serie Windows Media Video 9](#windows-media-video-9-series-codecs)
    -   [Windows Media Video 9](#windows-media-video-9-series-codecs)
    -   [Schermata Windows Media Video 9](#windows-media-video-9-screen)
    -   [Windows Media Video 9 Image versione 2](#windows-media-video-9-image-version-2)
    -   [Windows Media Video 9 VCM](#windows-media-video-9-vcm)
    -   [Compatibilità](#compatibility)
-   [Argomenti correlati](#related-topics)

## <a name="windows-media-audio-codecs"></a>Codec Windows Media Audio

### <a name="windows-media-audio-9"></a>Windows Media Audio 9

Questo codec esegue il campionamento audio a 44,1 o 48 kilohertz (kHz) con 16 bit, in modo analogo allo standard CD corrente, che offre la qualità del CD alle velocità dati da 64 a 192 kilobit al secondo (Kbps). La qualità del suono risultante è migliore del 20% rispetto all'audio campionato con Windows Media Audio 8 a frequenze dati equivalenti.

Il codec Windows Media Audio 9 (WMA 9) supporta la codifica della velocità in bit variabile (VBR), che consente un audio anche di qualità superiore a dimensioni di file più piccole, variando automaticamente la velocità in bit della codifica in base alla complessità dei dati audio. Con VBR, la velocità in bit di codifica aumenta per acquisire sezioni complesse di dati e quindi diminuisce per massimizzare la compressione delle sezioni meno complesse, producendo una compressione compatta e di alta qualità.

WMA 9 è compatibile con le versioni precedenti con i decodificatori precedenti compatibili con Windows Media Audio, il che significa che è possibile riprodurre il contenuto WMA 9 con le versioni precedenti di Windows Media Player o dispositivi elettronici di consumo meno recenti che supportano Windows Media. Come per tutti i codec della serie Windows Media 9, supporta la piattaforma Windows Media Digital Rights Management, che consente di creare in modo sicuro il pacchetto e la distribuzione di supporti digitali protetti da copia.

### <a name="windows-media-audio-10-professional"></a>Windows Media Audio 10 Professional

Windows Media Audio 10 Professional (WMA 10 Pro) è il codec audio Windows Media più flessibile disponibile, ovvero i profili di supporto che includono tutti gli elementi, dall'audio a 24 bit/96 kHz a risoluzione completa in stereo, dal canale 5,1 o anche dal suono surround del canale 7,1, alle funzionalità per dispositivi mobili estremamente efficienti a 24 kbps 128 e 96 kbps per il suono del canale 256. WMA 10 Pro offre una straordinaria qualità per i consumer che usano computer con hardware ad alta fedeltà e computer dotati di un canale di 5,1 e che consentono ai consumer di riprodurre contenuti audio nei propri dispositivi mobili. WMA 10 Pro supporta lo streaming, il download progressivo o la distribuzione di download e riproduzione a 128 a 768 kbps.

Quando si usa 5,1 audio surround compresso a 384 kbps con WMA 10 Pro, la maggior parte dei listener non riesce a discernere le differenze tra la musica compressa e i file di Pulse Code Modulation (PCM) originali. WMA Pro offre anche il controllo dinamico degli intervalli usando le ampiezze massime e medie dell'audio calcolate durante il processo di codifica. Utilizzando la funzionalità modalità non interattiva di Windows Media Player 9 e versioni successive, gli utenti possono udire l'intervallo dinamico completo, un intervallo di differenza medio fino a 12 decibel (dB) superiore alla media o una piccola differenza fino a 6 dB sopra la media.

Se un utente tenta di riprodurre un file codificato con il canale 5,1, funzionalità di campionamento di 96 kHz a 24 bit, ma non dispone di un sistema o di una scheda audio che supporta il suono multicanale o ad alta risoluzione, più canali vengono combinati in audio stereo (ad esempio, 16 bit, audio a due canali), assicurando che gli utenti ottengano la migliore esperienza di riproduzione dei propri sistemi.

Nella tabella seguente viene confrontato WMA Pro con la tecnologia di compressione concorrente.



| Dati audio              | Compressione del settore\*        | Windows Media\*            | Risparmio di compressione |
|-------------------------|-------------------------------|----------------------------|---------------------|
| 2 ch x 48 kHz x 16 bit | Dolby Digital 2,0 a 220 kbps | WMA 10 Pro a 128 kbps     | 1.7:1               |
| 6 ch x 48 kHz x 20 bit | Dolby Digital 5,1 a 384 kbps | WMA 10 Pro a 192-256 kbps | 1.5 – 2:1             |
| 6 ch x 48 kHz x 24 bit | DTS 5,1 a 1.536 Kbps         | WMA 10 Pro a 768 kbps     | 2:1                 |



 

\* Dipendente dal contenuto

### <a name="windows-media-audio-9-lossless"></a>Windows Media Audio 9 senza perdita di perdite

La qualità audio del contenuto compresso usando questo codec è il meglio di tutti i codec Windows Media Audio. Viene creato un duplicato bit per bit del file audio originale, in modo che non vengano persi dati, il che lo rende ideale per l'archiviazione di Master contenuto.

A seconda della complessità dell'originale, il contenuto verrà compresso con un rapporto 2:1 o 3:1. Sebbene questo sia inferiore rispetto al rapporto con altri codec serie Windows Media Audio 9, offre gli stessi vantaggi della compressione lasciando intatti i dati.

Come Windows Media Audio 9 Professional, il codec Windows Media Audio 9 Lossless offre anche il controllo dinamico degli intervalli usando le ampiezze audio massime e medie calcolate durante il processo di codifica. Utilizzando la funzionalità modalità non interattiva di Windows Media Player 9 e versioni successive, gli utenti possono udire l'intervallo dinamico completo, un intervallo di differenza medio fino a 12 dB al di sopra della media o una piccola differenza fino a 6 dB sopra la media.

### <a name="windows-media-audio-9-voice"></a>Windows Media Audio 9 Voice

Questo codec a bassa velocità è destinato principalmente al contenuto vocale, ma funziona molto bene con contenuto in modalità mista che include voce e musica. In modalità voce, il codec sfrutta i vantaggi dell'intervallo di frequenza relativamente meno complesso e più piccolo della voce umana per ottimizzare la compressione. In modalità musica il codec funziona come il codec standard Windows Media Audio 9. Il contenuto codificato può essere configurato in modo da passare automaticamente dalla modalità voce alla musica e viceversa.

Il codec Windows Media Audio 9 Voice offre qualità superiore per gli scenari di streaming a bassa velocità (meno di 20 Kbps), ad esempio trasmissioni radiofoniche, pubblicità, e-book, podcast e VoiceOver. Il codec vocale può anche comprimere il contenuto a un minimo di 4 kbps a 8 kHz.

### <a name="compatibility"></a>Compatibilità

Nella tabella seguente vengono illustrati i vantaggi che si verificano durante la riproduzione del contenuto della serie Windows Media Audio 9 nei precedenti sistemi operativi Microsoft Windows rispetto a Windows XP o con versioni precedenti di Windows Media Player. Questa tabella elenca inoltre la compatibilità per le piattaforme Apple Mac OS X e basate su Windows CE.



| Codec                              | Funzionalità                                       | Compatibilità con le versioni precedenti del lettore                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Audio 9              | Codifica della velocità in bit costante (CBR)              | <dl> Windows <dt>Media Player 6,4 o versioni successive su dispositivi non portabili (usando la transcodifica necessaria)</dt> <dt>Windows Media Player 9 per Mac OS X</dt> <dt>Windows Media Player 9 Series e Windows Media Player 9,1 per Pocket \* PC</dt> <dt>Windows Media Player 9 Series e Windows Media Player 9,1 per \* smartphone</dt> </dl> |
|                                    | Codifica con velocità in bit (VBR) variabile              | Windows Media Player 7 o versione successiva su tutti i dispositivi che supportano il lettore (usando la transcodifica in base alle esigenze)                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Media Audio 9 Professional | Generale                                       | <dl> Windows <dt>Media Player 7 o versioni successive</dt> <dt>Media Player 9 per Mac OS X</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | Riproduzione del canale discreto (ad esempio, 5,1) | Richiede Windows Media Player 9 Series (o SDK) o versioni successive, Windows XP e una scheda audio multicanale.                                                                                                                                                                                                                                                                                                                                                                                                                         |
|                                    | Audio ad alta risoluzione (24 bit, 96 kHz)        | Richiede Windows Media Player 9 Series (o SDK) o versioni successive, Windows XP e una scheda audio ad alta risoluzione.                                                                                                                                                                                                                                                                                                                                                                                                                      |
|                                    | Controllo intervallo dinamico                         | Richiede Windows Media Player 9 Series (o SDK) o versioni successive e Windows XP.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Windows Media Audio 9 senza perdita di perdite     | Generale                                       | <dl> Windows <dt>Media Player 7 o versioni successive</dt> <dt>Media Player 9 per Mac OS X</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | Riproduzione del canale discreto (ad esempio, 5,1) | Richiede Windows Media Player 9 Series (o SDK) o versioni successive, Windows XP e una scheda audio multicanale.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Media Audio 9 Voice        | Generale                                       | <dl> Windows <dt>Media Player 6,4 o versioni successive</dt> <dt>Windows Media Player 9 per Mac OS X</dt> <dt>Windows Media Player 9 serie e Windows Media Player 9,1 per Pocket \* PC</dt> <dt>Windows Media Player 9 Series e Windows Media Player 9,1 per \* smartphone</dt> </dl>                                                       |



 

> [!Note]  
> \* Tutte le versioni di Windows Media Player per Pocket PC e smartphone vengono fornite come parte del sistema operativo Microsoft Windows Mobile. Windows Media Player per Pocket PC e Windows Media Player per smartphone non sono disponibili per il download da Microsoft.

 

## <a name="windows-media-video-9-series-codecs"></a>Codec serie Windows Media Video 9

In 2006, la società di Motion Picture and Television Engineers (SMPTE) ha pubblicato formalmente la specifica finale per SMPTE 421M, nota anche come VC-1. La standardizzazione formale di VC-1 rappresenta il culmine di anni di esame tecnico di più di 75 società, che ha portato a un codec ben documentato, estremamente stabile, facilmente concesso in licenza e accettato dal settore. VC-1 supporta tre profili: Simple, Main e Advanced. I profili semplice e principale sono stati completati per diversi anni e le implementazioni esistenti, ad esempio WMV 9, hanno supportato a lungo la creazione e la riproduzione di contenuti usando questi profili, oltre a un'implementazione anticipata del profilo avanzato. Il completamento del profilo avanzato e la conseguente standardizzazione di tutti i profili in VC-1 rappresenta il passaggio finale di una specifica completa che offre contenuto a definizione elevata, interlacciato o progressivo, su qualsiasi supporto e su qualsiasi dispositivo idoneo.

### <a name="windows-media-video-9"></a>Windows Media Video 9

Windows Media Video 9 è l'implementazione Microsoft dello standard SMPTE VC-1. Supporta i profili semplici, principali e avanzati.

### <a name="simple-and-main-profiles"></a>Profili semplici e principali

I profili semplici e principali Windows Media Video 9 sono completamente conformi allo standard SMPTE VC-1 e offrono video di alta qualità per lo streaming e il download. Questi profili supportano un'ampia gamma di velocità in bit, dal contenuto ad alta definizione a una metà a un terzo della velocità in bit di MPEG-2, al video Internet a bassa velocità in bit distribuito tramite un modem remoto. Questo codec supporta anche video di qualità professionale scaricabile con codifica con velocità in bit doppia e velocità in bit variabile (VBR). Windows Media Video 9 è già supportata da un'ampia gamma di lettori e dispositivi.

### <a name="advanced-profile"></a>Profilo avanzato

Il profilo avanzato Windows Media Video 9 è completamente conforme allo standard SMPTE VC-1, supporta il contenuto interlacciato ed è indipendente dal trasporto. I creatori di contenuti possono usare questo profilo per distribuire contenuti progressivi o interlacciati a frequenze dati come minimo un terzo del codec MPEG-2, con la stessa qualità di MPEG-2.

In passato, il contenuto video interlacciato veniva sempre deinterlacciato prima della codifica con il codec Windows Media Video. A questo punto, le applicazioni di codifica quali Windows Media 9 e le soluzioni di codifica di terze parti possono supportare la compressione dei contenuti interlacciati senza prima convertirli in contenuti progressivi. La gestione dell'interlacciamento in un file codificato è importante se il rendering del contenuto viene eseguito su una visualizzazione interlacciata, ad esempio un televisore.

L'indipendenza del trasporto consente inoltre la distribuzione di Windows Media Video 9 profilo avanzato su sistemi che non sono basati su Windows Media, ad esempio infrastrutture di broadcast basate su standard (tramite flussi di trasporto MPEG-2 nativi), infrastrutture wireless (usando il protocollo di trasferimento in tempo reale \[ RTP \] ) o persino DVD.

Nella tabella seguente viene confrontato Windows Media Video 9 profilo avanzato alla tecnologia di compressione concorrente.



| Dati video                                                  | Compressione del settore\* | Windows Media\*                                      | Risparmio di compressione |
|-------------------------------------------------------------|------------------------|------------------------------------------------------|---------------------|
| 480/24p 720x480 pixel/frame x 8 bit per canale x 24 fps  | MPEG-2 a 4 – 6 Mbps     | Profilo avanzato Windows Media Video 9 a 1.3 – 2 Mbps | 3:1                 |
| 480/30i 720x480 pixel/frame x 8 bit per canale x 30 fps  | MPEG-2 a 6-8 Mbps     | Windows Media Video 9 profilo avanzato a 2-4 Mbps   | 2-3:1               |
| 720/24p 1280x720 pixel/frame x 8 bit per canale x 24 fps | MPEG-2 a 19 Mbps      | Windows Media Video 9 profilo avanzato a 5-8 Mbps   | 2.4 – 3.8:1           |



 

\*Dipendente dal contenuto

### <a name="windows-media-video-9-screen"></a>Schermata Windows Media Video 9

Il codec Windows Media Video 9 screen è ottimizzato per comprimere schermate sequenziali e video altamente statici acquisiti dallo schermo del computer, che lo rende ideale per la distribuzione di demo o per la dimostrazione dell'uso del computer per il training. Il codec sfrutta i vantaggi della tipica semplicità dell'immagine e della mancanza di movimento relativa per ottenere un rapporto di compressione molto elevato.

Durante il processo di codifica, il codec passa automaticamente tra le modalità di codifica con perdita di dati e senza perdita di dati, a seconda della complessità dei dati video. Per i dati complessi, la modalità senza perdita di dati conserva una copia esatta dei dati. Per i dati meno complessi, la modalità con perdita di dati Elimina alcuni dati per ottenere un rapporto di compressione più elevato. Passando automaticamente da una modalità all'altra, il codec mantiene la qualità del video e massimizza la compressione.

Nel complesso, il codec Windows Media Video 9 screen offre una gestione migliore delle immagini bitmap e del movimento dello schermo, anche in CPU relativamente modeste. È anche fino a 100 volte più efficiente rispetto alla codifica di lunghezza di esecuzione di uso comune.

### <a name="windows-media-video-9-image-version-2"></a>Windows Media Video 9 Image versione 2

Il codec Windows Media Video 9 Image versione 2 è diverso da quello degli altri codec video. Anziché elaborare video non compressi, trasforma le immagini ancora in video usando le transizioni Pan, zoom e dissolvenza incrociata tra le clip per creare un numero illimitato di effetti.

I risultati possono quindi essere recapitati a velocità dati fino a 20 kilobit al secondo (Kbps). Questi file vengono compressi usando la velocità in bit costante (CBR) o la modalità di velocità in bit variabile (VBR) a una sola sessione.

> [!Note]  
> Il codec Windows Media Video 9 Image versione 2 non è compatibile con il codec di immagine Windows Media Video 9.

 

### <a name="windows-media-video-9-vcm"></a>Windows Media Video 9 VCM

La versione di video Compression Manager (VCM) del codec della serie Windows Media Video 9 consente le versioni precedenti delle applicazioni di codifica e modifica per supportare il codec della serie Windows Media Video 9 nei contenitori di file, ad esempio Audio Video Interleaved (AVI). Questo pacchetto di codec consente inoltre di riprodurre i file di Windows Media Video (WMV) basati su Windows Media Format 9 in Windows Media Player 6,4, sia in contenitori di file ASF che AVI.

### <a name="compatibility"></a>Compatibilità

Nella tabella seguente vengono illustrati i vantaggi che si verificano durante la riproduzione del contenuto della serie Windows Media Video 9 nei precedenti sistemi operativi Microsoft Windows o nelle versioni precedenti di Windows Media Player. Questa tabella elenca inoltre la compatibilità per le piattaforme Apple Mac OS X e basate su Windows CE.



| Codec                                  | Funzionalità             | Compatibilità con le versioni precedenti del lettore                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Video 9                  | Generale             | <dl> Windows <dt>Media Player 6,4 o versioni successive</dt> <dt>Windows Media Player 9 per Mac OS X</dt> <dt>Windows Media Player 9 serie e Windows Media Player 9,1 per Pocket \* PC</dt> <dt>Windows Media Player 9 Series e Windows Media Player 9,1 per \* smartphone</dt> </dl> |
|                                        | Interpolazione frame | Richiede Windows Media Player 9 Series (o Software Development Kit) o versioni successive e Windows XP.                                                                                                                                                                                                                                                                                                                                                                           |
| Profilo avanzato Windows Media Video 9 | Generale             | Windows Media Player 7 o versione successiva                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Schermata Windows Media Video 9           | Generale             | Windows Media Player 7 o versione successiva                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Media Video 9 Image versione 2  | Generale             | Windows Media Player 7 o versione successiva                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

> [!Note]  
> \*Tutte le versioni di Windows Media Player per Pocket PC e smartphone vengono fornite come parte del sistema operativo Microsoft Windows Mobile. Windows Media Player per Pocket PC e Windows Media Player per smartphone non sono disponibili per il download da Microsoft.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



