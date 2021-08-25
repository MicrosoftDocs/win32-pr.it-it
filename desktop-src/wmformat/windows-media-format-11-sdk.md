---
title: Windows Media Format 11 SDK
description: Windows Media Format 11 SDK
ms.assetid: 875e8914-b861-46f1-9391-8724ff77d26b
keywords:
- Windows Media Format SDK, informazioni su
- Windows Media SDK
- Windows Media Format SDK,Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), about
- ASF (Advanced Systems Format),about
- Windows Media Format SDK, funzionalità
- Windows Media Format SDK, funzionalità chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70af68402ea5a22a9499ca09fd4b2e4022f304ee5ebf68a4f877a978ad168e4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839431"
---
# <a name="windows-media-format-11-sdk"></a>Windows Media Format 11 SDK

Questa documentazione descrive Microsoft Windows Media Format Software Development Kit (SDK) e si applica alle versioni a 32 bit e basate su x64 dell'SDK.

L Windows Media Format SDK è un componente di Microsoft Windows Media Software Development Kit (SDK). Altri componenti includono Servizi Windows Media SDK, Windows Media Encoder SDK, Windows Media Rights Manager SDK, Windows Media Device Manager SDK e Windows Media Player SDK.

L Windows Media Format SDK fornisce agli sviluppatori di applicazioni l'accesso ai componenti di Windows Media Format. Questi componenti includono il contenitore di file ASF (Advanced Systems Format), i codec audio e video Windows Media, la funzionalità di streaming di rete di base e la gestione dei diritti digitali. Gli oggetti dell'SDK Windows Media Format modificano i componenti di Windows Media a un livello basso; Gli altri componenti di Windows Media SDK includono oggetti che funzionano a un livello superiore.

Lo scopo principale di Windows Media Format SDK è consentire agli sviluppatori di creare applicazioni che consentono di riprodurre, scrivere, modificare, crittografare e distribuire file ASF (Advanced Systems Format) e flussi di rete. Questi file e flussi contengono in genere contenuti audio e video codificati Windows codec audio e video multimediali. Tuttavia, ASF può contenere qualsiasi tipo di dati. Per altre informazioni sulla struttura del contenitore Advanced Systems Format, vedere [Panoramica del formato ASF.](overview-of-the-asf-format.md)

Le funzionalità principali di Windows Media Format SDK sono:

-   Supporto per codec leader del settore. L Windows Media Format 11 SDK include il codec Microsoft Windows Media Video 9 e il codec Microsoft Windows Media Audio 9.1. Entrambi questi codec forniscono una codifica eccezionale del contenuto multimediale digitale. Novità di questa versione è il codec Windows Media Video 9 Advanced Profile, che offre ottimizzazioni per la trasmissione di video. Questo SDK include anche il codec dello schermo Microsoft Windows Media Video 9 per comprimere l'attività dello schermo del computer durante le sessioni di applicazioni utente e il codec voce Windows Media Audio 9.1, che codifica audio a bassa complessità, ad esempio voce e si adatta in modo intelligente ad audio più complesso, ad esempio musica, per una rappresentazione superiore degli scenari combinati di musica vocale.
-   Supporto per la scrittura di file ASF. I file vengono creati in base a profili personalizzabili, semplificando la configurazione e la standardizzazione dei file. Questo SDK può essere usato per scrivere file superiori a 2 gigabyte, consentendo file continui più lunghi e di migliore qualità.
-   Supporto per la lettura dei file ASF. Questo SDK fornisce il supporto per la lettura di file ASF locali e la lettura dei dati ASF trasmessi in rete. Viene inoltre fornito il supporto per molte funzionalità di lettura avanzate, ad esempio il supporto nativo per file MBR (Multiple Bit Rate), che contengono più flussi con lo stesso contenuto codificato a velocità in bit diverse. Il lettore seleziona automaticamente il flusso MBR da usare, a seconda della larghezza di banda disponibile al momento della riproduzione.
-   Supporto per la distribuzione di flussi ASF in rete. Questo SDK fornisce il supporto per la distribuzione di dati ASF tramite HTTP a computer remoti in una rete e anche per la distribuzione di dati direttamente a un server Windows Media remoto.
-   Supporto per la modifica dei metadati nei file ASF. Le informazioni su un file e il relativo contenuto vengono facilmente manipolate con questo SDK. Gli sviluppatori possono usare il solido sistema di attributi dei metadati inclusi nell'SDK o creare attributi personalizzati in base alle proprie esigenze.
-   Supporto per le applicazioni di modifica del contenuto. Questo SDK consente alle applicazioni di cercare punti all'interno di un file in base all'ora di presentazione e al fotogramma video. Inoltre, i file creati usando l'SDK Windows Media Format possono mantenere i timestamp nei formati usati nella produzione cinematografica e cinematografica.
-   Supporto per la lettura e la modifica dei metadati nei file MP3. Questo SDK offre supporto integrato per la lettura di file MP3 con gli stessi metodi usati per leggere i file ASF. Le applicazioni compilate con Windows Media Format SDK possono anche modificare gli attributi dei metadati nei file MP3 usando il supporto predefinito per i tag ID3 più comuni usati dagli autori di contenuti.
-   Supporto per la protezione Rights Management digitale. Questo SDK fornisce metodi per la lettura e la scrittura di file ASF e flussi di rete protetti da Digital Rights Management per impedire la riproduzione o la copia non autorizzata del contenuto.

Per scaricare Windows Media Format SDK, vedere la pagina [Windows Media Downloads](https://msdn.microsoft.com/windows/desktop/aa904949) nel sito Web Microsoft.

Questo documento descrive come sviluppare applicazioni multimediali digitali usando Windows Media Format SDK. È suddiviso nelle sezioni seguenti.

> [!Note]  
> Anche se questo documento contiene informazioni sulla versione più recente di Windows Media Format SDK, la maggior parte delle funzionalità descritte è supportata dalle versioni precedenti dell'SDK. Le pagine di riferimento per i metodi, le funzioni, le strutture e le enumerazioni di Windows Media Format SDK includono i requisiti di versione.

 



| Sezione                                                                                                          | Descrizione                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni su Windows Media Format SDK](about-the-windows-media-format-sdk.md)                                     | Vengono fornite informazioni generali e di base che è necessario conoscere prima di tentare di creare applicazioni.                                                                                  |
| [Guida per programmatori](programming-guide.md)                                                                       | Fornisce istruzioni dettagliate per l'esecuzione di varie attività, ad esempio la lettura, la scrittura e l'indicizzazione di file, la protezione dei file con digital Rights Management, lo streaming di dati ASF in rete e così via. |
| [Guida di riferimento alla programmazione](programming-reference.md)                                                               | Fornisce informazioni di riferimento per le interfacce, i metodi, le funzioni, le strutture, i tipi di enumerazione e le costanti Windows Media Format.                                                     |
| [Windows Interfacce codec audio e video multimediali](windows-media-audio-and-video-codec-interfaces--deprecated.md) | Fornisce istruzioni per l'uso diretto Windows codec video e audio multimediale.                                                                                           |
| [*Glossario*](wmformat-glossary.md)                                                                              | Definisce i termini usati nella documentazione di Windows Media Format SDK.                                                                                                                                    |



 

 

 




