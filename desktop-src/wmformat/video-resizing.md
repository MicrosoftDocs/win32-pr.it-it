---
title: Ridimensionamento video
description: Ridimensionamento video
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- Windows MEDIA Format SDK, ridimensionamento video
- Windows Media Format SDK, ridimensionamento di video
- Advanced Systems Format (ASF), ridimensionamento video
- ASF (Advanced Systems Format), ridimensionamento video
- Advanced Systems Format (ASF), ridimensionamento video
- ASF (Advanced Systems Format), ridimensionamento video
- ridimensionamento video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a3261b5b78b386a0589e2e5554b52793d478f052765cb9caa63cf7e399d90e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027189"
---
# <a name="video-resizing"></a>Ridimensionamento video

Quando si definiscono le impostazioni per un flusso video, è necessario specificare una larghezza e un'altezza per i fotogrammi video. Le dimensioni del video determinano le dimensioni dei fotogrammi video codificati nella sezione dei dati del file. Tuttavia, le dimensioni del video in un profilo non determinano o limitano le dimensioni del supporto di input recapitato al writer o le dimensioni del supporto di output ricevuto dal lettore. Lo scrittore può ridimensionare i fotogrammi video in base alle esigenze dell'applicazione.

Le dimensioni dell'immagine video possono essere pensate come attraversate da tre fasi: dimensioni del video di input, dimensioni del video di flusso e dimensioni del video di output.

Le dimensioni del video di input sono le dimensioni dei fotogrammi passati come esempi all'oggetto writer. Queste dimensioni vengono definite come una delle proprietà di input video necessarie. Per altre informazioni sulle proprietà di input, vedere [Per enumerare i formati di input.](to-enumerate-input-formats.md)

Le dimensioni del video di flusso sono le dimensioni dei fotogrammi nella sezione dei dati del file ASF. Queste dimensioni vengono definite come una delle impostazioni di configurazione del flusso necessarie nel profilo. Se si scrive un file e le dimensioni del video di input sono diverse dalle dimensioni del video di flusso, il writer ridimensiona i fotogrammi durante la codifica. Per altre informazioni sulle proprietà del flusso video, vedere [Configuring Video Flussi](configuring-video-streams.md).

Le dimensioni del video di output sono le dimensioni dei fotogrammi recapitati dal lettore o dal lettore sincrono. Queste dimensioni vengono definite come una delle proprietà di output video necessarie. Se si legge un file e le dimensioni del video di output sono diverse dalle dimensioni del video di flusso, il lettore ridimensiona i fotogrammi durante la decodifica.

Non è possibile impostare le dimensioni di un video di flusso su un numero dispari di pixel di larghezza. Se si imposta la larghezza di un flusso video su un valore dispari, il profilo non verrà accettato dal writer o il video risultante verrà codificato con una linea nera verso il basso di un lato per fare la differenza.

È consigliabile fare attenzione quando si ridimensiona il video. Le immagini tendono a guardare al meglio la risoluzione originale. Il ridimensionamento delle immagini spesso può causare distorsioni e rendere il testo illeggibile. Se si comprime il video a una velocità in bit bassa, si scoprirà anche che il ridimensionamento delle distorsioni può causare artefatti di compressione gravi.

Il codec Windows Media Video 9 Screen non supporta il ridimensionamento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di scrittura di file**](file-writing-features.md)
</dt> <dt>

[**Uso degli input**](working-with-inputs.md)
</dt> <dt>

[**Uso degli output**](working-with-outputs.md)
</dt> </dl>

 

 




