---
title: Lettura di file ASF
description: Lettura di file ASF
ms.assetid: e0aabe05-b317-42ac-85fc-5a75165722d4
keywords:
- Windows Media Format SDK,lettura di file ASF
- Windows Media Format SDK,Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), lettura di file
- ASF (Advanced Systems Format), lettura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01f417cafad4e125c6c176ac35e95ff3ab8f08c4f600b811865a9fb6ae51362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197519"
---
# <a name="reading-asf-files"></a>Lettura di file ASF

L Windows Media Format SDK può essere usato per distribuire esempi multimediali da un file ASF. Vengono usati due oggetti per recuperare gli esempi, l'oggetto reader e l'oggetto lettore sincrono.

L'oggetto lettore è l'oggetto di lettura originale in Windows Media Format SDK. L'oggetto reader usa un'architettura asincrona per eseguire il push di esempi in un'applicazione. Le applicazioni compilate usando l'oggetto reader devono implementare funzioni di callback che rispondono ai vari messaggi ed eventi risultati da questo modello multi-thread. Per maggiore chiarezza, questa sezione farà riferimento all'oggetto reader come lettore asincrono.

L'oggetto lettore sincrono è una novità per questa versione di Windows Media Format SDK. Il lettore sincrono non usa più thread nell'elaborazione di esempi da file ASF. Un'applicazione compilata usando il lettore sincrono recupera gli esempi su richiesta, anziché attendere che il lettore li invii.

Quando si crea un'applicazione per leggere i file ASF, è necessario scegliere l'oggetto lettore da usare. In generale, le applicazioni progettate per distribuire Windows contenuto basato su supporti devono essere create usando il lettore asincrono, mentre le applicazioni progettate per modificare i file ASF devono essere create con il lettore sincrono.

Nella tabella seguente sono elencate le principali funzionalità di entrambi gli oggetti reader. Usare questa tabella per determinare l'oggetto da usare per l'applicazione.



| Funzionalità                                                                    | Lettore asincrono | Lettore di sincronizzazione |
|----------------------------------------------------------------------------|--------------|-------------|
| Leggere gli esempi non compressi in base al numero di output                                 | Sì          | Sì         |
| Leggere gli esempi compressi in base al numero di flusso                                   | Sì          | Sì         |
| Leggere gli esempi non compressi in base al numero di flusso                                 | No           | Sì         |
| Leggere dal sito Internet                                                    | Sì          | No          |
| Leggere i metadati                                                              | Sì          | Sì         |
| Cercare l'ora di presentazione                                                  | Sì          | Sì         |
| Cercare di incorniciare                                                              | Sì          | Sì         |
| Cerca nel marcatore                                                             | Sì          | No          |
| Passare dal recapito dei campioni compresso a quello non compresso durante la riproduzione | No           | Sì         |
| Aprire file con **l'interfaccia IStream**                                     | Sì          | Sì         |



 

Le sezioni seguenti forniscono altre informazioni sull'uso dei due oggetti reader.



| Sezione                                                                                      | Descrizione                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Uso degli output](working-with-outputs.md)                                             | Viene descritto come usare e modificare gli output. Si applica a entrambi gli oggetti reader.                                                            |
| [Allocazione di buffer per la lettura di file](allocating-buffers-for-file-reading.md)               | Descrive come usare il proprio pool di buffer per contenere gli esempi forniti dal lettore o dal lettore sincrono.                            |
| [Lettura dei metadati in fase di riproduzione](reading-metadata-at-playback.md)                             | Viene descritto come sfruttare il supporto dei metadati in fase di riproduzione. Si applica a entrambi gli oggetti reader.                                        |
| [Recupero delle informazioni del profilo durante la riproduzione](getting-profile-information-at-playback.md)       | Viene descritto come accedere alle informazioni del profilo per i file aperti. Si applica a entrambi gli oggetti reader.                                           |
| [Lettura dell'audio multicanale](reading-multichannel-audio.md)                                 | Viene descritto come configurare il writer per decodificare correttamente l'audio multicanale.                                                            |
| [Rendering del contenuto](rendering-content.md)                                                   | Vengono illustrati i problemi relativi al rendering di esempi non compressi. Si applica a entrambi gli oggetti reader.                                         |
| [Ottenere le migliori prestazioni di ricerca di video](getting-the-best-video-seeking-performance.md) | Descrive i modi per migliorare le prestazioni di ricerca video.                                                                                    |
| [Lettura di file con il lettore asincrono](reading-files-with-the-asynchronous-reader.md) | Viene descritto come leggere i file ASF usando l'oggetto lettore asincrono.                                                                   |
| [Lettura di file con il lettore sincrono](reading-files-with-the-synchronous-reader.md)   | Viene descritto come leggere i file ASF usando l'oggetto lettore sincrono.                                                                    |
| [Abilitazione dell'accelerazione video DirectX](enabling-directx-video-acceleration.md)               | Descrive come implementare l'accelerazione video DirectX per usare le funzionalità di accelerazione hardware di alcune schede video per la decodifica video. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> <dt>

[**Oggetto Lettore**](reader-object.md)
</dt> <dt>

[**Oggetto lettore sincrono**](synchronous-reader-object.md)
</dt> </dl>

 

 




