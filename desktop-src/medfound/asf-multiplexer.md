---
description: Multiplexer ASF
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: Multiplexer ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362a1e0be72e8bc516e37ec83c36446177816f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049327"
---
# <a name="asf-multiplexer"></a>Multiplexer ASF

Il *multiplexing* ASF è un oggetto livello WMContainer che funziona con l' [oggetto dati ASF](asf-file-structure.md) e fornisce a un'applicazione la possibilità di generare pacchetti di dati per un contenitore ASF. Il multiplexer accetta dati multimediali sotto forma di [esempi di supporti](media-samples.md) e genera esempi di supporti basati sui parametri dei pacchetti ASF e di streaming definiti nell' [oggetto intestazione ASF](asf-file-structure.md). Gli esempi di supporti di output contengono riferimenti a uno o più buffer multimediali contenenti dati multimediali digitali in pacchetto. È possibile utilizzare questo oggetto in uno scenario di codifica dei file in cui vengono ricevuti esempi di flusso codificati dal codificatore o per la transcodifica ASF-ASF (remuxing).

Il diagramma seguente illustra la generazione di pacchetti di dati ASF per un file ASF usando multiplexer.

![diagramma che mostra la generazione di pacchetti di dati ASF](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

Per informazioni sulla struttura di un file ASF, vedere la pagina relativa alla [struttura dei file ASF](asf-file-structure.md).

Questa sezione contiene i seguenti argomenti:



| Argomento                                                                  | Descrizione                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Creazione dell'oggetto multiplexer](creating-the-multiplexer-object.md) | Come creare e inizializzare il multiplexer.                     |
| [Generazione di nuovi pacchetti di dati ASF](generating-new-asf-data-packets.md) | Come generare pacchetti di dati per costituire un nuovo oggetto dati ASF. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti ASF WMContainer](wmcontainer-asf-components.md)
</dt> <dt>

[Esercitazione: copia di flussi ASF da un file a un altro](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Esercitazione: scrittura di un file WMA usando la codifica CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



