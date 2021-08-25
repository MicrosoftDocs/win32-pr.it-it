---
title: Scrittura di immagini Flussi
description: Scrittura di immagini Flussi
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- Advanced Systems Format (ASF), scrittura di flussi di immagini
- ASF (Advanced Systems Format), scrittura di flussi di immagini
- Advanced Systems Format (ASF), flussi di immagini
- ASF (Advanced Systems Format), flussi di immagini
- flussi di immagini, scrittura
- flussi, scrittura di flussi di immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6061af2ff43cbeb3fe688b6533eee044036df029bdb7f7305af305c8d45084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006301"
---
# <a name="writing-image-streams"></a>Scrittura di immagini Flussi

Gli input per un flusso di immagini devono essere immagini bitmap in formato RGB. Il writer coordina la compressione degli esempi di immagini di input usando il formato JPEG. Prima di iniziare a scrivere un file contenente un flusso di immagini, è necessario impostare una qualità dell'immagine per l'input, usando l'impostazione \_ g wszJPEGCompressionQuality. Usare [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) per impostare la qualità su un valore **DWORD** compreso tra 1 e 100. I valori bassi rappresentano un rapporto di compressione elevato a scapito della qualità, mentre valori elevati producono immagini di alta qualità che richiedono più spazio.

I flussi di immagini richiedono spesso finestre del buffer più grandi rispetto ai normali flussi video. La dimensione esatta richiesta dipende, tra gli altri fattori, dal tipo di immagine e dalla qualità dell'immagine. Usare la versione di valutazione e l'errore per determinare le dimensioni appropriate per le immagini che si intende elaborare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Immagine Flussi**](image-streams.md)
</dt> <dt>

[**Per impostare i valori di Impostazioni**](to-set-input-settings.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




