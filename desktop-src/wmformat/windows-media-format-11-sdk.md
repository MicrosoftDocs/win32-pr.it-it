---
title: SDK di Windows Media Format 11
description: SDK di Windows Media Format 11
ms.assetid: 875e8914-b861-46f1-9391-8724ff77d26b
keywords:
- Windows Media Format SDK, informazioni
- Windows Media SDK
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Formato Advanced Systems (ASF), informazioni
- ASF (Advanced Systems Format), informazioni
- Windows Media Format SDK, funzionalità
- Windows Media Format SDK, funzionalità principali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363c268194b476b6d3326a9c57fe1e709d17e2fe
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104474549"
---
# <a name="windows-media-format-11-sdk"></a>SDK di Windows Media Format 11

In questa documentazione viene descritto il Software Development Kit (SDK) di Microsoft Windows Media Format e si applica alle versioni di SDK basate su 32 bit e x64.

Windows Media Format SDK è un componente di Microsoft Windows Media Software Development Kit (SDK). Altri componenti includono Windows Media Services SDK, Windows Media Encoder SDK, Windows Media Rights Manager SDK, Windows Media Gestione dispositivi SDK e Windows Media Player SDK.

Windows Media Format SDK consente agli sviluppatori di applicazioni di accedere ai componenti del formato Windows Media. Questi componenti includono il contenitore di file ASF (Advanced Systems Format), i codec Windows Media Audio e video, la funzionalità di streaming di rete di base e la Digital Rights Management. Gli oggetti di Windows Media Format SDK modificano i componenti di Windows Media a un livello basso. gli altri componenti di Windows Media SDK includono oggetti che funzionano a un livello superiore.

Lo scopo principale di Windows Media Format SDK è quello di consentire agli sviluppatori di creare applicazioni in grado di riprodurre, scrivere, modificare, crittografare e distribuire file ASF (Advanced Systems Format) e flussi di rete. Questi file e flussi contengono in genere contenuti audio e video codificati con i codec Windows Media Audio e video. Tuttavia, ASF può contenere qualsiasi tipo di dati. Per ulteriori informazioni sulla struttura del contenitore del formato Advanced Systems, vedere [Panoramica del formato ASF](overview-of-the-asf-format.md).

Le funzionalità principali di Windows Media Format SDK sono:

-   Supporto per i codec leader del settore. Windows Media Format 11 SDK include il codec Microsoft Windows Media Video 9 e il codec Microsoft Windows Media Audio 9,1. Entrambi questi codec forniscono una codifica eccezionale del contenuto multimediale digitale. Una novità di questa versione è il codec del profilo avanzato Windows Media Video 9, che fornisce le ottimizzazioni per la trasmissione di video. Questo SDK include anche il codec dello schermo Microsoft Windows Media Video 9 per comprimere l'attività dello schermo del computer durante le sessioni di applicazioni utente e il codec Windows Media Audio Voice 9,1, che codifica audio di bassa complessità come la sintesi vocale e si adatta in modo intelligente a audio più complessi, ad esempio la musica, per una rappresentazione superiore di scenari di musica vocale combinati.
-   Supporto per la scrittura di file ASF. I file vengono creati in base ai profili personalizzabili, semplificando la configurazione e la standardizzazione dei file. Questo SDK può essere usato per scrivere file in eccesso di 2 gigabyte, abilitando file continui più lunghi, di qualità superiore.
-   Supporto per la lettura dei file ASF. Questo SDK fornisce supporto per la lettura dei file ASF locali, nonché per la lettura di dati ASF trasmessi in una rete. Viene inoltre fornito il supporto per molte funzionalità di lettura avanzate, ad esempio il supporto nativo per i file con velocità in bit multipla (MBR), che contengono più flussi con lo stesso contenuto codificato a velocità in bit diverse. Il Reader seleziona automaticamente il flusso MBR da usare, a seconda della larghezza di banda disponibile al momento della riproduzione.
-   Supporto per la distribuzione di flussi ASF in una rete. Questo SDK fornisce supporto per la distribuzione di dati ASF tramite HTTP a computer remoti in una rete e anche per il recapito di dati direttamente a un server Windows Media remoto.
-   Supporto per la modifica dei metadati nei file ASF. Le informazioni su un file e sul relativo contenuto sono facilmente manipolabili con questo SDK. Gli sviluppatori possono utilizzare il solido sistema degli attributi dei metadati inclusi nell'SDK oppure creare attributi personalizzati in base alle proprie esigenze.
-   Supporto per le applicazioni di modifica del contenuto. Questo SDK consente alle applicazioni di cercare punti all'interno di un file in base all'ora di presentazione e al frame video. Inoltre, i file creati usando Windows Media Format SDK possono mantenere i timestamp nei formati usati per la produzione di film e televisione.
-   Supporto per la lettura e la modifica di metadati in file MP3. Questo SDK fornisce il supporto integrato per la lettura dei file MP3 con gli stessi metodi usati per leggere i file ASF. Le applicazioni compilate con Windows Media Format SDK possono anche modificare gli attributi dei metadati nei file MP3 usando il supporto incorporato per i tag ID3 più comuni usati dagli autori di contenuti.
-   Supporto per la protezione Rights Management digitale. Questo SDK fornisce metodi per la lettura e la scrittura di file ASF e flussi di rete protetti da Rights Management digitali per impedire la riproduzione o la copia del contenuto non autorizzati.

Per scaricare Windows Media Format SDK, vedere la pagina di [download di Windows Media](https://msdn.microsoft.com/windows/desktop/aa904949) nel sito Web Microsoft.

In questo documento viene descritto come sviluppare applicazioni multimediali digitali utilizzando Windows Media Format SDK. È divisa nelle sezioni seguenti.

> [!Note]  
> Sebbene in questo documento siano contenute informazioni sulla versione più recente di Windows Media Format SDK, la maggior parte delle funzionalità descritte è supportata dalle versioni precedenti dell'SDK. Le pagine di riferimento per metodi, funzioni, strutture ed enumerazioni di Windows Media Format SDK includono i requisiti di versione.

 



| Sezione                                                                                                          | Descrizione                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni su Windows Media Format SDK](about-the-windows-media-format-sdk.md)                                     | Vengono fornite informazioni generali e informazioni di base che è necessario conoscere prima di tentare di creare applicazioni.                                                                                  |
| [Guida per programmatori](programming-guide.md)                                                                       | Vengono fornite istruzioni dettagliate per l'esecuzione di varie attività, ad esempio la lettura, la scrittura e l'indicizzazione di file, la protezione di file con Rights Management digitali, il flusso di dati ASF in rete e così via. |
| [Guida di riferimento alla programmazione](programming-reference.md)                                                               | Fornisce informazioni di riferimento per le interfacce, i metodi, le funzioni, le strutture, i tipi di enumerazione e le costanti correlate al formato Windows Media.                                                     |
| [Interfacce di Windows Media Audio e codec video](windows-media-audio-and-video-codec-interfaces--deprecated.md) | Vengono fornite istruzioni per l'uso diretto di Windows Media Audio e video codec Digital Media Objects (DMOs).                                                                                           |
| [*Glossario*](wmformat-glossary.md)                                                                              | Definisce i termini usati nella documentazione di Windows Media Format SDK.                                                                                                                                    |



 

 

 




