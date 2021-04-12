---
title: Lettura di file ASF
description: Lettura di file ASF
ms.assetid: e0aabe05-b317-42ac-85fc-5a75165722d4
keywords:
- Windows Media Format SDK, lettura di file ASF
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Formato di sistemi avanzati (ASF), lettura di file
- ASF (Advanced Systems Format), lettura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f35cbd0e9a7dde800e23f83337ac30cdd66582
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331935"
---
# <a name="reading-asf-files"></a>Lettura di file ASF

Windows Media Format SDK può essere usato per distribuire esempi di supporti da un file ASF. Due oggetti vengono utilizzati per recuperare gli esempi, l'oggetto Reader e l'oggetto Reader sincrono.

L'oggetto Reader è l'oggetto di lettura originale in Windows Media Format SDK. L'oggetto Reader usa un'architettura asincrona per eseguire il push degli esempi in un'applicazione. Le applicazioni compilate utilizzando l'oggetto Reader devono implementare funzioni di callback che rispondono ai vari messaggi ed eventi risultanti da questo modello multithread. Per maggiore chiarezza, in questa sezione verrà fatto riferimento all'oggetto Reader come lettore asincrono.

L'oggetto Reader sincrono è una novità di questa versione di Windows Media Format SDK. Il lettore sincrono non utilizza più thread nell'elaborazione di esempi da file ASF. Un'applicazione compilata utilizzando il lettore sincrono recupera esempi su richiesta, anziché attendere che il lettore li invii.

Quando si crea un'applicazione per leggere i file ASF, è necessario scegliere l'oggetto Reader da usare. In generale, le applicazioni progettate per fornire contenuti basati su Windows Media devono essere create utilizzando il lettore asincrono, mentre le applicazioni progettate per modificare i file ASF devono essere create con il lettore sincrono.

Nella tabella seguente sono elencate le principali funzionalità di entrambi gli oggetti Reader. Usare questa tabella per determinare l'oggetto da usare per l'applicazione.



| Funzionalità                                                                    | Lettore asincrono | Lettore di sincronizzazione |
|----------------------------------------------------------------------------|--------------|-------------|
| Leggi campioni non compressi per numero di output                                 | Sì          | Sì         |
| Leggere esempi compressi per numero di flusso                                   | Sì          | Sì         |
| Leggi esempi non compressi per numero di flusso                                 | No           | Sì         |
| Leggi da sito Internet                                                    | Sì          | No          |
| Lettura dei metadati                                                              | Sì          | Sì         |
| Cerca in fase di presentazione                                                  | Sì          | Sì         |
| Cerca al frame                                                              | Sì          | Sì         |
| Cerca marcatore                                                             | Sì          | No          |
| Passa tra il recapito di esempio compresso e non compresso durante la riproduzione | No           | Sì         |
| Apri file con l'interfaccia **IStream**                                     | Sì          | Sì         |



 

Nelle sezioni seguenti vengono fornite ulteriori informazioni sull'utilizzo dei due oggetti Reader.



| Sezione                                                                                      | Descrizione                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Uso degli output](working-with-outputs.md)                                             | Viene descritto come utilizzare e modificare gli output. Si applica a entrambi gli oggetti Reader.                                                            |
| [Allocazione di buffer per la lettura di file](allocating-buffers-for-file-reading.md)               | Viene descritto come utilizzare il proprio pool di buffer per conservare gli esempi recapitati dal lettore o dal lettore sincrono.                            |
| [Lettura dei metadati durante la riproduzione](reading-metadata-at-playback.md)                             | Viene descritto come sfruttare i vantaggi del supporto dei metadati durante la riproduzione. Si applica a entrambi gli oggetti Reader.                                        |
| [Recupero delle informazioni sul profilo durante la riproduzione](getting-profile-information-at-playback.md)       | Viene descritto come accedere alle informazioni sul profilo per i file aperti. Si applica a entrambi gli oggetti Reader.                                           |
| [Lettura dell'audio multicanale](reading-multichannel-audio.md)                                 | Viene descritto come configurare il writer per la decodifica corretta dell'audio multicanale.                                                            |
| [Rendering del contenuto](rendering-content.md)                                                   | Vengono illustrati i problemi correlati al rendering di esempi non compressi. Si applica a entrambi gli oggetti Reader.                                         |
| [Ottenere le migliori prestazioni di ricerca video](getting-the-best-video-seeking-performance.md) | Descrive i modi per migliorare le prestazioni di ricerca dei video.                                                                                    |
| [Lettura di file con il lettore asincrono](reading-files-with-the-asynchronous-reader.md) | Viene descritto come leggere i file ASF utilizzando l'oggetto Reader asincrono.                                                                   |
| [Lettura di file con il lettore sincrono](reading-files-with-the-synchronous-reader.md)   | Viene descritto come leggere i file ASF utilizzando l'oggetto Reader sincrono.                                                                    |
| [Attivazione dell'accelerazione video DirectX](enabling-directx-video-acceleration.md)               | Viene descritto come implementare l'accelerazione video DirectX per usare le funzionalità di accelerazione hardware di alcune schede video per la decodifica del video. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> <dt>

[**Oggetto Lettore**](reader-object.md)
</dt> <dt>

[**Oggetto lettore sincrono**](synchronous-reader-object.md)
</dt> </dl>

 

 




