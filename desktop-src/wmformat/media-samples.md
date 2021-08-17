---
title: Esempi di supporti (Windows Media Format 11 SDK)
description: Informazioni sugli esempi di supporti in Windows Media Format 11 SDK. Un esempio di supporto è un oggetto che contiene un elenco ordinato di zero o più buffer.
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows MEDIA Format SDK, esempi di supporti
- Windows MEDIA Format SDK,esempi
- Advanced Systems Format (ASF), esempi di supporti
- ASF (Advanced Systems Format), esempi multimediali
- Advanced Systems Format (ASF), esempi
- ASF (Advanced Systems Format), esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741641bfa326357114f5a02e81a32ac47691661f331355d91a2c3e187ad4233b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117654585"
---
# <a name="media-samples-windows-media-format-11-sdk"></a>Esempi di supporti (Windows Media Format 11 SDK)

Un campione multimediale, o campione, è un blocco di dati multimediali digitali. Un esempio è l'unità di base che viene manipolata dagli oggetti di lettura e scrittura di Windows Media Format SDK. Il contenuto di un singolo campione è determinato dal tipo di supporto associato all'esempio. Per i video, ogni esempio rappresenta un singolo fotogramma. Per l'audio, la quantità di dati in un singolo campione viene impostata nel profilo usato per creare il file ASF.

Gli esempi possono contenere dati non compressi o possono contenere dati compressi, nel qual caso sono detti *esempi di flusso.* Quando si crea un file ASF, si passano esempi al writer. Il writer coordina la compressione degli esempi con il codec appropriato e dispone i dati compressi nella sezione dei dati del file ASF. Durante la riproduzione, il lettore legge i dati compressi, decomprime i dati e fornisce i dati non compressi ricostruiti come campioni di output.

Tutti gli esempi usati da Windows Media Format SDK vengono incapsulati nell'oggetto buffer la cui memoria viene allocata automaticamente dai componenti di run-time dell'SDK. È anche possibile allocare buffer personalizzati, se necessario, usando le funzionalità avanzate del writer e del lettore.

**Nota** Il termine esempio viene usato in questo SDK per fare riferimento a un campione multimediale, non a un esempio audio. Nella codifica audio, un campione fa riferimento a un singolo valore audio codificato. In genere, la qualità dell'audio codificato viene specificata da un numero di campioni al secondo. Ad esempio, il suono di qualità CD viene registrato a 44.100 campioni al secondo. Questo valore è comunemente abbreviato con la notazione Hz, quindi 44.100 campioni al secondo sarebbero 44.100 Hz o 44,1 kHz.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](concepts.md)
</dt> <dt>

[**Interfaccia INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**Input, Flussi e output**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




