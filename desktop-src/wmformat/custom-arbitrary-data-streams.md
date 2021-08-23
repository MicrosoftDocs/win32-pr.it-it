---
title: Dati arbitrari personalizzati Flussi
description: Dati arbitrari personalizzati Flussi
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- Windows Media Format SDK, flussi di dati arbitrari personalizzati
- Advanced Systems Format (ASF), flussi di dati arbitrari personalizzati
- ASF (Advanced Systems Format), flussi di dati arbitrari personalizzati
- Windows MEDIA Format SDK, flussi
- Advanced Systems Format (ASF), streams
- ASF (Advanced Systems Format), flussi
- flussi di dati arbitrari personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde40c7283620aba9c0bbdd0a1b376538ce7e4f22ac12e9fcdfe78d75195a516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027939"
---
# <a name="custom-arbitrary-data-streams"></a>Dati arbitrari personalizzati Flussi

È possibile creare un flusso in un file ASF per contenere qualsiasi tipo di dati. Se nessuno dei tipi di flusso supportati soddisfa le proprie esigenze, è necessario usare un flusso di dati arbitrario. L'oggetto writer gestisce un flusso di dati arbitrario esattamente come qualsiasi flusso non compresso. Gli esempi vengono pacchettizzati e combinati con gli esempi di altri flussi nella sezione dei dati del file. Naturalmente, solo un'applicazione di lettura programmata in modo specifico per gestire il tipo arbitrario sarà in grado di gestire i dati dopo che sono stati recapitati dall'oggetto di lettura.

Un uso comune di flussi di dati arbitrari è per i dati multimediali codificati tramite un codec di terze parti. Poiché gli oggetti di questo SDK non interagiscono direttamente con codec di terze parti, l'applicazione di scrittura deve elaborare gli esempi con la parte di codifica del codec e passare gli esempi compressi al writer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Elementi Flussi**](arbitrary-streams.md)
</dt> <dt>

[**Configurazione di modelli arbitrari personalizzati Flussi**](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




