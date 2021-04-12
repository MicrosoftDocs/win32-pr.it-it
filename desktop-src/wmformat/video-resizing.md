---
title: Ridimensionamento video
description: Ridimensionamento video
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- Windows Media Format SDK, ridimensionamento video
- Windows Media Format SDK, ridimensionamento del video
- ASF (Advanced Systems Format), ridimensionamento video
- ASF (Advanced Systems Format), ridimensionamento video
- ASF (Advanced Systems Format), ridimensionamento del video
- ASF (Advanced Systems Format), ridimensionamento del video
- ridimensionamento video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200496b1dead3abacfbfad7674519e0cf7ce4f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221208"
---
# <a name="video-resizing"></a>Ridimensionamento video

Quando si definiscono le impostazioni per un flusso video, è necessario specificare una larghezza e un'altezza per i fotogrammi video. Questa dimensione video determina la dimensione dei fotogrammi video codificati nella sezione dati del file. Tuttavia, le dimensioni del video in un profilo non determinano, o limitano, le dimensioni del supporto di input recapitato al writer o la dimensione del supporto di output ricevuto dal lettore. Il writer può ridimensionare i fotogrammi video in base alle esigenze dell'applicazione.

Le dimensioni dell'immagine video possono essere considerate come in tre fasi: dimensioni del video di input, dimensioni del video di flusso e dimensioni del video di output.

Dimensioni video di input è la dimensione dei frame passati come campioni all'oggetto writer. Queste dimensioni vengono definite come una delle proprietà di input video obbligatorie. Per ulteriori informazioni sulle proprietà di input, vedere [per enumerare i formati di input](to-enumerate-input-formats.md).

Dimensioni video flusso corrisponde alla dimensione dei frame nella sezione dati del file ASF. Queste dimensioni vengono definite come una delle impostazioni di configurazione del flusso necessarie nel profilo. Se si scrive un file e le dimensioni del video di input sono diverse dalle dimensioni del video del flusso, il writer ridimensiona i frame durante la codifica. Per ulteriori informazioni sulle proprietà del flusso video, vedere [Configuring video](configuring-video-streams.md)Streams.

Dimensioni video di output corrisponde alla dimensione dei frame recapitati dal lettore o dal lettore sincrono. Queste dimensioni vengono definite come una delle proprietà di output video obbligatorie. Se si legge un file e le dimensioni del video di output sono diverse dalla dimensione del video del flusso, il lettore ridimensiona i frame durante la decodifica.

Non è possibile impostare una dimensione del video del flusso su un numero dispari di pixel in larghezza. Se si imposta la larghezza di un flusso video su un valore dispari, il profilo non verrà accettato dal writer oppure il video risultante verrà codificato con una linea nera verso il basso di una parte per compensare la differenza.

È necessario prestare attenzione durante il ridimensionamento del video. Le immagini tendono a essere più adatte alla soluzione originale. Le immagini di ridimensionamento possono spesso provocare distorsioni e rendere il testo illeggibile. Se si comprime il video a una velocità in bit bassa, si noterà anche che le distorsioni di ridimensionamento possono causare artefatti di compressione gravi.

Il codec della schermata Windows Media Video 9 non supporta il ridimensionamento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di scrittura di file**](file-writing-features.md)
</dt> <dt>

[**Utilizzo degli input**](working-with-inputs.md)
</dt> <dt>

[**Uso degli output**](working-with-outputs.md)
</dt> </dl>

 

 




