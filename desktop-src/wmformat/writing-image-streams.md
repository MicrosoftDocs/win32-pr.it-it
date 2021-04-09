---
title: Scrittura di flussi di immagini
description: Scrittura di flussi di immagini
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- Formato di sistemi avanzati (ASF), scrittura di flussi di immagini
- ASF (Advanced Systems Format), scrittura di flussi di immagini
- Formati di sistemi avanzati (ASF), flussi di immagini
- ASF (formato avanzato dei sistemi), flussi di immagini
- flussi di immagini, scrittura
- flussi, scrittura di flussi di immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60daa9b62701c172d127c4cff1fb6c301edf7d86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956192"
---
# <a name="writing-image-streams"></a>Scrittura di flussi di immagini

Gli input per un flusso di immagini devono essere immagini bitmap in formato RGB. Il writer coordina la compressione degli esempi di immagini di input usando il formato JPEG. Prima di iniziare a scrivere un file contenente un flusso di immagini, è necessario impostare la qualità dell'immagine per l'input usando l' \_ impostazione g wszJPEGCompressionQuality. Usare [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) per impostare la qualità su un valore **DWORD** compreso tra 1 e 100. I valori bassi rappresentano un rapporto di compressione elevato a scapito della qualità, mentre i valori elevati producono immagini di alta qualità che richiedono più spazio.

I flussi di immagini spesso richiedono finestre di buffer più grandi rispetto ai flussi video comuni. La dimensione esatta richiesta dipende dal tipo di immagine e dalla qualità dell'immagine, tra gli altri fattori. Utilizzare la versione di valutazione e l'errore per determinare le dimensioni appropriate per le immagini che si desidera elaborare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Flussi di immagini**](image-streams.md)
</dt> <dt>

[**Per impostare le impostazioni di input**](to-set-input-settings.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




