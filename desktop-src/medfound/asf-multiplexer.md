---
description: ASF Multiplexer
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: ASF Multiplexer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e1577f005004dbbe6bbb27e1ce7af346e56e134aff2b3201f5670175b015c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035564"
---
# <a name="asf-multiplexer"></a>ASF Multiplexer

Il *multiplexer* ASF è un oggetto livello WMContainer che funziona con l'oggetto dati [ASF](asf-file-structure.md) e offre a un'applicazione la possibilità di generare pacchetti di dati per un contenitore ASF. Il multiplexer accetta dati multimediali [](media-samples.md) sotto forma di campioni multimediali e restituisce campioni multimediali in base ai parametri di streaming e di pacchetto ASF definiti nell'oggetto intestazione [ASF](asf-file-structure.md). Gli esempi di supporti di output contengono riferimenti a uno o più buffer multimediali contenenti dati multimediali digitali in pacchetto. È possibile usare questo oggetto in uno scenario di codifica file in cui riceve esempi di flussi codificati dal codificatore o per la transcodificare ASF-ASF (remuxing).

Il diagramma seguente illustra la generazione di pacchetti di dati ASF per un file ASF usando il multiplexer.

![Diagramma che mostra la generazione di pacchetti di dati asf](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

Per informazioni sulla struttura di un file ASF, vedere [Struttura del file ASF.](asf-file-structure.md)

Questa sezione contiene i seguenti argomenti:



| Argomento                                                                  | Descrizione                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Creazione dell'oggetto Multiplexer](creating-the-multiplexer-object.md) | Come creare e inizializzare il multiplexer.                     |
| [Generazione di nuovi pacchetti di dati ASF](generating-new-asf-data-packets.md) | Come generare pacchetti di dati per costituire un nuovo oggetto dati ASF. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti ASF WMContainer](wmcontainer-asf-components.md)
</dt> <dt>

[Esercitazione: Copia di file ASF Flussi da un file a un altro](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Esercitazione: Scrittura di un file WMA usando la codifica CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



