---
title: Flussi di dati arbitrari personalizzati
description: Flussi di dati arbitrari personalizzati
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- Windows Media Format SDK, flussi di dati arbitrari personalizzati
- Formati di sistemi avanzati (ASF), flussi di dati arbitrari personalizzati
- ASF (Advanced Systems Format), flussi di dati arbitrari personalizzati
- Windows Media Format SDK, flussi
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- flussi di dati arbitrari personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c031e6d02864cae326a9cadb48577e1ea76c0e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298919"
---
# <a name="custom-arbitrary-data-streams"></a>Flussi di dati arbitrari personalizzati

È possibile creare un flusso in un file ASF per contenere qualsiasi tipo di dati. Se nessuno dei tipi di flusso supportati è adatto alle proprie esigenze, è necessario usare un flusso di dati arbitrari. L'oggetto writer gestisce un flusso di dati arbitrari Analogamente a qualsiasi flusso non compresso. gli esempi sono disponibili in pacchetti e combinati con gli esempi di altri flussi nella sezione dati del file. Naturalmente, solo un'applicazione di lettura che è stata programmata in modo specifico per gestire il tipo arbitrario sarà in grado di gestire i dati dopo che sono stati recapitati dall'oggetto di lettura.

Un uso comune di flussi di dati arbitrari è per i dati multimediali codificati usando un codec di terze parti. Poiché gli oggetti di questo SDK non interagiscono direttamente con i codec di terze parti, l'applicazione di scrittura deve elaborare gli esempi con la parte di codifica del codec e passare gli esempi compressi al writer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Flussi arbitrari**](arbitrary-streams.md)
</dt> <dt>

[**Configurazione di flussi arbitrari personalizzati**](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




